OSG Software Stack -- Data Release -- 3.4.4-2
=============================================

**Release Date**: 2017-10-11

Summary of changes
------------------

This release contains:

-   CA Certificates based on [IGTF 1.86](http://dist.eugridpma.info/distribution/igtf/current/CHANGES)
    - updated MaGrid CA with extended validity period (MA)
    - removed discontinued pkIRISGrid CA (ES)
-   [VO Package v75](https://github.com/opensciencegrid/osg-vo-config/releases/tag/release-75)
    - Add CMS wildcard to default map file

These [JIRA tickets](https://jira.opensciencegrid.org/issues/?jql=project%20%3D%20SOFTWARE%20AND%20fixVersion%20%3D%203.4.4-2%20ORDER%20BY%20priority%20DESC%2C%20key%20DESC) were addressed in this release.

Detailed changes are below. All of the documentation can be found [here](../../).

Updating to the new release
---------------------------

### Update Repositories

To update to this series, you need [install the current OSG repositories](../../common/yum#install-osg-repositories).

### Update Software

Once the repositories are installed, you can update to this new release with:

``` console
root@host # yum update
```

!!! note
    Please be aware that running `yum update` may also update other RPMs. You can exclude packages from being updated using the `--exclude=[package-name or glob]` option for the `yum` command.

!!! note
    Watch the yum update carefully for any messages about a `.rpmnew` file being created. That means that a configuration file had been editted, and a new default version was to be installed. In that case, RPM does not overwrite the editted configuration file but instead installs the new version with a `.rpmnew` extension. You will need to merge any edits that have made into the `.rpmnew` file and then move the merged version into place (that is, without the `.rpmnew` extension). Watch especially for `/etc/lcmaps.db`, which every site is expected to edit.

Need help?
----------

Do you need help with this release? [Contact us for help](../../common/help).

Detailed changes in this release
--------------------------------

### Packages

We added or updated the following packages to the production OSG yum repository. Note that in some cases, there are multiple RPMs for each package. You can click on any given package to see the set of RPMs or see the complete list below.

#### Enterprise Linux 6

-   [igtf-ca-certs-1.86-1.osg34.el6](https://koji.chtc.wisc.edu/koji/search?match=glob&type=build&terms=igtf-ca-certs-1.86-1.osg34.el6)
-   [osg-ca-certs-1.66-1.osg34.el6](https://koji.chtc.wisc.edu/koji/search?match=glob&type=build&terms=osg-ca-certs-1.66-1.osg34.el6)
-   [vo-client-75-1.osg34.el6](https://koji.chtc.wisc.edu/koji/search?match=glob&type=build&terms=vo-client-75-1.osg34.el6)

#### Enterprise Linux 7

-   [igtf-ca-certs-1.86-1.osg34.el7](https://koji.chtc.wisc.edu/koji/search?match=glob&type=build&terms=igtf-ca-certs-1.86-1.osg34.el7)
-   [osg-ca-certs-1.66-1.osg34.el7](https://koji.chtc.wisc.edu/koji/search?match=glob&type=build&terms=osg-ca-certs-1.66-1.osg34.el7)
-   [vo-client-75-1.osg34.el7](https://koji.chtc.wisc.edu/koji/search?match=glob&type=build&terms=vo-client-75-1.osg34.el7)

### RPMs

If you wish to manually update your system, you can run yum update against the following packages:

    igtf-ca-certs osg-ca-certs osg-gums-config vo-client vo-client-edgmkgridmap vo-client-lcmaps-voms

If you wish to only update the RPMs that changed, the set of RPMs is:

#### Enterprise Linux 6

``` file
igtf-ca-certs-1.86-1.osg34.el6
osg-ca-certs-1.66-1.osg34.el6
osg-gums-config-75-1.osg34.el6
vo-client-75-1.osg34.el6
vo-client-edgmkgridmap-75-1.osg34.el6
vo-client-lcmaps-voms-75-1.osg34.el6
```

#### Enterprise Linux 7

``` file
igtf-ca-certs-1.86-1.osg34.el7
osg-ca-certs-1.66-1.osg34.el7
osg-gums-config-75-1.osg34.el7
vo-client-75-1.osg34.el7
vo-client-edgmkgridmap-75-1.osg34.el7
vo-client-lcmaps-voms-75-1.osg34.el7
```
