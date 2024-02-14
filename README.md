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

🔻

## A7 – Architecture d'intégration - choisir le meilleur mode de communication entre chaque brique logicielle
### Objectifs du TD
*	Questionner les différents modes d'échanges (Requête, Message, BDD, Fichier)
*	Apprendre à se poser les bonnes questions
### Description de l’activité
* A partir du schéma construit à l'activité suivante, choisir comment les modules applicatifs communiquent entre eux, argumenter chaque choix d'échange de données.
* Rajouter les bases de données permettant de stocker les types de données suivantes: > 💾 Base des données de référence (liste capteurs, besoins de pose...) 💾 Base des données collectées sur les capteurs (historiques de valeurs...) 💾 Informations relatives à l'installation des capteurs (CR d'installation, état des poses)

