.PHONY: clean clean-test clean-pyc clean-build docs help

clean: clean-build clean-pyc clean-test ## remove all build, test, coverage and Python artifacts

clean-build: ## Remove build artifacts
	rm -fr build/
	rm -fr dist/
	rm -fr .eggs/
	find . -name '*.egg-info' -exec rm -fr {} +
	find . -name '*.egg' -exec rm -f {} +

clean-pyc: ## remove Python file artifacts
	find . -name '*.pyc' -exec rm -f {} +
	find . -name '*.pyo' -exec rm -f {} +
	find . -name '*~' -exec rm -f {} +
	find . -name '__pycache__' -exec rm -fr {} +

clean-test: ## remove test and coverage artifacts
	rm -fr .tox/
	rm -f .coverage
	rm -fr htmlcov/
	rm -fr .pytest_cache

reqs: ## Update all requirements
	poetry update
	poetry export --without-hashes -f requirements.txt -o requirements.txt
	poetry export --without-hashes --dev -f requirements.txt -o requirements/dev.txt
	poetry show --tree > requirements/graph.txt

install: clean ## install the package to the active Python's site-packages
	poetry install
