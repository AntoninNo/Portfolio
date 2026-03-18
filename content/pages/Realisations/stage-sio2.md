Title: Stage SIO2

> **<u>FICHE DESCRIPTIVE :</u>**

> <u>**Dates du stage :**</u>
>
> - **Date début :** 05/01/2026
> - **Date fin :** 13/02/2026
>
> **Entreprise :** SDIS de Seine-et-Marne

# Présentation de l'entreprise/société : Le SDIS – Service Départemental d'Incendie et de Secours
Le SDIS est l'organisme public chargé de la gestion des services d'incendie et de secours à l'échelle d'un département français. Il en existe un par département, soit 101 en France métropolitaine et outre-mer.
Le SDIS intervient dans trois grands domaines : la prévention et l'évaluation des risques, la protection des personnes, des biens et de l'environnement, ainsi que les secours d'urgence aux personnes (secours à victimes, aide médicale urgente).
Organisation
Il est placé sous l'autorité du préfet pour les missions opérationnelles, et sous celle du président du Conseil départemental pour sa gestion administrative et financière. Il est dirigé par un Directeur Départemental des Services d'Incendie et de Secours (DDSIS), officier sapeur-pompier.



# Missions & tâches réalisés : 

J'ai réalisé un outil d'analyse d'e-mail de phishing a l'aide d'un outil d'orchestration : N8N. Hebergé localement sur un ordinateur du SDIS, j'ai récupéré le projet déjà commencé par un autre stagiaire avant moi. 

1/ Boite mail 

Ceci ma amené au premier problème rencontré au niveau de la boite mail car la boite utilisé precédemment était une GMAIL sauf qu'elle était banni en environ 3 semaines car ils soupçonnaient un email de phishing a cause des tests, j'ai donc du chercher d'autre alternative et j'ai jeté mon dévolu sur ProtonMail car le SDIS avait déjà des mails proton payants permettant de faire ce qu'on voulait sans rencontrer de problème de bannisement. 
Pour connecter cette adresse mail à N8N j'ai du utiliser un bridge qui imite une boite mail, j'ai effectuer la meme manipulation dans l'autre sens pour envoyer les mails (résultats) IMAP/SMTP 

2/ Analyse des e-mails

Une fois la boîte mail fonctionnelle, j’ai pu travailler sur la partie principale du projet : l’analyse automatique des e-mails reçus.

Le but de cet outil est d’analyser un e-mail suspect afin de déterminer s’il s’agit potentiellement d’un mail de phishing.

Pour cela, j’ai dû modifier et compléter le code déjà existant afin de :

récupérer le contenu des e-mails reçus,

analyser l’adresse e-mail de l’expéditeur,

extraire les informations importantes du message,

préparer les données pour qu’elles puissent être analysées par l’intelligence artificielle.

J’ai également ajouté différents tests de validation sur les adresses e-mail, afin de vérifier leur format et éviter certaines erreurs lors du traitement.

3/ Gestion des différents types d’e-mails

Un autre travail important a été d’adapter l’outil pour gérer différents formats d’e-mails.

En effet, lors des tests, nous avons constaté que les e-mails suspects pouvaient arriver sous plusieurs formes :

e-mails classiques,

e-mails transférés,

e-mails envoyés en pièce jointe au format EML.

J’ai donc dû modifier le code afin de prendre en compte ces différents cas et permettre au système d’extraire correctement les informations nécessaires à l’analyse.

Cela a demandé plusieurs ajustements et tests pour s’assurer que le traitement fonctionnait dans chaque situation.

4/ Intégration de l’intelligence artificielle

Une partie importante du projet consistait à utiliser un modèle d’intelligence artificielle pour analyser le contenu des e-mails.

Ce modèle devait interpréter les informations du message afin de déterminer si celui-ci présentait des caractéristiques d’un mail frauduleux ou de phishing.

Lors des premiers essais, nous utilisions un modèle assez léger pour gagner en rapidité. Cependant, ce modèle produisait des résultats incohérents, car les réponses variaient d’un test à l’autre pour un même e-mail.

Afin d’obtenir des résultats plus fiables, nous avons donc décidé d’utiliser un modèle plus performant, bien que légèrement plus lent. Cela a permis d’obtenir des analyses plus stables et plus cohérentes.

5/ Problèmes réseau et envoi des résultats

Une fois l’analyse réalisée, le système devait envoyer automatiquement un e-mail de réponse contenant les résultats de l’analyse.

Lors de la mise en place de cette fonctionnalité avec SMTP, j’ai rencontré un problème de configuration DNS empêchant l’envoi des mails vers des adresses externes.

Pour résoudre ce problème, j’ai contacté le support ProtonMail, qui m’a fourni les informations nécessaires pour corriger la configuration.

J’ai ensuite transmis ces informations à l’équipe chargée du réseau du SDIS, afin qu’ils puissent effectuer les modifications nécessaires sur l’infrastructure réseau.

Après ces ajustements, l’envoi des e-mails de résultats a pu fonctionner correctement.

<img src="../images/image a mettre.jpg" width="300">