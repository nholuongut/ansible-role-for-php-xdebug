# Ansible Role: PHP-XDebug

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

Installs PHP [XDebug](http://xdebug.org/) on Linux servers.

## Requirements

Prior to running this role, make sure the `php-devel` and `@Development Tools` (for RHEL/CentOS) or `php5-dev` + `build-essential` packages (for Debian/Ubuntu) are present on the system, as they are required for the build of Xdebug.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    workspace: /root

Where Xdebug setup files will be downloaded and built.

    php_xdebug_version: 2.9.5

The version of Xdebug to be installed (see [Updates](https://xdebug.org/updates.php) for a current listing).

    php_xdebug_default_enable: 1
    php_xdebug_coverage_enable: 1

Whether to enable XDebug coverage and default exception handling or not. Disable these for slightly improved PHP performance, enable these to use XDebug to the fullest extent.

    php_xdebug_module_path: /usr/lib64/php/modules

The path where `xdebug.so` will be installed.

    php_xdebug_remote_enable: "false"

Whether remote debugging is enabled.

    php_xdebug_remote_connect_back: "false"

If this is set to true, Xdebug will respond to any request from any IP address; use only for local development on non-public installations!

    php_xdebug_remote_host: localhost
    php_xdebug_remote_port: "9000"

The host and port on which Xdebug will listen.

    php_xdebug_remote_log: /tmp/xdebug.log

The location of the xdebug log (useful if you're having trouble connecting).

    php_xdebug_idekey: sublime.xdebug

The IDE key to use in the URL when making Xdebug requests (e.g. `http://example.local/?XDEBUG_SESSION_START=sublime.xdebug`).

    php_xdebug_max_nesting_level: 256

The maximimum function nesting level before Xdebug bails and throws a fatal exception.

    php_xdebug_cli_disable: false

(Debian/Ubuntu ONLY) Disable xdebug for the CLI SAPI.

## Dependencies

  - nholuong.php

## Example Playbook

    - hosts: webservers
      roles:
        - { role: nholuong.php-xdebug }

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟