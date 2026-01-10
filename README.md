These of my Pull-Requests are merged here:

- [x] autostart disabled by overwrite with a local file, instead of rm/create system-wide
- [x] [offer fallback from HiDPI on low resolution displays](https://github.com/ubuntu-mate/mate-tweak/pull/113)
- [x] [minimal changes:](https://github.com/ubuntu-mate/mate-tweak/pull/112) 
   - deprecated part ;
   - missing check at layout opensuse ;
   - keep history-last-run ;
   - active compiz was not detected ;
   - check Layout was saved/deleted
- [x] [mate-volume-control has changed: applet => status-icon \[high prio\] (bugfix #94)](https://github.com/ubuntu-mate/mate-tweak/pull/111)
- [x] [Layout netbook: add check of window-buttons-applet](https://github.com/ubuntu-mate/mate-tweak/pull/110)
- [ ] [add picom-conf (GUI) as link / option [suggested feature] \[low Prio\]](https://github.com/ubuntu-mate/mate-tweak/pull/109) (currently not sure about it)
- [x] [prevent autostart picom (also bugfix #97)](https://github.com/ubuntu-mate/mate-tweak/pull/108)
- [x] [mark default windowmanager](https://github.com/ubuntu-mate/mate-tweak/pull/107)
- [x] [remove deprecated window-manager xr_glx_hybrid](https://github.com/ubuntu-mate/mate-tweak/pull/106)
- [x] [l10n: added missing strings ; update DE](https://github.com/ubuntu-mate/mate-tweak/pull/104)
- [ ] ~[add post_uninstall.sh: reset window-manager to default \[low Prio\]](https://github.com/ubuntu-mate/mate-tweak/pull/103)~ (I prefer other solution)
- [x] [add user-info at panel save: no custom launcher will be saved + list](https://github.com/ubuntu-mate/mate-tweak/pull/102)
- [x] [change build system to meson](https://github.com/ubuntu-mate/mate-tweak/pull/101)  => without it, look in this merged branch [master](https://github.com/2387skju/mate-tweak/tree/master)


This is maybe a Work in Process: Currently my Pull-Requests are not included in [Origin Repostory](https://github.com/ubuntu-mate/mate-tweak). If i found an error, i will do a git rebase and git push --force-with-lease to keep the commit history clean.

------------

This is MATE Tweak, a fork of [mintDesktop](https://github.com/linuxmint/mintdesktop).

  * MATE Tweak removes the Mint specific configuration options.
  * MATE Tweak adds User Interfacing switching.
  * MATE Tweak adds live Compiz switching.

MATE Tweak needs translators!

  * https://www.transifex.com/projects/p/MATE/resource/mate-tweak/

------------

Compile:
-  meson build --libdir=/usr/lib/ --prefix=/usr/ --sysconfdir=/etc
-  cd build
-  meson compile
-  sudo meson install

Remove:
-  sudo ninja uninstall


