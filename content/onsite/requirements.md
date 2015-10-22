<!--
order: 2
title: Requirements
-->

# npm On-Site installation requirements

npm On-Site has been extensively tested Ubuntu 14 (Trusty), and is
supported on most recent public Linux distributions. It can run inside a
virtual machine or on standard hardware. It can also be run in a [Docker container](https://github.com/npm/npme-docker).

Since it can be configured to only selectively mirror the public registry in
addition to your private packages, its disk space requirements are significantly
lighter than other private registry solutions. npm On-Site does not use a great
deal of processor or memory, so stock hardware will work, with at least 2GB of RAM.

Its primary variable requirement is disk space: you need enough disk to hold every
version of every package you publish, and all the packages you mirror. This can be
anywhere from a few gigabytes to half a terabyte if you mirror the entire registry,
so prepare accordingly and adjust your [whitelist settings](/onsite/whitelist)
to limit the packages you mirror.

For a walkthrough of installation, you can watch our [quickstart video](/onsite/intro).

## Install the latest version of Node

[Update Node](/getting-started/installing-node) to the latest version.

For Ubuntu, we recommend the distribution put together by our friends at
[NodeSource](https://nodesource.com/). To install it, run:

```bash
curl -sL https://deb.nodesource.com/setup | sudo bash -
sudo apt-get install nodejs
```

## Install the latest version of npm

To use npm On-Site, the server needs to have a recent version (2.x or higher) of the npm client installed. To update npm, run:

```bash
sudo npm install npm -g
```

NOTE: Depending on your local setup, you may be able to omit sudo.

## Remove password requirement for sudo

npm On-Site must be installed from an account that has passwordless sudo. As part of the installation process, npm On-Site creates the npme user.

See [How to remove password prompt](http://askubuntu.com/questions/235084/how-do-i-remove-ubuntus-password-requirement).
