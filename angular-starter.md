## :tada: Angular
***

##### :pencil: Notes

- [x] **'set_\*\*'**: fill by yourself
- [x] **-g**: stand for `global`
- [x] **--skipTests=true**: ignore create file test with extension <b>.spec.ts</b>
- [x] **--save**: is used to save the package required for the application to run (a new value in your `package.json` <b>dependencies</b>).
- [x] **--save-dev**: is used to save the package for development purpose (a new value in your `package.json` <b>devDependencies</b>).
- [x] **--style=scss**: set style use `scss` (`css/sass/...`) for project
- [x] **--o**: auto open browser
- [x] **--port**: run project on port. Example `--port 4202` ~ run on port 4202 
- [x] **--flat=true**: disable generate sub-folder object
- [x] **--module=app**: set object generated to specific module (_import object to module existed_). Example `--module=app` import to parent module `app.module.ts` (default)
- [x] **--export=true**: export object generated to reuse
- [x] **--createApplication="false"**: like `--create-application=false`, stops the creation of the initial app. It only creates the workspace.

***

### Install Angular CLI

```shell
npm install -g @angular/cli
```

### Upgrade Angular version latest

```shell
npm update @angular/cli @angular/core
```

### Uninstall Angular CLI

```shell
npm uninstall -g @angular/cli

npm cache clean
```

### Install Jquery into project Angular

```shell
npm install jquery --save
```

### How to generate new project ?

```shell
ng new 'set_name_project' --style=scss --skipTests=true
```

### How to run project?

```shell
ng serve --o --port 4201
```

### How to generate new `component`?

```shell
ng generate component 'set_name_component' --flat=true --skipTests=true
```


### How to generate new `module`?

```shell
ng generate module 'set_name_module' --flat=true --module=app
```

### How to generate new `routing`?

```shell
ng generate module 'set_name'-routing --flat=true --module=app
```

### How to generate new `service`? 

```shell
ng generate service 'set_name_service' --skipTests=true
```

### How to generate new `model` (class)?

> Will be generated file similar to: `sample.model.ts`

```shell
ng generate class 'set_name_model' --type=model --skipTests=true 
```

### How to generate new `directive`?

```shell
ng generate directive 'set_name_directive' --export=true --flat=false --module=app --skipTests=true
```

### How to generate new `pipe`?

```shell
ng generate pipe 'set_name_pipe' --export=true --flat=false --module=app --skipTests=true
```

### How to generate new `guard`?

```shell
ng generate guard 'set_name_guard' --skipTests=true
```

### How to generate new `interface`?

```shell
ng generate interface 'set_name_interface' --type=model --skipTests=true
```

### How to generate new `enum`?

```shell
ng generate enum 'set_name_enum'
```

### How to create the empty `workspace`?

```shell
ng new 'set_name_workspace' --createApplication="false" --style=scss --skipTests=true
```

### How to add new `project`(`application`) to `workspace`?

```shell
ng generate application 'set_name_project' --skipTests=true --style=scss
```

### How to run specific `project` from `workspace`?

```shell
ng serve --project='set_name_project' --o --port 4201
```

_or_

```shell
ng serve 'set_name_project' --o --port 4201
```

### How to build the app with specific `project` for Production or Development from `workspace`?

> Build prod

```shell
ng build --prod --project='set_name_project'
```

> Build dev

```shell
ng build --project='set_name_project'
```

### How to create new `library` from `workspace`?

```shell
ng generate library 'set_name_library' --skipTests=true --style=scss
```

### How to create a shared service/component/pipe/directive to `application` or `library` from `workspace`?

```shell
ng generate service 'set_name_service' --project='set_name_application_or_library'
```

