# GitHub Actions - Helm

This package is to showcase a simple **GitHub Action** workflow that publishes a helm chart onto an Artifactory server.

This solution uses GitHub secrets in **GitHub Action** to follow industry best practices of not storing user data as part of the source control.

In an actual ***CI/CD*** pipeline there would be steps to set the package version according to an internal rule as well as make sure the version is compliant with **SemVer 2.0**. 

This Repo does not cover this aspect yet.

# Technical details

This repository contains a basic chart. It 

The NuGet package details are stored in the ***.csproj*** file.

The source for this **GitHub Action** is in 

    .github/workflows

# Installation

Simply clone this repository

    git clone https://github.com/karolswdev/BCT.GHActions.NuGet.Example.git

On your **GitHub** account, in the repository's ***Settings*** section find the ***Secrets*** sub-section and make sure to fill out the following information:

 - *artifactory_username* - your artifactory username (usually, your e-mail address)
 - *artifactory_password* - your artifactory password

Now, every time you commit into master or any other branch this pipeline will be launched and you will be able to observe its results using the **Actions** link on your repisitory's page.

