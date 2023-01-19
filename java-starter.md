## :tada: Java
***

##### :pencil: Notes

- [x] **gradle bootJar**: using gradle dependencies to build application (example: Spring Boot Framework) (or *gradlew bootJar*)
- [x] **gradle jar**: using gradle dependencies to build file jar
- [x] **mvn clean build**: using maven dependencies to build application (example: Spring Boot Framework)

***

### Bash-script for application using Spring Boot Framework

`our program JAR package is /path/to/xxx.jar`

> start.sh: is the start script, which provides the path to Java, executes the start command of the JAR file, and outputs the information.

```sh
#!/bin/bash
export JAVA_HOME=/usr/java/jdk1.8.0_131
export PATH=$JAVA_HOME/bin:$PATH
APP_NAME=xxx
nohup java -jar /path/to/xxx.jar.jar > xxx.log 2>&1 &
echo "$APP_NAME is running"
```

> stop.sh: is a stop script, which finds the PID of the corresponding process of the program by using the ps command, if it doesn’t exist, the program is not running, so don’t do anything, if it exists, then kill it with the kill command.

```sh
#!/bin/bash
APP_NAME=xxx
pid=`ps -ef | grep $APP_NAME | grep -v grep | awk '{print $2}'`
  
if [ -z "${pid}" ]; then
   echo "$APP_NAME is not running"
else
    echo "kill thread...$pid"
    kill -9 $pid
fi
```

> restart.sh:  is a restart script, which is a combination of the above two, to terminate the program first, and then start it.

```sh
#!/bin/bash
export JAVA_HOME=/usr/java/jdk1.8.0_131
export PATH=$JAVA_HOME/bin:$PATH
APP_NAME=xxx
pid=`ps -ef | grep $APP_NAME | grep -v grep | awk '{print $2}'`
  
if [ -z "${pid}" ]; then
   echo "$APP_NAME is not running"
else
    echo "kill thread...$pid"
    kill -9 $pid
fi

nohup java -jar /path/to/xxx.jar > xxx.log 2>&1 &
echo "$APP_NAME is running"
```

> With these three scripts in the `/path/to/bin/` directory, we now configure the system service (assuming the service is named `xxx`). In the `/usr/lib/systemd/system/` directory, create the `xxx.service` file with the following contents.

```fallback
[Unit]
Description=xxx
After=syslog.target network.target remote-fs.target nss-lookup.target

[Service]
Type=forking
ExecStart=/path/to/bin/start.sh
ExecReload=/path/to/bin/restart.sh
ExecStop=/path/to/bin/stop.sh
PrivateTmp=true

[Install]
WantedBy=multi-user.target
```

In this file, there are three sections.

- Unit block contains the configuration describing the content and the startup order. After indicates that it starts after these services are started.
- The Service block configures the startup behavior, using the three previous script files as the scripts for starting, terminating, and restarting the services, respectively.
- Install block configures how to install this configuration file, `WantedBy=multi-user.target` means the Target where this service is located is `multi-user.target`

With this configuration file, the following commands can be used to operate this service.

```sh
# start xxx.service
systemctl start xxx
# stop xxx.service
systemctl stop xxx
# restart xxx.service
systemctl restart xxx
# checking status xxx.service
systemctl status xxx
# to have the xxx.service start with the system, simply execute the following command
systemctl enable xxx
# to un-boot xxx.service with the system, use the following command
systemctl disable xxx
```