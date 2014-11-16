# Ansible Role: NTP

[![Build Status](https://travis-ci.org/cecepm/ansible-role-locale.svg?branch=master)](https://travis-ci.org/cecepm/ansible-role-locale)

Set system wide locale.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    locale_language_packs:
    - language-pack-en
    - language-pack-en-base

    locale_locales:
    - { locale: en_US.UTF-8, state: present }

    locale_settings:
      LANG: en_US.UTF-8
      LANGUAGE: en_US:

## Dependencies

None.

## Example Playbook

Using default value

    - hosts: server
      roles:
      - cecepm.locale

Example, you want your system using Bahasa Indonesia

  - hosts: server
    vars:
      locale_language_packs:
      - language-pack-en
      - language-pack-en-base
      - language-pack-id
      - language-pack-id-base
      locale_locales:
      - { locale: en_US.UTF-8, state: present }
      - { locale: id_ID.UTF-8, state: present }
      locale_settings:
        LANG: "id_ID.UTF-8"
        LANGUAGE: "id_ID:"
    roles:
    - cecepm.locale


## License

MIT / BSD

## Author Information

This role was created in 2014 by [Cecep Mahbub](http://ngadimin.org/).
