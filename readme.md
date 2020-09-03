## Slackin for SDKMAN

[![Slack](https://img.shields.io/badge/chat-on%20slack-red.svg)](https://slack.sdkman.io)

## What?

This is a fork of the popular [Slackin](https://github.com/rauchg/slackin) project and allows users to sign up to [Slack](https://slack.com) very easily.

### Where?

This service is hosted at https://slack.sdkman.io and Docker images can be found on [Docker Hub](https://cloud.docker.com/u/sdkman/repository/docker/sdkman/sdkman-slackin).

### Why?

The repo was forked to make minor tweaks to the Dockerfile so that it can be used from within Ansible.

## How?

Run it locally with the following command, passing in environment variables as needed:

```
docker run -e "SLACK_ORG=sdkman" -e "SLACK_TOKEN=???" -e "GOOGLE_CAPTCHA_SECRET=???" -e "GOOGLE_CAPTCHA_SITEKEY=???" sdkman/sdkman-slackin:latest
```

Or in Ansible using `docker_service`:
```
slackin:
  image: "{{ slackin_docker_image }}"
  container_name: sdkman-slackin
  expose:
    - "3000"
  environment:
    - SLACK_ORG=sdkman
    - SLACK_TOKEN={{ slack_token }}
    - GOOGLE_CAPTCHA_SECRET={{ google_captcha_secret }}
    - GOOGLE_CAPTCHA_SITEKEY={{ google_captcha_sitekey }}
```
