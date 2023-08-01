[![Test deployment](https://github.com/GeekOops/geekoops-zoneminder/actions/workflows/CI.yml/badge.svg)](https://github.com/GeekOops/geekoops-zoneminder/actions/workflows/CI.yml)

# Set up Zoneminder

Configurable ansible role for installing [ZoneMinder](https://zoneminder.com/).
To that end we will use the repos by the spins-invis [project](https://build.opensuse.org/package/show/spins:invis:15:common/ZoneMinder)
mysql/mariadb is used for the database. The setup of mysql and a webserver
requires separate ansible roles.

- openSUSE Leap 15.4 -> tested

## Role Variables
--------------

You can set the following variables to configure the role. Here listed are the variables and their default settings.


| Value | Description | Default |
|-------|-------------|---------|
|`zm_domain` | The domain used by ZoneMinder | "zm.example.org" |

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: jellyfish
      roles:
         - { role: geekoops-zoneminder, zm_domain: "zm.example.org"}

An advanced example for the imaginary `jellyfish` test server

    - hosts: jellyfish
      roles:
         - role: geekoops-drupal
           vars:
             drupal_db_user: "drupal-user"
             drupal_db_pw: "1234abcd"

## Stuff to do afterwards
A good resource for checking the fpm configuration is here: https://wiki.gentoo.org/wiki/ZoneMinder

## License

MIT

## Development

