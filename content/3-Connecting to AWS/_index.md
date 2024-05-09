---
title: "Connecting AWS Accounts"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: "<b> 3. </b>"
---

#### Guide to Connect AWS Toolkit for Visual Studio Code with AWS Account

The AWS Toolkit for Visual Studio Code is a powerful tool for developers using Amazon Web Services (AWS) services. To utilize the full functionality of the Toolkit, you need an AWS account. However, you can still explore some Toolkit features without connecting to an account.

If you've previously set up an AWS account and authenticated through other AWS services like the AWS Command Line Interface, the AWS Toolkit will automatically detect your login information.

#### Preparation Steps

Here are three main steps to connect AWS Toolkit to your AWS account:

#### 1. Sign Up for an AWS Account

You can sign up for an AWS account through the AWS registration portal. For detailed information on setting up a new AWS account, refer to the Overview section of the AWS Setup Guide.

#### 2. Authentication Setup

There are three main authentication methods to connect to your AWS account from the AWS Toolkit:
- Authenticate and connect with AWS IAM Identity Center
- Authenticate and connect with IAM Credentials
- Authenticate and connect with AWS Builder ID

#### 3. Authenticate with AWS from Toolkit

You can connect to your AWS account from the Toolkit by completing the procedures in the following sections of this guide.

#### Open AWS Toolkit Login Panel

#### From AWS Explorer

- Open AWS Toolkit for Visual Studio Code and expand the EXPLORER section.
- Select the ... icon to expand the More Actions... menu.
- Choose Connect to AWS to open the AWS Toolkit login panel.

#### Using VS Code Command Palette

- Open the command palette by pressing Shift+Command+P (or Ctrl+Shift+P on Windows).
- Type AWS: Add a New Connection into the search field.
- Select AWS: Add a New Connection to open the AWS Toolkit login panel.

![Amazon Q](/images/00016.png?featherlight=false&width=90pc)

#### Connect to AWS from Toolkit

To authenticate and connect to AWS using AWS IAM Identity Center, complete the following steps:
- In the AWS Toolkit login panel, select the Workforce tab and then select the Continue button.
- In the Sign in with IAM Identity Center panel, enter the Start URL for your organization.
- Choose the AWS Region from the dropdown menu.
- Select the Continue button and confirm you want to open the AWS authentication request website in your default browser.
- Follow the instructions on the browser; you will be notified when the authentication process is complete.

With these steps, you can start working effectively with the AWS Toolkit for Visual Studio Code.

