ansible-role-inetutils-syslogd
==============================

Setup inetutils-syslogd

Role Variables
--------------

`syslogd_opts`: default to "--no-forward" as the debian package.

Typical example for use in containers:
```
syslogd_opts: "--mark=0 --no-klog"
```

`syslogd_remote`: if defined, will forward logs to the specified hostname or ip
                  make sure to also remove "--no-forward" from `syslogd_opts`.

Dependencies
------------

n/a

Example Playbook
----------------

```
- hosts: hosts
  become: yes
  roles:
    - { role: ansible-role-inetutils-syslogd }
```

License
-------

Copyright 2019 Julien Viard de Galbert

Licensed under the Apache License, Version 2.0 (the "License"); you may
not use this file except in compliance with the License. You may obtain
a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the
License for the specific language governing permissions and limitations
under the License.

Credits
-------

I want to credit the following sources that inspired me in writing this module:

- [ansible-role-rsyslog](https://github.com/robertdebock/ansible-role-rsyslog) by Robert de Bock.
- This [message on debian-devel](https://lists.debian.org/debian-devel/2014/11/msg01297.html) by Thorsten Glaser about "Guillem’s recommendation to switch to inetutils-syslogd".

Author Information
------------------

Julien Viard de Galbert

http://silicone.blogsite.org/

