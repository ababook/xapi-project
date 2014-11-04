The [xapi toolstack](http://www.xenproject.org/developers/teams/xapi.html)
==========================================================================

- manages clusters of Xen hosts as single entities
- allows running VMs to be migrated between hosts (including with storage)
  with minimal downtime
- automatically restarts VMs after host failure ("High Availability")
- facilitates disaster recovery cross-site
- simplifies maintainence through rolling pool upgrade
- collects performance statistics for historical analysis and for alerting
- has a full-featured XML-RPC based API, used by clients such as
  [XenCenter](https://github.com/xenserver/xenadmin),
  [Xen Orchestra](https://xen-orchestra.com),
  [OpenStack](http://www.openstack.org)
  and [CloudStack](http://cloudstack.apache.org)

The xapi toolstack is developed by the
[xapi project](http://www.xenproject.org/developers/teams/xapi.html):
a sub-project of the Linux Foundation Xen Project.

Contents
--------

- [Architecture](doc/architecture/README.md): read about how the components of the
  xapi toolstack work together
- [Features](doc/features/README.md): learn about the features supported by xapi and
  how they work.
- [Designs](doc/designs/README.md): explore designs for cross-cutting features.
- [Xen API documentation](https://xapi-project.github.io/xen-api/): explore
  the Xen API
- [Futures](doc/futures/README.md): find out how the xapi toolstack is likely to change and
  how you can help.
- [Xapi project](http://wiki.xenproject.org/wiki/XAPI): learn about the xapi project
  on the Xen wiki

Components
----------

- [Xenopsd](https://github.com/xapi-project/xenopsd/tree/master/doc): a low-level
  "domain manager" which takes care of creating, suspending, resuming, migrating,
  rebooting domains by interacting with Xen via libxc and libxl.
- [Xcp-rrdd](https://github.com/xapi-project/xcp-rrdd/tree/master/doc): a
  performance counter monitoring daemon which aggregates "datasources" defined
  via a plugin API and records history for each.
- [Xcp-networkd](https://github.com/xapi-project/xcp-networkd/tree/master/doc):
  a host network manager which takes care of configuring interfaces, bridges
  and OpenVSwitch instances
- [SM](https://github.com/xapi-project/sm/tree/master/doc): Storage Manager
  plugins which connect Xapi's internal storage interfaces to the control
  APIs of external storage systems.
