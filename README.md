# rethink-group

Public web site for [www.rethinkgroup.ca](https://www.rethinkgroup.ca).

![Button](./public/static/logo_sm.png?raw=true)

## Development

To run a local development version of the site, `npm install` dependencies and `npm start` to launch the [@web/dev-server](https://github.com/modernweb-dev/web/tree/master/packages/dev-server).

## Deployment

Site will deploy to S3 upon merge to the `main` branch if the HEAD commit
contains the word `[deploy]`.

### S3

Static contents of the site are stored in the `www.rethinkgroup.ca` S3 bucket, which is not accessible to the public. A second `rethinkgroup.ca` S3 bucket is configured to redirect traffic to the `www` endpoint.

### CloudFront

A CloudFront distribution sits in front of S3 to handle public access.