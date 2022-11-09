# Internet of Things Exercise

Build an Internet of Things device.

## Concept

The Internet of Things (IoT) is the network of connected physical and virtual devices that communicate with one-another. Often envisioned as "smart devices" -- from smart toasters to self-driving cars -- that can sense and respond to their usage, internal state, and external environment, IoT devices are often used to collect data and automate tasks. In this exercise, we will build an IoT device that senses its environment, reports the data it collects to a central server which provides a web dashboard through which users can visualize the data.

## Requirements

The IoT client device will be built using a [Raspberry Pi](https://www.raspberrypi.com/) and any additional hardware of your choice, with custom programs written primarily in Python.

- The client must collect data using one or more hardware sensors, such as camera, microphone, temperature sensor, humidity sensor, proximity sensor, etc.
- The client must do some form of analysis of the data, such as image recognition, speech recognition, classification, etc, either using third-party APIs or code libraries designed for this purpose.
- The collected data must be sent to the IoT server using a REST API.

The IoT server will be built using the Python [flask](https://palletsprojects.com/p/flask/) framework and a [MongoDB](https://www.mongodb.com/) database connected via [pymongo](https://pymongo.readthedocs.io/en/stable/), continuously deployed to a web server hosted with [Digital Ocean](https://m.do.co/c/4d1066078eb0) (note that this link includes a referral code that will give you $200 of credit, which is more than enough to cover this project. Just remember to cancel your account once the project is over to avoid being charged when the credit expires).

- The IoT server must store the data received in a database and provide a web dashboard for users to visualize the data.
- Unit tests using [pytest](https://docs.pytest.org/en/7.2.x/) and [pytest-flask](https://pytest-flask.readthedocs.io/en/latest/) must be written for the server code that provide at least 50% code coverage.
- The IoT server must have a Continuous Integration / Continuous Deployment (CI/CD) workflow using [GitHub Actions](https://github.com/features/actions) that automatically deploys the updated server as a Docker container every time a pull request is approved and code is merged into the main branch.

Both parts of this project must be stored in this "monorepo" - a single repository housing multiple independent subsystems of a single software project.

A starter `.gitignore` file has been provided. However, this should be updated as necessary to make sure that any 3rd-party Python modules or subsystems used by this proejct are not included in version control for this project. Use `pip` or `pipenv` to document and install any 3rd-party Python software dependencies.

## Developer workflow

All team members must have visibly contributed to the code using their own git & GitHub accounts in order to claim that they contributed to the project.

All code changes must be done in feature branches and not directly in the `main` branch.

To merge code from a feature branch into the `main` branch, do the following:

1. Create a pull request from the feature branch to the `main` branch.
1. Ask a fellow developer to review your code.
1. The reviewer must review the code and run unit tests to verify that the functions behave as expepcted.
1. If the reviewer has any concerns, discuss then and make any changes agreed upon.
1. Merge the pull request into the `main` branch.
1. Delete the feature branch.
1. Pull the latest changes from the remote `main` branch to your local `main` branch.

**Warning**: the longer you let code sit in a feature branch, the more likely your team is to end up in [merge hell](https://en.wikipedia.org/wiki/Merge_hell). . Merge feature branches into `main` often to avoid this fate.

## Documentation

Replace the contents of the [README.md](./README.md) file with a beautifully-formatted Markdown file including a plain-language **description** of your project, including:

Include a [badge](https://docs.github.com/en/actions/monitoring-and-troubleshooting-workflows/adding-a-workflow-status-badge) at the top of the `README.md` file showing the result of the latest build/test workflow of the server.

Include the names of all teammates as links to their GitHub profiles in the `README.md` file.

Include a link to your package's page on the PyPI website.
