# Dependencies

## General
- Node v14.15.1 (LTS) or more recent. While older versions can work it is advisable to keep node to latest LTS version
- npm 6.14.8 (LTS) or more recent, Yarn can work but was not tested for this project
- AWS CLI v2, v1 can work but was not tested for this project
- A RDS database running Postgres.
- A S3 bucket for hosting uploaded pictures.
- Another S3 bucket for hosting the frontend (or some custom server hosting the frontend).
- Some Elastic Beanstalk environment to host the backend (or some custom server hosting the backend).

## Libraries for building and running
### Backend
In particular:
- Bcrypt
- Express
- PG
- Typescript

For details see [package.json](/udagram-api/package.json).

### Frontend
In particular:
- Angular
- Jasmine
- Karma

For details see [package.json](/udagram-frontend/package.json).
