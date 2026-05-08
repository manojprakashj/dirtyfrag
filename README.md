# Dirty Frag

**Dirty Frag** is a deterministic Local Privilege Escalation (LPE) vulnerability class discovered and reported by Hyunwoo Kim (@v4bel). It grants root privileges on major Linux distributions by chaining two vulnerabilities:
1. **xfrm-ESP Page-Cache Write**
2. **RxRPC Page-Cache Write**

As a descendant of the *Dirty Pipe* and *Copy Fail* bug classes, this exploit does not rely on race conditions, does not cause a kernel panic upon failure, and boasts a very high success rate. Notably, it **bypasses existing Copy Fail mitigations** (such as the `algif_aead` blacklist).

---

## Affected Versions

The vulnerabilities have existed in the upstream kernel for roughly 9 years:
* **xfrm-ESP Page-Cache Write:** In scope from `cac2661c53f3` (Jan 2017) to upstream.
* **RxRPC Page-Cache Write:** In scope from `2dc334f1a63a` (June 2023) to upstream.

This exploit has been successfully tested on the following distribution versions:
* **Ubuntu 24.04.4** (6.17.0-23-generic)
* **RHEL 10.1** (6.12.0-124.49.1.el10_1.x86_64)
* **CentOS Stream 10** (6.12.0-224.el10.x86_64)
* **AlmaLinux 10** (6.12.0-124.52.3.el10_1.x86_64)
* **Fedora 44** (6.19.14-300.fc44.x86_64)
* **openSUSE Tumbleweed** (7.0.2-1-default)

---

