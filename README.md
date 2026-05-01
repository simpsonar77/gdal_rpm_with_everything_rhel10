# gdal_rpm_with_everything_rhel10
Fixes Redhat's stupiditiy.  Adds all of the missing drivers back into a single gdal rpm.

Redhat decided to remove nearly all of the plugins/drivers from it's gdal rpms, including those in EPEL, for RHEL 9.7 and 10.1 and up.

This includes removing even the most back of drivers like geotiff... And it went against strong urging from the gdal maintainer.  RHEL's reasoning was super weak.

This repo re-enables all of that and is based of of the rhel 10.0 source package/spec.  

Source version is 3.10.3

an Epoch of 1 is used to help keep future rhel updates from causing this package to get updated by accident.

##Build Command:
 (mkidr rpmbuild/RPMS|BUILD|BUILDROOT|SRPMS|SOURCE|SPECS) or, don't use the _topdir var and just use the default rpmbuild dir...
 rpmbuild --define "_topdir /some/path/to/rpmbuild" -bb gdal.spec 


