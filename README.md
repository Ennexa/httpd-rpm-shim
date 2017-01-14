Dummy RPM for httpd. Used to satisfy httpd dependency for installing mod_pagespeed on cPanel EA4 servers.

Based on

https://www.mnxsolutions.com/quick-tip/building-an-empty-rpm.html

Build using

    docker run -ti -v `pwd`:/work -w /work centos sh -c 'yum install -y rpm-build && rpmbuild -bb httpd.spec && ls -l && /bin/cp -f /root/rpmbuild/RPMS/x86_64/httpd-*.rpm /work'

