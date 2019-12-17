# GitHub Actions - Helm

This package is to showcase a simple **GitHub Action** workflow that publishes a helm chart onto an Artifactory server.

This solution uses GitHub secrets in **GitHub Action** to follow industry best practices of not storing user data as part of the source control.

In an actual ***CI/CD*** pipeline there would be steps to set the package version according to an internal rule as well as make sure the version is compliant with **SemVer 2.0**. 

This repository does **not** cover this aspect yet.

# Technical details

This repository contains a basic **Helm 3** chart.

The GitHub action is stored in

    .github/workflows/main.yml

# Installation

Simply clone this repository

    git clone https://github.com/karolswdev/bct-ghactions-helm-example

On your **GitHub** account, in the repository's ***Settings*** section find the ***Secrets*** sub-section and make sure to fill out the following information:

 - *artifactory_username* - your Artifactory username (usually, your e-mail address)
 - *artifactory_password* - your Artifactory password
 - *artifactory_apikey* - your Artifactory API key

Now, every time you commit into master or any other branch this pipeline will be launched and you will be able to observe its results using the **Actions** link on your repisitory's page.

