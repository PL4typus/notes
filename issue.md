### Problem Description

 - The CI with hardware is complicated, limits where the runners can be located (CAC export control, hardware requirement), which limits when it can be run. It is also less easy to reproduce hardware tests for contributors with limited ressources.
 - Travis CI doesn't offer a varied choice of up to date images to run tests. 
 
### Proposed Resolution

This proposal is about implementing OpenSC CI operating on virtual smart cards and using GitLab CI. This was done using Libcacard to emulate Common Access  Cards (CAC), but could be done with any kind of virtual smart card (for example, see the [vsmartcard project](https://github.com/frankmorgner/vsmartcard/)).
It is divided in three related sub-projects:

 - First of all, there is [virt_cacard](https://github.com/PL4typus/virt_cacard), a program using [libcacard](https://gitlab.freedesktop.org/spice/libcacard/), [virtualsmartcard's vpcd](https://github.com/frankmorgner/vsmartcard/tree/master/virtualsmartcard) and [softhsm2](https://github.com/opendnssec/SoftHSMv2) to present a virtual CAC to the user through the PC/SC interface. 
 
 <p align="center">
  <img src="https://github.com/PL4typus/notes/blob/master/virt_cacard.jpg" />
</p>
 
 - Then, I integrated [virt_cacard as a submodule for OpenSC.](https://github.com/PL4typus/OpenSC/tree/virt_cacard) I made a mirror of this repository on GitLab and [wrote CI jobs that run the p11tests on the virtual CAC](https://gitlab.com/PL4typus/OpenSC/pipelines/74197004). 
 Mirroring pulls the changes from the GitHub repo automatically and runs the CI tests as set up. For instance, this could be done with pull requests.
 - Finally, those jobs are run by GitLab shared runners using container images built using GitLab-CI [in this project](https://gitlab.com/PL4typus/opensc-images) and stored in GitLab's container registry. This is done in a similar fashion to [GnuTLS](https://gitlab.com/gnutls/gnutls)'s CI and [build-images repository](https://gitlab.com/gnutls/build-images/). 
 This gives more flexibility to test on different platforms, and also presents to the user a clear method for setting up a build environment, or to use the provided container images to try things out. 
 
 
Integrating this project to upstream and increasing the test coverage of the OpenSC will avoid future regressions and breakages already in upstream.
