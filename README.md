# 0xC0ncord's Gentoo SELinux Overlay

This is my personal Gentoo SELinux overlay. This overlay contains SELinux policy modules targetting the Gentoo SELinux policy that are otherwise not yet upstreamed into Portage.

## Installation

This repository can be added manually or by using eselect-repository or layman.

### eselect-repository

```
# eselect repository add concord-selinux git https://github.com/0xC0ncord/concord-selinux-overlay.git
```

### Layman

```
# layman -o https://raw.githubusercontent.com/0xC0ncord/concord-selinux-overlay/master/repositories.xml -f -a concord-selinux
```

### Manually

1. Clone this repository somewhere.

```
$ git clone https://github.com/0xC0ncord/concord-selinux-overlay.git
```

2. Create a new file called `concord-selinux.conf` in `/etc/portage/repos.conf` with the following content:
```
[concord-selinux]
location = /path/to/cloned/repository
```

3. Install the package(s) using Portage.
4. To update the overlay just run `git pull` in the cloned repository.

## Contributing

You can report any ebuild issues or feature requests in the [issue tracker](https://github.com/0xC0ncord/concord-selinux-overlay/issues).
