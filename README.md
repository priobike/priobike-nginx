# PrioBike Nginx

We modified the original Nginx configuration to reduce logging and eliminate client IP addresses from the logs. The custom configuration is in the `nginx.conf` file.

## Why also a master branch?

Normally we have three branches: `main`, `stable` and `release`, used for our `staging`, `beta`/`production` and `release` environment. Some of our services still have a legacy naming scheme and use `master` as the default branch. Since the services fetch the nginx image based on their own branch name, we also need to build the image with a `master` tag. Ideally it should always mirror the `main` branch.