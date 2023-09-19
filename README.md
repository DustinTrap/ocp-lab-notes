# ocp-lab-notes

## Section 1
### 1.7 missing jq

```
[dev-admin@bastion ~]$ oc get networks.config.openshift.io cluster -o json | jq .spec
-bash: jq: command not found
[dev-admin@bastion ~]$ sudo dnf install jq -y
Updating Subscription Management repositories.
Red Hat Enterprise Linux 8 for x86_64 - BaseOS (RPMs)                                                                                  8.1 kB/s | 2.4 kB     00:00
Red Hat Ceph Storage MON 4 for RHEL 8 x86_64 (RPMs)                                                                                    7.3 kB/s | 2.4 kB     00:00
Red Hat Ceph Storage OSD 4 for RHEL 8 x86_64 (RPMs)                                                                                    7.8 kB/s | 2.4 kB     00:00
Red Hat Enterprise Linux 8 for x86_64 - Supplementary (RPMs)                                                                           7.1 kB/s | 2.1 kB     00:00
Red Hat Ansible Engine 2.9 for RHEL 8 x86_64 (RPMs)                                                                                    7.3 kB/s | 2.4 kB     00:00
Red Hat Ansible Engine 2.8 for RHEL 8 x86_64 (RPMs)                                                                                    6.8 kB/s | 2.4 kB     00:00
Red Hat Ceph Storage Tools 4 for RHEL 8 x86_64 (RPMs)                                                                                  6.7 kB/s | 2.1 kB     00:00
Red Hat Enterprise Linux 8 for x86_64 - AppStream (RPMs)                                                                               9.3 kB/s | 2.8 kB     00:00
Dependencies resolved.
=======================================================================================================================================================================
 Package                           Architecture                   Version                               Repository                                                Size
=======================================================================================================================================================================
Installing:
 jq                                x86_64                         1.5-12.el8                            rhel-8-for-x86_64-appstream-rpms                         161 k
Installing dependencies:
 oniguruma                         x86_64                         6.8.2-2.el8                           rhel-8-for-x86_64-appstream-rpms                         187 k

Transaction Summary
=======================================================================================================================================================================
Install  2 Packages

Total download size: 349 k
Installed size: 1.0 M
Downloading Packages:
(1/2): jq-1.5-12.el8.x86_64.rpm                                                                                                        375 kB/s | 161 kB     00:00
(2/2): oniguruma-6.8.2-2.el8.x86_64.rpm                                                                                                405 kB/s | 187 kB     00:00
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
Total                                                                                                                                  749 kB/s | 349 kB     00:00
Running transaction check
Transaction check succeeded.
Running transaction test
Transaction test succeeded.
Running transaction
  Preparing        :                                                                                                                                               1/1
  Installing       : oniguruma-6.8.2-2.el8.x86_64                                                                                                                  1/2
  Running scriptlet: oniguruma-6.8.2-2.el8.x86_64                                                                                                                  1/2
  Installing       : jq-1.5-12.el8.x86_64                                                                                                                          2/2
  Running scriptlet: jq-1.5-12.el8.x86_64                                                                                                                          2/2
  Verifying        : oniguruma-6.8.2-2.el8.x86_64                                                                                                                  1/2
  Verifying        : jq-1.5-12.el8.x86_64                                                                                                                          2/2
Installed products updated.

Installed:
  jq-1.5-12.el8.x86_64                                                           oniguruma-6.8.2-2.el8.x86_64

Complete!

```
