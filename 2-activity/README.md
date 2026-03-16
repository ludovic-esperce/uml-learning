# Initiation à la conception de diagrammes d'activité

## Introduction

Ce dépôt contient un ensemble d'exercices d'entraînement à la création de diagrammes d'activités.

Pour chaque cahier des charges il vous faudra :
- mettre en place un diagramme détaillant au mieux ce qui est décrit par l'énoncé

---

## Vente de billets de train

Construire un diagramme d'activité décrivant le processus permettant à un utilisateur d'acheter un ou plusieurs billet(s) de train en utilisant un distributeur automatique disponible en gare.

L'activité est débutée lorsque l'utilisateur interagit avec la machine.
Le système demande alors les informations de voyage.

Parmi ces informations on retrouve le nombre de tickets demandés, la destination, s'il s'agit d'un aller simple ou un aller-retour.

Avec les informations communiquées par l'utilisateur, la machine va calculer la somme due et demander à l'utilisateur de procéder au paiement.

L'utilisateur peut alors payer en espèce ou par carte.

S'il s'agit d'un paiement par carte une vérification bancaire est effectuée (via un système extérieur).

---

## Demande de crédit

Construire un diagramme d'activités qui décrit le processus de traitement des demandes de crédit « en ligne » dans un organisme financier.

Ci-dessous une description textuelle : 
Un internaute fait une demande de crédit en ligne, en renseignant son nom, prénom, coordonnées postales, téléphone, adresse email, revenus mensuels, montant et durée du crédit demandé.
Ces demandes sont étudiées sous 24 heures par le service clientèle de l'organisme.

A la suite de cette étude, le service clientèle indique sa décision quant à la demande : accord de principe, refus, étude complémentaire nécessaire. 

Si une étude complémentaire est nécessaire, la demande est transmise au service de gestion des risques, qui, après étude du dossier, renvoie au service clientèle un accord de principe ou un refus. L'étude du dossier peut nécessiter des compléments d'informations de la part du client. Celui-ci est alors contacté par mail et répond au mail pour fournir les compléments d'informations demandés. 

Tout refus fait l'objet d'une notification au client. 

En cas d'accord de principe, le client est averti et reçoit les conditions commerciales relatives au crédit demandé.

Il dispose alors de 7 jours pour accepter l'offre proposée. Pour accepter une offre, le client renvoie l'offre, signée, ainsi que les éléments justifiant les informations fournies lors de la demande (bulletins de salaire, justificatif de domicile, …). 

Après avoir vérifié que le dossier était complet, l'offre est transmise au service financier par le service clientèle.

---

## Gestion des prêts d'une médiathèque

> [!IMPORTANT]
> Le diagramme d'activité à construire doit uniquement correspondre au **prêt d'un document**.
>
> Le descriptif du système couvre volontairement des éléments qui ne sont pas en lien avec le prêt.
> A vous de mener une analyse fine du texte.

### Descriptif du système

L'objectif du programme est la gestion des achats et des prêts de documents (papier, vidéo, son, …) aux usagers d'une médiathèque municipale.

Il existe plusieurs types de documents :
- les livres, et parmi eux des livres spéciaux qui seront consultables uniquement sur place
- les journaux qui seront consultables uniquement sur place
- les Blurays qui pourront être prêtés avec une caution

Chaque document est repéré par sa côte. Un livre ou un Bluray pourra être trouvé également par son titre et son (ses) auteur(s), un journal par son titre et sa date.

Concrètement, l'usager peut consulter sur un poste informatique la liste des documents, une consultation par ordre alphabétique selon le type de document, par auteur (tous types de documents confondus), par la côte du document ou par sa référence (titre, …).

Ensuite, l'usager doit aller chercher le document, soit directement dans le rayonnage où il est rangé pour les livres et les journaux, soit à un guichet pour les Blurays.

Le Bluray ne lui sera remis qu'en échange d'une caution, après qu'il ait présenté sa carte de lecteur.
Cette caution lui sera rendue au retour du Bluray. La bibliothèque dispose de lecteurs permettant une consultation sur place des Blurays.

S'il désire emprunter chez lui un Bluray ou un livre, il doit en sortant se présenter à un employé de la bibliothèque et lui fournir sa carte de lecteur et le document; l'employé référence alors l'emprunt par le numéro du lecteur et par la côte du document. 

Toute **mise en circulation** de Bluray génère une fiche de prêt dans le système informatique. De même lors d'emprunts à domicile d'un livre.

Les achats des documents, ainsi que les inscriptions de nouveaux usagers seront réalisés uniquement par le personnel de la bibliothèque.

Les prêts de documents aux usagers pourront être effectués par le personnel, mais également par une équipe de bénévoles qui n'auront ce droit accordé que pour une période limitée.

Les usagers quant à eux auront possibilité de consulter la liste des documents et de savoir si ceux-ci sont disponibles (ni prêtés, ni perdus).

L'enregistrement d'un nouveau document génère un numéro (sa côte) unique; ce numéro est calculé automatiquement en fonction du titre du document, de son/ses auteurs(s) et de sa catégorie.

Les usagers de la médiathèque ont également un identifiant unique, incrémenté automatiquement.

Un employé de la médiathèque peut modifier les caractéristiques des fiches lecteurs (adresse, numéro de téléphone...) et de mettre hors service un document qui a été perdu ou volé.

Un prêt ne sera accordé qu'à la condition que le lecteur ait réglé sa cotisation et n'ait pas plus de 5 emprunts simultanés.

Le prêt est daté et après 4 semaines, un email de relance automatique sera envoyé au lecteur.

Les employés de la bibliothèque peuvent consulter les états des lecteurs (nombre d'emprunts, lesquels …) et les lecteurs peuvent consulter l'état de leurs prêts.

### Règles de gestion diverses

1.	tout emprunteur doit posséder une carte de lecteur
2.	tout emprunt de Bluray nécessite une caution
3.	tout document emprunté est enregistré (n° lecteur + côte document)
4.	les enregistrements des emprunts peuvent être effectués soit par le personnel, soit par des bénévoles
5.	les enregistrements des nouveaux documents ou des nouveaux lecteurs sont effectués uniquement par le personnel
6.	les bénévoles n'ont accès à l'enregistrement des emprunts que sur une période déterminée
7.	la côte d'un document et le n° d'un lecteur sont des numéros incrémentés à leur création
8.	un lecteur ne peut emprunter que s'il a payé sa cotisation et n'a pas plus de 5 emprunts en cours
9.	au delà de 4 semaines d'emprunt, un email de relance sera envoyé au lecteur
10.	les documents perdus ou volés doivent être mis hors service
11.	les enregistrements lecteur et document ne sont pas supprimables
12.	les lecteurs peuvent consulter selon plusieurs critères les documents et leurs disponibilités
13.	le personnel peut consulter la situation de chaque lecteur
