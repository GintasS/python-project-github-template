<h1 align="center">
  <a href="https://github.com/dec0dOS/amazing-github-template">
    <img src="{{cookiecutter.repo_slug}}/docs/images/logo.svg" alt="Logo" width="125" height="125">
  </a>
</h1>

<div align="center">
  Amazing GitHub Template - Sane defaults for your next project!
  <br />
  <br />
  <a href="https://github.com/dec0dOS/amazing-github-template/issues/new?assignees=&labels=bug&template=01_BUG_REPORT.md&title=bug%3A+">Report a Bug</a>
  ·
  <a href="https://github.com/dec0dOS/amazing-github-template/issues/new?assignees=&labels=enhancement&template=02_FEATURE_REQUEST.md&title=feat%3A+">Request a Feature</a>
  .
  <a href="https://github.com/dec0dOS/amazing-github-template/discussions">Ask a Question</a>
</div>

<div align="center">
<br />

</div>

<details open="open">
<summary>Table of Contents</summary>

- [About](#about)
  - [Built With](#built-with)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Usage](#usage)
    - [Cookiecutter template](#cookiecutter-template)
    - [Manual setup](#manual-setup)
    - [Variables reference](#variables-reference)
- [License](#license)

</details>

---

## About

<table>
<tr>
<td>

Open Source Software is not about the code in the first place but the communications and community. People love good documentation and obvious workflows. If your software solves some problem, but nobody can figure out how to use it or, for example, how to create an effective bug report, there's something very bad going on. Did you hear about Readme Driven Development? Check out the awesome [article written by GitHub co-founder Tom Preston-Werner](https://tom.preston-werner.com/2010/08/23/readme-driven-development.html).

There are many great README or issues templates available on GitHub, however, you have to find them yourself and combine different templates yourself. In addition, if you want extensive docs like CODE_OF_CONDUCT.md, CONTRIBUTING.md, SECURITY.md or even advanced GitHub features like a pull request template, additional labels, code scanning, and automatic issue/PR closing and locking you have to do much more work. Your time should be focused on creating something **amazing**. You shouldn't be doing the same tasks over and over like creating your GitHub project template from scratch. Follow the **don’t repeat yourself** principle. Use a template **and go create something amazing**!

<details open>
<summary>Additional info</summary>
<br>

This project is the result of huge research. I'm a long-time GitHub user so I've seen more than [7.3k](https://github.com/dec0dOS?tab=stars) READMEs so far. I've started writing docs for my open source projects (that are currently in their early stages so they exist in the private space for now). After I've analyzed many popular GitHub READMEs and other GitHub-related docs and features I've tried to create a general-propose template that may be useful for any project.

Of course, no template will serve all the projects since your needs may be different. So [Cookiecutter](https://github.com/cookiecutter/cookiecutter) comes to the rescue. It allows [Jinja template language](https://jinja.palletsprojects.com) to be used for complex cases. Just enter up the project preferences you want in the Cookiecutter interactive menu and that's it. There is a manual setup that could be useful for your existing projects (or if you don't want to use Cookiecutter for some reason). **This README.md file is not a template itself**, you should [download the precompiled template](https://github.com/dec0dOS/amazing-github-template/releases/download/latest/template.zip) and replace the predefined values, then remove unused sections.

</details>

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

1. After installing Cookiecutter, all you need to do is to run the following command:

```sh
cookiecutter gh:dec0dOS/amazing-github-template
```

#### Variables reference

Please note that entered values are case-sensitive.
Default values are provided as an example to help you figure out what should be entered.

> On manual setup, you need to replace only values written in **uppercase**.

| Name                       | Default value      | Description                                                                 |
| -------------------------- | ------------------ | --------------------------------------------------------------------------- |
| PROJECT_NAME               | My Amazing Project | Your project name                                                           |
| REPO_SLUG                  | my-amazing-project | Repo slug must match the GitHub repo URL slug part                          |
| GITHUB_USERNAME            | dec0dOS            | Your GitHub username **without @**                                          |
| FULL_NAME                  | Alexey Potapov     | Your full name                                                              |
| OPEN_SOURCE_LICENSE        | MIT license        | Full OSS license name                                                       |
| modern_header              | y                  | Use HTML to prettify your header                                            |
| table_in_about             | n                  | Use table to wrap around About section                                      |
| include_logo               | y                  | Include Logo section. Only valid when `modern_header == y`          |
| include_badges             | y                  | Include section for badges                                                  |
| include_toc                | y                  | Include Table of Contents                                                   |
| include_screenshots        | y                  | Include Screenshots section                                                 |
| include_project_assistance | y                  | Include Project assistance section                                          |
| include_authors            | y                  | Include Authors & contributors section                                      |
| include_security           | y                  | Include Security section and SECURITY.md file                               |
| include_acknowledgements   | y                  | Include Acknowledgements section                                            |
| include_code_of_conduct    | y                  | Include CODE_OF_CONDUCT.md file                                             |
| include_workflows          | y                  | Include .github/workflows directory                                         |
| use_codeql                 | y                  | Use [CodeQL](https://securitylab.github.com/tools/codeql/)                  |
| use_conventional_commits   | y                  | Add [Conventional Commits](https://www.conventionalcommits.org) notice      |
| use_github_discussions     | n                  | Use [GitHub Discussions](https://docs.github.com/en/discussions/quickstart) |

## License

This project is licensed under the **MIT license**. Feel free to edit and distribute this template as you like.

See [LICENSE](LICENSE) for more information.
