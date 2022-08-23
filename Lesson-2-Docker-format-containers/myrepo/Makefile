SHELL := /bin/bash
setup:
	python3 -m venv ~/.myrepo

activate:
	source ~/.myrepo/bin/activate

install:
	pip install -r requirements.txt

test:
	python -m pytest -vv --cov=myrepolib tests/*.py
	python -m pytest --nbval notebook.ipynb


lint:
	pylint --disable=R,C myrepolib cli web

all: activate install lint test