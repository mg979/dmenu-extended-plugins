## dmenu-extended plugins

This repo hosts 3 plugins for
[dmenu-extended](https://github.com/MarkHedleyJones/dmenu-extended):

* Filters
* Projects
* Sheets

All plugins' configuration files can be accessed from within the plugins themselves.

### Filters

You can define and then choose filters for your indexed files. For example, by default the
filter `Documents` will show files with extensions `txt`, `pdf`, `md`, etc. You can define
the filters' names and the extensions they show.

### Projects

Each 'project' is made of a `name` (shown in dmenu), a `type` (optional, also shown in
dmenu) and `commands`. The latter is a list of commands, that will be executed in separate
processes.

You can use this plugins to fire up different programs, loading different files, or a
shell script, etc. An example of the configuration file:

    {
        "dmenu": {
            "type": "Vim",
            "command": ["gvim -S /home/me/.vim/projects/dmenux.vim"]
        }
    }

### Sheets

A simple plugin that shows all files recursively from a base directory, showing only
relative paths. It doesn't rely on dmenu indexed files. The configuration holds a list of
directories that will be searched for files. I use it to browse my annotation sheets
(hence the name).
