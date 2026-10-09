# 🌾 Transformation Numérique & Gouvernance de la Traçabilité de la Chaîne de Valeur Agro-Industrielle (Cas SAAC)

> **Projet d'Architecture d'Entreprise, Intégration ERP/SCM, IoT, Blockchain et Gouvernance des TI face aux exigences du Règlement Européen sur la Déforestation (RDUE).**

---

## 📌 Sommaire Exécutif

La **Société Agricole d’Achat du Cacao (SAAC)** est une entreprise de négoce international opérant entre les coopératives agricoles de Côte d'Ivoire et les multinationales exportatrices. 

Historiquement, l’ensemble de ses opérations (achats bord champ, pesées, contrôle qualité, expéditions maritimes) reposait sur des processus manuels et des registres papier. Cette absence de supervision numérique provoquait :
* Des **pertes financières directes de 5 à 15 %** du tonnage annuel déclaré (fraudes, vols, freintes non tracées).
* Des **conflits de concordance qualité** récurrents entre les magasins régionaux et le port d'exportation d'Abidjan.
* Un **risque juridique et commercial existentiel** : l'incapacité formelle de prouver la provenance licite du cacao face aux nouvelles réglementations internationales, notamment le **Règlement de l'Union Européenne sur la Déforestation (RDUE)** et les normes strictes de lutte contre le travail des enfants.

### La Solution Modélisée
Ce projet propose une **Refonte des Processus d'Affaires (BPR)** complète articulée autour :
1. D'un **Progiciel de Gestion Intégré (ERP)** centralisant les flux d'achats, stocks, finances et logistique (**SCM / WMS / TMS**).
2. D'un niveau opérationnel durci (**STT / TPS**) alimenté par des terminaux mobiles de terrain et des balances connectées (**IoT / Edge Computing**).
3. D'un référentiel de parcelles géré par **Master Data Management (MDM)** et vérifié par géorepérage GPS (**Geofencing**).
4. D'un registre immuable (**Blockchain & Smart Contracts**) certifiant l'authenticité de la chaîne de traçabilité jusqu'à l'embarquement portuaire.
5. D'une gouvernance d'entreprise alignée sur **COBIT**, le modèle des **Trois Lignes** et la norme **ISO/IEC 27001**.

---

## 🏢 Analyse de la Situation Actuelle (As-Is) & Diagnostic
### Dysfonctionnements Majeurs Identifiés :
1. **Défaillance de la Qualité des Données :** L'information sur papier souffre de redondances massives, d'erreurs de transcription et de délais d'acheminement de plusieurs jours, empêchant toute supervision en temps réel.
2. **Vulnérabilité à la Fraude et Corruption Locale :** L'absence de séparation des tâches (**SoD**) permettait aux magasiniers et contrôleurs de manipuler manuellement les registres de poids et les catégories de qualité.
3. **Risque de Non-Conformité Réglementaire (Quadrant Illégal & Non Éthique) :** Pénétration clandestine de fèves cultivées dans des forêts classées protégées ou exploitant la main-d'œuvre infantile, exposant la SAAC au rejet immédiat des cargaisons à destination de l'Europe.
4. **Blocage Décisionnel :** La direction générale était confinée dans la résolution d'urgences opérationnelles de bas niveau, sans accès à des tableaux de bord analytiques fiables (**MIS / EIS**).

---

## 🏛️ Architecture Cible du Système d'Information (To-Be)

L'architecture d'entreprise cible décloisonne les 4 filiales régionales et le siège social à travers une architecture en couches intégrée :
### 1. Dorsale Progicielle (ERP / SCM / CRM)
* **ERP Central :** Module unique unifiant la comptabilité d'achat, les valorisations d'inventaires et les règlements bancaires.
* **SCM & WMS / TMS :** Planification des flux de cacao, gestion de l'adressage en entrepôt régional et optimisation des tournées camions avec suivi GPS en direct.
* **CRM Fournisseurs :** Fiche d'identité numérique de chaque coopérative et planteur incluant l'historique de conformité légale et sociale.
* **STT / TPS Intégré :** Chaque pesée et analyse qualité génère un événement transactionnel inviolable respectant les propriétés **ACID** (Atomicité, Cohérence, Isolation, Durabilité).

### 2. Captation Terrain, IoT & Edge Computing
* **Balances Numériques Connectées (IoT / Edge) :** Les balances électroniques de bord-champ et de magasin pèsent et chiffrent la donnée directement à la source (*Edge Computing*), interdisant toute saisie manuelle manipulable.
* **Géorepérage Dynamique (Geofencing) :** Intégration du cadastre officiel des forêts classées de Côte d'Ivoire. Si les coordonnées GPS de collecte ou l'itinéraire du camion intersectent une zone protégée, le système génère un blocage transactionnel immédiat.

### 3. Gestion des Données Maîtres (MDM) & Blockchain
* **Master Data Management (MDM) :** Création du *Golden Record* pour chaque parcelle (Identifiant unique, polygone GPS vérifié, statut de certification).
* **Smart Contracts & Blockchain :** Les attributs critiques (`Plantation_ID`, `Tonnage`, `Statut_Non_Déforestation`, `Audit_Travail_Enfants`) sont ancrés dans un registre distribué immuable. Un contrat intelligent (*Smart Contract*) rejette automatiquement le lot si l'audit social de l'exploitant a expiré.
* **Data Lineage (Lignage de la donnée) :** Reconstitution instantanée de la filiation complète d'un sac de cacao de l'arbre jusqu'au conteneur maritime.

---

## 🔒 Cadre de Gouvernance, Sécurité & Maîtrise des Risques

Le déploiement technique s'adosse à un cadre de contrôle interne robuste pour garantir que l'outil informatique se traduise par une conformité réelle :

```text
          ┌────────────────────────────────────────────────────────┐
          │     CONSEIL D'ADMINISTRATION & DIRECTION GÉNÉRALE      │
          │         Appétence au risque • Alignement COBIT         │
          └───────────────────────────┬────────────────────────────┘
                                      │
       ┌──────────────────────────────┼──────────────────────────────┐
       ▼                              ▼                              ▼
 1re LIGNE (Métier)           2e LIGNE (Supervision)        3e LIGNE (Assurance)
Acheteurs, Magasiniers        RSSI, Responsable Qualité      Audit Interne Indépendant
Application des contrôles     Surveillance des alertes       Vérification des preuves
```
   ### 1. Séparation des Tâches (Segregation of Duties - SoD)
Application stricte de la règle des quatre yeux :
* Le commercial terrain ne peut pas valider l'analyse qualité.
* Le contrôleur qualité du magasin ne peut pas modifier la pesée IoT.
* Le chef de site ne peut pas décaisser les fonds sans rapprochement automatique 3 voies (Bon de réception + Pesée IoT + Certificat GPS).

### 2. Sécurité de l'Information & Zero Trust (ISO/IEC 27001 & 27002)
* **IAM & Authentification Forte (MFA) :** Accès aux applications conditionné par des certificats matériels et authentification multifacteur pour tous les chefs de sites et acheteurs.
* **Chiffrement de bout en bout :** Données en transit sécurisées par TLS 1.3 / mTLS entre les boîtiers IoT et l'ERP ; données au repos chiffrées (AES-256) sur le Lakehouse.
* **Gestion du Risque Résiduel :** Réduction du risque brut (rejet des cargaisons à l'export) à un niveau résiduel maîtrisé sous le seuil d'appétence fixé par le Conseil d'administration.

---

## 📊 Facteurs Clés de Performance (KPI / KRI) & Résultats Modélisés

| Indicateur | Typologie | Définition & Formule | Cible Visée |
| :--- | :--- | :--- | :--- |
| **TCEL** *(Taux de Conformité Éthique & Légale)* | KPI Efficacité | $(Lots\ validés\ conformes\ RDUE / Total\ lots\ achetés) \times 100$ | **100 %** |
| **TCT** *(Taux de Conformité des Tonnages)* | KPI Efficience | $(Tonnage\ réceptionné\ port / Tonnage\ acheté\ bord\ champ) \times 100$ | **> 98 %** *(Pertes < 2 %)* |
| **TCQ** *(Taux de Concordance Qualité)* | KPI Contrôle | $(Lots\ confirmés\ port / Lots\ catégorisés\ magasin) \times 100$ | **> 95 %** |
| **Temps de Traçabilité Bout-en-Bout** | KPI Agilité | Temps requis pour extraire l'arbre généalogique d'un lot exporté | **< 5 minutes** *(vs 4 jours)* |
| **KRI Anomalies Géorepérage** | KRI Risque | Alertes de tentatives de collecte en zone classée | **0 alerte non traitée** |

---

## 📅 Méthodologie de Déploiement (CVES / SDLC)

Le projet est articulé selon un cycle de développement structuré en 4 phases majeures (18 mois) :

1. **Phase 1 : Cadrage, Analyse & Sélection (Mois 1-3) :** Formalisation des exigences RDUE, matrice RACI, cahier des charges et sélection de l'intégrateur ERP.
2. **Phase 2 : Modélisation, Architecture & Développement (Mois 4-9) :** Conception du schéma entité-association, configuration des modules SCM/WMS, développement des connecteurs API IoT et des Smart Contracts.
3. **Phase 3 : Tests d'Intégration & Déploiement Pilote (Mois 10-18) :** Tests d'acceptation utilisateur (UAT), tests de résilience réseau et mise en service pilote sur la filiale régionale d'Abengourou avant généralisation.
4. **Phase 4 : Exploitation, Audit & Analytique Avancée (Mois 19+) :** Activation des modèles prédictifs d'achat, audits ISO 27001 et exploitation des tableaux de bord décisionnels.

---

## 💡 Création de Valeur & Conclusion

Ce projet démontre qu'une modernisation technologique ne se résume pas à l'achat d'outils, mais à l'alignement harmonieux entre **Personnes, Processus, Données, Technologies et Gouvernance** :
* **Valeur Financière :** Récupération de 8 à 13 % de pertes de fèves, générant un retour sur investissement (ROI) estimé sous 18 mois.
* **Valeur Stratégique & Commerciale :** Positionnement de la SAAC comme exportateur de premier rang capable de fournir un cacao certifié « zéro déforestation » auditable par QR Code.
* **Valeur Éthique & Sociale :** Contribution directe à la préservation du couvert forestier ivoirien et à l'élimination du travail des enfants dans la filière.

---
*Auteur : Joye Badou — DESS en Gouvernance des Systèmes d'Information*
