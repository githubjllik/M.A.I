# Note de Synthèse (Version Adaptée)
## Méthodologie MERISE : Fondements, Évolutions et Conduite de Projets

---

**Cours :** Méthodologie d'Analyse Informatique 1 (M.A.I 1)

**Ouvrages de référence :**
- *La Méthode MERISE* — Hubert Tardieu, Arnold Rochfeld, René Colletti
- *Ingénierie des Systèmes d'Information : MERISE Deuxième Génération* — Dominique Nanci, Bernard Espinasse
- *Conduite de Projets Informatiques* — José Moréjon, Jean-René Rames

---

## Introduction

La conception des systèmes d'information constitue un défi majeur de l'informatique d'entreprise. MERISE, méthode française née à la fin des années 1970, répond à cette problématique en proposant un cadre structuré pour passer d'un besoin utilisateur à un système informatique fonctionnel et évolutif.

Les trois ouvrages étudiés offrent une vision complète de cette méthodologie. Le premier pose les bases théoriques et conceptuelles de MERISE. Le deuxième propose MERISE/2, une version modernisée intégrant les évolutions technologiques. Le troisième se concentre sur la dimension pratique de la conduite de projets.

Cette synthèse restitue les concepts fondamentaux, les modèles, les techniques et les bonnes pratiques qui font de MERISE un outil pertinent pour l'analyse et la conception des systèmes d'information.

---

## Première partie : Les fondements de MERISE

### 1. Contexte d'émergence et philosophie

MERISE est née d'un constat des années 1970 : les projets informatiques échouaient souvent en raison d'une mauvaise compréhension des besoins et d'une communication défaillante entre informaticiens et utilisateurs. Le ministère de l'Industrie français a alors lancé le développement d'une méthode nationale de conception des systèmes d'information.

Le nom "MERISE" fait référence au merisier, arbre fruitier qui nécessite du temps pour porter ses fruits mais offre ensuite une production durable. Cette métaphore traduit la philosophie de la méthode : investir du temps dans l'analyse et la conception pour obtenir un système robuste et pérenne.

**Les principes fondateurs** structurent l'ensemble de la démarche MERISE :

- **Séparation des préoccupations** : Distinguer ce qui relève des données de ce qui relève des traitements, ce qui est stable de ce qui évolue, pour maîtriser la complexité.

- **Abstraction progressive** : Partir du général pour aller vers le particulier, du conceptuel vers le physique. Chaque niveau d'abstraction a sa propre cohérence.

- **Validation permanente** : À chaque étape, vérifier que le résultat correspond aux attentes et qu'il est techniquement réalisable, en impliquant utilisateurs et informaticiens.

- **Documentation systématique** : Consigner tout ce qui est décidé, modélisé ou spécifié dans des documents normalisés servant de mémoire et d'outil de communication.

Le système d'information est défini comme la partie de l'organisation qui assure la mémorisation, le traitement et la circulation des informations nécessaires au fonctionnement de l'entreprise. Il se situe à l'interface entre le système de pilotage (qui décide) et le système opérant (qui produit). L'informatisation consiste à automatiser une partie de ce système d'information, sans le réduire au seul système informatique.

### 2. Le double axe de modélisation

L'innovation majeure de MERISE est de proposer une grille de lecture du système d'information selon deux axes complémentaires.

**Le cycle d'abstraction** distingue trois niveaux :

- **Niveau conceptuel** (Quoi ?) : Décrit ce que fait le système indépendamment de toute considération organisationnelle ou technique. Il s'intéresse à la sémantique pure, au sens des informations et des traitements.

- **Niveau logique/organisationnel** (Qui, où, quand ?) : Intègre les contraintes d'organisation sans descendre dans les détails techniques. On y définit les postes de travail, les acteurs, les sites et la répartition des tâches.

- **Niveau physique** (Comment ?) : Décrit la mise en œuvre concrète avec les moyens techniques choisis (structures de bases de données, programmes, architectures matérielles).

Cette progression garantit que les décisions sont prises dans le bon ordre : on comprend d'abord le besoin avant de choisir les outils et de définir l'organisation.

**La distinction données-traitements** offre deux perspectives complémentaires :

- **Perspective données** : Aspect statique du système, décrivant les informations manipulées, les objets du monde réel, leurs caractéristiques et leurs relations. Les données constituent la mémoire de l'organisation.

- **Perspective traitements** : Aspect dynamique du système, décrivant les activités, les processus et les événements qui déclenchent des actions. Les traitements donnent vie et valeur aux données.

**La matrice MERISE** croise ces deux axes pour obtenir six modèles :

- Au niveau conceptuel : **MCD** (Modèle Conceptuel des Données) et **MCT** (Modèle Conceptuel des Traitements)
- Au niveau logique : **MLD** (Modèle Logique des Données) et **MOT** (Modèle Organisationnel des Traitements)
- Au niveau physique : **MPD** (Modèle Physique des Données) et **MOpT** (Modèle Opérationnel des Traitements)

Cette matrice n'est pas rigide : selon les projets, certains modèles peuvent être plus ou moins développés. L'essentiel est de respecter la progression du conceptuel vers le physique et de maintenir la cohérence entre données et traitements.

### 3. La modélisation des données

**Le Modèle Conceptuel des Données (MCD)** est le modèle le plus emblématique de MERISE. Il s'appuie sur le formalisme entité-association enrichi et normalisé.

Une **entité** représente un objet du monde réel (client, produit, facture) dont le système doit mémoriser des informations. Elle est caractérisée par des propriétés et un identifiant unique.

Une **association** représente un lien sémantique entre deux ou plusieurs entités (un client passe des commandes, un employé travaille dans un service). Elle peut porter ses propres propriétés.

Les **cardinalités** précisent combien d'occurrences d'une entité peuvent être liées à une autre via une association. On distingue les cardinalités minimales (participation obligatoire ou facultative) et maximales (lien unique ou multiple). Les combinaisons classiques sont 0-1, 1-1, 0-n et 1-n.

La construction d'un MCD obéit à des règles de normalisation : chaque propriété doit être élémentaire et dépendre de la totalité de l'identifiant. Ces règles évitent les redondances et les incohérences.

**Le passage du MCD au MLD** (Modèle Logique des Données) transforme le modèle conceptuel en un modèle compatible avec la technologie de base de données choisie. Pour les bases relationnelles :

- Chaque entité devient une table, l'identifiant devient la clé primaire
- Une association un-à-plusieurs se traduit par une clé étrangère dans la table côté "plusieurs"
- Une association plusieurs-à-plusieurs devient une table de jonction
- Les propriétés des associations migrent vers les tables appropriées

Le MLD intègre également les contraintes d'intégrité (valeurs obligatoires, domaines autorisés, contraintes de vérification).

**Le Modèle Physique des Données (MPD)** traduit le MLD dans le langage du SGBD retenu (scripts SQL). Il intègre les considérations de performance : définition des index, éventuelles dénormalisations, dimensionnement des espaces de stockage. Le MPD est intimement lié à l'environnement technique.

### 4. La modélisation des traitements

**Le Modèle Conceptuel des Traitements (MCT)** décrit la dynamique du système au niveau conceptuel.

Un **événement** est un fait qui survient et déclenche une réaction du système. Il peut être externe (réception d'une commande), interne (atteinte d'une échéance) ou résultat d'une opération précédente.

Une **opération** est un ensemble d'actions déclenchées par un ou plusieurs événements et produisant des résultats. Elle est atomique (s'exécute entièrement ou pas du tout) et synchrone (s'exécute sans interruption).

La **synchronisation** définit les conditions de déclenchement d'une opération : un seul événement, plusieurs événements simultanés ou successifs (opérateurs ET et OU).

Le MCT se représente graphiquement par des diagrammes où les événements sont figurés par des ovales, les opérations par des rectangles et les flux par des flèches.

**Le Modèle Organisationnel des Traitements (MOT)** enrichit le MCT en ajoutant les dimensions organisationnelles :

- **Qui** : Postes de travail responsables (humains ou automatisés), caractérisés par leurs compétences
- **Où** : Sites ou lieux d'exécution des tâches
- **Quand** : Temporalité (tâches temps réel ou différées)

Le MOT introduit la notion de **procédure** : enchaînement de tâches réalisées par un même poste de travail et déclenchées par un même événement. Le formalisme reprend celui du MCT avec une représentation en colonnes par poste de travail et des indications temporelles.

**Le Modèle Opérationnel des Traitements (MOpT)** décrit la mise en œuvre technique : architecture applicative, transactions, interfaces utilisateur, algorithmes. Il est lié aux outils de développement et constitue la base des spécifications techniques détaillées pour les programmeurs.

---

## Deuxième partie : MERISE Deuxième Génération

### 5. Les extensions de MERISE/2

MERISE première génération présentait des limites face aux évolutions technologiques des années 1990 : architectures client-serveur, programmation orientée objet, interfaces graphiques, besoins temps réel et décisionnels. La modélisation des traitements était moins aboutie que celle des données, et l'intégration des aspects temporels était insuffisante.

**MERISE/2 propose plusieurs extensions majeures :**

**Le modèle de communication** représente les échanges d'information entre l'organisation et son environnement, ainsi qu'entre domaines internes. Il utilise la notion d'acteur (agent externe ou interne communicant avec le système) et de flux (informations échangées). Le modèle de contexte donne une vision synthétique, le modèle de flux les détaille.

**L'expression des contraintes d'intégrité** : MERISE/2 propose un langage formalisé pour les contraintes non représentables par le seul formalisme entité-association. Ces contraintes peuvent porter sur les données (exclusion, partition) ou les traitements (précédence, simultanéité).

**La modélisation du temps** introduit des concepts pour gérer l'historisation des données et la dimension temporelle des traitements. On peut modéliser l'évolution des informations dans le temps et conserver la trace de leurs valeurs successives.

**L'intégration de concepts objet** : Sans devenir une méthode objet, MERISE/2 emprunte la notion d'héritage et de généralisation/spécialisation dans le modèle de données.

### 6. Le modèle de communication

**Le diagramme de contexte**, premier modèle à construire, donne une vue d'ensemble du système dans son environnement. Au centre, le domaine d'étude (partie de l'organisation à informatiser). Autour, les acteurs externes (clients, fournisseurs, administrations, autres systèmes). Entre eux, les flux d'information échangés. Ce modèle délimite le périmètre du projet et identifie les interfaces à gérer.

**Le diagramme de flux** affine le modèle de contexte en décomposant le domaine en sous-domaines ou activités et en détaillant les flux internes. Chaque activité représente un ensemble cohérent de tâches. Ce modèle permet de comprendre le fonctionnement global et d'identifier les grandes fonctions du système. Il sert de base à la décomposition du projet en lots.

### 7. Les extensions du modèle de données

**La généralisation et la spécialisation** permettent de représenter qu'une entité peut avoir des sous-types héritant de ses propriétés tout en ayant des propriétés propres. Par exemple, PERSONNE peut être spécialisée en CLIENT et EMPLOYE. Les propriétés communes (nom, adresse) sont portées par l'entité générique, les propriétés spécifiques (chiffre d'affaires, salaire) par les entités spécialisées. Cette modélisation est contrainte par des règles de couverture (toute occurrence appartient-elle nécessairement à un sous-type ?) et d'exclusion (peut-elle appartenir à plusieurs sous-types simultanément ?).

**Les contraintes d'intégrité étendues** enrichissent la typologie :
- Contraintes intra-association (totalité, exclusion)
- Contraintes inter-associations (inclusion, égalité, exclusion, partition)
- Contraintes sur les propriétés (domaine, format, contraintes calculées)

**La dimension temporelle des données** introduit l'historisation :
- Des propriétés : conserver les valeurs successives (adresses d'un client)
- Des associations : conserver la trace des liens (affectations d'un employé)
- Des occurrences : conserver les entités disparues (clients inactifs)

Ces mécanismes sont matérialisés par des notations spécifiques et donnent lieu à des structures particulières dans le modèle physique.

### 8. L'évolution de la modélisation des traitements

MERISE/2 enrichit la modélisation des traitements en s'appuyant sur le modèle de flux. Chaque activité peut être détaillée par un sous-modèle décrivant son fonctionnement interne, permettant une décomposition hiérarchique gérant la complexité par raffinements successifs.

La **typologie des événements** s'affine : externes (provenant de l'environnement), internes (résultant du système) et temporels (liés à des échéances). Les opérations sont mieux caractérisées : nature interactive ou automatique, mode de déclenchement temps réel ou différé, impact sur les données (consultation ou mise à jour).

**La cohérence données-traitements** doit être systématiquement vérifiée : chaque entité et propriété du MCD doit être utilisée par au moins un traitement ; inversement, chaque traitement ne manipule que des données définies dans le MCD. Les règles de gestion exprimées comme contraintes d'intégrité doivent être cohérentes avec les traitements qui les mettent en œuvre.

---

## Troisième partie : La conduite de projets informatiques

### 9. Le cycle de vie d'un projet

**Le schéma directeur** (étape préliminaire) définit la stratégie informatique de l'organisation à moyen terme : domaines à informatiser, priorités, moyens à mettre en œuvre.

**L'étude préalable** (première étape d'un projet spécifique) analyse l'existant, recueille les besoins et propose des solutions d'ensemble. Elle débouche sur un dossier de choix permettant la décision de lancement et la sélection de la solution.

**L'étude détaillée** approfondit la solution retenue en produisant les spécifications fonctionnelles complètes (ce que doit faire le système). Les modèles conceptuels et organisationnels sont élaborés.

**L'étude technique** traduit les spécifications fonctionnelles en spécifications techniques : architecture, choix technologiques, structures physiques, spécifications des programmes. Les modèles physiques sont élaborés.

**La réalisation** développe, teste et documente les programmes et bases de données.

**La mise en œuvre** déploie le système en production, forme les utilisateurs et assure la transition.

**La maintenance** corrige les anomalies et fait évoluer le système après sa mise en service.

Chaque étape produit des **livrables normalisés** (documents de spécification, modèles, programmes, manuels) et se termine par un **point de décision** (jalon ou revue) validant le passage à l'étape suivante. La revue de fin d'étude préalable valide le périmètre, le budget, le délai et la solution. La revue de fin d'étude détaillée valide les spécifications fonctionnelles. La recette fonctionnelle valide la conformité du système développé.

### 10. L'organisation du projet

**Les acteurs du projet** ont des rôles distincts :

- **Maître d'ouvrage** : Client du projet, exprime le besoin, finance et valide le résultat. Responsable du périmètre fonctionnel et de la recette finale.

- **Maître d'œuvre** : Réalisateur du projet, conçoit et développe la solution. Responsable de la qualité technique, des délais et du budget.

- **Comité de pilotage** : Réunit les représentants au plus haut niveau, prend les décisions stratégiques, arbitre les conflits et valide les livrables majeurs.

- **Chef de projet maîtrise d'ouvrage** : Coordonne côté client, s'assure de la bonne expression des besoins et de la disponibilité des utilisateurs.

- **Chef de projet maîtrise d'œuvre** : Coordonne la conception et le développement, gère l'équipe, le planning, les risques et la qualité.

- **Utilisateurs** : Participent à l'expression des besoins, aux validations et à la recette finale. Leur implication est un facteur clé de succès.

**Les instances de pilotage** structurent le projet :

- **Comité de pilotage** : Se réunit mensuellement pour suivre l'avancement global et prendre les décisions stratégiques.

- **Comité de projet** : Se réunit hebdomadairement, traite les problèmes courants et prépare les décisions du comité de pilotage.

- **Groupes de travail thématiques** : Approfondissent certains sujets (ergonomie, reprise de données, formation).

**La communication** doit être organisée et formalisée : communication interne à l'équipe (réunions, documents partagés), communication vers les parties prenantes (comptes rendus, présentations), communication de crise (préparée à l'avance pour faire face aux difficultés majeures).

### 11. La planification et le suivi

**L'estimation des charges** conditionne le budget et le calendrier. Plusieurs méthodes existent :

- Estimation par analogie (référence à des projets similaires)
- Estimation paramétrique (ratios comme jours par point de fonction)
- Estimation analytique (décomposition en tâches élémentaires)

L'estimation doit être réaliste avec une marge pour risques (10 à 30 % selon l'incertitude) et révisée régulièrement.

**La planification** ordonnance les tâches dans le temps selon les contraintes de dépendance, de ressources et de délais. Le diagramme de Gantt représente les tâches sous forme de barres positionnées sur une échelle de temps. La méthode PERT identifie le chemin critique (enchaînement déterminant la durée minimale du projet). La planification distingue un planning macro (vision d'ensemble) et des plannings détaillés (phases en cours).

**Le suivi d'avancement** compare régulièrement la situation réelle à la situation prévue. Les indicateurs portent sur les délais, les charges et les livrables. Le reste à faire doit être réévalué : un projet ayant consommé 80 % du budget peut n'être qu'à 50 % d'avancement réel. Les réunions d'avancement permettent le reporting et la mise à jour du planning.

### 12. La gestion des risques

**L'identification des risques** doit être réalisée dès le début et mise à jour régulièrement. Les risques peuvent être techniques (complexité, performances), fonctionnels (adéquation aux besoins), organisationnels (disponibilité des ressources) ou contractuels (relations avec les prestataires).

**L'évaluation et la priorisation** se font selon deux dimensions : probabilité d'occurrence et impact. En croisant ces dimensions, on obtient un niveau de criticité permettant de prioriser. Une matrice des risques visualise cette priorisation.

**Le traitement des risques** utilise plusieurs stratégies :

- **Évitement** : Modifier le projet pour supprimer le risque
- **Réduction** : Diminuer la probabilité ou l'impact (formation, tests renforcés)
- **Transfert** : Faire porter le risque par un tiers (sous-traitance, assurance)
- **Acceptation** : Ne rien faire en étant conscient du risque (adaptée aux faibles criticités)

Un plan de contingence prépare les actions si le risque se concrétise.

### 13. La qualité dans les projets

**Les dimensions de la qualité** sont multiples :

- Conformité fonctionnelle (adéquation aux besoins)
- Fiabilité (fonctionnement sans défaillance, résultats corrects)
- Performance (temps de réponse, capacité de charge)
- Utilisabilité (facilité d'utilisation)
- Maintenabilité (facilité de correction et d'évolution)
- Sécurité (protection contre les accès non autorisés)

**L'assurance qualité** s'appuie sur un plan qualité décrivant les objectifs, les moyens et les indicateurs. Elle utilise :

- **Revues** : Examens formels des livrables par des pairs ou experts (spécifications, conception, code)
- **Audits** : Examens du respect des processus définis
- **Tests** : Vérifications du bon fonctionnement (unitaires, d'intégration, système, recette)

**La gestion de configuration** maîtrise l'évolution des livrables avec des outils de gestion de versions traçant toutes les modifications. Chaque livrable est identifié de manière unique et son évolution est suivie. Les changements sont formalisés par des demandes évaluées et approuvées.

---

## Quatrième partie : Approfondissements

### 14. L'expression des besoins

L'expression des besoins conditionne tout le projet. Si les besoins sont mal compris ou incomplets, le système ne satisfera pas les utilisateurs.

**Les sources d'information** sont multiples : documents existants (procédures, formulaires), entretiens avec utilisateurs et responsables métier, observation du travail réel, systèmes analogues dans d'autres organisations.

**Les techniques de recueil** incluent :

- Entretien individuel (échange approfondi, sujets sensibles)
- Entretien de groupe (confrontation de points de vue, émergence de consensus)
- Questionnaire (grand nombre de personnes, questions fermées)
- Atelier de travail (production collaborative, implication et créativité)

**La formalisation des besoins** structure les informations recueillies :

- Exigences fonctionnelles (ce que le système doit faire)
- Exigences non fonctionnelles (qualités attendues : performances, disponibilité, sécurité, ergonomie)
- Contraintes (éléments imposés : technologies, interfaces, réglementations)
- Règles de gestion (politiques métier à mettre en œuvre)

### 15. La conception des interfaces

**L'ergonomie des interfaces** conditionne l'acceptation du système. Les principes d'ergonomie incluent :

- Cohérence (mêmes actions de la même manière)
- Visibilité (état du système toujours perceptible)
- Feedback (chaque action reçoit une réponse)
- Prévention des erreurs (empêcher les actions incorrectes)
- Réversibilité (possibilité d'annuler)

**La maquette** (représentation visuelle des écrans) permet de valider l'ergonomie et la navigation avant développement. Elle peut être réalisée sur papier ou avec des outils de maquettage.

**Le prototype** (version simplifiée mais fonctionnelle) valide l'ergonomie et certains aspects techniques. Le prototypage itératif enrichit progressivement le prototype jusqu'au système final. Ces techniques réduisent les risques de rejet et les coûts de modification tardive.

### 16. La reprise de l'existant

**La reprise des données** est généralement nécessaire. Elle comprend :

- Analyse des données existantes (quoi reprendre, qualité, signification, format)
- Transformation (conversion de l'ancien vers le nouveau format)
- Nettoyage (correction des erreurs, complément des manques, harmonisation)
- Migration effective (planification de la fenêtre de migration)

**Le basculement** (passage de l'ancien au nouveau système) utilise plusieurs stratégies :

- Basculement direct (simple mais risqué)
- Fonctionnement en parallèle (sécurisant mais coûteux)
- Basculement progressif (par étapes, limite les risques mais allonge la transition)

Un plan de retour arrière doit toujours être prévu.

---

## Conclusion

Cette synthèse des trois ouvrages de référence sur MERISE montre la richesse et la cohérence de cette méthode française qui a marqué l'ingénierie des systèmes d'information.

**Les apports fondamentaux de MERISE sont :**

- Un cadre de pensée structuré avec séparation en niveaux d'abstraction et distinction données-traitements
- Un ensemble de modèles formalisés précis mais accessibles
- Une organisation du projet en étapes balisées par des livrables et validations
- Une implication permanente des utilisateurs tout au long du projet

**Les évolutions** témoignent de la capacité d'adaptation de MERISE : intégration de concepts objet dans MERISE/2, ouverture vers les architectures distribuées, compatibilité possible avec des approches agiles.

**Les limites** invitent à l'adaptation : lourdeur parfois disproportionnée pour les petits projets, difficulté à gérer les changements tardifs dans un cycle en cascade, ancrage dans un monde de bases relationnelles et d'applications transactionnelles. Ces limites n'invalident pas la méthode mais invitent à l'utiliser avec discernement.

Au-delà des outils et techniques, MERISE propose une philosophie durable : informatique au service des utilisateurs, conception rigoureuse mais pragmatique, dialogue permanent entre maîtrise d'ouvrage et maîtrise d'œuvre. Les concepts fondamentaux (abstraction progressive, séparation des préoccupations, modélisation structurée) restent des acquis qui transcendent les évolutions technologiques et servent de base même à l'utilisation d'autres méthodes comme UML ou les approches agiles.

---

**Glossaire des termes clés :**

**Association** : Lien sémantique entre entités dans le MCD  
**Cardinalité** : Nombre min/max d'occurrences d'une entité dans une association  
**Entité** : Objet du monde réel dont le SI mémorise des informations  
**Événement** : Fait déclenchant une réaction du système  
**Maître d'ouvrage** : Client du projet, responsable des besoins et de la validation  
**Maître d'œuvre** : Réalisateur du projet, responsable de la conception et du développement  
**MCD** : Modèle Conceptuel des Données  
**MCT** : Modèle Conceptuel des Traitements  
**MLD** : Modèle Logique des Données  
**MOT** : Modèle Organisationnel des Traitements  
**MPD** : Modèle Physique des Données  
**Opération** : Ensemble d'actions déclenchées par des événements  
**Propriété** : Caractéristique élémentaire d'une entité ou association  
**Règle de gestion** : Politique métier à mettre en œuvre

---

*Fin de la note de synthèse adaptée*