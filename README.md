# Simplon-Engine
Simplon Engine est une application web de gestion des sessions d’examen qui centralise les référentiels, déroulés, candidats, aménagements, plannings, convocations et utilisateurs dans un environnement rapide, structuré et sécurisé.


readme = """# Simplon Engine

Simplon Engine est une application web de gestion des sessions d’examen conçue pour centraliser les référentiels, déroulés, étapes, sessions, candidats, aménagements, plannings, convocations et utilisateurs dans un environnement rapide, structuré et sécurisé.

## Objectif

L’outil permet de remplacer une gestion dispersée et lente par une application unique, plus fiable et plus simple à maintenir.

## Fonctionnalités principales

- Authentification utilisateur
- Gestion des référentiels
- Gestion des déroulés et des étapes
- Gestion des sessions d’examen
- Gestion des candidats
- Gestion des aménagements individuels
- Génération automatique des passages
- Affichage du planning de session
- Génération du déroulé d’examen
- Préparation des convocations
- Gestion des localisations
- Gestion des utilisateurs et des rôles

## Stack technique

### Front-end
- HTML
- CSS
- JavaScript
- Google Apps Script HTML Service

### Back-end
- Google Apps Script

### Base de données
- Firebase / Cloud Firestore

### Authentification
- Firebase Authentication

## Architecture générale

Simplon Engine repose sur une séparation simple :

- `index.html` : page de connexion
- `app.html` : application principale
- `style.html` : styles partagés
- fichiers `.gs` : logique serveur, CRUD, services Firestore, authentification et traitements métier

## Collections Firestore principales

- `referentiels`
- `deroules`
- `derouleEtapes`
- `sessions`
- `sessionCandidats`
- `candidatAmenagements`
- `localisations`
- `users`

## Identifiants métier

Les entités utilisent des identifiants lisibles pour faciliter la maintenance :

- `REF_001`
- `DER_001`
- `DET_001`
- `SES_001`
- `CAN_001`
- `AMG_001`
- `LOC_001`
- `USR_001`

## Principes de fonctionnement

1. L’utilisateur se connecte à l’application
2. Les données de référence sont chargées
3. Les sessions sont créées à partir d’un déroulé
4. Les candidats sont rattachés à une session
5. Les aménagements sont appliqués si nécessaire
6. Les passages sont générés automatiquement
7. Le planning et le déroulé d’examen sont exploités pour l’organisation
8. Les convocations sont préparées à partir des données générées

## Points forts

- Structure de données claire
- Meilleures performances que Google Sheets
- Interface orientée usage métier
- Base de données moderne et extensible
- Possibilité d’évolution vers une gestion avancée des droits et des documents

## Installation / déploiement

### Prérequis
- Un projet Google Apps Script
- Un projet Firebase
- Firestore activé
- Firebase Authentication activé
- Une web app Apps Script déployée

### Paramétrage
- Configurer les propriétés de script nécessaires
- Configurer Firebase dans les pages HTML
- Créer les collections Firestore nécessaires
- Déployer l’application via Apps Script

## Sécurité

- Authentification utilisateur obligatoire
- Séparation entre identité technique et profil métier
- Préparation à la gestion des rôles et permissions

## Roadmap

- Stabilisation des modules CRUD
- Finalisation du moteur de génération des passages
- Amélioration des convocations
- Renforcement de la gestion des droits
- Export documentaire avancé
- Journalisation et suivi d’activité

## Auteur / projet

Projet : **Simplon Engine**  
Usage : gestion des sessions d’examen  
Architecture : **Google Apps Script + Firebase**
"""
path = "/mnt/data/README_Simplon_Engine.md"
with open(path, "w", encoding="utf-8") as f:
    f.write(readme)
print(path)
