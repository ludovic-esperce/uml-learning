# Initiation à la conception de diagrammes de cas d'utilisation

## Introduction

Ce dépôt contient un ensemble d'exercices d'entraînement à la ccréation de diagrammes de cas d'utilisation.

Chaque exercice peut être considéré comme un cahier des charges minimaliste à analyser.

Pour chaque cahier des charges il vous faudra :
- établir une liste des **acteurs du système**
- trouver les **cas d'utilisation**
- trouver les **relations** entre les acteurs et les cas d'utilisation

---

## Système de vente en ligne

Le magasin "HighRise" vend du matériel de haute montagne et a besoin d’un système de gestion de vente en ligne.

![Logo Highrise](img/logo-highrise.svg)

Les besoins fonctionnels exprimés par le client sont les suivants :
-	Le client doit être capable de consulter le catalogue, remplir un panier et valider une commande.
-	Le client doit pouvoir payer en ligne par carte bancaire ou via un système tel que PayPal.
-	Pour une commande non payée en ligne, un commercial doit prendre contact avec le client pour établir les procédures de paiement. Une fois le paiement reçu, le commercial valide la commande.
-	Pour une commande payée et non livrée, le magasinier prépare la commande du client et enregistre les informations concernant la livraison sur le système.
-	Le magasinier peut aussi créer un nouveau produit s'il n’existe pas dans le catalogue.
-	Le comptable doit être capable de visualiser les ventes et le chiffre d’affaires réalisé.
-	Le directeur peut consulter des rapports de vente pour les analyser.

---

## Sécurité sociale

Un organisme de sécurité sociale souhaite développer une application gérant des patients, leur médecin traitant et des médecins spécialistes.

Une personne est soit un assuré, soit un médecin, un médecin peut être malade et donc assuré.

Un médecin est soit généraliste, soit spécialiste, un généraliste ne pouvant pas être spécialiste et inversement. Un patient a choisi ou non son médecin traitant.

Un patient consulte, à une date donnée, un généraliste. Lors des consultations, le généraliste peut ou
non prescrire une ou plusieurs consultations chez un spécialiste.

Cette application peut être utilisée par l'organisme de sécurité sociale pour inscrire un assuré, enregistrer un médecin traitant pour un assuré, enregistrer des feuilles de maladie et effectuer des remboursements.

Tout médecin peut également, via l'application, enregistrer une feuille de maladie, prescrire des médicaments et prescrire une consultation chez un spécialiste.

---

## Application de réservation/plannification de voyage

L'agence de voyage "Fast Journey" désire mettre en place un système de plannification de voyage à la carte pour ses clients.

L'agence est en partenariat avec un ensemble de guides dans différents pays et villes. Chaque guide a sa spécialité et une zone géographique qui lui est propre.

Un client peut choisir une destination (ville ou pays) et l'application l'aiguillera dans la plannification de son voyage.

Une plannification de voyage sera composée de différents **éléments** détaillé dans la partie suivante.

### Elément de voyage et plannification à la carte

Un élément de voyage représente une **activité ou réservation associée à une date, un horaire, un tarif et une adresse.**.

Un voyageur peut ajouter un élément dans sa plannification, par exemple :
- choix d'une visite guidée
- choix de réservation dans un hôtel/AirBnb
- choix de réservation dans un restaurant

Pour chacun des éléments c'est au voyagiste de gérer la réservation.

Par exemple, un voyageur ajoute à sa plannification une nuit dans un hôtel. La réservation ne se fait pas automatiquement, le voyagiste est notifié et ensuite il effectue la réservation.

Les éléments de voyage sont ajoutés par le voyagiste.

### Relation client

L'agence désire garder le contact avec sa clientèle et des voyagistes devront pouvoir aider les voyageur 

Parmis les fonctionnalités d'un voyagiste on retrouve :
- l'inscription sur l'application d'un nouveau voyageur (ou groupe de voyageur)
- ajout d'un élément de voyage (par exemple un nouveau musée)
- construction d'une plannification de voyage pré-établi pouvant être proposé à tout voyageur
- modification d'une plannification de voyage pour un client spécifique
- proposition d'une élément de parcours de voyage pour un client spécifique

### Parcours de voyage pré-établi

Les voyagistes pourront mettre en place des programmes de voyages pré-établis qui seront proposés à leurs clients (aussi appelé "Modèle de voyage").

Par exemple un programme nommé "Mont-de-Marsan en 2 jours" avec un ensemble d'activités tells que :
```text
- J1 : 
  - Visite des arènes à 10h
  - Déjeuner au restaurant 
  - Visite du musée Despiau-Wlérik
  - Dégustation de Tourtière Landaise à 16h
  - Dîner/nuit à l'hôtel
- J2 :
  - promenade le long de la Midouze 10h
  - ... 
```

Un voyageur peut déccider de baser sa plannification sur un parcours pré-établi et le modifier.

### Proposition d'activité par un guide

Un voyagiste peut ajouter des guides dans le système.

Une fois qu'un guide est inscrit il pourra ajouter des activités (par exemple une visite d'un endroit).

L'ativité que propose un guide est un élément de voyage et donc caractérisé par ec qui indiqué plus haut :
- une date ;
- un horaire ;
- un tarif ;
- une adresse.
