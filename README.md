# To Do 

To do app written in Node JS to practice Java Script.

## Problem Statement

Write a console based todo application which accept following command line arguments

| argument | shortcut | description                                                                          |
|----------|----------|--------------------------------------------------------------------------------------|
| --title  |          | Mandatory for add, edit, & remove. Title of to do.                                   |
| --desc   |          | Optional. Optional description of the to do                                          |
| --file   |          | Optional. File name to be saved. Default todo.json. .json extension is optional      |

It also need to support following commands

- add - Add new todo
- edit - Edit existing todo's description
- list - List all todo
- remove - remove given todo

## Example usage

```bash
node todo.js add --title Kapil --desc="Sharma"
ToDo added: {title: "Kapil", description: "Sharma" } in todo.json

node todo.js add --title="task 1" --desc "description 1"
ToDo added: { title: "Task 1", description: "description 1" } in todo.json

node todo.js add --title Kapil --desc="Sharma"
Error: ToDo (Kapil) already exists.

node todo.js add --title Kapil --desc="Sharma" --file names
ToDo added: {title: Kapil, description: Sharma } in names.json

node todo.js add --title="task 2" --desc "description 2" --file"names.json"
ToDo added: { title: "Task 2", description: "description 2" } in names.json

less todo.json
[{"title":"Kapil","description":"Sharma"},{"title":"task 1","description":"description 1"}]

less names.json
[{"title":"Kapil","description":"Sharma"},{"title":"task 2","description":"description 2"}]

node todo.js list
===================
Title | Description
------|------------
Kapil | Sharma
task 1 | description 1
===================

node todo.js list --file names.json
===================
Title | Description
------|------------
Kapil | Sharma
task 2 | description 2
===================

node todo.js edit --title kapil --description "Title edited"
ToDo edited: {title: "kapil", description: "Title edited" } in todo.json

node todo.js list
===================
Title | Description
------|------------
Kapil | Title edited
task 1 | description 1
===================

node todo.js remove --title kapil
ToDo deleted: {title: "kapil", description: "Title edited" } from todo.json

node todo.js list
===================
Title | Description
------|------------
task 1 | description 1
===================
```
