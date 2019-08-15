Étapes:
 - Présentation du projet                                                             I)
  - Problématiques
  - Objectifs
  - Pistes
 - Developpement de la carte virtuelle                                                II)
  - Recherche et conception
  - Idée de l'architecture
  - developpement de virt_cacard.c
 - Intégration Continue                                                               III)
  - Premier essai sur Travis-CI
  - GitLab-CI
  - CI/CD pour les images de conteneurs
 - Pull request et fin                                                                IV)
  - WIP
  - Retour sur Travis (màj)
  - Separation 

Implémenter l'intégration continue d'OpenSC sans carte à puce matérielle

L'intégration continue avec du matériel est compliquée, limite où les environements d'exécution peuvent être localisés (Contrôle d'export sur les CAC, exigences matérielle...), ce qui limite également quand les tests d'intégration peuvent être exécutés. Les tests avec des cartes physiques sont aussi moins facile à reproduire pour les contrbuteurs aux ressources limitées.

Le project consiste à implémenter l'IC d'OpenSC sur des cartes virtuelles et en utilisant GitLab-CI. 

Durant mon stage 

### Sources

 - [libcacard source](https://gitlab.freedesktop.org/spice/libcacard/)
 - [Virtual Smart Card Architecture](http://frankmorgner.github.io/vsmartcard/index.html)
 - [VPCD-Driver](https://github.com/frankmorgner/vsmartcard/blob/master/pcsc-relay/src/vpcd-driver.c)
 - [Libcacard setup](https://www.spice-space.org/smartcard-usage.html)
 - [libcacard doc](https://gitlab.freedesktop.org/spice/libcacard/blob/master/docs/libcacard.txt)
 - [PC/SC lite project](https://pcsclite.apdu.fr/)
 - [PC/SC source](https://salsa.debian.org/rousseau/PCSC)
 - [Ludovic Rousseau's Blog](https://ludovicrousseau.blogspot.com/)
 - [virt_cacard source](https://github.com/PL4typus/virt_cacard)
 - [virt_cacard issues](https://github.com/PL4typus/virt_cacard/issues)
 - [vpcd-selinux source](https://github.com/PL4typus/vpcd-selinux)
 - [vsmartcard-rpm, a RHEL 8 package for virtualsmartcard](https://github.com/PL4typus/vsmartcard-rpm)
 - [OpenSC Pull Request](https://github.com/OpenSC/OpenSC/pull/1757)
 - [OpenSC Official Repo](https://github.com/OpenSC/OpenSC)
 - [OpenSC fork](https://github.com/PL4typus/OpenSC)
 - [OpenSC-images repo](https://gitlab.com/PL4typus/opensc-images)
 - [OpenSC CI mirror](https://gitlab.com/PL4typus/OpenSC)
 - [OpenSC Travis CI](https://travis-ci.org/PL4typus/OpenSC)
 - [OpenSC's hardware CAC test by Jakub Jelen](https://gitlab.com/redhat-crypto/OpenSC/pipelines)
 - [GNUTLS Repo](https://gitlab.com/gnutls/gnutls)
 - [GNUTLS build-images repo](https://gitlab.com/gnutls/build-images)
 - [ISO 7816-4 section 5, Basic Organizations](https://cardwerk.com/smart-card-standard-iso7816-4-section-5-basic-organizations/)
 - [Red Hat Developer Blog](https://developers.redhat.com/blog/)
 - [Dan Walsh's Red Hat blog](https://developers.redhat.com/blog/author/rhatdan/)
 - [Controlling access to smart cards](https://access.redhat.com/blogs/766093/posts/1976313)
 - [GitLab documentation](https://docs.gitlab.com/ce/README.html)
 - [Travis documentation](https://docs.travis-ci.com/)
 - [SoftHSM website](https://www.opendnssec.org/softhsm/)
 - [SoftHSM sources](https://github.com/opendnssec/SoftHSMv2)
 - [Common Access Card](https://www.cac.mil/common-access-card/)
 - [CAC developer resources](https://www.cac.mil/common-access-card/developer-resources/)
 - [CAC specifications](https://www.cac.mil/Portals/53/Documents/Technical-Bulletin_CAC-Data-Model-Change_CAC-2-6-2b-Applet-Structure_June2009UPDATED.pdf)
