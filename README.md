# Cours Architecture de Systèmes d’Information
**Travaux Dirigés 2024 - Julien COGNET**


> 💬 Votre travail va remplir une grande partie de votre vie, et la seule façon d'être vraiment satisfait est de faire ce que vous croyez être un grand travail. Et la seule façon de faire un grand travail est d'aimer ce que vous faites.
>
> **Steve Jobs**

🔻


## A1 – Quizz d’évaluation des compétences informatiques
Accédez au quiz sur https://joinmyquiz.com 

🔻

## A2 - Découverte d’un référentiel d’architecture d’entreprise
### Objectifs du TD
*	Comprendre le concept et l’intérêt des vues
*	Mettre du concret sur tous les concepts abordés en début de cours
*	Découvrir un référentiel d’EA

### Description de l’activité
-	Par groupe de 4 personnes
-	Contexte : 4 postes d’architectes sont ouverts dans l’entreprise dans laquelle vous intervenez et tous les groupes sont mis en concurrence pour obtenir ce poste. Le DSI vous pose 4 questions à chacun des groupes auxquelles vous devez essayer 
-	Le DSI vous pose ces 4 questions :
    - Q1 - Quels sont les 2 domaines métiers les moins bien digitalisés (c'est-à-dire les moins pourvus en outil efficace) ?
    - Q2 - Pouvez-vous me décrire la stratégie applicative qui a été adoptée pour mieux gérer la télérelève des compteurs (Meter Management) ?
    - Q3 - Internet explorer sera bientôt dé-commissionné. Quels sont les risques encourus par mon SI ? 
    - Q4 - Quelles sont les économies réalisables si nous rationalisons les applications utilisées pour analyser les prix de l'énergie (si nous omettons la problématique d'adéquation technique) ? 
-	Vous disposez de 15 minutes pour rechercher la réponse à la question qui vous est posée dans l'outil de capitalisation d'architecture d'entreprise EssentialViewer disponible à l'adresse suivante https://essentialviewer.com
-	Chaque fois que vous pensez avoir trouvé la bonne réponse, faites vérifier votre réponse auprès du professeur.
-	Le premier groupe à avoir répondu avec succès aux 4 questions aura l’opportunité de présenter les résultats de son étude au DSI.

🔻

## A3 – Créez le business motivation model du projet de déploiement de capteurs IoT pour un grand acteur énergétique
### Objectifs du TD
*	Découvrir le langage de modélisation Archimate
*	Comprendre les rudiments de l’architecture des motivations
*	S’entraîner au questionnement à base de questions ouvertes et à l’écoute active
*	Prendre de la hauteur de vue par rapport à un problème
### Description de l’activité
*	Ouvrir https://app.diagrams.net/
*	Créez un nouveau diagramme à partir du modèle « Business Motivation Model Sample.drawio » grâce à l’entrée de menu File > Open from … > Device
*	Posez des questions à votre professeur qui joue le rôle du directeur de département SI des Systèmes Connectés
*	Présenter votre diagramme complété à l’ensemble de la classe


🔻
 
## A4 – Créez le business motivation model du projet de déploiement de capteurs IoT pour un grand acteur énergétique
### Objectifs du TD
*	Approfondir sa connaissance du langage BPMN (Business Process Modeling Notation)
*	S’entraîner à modéliser un processus métier
### Description de l’activité
*	Ouvrir https://demo.bpmn.io/new
*	Questionnez le formateur pour comprendre le processus métier
*	Modélisez à plusieurs le processus métier existant et le processus métier futur
*	Pensez bien à modéliser les cas d’erreur

🔻

## A5 – Analyse et choix des principes d’architecture les plus appropriés à notre cas fil rouge
### Objectifs du TD
*	Approfondir sa connaissance du langage BPMN (Business Process Modeling Notation)
*	S’entraîner à modéliser un processus métier
### Description de l’activité
*	Parcourir le catalogue de principes d’architecture proposé en annexe du support de cours
*	Choisir 3 principes d’architecture qui s’appliquent particulièrement au contexte du projet fil rouge.
*	Expliquez pourquoi vous avez choisi ce principe d’architecture

🔻

## A6 – Architecture applicative - approche C4
### Objectifs du TD
*	Découvrir l'approche de modélisation C4 de Simon Brown
*	Identifier les modules fonctionnels d'un logiciel
*	Réfléchir au découpage d'une architecture logicielle
*	Représenter une architecture logicielle
### Description de l’activité
- A partir de la description du besoin applicatif et des questions que vous poserez à votre professeur. Identifiez la liste des composants applicatifs, des bases de données, et des utilisateurs de l'application

>    <details>
>    <summary>Réponse à ne consulter qu'en extrême recours</summary>
> ⚫ Application mobile d'outil de déploiement du technicien ⚫ Application web de référencement des capteurs et des besoins de pose ⚫ Application de consultation des historiques de données collectées 
> ⚫ Portail de l'opérateur LoRAWAn (Bouygues Telecom et Orange) ⚫ Système de collecte et traitement 
> 📲 Capteurs ⛅ Réseau LoraWan 👤 Technicien 👤 Client 👤 Gestionnaire des systèmes connectés
> </details>

- Dessinez les niveaux Context et Containers de cette architecture en précisant les interactions entre les différents composants / utilisateurs

### Processus métier
![image](https://github.com/juliencognet/CoursArchitectureSI2024/assets/26428851/7dc22dd0-6a61-48a0-bf1c-b9604c24fb1b)

* Un ingénieur d'exploitation définit les besoins de pose de capteurs dans l'application exploitation
* Il achète ensuite des capteurs et les déclare dans un référentiel de capteurs.
* Quand il déclare ces capteurs, une action sera automatiquement réalisée sur les portails des opérateurs télécom (Objenious ou LiveObject) pour déclarer les capteurs qui seront installés (pour qu’ils puissent être reconnus par le réseau).
* Un technicien récupère grâce à son application mobile de pose une liste de besoins de pose à pourvoir, il récupère des capteurs physiques.
* Ces capteurs physiques sont ensuite installés sur site. 
* Lors de l’installation, il passe un aimant sur le capteur qui se met à émettre des données sur le réseau Lora.
* Les données transitent alors sur le réseau LoraWan, sont interceptées par un opérateur LoraWan qui pousse ensuite les données de façon asynchrone au système de collecte, traitement et sauvegarde des données.
* Le système de collecte, traitement et sauvegarde des données vérifie si les données qu'il reçoit correspondent à des capteurs déclarés dans le référentiel de capteurs. Si c'est le cas, il historise les valeurs reçues dans une base de données historique.
* Si jamais les données ne sont pas reçues côté Dalkia, il doit repasser plusieurs jours après pour réinstaller le capteur ou le remplacer.
* Enfin les clients de Dalkia peuvent accéder à leurs données historisés via un portail client. Le portail client (hors scope du système étudié) utilise une API d'exposition des données externes fournies par notre système d'information.


🔻

## A7 – Architecture d'intégration - choisir le meilleur mode de communication entre chaque brique logicielle
### Objectifs du TD
*	Questionner les différents modes d'échanges (Requête, Message, BDD, Fichier)
*	Apprendre à se poser les bonnes questions
### Description de l’activité
* A partir du schéma construit à l'activité suivante, choisir comment les modules applicatifs communiquent entre eux, argumenter chaque choix d'échange de données.
* Rajouter les bases de données permettant de stocker les types de données suivantes: > 💾 Base des données de référence (liste capteurs, besoins de pose...) 💾 Base des données collectées sur les capteurs (historiques de valeurs...) 💾 Informations relatives à l'installation des capteurs (CR d'installation, état des poses)


### Indications supplémentaires
* Schéma duquel partir pour choisir les modes de communications : https://github.com/juliencognet/CoursArchitectureSI2024/assets/26428851/7332016b-f729-4a06-a7ba-f5c7817fd616
* Pour la sécurité du personnel qui intervient dans les chaudières, des capteurs de présences IoT sont installés dans les locaux qui hébergent les équipements. Si une personne est détectée, alors aucune commande ne doit être envoyée à l'équipement de chauffage, et c'est l'information de présence qui permet de gérer cette interdiction.
* Le schéma support de l'exercice propose 2 bases de données pour stocker les informations manipulées par notre application. Cela force un mode de communication entre certains composants du système. Est-ce une bonne pratique ? Quelle alternative pourrait-on proposer ? Quels sont les avantages et inconvénients à dupliquer les données ?


🔻

## A8 – Architecture de données - Concevoir le modèle logique de données relationnelles
### Objectifs du TD
*	Apprendre à réaliser une modélisation de base de données
### Description de l’activité
* Modéliser avec DBDiagram (https://dbdiagram.io/d) le modèle logique relationnel de données qui permet de modéliser le sous-domaine de notre cas fil rouge
### Sous-domaine à modéliser
* Un besoin de pose identifie le besoin d’installer plusieurs capteurs d’un certain type sur un site avant une date cible.
* Lors de l’installation d’un capteur, un technicien identifié par son matricule et son nom sélectionne un capteur physique identifié par son identifiant unique et l’installe sur un site à un emplacement donné pour répondre à un besoin de pose à une date d’installation donnée.
* Enfin, l’installateur fournira un statut d’installation pour préciser si l’installation s’est terminée en succès ou en échec.
* En cas d’échec, le technicien doit saisir une cause d’échec parmi une liste de causes disponibles.


🔻

## A9 – Architecture de données - Concevoir le modèle en étoile permettant d'analyser l'activité 
### Objectifs du TD
*	Apprendre à réaliser une modélisation de base de données
### Description de l’activité
* Modéliser avec DBDiagram (https://dbdiagram.io/d) le modèle logique relationnel de données qui permet de modéliser le sous-domaine de notre cas fil rouge
### Problème à résoudre
* Contexte: analyse des succès / échecs d’installation
* De nombreuses installation de capteurs IoT se terminent en échec actuellement. Nos ingénieurs d’exploitation souhaitent en déterminer les causes. Par conséquent, ils souhaitent obtenir un reporting analytique qui leur permet d’analyser les causes de succès et d’échec suivant différents axes. 
* A partir du modèle de données précédent, concevoir le star schéma qui permettra d’analyser le problème suivant les différentes dimensions.
* Déterminer d’abord quelles sont les métriques analysées
* En déduire la table de faits,
* Puis ajouter toutes les dimensions disponibles sous forme de tables additionnelles jointes à la table de faits





🔻

## Devoir noté à faire par groupe pour la dernière séance

### Objectifs & critères d'évaluation
- Etudier en groupe les solutions d'architecture à apporter pour répondre à un critère de **qualité logicielle**
- Vous serez évalués en groupe sur la **qualité de vos arguements**
- Vous serez évalués individuellement sur votre **aisance à l'oral et votre capacité à expliquer votre sujet**
- Vous serez évalués en groupe sur votre **respect du sujet et la façon de le raccrocher à des éléments abordés en cours**

### Consigne
- Activité à faire en groupe
- Les groupes se répartissent les critères de qualité suivants (chaque critère de qualité doit être pris au moins une fois):
    - Adéquation fonctionnelle
    - Performance
    - Robustesse
    - Maintenabilité / évolutivité
    - Exploitabilité
    - Portabilité
    - Empreinte écologique
    - Sécurité
 - Votre exposé durera 10min
 - Tous les membres du groupe doivent présenter une partie de l'exposé à l'oral 
 - Votre exposé doit suivre le plan suivant:
    - Importance de la problématique (pourquoi faut-il se soucier de ...)
    - Questions à poser aux interlocuteurs métier lors des phases d'étude de l'architecture stratégique et fonctionnelle
    - Critères et moyens de mesure
    - Quelle solution d'architecture applicative (logicielle et/ou données) apporter ?
    - Quelle solution d'architecture technique apporter ?  
