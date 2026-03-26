## The CI/CD test
A test for CI/CD pipeline constain simple python with Flask, Docker, GitHub Actions, adn AWS EC2

## This pipeline does
Every time code is pushed to main or PR to main:
1. GitHub Actions runs automated tests
2. Builds a Docker Image
3. Pushes the image to Docker Hub
4. App is deployed on AWS EC2

## Stack

- **Python** / **Flask** - Simple Web app
- **Docker** - containization
- **GitHub Actions** - CI/CD pipeline
- **AWS EC2** - Cloud compute deployment
- **Docker Hub** - image registry

## To run locally

Clone the repo:
git clone https://github.com/PaleCanary/Pipeline_test.git
cd Pipeline_test

## Run with Docker

docker pull palecanary/my-pipeline:latest
docker run -p 3000:3000 palecanary/my-pipeline:latest

## Overview

push to GitHub main > test with Actionsdocker build > docker push > EC2 deploy
