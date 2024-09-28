<div align="center">
  <h1>Amazing GitHub Template - Sane defaults for your next project!</h1>
  <br />
  <br />
</div>

<details open="open">
<summary>Table of Contents</summary>

- [About](#about)
  - [Built With](#built-with)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Usage](#usage)
    - [Manual setup](#manual-setup)
    - [Deploying to AWS](#deploying-to-aws)
    - [Environment variables](#environment-variables)
- [License](#license)

</details>

---

## About

<table>
<tr>
<td>

Open Source Software is not about the code in the first place but the communications and community. People love good documentation and obvious workflows. If your software solves some problem, but nobody can figure out how to use it or, for example, how to create an effective bug report, there's something very bad going on. Did you hear about Readme Driven Development? Check out the awesome [article written by GitHub co-founder Tom Preston-Werner](https://tom.preston-werner.com/2010/08/23/readme-driven-development.html).

There are many great README or issues templates available on GitHub, however, you have to find them yourself and combine different templates yourself. In addition, if you want extensive docs like CODE_OF_CONDUCT.md, CONTRIBUTING.md, SECURITY.md or even advanced GitHub features like a pull request template, additional labels, code scanning, and automatic issue/PR closing and locking you have to do much more work. Your time should be focused on creating something **amazing**. You shouldn't be doing the same tasks over and over like creating your GitHub project template from scratch. Follow the **don’t repeat yourself** principle. Use a template **and go create something amazing**!

</td>
</tr>
</table>

### Built With

- [GitHub Flavored Markdown Spec](https://github.github.com/gfm/)
- [Cookiecutter](https://github.com/cookiecutter/cookiecutter)
- [GitHub Actions](https://github.com/features/actions)
- [markdownlint-cli](https://github.com/igorshubovych/markdownlint-cli)

## Getting Started

### Prerequisites

1. The easiest way to install Cookiecutter is by running:

    ```sh
    pip install --user cookiecutter
    ```

### Usage

#### Manual setup

Please follow these steps for manual setup:
1. Set-up the Discord bot on the Discord Developer Portal and add it to your server.
2. Download this GitHub repository.
3. Create a virtual environment.

    ```
    python3 -m venv <myenvname>
    ```

4. Activate virtual environment.

    ```
    cd venv
    Scripts\Activate.ps1
    ```
    Or different Activate script, if you are not working from Visual Code.

5. Install packages from requirements.txt

    ```
    pip install -r /path/to/requirements.txt
    ```

#### Deploying to AWS

1. Create a AWS RDS instance to host the PostgreSQL database.
2. Make sure the program works, run at least once to check if the discord bot is running.
3. In the ```.env``` file, change the ```CURRENT_ENVIRONMENT_NAME``` variable to use ```PROD``` .
4. Run Docker command from the terminal to build an image:
    ```
    docker build -t questions-answer-matcher-container .
    ```
5. Run AWS CLI command to push the Docker Image:
    ```
    aws lightsail push-container-image --service-name question-answer-matcher-service --label questions-answer-matcher-container --image questions-answer-matcher-container
    ```
6. Change the ```containers.json``` in the app directory to use the latest image
    ```
    question-answer-matcher-service.questions-answer-matcher-prodX.X
    ```
7. Create an AWS deployment like this:
    ```
    aws lightsail create-container-service-deployment --service-name question-answer-matcher-service --containers file://containers.json
    ```
8. Check AWS Web UI for any errors.


#### Environment variables

in the .env file, replace these environment variables with your own values.

| Name                       | Default value      | Description                                                                 |
| -------------------------- | ------------------ | --------------------------------------------------------------------------- |
| PROJECT_NAME               | My Amazing Project | Your project name                                                           |
| REPO_SLUG                  | my-amazing-project | Repo slug must match the GitHub repo URL slug part                          |
| GITHUB_USERNAME            | dec0dOS            | Your GitHub username **without @**                                          |
| FULL_NAME                  | Alexey Potapov     | Your full name                                                              |
| OPEN_SOURCE_LICENSE        | MIT license        | Full OSS license name                                                       |

## License

This project is licensed under the **MIT license**. Feel free to edit and distribute this template as you like.

See [LICENSE](LICENSE) for more information.
