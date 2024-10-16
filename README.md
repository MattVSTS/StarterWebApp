# This is a starter Web App
This application was created by running `dotnet new mvc`, it is a vanilla application.

If you want to create your own, install the .NET SDK and run `dotnet new mvc` from your CLI. There are other templates available other than `mvc`.

## CI Pipeline Setup

This repository includes a CI pipeline setup using GitHub Actions. The workflow file is located at `.github/workflows/starter-web-app-ci.yml`.

### Purpose

The GitHub Actions workflow file is used to automate the build and packaging process for the code. It ensures that the code is built and packaged automatically on each push or pull request to the `main` branch.

### How to Use

1. Make sure you have a GitHub repository with this code.
2. Push your changes to the `main` branch or create a pull request targeting the `main` branch.
3. The GitHub Actions workflow will be triggered automatically.
4. The workflow will set up the .NET environment, restore dependencies, build the project, and package the output.

You can check the status of the workflow in the "Actions" tab of your GitHub repository.

### Packaging the Website

After the project is published, the CI pipeline includes a step to package the website in a MSDeploy zip file. This step runs the `dotnet msbuild` command with the `MSDeployPublish` target to create the MSDeploy zip package. The MSDeploy zip package is created in the `./publish` directory.
