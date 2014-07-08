Pathes used by apt-cyg
-------


* /etc/setup

  * $pkg.lst.gz: File list of each installed package
    Can be generated by tar -t

  * installed.db: List of installed packages
    Each line is like "<pkgname> <archive_filename> 0"


* /setup

Cache of archives


    /setup
    |
    `-- $mirror_url/
        |
        |- release/
        |  |
        |  `- $pkgname/
        |     |
        |     |- $pkgname-$pkgvar.tar.bz2
        |     |
        |     `- desc -- package description extracted from setup.ini
        |
        `- setup.ini -- Package descriptions provided by that mirror


Hook Script
-------

Some hook script provided by package itself

* /etc/postinstall/
* /etc/preremove/