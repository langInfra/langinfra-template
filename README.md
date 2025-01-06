# Langinfra-Template Template Repository

This repository is a template for creating new repositories for Langinfra-Template. It contains the necessary files and folders to get started with creating a new Langinfra-Template repository.

## Getting Started

Install Poetry:

Follow the steps in the [Poetry documentation](https://python-poetry.org/docs/) to install Poetry.

Install the dependencies:

```bash
poetry install
```

## Extending Langinfra-Template

Add new components to the folder `src/langinfra_template/components`. Each component should be in its category folder (almost always `custom_components`) and the component should subclass `langinfra.interface.custom.custom_component.CustomComponent`

There is an example component in `src/langinfra_template/components/custom_components/ComponentExample.py` that you can use as a template.

Documentation for the CustomComponent can be found in Langinfra's [documentation](https://langinfra.org).

Any other modules you need to add can be added normally using poetry.

## Usage

To run Langinfra-Template, run the following command:

```bash
poetry run python -m langinfra serve
```

## Docker

There is a Dockerfile included in this repository.
To run Langinfra-Template in a Docker container, run the following command:

```bash
docker build -t langinfra-template .
docker run -p 5352:5352 -it langinfra-template
```
