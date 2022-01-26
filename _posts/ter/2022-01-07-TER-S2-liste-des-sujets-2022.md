---
layout: page-fullwidth
#
# Content
#
subheadline: "M1 INFO et MIAGE"
title: "Liste des sujets de TER 2022"
logo: "logo_blanc.png"
teaser: "Le TER (Travail d’Étude et de Recherche) est un stage sous la direction d’un encadrant universitaire ou industriel qui s’effectue par groupe de 2 à 4 étudiants (ingénierie) ou seul (recherche). Il sanctionne la fin du Master 1 et s’étend sur environ 3-4 mois (1 jour par semaine)."
categories:
  - TER
tags:
  - S2
  - NEWS
#
# Styling
#
image:
  thumb: "liste-unsplash.jpg"
  homepage: "header-liste-unsplash.jpg"
header:
  image_fullwidth: "header-liste-unsplash.jpg"
---

1. TOC
{:toc}

{% include numbered-headings main=3 %}

N'hésitez pas à consulter aussi les listes des années précédentes accessibles en bas de la [page principale du TER]({% post_url /s2/2018-09-07-travail-etude-recherche %})

### Compression d’ensembles ordonnés ###

- Nombre d'étudiants souhaité : 1-2
- Encadrant : [Jean-Charles Régin & Marie Pelleau](mailto:jean-charles.regin@univ-cotedazur.fr,marie.pelleau@univ-cotedazur.fr).
- Prérequis : Aucun pré-requis n'est nécessaire. Cependant, une bonne connaissance de C ou Java est demandée.

#### Sujet ####
{:.no_toc}

Le but de ce TER est d'étudier et d'implémenter des algorithmes de compression d'ensembles ordonnés afin de permettre une représentation plus compacte d'un modèle structuré. 

L'idée générale est de remplacer le processus classique de transfert d'un modèle entre 2 ordinateurs par le processus suivant : compression - transfert - décompression. La difficulté est que ce second processus soit plus rapide.

Dans ce TER on se propose de définir des algorithmes de compression et décompression basés sur les spécificités de la programmation par contraintes.

En programmation par contraintes, les problèmes sont modélisés par un ensemble de variables, un ensemble de domaines, et un ensemble de contraintes. Les contraintes sont les relations qui existent entre les variables d'un problème. Les domaines sont les valeurs qui peuvent être prises par les variables.
Ils peuvent être représentés par un intervalle de valeurs (\[1, 10\], toutes les valeurs entre 1 et 10) ou par un ensemble de valeurs ({1, 2, 3, 4, 5, 6, 7, 8, 10}, toutes les valeurs de 1 à 8 et 10).
La première représentation est plus compacte mais beaucoup moins précise. En effet, on ne peut pas préciser qu'une valeur à l'intérieur de l'intervalle ne peut pas être prise par les variables.
La seconde représentation est beaucoup moins compacte cependant elle est beaucoup plus précise.

Dans le cas d'ensembles ordonnés, une solution pour compresser l'information est d'effectuer des différences puis d'utiliser un codage tel que le codage par plages \[1\] ou le codage de Huffman \[2\]. Par exemple, prenons l'ensemble {1, 2, 3, 4, 5, 6, 7, 8, 10}, le premier élément est conservé, puis pour les autres on effectue la différence entre lui-même et l'élément précédent. On obtient donc 1 1 1 1 1 1 1 1 2, huit 1 et un 2. En utilisant le codage par plages on peut représenter cet ensemble par 8112. D'autres codages plus récents seront considérés \[3,4\].

- Références :
  {%- include ref liste="
   -* Codage par plages ([page Wikipedia](https://fr.wikipedia.org/wiki/Codage_par_plages))
   -* Codage de Huffman ([page Wikipedia](https://fr.wikipedia.org/wiki/Codage_de_Huffman))
   -* Stream VByte: Faster Byte-Oriented Integer Compression -- Daniel Lemire, Nathan Kurz, Christoph Rupp ([pdf](https://arxiv.org/abs/1709.08990))
   -* Decoding billions of integers per second through vectorization -- Daniel Lemire, Leonid Boytsovn ([pdf](https://arxiv.org/abs/1209.2137))" %}


### Outils logiciels pour la gestion et la visualisation de données de capteurs ###

- Encadrant: [Eric Madelaine](mailto:eric.madelaine@inria.fr), Equipe Kairos, Inria
- Sujet ``ingénierie'' pour 2-3 étudiants.

#### Méthodes, langages ou technologies envisagés ####
{:.no_toc}

Les étudiant.e.s devront avoir des connaissances et un intérêt pour le développement logiciel, en particulier en environnement Java, et un intérêt pour un ou plusieurs des domaines suivants :

- IHM et interfaces graphiques Java
- Web sémantique, interfaces web sémantique / bases de données 

#### Sujet ####
{:.no_toc}

Speleograph (speleograph.free.fr) est un logiciel destiné à la visualisation de données de capteurs de mesures physiques, initialement dans le domaine de l’étude de débit des rivières souterraines, ou plus généralement la corrélation et la visualisation de données de capteurs. Nous souhaitons améliorer Speleograph pour simplifier et étendre son utilisation, en particulier pour des usages pédagogiques, dans le contexte du projet Edumed ([http://edumed.unice.fr/fr](http://edumed.unice.fr/fr)). Plus généralement, nous voulons pouvoir utiliser depuis Speleograph des données disponibles dans des bases de données sur le web, à travers des requêtes de type web sémantique du genre ``trouvez-moi les données de hauteur d’eau souterraines des cavités de tel secteur, entre 2019 et 2020''... Les vocabulaires nécessaires à décrire ces données, et leurs métadonnées, sont en course de définition par leprojet Karstlink ([http://uisic.uis-speleo.org/exchange/karstlink/index-fr.html](http://uisic.uis-speleo.org/exchange/karstlink/index-fr.html))

Le ou les stagiaires, après une familiarisation avec le sujet, devront :

- Mettre en place de nouvelles fonctionnalités pour le logiciel Spéléograph, en particulier répondant aux besoins spécifiques
des enseignants et des élèves dans le cadre d’Edumed.
- Ajouter à Speleograph un module d’accès à des ressources de type « séries de données de capteurs physiques ».
- Participer à la définition des ontologies « données de capteurs physiques » dans le cadre de Karstlink.
- valider et documenter l’ensemble des outils ainsi assemblés, ainsi qu’une bibliothèque d’exemples.

### Création de 2 applications web – CMS et Framework ###

- Encadrant: [Florian Fecard](mailto:fecard@protonmail.com)
- Sujet ``ingénierie'' pour 2-3 étudiants.

#### Méthodes, langages ou technologies envisagés ####
{:.no_toc}

Réflexion / Création de contenu numérique / Quizz en ligne avec visualisation des données.

#### Sujet ####
{:.no_toc}

Pour ce projet, votre but sera de réaliser deux applications Web. Dans un premier temps, un site web réalisé grâce à un Framework choisi, pour un escape-game. Enfin un site web vitrine sera réalisé grâce à un CMS pour une entreprise travaillant dans la cybersécurité.

Ces 2 projets permettront aux étudiants d’obtenir des connaissances sur 2 types d’applications différentes : via Framework ou CMS.

##### Partie 1 : Site web escape-game #####
{:.no_toc}
	
À la suite de la création d’un escape-game basé sur la cybersécurité, un quizz permettra de déterminer le niveau moyen de sensibilité à la cybersécurité de ses participants. Lors de ce projet, il faudra créer une application web contenant ce quizz permettant au client final de visualiser le niveau de sensibilité moyen de ses employés, vis-à-vis de la cybersécurité. 


Le rôle du / des étudiants : 

- Comparer les Framework existants et choisir le plus adapté ;
- Créer l’application web, qui aura les propriétés suivantes : 
	- Collecte des données du quizz 
	- Classification des données en fonction des clients 
	- Exportation et mise en forme des données pour les clients (sous forme de graphique)

##### Partie 2 : Site web vitrine pour une entreprise #####
{:.no_toc}

Un site vitrine est indispensable pour une entreprise, il permet d’obtenir des demandes de devis, de contact, des appels téléphoniques… Votre rôle sera de créer un site web vitrine via CMS, pour une entreprise travaillant dans la cybersécurité (hacking éthique).

Le rôle du/des étudiants : 

- Comparer les CMS existants et choisir le plus adapté ;
- Créer le site vitrine avec le CMS choisi ;
-  Rédaction du contenu numérique basé sur les documents fournis par l’entreprise.

### Création d’une interface frontend - bot de trading customisable  ###

- Encadrant: [Florian Fecard](mailto:fecard@protonmail.com)
- Sujet ``ingénierie'' pour 2-3 étudiants.

#### Méthodes, langages ou technologies envisagés ####
{:.no_toc}

Algorithmique / Vue.js / MySQL.

#### Sujet ####
{:.no_toc}

Les crypto-monnaies apportent une technologie indéniablement novatrice et prometteuse. Elles entraînent également beaucoup de spéculations, le monde du trading s'est donc invité dans ce domaine. De nombreuses entreprises proposent désormais aux particuliers d'investir dans ce marché de manière automatique, via des "bots de trading". Les particuliers peuvent ainsi choisir de suivre les bots de l’entreprise ou créer les leurs. Ces bots sont cependant onéreux.

Le projet consiste à développer la partie frontend d’un bot abordable, permettant ainsi aux particuliers de créer leur propre bot de trading via une interface intuitive. Pour ce TER, les étudiants créeront un dashboard dynamique en Vue.js, permettant à un utilisateur de faire son propre bot, basé sur des indicateurs mathématiques choisis par ce dernier.

##### Les missions du / des étudiants :#####
{:.no_toc}

- Créer un dashboard contenant un menu déroulant, permettant d’ajouter des blocs. Chacun de ces blocs représentera :
	- Un ordre financier (achat ou vente)
	-  Un opérateur mathématique (=, >, <…)
	- Un indicateur mathématique boursier (RSI, SMAs…)
	- Une crypto-monnaie ou monnaie fiduciaire (Dollar, Bitcoin…)
	- Un type de montant (minimum, maximum, pourcentage)
	- Une entrée utilisateur libre représentant un montant (int)
- Les blocs sélectionnés doivent être mobiles et être mis en relation les uns avec les autres afin de créer une liste d’ordres, suivant les conditions choisies. Voici un exemple : 

		IF BITCOIN RSI > 30 THEN BUY 200 DOLLARS

- La sécurité de l’application étant une priorité, diverses actions seront effectuées en ce sens. Par exemple, les ordres créés devront suivre une logique de positionnement de blocs bien précise. Une whitelist des blocs autorisés sera également à définir pour protéger l’application d’injections potentielles ;
- La liste d’ordres créée devra être ajoutée à la base de données, pour l’utilisateur concerné et selon un format choisi ;
- (Optionnel, si le temps le permet) Le bot de trading fonctionne actuellement avec une application tierce (TradingView). Il conviendra de modifier le bot afin de se séparer de ce tiers :
	- Le bot récupère ses données via ce tiers (ex. valeur du Bitcoin à l’instant T…), celui-ci sera modifié pour récupérer les données directement depuis Binance; 
	- Le bot de trading est partiellement développé dans le langage de TradingView (Pine script), celui-ci sera recréé en Python pour être uniquement hébergé sur le serveur hôte.

### Refonte de l’architecture d’un site Web ###

- Encadrant: [Florian Fecard](mailto:fecard@protonmail.com)
- Sujet ``ingénierie'' pour 2-3 étudiants.

#### Méthodes, langages ou technologies envisagés ####
{:.no_toc}

D’un site 100% backend à une segmentation sous forme « Backend <-> API <-> FrontEnd »

Technologies : 

- Backend: Python (Django)
- Frontend: Javascript (Vue.js) 
- Autres: Bootstrap – REST API – JSON 

#### Sujet ####
{:.no_toc}

Vous interviendrez sur une application Web en construction, traitant du trading automatique sur les crypto-monnaies.


Actuellement, cette application dispose d’un backend Django renvoyant les données obtenues (sous format JSON) vers la page HTML. Ces données sont ensuite affichées grâce à du code JavaScript. 
Le rôle des étudiants sera de séparer distinctement le backend du frontend, en utilisant une API REST pour communiquer entre ces derniers.


##### Les missions du / des étudiants : #####
{:.no_toc}

- Créer une première application de type « Hello World ! » qui utilisera les technologies Django (et son API REST) et Vue.js pour se familiariser avec le fonctionnement de ces dernières ;
- Séparer l’application existante de la manière décrite ci-dessus ;
- Récupérer les données envoyées par Django dans le frontend nouvellement déployé et les afficher sous forme de graphique, en utilisant la librairie Vue-Chartjs ;
- (Optionnel si le temps le permet) Un script de non-régression sera à créer pour s’assurer que toutes les fonctionnalités soient toujours fonctionnelles après une mise-à-jour.

### Développement d'un gestionnaire de cycles de vie de services pour l'IoT ###

- Encadrant: [Rey Gaëtan](mailto:Gaetan.Rey@univ-cotedazur.fr)
- Sujet ``ingénierie'' pour 1-2 étudiants.

#### Méthodes, langages ou technologies envisagés ####
{:.no_toc}

Le projet pourrait être développé en .NetCore6 pour des questions de portabilité. Les communications utiliseront principalement les protocoles web.

#### Sujet ####
{:.no_toc}

Aujourd’hui avec le développement important de l’IoT, de plus en plus de protocoles de communication différents sont utilisés. Pour pallier ce problème de la grande variété des protocoles de communication, une des tendances actuelles est de ne plus concevoir des applications qui pilotent directement les dispositifs mais de passer par des Gateway qui fournissent un protocole de plus haut-niveau d’abstraction. Cependant, malgré cette réduction des protocoles il en existe encore de nombreux à prendre en compte.

Plus important encore que leur nombre, ces protocoles, même ceux de haut niveau, n’offrent pas obligatoirement l’ensemble de fonctionnalités attendues pour gérer convenablement les dispositifs de l’IoT. En effet, si l’adressage et le liaison sont assurés par tous, la présentation d’un véritable contrat de description de services est plus rare et peu de protocoles offrent des fonctionnalités de gestion de la découverte de services, de la gestion de la disparition … La gestion du cycle de vie des services et dispositifs est le parent pauvre des protocole de l’IoT.

Le projet OCTOPUS, financé par la BPI et en partenariat avec le CEA, EDF R\&D, Scalian et d’autres entreprises, consiste en la mise en œuvre d’une plateforme qui assure la continuité des services des travailleurs mobiles en fonction du contexte. Ce projet est la concrétisation du plusieurs années de recherche effectuée au sein du groupe de recherche en intelligence ambiante de l’équipe SPARKS du laboratoire I3S. Plusieurs briques logicielles composent cette plateforme OCTOPUS, le but serait ici de développer un gestionnaire de cycle de vie.

Dans le cadre de ce projet, le travail attendu est le suivant :

- Etudier et comprendre l'intérêt des outils proposés dans le projet pour adresser les problématiques de la continuité de service et en particulier architecture de la plateforme.
- Développer l’outil de gestion de cycle de vie des services. Celui-ci devra être en mesure de gérer les protocoles suivants : UPnP, OpenHab et Swagger. Il devra assurer la découverte et la disparition des services au travers de ces protocoles, ainsi que la transmission d'un contrat (description du service) au format WoT-TD.
- Etendre le projet (si celui-ci avance bien) avec d'autres protocoles (comme BLE par exemple ou d'autres proposés par les étudiants).
- Travailler avec les encadreurs sur un/des scénario(s) mettant en évidence les contributions et l'intérêt des outils proposés et déjà disponibles.
- Mettre en œuvre ce scénario à l'aide de notre plateforme

### Développement d'un générateur de flow Node-Red pour l'IoT ###

- Encadrant: [Rey Gaëtan](mailto:Gaetan.Rey@univ-cotedazur.fr)
- Sujet ``ingénierie'' pour 1-2 étudiants.

#### Méthodes, langages ou technologies envisagés ####
{:.no_toc}

le projet pourrait être développé en .NetCore6 pour des questions de portabilité. Les communications utiliseront principalement les protocoles web.

#### Sujet ####
{:.no_toc}

Le projet OCTOPUS financé par la BPI et en partenariat avec le CEA, EDF R\&D, Scalian et d’autres entreprises consiste en la mise en œuvre d’une plateforme qui assure la continuité des services des travailleurs mobiles en fonction du contexte, c’est-à-dire en fonction de leur environnement physique et social, de leur activités et des dispositifs présents. Ce projet est la concrétisation du plusieurs années de recherche effectuée au sein du groupe de recherche en intelligence ambiante de l’équipe SPARKS du laboratoire I3S.

La plateforme ainsi développée assure 2 niveaux d’adaptation dynamique de l’application : un niveau d’adaptation opportuniste qui va construire tout ce qui est possible de construire dans la situation courante pour offrir un maximum de possibilités à l’utilisateur et un niveau de pilotage contextuel qui va sélectionner les éléments à mettre en œuvre pour que ceux-ci soient pertinents en fonction de la situation courante et des attentes utilisateurs.

Plusieurs briques logicielles composent cette plateforme OCTOPUS. Le but du projet, qui est proposer ici, est de substituer le conteneur applicatif développé par notre groupe de recherche par un conteneur open-source très utilisé dans le monde de l’IoT : Node-red. Pour cela une projection de notre modèle théorique (LCA) a déjà été faite et une première implémentation partielle a également été réalisé.

Le but de ce projet serait alors :

- Etudier et comprendre l'intérêt des outils proposés dans le projet pour adresser les problématiques de la continuité de service et en particulier architecture de la plateforme.
- Développer un générateur de proxy permettant de transformer un service décrit à l'aide d'un contrat WoT-TD en un flow/ensemble de flow Node-Red.
- Mettre en place une solution permettant de déployer des graphes de services (services et liens de communication entre les services) sur Node-Red en s'appuyant (ou non) sur la première projection effectuée.
- Travailler avec les encadreurs sur un/des scénario(s) mettant en évidence les contributions et l'intérêt des outils proposés et déjà disponibles.
- Mettre en œuvre ce scénario à l'aide de notre plateforme.

### Neuromorphic hardware comparison: Human Brain Project SpiNNaker vs Intel Loihi ###

- Encadrant: [Jean Martinet](mailto:jean.martinet@univ-cotedazur.fr)
- Sujet ``ingénierie'' pour 2 étudiants.

#### Méthodes, langages ou technologies envisagés ####
{:.no_toc}

Programming skills in Python, interest in machine learning, bio-inspiration and neuroscience.

Extra references : 

- SpiNNaker: A Spiking Neural Network Architecture. Steve Furber, Petrut Antoniu Bogdan. March 2020. DOI: 10.1561/9781680836523
- Loihi: A Neuromorphic Manycore Processor with On-Chip Learning. Mike Davies et al. January 2018. DOI: 10.1109/MM.2018.112130359
- Performance Comparison of the Digital Neuromorphic Hardware SpiNNaker and the Neural Network Simulation Software NEST for a Full-Scale Cortical Microcircuit Model. Sacha J. van Albada et al. Front. Neurosci., 23 May 2018. https://doi.org/10.3389/fnins.2018.00291
- URL: [https://towardsdatascience.com/spiking-neural-networks-the-next-generation-of-machine-learning-84e167f4eb2b](https://towardsdatascience.com/spiking-neural-networks-the-next-generation-of-machine-learning-84e167f4eb2b)
- URL: [https://towardsdatascience.com/neuromorphic-hardware-trying-to-put-brain-into-chips-222132f7e4de](https://towardsdatascience.com/neuromorphic-hardware-trying-to-put-brain-into-chips-222132f7e4de)

#### Sujet ####
{:.no_toc}

Spiking Neural Networks (SNN) represent a special class of artificial neural networks, where neurons communicate by sequences of spikes \[Ponulak, 2011\]. Contrary to deep convolutional networks, spiking neurons do not fire at each propagation cycle, but rather fire only when their activation level (or membrane potential, an intrinsic quality of the neuron related to its membrane electrical charge) reaches a specific threshold value. Therefore, the network is asynchronous and allegedly likely to handle well temporal data such as video. When a neuron fires, it generates a non-binary signal that travels to other neurons, which in turn increases their potentials. The activation level either increases with incoming spikes, or decays over time. Regarding inference, SNN does not rely on stochastic gradient descent and backpropagation. Instead, neurons are connected through synapses, that implement learning mechanisms inspired from biology for updating synaptic weights (strength of connections) or delays (propagation time for an action potential).

Simulating such models is time and resource consuming. However, the use of dedicated hardware   enable fast runs. On the one hand in EU, the Human Brain Project (HBP) is building a research infrastructure to help advance neuroscience, medicine, and computing. On the other hand in the USA, Intel is building a neuromorphic research test chip that uses an asynchronous SNN to implement adaptive self-modifying event-driven fine-grained parallel computations used to implement learning and inference with high efficiency.

The objective of this project is to carry out a theoretical and experimental survey to point out strength and weaknesses of both solutions.

The candidate will have access to the hardware (an access to local SpiNN-3 and SpiNN-5 boards and a remote access to Loihi SDK) throughout the tutorship. An evaluation of the power consumption of the SpiNN-3 board would be a plus.

At the end of the project, the candidate might be offered an internship. This project takes place with the EU programme APROVIS3D ([http://www.chistera.eu/projects/aprovis3d](http://www.chistera.eu/projects/aprovis3d)) that started in April 2020, and that targets embedded bio-inspired machine learning and computer vision, with an application to autonomous drone navigation.

### Stereo Matching for Event-Based Cameras Demonstration ###

- Encadrant: [Jean Martinet](mailto:jean.martinet@univ-cotedazur.fr)
- Sujet ``ingénierie'' pour 2 étudiants.

#### Méthodes, langages ou technologies envisagés ####
{:.no_toc}

Programming skills in Python, strong interest for research in vision, development, proficiency in Linux.

Extra references : 

- \[Steffen et al., 2019\] L. Steffen, D. Reichard, J. Weinland, J. Kaiser, A. Roennau, and R. Dillmann, 'Neuromorphic Stereo Vision: A Survey of Bio-Inspired Sensors and Algorithms', Front. Neurorobot., vol. 13, 2019, doi: 10.3389/fnbot.2019.00028.
- \[Dikov et al., 2017\] G. Dikov, M. Firouzi, F. Röhrbein, J. Conradt, and C. Richter, 'Spiking Cooperative Stereo-Matching at 2 ms Latency with Neuromorphic Hardware', 2017, doi: 10.1007/978-3-319-63537-8\_11.
- URL: [https://www.prophesee.ai](https://www.prophesee.ai)

#### Sujet ####
{:.no_toc}

Event-based cameras are bio-inspired sensors that work in radically different ways from traditional cameras. Instead of capturing images at a fixed rate, they measure changes in brightness per pixel asynchronously. This results in a flow of events, which encode the instant, location and sign of brightness changes. These cameras have exceptional properties compared to traditional cameras: very high dynamic range (140 dB against 60 dB), high temporal resolution (order of 10-6s), low energy consumption and absence of motion. Therefore, these sensors bring a great potential for computer vision and robotics in challenging scenarios. However, new computing methods are needed to deal with the unconventional output of these sensors in order to unlock their potential.

In this project, we wish to develop a demonstrator for an existing event-based stereo matching system. We will need to adapt and connect existing pieces of software written in Python, namely :

- a stereo matching code taking static data of two event flow from left and right cameras stored on a drive, and
- a pair of Prophesee event cameras that generate a live event flow.


Optionally (if there is time), we will carry out an experimental evaluation of the demonstrator.

The project will extend previous internship work done in the lab in 2020 and 2021.  At the end of the project, the candidate might be offered an internship. This project takes place within the EU programme APROVIS3D ([http://www.chistera.eu/projects/aprovis3d](http://www.chistera.eu/projects/aprovis3d)) that started in April 2020, and that targets embedded bio-inspired machine learning and computer vision, with an application to autonomous drone navigation.

### Synaptic delays for temporal pattern recognition ###

- Encadrant: [Jean Martinet](mailto:jean.martinet@univ-cotedazur.fr)
- Sujet ``ingénierie'' pour 2-4 étudiants.

#### Méthodes, langages ou technologies envisagés ####
{:.no_toc}

Programming skills in Python, strong interest for research in applied machine learning, bio-inspiration and neurosciences.

Extra references : 

- \[Reichardt, 1987\] Werner Reichardt : Evaluation of optical motion information by movement detectors. Journal of Comparative Physiology A, 1987. DOI:10.1007/BF00603660.
- \[Ponulak, 2011\] Filip Ponulak, Andrzej Kasinski. Introduction to spiking neural networks: Information processing, learning and applications. Acta Neurobiol Exp (Wars). 2011;71(4):409-33.
- \[Paredes, 2019\] Paredes-Vallés, F., Scheper, K. Y. W., \& De Croon, G. C. H. E. (2019). Unsupervised learning of a hierarchical spiking neural network for optical flow estimation: From events to global motion perception. IEEE transactions on pattern analysis and machine intelligence.
- \[Oudjail, 2019\] Veïs Oudjail, Jean Martinet. Bio-inspired event-based motion analysis with spiking neural networks. International Conference on Computer Vision Theory and Applications (VISAPP'19), Feb 25-27 2019, Prague, Czech Republic ([https://hal.archives-ouvertes.fr/hal-01940917v1](https://hal.archives-ouvertes.fr/hal-01940917v1))

#### Sujet ####
{:.no_toc}

Spiking Neural Networks (SNN) represent a special class of artificial neural networks, where neurons communicate by sequences of spikes \[Ponulak, 2011\]. Contrary to deep convolutional networks, spiking neurons do not fire at each propagation cycle, but rather fire only when their activation level (or membrane potential, an intrinsic quality of the neuron related to its membrane electrical charge) reaches a specific threshold value. Therefore, the network is asynchronous and allegedly likely to handle well temporal data such as video. When a neuron fires, it generates a non-binary signal that travels to other neurons, which in turn increases their potentials. The activation level either increases with incoming spikes, or decays over time. Regarding inference, SNN does not rely on stochastic gradient descent and backpropagation. Instead, neurons are connected through synapses, that implement learning mechanisms inspired from biology for updating synaptic weights (strength of connections) or delays (propagation time for an action potential).

The development of event-based cameras, inspired by the retina, fosters the application of SNN to computer vision. Instead of measuring the intensity of every pixel in a fixed time interval like standard cameras, they report events of significant pixel intensity changes. Every such event is represented by its position, sign of change, and timestamp -- accurate to the microsecond. Due to their asynchronous course of operation, considering the precise occurrence of spikes, Spiking Neural Networks are a natural match for event-based cameras. State-of-the-art approaches in machine learning provide excellent results with standard cameras, however, asynchronous event sequences require special handling, and spiking networks can take advantage of this asynchrony.

In this project, we wish to extend a previous project in which we designed a specific elementary SNN and tuned synaptic delays to recognise prototypical temporal patterns from event cameras, inspired by Reichardt detectors. The objective is to apply this model to real world data in order to recognize features such as motion direction and speed. The implementation will use either Human Brain Project SpiNNaker.

At the end of the project, the candidate might be offered an internship. This project takes place within the EU programme APROVIS3D ([http://www.chistera.eu/projects/aprovis3d](http://www.chistera.eu/projects/aprovis3d)) that started in April 2020, and that targets embedded bio-inspired machine learning and computer vision, with an application to autonomous drone navigation.

### Ontologie pour décrire les types de publications scientifiques  ###

- Encadrant: [Marco Winckler](mailto:Marco.Winckler@univ-cotedazur.fr)
- Sujet "recherche appliquée" pour 2-4 étudiants,

#### Méthodes, langages ou technologies envisagés ####
{:.no_toc}

RDF, SPARQL, OWL, Protege.

#### Sujet ####
{:.no_toc}

Il existe dans la littérature plusieurs efforts pour décrire le domaine des publications, notamment à travers des ontologies : SPAR (Semantic Publishing and Referencing) (Peroni \& Shotton, 2018), DCTerms (Dublin Core Metadata Terms)  et BiBO (Bibliographic Ontology) . Bien que ces ontologies permettent de décrire les publications scientifiques à travers des aspects divers, elles ne sont pas toujours adoptées de la même manière dans les graphes de connaissances représentant les métadonnées des articles scientifiques. Par exemple, le graphe de connaissance HAL  combine trois ontologies (FaBiO , BiBO et COAR ) pour décrire les différents types de documents selon une granularité plus fine que celle trouvée dans le graphe de connaissances « Microsoft Academic » , qui s'appuie seulement sur l'ontologie FaBiO. De ce fait, ce projet a pour objectif de proposer une ontologie et un système de proxy qui permette de normaliser l'accès aux données des différents graphes de connaissances. Particulièrement, les étudiants devront réaliser les tâches suivantes :

- Extraire des ontologies utilisées dans des graphes de connaissance (ex : HAL, MAKG)
- Identifier les aspects communs et différents entre elles
- Créer une nouvelle ontologie commune (de référence) qui permettra de décrire les concepts bibliographiques ; cette partie sera réalisée en collaboration avec des chercheurs du domaine
- Créer des scripts qui serviront de proxy pour consulter de façon automatique les différents graphes de connaissances en utilisant l'ontologie de référence
- Rechercher et identifier des solutions existantes dans la littérature
Ce travail s'effectuera dans l'équipe WIMMICS commune à I3S/INRIA, et vient en complément d'une thèse en cours sur la visualisation de données musicale multidimensionnelle (audio + graphique).

### Outil pour exploration d'une base de connaissance musicale ###

- Encadrant: [Michel Buffa](mailto:michel.buffa@univ-cotedazur.fr)
- Sujet "recherche appliquée" pour 2-4 étudiants,

#### Méthodes, langages ou technologies envisagés ####
{:.no_toc}

JavaScript/TypeScript/HTML/CSS pour front-end et NodeJS / MongoDB ou autre pour back end, sans doute un peu de script shell ou perl ou python, APIs WebAudio, librairie D3JS.

#### Sujet ####
{:.no_toc}

Nous disposons d'une base de connaissances musicale contenant des informations sur 2 millions de chansons commerciales (typiquement pop/rock/rap/funk etc. avec les artistes / albums et chansons les plus connues). Toutes ces données sont accessibles à travers une API REST classique. Nous développons dans le cadre de nos travaux de recherche des outils d'exploration visuels et audio pour par exemple, étudier l'oeuvre d'un artiste ou d'un groupe de musique : frise temporelle de sortie des albums, collaborations, influences, etc. 

Nous avons commencé à développer tout cela en ajoutant une dimension "audio" :  quand on visualise la discographie de Queen, on pourra, en interagissant sur la vue graphique (frise temporelle avec les albums et les chansons) écouter un résumé audio de la discographie complète de Queen, d'un album, ou d'une chanson. Nous désirons approfondir et compléter les options existantes en ajoutant par exemple une vue "détail" d'une chanson, (en utilisant des services distants permettant d'effectuer une analyse audio de la chanson pour calculer de nouvelle visualisations telles que spectrogramme, courbe de variation du volume etc.), mais aussi un éditeur interactif permettant de choisir un "meilleur extrait" de la chanson que celui proposé par les outils de calcul de résumé automatique. Un peu comme quand on poste une vidéo sur YouTube, une image représentant la vidéo est proposée, mais on peut aussi en choisir une manuellement. Autre besoin : avoir un lecteur audio permettant de lire un fichier audio à différentes vitesses, en voyant dans son interface les différents "segments" (ex: extraits de 2s des chansons) qui composent le fichier audio, etc.

Ce travail s'effectuera dans l'équipe WIMMICS commune à I3S/INRIA, et vient en complément d'une thèse en cours sur la visualisation de données musicale multidimensionnelle (audio + graphique).

### Cross compilation C++/Rust/Web assembly, écriture d'un logiciel hôte pour des plugins WebAudio écrits en WebAssembly ###

- Encadrant: [Michel Buffa](mailto:michel.buffa@univ-cotedazur.fr)
- Sujet "recherche appliquée" pour 2-4 étudiants,

#### Méthodes, langages ou technologies envisagés ####
{:.no_toc}

C++/JavaScript, cross compilateurs LLVM ou emscripten

#### Sujet ####
{:.no_toc}

Avec un groupe de chercheurs et d'industriels spécialistes de la musique assistée par ordinateur (MAO) nous avons développé un standard pour des plugins audio réutilisables sous forme de Web Components (composants web complets réutilisables et inter-opérables sur le Web). Ces plugins sont des effets audio (ex: autotune, distorsion, echo/delay, réverbération, égaliseurs, etc.) ou des instruments (synthétiseurs, samplers, générateurs de musique automatique etc.).

On peut écrire ces plugins avec divers langages (JavaScript, TypeScript, C++, RUST, FAUST, CSOUND, etc.), mais les résultats les plus performants sont ceux qui produisent un résultat cross compilé en WebAssembly (un bytecode tournant dans les browsers, c'est le 4ème langage compris par les browsers web après HTML/CSS et JS). Dans ce cas un plugin = une interface graphique en HTML/CSS/JS et le "coeur" en WebAssembly. 

Pour ces derniers types de plugins, le top pour rester dans ce qu'on appelle le "thread audio", sans passer par le "main thread" (qui gère la GUI), est d'avoir aussi un logiciel hôte en WebAssembly. 
Le projet consiste donc à écrire un logiciel hôte en C++ ou RUST cross compilé en WebAssembly (avec une GUI en HTML/CSS/JS), capable de charger des plugins eux aussi écrits en WebAssembly. Nous avons déjà un certain nombre de plugins de ce type. Le projet est bien de se focaliser sur le logiciel hôte.
Voici un exemple de logiciel hôte : 

- [https://mainline.i3s.unice.fr/wam2/packages/\_/](https://mainline.i3s.unice.fr/wam2/packages/_/) (cliquer sur un plugin, puis sur le bouton "load plugin")
![image_buffa_cross]({% include link-asset asset="TER-M1-2022_Michel_Buffa_cross_compilation.png" %})

- L'hôte ci-dessus est écrit en pur JavaScript, mais on trouve des hôtes dont le coeur est écrit en C++, comme par exemple le logiciel commercial ampedstudio.com

L'objectif du TER est donc d'écrire un petit logiciel hôte avec un noyaux en C++ ou en RUST compilé en Web Assembly via une chaine de cross compilation (emscripten par exemple), et une GUI "wrapper" autour  écrite en HTML/CSS/JS.

Ce travail s'effectuera dans l'équipe WIMMICS commune à I3S/INRIA.

### Ecriture d'une application "multi-effets audio à base de plugins de type WebAudio Modules 2.0" ###

- Encadrant: [Michel Buffa](mailto:michel.buffa@univ-cotedazur.fr)
- Sujet "recherche appliquée" pour 2-4 étudiants,

#### Méthodes, langages ou technologies envisagés ####
{:.no_toc}

JavaScript, WebAudio, WebComponents, peut-être une framework web type React, SDK du standard de plugins WebAudio que nous avons développé (WebAudio Modules 2.0 ou "WAM2".

#### Sujet ####
{:.no_toc}

Avec un groupe de chercheurs et d'industriels spécialistes de la musique assistée par ordinateur (MAO) nous avons développé un standard pour des plugins audio réutilisables sous forme de Web Components (composants web complets réutilisables et inter-opérables sur le Web). Ces plugins sont des effets audio (ex: autotune, distorsion, echo/delay, réverbération, égaliseurs, etc.) ou des instruments (synthétiseurs, samplers, générateurs de musique automatique etc.). Souvent, on est amené à "assembler" plusieurs effets, à les chaîner ou à les relier dans un graphe. Le son source (par exemple un micro) sera donc transformé à travers plusieurs effets (ex: on ajoute des aigus, puis on ajoute un effet de réverbération, puis un peu d'echo etc.).

Le but de ce TER est d'écrire une application "hôte" permettant de charger plusieurs plugins d'effets et de les organiser en chaîne de traitement (avec drag n drop, ajout/suppression et sauvegarde de configurations/presets). L'application en question sera elle-même un plugin.

Ici une photo d'un prototype existant :

![]({% include link-asset asset="TER-M1-2022_Michel_Buffa_multi-effets.png" %})
   
Chaque pédale d'effet est un plugin, sur la droite on a le "browser de plugins", quand on clique sur une imagette à droitre elle apparait dans la chaine de gauche, et là on peut utiliser les boutons, etc. on peut changer l'ordre (ce qui affecte le son). Ce prototype / preuve de concept existe (et je peux vous en faire la démonstration), mais il faudrait le re-écrire et le compléter car il manque encore beaucoup de choses (notamment la sauvegarde/restauration, la possibilité de gérer plusieurs URLs de serveurs de plugins (un plugin = un URL), etc.

Vous pouvez regarder sur YouTube des démos d'applications de ce genre que nous avons développées par le passé (ici par ex: [https://www.youtube.com/watch?v=pe8zg8O-BFs](https://www.youtube.com/watch?v=pe8zg8O-BFs))

Ce travail s'effectuera dans l'équipe WIMMICS commune à I3S/INRIA.

### Étude des compteurs matériels des performances ###

- Encadrant: [Sid Touati](mailto:sid.touati@inria.fr)
- INRIA-Sophia. Équipe KAIROS.
- Prérequis: avoir suivi le cours d’architecture des processeurs.

#### Sujet ####
{:.no_toc}

Afin d’aider un peu plus l’analyse et la compréhension des performances observées, les comp- teurs matériels de performances (registres spéciaux), si présents dans le CPU, peuvent être exploités. Ces compteurs enregistrent plein d’événements matériels relatifs aux performances qui sont provoqués par l’exécution de processus: nombre de cycles d’horloge, nombre d’accès mémoire, nombre d’accès au cache L1, nombre de défauts de cache, etc. La nature des événe- ments enregistrés par les compteurs matériels de performances dépend d’une architecture de CPU à une autre. La portabilité n’est donc pas assurée, mais les mesures sont extrêmement précises.

Notons deux façons pour utiliser les compteurs matériels de performances:

1. **Analyser les événements matériels d’un CPU qui exécute plusieurs programmes en concurrence.** Par exemple, l’outil Likwid installé sur vos machines de l’université récupère les valeurs des compteurs matériels par cœur (et non pas par processus). Il peut agréger les compteurs matériels de tous les cœurs. Cette façon d’utiliser les compteurs matériels de performances permet d’avoir une vue globale du fonctionnement et des per- formances d’un cœur ou d’un système entier qui exécute plusieurs processus en même temps.
2. **Analyser les événements matériels provoqués par un seul processus qui s’exécute sur une machine.** C’est la façon à utiliser pour analyser et éventuellement optimiser les performances d’un programme particulier qui s’exécute sur une architecture matérielle précise.

Là aussi, notons deux façons pour utiliser des compteurs matériels de performances pour un code donné:
 
1. Soit l’utilisateur est intéressé par l’analyse des performances d’un bout son programme (par exemple étudier les performances d’une boucle précise ou d’une fonction particulière). Dans ce cas, il faut détenir le code source pour l’instrumenter (le modifier). Le code modifié contiendrait des instructions utilisant des librairies d’accès aux compteurs matériels de performances. La librairie **LibPFM** ou **PAPI** permet par exemple à un programme d’accéder aux valeurs des compteurs matériels de performances.
2. Soit l’utilisateur est intéressé par l’analyse des performances d’un processus entier (pas uniquement un bout du programme). Dans ce cas de figure, l’utilisateur n’a pas besoin d’instrumenter le code source. Il peut utiliser des outils en ligne de commande comme **perf** pour évaluer les performances du code binaire.

Dans ce TER nous allons étudier en détails ces compteurs matériels de performances. L’étudiant devra se familiariser avec les différents aspects comme ceci:

1. Étudier les événements matériels pouvant être enregistrés sur votre machine de test.
2. Reprendre des codes de micro-benchmarks vus en TP et les analyser finement avec les compteurs matériels de performances.

### Comparaison des performances de codes de calculs scientifiques C++ versus Java ###

- Encadrant: [Sid Touati](mailto:sid.touati@inria.fr)
- INRIA-Sophia. Équipe KAIROS.
- Prérequis: Maîtrise des langages de programmation C++ et Java.


#### Sujet ####
{:.no_toc}

Ce sujet TER permet de débuter un premier travail d’analyse et d’optimisation des perfor- mances de codes C++ et java. La même problématique pour les langages impératifs classiques (C, fortran) est connue et largement abordée depuis plusieurs décennies en compilation et en calculs hautes performances. En revanche, le sujet est moins exploré pour les langages orientés objets compilés comme C++ ou interprétés comme Java. Or, il y a une tendance nette d’écriture d’applications hautes performances en C++ ou en Java, car ces langages ont des propriétés de composition et de maintenance plus intéressantes que le C ou le fortran.

Ce TER contient deux volets:
	
1. Écrire une librairie de codes de calculs matriciels en JAVA et en C++ (ces codes peuvent être récupérés sur le net), puis comparer les performances entre les deux langages.
2. Optimiser les performances des deux codes en utilisant les options de compilation du compilateur pour C++ et les options de Java.
3. Comparer les avantages et les inconvénients entre C++ et Java dans notre contexte.

### Métriques de variabilité : des calculs à la visualisation ###

- Encadrant: [Mireille Blay](mailto:Mireille.BLAY@univ-cotedazur.fr)

#### Méthode ####
{:.no_toc}

Analyse du sujet, conception d'une architecture élémentaire pour supporter le développement en mode itératif, mise en oeuvre séquentielle des différentes fonctionnalités.

#### Technologies ####
{:.no_toc}

Le choix de la technologie et du langage font partie du projet.
Cependant, les pré-requis sont : accès à la plateforme d'évaluation des métrics sur le web, ajout « facile » de nouveaux éléments (composant d'analyse et visualisation), sensibilisation à la complexité des calculs.  Un dépôt GitHub sera utilisé et si possible une intégration continue sera mise en place.`

#### Sujet ####
{:.no_toc}

La nécessité de produire des logiciels dans les délais et les budgets impartis, tout en pouvant les adapter à des contextes différents, conduit à mettre en place différents mécanismes pour maîtriser la variabilité des logiciels, notamment par des technologies de lignes de produits. Dans ce projet, nous nous intéresserons aux métriques qui permettent d'évaluer une ligne de produits (eg. nombre de features, cf. article ci-joint \[1\]) et à d'autres métriques pour mesurer par exemple la « couverture » des produits construits.

Dans ce projet, nous vous proposons donc de construire les premières briques d'un « SonarQube » pour lignes de produits logiciels. Il s'agit de comprendre le formalisme des feature models dont on peut trouver des implémentations en JS \[2\] ou en Java \[3\], d'implémenter les métriques choisies ensemble et de les visualiser. Puis de réitérer le processus sur différentes métriques. Le cadre d'application sera à minima l'évaluation d'une ligne dont les produits sont des workflows de machine learning.

1. S. El-Sharkawy, N. Yamagishi-Eichler, and K. Schmid, "Metrics for analyzing variability and its implementation in software product lines: A systematic literature review," Information and Software Technology, vol. 106. Elsevier, pp. 1–30, Feb. 01, 2019, doi: 10.1016/j.infsof.2018.08.015.
2. [https://github.com/ekuiter/feature-configurator](https://github.com/ekuiter/feature-configurator)
3. [https://github.com/FeatureIDE/FeatureIDE](https://github.com/FeatureIDE/FeatureIDE)

### Human motion capture using RGBD cameras  ###

- Encadrants: [Andrew Comport](mailto:Andrew.Comport@cnrs.fr) et Arnab Dey

#### Méthodes, langages ou technologies envisagés ####
{:.no_toc}

Python, C++, knowledge about camera calibration, and computer vision. Knowledge about deep learning methods can be a plus.

#### Sujet ####
{:.no_toc}

Human volumetric capture is a long-standing topic in computer vision. Although high-quality results can be achieved using sophisticated off-line systems, real-time human volumetric capture of complex scenarios, especially using lightweight setups. So our objective is to capture dense human motion using a network for RGBD(Azure kinect) cameras in real time. The objectives include RGBD camera calibration, multiple RGBD camera synchronization, dense capturing of the scene, point cloud generation, 3D registration, 3D mesh generation, dataset generation, and applying deep learning models for different applications. 

References: 

- [https://dl.acm.org/doi/abs/10.1145/3130800.3130801](https://dl.acm.org/doi/abs/10.1145/3130800.3130801)
- [https://openaccess.thecvf.com/content/CVPR2021/html/Yu_Function4D_Real-Time_Human_Volumetric_Capture_From_Very_Sparse_Consumer_RGBD_CVPR_2021_paper.html](https://openaccess.thecvf.com/content/CVPR2021/html/Yu_Function4D_Real-Time_Human_Volumetric_Capture_From_Very_Sparse_Consumer_RGBD_CVPR_2021_paper.html)