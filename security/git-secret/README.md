# git-secret freebsd port development


Output of tests in /usr/ports/security/git-secret

````
freebsd2# make stage
===>  License MIT accepted by the user
===>   git-secret-0.2.5 depends on file: /usr/local/sbin/pkg - found
===> Fetching all distfiles required by git-secret-0.2.5 for building
===>  Extracting for git-secret-0.2.5
=> SHA256 Checksum OK for sobolevn-git-secret-0.2.5-94d5ae4_GH0.tar.gz.
===>  Patching for git-secret-0.2.5
===>  Configuring for git-secret-0.2.5
===>  Building for git-secret-0.2.5
`git-secret' is up to date.
===>  Staging for git-secret-0.2.5
===>   git-secret-0.2.5 depends on executable: gawk - found
===>   git-secret-0.2.5 depends on executable: git - found
===>   git-secret-0.2.5 depends on executable: gpg2 - found
===>   Generating temporary packing list
install  -m 555 /home/user/freebsd-ports/security/git-secret/work/git-secret-94d5ae4/git-secret /home/user/freebsd-ports/security/git-secret/work/stage/usr/local/bin/
install  -m 444 /home/user/freebsd-ports/security/git-secret/work/git-secret-94d5ae4/man/man1/*.1 /home/user/freebsd-ports/security/git-secret/work/stage/usr/local/man/man1/
install  -m 444 /home/user/freebsd-ports/security/git-secret/work/git-secret-94d5ae4/man/man7/*.7 /home/user/freebsd-ports/security/git-secret/work/stage/usr/local/man/man7/
====> Compressing man pages (compress-man)

freebsd2# make check-orphans
====> Checking for pkg-plist issues (check-plist)
===> Parsing plist
===> Checking for items in STAGEDIR missing from pkg-plist
===> Checking for items in pkg-plist which are not in STAGEDIR
===> No pkg-plist issues found (check-plist)

freebsd2# make package
===>  Building package for git-secret-0.2.5

freebsd2# make install
===>  Installing for git-secret-0.2.5
===>  Checking if git-secret already installed
===>   Registering installation for git-secret-0.2.5
Installing git-secret-0.2.5...

freebsd2# make deinstall
===>  Deinstalling for git-secret
===>   Deinstalling git-secret-0.2.5
Updating database digests format: 100%
Checking integrity... done (0 conflicting)
Deinstallation has been requested for the following 1 packages (of 0 packages in the universe):

Installed packages to be REMOVED:
    git-secret-0.2.5

Number of packages to be removed: 1
[1/1] Deinstalling git-secret-0.2.5...
[1/1] Deleting files for git-secret-0.2.5: 100%
````
