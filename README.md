
iplock
======

The `iplock` command line is an `iptable` firewall IP address blocker.

We use it with Snap! to block unwanted users either through tools
such as `fail2ban` or from within our `libsnapwebsites` library.

The library comes with setup files which control how we add and remove
IP addresses to the firewall. There are several methods depending on
what `iplock` does.


Not a Bug
=========

Note that when you uninstall `iplock` from your system, it does not
automatically remove the IP address that were blocked by it for
security reasons. This is not a bug. It is expected that if you
uninstall our tool, you are probably going to install another tool
which will re-add those IP addresses.

If you want to clear your firewall and still have Snap! installed
you can reset it by running the default firewall script:

    sudo /etc/network/firewall

This command resets the firewall as it looks like after a reboot on
a Snap! system.

Note that when `snapfirewall` starts, it adds the IP address using
the `iplock` tool first, then allows Snap! to work.


Bugs
====

Submit bug reports and patches on
[github](https://github.com/m2osw/snapwebsites/issues).


_This file is part of the [snapcpp project](https://snapwebsites.org/)._
