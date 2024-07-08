# PrioBike Nginx

This repo is used to run a nginx with a modified configuration so that the logging is reduced and the client IP addresses are eliminated from the logs.
The custom configuration file is in the `nginx.conf` file.

This image is used for multiple other PrioBike services e.g. [Priobike-Privacy-Policy-Service](https://github.com/priobike/priobike-privacy-policy-service), [Priobike-Load-Service](https://github.com/priobike/priobike-load-service), and more.

[Learn more about PrioBike](https://github.com/priobike)

## Quickstart

The easiest way to run the priobike-nginx us to use the contained `Dockerfile`:
```
docker build -t priobike-nginx . && docker run -p80:80 --rm priobike-nginx
```

## What else to know
- Normally we have three branches: `main`, `stable` and `release`, used for our `staging`, `beta`/`production` and `release` environment. Some of our services still have a legacy naming scheme and use `master` as the default branch. Since the services fetch the nginx image based on their own branch name, we also need to build the image with a `master` tag. Ideally it should always mirror the `main` branch.

## Contributing

We highly encourage you to open an issue or a pull request. You can also use our repository freely with the `MIT` license.

Every service runs through testing before it is deployed in our release setup. Read more in our [PrioBike deployment readme](https://github.com/priobike/.github/blob/main/wiki/deployment.md) to understand how specific branches/tags are deployed.

## Anything unclear?

Help us improve this documentation. If you have any problems or unclarities, feel free to open an issue.
