# Note de Synthèse Condensée
## Méthodologie MERISE : Fondements et Conduite de Projets

**Cours :** Méthodologie d'Analyse Informatique 1 (M.A.I 1)

**Ouvrages de référence :**
- *La Méthode MERISE* — Hubert Tardieu, Arnold Rochfeld, René Colletti
- *Ingénierie des Systèmes d'Information : MERISE Deuxième Génération* — Dominique Nanci, Bernard Espinasse
- *Conduite de Projets Informatiques* — José Moréjon, Jean-René Rames

---

## Introduction

MERISE est une méthode française de conception de systèmes d'information née à la fin des années 1970 suite à un appel d'offres du ministère de l'Industrie. Tardieu, Rochfeld et Colletti en posent les fondements théoriques, tandis que Nanci et Espinasse proposent une version modernisée (MERISE/2) et que Moréjon et Rames se concentrent sur les aspects pratiques de gestion de projets. Cette synthèse restitue les concepts essentiels articulant modèles, techniques et bonnes pratiques qui font la pertinence durable de MERISE.

---

## I. Les fondements de MERISE selon Tardieu, Rochfeld et Colletti

### 1. Contexte et philosophie

Face aux échecs répétés de projets informatiques dans les années 1970, MERISE répond à un besoin de méthode structurée. Le nom évoque le merisier, arbre nécessitant du temps pour porter des fruits durables, métaphore du système d'information robuste.

Les **principes fondateurs** structurent la démarche :
- **Séparation des préoccupations** : distinguer données/traitements, stable/évolutif, organisationnel/technique pour maîtriser la complexité
- **Abstraction progressive** : du général au particulier, du conceptuel au physique
- **Validation permanente** : vérification à chaque étape de l'adéquation aux attentes
- **Documentation systématique** : traçabilité et communication entre intervenants

Le **système d'information** est défini comme la partie de l'organisation assurant mémorisation, traitement et circulation des informations. Il dépasse le système informatique en incluant procédures manuelles et échanges informels.

### 2. Le double axe de modélisation

L'innovation majeure de MERISE réside dans sa grille bidimensionnelle :

**L'axe d'abstraction** distingue trois niveaux :
- **Niveau conceptuel** : "quoi ?" - la sémantique pure, indépendante de l'organisation et de la technique
- **Niveau logique/organisationnel** : "qui, où, quand ?" - l'intégration des contraintes d'organisation
- **Niveau physique** : "comment ?" - la mise en œuvre technique concrète

**L'axe données-traitements** sépare :
- **Perspective données** : aspect statique, ce qui persiste (mémoire de l'organisation)
- **Perspective traitements** : aspect dynamique, ce qui transforme les données

Le **croisement des axes** génère une matrice à six cases : MCD/MCT (conceptuel), MLD/MOT (logique), MPD/MOpT (physique). Cette structuration garantit que les décisions sont prises dans le bon ordre.

### 3. La modélisation des données

Le **Modèle Conceptuel des Données (MCD)** s'appuie sur le formalisme entité-association enrichi par MERISE :
- **Entité** : objet du monde réel avec ses propriétés et un identifiant unique
- **Association** : lien sémantique entre entités, pouvant porter des propriétés
- **Cardinalités** : indication min-max (0-1, 1-1, 0-n, 1-n) précisant les participations

Les règles de normalisation évitent redondances et incohérences : propriétés élémentaires, dépendances fonctionnelles respectées.

Le **Modèle Logique des Données (MLD)** transforme le MCD selon la technologie choisie (typiquement relationnelle) :
- Entités → tables avec clés primaires
- Associations 1-n → clés étrangères
- Associations n-n → tables de jonction

Le **Modèle Physique des Données (MPD)** traduit le MLD en scripts SQL avec considérations de performance (index, dénormalisation éventuelle).

### 4. La modélisation des traitements

Le **Modèle Conceptuel des Traitements (MCT)** décrit la dynamique via :
- **Événements** : faits déclencheurs (externes, internes, temporels)
- **Opérations** : actions atomiques et synchrones produisant des résultats
- **Synchronisation** : conditions logiques (ET/OU) de déclenchement
- **Règles d'émission** : conditions de production des résultats

Le **Modèle Organisationnel des Traitements (MOT)** enrichit le MCT avec :
- Postes de travail (qui)
- Sites géographiques (où)
- Temporalité : temps réel vs différé (quand)
- Procédures : enchaînements de tâches par poste

Le **Modèle Opérationnel des Traitements (MOpT)** définit architecture applicative, transactions, interfaces et algorithmes.

---

## II. MERISE/2 : évolutions selon Nanci et Espinasse

### 1. Contexte d'évolution

Face aux architectures client-serveur, programmation objet et nouvelles interfaces des années 1990, Nanci et Espinasse identifient des limites de MERISE initiale et proposent des extensions majeures.

### 2. Le modèle de communication

**Diagramme de contexte** : vision d'ensemble situant le domaine d'étude dans son environnement, avec acteurs externes et flux échangés.

**Diagramme de flux** : décomposition en sous-domaines/activités avec flux internes et externes, servant de base à la structuration du projet.

### 3. Extensions du modèle de données

**Généralisation/spécialisation** : concept objet permettant l'héritage (ex: PERSONNE → CLIENT/EMPLOYE), avec règles de couverture et d'exclusion.

**Contraintes d'intégrité étendues** :
- Intra-association : totalité, exclusion
- Inter-associations : inclusion, égalité, partition
- Sur propriétés : domaines, formats, calculs

**Dimension temporelle** : mécanismes d'historisation des propriétés, associations et occurrences pour gérer l'évolution dans le temps.

### 4. Évolution des traitements

- Typologie enrichie des événements (externes/internes/temporels)
- Caractérisation des opérations (interactive/automatique, temps réel/différé)
- **Vérification systématique de cohérence données-traitements** : chaque entité utilisée par au moins un traitement, règles de gestion cohérentes avec leur mise en œuvre

---

## III. Conduite de projets selon Moréjon et Rames

### 1. Cycle de vie et étapes

Le projet se structure en étapes successives :

**Schéma directeur** : stratégie informatique à moyen terme, identification des domaines et priorités

**Étude préalable** : analyse de l'existant, recueil des besoins, scénarios de solutions avec dossier de choix

**Étude détaillée** : spécifications fonctionnelles complètes, production des modèles conceptuels et organisationnels

**Étude technique** : architecture, choix technologiques, modèles physiques, spécifications détaillées

**Réalisation** : développement, tests, documentation

**Mise en œuvre** : déploiement, formation, transition

**Maintenance** : corrections et évolutions post-production

Chaque étape produit des **livrables normalisés** validés par des **points de décision** (jalons) où la direction autorise le passage à l'étape suivante.

### 2. Organisation du projet

**Acteurs principaux** :
- **Maître d'ouvrage** : exprime le besoin, finance, valide le résultat
- **Maître d'œuvre** : conçoit et développe la solution
- **Comité de pilotage** : décisions stratégiques, arbitrages
- **Chefs de projet** (MOA/MOE) : coordination opérationnelle
- **Utilisateurs** : expression des besoins, validations, recette

**Instances de pilotage** :
- Comité de pilotage (mensuel) : suivi global et décisions majeures
- Comité de projet (hebdomadaire) : problèmes courants
- Groupes de travail thématiques

La **communication** est formalisée : interne équipe, vers parties prenantes, plan de crise préparé.

### 3. Planification et suivi

**Estimation des charges** par analogie, méthodes paramétriques ou analytiques, avec marge pour risques (10-30%).

**Planification** via Gantt et PERT pour identifier le chemin critique.

**Suivi d'avancement** par indicateurs de délais, charges et livrables, avec réévaluation du reste à faire.

### 4. Gestion des risques

**Identification** des risques techniques, fonctionnels, organisationnels, contractuels dès le début du projet.

**Évaluation** selon probabilité et impact pour priorisation par matrice des risques.

**Stratégies de traitement** :
- Évitement (modifier le projet)
- Réduction (mesures préventives)
- Transfert (sous-traitance, assurance)
- Acceptation (risques faibles)

**Plan de contingence** si le risque se concrétise.

### 5. Qualité

**Dimensions** : conformité fonctionnelle, fiabilité, performance, utilisabilité, maintenabilité, sécurité.

**Assurance qualité** via plan qualité, revues (spécifications, conception, code), audits de processus, tests multiniveaux (unitaires, intégration, système, recette).

**Gestion de configuration** : outils de versioning, traçabilité des modifications, contrôle des changements.

### 6. Aspects critiques

**Expression des besoins** : multiples sources (documents, entretiens, observation), techniques variées (entretiens individuels/groupe, questionnaires, ateliers), formalisation en exigences fonctionnelles/non-fonctionnelles/contraintes/règles de gestion.

**Reprise de l'existant** : analyse/transformation/nettoyage des données, stratégies de basculement (direct, parallèle, progressif) avec plan de retour arrière.

---

## Conclusion

Les trois ouvrages offrent une vision complète et complémentaire de MERISE. Tardieu, Rochfeld et Colletti posent un cadre conceptuel rigoureux avec la double grille abstraction/données-traitements et les modèles associés. Nanci et Espinasse modernisent l'approche en intégrant communication, contraintes étendues et dimension temporelle. Moréjon et Rames ancrent la méthode dans la réalité organisationnelle des projets avec planification, gestion des risques et assurance qualité.

**Apports durables** :
- Cadre de pensée structuré maîtrisant la complexité
- Modèles formalisés mais accessibles
- Organisation rigoureuse du projet
- Implication permanente des utilisateurs

**Limites reconnues** : lourdeur pour petits projets, difficulté face aux changements fréquents, ancrage dans un contexte relationnel/transactionnel. Ces critiques invitent à adapter MERISE au contexte, éventuellement en la combinant avec approches agiles ou objet.

Au-delà des outils, MERISE transmet une philosophie d'informatique au service des utilisateurs, de conception rigoureuse mais pragmatique, de dialogue permanent maîtrise d'ouvrage/maîtrise d'œuvre. Cette philosophie reste pertinente pour tout analyste informatique, quelle que soit la méthode ultérieurement utilisée.

---

**Glossaire minimal** :
- **MCD/MCT** : Modèles Conceptuels Données/Traitements
- **MLD/MOT** : Modèles Logiques Données / Organisationnels Traitements  
- **MPD/MOpT** : Modèles Physiques Données/Traitements
- **Entité** : objet du monde réel à mémoriser
- **Association** : lien sémantique entre entités
- **Cardinalité** : quantification des participations (min-max)
- **Événement** : déclencheur de traitement
- **Opération** : ensemble d'actions atomiques