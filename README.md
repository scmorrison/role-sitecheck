Role: cns.sitecheck
========

This role sets "site up" ping checks for any URL configured in the `websites` dict.

Requirements
------------

Nothing, it runs out of the box.

Role Variables
--------------

In the current version, you can specify the following variables:

| Name               | Default |                                      |
|--------------------|---------|--------------------------------------|
| websites           |   ---   | List of target ping URLS for site checks. |
| disabled_websites  |   ---   | List of target ping URLS to be removed from crontab site checks. |


Dependencies
------------

This package has no dependencies.

License
-------

GPLv2

Author Information
------------------

Created by [Sam Morrison](https://www.twitter.com/samcns)

Examples
--------

```yaml
---
- name: cns.sitecheck example
  hosts: all
  roles:
    - cns.sitecheck
```

```yaml
# Example websites / disabled_websites dicts
---
websites:
  - url: "https://www.clientsite.com/ping"
  - url: "https://www.otherclient.com/"
  - url: "https://shop.thirdclient.org/check"

disabled_websites:
  - url: "http://www.fourthclient.com/ping"
  - url: "https://support.client.net/status"
```
