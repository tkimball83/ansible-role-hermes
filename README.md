# ansible-role-hermes

[![Build Status](https://travis-ci.org/tkimball83/ansible-role-hermes.svg?branch=master)](https://travis-ci.org/tkimball83/ansible-role-hermes)

macOS - Pandora Client

## Requirements

This role requires Homebrew and Homebrew Cask to be installed

## Role Variables

Available variables are listed below, along with default values:

    hermes_pkg: Hermes
    hermes_domain: "com.alexcrichton.{{ hermes_pkg }}"

You can modify the Hermes plist by setting the following:

    hermes_plist:
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

## Dependencies

None

## Example Playbook

    - hosts: localhost
      connection: local
      roles:
        - role: tkimball83.hermes
          hermes_plist:
            SUAutomaticallyUpdate:
              type: bool
              value: true
            audioQuality:
              type: int
              value: 0
            pauseOnScreenLock:
              type: bool
              value: true
            pauseOnScreensaverStart:
              type: bool
              value: true
            playOnScreenUnlock:
              type: bool
              value: true
            playOnScreensaverStop:
              type: bool
              value: true
            pleaseGrowlPlay:
              type: bool
              value: true
            statusBarIcon:
              type: bool
              value: true
            statusBarIconBlackWhite:
              type: bool
              value: true

## License

BSD

## Author Information

This role was created by [Taylor Kimball](http://www.tkimball83.org).

