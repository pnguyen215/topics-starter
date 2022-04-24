## :tada: Git

### Commit Message Style
A commit messages consists of three distinct parts separated by a blank line: the title, an optional body and an optional footer. The layout looks like this

```cmd
:emoji:  type: Subject

body

footer
```

##### The Type
The type is contained within the title and can be one of these types:

- **feat**: A new feature
- **fix**: A bug fix
- **docs**: Changes to documentation
- **style**: Formatting, missing semi colons, etc; no code change
- **refactor**: Refactoring production code
- **test**: Adding tests, refactoring test; no production code change
- **chore**: Updating build tasks, package manager configs, etc,... no production code change

##### The Subject
1. Subjects should be no greater than 50 characters, should begin with a capital letter and do not end with a period.
2. Use an imperative tone to describe what a commit does, rather than what it did. For example, use change; not changed or changes.

##### The Body
1. Not all commits are complex enough to warrant a body, therefore it is optional and only used when a commit requires a bit of explanation and context. Use the body to explain the what and why of a commit, not the how.
2. When writing a body, the blank line between the title and the body is required and you should limit the length of each line to no more than 72 characters.


##### The Footer
The footer is optional and is used to reference issue tracker IDs.


### Example Commit Message


```cmd
✨ :feat: Summarize changes in around 50 characters or less

More detailed explanatory text, if necessary. Wrap it to about 72
characters or so. In some contexts, the first line is treated as the
subject of the commit and the rest of the text as the body. The
blank line separating the summary from the body is critical (unless
you omit the body entirely); various tools like `log`, `shortlog`
and `rebase` can get confused if you run the two together.

Explain the problem that this commit is solving. Focus on why you
are making this change as opposed to how (the code explains that).
Are there side effects or other unintuitive consequences of this
change? Here's the place to explain them.

Further paragraphs come after blank lines.

 - Bullet points are okay, too

 - Typically a hyphen or asterisk is used for the bullet, preceded
   by a single space, with blank lines in between, but conventions
   vary here

If you use an issue tracker, put references to them at the bottom,
like this:

Resolves: #123
See also: #456, #789
```


### Emojis
#### Status / Warnings


 |        Image        | GFM short code        | When to use it                                                          |
 | :-----------------: | :-------------------- | :---------------------------------------------------------------------- |
 |       :tada:        | `:tada:`              | Initial (new) commit                                                    |
 |   :construction:    | `:construction:`      | Work in progress / when the change is a work in progress (do not merge) |
 |     :ambulance:     | `:ambulance:`         | Critical hotfix                                                         |
 |     :sparkles:      | `:sparkles:`          | Introducing new features                                                |
 |       :beers:       | `:beers:`             | Writing code drunkenly                                                  |
 |      :hankey:       | `:hankey:`            | Writing bad code that needs to be improved                              |
 |  :rotating_light:   | `:rotating_light:`    | Removing linter warnings                                                |
 |      :rewind:       | `:rewind:`            | Reverting changes                                                       |
 |      :alembic:      | `:alembic:`           | Experimenting new things                                                |
 |       :lock:        | `:lock:`              | Fixing security issues                                                  |
 |        :zap:        | `:zap:`               | Improving performance / when making a backwards-incompatible change     |
 | :children_crossing: | `:children_crossing:` | Improving user experience / usability                                   |
 |        :bug:        | `:bug:`               | Fixing a bug                                                            |


 #### Documentation
 

  |         Image         | GFM short code          | When to use it                            |
  | :-------------------: | :---------------------- | :---------------------------------------- |
  |        :memo:         | `:memo:`                | Writing docs (e.g. README, code comments) |
  |        :bulb:         | `:bulb:`                | Documenting source code                   |
  |         :mag:         | `:mag:`                 | Improving SEO                             |
  | :busts_in_silhouette: | `:busts_in_silhouette:` | Adding contributor(s)                     |
  |        :book:         | `:book:`                | Issue                                     |


  #### Testing


  |       Image        | GFM short code       | When to use it                           |
  | :----------------: | :------------------- | :--------------------------------------- |
  | :white_check_mark: | `:white_check_mark:` | Updating tests                           |
  |     :ok_hand:      | `:ok_hand:`          | Updating code due to code review changes |
  |    :clown_face:    | `:clown_face:`       | Mocking things                           |
  |  :crossed_flags:   | `:crossed_flags:`    | when adding an A/B test or feature flag  |


  #### Dependency management


|       Image        | GFM short code       | When to use it                                       |
| :----------------: | :------------------- | :--------------------------------------------------- |
|       :boom:       | `:boom:`             | Introducing breaking changes  /  when fixing a crash |
|    :arrow_down:    | `:arrow_down:`       | Downgrading dependencies                             |
|     :arrow_up:     | `:arrow_up:`         | Upgrading dependencies                               |
|     :pushpin:      | `:pushpin:`          | Pinning dependencies to specific versions            |
| :heavy_plus_sign:  | `:heavy_plus_sign:`  | Adding a dependency                                  |
| :heavy_minus_sign: | `:heavy_minus_sign:` | Removing a dependency                                |


#### Coding Content


|           Image            | GFM short code               | When to use it                              |
| :------------------------: | :--------------------------- | :------------------------------------------ |
|  :building_construction:   | `:building_construction:`    | Making architectural changes                |
|           :fire:           | `:fire:`                     | Removing code or files                      |
|         :pencil2:          | `:pencil2:`                  | Fixing typos                                |
|        :loud_sound:        | `:loud_sound:`               | Adding logs                                 |
|           :mute:           | `:mute:`                     | Removing  logs                              |
|           :art:            | `:art:`                      | Improving structure / format of the code    |
|         :recycle:          | `:recycle:`                  | Refactoring code logic                      |
|   :construction_worker:    | `:construction_worker:`      | Adding CI build system                      |
|          :rocket:          | `:rocket:`                   | Deploying stuff / when improving dev tools  |
|         :bookmark:         | `:bookmark:`                 | Releasing / Version tags                    |
|      :speech_balloon:      | `:speech_balloon:`           | Updating text and literals                  |
| :chart_with_upwards_trend: | `:chart_with_upwards_trend:` | Adding analytics or tracking code           |
|     :wheel_of_dharma:      | `:wheel_of_dharma:`          | Work about Kubernetes                       |
|   :globe_with_meridians:   | `:globe_with_meridians:`     | Internationalization and localization       |
|           :egg:            | `:egg:`                      | Adding an easter egg                        |
|          :label:           | `:label:`                    | Adding or updating types (Flow, TypeScript) |
|      :card_file_box:       | `:card_file_box:`            | Performing database related changes         |
|        :wheelchair:        | `:wheelchair:`               | Improving accessibility                     |
|         :lipstick:         | `:lipstick:`                 | Updating the UI and style files             |
|           :gem:            | `:gem:`                      | when cutting a new release / version bump   |
|        :racehorse:         | `:racehorse:`                | when improving performance                  |
|    :non-potable_water:     | `:non-potable_water:`        | when fixing a memory leak                   |



#### Configuration / Metadata


|            Image            | GFM short code                | When to use it                                                           |
| :-------------------------: | :---------------------------- | :----------------------------------------------------------------------- |
|           :whale:           | `:whale:`                     | Work about Docker                                                        |
|        :green_heart:        | `:green_heart:`               | Fixing CI Build                                                          |
|          :wrench:           | `:wrench:`                    | Changing configuration files / when updating configs                     |
| :twisted_rightwards_arrows: | `:twisted_rightwards_arrows:` | Merging branches                                                         |
|          :package:          | `:package:`                   | Updating compiled files or packages / when refactoring or improving code |
|           :alien:           | `:alien:`                     | Updating code due to external API changes                                |
|           :truck:           | `:truck:`                     | Moving or renaming files                                                 |
|      :page_facing_up:       | `:page_facing_up:`            | Adding or updating license                                               |
|           :bento:           | `:bento:`                     | Adding or updating assets                                                |
|        :see_no_evil:        | `:see_no_evil:`               | Adding or updating a .gitignore file                                     |
|       :camera_flash:        | `:camera_flash:`              | Adding or updating snapshots                                             |
|          :iphone:           | `:iphone:`                    | Working on responsive design                                             |
|         :satellite:         | `:satellite:`                 | when adding instrumentation or metrics design                            |



#### Operating system specific


|      Image       | GFM short code     | When to use it              |
| :--------------: | :----------------- | :-------------------------- |
|  :green_apple:   | `:green_apple:`    | Fixing something on iOS     |
|     :apple:      | `:apple:`          | Fixing something on macOS   |
|    :penguin:     | `:penguin:`        | Fixing something on Linux   |
| :checkered_flag: | `:checkered_flag:` | Fixing something on Windows |
|     :robot:      | `:robot:`          | Fixing something on Android |



### Ref emojis

1. https://gist.github.com/rxaviers/7360908
2. https://wilsonmar.github.io/git-messages/