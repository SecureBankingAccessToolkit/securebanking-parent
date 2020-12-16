# Git Changelog Maven plugin changelog
Changelog of Git Changelog Maven plugin.
## Unreleased
### GitHub [#1](https://github.com/SecureBankingAcceleratorToolkit/securebanking-parent/pull/1) 4: Use current version of spring
[4a3c414a922e89c](https://github.com/SecureBankingAcceleratorToolkit/securebanking-openbanking-aspsp/commit/4a3c414a922e89c) Jamie Bowen *2020-11-19 13:20:35*
4: Use current version of spring (#1)

Part of https://github.com/SecureBankingAcceleratorToolkit/SecureBankingAcceleratorToolkit/issues/4
### GitHub [#10](https://github.com/SecureBankingAcceleratorToolkit/securebanking-parent/pull/10) 4: Publish SNAPSHOT release on merge to master
[49242001cf477e0](https://github.com/SecureBankingAcceleratorToolkit/securebanking-openbanking-aspsp/commit/49242001cf477e0) Jamie Bowen *2020-12-10 13:59:51*
4: Publish SNAPSHOT release on merge to master (#10)

Separated the action out. Now have merge-master action and check-build.
Merge-master action will publish a SNAPSHOT release when merging to
master.

Full releases must be managed locally to perform the release and then
when a release is created in github the release artifact will be
pubished.

Issue: https://github.com/SecureBankingAcceleratorToolkit/SecureBankingAcceleratorToolkit/issues/4
### GitHub [#11](https://github.com/SecureBankingAcceleratorToolkit/securebanking-parent/pull/11) 4: Publish SNAPSHOT release on merge to master
[b913a04d8498bc3](https://github.com/SecureBankingAcceleratorToolkit/securebanking-openbanking-aspsp/commit/b913a04d8498bc3) Jamie Bowen *2020-12-10 16:20:54*
4: Publish SNAPSHOT release on merge to master (#11)

Separated the action out. Now have merge-master action and check-build.
Merge-master action will publish a SNAPSHOT release when merging to
master.

Full releases must be managed locally to perform the release and then
when a release is created in github the release artifact will be
pubished.

Issue: https://github.com/SecureBankingAcceleratorToolkit/SecureBankingAcceleratorToolkit/issues/4
### GitHub [#12](https://github.com/SecureBankingAcceleratorToolkit/securebanking-parent/pull/12) 4: Publish SNAPSHOT release on merge to master
[4611923c265cf37](https://github.com/SecureBankingAcceleratorToolkit/securebanking-openbanking-aspsp/commit/4611923c265cf37) Jamie Bowen *2020-12-11 14:10:58*
4: Publish SNAPSHOT release on merge to master (#9) (#12)

Separated the action out. Now have merge-master action and check-build.
Merge-master action will publish a SNAPSHOT release when merging to
master.

Full releases must be managed locally to perform the release and then
when a release is created in github the release artifact will be
pubished.

Issue: https://github.com/SecureBankingAcceleratorToolkit/SecureBankingAcceleratorToolkit/issues/4
### GitHub [#13](https://github.com/SecureBankingAcceleratorToolkit/securebanking-parent/pull/13) 4: Update snapshots and remove bad spring-boot-starter-test
[ebc30582019ebb5](https://github.com/SecureBankingAcceleratorToolkit/securebanking-openbanking-aspsp/commit/ebc30582019ebb5) Jamie Bowen *2020-12-11 15:50:58*
4: Update snapshots and remove bad spring-boot-starter-test (#13)

In trying to exclude junit4 from spring-boot-starter-test I was
overriding the import from the spring-boot-dependencies bom and hiding
the version!

Issue: https://github.com/SecureBankingAcceleratorToolkit/SecureBankingAcceleratorToolkit/issues/4
### GitHub [#14](https://github.com/SecureBankingAcceleratorToolkit/securebanking-parent/pull/14) 27: Add dependencies for aspsp-simulator
[df3d32d82f5e2dd](https://github.com/SecureBankingAcceleratorToolkit/securebanking-openbanking-aspsp/commit/df3d32d82f5e2dd) Matt Wills *2020-12-16 09:27:20*
27: Add dependencies for aspsp-simulator (#14)

- Add required depdendencies
    - Strip out JUnit 4

Issue: https://github.com/SecureBankingAcceleratorToolkit/SecureBankingAcceleratorToolkit/issues/27
### GitHub [#2](https://github.com/SecureBankingAcceleratorToolkit/securebanking-parent/pull/2) 4: Use secure banking BOM and spring BOM
[989bdb467d4f87b](https://github.com/SecureBankingAcceleratorToolkit/securebanking-openbanking-aspsp/commit/989bdb467d4f87b) Jamie Bowen *2020-11-27 17:22:21*
4: Use secure banking BOM and spring BOM (#2)

Also adds a read me and some more 3rd party dependencies
Issue: https://github.com/SecureBankingAcceleratorToolkit/SecureBankingAcceleratorToolkit/issues/4
### GitHub [#3](https://github.com/SecureBankingAcceleratorToolkit/securebanking-parent/pull/3) 4: Refactor how Java 14 is specified
[dfd4913232b2ad4](https://github.com/SecureBankingAcceleratorToolkit/securebanking-openbanking-aspsp/commit/dfd4913232b2ad4) Jamie Bowen *2020-11-30 16:24:20*
4: Refactor how Java 14 is specified (#3)

After testing, and also getting JAVA_HOME set to the right JDK in
/etc/profile.d/jdk.sh (on Ubuntu 20.04) then I could be much more hands
off with regard to specifying the java version. I no longer need to have
the maven-complier-plugin specify which javac compiler to use!

Removed the import of the securbanking-bom

After discussion with the team it was felt that the best approach would
be to not include all versions in an imported parent bom. This leads to
circular dependencies when you update the bom with latest versions,
update the parent pom to use the latest bom, then need to update all the
child projects that use the parent... not good.

So instead we will use a bom file in the securebanking-commons library
that may be imported into clients such as the securebanking-rcs or
securebanking-openbanking-aspsp projects.

Issue: https://github.com/SecureBankingAcceleratorToolkit/SecureBankingAcceleratorToolkit/issues/4
### GitHub [#4](https://github.com/SecureBankingAcceleratorToolkit/securebanking-parent/pull/4) Create check build github action
[f05aa038c63df9f](https://github.com/SecureBankingAcceleratorToolkit/securebanking-openbanking-aspsp/commit/f05aa038c63df9f) Jamie Bowen *2020-12-01 10:54:09*
Create check build github action (#4)

Checks the build integrity on creation of a pr or a push to master. i.e.
when a PR is create, and when code is merged into master

Issue: https://github.com/SecureBankingAcceleratorToolkit/SecureBankingAcceleratorToolkit/issues/4
### GitHub [#5](https://github.com/SecureBankingAcceleratorToolkit/securebanking-parent/pull/5) 12: Manage securebanking-common dependencies
[38e6fa427151584](https://github.com/SecureBankingAcceleratorToolkit/securebanking-openbanking-aspsp/commit/38e6fa427151584) Jamie Bowen *2020-12-02 14:03:12*
12: Manage securebanking-common dependencies (#5)

While addressing PR comments for https://github.com/SecureBankingAcceleratorToolkit/securebanking-common/pull/1
I have moved some of the dependencies that were being managed in
securebanking-common-openbanking-uk-datamodel into the parent pom

Issue: https://github.com/SecureBankingAcceleratorToolkit/SecureBankingAcceleratorToolkit/issues/12
### GitHub [#6](https://github.com/SecureBankingAcceleratorToolkit/securebanking-parent/pull/6) Runs a license header check when building
[a8815ea89e8dde9](https://github.com/SecureBankingAcceleratorToolkit/securebanking-openbanking-aspsp/commit/a8815ea89e8dde9) Jamie Bowen *2020-12-09 10:17:48*
Runs a license header check when building (#6)

The license header check was failing in the github actions and needed
fixing.

Issue: https://github.com/SecureBankingAcceleratorToolkit/SecureBankingAcceleratorToolkit/issues/4
### GitHub [#7](https://github.com/SecureBankingAcceleratorToolkit/securebanking-parent/pull/7) Places license at top of file using JAVADOC_STYLE
[8400cec9f2867c4](https://github.com/SecureBankingAcceleratorToolkit/securebanking-openbanking-aspsp/commit/8400cec9f2867c4) Jamie Bowen *2020-12-09 14:21:52*
Places license at top of file using JAVADOC_STYLE (#7)

The JAVADOC_STYLE is more familiar and I can see no benefit to having
the license placed after the package declaration in the .java file.

Issue: https://github.com/SecureBankingAcceleratorToolkit/SecureBankingAcceleratorToolkit/issues/4
### GitHub [#8](https://github.com/SecureBankingAcceleratorToolkit/securebanking-parent/pull/8) 4: Publish to artifactory when a release is made
[8043fd258e8bb47](https://github.com/SecureBankingAcceleratorToolkit/securebanking-openbanking-aspsp/commit/8043fd258e8bb47) Jamie Bowen *2020-12-10 11:53:03*
4: Publish to artifactory when a release is made (#8)

Issue: https://github.com/SecureBankingAcceleratorToolkit/SecureBankingAcceleratorToolkit/issues/4
### GitHub [#9](https://github.com/SecureBankingAcceleratorToolkit/securebanking-parent/pull/9) 4: Publish SNAPSHOT release on merge to master
[4611923c265cf37](https://github.com/SecureBankingAcceleratorToolkit/securebanking-openbanking-aspsp/commit/4611923c265cf37) Jamie Bowen *2020-12-11 14:10:58*
4: Publish SNAPSHOT release on merge to master (#9) (#12)

Separated the action out. Now have merge-master action and check-build.
Merge-master action will publish a SNAPSHOT release when merging to
master.

Full releases must be managed locally to perform the release and then
when a release is created in github the release artifact will be
pubished.

Issue: https://github.com/SecureBankingAcceleratorToolkit/SecureBankingAcceleratorToolkit/issues/4
[a4134d970650a0d](https://github.com/SecureBankingAcceleratorToolkit/securebanking-openbanking-aspsp/commit/a4134d970650a0d) Jamie Bowen *2020-12-10 13:43:58*
4: Publish SNAPSHOT release on merge to master (#9)

Separated the action out. Now have merge-master action and check-build.
Merge-master action will publish a SNAPSHOT release when merging to
master.

Full releases must be managed locally to perform the release and then
when a release is created in github the release artifact will be
pubished.

Issue: https://github.com/SecureBankingAcceleratorToolkit/SecureBankingAcceleratorToolkit/issues/4
[29dd01620d0a457](https://github.com/SecureBankingAcceleratorToolkit/securebanking-openbanking-aspsp/commit/29dd01620d0a457) JamieB *2020-11-19 09:45:19*
Initial commit
