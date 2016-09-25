starstar
--------

This repo contains a simple example of a pattern in python that I've found useful when I need to load a config file and do something with the data it contains.

The pattern is simple:

1. Load the config file off of disk
2. Parse it into python objects using the `**` operator and list comprehensions
3. Do something with the python objects

In this example the config file is a YAML file, although it could just as easily be JSON, TOML, or a CSV, and we use it to instantiate python objects which then serve as the context for a jinja2 markdown template. This might also be useful for parsing a config file that contains program settings.

There are a number of advantages to this approach:

- It is resistant to bugs caused by misspellings in the config file. If you misspell an item in the config file, the corresponding call to `__init__` will fail with a helpful error message.

- If you misspell a property name in a template you'll get an error message which has the class name in it, instead of a generic dictionary key error.

- It is concise and appealing.

Files:

- `main` is the code. Start reading here
- `README.md` is this readme
- `config.yaml` is the YAML config file
- `template.md` is the jinja2 markdown template
- `output.md` is the rendered template
- `yaml` is a copy of the PyYAML YAML library
- `jinja2` is a copy of Jinja2 template engine
