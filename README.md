# AWS Toolkit for VS Code: Amazon Q & CodeWhisperer

> AWS Toolkit for Visual Studio Code.

A hands-on workshop from the [AWS First Cloud Journey](https://github.com/vanhoangkha/aws-first-cloud-journey) series, available in English and Vietnamese.

**Read the workshop online:** https://vanhoangkha.github.io/000087-AWS-Toolkit-for-Visual-Studio-Code/

## Overview

The AWS Toolkit for Visual Studio Code is an open-source extension designed for the Visual Studio Code (VS Code) editor. This tool assists developers in developing, debugging, and deploying serverless applications using Amazon Web Services (AWS) services.

Amazon Q is a conversational assistant to help build, maintain, and transform applications. From the Integrated Development Environment (IDE), Amazon Q can:

## Workshop contents

1. Introduction
2. AWS Toolkit for Visual Studio Code
3. Connecting AWS Accounts
4. Change AWS Region
5. Authentication
   - AWS IAM credentials
6. Interacting with Services
   - AWS Explorer
   - Amazon Q
   - Amazon CodeWhisperer

## Prerequisites

- An AWS account with permissions to create the resources used in the labs
- Basic familiarity with the AWS Management Console
- [Hugo](https://gohugo.io/installation/) (extended edition) if you want to run the site locally

## Run locally

```bash
git clone https://github.com/vanhoangkha/000087-AWS-Toolkit-for-Visual-Studio-Code.git
cd 000087-AWS-Toolkit-for-Visual-Studio-Code
hugo server
```

Then open http://localhost:1313 in your browser.

## Repository structure

| Path | Purpose |
| --- | --- |
| `content/` | Workshop pages (`*.md` English, `*.vi.md` Vietnamese) |
| `static/` | Images and other static assets |
| `layouts/` | Hugo layout overrides |
| `themes/` | Hugo theme |
| `config.toml` | Site configuration |

## Cost and cleanup

The labs create AWS resources that may incur charges. Delete the resources you created when you finish the workshop.

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

To report a security issue, see [SECURITY.md](SECURITY.md).

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE).
