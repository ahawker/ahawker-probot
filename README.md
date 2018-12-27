# ahawker-probot

A [Probot](https://github.com/probot/probot) app for [personal](https://github.com/ahawker) repositories.

## Deployment

This probot instance is deployed on [Heroku](https://heroku.com/) free tier.

Simply make necessary changes, commit them to this repository and then push them to Heroku with:

```bash
$ git push heroku master
```

## Debugging

Temporary increase of the log level can help you understand what's happening...

```bash
$ heroku config:set LOG_LEVEL=trace
$ heroku logs --tail
```

## Configuration

The following environment variables need to be configured/set:

* WEBHOOK_SECRET - Randomly generated secret set/stored in GitHub webhook integration.
* PRIVATE_KEY - PEM file data for the GitHub integration.
* SENTRY_DSN - (Optional) If you wish to have this probot instance report exceptions to [Sentry](https://sentry.io)

## Apps

Depending on what apps are configured, this app integration will require a differing set of permissions. This following is a list
of probot apps used.

* [WIP](https://github.com/wip/app)
* [Stale](https://github.com/probot/stale)
* [Reminders](https://github.com/probot/reminders)

## License

[Apache 2.0](LICENSE)
