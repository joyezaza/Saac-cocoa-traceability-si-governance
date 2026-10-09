# 🌾 De la Plantation au Port : Traçabilité Numérique et Gouvernance de la Chaîne du Cacao (Cas SAAC)

> Projet de Modernisation des Systèmes d'Information, Architecture d'Entreprise et Gestion des Risques  
> Comment transformer une chaîne d'approvisionnement agro-industrielle manuelle et opaque en un écosystème numérique infalsifiable conforme aux normes internationales (Règlement Européen sur la Déforestation - RDUE).

---

## 📌 Table des Matières
1. Sommaire Exécutif & Cadrage Métier
2. Diagnostic de la Situation Actuelle (As-Is) & Dysfonctionnements
3. Le Parcours Concret d'un Lot : Avant vs Après
4. Architecture Cible du Système d'Information (To-Be)
5. Rôle Pratique et Opérationnel des Outils Technologiques
6. Cadre de Gouvernance, Contrôle Interne & Cybersécurité
7. Indicateurs Clés de Performance (KPI / KRI) & Métriques Cibles
8. Méthodologie et Feuille de Route de Déploiement (18 Mois)
9. Création de Valeur Globale & Enseignements

---

## 1. Sommaire Exécutif & Cadrage Métier

### Le Métier de la SAAC
La Société Agricole d’Achat du Cacao (SAAC) est une entreprise privée de négoce international opérant en Côte d'Ivoire. Elle assure le rôle d'intermédiaire commercial et logistique entre des milliers de petits exploitants agricoles / coopératives locales et les grands négociants et chocolatiers mondiaux (Europe, Amérique du Nord). L'entreprise s'organise autour d'un siège central à Abidjan et de quatre filiales régionales situées au cœur des bassins de production.

### La Problématique d'Affaires
Historiquement, la totalité de la chaîne d'approvisionnement (achats en bord champ, chargement, pesées intermédiaires, tests d'humidité, stockage et transport portuaire) reposait sur des processus manuels et des registres papier. Cette absence de visibilité numérique engendrait trois menaces majeures :
* Pertes financières massives : Entre l'achat en brousse et l'embarquement portuaire, 5 à 15 % du tonnage disparaissait chaque année (vols, détournements de cargaisons, erreurs de pesée mécanique et freintes non contrôlées).
* Discordance et fraude sur la qualité : Des lots déclarés de premier choix en magasin régional arrivaient déclassés au port après mélange clandestin ou altération, causant des litiges et des pénalités financières.
* Risque réglementaire existentiel : L'Union Européenne a mis en application le Règlement sur la Déforestation (RDUE), interdisant l'importation de cacao cultivé sur des terres déboisées après 2020 ou lié au travail des enfants. Incapable de prouver l'origine parcellaire de ses fèves, la SAAC risquait l'embargo total et la faillite.

### La Réponse Stratégique
La solution conçue ne se limite pas à informatiser des cahiers existants ; elle orchestre une Refonte des Processus d'Affaires (BPR) complète. Elle déploie un système d'information intégré reliant des balances connectées (IoT), un suivi de flotte par géorepérage (GPS/Geofencing), une dorsale de gestion unifiée (ERP / SCM), un référentiel de données maîtres (MDM) et un registre immuable de certification (Blockchain).

---

## 2. Diagnostic de la Situation Actuelle (As-Is) & Dysfonctionnements

Flux Actuel :
* Étape 1 (Plantation) : Négociation orale bord champ, aucun contrôle d'origine ni d'âge des travailleurs.
* Étape 2 (Transport initial) : Transport en vrac sans suivi, arrêts non tracés.
* Étape 3 (Magasin régional) : Pesée mécanique sur peson manuel, enregistrement sur cahier papier.
* Étape 4 (Analyse 1) : Évaluation visuelle de la qualité par le magasinier (fort risque de complaisance).
* Étape 5 (Transport portuaire) : Camions tiers sans balise GPS, risques de déchargements sauvages.
* Étape 6 (Arrivée au port) : Analyse 2 par un laboratoire tiers révélant des écarts de qualité et de tonnage inexpliqués.

Dysfonctionnements majeurs :
1. Défaillance de la Qualité des Données : L'information sur papier souffre de redondances, d'erreurs d'écriture et de retards de plusieurs jours.
2. Vulnérabilité à la Fraude Locale : L'absence de séparation des tâches permet aux magasiniers de manipuler les registres.
3. Risque d'Exclusion Internationale : Incapacité d'apporter la preuve de non-déforestation exigée par l'UE (RDUE).
4. Pilotage à l'Aveugle : La direction générale ne dispose d'aucun tableau de bord fiable en temps réel.

---

## 3. Le Parcours Concret d'un Lot : Avant vs Après

| Étape du Flux | Processus Actuel (As-Is / Papier) | Risques et Vulnérabilités | Processus Cible (To-Be / Numérique) | Contrôle et Sécurité Apportés |
| :--- | :--- | :--- | :--- | :--- |
| 1. Enregistrement Plantation | Déclaration orale, aucun relevé géographique. | Achat de cacao cultivé en forêt classée interdite. | Cartographie GPS de la parcelle enregistrée dans le MDM. | Vérification automatique d'exclusion des zones protégées par cadastre numérique. |
| 2. Achat bord champ & Pesée | Peson mécanique à ressort, reçu écrit à la main au crayon. | Falsification du poids par l'acheteur, vol de fèves, prix arbitraire. | Balance numérique connectée (IoT / Edge) et application mobile synchronisée. | Le poids est chiffré et horodaté dès la pesée ; aucun champ modifiable à la main. |
| 3. Transport régional | Chauffeur sans suivi d'itinéraire, lettre de voiture papier. | Détournement du camion, chargement clandestin de sacs illégaux en route. | Balise télématique GPS sur le camion avec géorepérage (Geofencing). | Alerte immédiate au siège social si le véhicule s'arrête en zone anormale ou dévie de sa route. |
| 4. Réception magasin & Qualité | Analyse visuelle manuelle notée sur cahier par le magasinier. | Corruption locale, reclassement complaisant de cacao moisi ou trop humide. | Analyseur d'humidité connecté et tablette dédiée au contrôleur qualité (Séparation SoD). | Rapprochement automatique 3 voies dans l'ERP (Poids IoT + Qualité + Identifiant Planteur). |
| 5. Transport vers le Port | Transport vrac confié à des prestataires non tracés. | Déchargement partiel en cours de route, freintes inexpliquées (5 à 15 %). | Scellés électroniques RFID sur les conteneurs et pesée automatisée au pont-bascule portuaire. | Comparaison instantanée entre le tonnage de départ et d'arrivée ; tolérance fixée à moins de 2 %. |
| 6. Vente et Export | Dossier douanier papier expédié par courrier, contestations fréquentes. | Rejet des cargaisons aux douanes européennes par manque de preuves RDUE. | Émission d'un QR Code lié à un contrat intelligent (Blockchain Smart Contract). | Les acheteurs scannent le lot et accèdent en 30 secondes à la preuve infalsifiable d'origine. |

---

## 4. Architecture Cible du Système d'Information (To-Be)

L'architecture décloisonne les filiales régionales et le siège social à travers une structure en couches :

1. Couche Décision & Gouvernance : Tableaux de Bord Exécutifs (EIS/BI), alertes conformité RDUE en temps réel et suivi du risque résiduel.
2. Couche Dorsale Applicative (ERP Central) : Modules Finances, Achats, Chaîne Logistique (SCM), Gestion d'entrepôt et transport (WMS/TMS), et moteur transactionnel (STT/TPS).
3. Couche Collecte Terrain : Application mobile commerciale avec coordonnées GPS, balances connectées (IoT), boîtiers camions géorepérés.
4. Couche Confiance & Registre Distribué : Blockchain de traçabilité, contrats intelligents (Smart Contracts) rejetant automatiquement les lots non certifiés, et QR Codes pour les acheteurs internationaux.

---

## 5. Rôle Pratique et Opérationnel des Outils Technologiques

1. L'ERP / PGI (Progiciel de Gestion Intégré) :
Centralise les Achats, Stocks, Logistique et Comptabilité. Dès qu'un sac de cacao est scanné et pesé, l'ERP met à jour le stock disponible, calcule le paiement officiel, génère la liasse de transport et passe l'écriture comptable sans ressaisie.

2. Le Moteur Transactionnel (STT / TPS) :
Garantit le respect des propriétés ACID (Atomicité, Cohérence, Isolation, Durabilité). Si la connexion mobile coupe au milieu d'un enregistrement en brousse, la transaction n'est pas corrompue et se resynchronise dès le retour du réseau.

3. Les Balances Connectées (IoT & Edge Computing) :
Les balances capturent la masse, la signent numériquement et la transmettent par réseau mobile. L'opérateur ne peut pas modifier le chiffre sur son écran pour voler la différence de poids.

4. Le Géorepérage GPS (Geofencing) :
Le cadastre des forêts classées de Côte d'Ivoire est intégré dans l'application mobile. Si un commercial tente d'enregistrer un achat sur des coordonnées GPS situées dans un périmètre protégé, le système bloque la transaction.

5. La Gestion des Données Maîtres (MDM — Master Data Management) :
Crée le Golden Record (enregistrement unique et certifié) de chaque producteur. Empêche qu'un même planteur soit enregistré deux fois avec des identités ou des surfaces différentes.

6. La Blockchain & les Smart Contracts :
Registre distribué partagé entre la SAAC, les coopératives, les douanes et les clients exportateurs. Un Smart Contract rejette automatiquement le lot si l'audit social de conformité (zéro travail des enfants) a expiré.

7. La Business Intelligence (BI / EIS) :
Tableaux de bord visuels en temps réel pour la direction à Abidjan. Les dirigeants identifient les anomalies de tonnage par région, les niveaux de stock portuaire et l'état de conformité des commandes en cours d'embarquement.

---

## 6. Cadre de Gouvernance, Contrôle Interne & Cybersécurité

Organisation en Trois Lignes de Maîtrise :
* 1re Ligne (Opérations & Terrain) : Acheteurs, magasiniers et chauffeurs appliquant les contrôles obligatoires via l'application mobile et les balances connectées.
* 2e Ligne (Supervision & Conformité) : Le Responsable de la Sécurité des Systèmes d'Information (RSSI) et le Responsable Qualité surveillant les alertes de géorepérage et les écarts de stock.
* 3e Ligne (Assurance Indépendante) : Audit interne réalisant des pesées inopinées sur site pour vérifier la concordance exacte entre stock physique et stock numérique.

Séparation des Tâches (Segregation of Duties - SoD) :
* Le commercial terrain ne peut pas évaluer la qualité du produit.
* Le contrôleur qualité du magasin ne peut pas modifier la pesée issue de la balance IoT.
* Le chef de site régional ne peut pas ordonner le paiement bancaire sans le rapprochement automatique 3 voies (Pesée IoT + Analyse Qualité + Certificat GPS hors forêt classée).

Cybersécurité & Modèle Zero Trust (Alignement ISO/IEC 27001 & 27002) :
* Gestion des Identités (IAM & MFA) : Chaque employé dispose d'un compte individuel protégé par authentification multifacteur (MFA).
* Gestion des Comptes à Privilèges (PAM) : Les accès des administrateurs aux serveurs sont temporaires et journalisés de manière inaltérable.
* Chiffrement : Flux chiffrés en transit (mTLS / TLS 1.3) et bases de données chiffrées au repos (AES-256).

---

## 7. Indicateurs Clés de Performance (KPI / KRI) & Métriques Cibles

| Indicateur | Typologie | Définition & Formule de Calcul | Cible Visée |
| :--- | :--- | :--- | :--- |
| TCEL (Taux de Conformité Éthique & Légale) | KPI Efficacité | (Lots validés conformes RDUE / Total lots achetés) * 100 | 100 % |
| TCT (Taux de Conformité des Tonnages) | KPI Efficience | (Tonnage réceptionné port / Tonnage acheté bord champ) * 100 | > 98 % (Pertes < 2 %) |
| TCQ (Taux de Concordance Qualité) | KPI Contrôle | (Lots confirmés port / Lots catégorisés magasin) * 100 | > 95 % |
| Temps de Traçabilité Bout-en-Bout | KPI Agilité | Temps pour extraire l'historique complet d'un lot exporté | < 5 minutes (vs 4 jours) |
| KRI Alertes Géorepérage | KRI Risque | Tentatives d'achat ou de transit en zone protégée | 0 alerte non traitée |

---

## 8. Méthodologie et Feuille de Route de Déploiement (18 Mois)

Déploiement en 5 phases structurées (Cycle de Vie d'Élaboration des Systèmes - CVES) :
* Mois 1 à 3 (Phase 1) : Cadrage, analyse des besoins RDUE et sélection de l'ERP.
* Mois 4 à 9 (Phase 2) : Modélisation, paramétrage ERP/SCM, intégration IoT et Smart Contracts.
* Mois 10 à 14 (Phase 3) : Déploiement Pilote sur le site régional d'Abengourou et tests d'acceptation utilisateur (UAT).
* Mois 15 à 18 (Phase 4) : Généralisation aux 4 filiales régionales et raccordement au port d'Abidjan.
* Mois 19 et plus (Phase 5) : Exploitation continue, audits de conformité ISO 27001 et exploitation de la BI prédictive.

---

## 9. Création de Valeur Globale & Enseignements

Ce projet démontre qu'une transformation numérique réussie repose sur l'alignement entre Personnes, Processus, Données, Technologies et Gouvernance :
* Valeur Financière : Récupération de 8 à 13 % de tonnages perdus, assurant un retour sur investissement (ROI) modélisé sous 18 mois.
* Valeur Stratégique & Commerciale : Pérennisation des contrats avec les multinationales du chocolat grâce à une certification infalsifiable par QR Code.
* Valeur Sociale & Éthique : Protection active des forêts classées ivoiriennes et élimination du travail des enfants dans la filière d'approvisionnement.

---
Projet d'étude conçu et formalisé par Joye Badou — Spécialisation en Gouvernance des Systèmes d'Information
