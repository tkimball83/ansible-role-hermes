# ansible-role-hermes

[![Build Status](https://travis-ci.org/tkimball83/ansible-role-hermes.svg?branch=master)](https://travis-ci.org/tkimball83/ansible-role-hermes)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-hermes-blue.svg?style=flat)](https://galaxy.ansible.com/tkimball83/hermes)
[![License](https://img.shields.io/badge/license-GPLv3-brightgreen.svg?style=flat)](COPYING)

macOS - Pandora Client

## Requirements

This role requires homebrew and homebrew cask to be installed

## Role Variables

Available variables are listed below, along with default values:

    hermes_defaults: {}
    hermes_domain: "com.alexcrichton.{{ hermes_package }}"
    hermes_package: Hermes

## Dependencies

None

## Example Playbook

    - hosts: localhost
      connection: local
      roles:
        - role: tkimball83.hermes
          hermes_defaults:
            SUAutomaticallyUpdate:
              type: bool
              value: false
            SUHasLaunchedBefore:
              type: bool
              value: true
            audioQuality:
              type: int
              value: 1
            alwaysOnTop:
              type: bool
              value: false
            drawerWidth:
              type: int
              value: 130
            openDrawer:
              type: int
              value: 0
            pauseOnScreenLock:
              type: bool
              value: false
            pauseOnScreensaverStart:
              type: bool
              value: false
            playOnScreenUnlock:
              type: bool
              value: false
            playOnScreensaverStop:
              type: bool
              value: false
            pleaseGrowlPlay:
              type: bool
              value: false
            sortStations:
              type: int
              value: 2
            statusBarIcon:
              type: bool
              value: false
            statusBarIconBlackWhite:
              type: bool
              value: false

## License

Copyright (C) 2018 Taylor Kimball <tkimball@linuxhq.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
