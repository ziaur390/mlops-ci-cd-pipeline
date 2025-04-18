# Build CI/CD Pipeline for ML Models using Docker and GitHub Actions

This repository contains code and files for building and deploying a Machine Learning model for predicting the survival of Titanic passengers using Docker and GitHub Actions.

## Overview

The project consists of the following components:

- **titanic_model**: A Python package that contains the data processing and model training scripts for the Titanic survival prediction task.
- **titanic_model_api**: A Flask web application that serves the trained model as a RESTful API endpoint.
- **Dockerfile**: A file that defines the steps and commands for creating a Docker image of the web application.
- **.github/workflows**: A folder that contains the GitHub Actions workflow file for automating the Docker image building and pushing process.
- **tests**: A folder that contains unit tests and integration tests for the Python package and the web application.
- **requirements**: A file that lists the Python dependencies for the project.
- **setup.py**: A file that defines the metadata and installation instructions for the Python package.
- **MANIFEST.in**: A file that specifies the non-code files to be included in the Python package distribution.
- **mypy.ini**: A file that configures the type checking tool mypy for the project.
- **pyproject.toml**: A file that defines the formatting tool black for the project.

## Installation

To install the Python package, run the following command from the root directory of the repository:

```bash
pip install .
```

To build the Docker image, run the following command from the root directory of the repository:

```bash
docker build -t titanic-model-api .
```

To run the Docker container, run the following command:

```bash
docker run -p 5000:5000 titanic-model-api
```

## Usage

To use the web application, send a POST request to the `/predict` endpoint with a JSON payload containing the features of a Titanic passenger. For example:

```bash
curl -X POST -H "Content-Type: application/json" -d '{"Pclass": 3, "Sex": "male", "Age": 22, "SibSp": 1, "Parch": 0, "Fare": 7.25, "Embarked": "S"}' http://localhost:5000/predict
```

The response will be a JSON object containing the predicted probability of survival for the passenger. For example:

```json
{"survival_probability": 0.087}
```

## Testing

To run the unit tests and integration tests, run the following command from the root directory of the repository:

```bash
pytest
```

To run the type checking and formatting tools, run the following commands:

```bash
mypy titanic_model titanic_model_api
black titanic_model titanic_model_api
```

## Contributing

If you have a Data Science mini-project that you'd like to share, please follow the guidelines in [CONTRIBUTING.md](https://github.com/Praveen76/Data-Science-Mini-Projects/blob/main/contributing.md).

## Code of Conduct
Please adhere to our [Code of Conduct](https://github.com/Praveen76/Data-Science-Mini-Projects/blob/main/CODE_OF_CONDUCT.md) in all your interactions with the project.

## License

This project is licensed under the [MIT License](LICENSE).

## Contact

For questions or inquiries, feel free to contact me on [Linkedin](https://www.linkedin.com/in/praveen-kumar-anwla-49169266/).

## **About Me**:
I’m a seasoned Data Scientist and founder of [TowardsMachineLearning.Org](https://towardsmachinelearning.org/). I've worked on various Machine Learning, NLP, and cutting-edge deep learning frameworks to solve numerous business problems.

