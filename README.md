# RoadWatch Tana : Plateforme de signalement et suivi des travaux routiers à Antananarivo 

*Confidential - Not for Public Consumption or Distribution*

---

## Objectifs

- Mettre en place un fournisseur d’identité sur une des plateformes suivantes (Docker) :
  - PHP MVC (pas de FlightPHP)
  - Java
  - .NET
  - Node.js
- **API uniquement** (pas d’interface graphique)

*Confidential - Not for Public Consumption or Distribution*

---

## Module Authentification

Utilisation de **Firebase** si connexion Internet, sinon base locale dans Docker.

### Fonctionnalités minimales :
- Authentification
- Inscription
- Modification des informations utilisateur
- Durée de vie des sessions configurable
- Limite du nombre de tentatives de connexion (paramétrable, par défaut 3)
- API REST permettant de réinitialiser le blocage pour un utilisateur donné
- Documentation API via **Swagger**

*Confidential - Not for Public Consumption or Distribution*

---

## Module Cartes


- Installer un serveur de carte **Offline** dans Docker
- Télécharger la ville d’**Antananarivo** avec ses tuiles
- Utiliser **Leaflet** pour afficher et manipuler la carte dans l’application web

*Confidential - Not for Public Consumption or Distribution*

---

## Module Web

Application permettant de signaler et suivre les travaux routiers à Antananarivo.

- Utilisation de l’**API Rest d’authentification** pour se connecter et créer un compte
- 3 profils utilisateurs :
  1. **Visiteur** (sans compte)
  2. **Utilisateur** (avec compte créé)
  3. **Manager** (compte créé par défaut)

### Fonctionnalités Visiteur :
- Voir la carte avec les points représentant les problèmes routiers
- Survol d’un point → affichage des informations (date, statut, surface en m², budget, entreprise concernée)
- Voir le tableau récapitulatif (nombre de points, surface totale, avancement en %, budget total)

### Fonctionnalités Manager :
- Bouton de synchronisation
- Récupération des signalements en ligne (Firebase)
- Envoi des données nécessaires en ligne pour affichage mobile
- Gestion des informations par signalement (surface, budget, entreprise, etc.)
- Modification des statuts des signalements

*Confidential - Not for Public Consumption or Distribution*

---

## Module Mobile

### Fonctionnalités Utilisateur :
- Se connecter sur **Firebase** en ligne
- Signaler des problèmes routiers depuis la carte (Leaflet + OpenStreetMap en ligne)
- Localisation
- Affichage de la carte et récapitulatif (cf. fonctionnalités visiteur)
- Filtre : afficher uniquement mes signalements

*Confidential - Not for Public Consumption or Distribution*

---

## Notes

- **Fonctionnalités**
- **Code** : hébergé sur GitHub ou GitLab public
- **Design**
- **Suivi des tâches**
- **APK pour mobile**
- **Documentation technique**
- **Aléas possibles**

*Confidential - Not for Public Consumption or Distribution*

---

## Contenu de la Documentation Technique

- **Projet** :
  - MCD (Modèle Conceptuel de Données)
  - Scénarios d’utilisation avec copies d’écran
- **Liste des membres** :
  - Nom, prénom et NumETU

*Confidential - Not for Public Consumption or Distribution*