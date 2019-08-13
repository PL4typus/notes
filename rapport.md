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


### Sources


