# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## 2.2.0

### Added
- Add support for changing the default urgency of a todo with `TODO.initial_urgency`
- Add support for changing urgency colors with `TODO.urgency1_color` to `TODO.urgency4_color`
- Add shortcut for recursively expanding and closing todos (Ctrl + Z)
- Add `WORKSPACE.start_expanded` and `TODO.start_expanded` to launch with the Workspace and Todo tree fully expanded
- Dooit can now also be launched with `python -m dooit`

### Fixed

- App crashes when an opened workspace is deleted (closes https://github.com/kraanzu/dooit/issues/169)
- App crash on adding a workspace (closes https://github.com/kraanzu/dooit/issues/167)

## 2.0.2

### Added
- Add `DATE_FORMAT` and `TIME_FORMAT` to allow users to customize due date https://github.com/kraanzu/dooit/issues/141 (Also [see this](https://github.com/kraanzu/dooit/wiki/Configuration#general))

## 2.0.1

### Added
- Add `USE_DAY_FIRST` settings to allow users to switch between day and month

### Fixed
- `Ctrl+q` did not exit the app (closes https://github.com/kraanzu/dooit/issues/140)


## 2.0.0

### Added
- Dooit now allows duplicate descriptions to be added(closes https://github.com/kraanzu/dooit/issues/113)
- Clear due date when selected (closes https://github.com/kraanzu/dooit/issues/111)
- Add support for h / l to switch between panes (closes https://github.com/kraanzu/dooit/issues/96)
- Add support for yank whole todos/workspaces (closes https://github.com/kraanzu/dooit/issues/76)
- Add support for `save on escape` (closes https://github.com/kraanzu/dooit/issues/106)
- Add support for opening and highlighting urls (closes https://github.com/kraanzu/dooit/issues/108)
- Add support for changing due date format (due/remaining time) (closes https://github.com/kraanzu/dooit/issues/116)

### Fixed
- Slowness due to un-necessary rendering of the app
- Slow loading of app because of dateparser (see https://github.com/kraanzu/dooit/issues/136)
- Text disappearing for non-alphabet characters in description(closes https://github.com/kraanzu/dooit/issues/112)
- Todos disappearing when wrapping descriptions with tags/quotes/brackets (closes https://github.com/kraanzu/dooit/issues/107)
- Use background color specified in config for help menu
- Bar did not pick color from config and used the regular background

### Breaking Changes
- Tags are now built-in within the description. They start with @ symbol (eg bring milk @chore)
- Todos are no longer stored in a todo.txt format yaml file. This shouldn't break anything and the new version will take care of that!

## 1.0.1

### Fixed
- File not found error on windows (closes https://github.com/kraanzu/dooit/issues/91)
- crash for python <= 3.10 (closes https://github.com/kraanzu/dooit/issues/99)

## 1.0.0

### Added 

- **A whole new API to interact with dooit** (closes https://github.com/kraanzu/dooit/issues/23)
- **Unlimited branching of todos and workspaces** (closes https://github.com/kraanzu/dooit/issues/85 and https://github.com/kraanzu/dooit/issues/70 and https://github.com/kraanzu/dooit/issues/58)
- **Smart node addition on <enter>**
  - Dooit now will not add an extra item automatically if you are just editing description of some node
- **Support for edit and addition in SEARCH mode**
  - Previously users were only allowed to jump to the todo
- **Synchronisation between multiple instances** 
  - Previously dooit printed a warning and exited with a message indicating that it's already running (closes https://github.com/kraanzu/dooit/issues/49)
- **New parameters for todos!**
  - **Recurrence** ==> Adds recurrence to todos for regular reminder!
  - **Effort** ==> An Integer Value to determine the effort/time it will take to complete the todo (for https://github.com/kraanzu/dooit/issues/74)
  - **Tags** ==> Add tags to todos
  - **Time** ==> Previously only date was supported (closes https://github.com/kraanzu/dooit/issues/66)
- **Better date&time parsing** 
  - Dooit now uses [dateparser](https://pypi.org/project/dateparser/) module to make it a lot easier to add and edit date&time (for https://github.com/kraanzu/dooit/issues/71)
- **Custiomizable Bar**
  - Dooit now has a bar that can be customized to your liking!
  - You can now use python scripts to display your desired content in the bar
  - You can also use dooit API to display info in status bars
- A better config parser which handles ovveriden case better! (closes https://github.com/kraanzu/dooit/issues/64)

### Fixed
  - Update textual which might fix several issues! (maybe closes https://github.com/kraanzu/dooit/issues/57 and https://github.com/kraanzu/dooit/issues/57)
  - Using '/' in todos crashes app (closes https://github.com/kraanzu/dooit/issues/84)
  

### Changed
  - Remove mouse support...coz why not? (closes https://github.com/kraanzu/dooit/issues/69)
  - Some keybindings
  - Unicode by default (remove nerd font icons from default config)
  - match-case stmts (Adds support for python>=3.7)
  
