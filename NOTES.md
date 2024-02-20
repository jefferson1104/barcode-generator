## NOTES

#### virtualenv

A tool for creating isolated virtual python environments.
https://pypi.org/project/virtualenv/
https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/

```bash
$ pip3 install virtualenv

$ python3 -m venv .venv

$ source .venv/bin/activate

# every time you install some dependency in your project you need to run this command to update the requirements.txt
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

#### Flask

Flask is a lightweight WSGI web application framework.
https://pypi.org/project/Flask/

```bash
$ pip3 install flask
```

#### Python-barcode & pillow

python-barcode provides a simple way to create barcodes in Python.
https://pypi.org/project/python-barcode/

The Python Imaging Library adds image processing capabilities to your Python interpreter.
This library provides extensive file format support.
https://pypi.org/project/pillow/

```bash
$ pip3 install python-barcode

$ pip3 install pillow
```

### Cerberus

Cerberus provides powerful yet simple and lightweight data validation functionality
https://docs.python-cerberus.org/
https://pypi.org/project/Cerberus/

```bash
$ pip3 install Cerberus
```

### Endpoint

```bash
# endpoint
http://localhost:3000/create_tag

# json body
{
    "product_code": "HelloWorld"
}
```

### Run project

```bash
$ python3 [file_name]
# python3 run.py

```
