# Note de Synthèse
## Méthodologie MERISE : Fondements, Évolutions et Conduite de Projets

---

**Cours :** Méthodologie d'Analyse Informatique 1 (M.A.I 1)
**Ouvrages de référence :**
- *La Méthode MERISE* — Hubert Tardieu, Arnold Rochfeld, René Colletti
- *Ingénierie des Systèmes d'Information : MERISE Deuxième Génération* — Dominique Nanci, Bernard Espinasse
- *Conduite de Projets Informatiques* — José Moréjon, Jean-René Rames

---

## Introduction générale

La conception des systèmes d'information constitue l'un des défis majeurs de l'informatique d'entreprise. Comment passer d'un besoin exprimé parfois confusément par des utilisateurs à un système informatique fonctionnel, performant et évolutif ? C'est précisément à cette question que répond MERISE, une méthode française née à la fin des années 1970 qui a profondément marqué le paysage de l'ingénierie informatique.

Les trois ouvrages étudiés offrent une vision complète de cette méthodologie. Le premier, écrit par les pères fondateurs Tardieu, Rochfeld et Colletti, pose les bases théoriques et conceptuelles de MERISE. Le deuxième, signé Nanci et Espinasse, propose une version modernisée baptisée MERISE/2 qui intègre les évolutions technologiques et méthodologiques. Le troisième, rédigé par Moréjon et Rames, se concentre sur la dimension pratique et organisationnelle de la conduite de projets utilisant cette méthode.

Cette synthèse vise à restituer l'essentiel de ces trois lectures en articulant les concepts fondamentaux, les modèles, les techniques et les bonnes pratiques qui font de MERISE un outil toujours pertinent pour l'analyse et la conception des systèmes d'information.

---

## Première partie : Les fondements de MERISE

### Chapitre 1 : Contexte d'émergence et philosophie générale

#### 1.1 Naissance d'une méthode française

MERISE est née d'un constat partagé par de nombreux professionnels de l'informatique à la fin des années 1970 : les projets informatiques échouaient trop souvent, non pas à cause de problèmes techniques, mais en raison d'une mauvaise compréhension des besoins et d'une communication défaillante entre informaticiens et utilisateurs. Le ministère de l'Industrie français a alors lancé un appel d'offres pour développer une méthode nationale de conception des systèmes d'information. C'est le consortium CTI, regroupant notamment le CETE d'Aix-en-Provence et plusieurs universitaires, qui a remporté ce marché et donné naissance à MERISE.

Le nom lui-même est évocateur. Le merisier est un arbre fruitier qui, comme un système d'information, nécessite du temps pour porter ses fruits mais offre ensuite une production durable. Cette métaphore agricole traduit bien la philosophie de la méthode : investir du temps dans l'analyse et la conception pour récolter ensuite un système robuste et pérenne.

#### 1.2 Les principes fondateurs

Tardieu, Rochfeld et Colletti posent dès le départ plusieurs principes qui structurent l'ensemble de la démarche MERISE.

Le premier principe est celui de la séparation des préoccupations. On ne peut pas tout traiter en même temps. Il faut distinguer ce qui relève des données de ce qui relève des traitements, ce qui est stable de ce qui évolue, ce qui concerne l'organisation de ce qui touche à la technique. Cette séparation n'est pas une fin en soi, mais un moyen de maîtriser la complexité.

Le deuxième principe est celui de l'abstraction progressive. On part du général pour aller vers le particulier, du conceptuel vers le physique. Chaque niveau d'abstraction a sa propre cohérence et ses propres règles de validation. Ce principe permet de s'assurer que les choix fondamentaux sont pris avant de s'enliser dans les détails techniques.

Le troisième principe est celui de la validation permanente. À chaque étape, on s'assure que ce qui a été produit correspond bien aux attentes et qu'il est techniquement réalisable. Cette validation implique les utilisateurs, les informaticiens et parfois la direction générale.

Le quatrième principe est celui de la documentation systématique. Tout ce qui est décidé, modélisé ou spécifié doit être consigné dans des documents normalisés. Cette documentation sert à la fois de mémoire du projet et d'outil de communication entre les différents intervenants.

#### 1.3 Le système d'information comme objet d'étude

Avant de parler de méthode, il convient de définir ce qu'est un système d'information. Pour les auteurs, le système d'information est la partie de l'organisation qui assure la mémorisation, le traitement et la circulation des informations nécessaires au fonctionnement de l'entreprise. Il se situe à l'interface entre le système de pilotage, qui prend les décisions, et le système opérant, qui réalise l'activité productive.

Le système d'information n'est pas réductible au système informatique. Il englobe aussi les procédures manuelles, les documents papier, les échanges verbaux. L'informatisation consiste à automatiser une partie de ce système d'information, mais pas nécessairement sa totalité. Cette distinction est fondamentale car elle rappelle que la technique doit être au service de l'organisation et non l'inverse.

Le système d'information remplit plusieurs fonctions essentielles. Il collecte les informations en provenance de l'environnement externe et du fonctionnement interne de l'organisation. Il mémorise ces informations pour les rendre disponibles ultérieurement. Il traite ces informations pour produire de nouvelles informations à valeur ajoutée. Il diffuse ces informations vers les acteurs qui en ont besoin pour agir ou décider.

### Chapitre 2 : Le double axe de modélisation

#### 2.1 Le cycle d'abstraction

L'une des innovations majeures de MERISE est de proposer une grille de lecture du système d'information selon deux axes complémentaires. Le premier axe est celui de l'abstraction, qui distingue trois niveaux.

Le niveau conceptuel répond à la question "quoi ?". Il décrit ce que fait le système d'information indépendamment de toute considération organisationnelle ou technique. À ce niveau, on s'intéresse à la sémantique pure, au sens des informations et des traitements. Un modèle conceptuel est en quelque sorte une photographie de la réalité métier, indépendante des moyens utilisés pour la mettre en œuvre.

Le niveau logique ou organisationnel répond à la question "qui fait quoi, où et quand ?". Il intègre les contraintes d'organisation sans pour autant descendre dans les détails techniques. On y définit les postes de travail, les acteurs, les sites, la répartition des tâches et des données. Ce niveau fait le pont entre la vision métier et la vision technique.

Le niveau physique répond à la question "comment ?". Il décrit la mise en œuvre concrète du système avec les moyens techniques choisis. On y trouve les structures de bases de données, les programmes, les architectures matérielles et logicielles. Ce niveau est le plus proche de la réalisation effective.

Cette progression en trois niveaux garantit que les décisions sont prises dans le bon ordre. On ne choisit pas un outil avant d'avoir compris le besoin. On ne définit pas l'organisation avant d'avoir clarifié les concepts métier.

#### 2.2 La distinction données-traitements

Le second axe de modélisation distingue deux perspectives complémentaires sur le système d'information.

La perspective "données" s'intéresse à l'aspect statique du système. Elle répond à la question "quelles sont les informations manipulées ?". Elle décrit les objets du monde réel que le système doit connaître, leurs caractéristiques et leurs relations. Les données sont ce qui persiste dans le temps, ce qui constitue la mémoire de l'organisation.

La perspective "traitements" s'intéresse à l'aspect dynamique du système. Elle répond à la question "que fait-on avec ces informations ?". Elle décrit les activités, les processus, les événements qui déclenchent des actions et les résultats qui en découlent. Les traitements sont ce qui fait vivre les données, ce qui leur donne du sens et de la valeur.

Cette distinction n'est pas une séparation hermétique. Données et traitements sont intimement liés : les traitements utilisent et produisent des données, les données n'ont de sens que par les traitements qui les exploitent. Mais en les modélisant séparément, on évite de mélanger les problèmes et on facilite la vérification de la cohérence globale.

#### 2.3 La matrice MERISE

En croisant ces deux axes, on obtient une matrice à six cases qui structure l'ensemble de la démarche de modélisation.

Au niveau conceptuel, on trouve le Modèle Conceptuel des Données (MCD) côté données et le Modèle Conceptuel des Traitements (MCT) côté traitements. Ces deux modèles décrivent le système d'information dans sa dimension métier, indépendamment de toute contrainte.

Au niveau logique ou organisationnel, on trouve le Modèle Logique des Données (MLD) et le Modèle Organisationnel des Traitements (MOT). Ces modèles intègrent les choix d'organisation et préparent le passage à la technique.

Au niveau physique, on trouve le Modèle Physique des Données (MPD) et le Modèle Opérationnel des Traitements (MOpT). Ces modèles décrivent la solution technique effective.

Cette matrice n'est pas un carcan rigide. Selon les projets, certaines cases peuvent être plus ou moins développées. L'essentiel est de respecter la logique de progression du conceptuel vers le physique et de maintenir la cohérence entre données et traitements.

### Chapitre 3 : La modélisation des données

#### 3.1 Le Modèle Conceptuel des Données

Le MCD est sans doute le modèle le plus emblématique de MERISE. Il s'appuie sur le formalisme entité-association, parfois appelé entité-relation, qui a été proposé par Peter Chen en 1976 mais que MERISE a enrichi et normalisé.

Une entité représente un objet du monde réel que le système d'information doit connaître et dont il doit mémoriser des informations. Une entité peut être concrète comme un client, un produit ou une facture, ou plus abstraite comme un contrat ou une compétence. Chaque entité est caractérisée par des propriétés qui décrivent ses aspects pertinents. Parmi ces propriétés, un identifiant permet de distinguer de manière unique chaque occurrence de l'entité.

Une association représente un lien sémantique entre deux ou plusieurs entités. Elle traduit le fait que ces entités sont en relation dans le monde réel. Par exemple, un client passe des commandes, un employé travaille dans un service, un étudiant est inscrit à des cours. Une association peut elle aussi porter des propriétés qui caractérisent la relation elle-même.

Les cardinalités précisent combien d'occurrences d'une entité peuvent être liées à une occurrence d'une autre entité via une association donnée. On distingue les cardinalités minimales, qui indiquent si la participation à l'association est obligatoire ou facultative, et les cardinalités maximales, qui indiquent si une occurrence peut être liée à une seule ou à plusieurs occurrences. Les combinaisons classiques sont 0-1, 1-1, 0-n et 1-n.

La construction d'un MCD obéit à des règles de normalisation qui garantissent la qualité du modèle. Chaque propriété doit être élémentaire, c'est-à-dire non décomposable. Chaque propriété doit dépendre de la totalité de l'identifiant de l'entité ou de l'association qui la porte. Ces règles évitent les redondances et les incohérences qui compliqueraient la gestion ultérieure des données.

#### 3.2 Le Modèle Logique des Données

Le passage du MCD au MLD consiste à transformer le modèle conceptuel en un modèle compatible avec la technologie de base de données retenue. Dans le cas le plus courant des bases de données relationnelles, cette transformation suit des règles précises.

Chaque entité devient une table. L'identifiant de l'entité devient la clé primaire de la table. Les propriétés de l'entité deviennent les colonnes de la table.

Pour les associations, la transformation dépend des cardinalités. Une association de type un-à-plusieurs se traduit par l'ajout d'une clé étrangère dans la table côté "plusieurs". Une association de type plusieurs-à-plusieurs devient une table intermédiaire, appelée table de jonction, qui contient les clés étrangères vers les deux tables associées. Une association de type un-à-un peut se traiter de différentes manières selon les contraintes spécifiques.

Les propriétés portées par les associations migrent vers la table appropriée selon les mêmes règles. Une propriété d'une association un-à-plusieurs migre vers la table côté "plusieurs". Une propriété d'une association plusieurs-à-plusieurs reste dans la table de jonction.

Le MLD peut également intégrer des contraintes d'intégrité comme les valeurs obligatoires, les domaines de valeurs autorisées ou les contraintes de vérification.

#### 3.3 Le Modèle Physique des Données

Le MPD traduit le MLD dans le langage de définition de données du système de gestion de base de données retenu. Pour une base relationnelle, il s'agit typiquement de scripts SQL qui créent les tables, les index, les contraintes et les autres objets de la base.

À ce niveau, on intègre également les considérations de performance. On définit les index qui accéléreront les recherches fréquentes. On peut dénormaliser certaines structures pour optimiser les temps d'accès au détriment de la redondance. On dimensionne les espaces de stockage.

Le MPD est intimement lié à l'environnement technique et doit être adapté chaque fois que cet environnement évolue.

### Chapitre 4 : La modélisation des traitements

#### 4.1 Le Modèle Conceptuel des Traitements

Le MCT décrit la dynamique du système d'information au niveau conceptuel. Il s'appuie sur la notion d'événement et d'opération.

Un événement est un fait qui survient dans l'environnement du système et qui déclenche une réaction de celui-ci. Il peut s'agir d'un événement externe comme la réception d'une commande client, ou d'un événement interne comme l'atteinte d'une date d'échéance. Un événement peut aussi être le résultat d'une opération précédente.

Une opération est un ensemble d'actions déclenchées par un ou plusieurs événements et qui produit un ou plusieurs résultats. Une opération est atomique au sens où elle s'exécute entièrement ou pas du tout. Elle est également synchrone au sens où elle s'exécute sans interruption une fois déclenchée.

La synchronisation définit les conditions de déclenchement d'une opération. Une opération peut nécessiter qu'un seul événement se produise, ou au contraire que plusieurs événements se produisent simultanément ou successivement. Les opérateurs logiques ET et OU permettent d'exprimer ces conditions.

Les résultats d'une opération peuvent être de différentes natures. Il peut s'agir d'événements qui déclencheront d'autres opérations, de documents émis vers l'extérieur, ou de modifications de l'état des données.

Le MCT se représente graphiquement par un diagramme où les événements sont figurés par des ovales, les opérations par des rectangles et les flux par des flèches. Les règles d'émission, qui conditionnent la production des résultats, sont indiquées à la sortie des opérations.

#### 4.2 Le Modèle Organisationnel des Traitements

Le MOT enrichit le MCT en y ajoutant les dimensions organisationnelles. Il répond aux questions qui, où et quand.

La dimension "qui" définit les postes de travail responsables de l'exécution des tâches. Un poste de travail peut être humain ou automatisé. Il est caractérisé par ses compétences et ses responsabilités.

La dimension "où" définit les sites ou les lieux où s'exécutent les tâches. Cette dimension est particulièrement importante dans les organisations géographiquement distribuées.

La dimension "quand" définit la temporalité des tâches. On distingue les tâches temps réel, qui doivent s'exécuter immédiatement en réponse à un événement, des tâches différées, qui peuvent être regroupées et exécutées à des moments prédéfinis.

Le MOT introduit également la notion de procédure, qui est un enchaînement de tâches réalisées par un même poste de travail et déclenchées par un même événement. La procédure constitue l'unité d'organisation du travail.

Le formalisme du MOT reprend celui du MCT en le complétant par une représentation en colonnes correspondant aux différents postes de travail et par des indications temporelles.

#### 4.3 Le Modèle Opérationnel des Traitements

Le MOpT, parfois appelé Modèle Physique des Traitements, décrit la mise en œuvre technique des traitements. Il s'intéresse à l'architecture applicative et aux programmes.

À ce niveau, on définit les transactions, c'est-à-dire les unités de travail qui garantissent la cohérence des données. On spécifie les interfaces utilisateur avec leurs écrans et leurs enchaînements. On décrit les algorithmes des traitements complexes.

Le MOpT est étroitement lié aux outils de développement utilisés et constitue la base des spécifications techniques détaillées destinées aux programmeurs.

---

## Deuxième partie : MERISE Deuxième Génération

### Chapitre 5 : Contexte d'évolution et apports de MERISE/2

#### 5.1 Les limites de MERISE première génération

Nanci et Espinasse partent du constat que MERISE, telle que définie initialement, présentait certaines limites face aux évolutions du contexte informatique. La méthode avait été conçue dans un environnement dominé par les systèmes centralisés, les bases de données hiérarchiques ou naissantes relationnelles, et les interfaces en mode caractère.

Les années 1990 ont vu émerger de nouvelles architectures client-serveur, de nouveaux paradigmes de programmation comme l'orienté objet, de nouvelles interfaces graphiques et de nouveaux besoins comme le temps réel ou l'aide à la décision. MERISE devait évoluer pour rester pertinente dans ce nouveau contexte.

Par ailleurs, la méthode originelle souffrait de certaines lacunes. La modélisation des traitements était jugée moins aboutie que celle des données. Le lien entre les différents modèles n'était pas toujours explicite. L'intégration des aspects temporels et des contraintes dynamiques était insuffisante.

#### 5.2 Les extensions proposées

MERISE/2 propose plusieurs extensions majeures qui enrichissent le cadre méthodologique initial.

La première extension concerne le modèle de communication. Ce modèle permet de représenter les échanges d'information entre l'organisation étudiée et son environnement, ainsi qu'entre les différents domaines internes. Il utilise la notion d'acteur, qui représente tout agent externe ou interne avec lequel le système d'information communique, et la notion de flux, qui représente les informations échangées. Le modèle de contexte donne une vision synthétique de ces échanges tandis que le modèle de flux les détaille.

La deuxième extension concerne l'expression des contraintes d'intégrité. MERISE/2 propose un langage formalisé pour exprimer les contraintes qui ne peuvent pas être représentées par le seul formalisme entité-association. Ces contraintes peuvent porter sur les données, comme les contraintes d'exclusion ou de partition, ou sur les traitements, comme les contraintes de précédence ou de simultanéité.

La troisième extension concerne la modélisation du temps. MERISE/2 introduit des concepts permettant de gérer l'historisation des données et la dimension temporelle des traitements. On peut ainsi modéliser le fait qu'une information évolue dans le temps et qu'il est nécessaire de conserver la trace de ses valeurs successives.

La quatrième extension concerne l'intégration de concepts issus de l'approche objet. Sans devenir une méthode objet à part entière, MERISE/2 emprunte à ce paradigme la notion d'héritage et de généralisation/spécialisation dans le modèle de données.

### Chapitre 6 : Le modèle de communication

#### 6.1 Le diagramme de contexte

Le modèle de contexte est le premier modèle à construire dans une démarche MERISE/2. Il donne une vue d'ensemble du système d'information en le situant dans son environnement.

Au centre du diagramme, on représente le domaine d'étude, c'est-à-dire la partie de l'organisation dont on veut informatiser le système d'information. Autour, on représente les acteurs externes qui interagissent avec ce domaine. Ces acteurs peuvent être des personnes comme les clients ou les fournisseurs, des organisations comme les administrations ou les partenaires, ou des systèmes comme d'autres applications informatiques.

Entre le domaine et les acteurs, on représente les flux d'information échangés. Chaque flux porte un nom qui indique la nature de l'information transmise. Le sens de la flèche indique le sens de la transmission.

Ce modèle permet de délimiter clairement le périmètre du projet et d'identifier les interfaces que le futur système devra gérer.

#### 6.2 Le diagramme de flux

Le diagramme de flux affine le modèle de contexte en décomposant le domaine d'étude en sous-domaines ou activités et en détaillant les flux internes.

Chaque activité représente un ensemble cohérent de tâches concourant à un même objectif métier. Les flux entre activités montrent comment l'information circule à l'intérieur du domaine. Les flux avec les acteurs externes reprennent ceux du diagramme de contexte.

Ce modèle permet de comprendre le fonctionnement global du domaine et d'identifier les grandes fonctions que le système d'information devra supporter. Il sert également de base à la décomposition du projet en sous-projets ou en lots.

### Chapitre 7 : Les extensions du modèle de données

#### 7.1 La généralisation et la spécialisation

MERISE/2 introduit dans le modèle entité-association le concept de généralisation/spécialisation emprunté à l'approche objet. Ce concept permet de représenter le fait qu'une entité peut avoir des sous-types qui héritent de ses propriétés tout en ayant des propriétés propres.

Par exemple, une entité PERSONNE peut être spécialisée en CLIENT et EMPLOYE. Les propriétés communes comme le nom et l'adresse sont portées par l'entité générique PERSONNE. Les propriétés spécifiques comme le chiffre d'affaires pour CLIENT ou le salaire pour EMPLOYE sont portées par les entités spécialisées.

Cette modélisation est contrainte par des règles de couverture et d'exclusion. La couverture indique si toute occurrence de l'entité générique appartient nécessairement à au moins un sous-type. L'exclusion indique si une occurrence peut appartenir à plusieurs sous-types simultanément ou non.

#### 7.2 Les contraintes d'intégrité étendues

MERISE/2 propose une typologie enrichie des contraintes d'intégrité pouvant porter sur le modèle de données.

Les contraintes intra-association concernent une seule association. La contrainte de totalité impose qu'au moins une des participations à l'association soit effective. La contrainte d'exclusion impose qu'au plus une des participations soit effective.

Les contraintes inter-associations concernent plusieurs associations et s'expriment par des opérateurs comme l'inclusion, l'égalité, l'exclusion ou la partition.

Les contraintes sur les propriétés définissent les valeurs autorisées au-delà du simple typage. Elles peuvent être des contraintes de domaine, des contraintes de format ou des contraintes calculées.

Toutes ces contraintes sont exprimées dans un langage semi-formel qui peut ensuite être traduit en contraintes techniques dans le modèle physique.

#### 7.3 La dimension temporelle des données

MERISE/2 introduit des mécanismes pour gérer l'historisation des données. On distingue plusieurs cas de figure selon ce que l'on souhaite conserver.

L'historisation des propriétés permet de conserver les valeurs successives d'une propriété dans le temps. Par exemple, on peut vouloir garder la trace de toutes les adresses successives d'un client.

L'historisation des associations permet de conserver la trace des liens qui ont existé entre entités. Par exemple, on peut vouloir garder l'historique des affectations d'un employé aux différents services.

L'historisation des occurrences permet de conserver les entités qui n'existent plus dans la réalité. Par exemple, on peut vouloir garder en base les clients qui ont cessé d'être actifs.

Ces mécanismes d'historisation sont matérialisés dans le modèle par des notations spécifiques et donnent lieu à des structures particulières dans le modèle physique.

### Chapitre 8 : L'évolution de la modélisation des traitements

#### 8.1 Le modèle de flux étendu

MERISE/2 enrichit la modélisation des traitements en s'appuyant sur le modèle de flux présenté précédemment. Chaque activité identifiée dans le diagramme de flux peut être détaillée par un sous-modèle qui décrit son fonctionnement interne.

Cette décomposition hiérarchique permet de gérer la complexité en procédant par raffinements successifs. On commence par une vision globale puis on descend progressivement dans les détails de chaque activité.

#### 8.2 Les événements et opérations enrichis

MERISE/2 propose une typologie plus fine des événements. On distingue les événements externes qui proviennent de l'environnement, les événements internes qui résultent du fonctionnement du système et les événements temporels qui sont liés à des échéances ou à des périodicités.

Les opérations sont également mieux caractérisées. On précise leur nature interactive ou automatique, leur mode de déclenchement temps réel ou différé, et leur impact sur les données en termes de consultation ou de mise à jour.

#### 8.3 La cohérence données-traitements

MERISE/2 insiste sur la nécessité de vérifier la cohérence entre le modèle de données et le modèle de traitements. Cette vérification porte sur plusieurs aspects.

Chaque entité et chaque propriété du modèle de données doit être utilisée par au moins un traitement, que ce soit en création, modification, suppression ou consultation. Inversement, chaque traitement ne peut manipuler que des données définies dans le modèle de données.

Les règles de gestion exprimées comme des contraintes d'intégrité doivent être cohérentes avec les traitements qui les mettent en œuvre. Si une contrainte impose qu'un client ait toujours une adresse, alors les traitements de création de client doivent inclure la saisie obligatoire de l'adresse.

Cette vérification systématique de la cohérence est un gage de qualité du futur système.

---

## Troisième partie : La conduite de projets informatiques

### Chapitre 9 : Le cycle de vie d'un projet MERISE

#### 9.1 Les étapes du projet

Moréjon et Rames présentent le projet informatique comme un processus structuré en étapes successives, chacune ayant ses objectifs, ses livrables et ses critères de validation.

Le schéma directeur constitue l'étape préliminaire qui définit la stratégie informatique de l'organisation à moyen terme. Il identifie les grands domaines à informatiser ou à rénover, les priorités entre ces domaines et les moyens à mettre en œuvre. Cette étape relève de la direction générale et dépasse le cadre d'un projet particulier.

L'étude préalable est la première étape d'un projet spécifique. Elle vise à analyser l'existant, à recueillir les besoins des utilisateurs et à proposer une ou plusieurs solutions d'ensemble. Elle débouche sur un dossier de choix qui permet à la direction de décider du lancement ou non du projet et de sélectionner la solution retenue.

L'étude détaillée approfondit la solution retenue en produisant les spécifications fonctionnelles complètes. Elle décrit précisément ce que doit faire le futur système sans entrer dans les détails techniques. Les modèles conceptuels et organisationnels sont élaborés à ce stade.

L'étude technique traduit les spécifications fonctionnelles en spécifications techniques. Elle définit l'architecture du système, les choix technologiques, les structures de données physiques et les spécifications des programmes. Les modèles physiques sont élaborés à ce stade.

La réalisation consiste à développer, tester et documenter les programmes et les bases de données conformément aux spécifications techniques.

La mise en œuvre déploie le système en environnement de production, forme les utilisateurs et assure la transition depuis l'ancien système.

La maintenance assure la correction des anomalies et l'évolution du système après sa mise en service.

#### 9.2 Les livrables de chaque étape

Chaque étape produit des documents normalisés qui constituent les livrables du projet.

Le schéma directeur produit un plan informatique qui décrit la cible à atteindre, les projets à lancer et le calendrier prévisionnel.

L'étude préalable produit un dossier d'expression des besoins, une analyse critique de l'existant, des scénarios de solutions avec leurs avantages, inconvénients et coûts, et une recommandation.

L'étude détaillée produit les modèles conceptuels des données et des traitements, les modèles organisationnels, le cahier des charges fonctionnel et le plan de développement.

L'étude technique produit les modèles physiques, les spécifications techniques détaillées et le dossier d'architecture.

La réalisation produit les programmes sources, les bases de données, la documentation technique et les jeux de tests.

La mise en œuvre produit les manuels utilisateurs, les supports de formation, le procès-verbal de recette et le dossier d'exploitation.

#### 9.3 Les points de décision

Le cycle de vie est ponctué de points de décision où la direction valide le passage à l'étape suivante. Ces points de décision, parfois appelés jalons ou revues, sont des moments clés du projet.

La revue de fin d'étude préalable est particulièrement importante car c'est à ce moment que l'on décide de l'investissement à consentir. La direction doit valider le périmètre fonctionnel, le budget, le délai et la solution retenue.

La revue de fin d'étude détaillée valide les spécifications fonctionnelles. C'est le moment où les utilisateurs s'engagent sur leurs besoins car les modifications ultérieures seront coûteuses.

La recette fonctionnelle valide que le système développé correspond aux spécifications. Elle conditionne la mise en production.

### Chapitre 10 : L'organisation du projet

#### 10.1 Les acteurs du projet

Un projet informatique mobilise de nombreux acteurs aux rôles distincts.

Le maître d'ouvrage est le client du projet. C'est lui qui exprime le besoin, finance le projet et validera le résultat. Il est généralement représenté par une direction métier de l'organisation. Le maître d'ouvrage est responsable de la définition du périmètre fonctionnel et de la recette finale.

Le maître d'œuvre est le réalisateur du projet. C'est lui qui conçoit et développe la solution. Il peut s'agir de la direction informatique interne ou d'un prestataire externe. Le maître d'œuvre est responsable de la qualité technique et du respect des délais et du budget.

Le comité de pilotage réunit les représentants de la maîtrise d'ouvrage et de la maîtrise d'œuvre au plus haut niveau. Il prend les décisions stratégiques, arbitre les conflits et valide les livrables majeurs.

Le chef de projet maîtrise d'ouvrage coordonne les activités côté client. Il s'assure que les besoins sont bien exprimés, que les utilisateurs sont disponibles pour les validations et que les décisions sont prises en temps voulu.

Le chef de projet maîtrise d'œuvre coordonne les activités de conception et de développement. Il gère l'équipe projet, le planning, les risques et la qualité des livrables.

Les utilisateurs participent à l'expression des besoins, aux validations intermédiaires et à la recette finale. Leur implication est un facteur clé de succès.

#### 10.2 Les instances de pilotage

Moréjon et Rames insistent sur l'importance de mettre en place des instances de pilotage adaptées à la taille et aux enjeux du projet.

Le comité de pilotage se réunit périodiquement, généralement chaque mois, pour suivre l'avancement global et prendre les décisions qui dépassent les prérogatives des chefs de projet. Il est présidé par un représentant de la direction générale.

Le comité de projet réunit plus fréquemment, généralement chaque semaine, les responsables opérationnels des deux côtés. Il traite les problèmes courants et prépare les décisions du comité de pilotage.

Des groupes de travail thématiques peuvent être constitués pour approfondir certains sujets comme l'ergonomie, la reprise des données ou la formation.

#### 10.3 La communication dans le projet

La communication est un facteur essentiel de réussite. Elle doit être organisée et formalisée.

La communication interne à l'équipe projet passe par des réunions régulières, un partage de documents et des outils collaboratifs. Chaque membre doit savoir ce que font les autres et comment son travail s'articule avec le leur.

La communication vers les parties prenantes vise à les tenir informées de l'avancement et à les impliquer aux moments clés. Elle passe par des comptes rendus, des présentations et des démonstrations.

La communication de crise est préparée à l'avance pour faire face aux difficultés majeures. Elle définit qui communique quoi à qui et comment on escalade vers la direction.

### Chapitre 11 : La planification et le suivi

#### 11.1 L'estimation des charges

L'estimation des charges de travail est un exercice difficile mais indispensable. Elle conditionne le budget et le calendrier du projet.

Plusieurs méthodes peuvent être utilisées. L'estimation par analogie consiste à se référer à des projets similaires déjà réalisés. L'estimation paramétrique utilise des ratios comme le nombre de jours par point de fonction ou par table. L'estimation analytique décompose le projet en tâches élémentaires dont on estime individuellement la charge avant de consolider.

Quelle que soit la méthode, l'estimation doit être réaliste et tenir compte des aléas. Il est prudent de prévoir une marge pour risques qui peut représenter 10 à 30 % de la charge estimée selon le niveau d'incertitude.

L'estimation doit être révisée régulièrement au fur et à mesure que l'on avance dans le projet et que l'on dispose d'informations plus précises.

#### 11.2 La planification

La planification consiste à ordonnancer les tâches dans le temps en tenant compte des contraintes de dépendance, de ressources et de délais.

L'outil classique de planification est le diagramme de Gantt qui représente les tâches sous forme de barres horizontales positionnées sur une échelle de temps. Les dépendances entre tâches sont matérialisées par des liens.

La méthode PERT permet d'identifier le chemin critique, c'est-à-dire l'enchaînement de tâches qui détermine la durée minimale du projet. Tout retard sur une tâche du chemin critique retarde d'autant la fin du projet.

La planification doit être suffisamment détaillée pour être utile mais pas trop pour rester gérable. On distingue généralement un planning macro qui donne la vision d'ensemble et des plannings détaillés pour les phases en cours.

#### 11.3 Le suivi d'avancement

Le suivi d'avancement permet de comparer régulièrement la situation réelle à la situation prévue et de prendre des mesures correctives si nécessaire.

Les indicateurs de suivi portent sur les délais (sommes-nous en avance ou en retard ?), les charges (avons-nous consommé plus ou moins que prévu ?) et les livrables (avons-nous produit ce qui était attendu ?).

Le reste à faire est une notion importante. Il ne suffit pas de savoir ce qui a été fait, il faut aussi réévaluer ce qui reste à faire. Un projet peut avoir consommé 80 % de son budget et n'être qu'à 50 % d'avancement réel.

Les réunions d'avancement permettent à chaque membre de l'équipe de rendre compte de son travail, de signaler les difficultés et de mettre à jour le planning.

### Chapitre 12 : La gestion des risques

#### 12.1 L'identification des risques

Un risque est un événement potentiel qui, s'il se produit, aura un impact négatif sur le projet. La gestion des risques consiste à anticiper ces événements pour les éviter ou en limiter les conséquences.

Les risques peuvent être de différentes natures. Les risques techniques concernent les choix technologiques, la complexité de la solution ou les performances. Les risques fonctionnels concernent l'adéquation aux besoins, la complétude des spécifications ou l'acceptation par les utilisateurs. Les risques organisationnels concernent la disponibilité des ressources, les conflits entre acteurs ou les changements de priorités. Les risques contractuels concernent les relations avec les prestataires.

L'identification des risques doit être réalisée dès le début du projet et mise à jour régulièrement. Elle s'appuie sur l'expérience des projets passés, l'analyse du contexte spécifique et des séances de brainstorming.

#### 12.2 L'évaluation et la priorisation

Chaque risque identifié doit être évalué selon deux dimensions. La probabilité d'occurrence mesure la vraisemblance que l'événement se produise. L'impact mesure la gravité des conséquences s'il se produit.

En croisant ces deux dimensions, on obtient un niveau de criticité qui permet de prioriser les risques. Les risques à forte probabilité et fort impact sont les plus critiques et doivent être traités en priorité.

Une matrice des risques permet de visualiser cette priorisation et de concentrer les efforts sur les risques qui méritent attention.

#### 12.3 Le traitement des risques

Plusieurs stratégies de traitement sont possibles selon la nature du risque.

L'évitement consiste à modifier le projet pour supprimer le risque. Par exemple, on peut renoncer à une fonctionnalité risquée ou choisir une technologie plus éprouvée.

La réduction consiste à prendre des mesures pour diminuer la probabilité ou l'impact. Par exemple, on peut former l'équipe sur une technologie mal maîtrisée ou prévoir des tests renforcés sur les parties critiques.

Le transfert consiste à faire porter le risque par un tiers. Par exemple, on peut sous-traiter un développement risqué à un spécialiste ou souscrire une assurance.

L'acceptation consiste à ne rien faire tout en étant conscient du risque. Cette stratégie est adaptée aux risques de faible criticité ou dont le coût de traitement serait disproportionné.

Un plan de contingence prépare les actions à mettre en œuvre si le risque se concrétise malgré tout.

### Chapitre 13 : La qualité dans les projets

#### 13.1 Les dimensions de la qualité

La qualité d'un système d'information peut être appréciée selon plusieurs dimensions.

La conformité fonctionnelle mesure l'adéquation du système aux besoins exprimés. Le système fait-il bien ce qui était demandé ?

La fiabilité mesure la capacité du système à fonctionner sans défaillance. Le système tombe-t-il souvent en panne ? Les résultats sont-ils corrects ?

La performance mesure les temps de réponse et les capacités de traitement. Le système répond-il assez vite ? Supporte-t-il la charge attendue ?

L'utilisabilité mesure la facilité d'utilisation. Les utilisateurs arrivent-ils à se servir du système sans difficulté ?

La maintenabilité mesure la facilité à corriger et faire évoluer le système. Les modifications sont-elles faciles à réaliser ? Le code est-il compréhensible ?

La sécurité mesure la protection contre les accès non autorisés et les pertes de données.

#### 13.2 L'assurance qualité

L'assurance qualité vise à garantir que le projet respecte les standards et les bonnes pratiques définis. Elle s'appuie sur un plan qualité qui décrit les objectifs de qualité, les moyens de les atteindre et les indicateurs de suivi.

Les revues sont des examens formels des livrables par des pairs ou des experts. Elles permettent de détecter les erreurs et les non-conformités avant qu'elles ne se propagent. On distingue les revues de spécifications, les revues de conception et les revues de code.

Les audits sont des examens du respect des processus définis. Ils vérifient que les méthodes et les procédures sont bien appliquées.

Les tests sont des vérifications du bon fonctionnement du système. Ils sont organisés en plusieurs niveaux : tests unitaires pour les composants isolés, tests d'intégration pour les assemblages, tests système pour l'ensemble, tests de recette pour la validation finale.

#### 13.3 La gestion de configuration

La gestion de configuration vise à maîtriser l'évolution des livrables du projet. Elle s'appuie sur des outils de gestion de versions qui permettent de tracer toutes les modifications, de revenir à des versions antérieures et de gérer les branches parallèles de développement.

Chaque livrable significatif est identifié de manière unique et son évolution est suivie. Les changements sont formalisés par des demandes de modification qui sont évaluées et approuvées avant d'être réalisées.

Cette rigueur peut sembler contraignante mais elle évite le chaos qui s'installe rapidement quand on perd le contrôle des versions.

---

## Quatrième partie : Approfondissements et aspects transversaux

### Chapitre 14 : L'expression des besoins

#### 14.1 Les sources d'information

L'expression des besoins est une étape cruciale qui conditionne tout le reste du projet. Si les besoins sont mal compris ou incomplets, le système développé ne satisfera pas les utilisateurs.

Les sources d'information sont multiples. Les documents existants comme les procédures, les formulaires, les états de sortie donnent une image de l'existant. Les entretiens avec les utilisateurs et les responsables métier permettent de recueillir leurs attentes et leurs priorités. L'observation du travail réel montre ce qui se passe effectivement, parfois différemment de ce qui est décrit. Les systèmes analogues déjà en place dans d'autres organisations fournissent des idées de solutions.

#### 14.2 Les techniques de recueil

Plusieurs techniques peuvent être utilisées pour recueillir les besoins.

L'entretien individuel permet un échange approfondi avec un interlocuteur. Il convient bien pour les sujets sensibles ou les personnes clés. Il doit être préparé avec soin pour être productif.

L'entretien de groupe rassemble plusieurs personnes qui échangent sur un thème commun. Il permet de confronter les points de vue et de faire émerger des consensus ou des divergences.

Le questionnaire permet de recueillir des informations auprès d'un grand nombre de personnes. Il convient pour des questions fermées mais moins pour des sujets ouverts.

L'atelier de travail réunit utilisateurs et informaticiens pour produire ensemble des éléments de spécification. Il favorise l'implication et la créativité.

#### 14.3 La formalisation des besoins

Les besoins recueillis doivent être formalisés dans un document structuré qui servira de référence tout au long du projet.

Les exigences fonctionnelles décrivent ce que le système doit faire. Elles sont exprimées du point de vue de l'utilisateur et non de l'informaticien. Chaque exigence est identifiée de manière unique pour permettre la traçabilité.

Les exigences non fonctionnelles décrivent les qualités attendues du système comme les performances, la disponibilité, la sécurité ou l'ergonomie.

Les contraintes décrivent les éléments imposés comme les technologies à utiliser, les interfaces à respecter ou les réglementations à appliquer.

Les règles de gestion décrivent les politiques métier que le système devra mettre en œuvre.

### Chapitre 15 : La conception des interfaces

#### 15.1 L'ergonomie des interfaces

L'ergonomie des interfaces conditionne l'acceptation du système par les utilisateurs. Une interface mal conçue génère des erreurs, des frustrations et une perte de productivité.

Les principes d'ergonomie sont nombreux. La cohérence veut que les mêmes actions se fassent toujours de la même manière. La visibilité veut que l'état du système soit toujours perceptible. Le feedback veut que chaque action de l'utilisateur reçoive une réponse. La prévention des erreurs veut que le système empêche les actions incorrectes plutôt que de les signaler après coup. La réversibilité veut que l'utilisateur puisse annuler ses actions.

#### 15.2 La maquette et le prototype

La maquette est une représentation visuelle des écrans avant leur développement. Elle permet de valider l'ergonomie et la navigation avec les utilisateurs sans avoir à programmer. La maquette peut être réalisée sur papier ou avec des outils de maquettage.

Le prototype est une version simplifiée mais fonctionnelle du système. Il permet de valider non seulement l'ergonomie mais aussi certains aspects techniques. Le prototypage peut être itératif, le prototype s'enrichissant progressivement jusqu'à devenir le système final.

Ces techniques de validation précoce réduisent les risques de rejet du système et les coûts de modification tardive.

### Chapitre 16 : La reprise de l'existant

#### 16.1 La reprise des données

Rares sont les projets qui partent d'une feuille blanche. Le plus souvent, il existe des données dans des systèmes antérieurs qu'il faut récupérer et intégrer dans le nouveau système.

L'analyse des données existantes est un préalable. Il faut identifier quelles données reprendre, évaluer leur qualité, comprendre leur signification et leur format.

La transformation des données consiste à convertir les données de l'ancien format vers le nouveau. Cette transformation peut être simple si les structures sont proches ou complexe si elles diffèrent significativement.

Le nettoyage des données vise à corriger les erreurs, à compléter les manques et à harmoniser les valeurs. C'est souvent l'occasion de faire un grand ménage dans des données qui se sont dégradées au fil du temps.

La migration effective doit être planifiée soigneusement. On définit une fenêtre de migration pendant laquelle l'ancien système est arrêté, les données sont transférées et le nouveau système est démarré.

#### 16.2 Le basculement

Le basculement est le moment critique où l'on passe de l'ancien système au nouveau. Plusieurs stratégies sont possibles.

Le basculement direct consiste à arrêter l'ancien système et à démarrer le nouveau à une date donnée. C'est la stratégie la plus simple mais aussi la plus risquée.

Le fonctionnement en parallèle consiste à faire tourner les deux systèmes simultanément pendant une période transitoire. Cela permet de vérifier que le nouveau système produit les mêmes résultats que l'ancien. C'est plus sécurisant mais plus coûteux.

Le basculement progressif consiste à migrer par étapes, par exemple site par site ou fonction par fonction. Cela limite les risques mais allonge la période de transition.

Quelle que soit la stratégie, un plan de retour arrière doit être prévu au cas où le basculement se passerait mal.

---

## Cinquième partie : Synthèse et perspectives

### Chapitre 17 : Les apports fondamentaux de MERISE

Les trois ouvrages étudiés permettent de dégager les apports fondamentaux de la méthode MERISE.

Le premier apport est de proposer un cadre de pensée structuré pour aborder la conception des systèmes d'information. La séparation en niveaux d'abstraction et la distinction données-traitements offrent une grille de lecture qui évite de tout mélanger et permet une progression ordonnée du général au particulier.

Le deuxième apport est de fournir un ensemble de modèles formalisés qui permettent de représenter le système d'information sous différents angles. Ces modèles sont suffisamment précis pour être non ambigus mais suffisamment accessibles pour être partagés avec les utilisateurs non informaticiens.

Le troisième apport est d'organiser le projet en étapes balisées par des livrables et des validations. Cette organisation apporte de la rigueur et de la prévisibilité dans une activité qui peut facilement déraper.

Le quatrième apport est d'impliquer les utilisateurs tout au long du projet et non seulement au début et à la fin. Cette implication est un facteur majeur de succès car elle garantit l'adéquation aux besoins réels.

### Chapitre 18 : Les évolutions et adaptations

MERISE a su évoluer pour rester pertinente face aux changements technologiques et méthodologiques.

L'intégration de concepts de l'approche objet dans MERISE/2 témoigne de cette capacité d'adaptation. Sans devenir une méthode objet, MERISE a su emprunter ce qui pouvait enrichir ses modèles.

L'ouverture vers les architectures distribuées et les nouvelles interfaces a également été intégrée, même si certains aspects mériteraient d'être approfondis.

La combinaison avec des approches agiles est possible, certains praticiens utilisant les modèles MERISE dans un cadre itératif avec des cycles courts et une adaptation permanente.

### Chapitre 19 : Les limites et les critiques

Il serait incomplet de ne pas mentionner les limites et les critiques adressées à MERISE.

On lui a reproché une certaine lourdeur, notamment pour les petits projets où la production de nombreux modèles peut sembler disproportionnée. Cette critique est partiellement justifiée et invite à adapter le formalisme au contexte.

On lui a reproché un manque d'agilité face aux changements de besoins en cours de projet. Le cycle en cascade traditionnel supporte mal les évolutions tardives. Là encore, des adaptations sont possibles.

On lui a reproché une certaine obsolescence face aux nouvelles technologies comme le web, le mobile ou le cloud. MERISE reste ancrée dans un monde de bases de données relationnelles et d'applications transactionnelles. Elle s'applique moins directement aux nouveaux paradigmes.

Ces critiques n'invalident pas la méthode mais invitent à l'utiliser avec discernement, en l'adaptant au contexte et en la combinant si nécessaire avec d'autres approches.

---

## Conclusion générale

Cette synthèse des trois ouvrages de référence sur MERISE permet de mesurer la richesse et la cohérence de cette méthode française qui a marqué l'histoire de l'ingénierie des systèmes d'information.

Du cadre conceptuel fondateur posé par Tardieu, Rochfeld et Colletti aux extensions modernisées de MERISE/2 proposées par Nanci et Espinasse, en passant par les techniques concrètes de conduite de projet détaillées par Moréjon et Rames, nous disposons d'un corpus complet pour aborder la conception et la réalisation de systèmes d'information.

Les concepts fondamentaux comme la séparation des niveaux d'abstraction, la distinction données-traitements, la modélisation entité-association et la structuration du projet en étapes restent des acquis durables qui transcendent les évolutions technologiques.

Les extensions proposées par MERISE/2 comme le modèle de communication, les contraintes d'intégrité étendues et la gestion du temps enrichissent le cadre initial et répondent à des besoins réels.

Les techniques de conduite de projet comme l'estimation des charges, la planification, la gestion des risques et l'assurance qualité sont indispensables pour mener à bien tout projet informatique, quelle que soit la méthode de conception utilisée.

Au-delà des outils et des techniques, c'est une philosophie qui se dégage de ces lectures : celle d'une informatique au service des utilisateurs, d'une conception rigoureuse mais pragmatique, d'un dialogue permanent entre maîtrise d'ouvrage et maîtrise d'œuvre. Cette philosophie reste d'une actualité brûlante à l'heure où les échecs de projets informatiques continuent de faire les gros titres.

L'étudiant en méthodologie d'analyse informatique trouvera dans MERISE non seulement un ensemble de modèles à maîtriser mais aussi une manière de penser qui lui servira tout au long de sa carrière, y compris s'il utilise par la suite d'autres méthodes comme UML ou les approches agiles.

---

## Annexe : Glossaire des termes clés

**Association** : Lien sémantique entre deux ou plusieurs entités dans le modèle conceptuel des données.

**Cardinalité** : Indication du nombre minimum et maximum d'occurrences d'une entité pouvant participer à une association.

**Entité** : Objet du monde réel dont le système d'information doit connaître et mémoriser des informations.

**Événement** : Fait survenant dans l'environnement du système et déclenchant une réaction.

**Maître d'ouvrage** : Client du projet, responsable de l'expression des besoins et de la validation du résultat.

**Maître d'œuvre** : Réalisateur du projet, responsable de la conception et du développement.

**MCD** : Modèle Conceptuel des Données, représentation des données au niveau conceptuel.

**MCT** : Modèle Conceptuel des Traitements, représentation des traitements au niveau conceptuel.

**MLD** : Modèle Logique des Données, représentation des données au niveau logique.

**MOT** : Modèle Organisationnel des Traitements, représentation des traitements au niveau organisationnel.

**MPD** : Modèle Physique des Données, représentation des données au niveau physique.

**Opération** : Ensemble d'actions déclenchées par des événements et produisant des résultats.

**Propriété** : Caractéristique élémentaire d'une entité ou d'une association.

**Règle de gestion** : Politique métier que le système d'information doit mettre en œuvre.

**Synchronisation** : Condition logique de déclenchement d'une opération en fonction des événements.

---

*Fin de la note de synthèse*