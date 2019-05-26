# Git Review API

[![CircleCI](https://circleci.com/gh/USA-RedDragon/GitReview-api/tree/master.svg?style=svg)](https://circleci.com/gh/USA-RedDragon/GitReview-api/tree/master) [![codecov](https://codecov.io/gh/USA-RedDragon/GitReview-api/branch/master/graph/badge.svg)](https://codecov.io/gh/USA-RedDragon/GitReview-api) [![API](https://images.microbadger.com/badges/image/jamcswain/gitreview-api.svg)](https://microbadger.com/images/jamcswain/gitreview-api "Get your own image badge on microbadger.com")

## Deploying

The Docker images for the current master branch are found on [Docker Hub](https://hub.docker.com/u/jamcswain) under `gitreview-api`. Versioning will be implemented once I reach stable 1.0.

The below documentation will go through the information you need.

As far as best practices, and how to deploy containers, a Google search is your best friend.

## Environment Variables

| Environment Variable |                   Details                   |                      Example                      |
| -------------------- | ------------------------------------------- | ------------------------------------------------- |
| DB_HOST              | The hostname for the database               | localhost                                         |
| DB_USERNAME          | The username for the database               | username                                          |
| DB_PASSWORD          | The password for the database               | password                                          |
| DB_DATABASE          | The name of the database to use             | data                                              |
| DB_DIALECT           | The type of database to use                 | mysql                                             |
| PORT                 | The port to run the app on                  | 3000                                              |
| HOST                 | The host the app is on                      | http://localhost:3000                             |
| GITHUB_CLIENT_ID     | The GitHub oauth client id                  | e784805167d98101e139                              |
| GITHUB_CLIENT_SECRET | The GitHub oauth client secret              | 9f626c1a443864ccc0f8397a933ca1f7edae870c          |
| GITHUB_CALLBACK_URL  | The GitHub oauth callback url               | http://localhost:3000/api/v1/auth/github/callback |
| SECRET               | The signing secret for sessions and cookies | secret                                            |

## Database

Any database system compatible with Sequelize will work with this

See <http://docs.sequelizejs.com/manual/dialects.html> for a list

Make sure to persist this and take backups
