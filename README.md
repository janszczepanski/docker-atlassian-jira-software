[![CircleCI Build Status](https://img.shields.io/circleci/project/janszczepanski/docker-atlassian-jira-software/master.svg?label=CircleCI)](https://circleci.com/gh/janszczepanski/docker-atlassian-jira-software) [![Open Issues](https://img.shields.io/github/issues/janszczepanski/docker-atlassian-jira-software.svg)](https://github.com/janszczepanski/docker-atlassian-jira-software/issues) [![Stars on GitHub](https://img.shields.io/github/stars/janszczepanski/docker-atlassian-jira-software.svg)](https://github.com/janszczepanski/docker-atlassian-jira-software/stargazers) [![Forks on GitHub](https://img.shields.io/github/forks/janszczepanski/docker-atlassian-jira-software.svg)](https://github.com/janszczepanski/docker-atlassian-jira-software/network) [![Stars on Docker Hub](https://img.shields.io/docker/stars/janszczepanski/docker-atlassian-jira-software.svg)](https://hub.docker.com/r/janszczepanski/docker-atlassian-jira-software/) [![Pulls on Docker Hub](https://img.shields.io/docker/pulls/janszczepanski/docker-atlassian-jira-software.svg)](https://hub.docker.com/r/janszczepanski/docker-atlassian-jira-software/) [![Sponsor by PayPal](https://img.shields.io/badge/sponsor-PayPal-blue.svg)](https://paypal.me/JanSzczepanski/5)

# Atlassian JIRA Software in a Docker container

This is a containerized installation of Atlassian JIRA Software with Docker, and it's a match made in heaven for us all to enjoy. The aim of this image is to keep the installation as straight forward as possible, but with a few Docker related twists. You can get started by clicking the appropriate link below and reading the documentation.

* [Atlassian JIRA Software](https://cptactionhank.github.io/docker-atlassian-jira-software)

If you want to help out, you can check out the contribution section further down.

## I'm in the fast lane! Get me started

To quickly get started running a JIRA Software instance, use the following command:
```bash
docker run --detach --publish 8080:8080 cptactionhank/atlassian-jira-software:latest
```

Then simply navigate your preferred browser to `http://[dockerhost]:8080` and finish the configuration.

## Configuration

You can configure a small set of things by supplying the following environment variables

| Environment Variable   | Description |
| ---------------------- | ----------- |
| X_PROXY_NAME           | Sets the Tomcat Connectors `ProxyName` attribute |
| X_PROXY_PORT           | Sets the Tomcat Connectors `ProxyPort` attribute |
| X_PROXY_SCHEME         | If set to `https` the Tomcat Connectors `secure=true` and `redirectPort` equal to `X_PROXY_PORT`   |
| X_PATH                 | Sets the Tomcat connectors `path` attribute |

## Contributions

This image has been created with the best intentions and an expert understanding of docker, but it should not be expected to be flawless. Should you be in the position to do so, I request that you help support this repository with best-practices and other additions.

CircleCI has been configured to build the Dockerfile and run acceptance tests on the Atlassian JIRA Software image to ensure it is working.

If you see out of date documentation, lack of tests, etc., you can help out by either
- creating an issue and opening a discussion, or
- sending a pull request with modifications (remember to read [contributing guide](https://github.com/janszczepanski/docker-atlassian-jira-software/blob/master/CONTRIBUTING.md) before.)

Continuous Integration and Continuous Delivery is made possible with the great services from [GitHub](https://github.com) and [CircleCI](https://circleci.com/) written in [Ruby](https://www.ruby-lang.org/), using [RSpec](http://rspec.info/), [Capybara](http://teamcapybara.github.io/capybara/), and [PhantomJS](http://phantomjs.org/) frameworks.
