# linuxbox-cookbook

This cookbook is designed to set up a development workstation or virtual machine
in one step, using chef-zero. This isn't necessarily something you would use
on a day-to-day basis (see: test kitchen, chef server, etc.).

## Supported Platforms

* Debian 8.5
* MacOS X 10.11

## Instructions

```
wget https://raw.githubusercontent.com/realchrisolin/linuxbox/master/bootstrap.sh && chmod +x bootstrap.sh && su root -c ./bootstrap.sh
```

## Why?

A lot of the examples out on the 'net for setting up a workstation
using chef are old, and rely on using `chef-solo` instead of `chef-zero`.

Others are unnecessarily complex; for example, they require adding a workstation
as an actual chef node, which is overkill if the node isn't actually going
to be managed.

I wanted to create something I could just check out from github and run
with a single command, which would install some stuff I needed in
a repeatable and testable manner.

It also allows me to maintain this as a real cookbook with no special
magic that would prevent regular chef runs, or tools, from working.

## How it works

Quick rundown:

1. Uses the [chefzero_simple](https://github.com/christopherdeutsch/chefzero_simple) gem
to enable running chef-zero locally with minimal hassle
2. Provides a `bootstrap.sh` shell script to download/install/run everything
3. Provides a `zero.json` file with the linuxbox cookbook runlist

## License and Authors

Author:: Chris Olin (contact@chrisolin.com)
License:: BSD

Original Author:: Christopher Deutsch (chef@ispeakdeutsch.com)
License:: BSD
