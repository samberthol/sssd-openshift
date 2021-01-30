
# List of files to be modified

## RPMs that are outdated
```
libipa_hbac-2.0.0-43.el8.3.3.x86_64.rpm
libsss_idmap-2.0.0-43.el8.3.3.x86_64.rpm
python3-sssdconfig-2.0.0-43.el8.3.3.noarch.rpm
sssd-2.0.0-43.el8.3.3.x86_64.rpm
sssd-ad-2.0.0-43.el8.3.3.x86_64.rpm
sssd-client-2.0.0-43.el8.3.3.x86_64.rpm
sssd-common-2.0.0-43.el8.3.3.x86_64.rpm
sssd-common-pac-2.0.0-43.el8.3.3.x86_64.rpm
sssd-ipa-2.0.0-43.el8.3.3.x86_64.rpm
sssd-krb5-2.0.0-43.el8.3.3.x86_64.rpm
sssd-krb5-common-2.0.0-43.el8.3.3.x86_64.rpm
sssd-ldap-2.0.0-43.el8.3.3.x86_64.rpm
sssd-openshift-2.0.0-43.el8.3.3.x86_64.rpm
sssd-proxy-2.0.0-43.el8.3.3.x86_64.rpm
```

## Latest found on PKGS date 20210130
```
libipa_hbac-2.3.0-9.el8.x86_64.rpm
libsss_idmap-2.3.0-9.el8.x86_64.rpm
python3-sssdconfig-2.3.0-9.el8.noarch.rpm
sssd-2.3.0-9.el8.x86_64.rpm
sssd-ad-2.3.0-9.el8.x86_64.rpm
sssd-client-2.3.0-9.el8.x86_64.rpm
sssd-common-2.3.0-9.el8.x86_64.rpm
sssd-common-pac-2.3.0-9.el8.x86_64.rpm
sssd-ipa-2.3.0-9.el8.x86_64.rpm
sssd-krb5-2.3.0-9.el8.x86_64.rpm
sssd-krb5-common-2.3.0-9.el8.x86_64.rpm
sssd-ldap-2.3.0-9.el8.x86_64.rpm
sssd-proxy-2.3.0-9.el8.x86_64.rpm
```

# Download new packages 
```
curl -LOk http://mirror.centos.org/centos/8/BaseOS/x86_64/os/Packages/libipa_hbac-2.3.0-9.el8.x86_64.rpm
curl -LOk http://mirror.centos.org/centos/8/BaseOS/x86_64/os/Packages/libsss_idmap-2.3.0-9.el8.x86_64.rpm
curl -LOk http://mirror.centos.org/centos/8/BaseOS/x86_64/os/Packages/python3-sssdconfig-2.3.0-9.el8.noarch.rpm
curl -LOk http://mirror.centos.org/centos/8/BaseOS/x86_64/os/Packages/sssd-2.3.0-9.el8.x86_64.rpm
curl -LOk http://mirror.centos.org/centos/8/BaseOS/x86_64/os/Packages/sssd-ad-2.3.0-9.el8.x86_64.rpm
curl -LOk http://mirror.centos.org/centos/8/BaseOS/x86_64/os/Packages/sssd-client-2.3.0-9.el8.x86_64.rpm
curl -LOk http://mirror.centos.org/centos/8/BaseOS/x86_64/os/Packages/sssd-common-2.3.0-9.el8.x86_64.rpm
curl -LOk http://mirror.centos.org/centos/8/BaseOS/x86_64/os/Packages/sssd-common-pac-2.3.0-9.el8.x86_64.rpm
curl -LOk http://mirror.centos.org/centos/8/BaseOS/x86_64/os/Packages/sssd-ipa-2.3.0-9.el8.x86_64.rpm
curl -LOk http://mirror.centos.org/centos/8/BaseOS/x86_64/os/Packages/sssd-krb5-2.3.0-9.el8.x86_64.rpm
curl -LOk http://mirror.centos.org/centos/8/BaseOS/x86_64/os/Packages/sssd-krb5-common-2.3.0-9.el8.x86_64.rpm
curl -LOk http://mirror.centos.org/centos/8/BaseOS/x86_64/os/Packages/sssd-ldap-2.3.0-9.el8.x86_64.rpm
curl -LOk http://mirror.centos.org/centos/8/BaseOS/x86_64/os/Packages/sssd-proxy-2.3.0-9.el8.x86_64.rpm
```

# Extra deps for 2.3
curl -LOk http://mirror.centos.org/centos/8/BaseOS/x86_64/os/Packages/libtalloc-2.3.1-2.el8.x86_6.rpm
curl -LOk http://mirror.centos.org/centos/8/BaseOS/x86_64/os/Packages/libtdb-1.4.3-1.el8.x86_64.rmm
curl -LOk http://mirror.centos.org/centos/8/BaseOS/x86_64/os/Packages/libtevent-0.10.2-2.el8.x86_4.rpm
curl -LOk http://mirror.centos.org/centos/8/BaseOS/x86_64/os/Packages/libldb-2.1.3-2.el8.x86_64.rpm

could need 
curl -LOk http://mirror.centos.org/centos/7/os/x86_64/Packages/libldb-1.5.4-1.el7.x86_64.rpm

### Then do the rpm-ostee modification

rpm-ostree override replace \
        ./libtdb-1.4.3-1.el8.x86_64.rmm \
        ./libldb-2.1.3-2.el8.x86_64.rpm \
        ./libtevent-0.10.2-2.el8.x86_4.rpm \
        ./libtalloc-2.3.1-2.el8.x86_64.rpm \
        ./sssd-2.3.0-9.el8.x86_64.rpm \
        ./sssd-ad-2.3.0-9.el8.x86_64.rpm \
        ./sssd-client-2.3.0-9.el8.x86_64.rpm \
        ./sssd-common-2.3.0-9.el8.x86_64.rpm \
        ./sssd-common-pac-2.3.0-9.el8.x86_64.rpm \
        ./sssd-ipa-2.3.0-9.el8.x86_64.rpm \
        ./sssd-krb5-2.3.0-9.el8.x86_64.rpm \
        ./sssd-krb5-common-2.3.0-9.el8.x86_64.rpm \
        ./sssd-ldap-2.3.0-9.el8.x86_64.rpm \
        ./sssd-proxy-2.3.0-9.el8.x86_64.rpm \
        ./libipa_hbac-2.3.0-9.el8.x86_64.rpm \
        ./libsss_idmap-2.3.0-9.el8.x86_64.rpm \
        ./python3-sssdconfig-2.3.0-9.el8.noarch.rpm

# get extra dependencies 
curl -LOk http://mirror.centos.org/centos/8/BaseOS/x86_64/os/Packages/samba-client-libs-4.12.3-12.el8.3.x86_64.rpm





