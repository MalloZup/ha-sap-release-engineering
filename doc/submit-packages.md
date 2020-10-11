# Submit packages

It follow a declarative API based on yaml:

Its main and unique usage is  send packages to various codestream. Maintaining them as declarative format.

* CODESTREAM (Following exact codestream of SLES) 
  - from:
  - packages:
      - foo
      - bar
```
The CODESTREAM is the targed, where we want to submit packages. On th
`from`: is the openSUSE project you want to sumbit the pkg from ( to sles ibs)
`packages`: is a list or single package to submits to target code stream

As you can see you can have multiple codestreams on a single yaml file.

Example:
```
SUSE:SLE-15:Update:
        - from: network:ha-clustering:sap-deployments:devel
        - packages: 
          - salt-hana-formula
          - ha-cluster-exporter

SUSE:SLE-12:Update:
        - from: network:ha-clustering:sap-deployments:devel
        - packages:
          - salt-hana-formula
          - ha-cluster-exporter
```
