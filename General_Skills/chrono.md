
<img width="614" alt="chrono_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/4a196d27-c523-493b-ae0c-c3fb9690fc96">

ssh to the server then look for crontab because it is the file that contains the instructions for cron which is for automating tasks in linux
/etc/crontab is the system wide crontab
per user crontabs are typically stored in: /var/spool/crontabs/<username>

```shell
┌──(xodzk㉿kali)-[~]
└─$ ssh picoplayer@saturn.picoctf.net -p 57945
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 5.19.0-1024-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

picoplayer@challenge:~$ pwd
/home/picoplayer
picoplayer@challenge:/home$ cd ..
picoplayer@challenge:/$ cd ..
picoplayer@challenge:/$ ls
bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
picoplayer@challenge:/$ cd etc
picoplayer@challenge:/etc$ ls
adduser.conf            cloud         debconf.conf    fstab      hostname     kernel         logrotate.d    mke2fs.conf          pam.conf   rc0.d  resolv.conf  ssh        sysctl.conf  update-motd.d
alternatives            cron.d        debian_version  gai.conf   hosts        ld.so.cache    lsb-release    modules-load.d       pam.d      rc1.d  rmt          ssl        sysctl.d     wgetrc
apt                     cron.daily    default         group      hosts.allow  ld.so.conf     machine-id     mtab                 passwd     rc2.d  security     subgid     systemd      xattr.conf
bash.bashrc             cron.hourly   deluser.conf    group-     hosts.deny   ld.so.conf.d   magic          networkd-dispatcher  passwd-    rc3.d  selinux      subgid-    terminfo     xdg
bindresvport.blacklist  cron.monthly  dhcp            gshadow    init.d       legal          magic.mime     networks             profile    rc4.d  shadow       subuid     timezone
binfmt.d                cron.weekly   dpkg            gshadow-   inputrc      libaudit.conf  mailcap        nsswitch.conf        profile.d  rc5.d  shadow-      subuid-    tmpfiles.d
ca-certificates         crontab       e2scrub.conf    gss        issue        localtime      mailcap.order  opt                  python3    rc6.d  shells       sudoers    ucf.conf
ca-certificates.conf    dbus-1        environment     host.conf  issue.net    login.defs     mime.types     os-release           python3.8  rcS.d  skel         sudoers.d  ufw
picoplayer@challenge:/etc$ cat crontab
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_5b7059d0}

```
