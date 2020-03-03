[![Build Status](https://travis-ci.org/instana/instana-agent-puppet.svg?branch=master)](https://travis-ci.org/instana/instana-agent-puppet)

:warning: :warning: :warning:

This repository is a blueprint to show how the Instana agent installation and configuration can be automated with Puppet and is intended for others to fork and build upon. It is not actively maintained. 
If you have introduce new functionality on your fork that you think is useful for others, get in touch so we can link to it from here.

:warning: :warning: :warning:

# instana-agent puppet module

This [Puppet](https://puppet.com/) module installs, configures and runs
the monitoring agent for the [Instana monitoring suite](https://www.instana.com).

## Flavors

**`instana-agent-dynamic`**

This blank agent comes bundled with a JDK and is configured to download all neccessary sensors when it starts. Additionally, it is configured to update its set of sensors on a daily basis.

**`instana-agent-static`**

This "gated" agent package is supposed to not connect to the internet at all. It comes with all the recent sensors and a JDK, and is your package of choice when you run a tight firewall setup.

## Monitoring endpoint

If you're an onprem customer, please specify your hostname and port in the corresponding attributes. If you're using our SaaS offering, and don't know which endpoint the agent should send to, feel free to ask our sales team.

## Supported operating systems

See [our official documentation](https://docs.instana.com).

## Hiera-Lookups

* They completely match the ones in our [Chef cookbook](https://github.com/instana/instana-agent-cookbook/blob/master/attributes/default.rb).

## License and Authors

This cookbook is being submitted and maintained under the [Apache v2.0 License](https://github.com/instana/cookbook/blob/master/LICENSE).

* [Zachary Schneider](https://github.com/sigil66 "Zachary Schneider")
* [Stefan Staudenmeyer](https://github.com/doerteDev "Stefan Staudenmeyer")

Copyright 2017, INSTANA Inc.
