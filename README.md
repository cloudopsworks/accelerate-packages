<!-- 
  ** DO NOT EDIT THIS FILE
  ** 
  ** This file was automatically generated. 
  ** 1) Make all changes to `README.yaml` 
  ** 2) Run `make init` (you only need to do this once)
  ** 3) Run`make readme` to rebuild this file. 
  -->
[![README Header][readme_header_img]][readme_header_link]

[![cloudopsworks][logo]](https://cloudops.works/)

# Cloud Ops Works Accelerate Packages

 [![Build Status](https://travis-ci.org/cloudopsworks/accelerate.svg?branch=master)](https://travis-ci.org/cloudopsworks/accelerate) [![Latest Release](https://img.shields.io/github/release/cloudopsworks/accelerate.svg)](https://github.com/cloudopsworks/accelerate/releases/latest) [![Slack Community](https://slack.cloudopsworks.com/badge.svg)](https://slack.cloudopsworks.com)


This `accelerate` is a collection of Makefiles to facilitate building Golang projects, Dockerfiles, Helm charts, and more.
It's designed to work with CI/CD systems such as GitHub Actions, Codefresh, Travis CI, CircleCI and Jenkins.


---

This project is part of our comprehensive approach towards DevOps Acceleration. 
[<img align="right" title="Share via Email" src="https://docs.cloudops.works/images/ionicons/ios-email-outline-2.0.1-16x16-999999.svg"/>][share_email]
[<img align="right" title="Share on Google+" src="https://docs.cloudops.works/images/ionicons/social-googleplus-outline-2.0.1-16x16-999999.svg" />][share_googleplus]
[<img align="right" title="Share on Facebook" src="https://docs.cloudops.works/images/ionicons/social-facebook-outline-2.0.1-16x16-999999.svg" />][share_facebook]
[<img align="right" title="Share on Reddit" src="https://docs.cloudops.works/images/ionicons/social-reddit-outline-2.0.1-16x16-999999.svg" />][share_reddit]
[<img align="right" title="Share on LinkedIn" src="https://docs.cloudops.works/images/ionicons/social-linkedin-outline-2.0.1-16x16-999999.svg" />][share_linkedin]
[<img align="right" title="Share on Twitter" src="https://docs.cloudops.works/images/ionicons/social-twitter-outline-2.0.1-16x16-999999.svg" />][share_twitter]




It's 100% Open Source and licensed under the [APACHE2](LICENSE).











## Screenshots


![demo](https://cdn.rawgit.com/cloudopsworks/accelerate/master/docs/demo.svg)
*Example of using the `accelerate` to build a docker image*



## Usage



At the top of your `Makefile` add, the following...

```make
-include $(shell curl -sSL -o .accelerate "https://cowk.io/acc"; echo .accelerate)
```

This will download a `Makefile` called `.accelerate` and include it at run-time. We recommend adding the `.accelerate` file to your `.gitignore`.

This automatically exposes many new targets that you can leverage throughout your build & CI/CD process.

Run `make help` for a list of available targets.

**NOTE:** the `/` is interchangable with the `:` in target names

## GitHub Actions

The `accelerate` is compatible with [GitHub Actions](https://github.com/features/actions).

Here's an example of running `make readme/lint` 

```
name: accelerate/readme/lint
on: [pull_request]
jobs:
  build:
    name: 'Lint README.md'
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@master
    - uses: cloudopsworks/accelerate@master
      with:
        entrypoint: /usr/bin/make
        args: readme/lint
 ```

## Quick Start

Here's how to get started...

1. `git clone https://github.com/cloudopsworks/accelerate.git` to pull down the repository
2. `make init` to initialize the [`accelerate`](https://github.com/cloudopsworks/accelerate/)




## Makefile Targets
```
Available targets:

  bash/lint                           Lint all bash scripts
  clean                               Clean Accelerate Tooling
  dist                                Create a distribution by coping $PACKAGES from $INSTALL_PATH to $DIST_PATH
  git/aliases-update                  Update git aliases
  git/export                          Export git vars
  git/submodules-update               Update submodules
  github/download-private-release     Download release from github
  github/download-public-release      Download release from github
  github/latest-release               Fetch the latest release tag from the GitHub API
  github/push-artifacts               Push all release artifacts to GitHub (Required: `GITHUB_TOKEN`)
  help                                Help screen
  help/all                            Display help for all targets
  help/short                          This help short screen
  init                                Init Accelerate Tooling
  make/lint                           Lint all makefiles
  packages/delete                     Delete packages
  packages/install                    Install packages 
  packages/install/%                  Install package (e.g. helm, helmfile, kubectl)
  packages/reinstall                  Reinstall packages
  packages/reinstall/%                Reinstall package (e.g. helm, helmfile, kubectl)
  packages/uninstall/%                Uninstall package (e.g. helm, helmfile, kubectl)
  readme                              Alias for readme/build
  readme/build                        Create README.md by building it from README.yaml
  readme/init                         Create basic minimalistic .README.md template file
  readme/lint                         Verify the `README.md` is up to date
  semver/export                       Export semver vars
  template/build                      Create $OUT file by building it from $IN template file

```



## Share the Love 

Like this project? Please give it a ★ on [our GitHub](https://github.com/cloudopsworks/accelerate-packages)! (it helps us **a lot**) 

Are you using this project or any of our other projects? Consider [leaving a testimonial][testimonial]. =)


## Related Projects

Check out these related projects.

- [Packages](https://github.com/cloudopsworks/accelerate) - Cloud Ops Works installer and distribution of native apps
- [Dev Harness](https://github.com/cloudopsworks/dev) - Cloud Ops Works Local Development Harness




## References

For additional context, refer to some of these links. 

- [Wikipedia - Test Harness](https://en.wikipedia.org/wiki/Test_harness) - The `accelerate` is similar in concept to a "Test Harness"


## Help

**Got a question?** We got answers. 

File a GitHub [issue](https://github.com/cloudopsworks/accelerate-packages/issues), send us an [email][email] or join our [Slack Community][slack].

[![README Commercial Support][readme_commercial_support_img]][readme_commercial_support_link]

## DevOps Tools

## Slack Community


## Newsletter

## Office Hours

## Contributing

### Bug Reports & Feature Requests

Please use the [issue tracker](https://github.com/cloudopsworks/accelerate-packages/issues) to report any bugs or file feature requests.

### Developing




## Copyrights

Copyright © 2021-2022 [Cloud ops Works LLC](https://cloudops.works)





## License 

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) 

See [LICENSE](LICENSE) for full details.

    Licensed to the Apache Software Foundation (ASF) under one
    or more contributor license agreements.  See the NOTICE file
    distributed with this work for additional information
    regarding copyright ownership.  The ASF licenses this file
    to you under the Apache License, Version 2.0 (the
    "License"); you may not use this file except in compliance
    with the License.  You may obtain a copy of the License at

      https://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing,
    software distributed under the License is distributed on an
    "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
    KIND, either express or implied.  See the License for the
    specific language governing permissions and limitations
    under the License.









## Trademarks

All other trademarks referenced herein are the property of their respective owners.

## About

This project is maintained by [Cloud Ops Works LLC][website]. 


### Contributors

|  [![Cristian Beraha][berahac_avatar]][berahac_homepage]<br/>[Cristian Beraha][berahac_homepage] |
|---|

  [berahac_homepage]: https://github.com/berahac
  [berahac_avatar]: https://img.cloudops.works/150x150/https://github.com/berahac.png

[![README Footer][readme_footer_img]][readme_footer_link]
[![Beacon][beacon]][website]

  [logo]: https://cloudops.works/logo-300x69.svg
  [docs]: https://cowk.io/docs?utm_source=github&utm_medium=readme&utm_campaign=cloudopsworks/accelerate-packages&utm_content=docs
  [website]: https://cowk.io/homepage?utm_source=github&utm_medium=readme&utm_campaign=cloudopsworks/accelerate-packages&utm_content=website
  [github]: https://cowk.io/github?utm_source=github&utm_medium=readme&utm_campaign=cloudopsworks/accelerate-packages&utm_content=github
  [jobs]: https://cowk.io/jobs?utm_source=github&utm_medium=readme&utm_campaign=cloudopsworks/accelerate-packages&utm_content=jobs
  [hire]: https://cowk.io/hire?utm_source=github&utm_medium=readme&utm_campaign=cloudopsworks/accelerate-packages&utm_content=hire
  [slack]: https://cowk.io/slack?utm_source=github&utm_medium=readme&utm_campaign=cloudopsworks/accelerate-packages&utm_content=slack
  [linkedin]: https://cowk.io/linkedin?utm_source=github&utm_medium=readme&utm_campaign=cloudopsworks/accelerate-packages&utm_content=linkedin
  [twitter]: https://cowk.io/twitter?utm_source=github&utm_medium=readme&utm_campaign=cloudopsworks/accelerate-packages&utm_content=twitter
  [testimonial]: https://cowk.io/leave-testimonial?utm_source=github&utm_medium=readme&utm_campaign=cloudopsworks/accelerate-packages&utm_content=testimonial
  [office_hours]: https://cloudops.works/office-hours?utm_source=github&utm_medium=readme&utm_campaign=cloudopsworks/accelerate-packages&utm_content=office_hours
  [newsletter]: https://cowk.io/newsletter?utm_source=github&utm_medium=readme&utm_campaign=cloudopsworks/accelerate-packages&utm_content=newsletter
  [email]: https://cowk.io/email?utm_source=github&utm_medium=readme&utm_campaign=cloudopsworks/accelerate-packages&utm_content=email
  [commercial_support]: https://cowk.io/commercial-support?utm_source=github&utm_medium=readme&utm_campaign=cloudopsworks/accelerate-packages&utm_content=commercial_support
  [we_love_open_source]: https://cowk.io/we-love-open-source?utm_source=github&utm_medium=readme&utm_campaign=cloudopsworks/accelerate-packages&utm_content=we_love_open_source
  [terraform_modules]: https://cowk.io/terraform-modules?utm_source=github&utm_medium=readme&utm_campaign=cloudopsworks/accelerate-packages&utm_content=terraform_modules
  [readme_header_img]: https://cloudops.works/readme/header/img
  [readme_header_link]: https://cloudops.works/readme/header/link?utm_source=github&utm_medium=readme&utm_campaign=cloudopsworks/accelerate-packages&utm_content=readme_header_link
  [readme_footer_img]: https://cloudops.works/readme/footer/img
  [readme_footer_link]: https://cloudops.works/readme/footer/link?utm_source=github&utm_medium=readme&utm_campaign=cloudopsworks/accelerate-packages&utm_content=readme_footer_link
  [readme_commercial_support_img]: https://cloudops.works/readme/commercial-support/img
  [readme_commercial_support_link]: https://cloudops.works/readme/commercial-support/link?utm_source=github&utm_medium=readme&utm_campaign=cloudopsworks/accelerate-packages&utm_content=readme_commercial_support_link
  [share_twitter]: https://twitter.com/intent/tweet/?text=Cloud+Ops+Works+Accelerate+Packages&url=https://github.com/cloudopsworks/accelerate-packages
  [share_linkedin]: https://www.linkedin.com/shareArticle?mini=true&title=Cloud+Ops+Works+Accelerate+Packages&url=https://github.com/cloudopsworks/accelerate-packages
  [share_reddit]: https://reddit.com/submit/?url=https://github.com/cloudopsworks/accelerate-packages
  [share_facebook]: https://facebook.com/sharer/sharer.php?u=https://github.com/cloudopsworks/accelerate-packages
  [share_googleplus]: https://plus.google.com/share?url=https://github.com/cloudopsworks/accelerate-packages
  [share_email]: mailto:?subject=Cloud+Ops+Works+Accelerate+Packages&body=https://github.com/cloudopsworks/accelerate-packages
  [beacon]: https://ga-beacon.cloudops.works/UA-76589703-4/cloudopsworks/accelerate-packages?pixel&cs=github&cm=readme&an=accelerate-packages
