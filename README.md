<div align="center" style="margin-bottom: 20px;">
  <div>
    <h1>BARCODE GENERATOR</h1>
  </div>

  <div align="center">
    <img alt="technology" src="https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue">
    <img alt="technology" src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white">
  </div>
</div>

## :memo: About project

This is a project developed in Python, using the Flask framework. The main goal is to provide a barcode generator for products. Some interesting features of this project include: Pylint and Pre-commit Configuration, Unit Testing with Pytest, Utilization of Libraries like python-barcode, Pillow and Cerberus.

## :rocket: Technologies

- [Python](https://docs.python.org/3/)
- [Virtual Env](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/)
- [Pylint](https://pylint.readthedocs.io/en/stable/)
- [Pre-commit](https://pre-commit.com/)
- [Flask](https://flask.palletsprojects.com/en/3.0.x/)
- [python-barcode](https://python-barcode.readthedocs.io/en/stable/)
- [Pillow](https://python-pillow.org/)
- [Cerberus](https://docs.python-cerberus.org/)
- [Pytest](https://docs.pytest.org/en/8.0.x/getting-started.html)

## :cyclone: Run this project

```bash
# Clone this project
$ git clone https://github.com/jefferson1104/barcode-generator.git

# Project directory
$ cd barcode-generator

# Install and config virtualenv
$ pip3 install virtualenv
$ python3 -m venv .venv
$ source .venv/bin/activate

# Install dependencies
$ pip install -r requirements.txt -v

# run project
$ python3 run.py
```

## :traffic_light: Endpoints

```bash
# to create tag
http://localhost:3000/create_tag

# body json example
{
    "product_code": "123456"
}
```
