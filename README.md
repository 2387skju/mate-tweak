# My Commits / Pull-Request merged together.


### You want to test?:
 Just copy the content of the file [`mate-tweak`](https://raw.githubusercontent.com/2387skju/mate-tweak/refs/heads/master/mate-tweak) to your system-file /bin/mate-tweak.
 Example: with text-Editor: `sudo pluma /bin/mate-tweak`

### Legende:
- [x] is a Pull-Request: is merged here
- [ ] is a Pull-Request: is not merged
-  is not a Pull-Requests (at the moment): is merged here


### Commits:
-  disable autostart of picom : ( follow up change of: picom shouldn't run, parallel with compiz or no-composite (bugfix #97) )
- [x] [rework: autostart managment: disable autostart by overwrite with a local file, instead of delete the system-wide](https://github.com/ubuntu-mate/mate-tweak/pull/114)
- [x] [offer fallback from HiDPI on low resolution displays](https://github.com/ubuntu-mate/mate-tweak/pull/113)
- [x] [minimal changes:](https://github.com/ubuntu-mate/mate-tweak/pull/112) 
   - deprecated part ;
   - missing check at layout opensuse ;
   - keep history-last-run ;
   - active compiz was not detected ;
   - check Layout was saved/deleted ;
   - check exists before remove autostart ;
- [x] [mate-volume-control has changed: applet => status-icon \[high prio\] (bugfix #94)](https://github.com/ubuntu-mate/mate-tweak/pull/111)
- [x] [Layout netbook: add check of window-buttons-applet](https://github.com/ubuntu-mate/mate-tweak/pull/110)
- [ ] [add picom-conf (GUI) as link / option [suggested feature] \[low Prio\]](https://github.com/ubuntu-mate/mate-tweak/pull/109) (currently not sure about it)
- [x] [picom shouldn't run, parallel with compiz or no-composite (also bugfix #97)](https://github.com/ubuntu-mate/mate-tweak/pull/108)
- [x] [mark default windowmanager](https://github.com/ubuntu-mate/mate-tweak/pull/107)
- [x] [remove deprecated window-manager xr_glx_hybrid](https://github.com/ubuntu-mate/mate-tweak/pull/106)
- [x] [translation: added missing strings ; update DE](https://github.com/ubuntu-mate/mate-tweak/pull/104)
- [ ] ~[add post_uninstall.sh: reset window-manager to default \[low Prio\]](https://github.com/ubuntu-mate/mate-tweak/pull/103)~ (I prefer other solution)
- [x] [user-info at panel save: no custom launcher will be saved, list them](https://github.com/ubuntu-mate/mate-tweak/pull/102)
- [ ] [change build system to meson](https://github.com/ubuntu-mate/mate-tweak/pull/101)  => look in this merged branch [master_with_meson__newer](https://github.com/2387skju/mate-tweak/tree/master_with_meson__newer)


This is maybe a Work in Process: Currently my Pull-Requests are not included in [Origin Repostory](https://github.com/ubuntu-mate/mate-tweak). If i found an error, i will do a git rebase and git push --force-with-lease to keep the commit history clean.

------------

This is MATE Tweak, a fork of [mintDesktop](https://github.com/linuxmint/mintdesktop).

  * MATE Tweak removes the Mint specific configuration options.
  * MATE Tweak adds User Interfacing switching.
  * MATE Tweak adds live Compiz switching.

MATE Tweak needs translators!

  * https://www.transifex.com/projects/p/MATE/resource/mate-tweak/
