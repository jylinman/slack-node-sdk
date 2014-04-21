slack-node-sdk
==============

[![Build Status](https://travis-ci.org/clonn/slack-node-sdk.svg?branch=master)](https://travis-ci.org/clonn/slack-node-sdk)

[Slack](https://slack.com/) Node SDK, full support Webhook and Slack API, continuous update.

##install

    npm install slack-node

##Slack Webhook usage

At first, you have to apply [Slack webhook](https://my.slack.com/services/new/incoming-webhook).

code example,

    domain = "--your-slack-subdomain--";
    webhookToken = "--your-slack-webhook--";

    slack = new Slack(webhookToken, domain);

    slack.webhook({
      channel: "#general",
      username: "webhookbot",
      text: "This is posted to #general and comes from a bot named webhookbot."
    }, function(err, response) {
      console.log(response);
    });

##Slack API

first you have to apply an API from [SLACK API page](https://api.slack.com/),

 * [https://api.slack.com/](https://api.slack.com/)

The method, please referece [Slack API page](https://api.slack.com/)

example code,

    apiToken = "-- api token --";

    slack = new Slack(apiToken);

    slack.api("users.list", function(err, response) {
      console.log(response);
    });


