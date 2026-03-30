---
tags:
  - infra/linux
---
[YUM and DNF vs. Zypper vs. APT, RPM vs. dpkg command comparison and cheat sheet](https://www.claudiokuenzler.com/blog/354/yum-dnf-zypper-apt-rpm-dpkg-command-comparison-suse-debian)

| Purpose                                             | yum (and dnf) command                                                                   | zypper command          | apt command                                                                |
| --------------------------------------------------- | --------------------------------------------------------------------------------------- | ----------------------- | -------------------------------------------------------------------------- |
| **Search a package**                                | yum search "pkgname"  <br>dnf search "pkgname"                                          | zypper se "pkgname"     | apt-cache search "pkgname"  <br>apt search "pkgname"                       |
| **Install a package**                               | yum install "pkgname"  <br>dnf install "pkgname"                                        | zypper in "pkgname"     | apt-get install "pkgname"  <br>apt install "pkgname"                       |
| **Update package list from repositories**           | tbv                                                                                     | zypper refresh          | apt-get update  <br>apt update                                             |
| **Update all packages**                             | yum update  <br>dnf update                                                              | zypper update           | apt-get upgrade  <br>apt upgrade                                           |
| **Upgrade all packages to a new major version**     | yum update  <br>dnf update                                                              | zypper dist-upgrade     | apt-get dist-upgrade  <br>apt dist-upgrade                                 |
| **Update a single package**                         | yum install "pkgname"  <br>dnf install "pkgname"                                        | zypper update "pkgname" | apt-get install "pkgname"  <br>apt install "pkgname"                       |
| **Downgrade a single package**                      | yum downgrade "pkgname-versiontag"  <br>dnf downgrade "pkgname-versiontag"              | tbv                     | apt-get install "pkgname=versiontag"  <br>apt install "pkgname=versiontag" |
| **Show packages with updates**                      | yum check-update  <br>dnf check-update                                                  | zypper list-updates     | apt-show-versions -u  <br>apt list --upgradable                            |
| **Re-Install a package**                            | yum reinstall "pkgname"  <br>dnf reinstall "pkgname"                                    | tbv                     | apt-get install --reinstall "pkgname"                                      |
| **Uninstall/remove a package**                      | yum remove "pkgname"  <br>dnf remove "pkgname"                                          | zypper remove "pkgname" | apt-get remove "pkgname"  <br>apt remove "pkgname"                         |
| **Remove unused packages**                          | yum autoremove  <br>dnf autoremove                                                      | tbv                     | apt-get autoremove  <br>apt autoremove                                     |
| **Show all packages found in repo(s)**              | yum list  <br>dnf list                                                                  | zypper packages         | apt-cache pkgnames                                                         |
| **Show all versions of a package in repo(s)  <br>** | dnf list "pkgname" --showduplicates                                                     | tbv                     | apt-cache show "pkgname" \| grep "^Version"                                |
| **Show description of a package**                   | yum info "pkgname"  <br>dnf info "pkgname"                                              | zypper info "pkgname"   | apt-cache show "pkgname"  <br>apt show "pkgname"                           |
| **Show dependencies of a package**                  | yum deplist "pkgname"  <br>dnf deplist "pkgname"  <br>dnf repoquery --deplist "pkgname" | tbv                     | apt-cache depends "pkgname"  <br>apt depends "pkgname"                     |
| **Show contents (files) of a package  <br>**        | repoquery -l "pkgname"  <br>dnf repoquery -l "pkgname"                                  | tbv                     | apt content "pkgname"                                                      |
