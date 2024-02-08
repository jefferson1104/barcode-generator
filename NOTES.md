## NOTES

#### virtualenv

A tool for creating isolated virtual python environments.
https://pypi.org/project/virtualenv/
https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/

```bash
$ pip3 install virtualenv

$ python3 -m venv .venv

$ source .venv/bin/activate

$ .venv/bin/pip3 freeze > requirements.txt
```

#### pylint

Pylint is a static code analyser for Python 2 or 3
https://pypi.org/project/pylint/

```bash
$ pip3 install pylint

$ pylint --generate-rcfile > .pylintrc
```

#### pre-commit

A framework for managing and maintaining multi-language pre-commit hooks.
https://pre-commit.com/

```bash
$ pip3 install pre-commit
```

create `.pre-commit-config.yaml` with this content below:

```bash
repos:
  - repo: local
    hooks:
      - id: pylint
        name: pylint
        entry: pylint
        language: system
        types: [python]
        args:
          [
            "-rn", # Only display messages
            "-sn", # Don't display the source
            "--rcfile=.pylintrc", # Link to your config file
            "--load-plugins=pylint.extensions.docparams", # Load an extension
          ]
```

run this commmand below

```bash
$ pre-commit install
```
