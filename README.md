## Slackin for SDKMAN

[![Slack](https://slack.sdkman.io/badge.svg)](https://slack.sdkman.io)

## What?

This is a fork of the popular [Slackin](https://github.com/rauchg/slackin) project and allows users to sign up to [Slack](https://slack.com) very easily.

### Where?

This service is hosted at https://slack.sdkman.io and Docker images can be found on [Docker Hub](https://cloud.docker.com/u/sdkman/repository/docker/sdkman/sdkman-slackin).

### Why?

The repo was forked to make minor tweaks to the Dockerfile so that it can be used from within Ansible.

## How?

Run it locally with the following command, passing in environment variables as needed:

```
docker run -e "SLACK_ORG=sdkman" -e "SLACK_TOKEN=???" -e "GOOGLE_CAPTCHA_SECRET=???" -e "GOOGLE_CAPTCHA_SITEKEY=???" sdkman/sdkman-slackin:0.1.0
```


