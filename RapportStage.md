<div style="font-size:var(--h1-fontsize);margin-bottom:1.5rem;font-weight:300;color:var(--header-color);">Remerciements</h1>

​	Avant toute chose, je tiens à remercier et à exprimer toute ma gratitude aux personnes suivantes, pour cette expérience enrichissante et professionnalisante. Qu'elles soient en France, aux États-Unis, ou ailleurs, elles ont permis que mon stage se déroule sans encombre et ont toutes été d'un grand recours.

​	**Monsieur Venkatesan Muthukumar**, mon tuteur, pour m'avoir permis d'effectuer mon stage au sein de l'Université du Nevada, Las Vegas *(UNLV)* et pour la confiance qu'il m'a accordé. Il m'a donné plusieurs missions qui m'ont fait découvrir de nouvelles technologies, et amélioré mes compétences techniques. Son équilibre entre liberté et supervision m'a laissé m'épanouir dans mon travail, tout en ayant quelqu'un à qui parler en cas de problème. Il m'a aussi permis de donner des cours au sein de l'UNLV.

​	**Madame Jennifer Reff**, assistante administrative du Electrical and Computer Engineering Department, pour m'avoir assisté dans les démarches auprès de l'United States Social Security Administration *(SSA)* afin de pouvoir travailler à l'UNLV en parallèle de mon stage.

​	**Monsieur Jaekeun Cho**, coordinateur du programme d'échange, pour avoir pris en charge mon dossier et pour m'avoir recommandé auprès de mon tuteur à la vue de mes anciens projets en lien avec le rythme cardiaque. 

​	**Monsieur Jason Lawrence**, conseiller aux étudiants internationaux, pour m'avoir guidé lors de mon arrivée à l'UNLV.

​	**Monsieur Patrick Albers**, professeur au sein de l'ESEO, pour m'avoir guidé et suivi pendant mon stage. 

​	**Messieurs Charles Cerisier, Yann Le Gall, Alex Manceau**, étudiants ESEO, avec qui je suis parti aux États-Unis et avec qui j'ai découvert une partie de la côte ouest de ce pays, rendant cette aventure aussi intéressante professionnellement que culturellement.

​	Je conclus ces remerciements en remerciant l'**ESEO**, pour m'avoir fourni une méthode d'apprentissage et une rigueur indispensable à la réalisation de ce stage technique.

<div style="page-break-after: always;"></div> 
<div style="font-size:var(--h1-fontsize);margin-top:2rem;margin-bottom:1rem;font-weight:300;color:var(--header-color);">Introduction</h1> 
</div>

​	Dans le cadre de ma formation d'ingénieur ESEO, j'ai eu l'occasion de réaliser un stage technique après ma première année du cycle ingénieur. Il est extrêmement important puisqu'il permet de découvrir le monde professionnel et de mettre ses compétences en action. 

​	Au terme de mes études, je souhaite travailler à l'étranger, au Canada ou aux États-Unis. L'ESEO a des partenariats avec des universités dans ces deux pays : l'UNLV et l'Université de Sherbrooke. Cependant, Sherbrooke est dans la partie francophone du Canada. J'ai donc décidé de faire mon stage à l'UNLV afin de perfectionner mon anglais.

​	M. Muthukumar a décidé de me prendre en stage afin de travailler sur une nouvelle méthode de diagnostic des Traumatismes Cranio-Cérébraux *(TCC)*. Le projet demandait majoritairement des compétences en informatique et abordait des technologies que je n'avais jamais utilisées auparavant : BLE, MQTT, Micro:bit... C'est ce qui m'a séduit. De plus, mettre mes compétences au service d'une cause médicale a fini de me convaincre.

​	Beaucoup de personnes souffrent de séquelles cognitives liées à un TCC sans le savoir. Elles sont la source de ce que l'on appelle plus communément le **handicap invisible**. Elles se manifestent différemment chez chaque patient et sont souvent une association de différents troubles comme des troubles de l'attention, de la concentration, une difficulté à marcher, etc. Ces troubles ne sont pas continuels et apparaissent occasionnellement. C'est là le plus gros problème : ils sont très difficiles à détecter. **Les patients peuvent n'avoir aucun symptômes pendant les consultations, mais être quand même atteints de séquelles**. 

​	Mon stage consiste donc à créer un dispositif que les patients pourraient porter à domicile pour collecter continuellement des données accélérométriques, gyrométriques et cardiaques. Ainsi, ce facteur aléatoire lors des consultations est supprimé. Le patient n'aura plus qu'à donner l'heure à laquelle il a ressenti les symptômes, et le médecin pourra extraire les données récoltées à ce moment. De plus, il devra aussi être possible au médecin de voir en temps réel les données accélérométriques et gyrométriques.

​	La programmation s'est faite en C++, en Python et en Javascript. J'ai travaillé sur des systèmes Linux et des architectures ARM, et j'ai envoyé des comptes rendus au minimum deux fois par semaine à mon tuteur. De plus, nous faisions des réunions hebdomadaires.

​	Le but de ce rapport de stage est de présenter l'UNLV et le contexte de mon projet dans un premier temps, puis d'exposer le résultat de mon travail pendant ces trois mois. Enfin, je ferai le bilan des compétences acquises pendant mon stage.

<div style="page-break-after: always;"></div> 
<div style="font-size:var(--h1-fontsize);margin-top:2rem;margin-bottom:1rem;font-weight:300;color:var(--header-color);">Fiche de synthèse du stage</h1> 
</div>

**Sujet** : Développement d'une nouvelle façon de détecter des séquelles des Traumatismes Cranio-Cérébraux

**Entreprise** : Université du Nevada, Las Vegas (UNLV)

**Dates de stage** : Débuté le 27 Aout 2018, terminé le 30 Novembre 2018

**Principales personnes avec qui j'ai travaillé** : Monsieur Venkatesan Muthukumar, mon tuteur

**Planning résumé** : 

- Prise en main du matériel (Micro:bit, Raspberry Pi, Arduino, AD8232, capteur Polar)
- Développement d'un programme C++ d'acquisition d'informations accélérométriques et gyroscopiques sur un Micro:bit en utilisant le MQTT-SN via BLE
- Modification du programme d'acquisition d'informations accélérométriques et gyroscopiques sur un Micro:bit en utilisant le BLE sans MQTT-SN
- Optimisation bas niveau du programme afin de pouvoir transmettre plus d'informations via BLE
- Création d'une  base de données MySQL pour stocker les données acquises
- Développement en Python d'un système d'envoi et de stockage d'informations vers un serveur MQTT et sur une base de données MySQL
- Modification d'un ancien programme Arduino (C) d'acquisition du signal cardiaque (patient immobile) pour l'adapter au capteur AD8232
- Modification d'un GUI Python afin d'afficher le signal cardiaque
- Création d'un programme Python d'analyse du signal cardiaque pour en extraire les pics P, Q, R, S et T, puis les afficher
- Ajout d'une fonctionnalité d'export des pics vers un fichier CSV
- Développement d'un programme Python d'acquisition du nombre de Battements Par Minute (BPM)  en utilisant un capteur Polar
- Développement d'un GUI Javascript / HTML / CSS afin d'afficher les informations accélérométriques, gyroscopiques et cardiaque (capteur Polar) récupérées sur le serveur MQTT
- Écriture d'un document expliquant comment utiliser mes programmes 

**Contraintes et difficultés rencontrées** : Le traitement des informations en temps réel à été une difficulté pour le développement des programmes. Le fonctionnement mission par mission a parfois été compliqué. En effet, au début de mon stage, mon tuteur me donnait une tâche à la fois, et une réunion était nécessaire pour avoir une nouvelle tâche. Cela a engendré une perte de temps au début du stage.

**Résultats** : Le système d'acquisition, de transmission et de stockage d'informations accélérométriques, gyroscopiques et cardiaques (BPM) a été testé pendant 8h consécutives sans problème. Le système d'acquisition du rythme cardiaque sur un patient immobile et de traitement des pics P, Q, R, S et T a été testé 10 fois pendant 20 min consécutives sans problème.

<div style="page-break-after: always;"></div> 
<div style="font-size:var(--h1-fontsize);margin-top:2rem;margin-bottom:1rem;font-weight:300;color:var(--header-color);">Sommaire</h1> 
</div>

[TOC]

<div style="page-break-after: always;"></div> 

# La société et le contexte

## Las Vegas

Las Vegas est la plus grande ville de l'état du Nevada. La ville est située au milieu du désert des Mojaves. Elle est aujourd'hui considérée comme la capitale des casinos.

### L'histoire de Las Vegas

La ville de Las Vegas voit le jour en 1905. Située sur le trajet Los Angeles - Est des États-Unis, c'est un arrêt d'approvisionnement en eau pour les convois de chariots et pour les chemins de fer. Peu après la création de la ville, le Nevada interdit les jeux d'argent en 1910. Néanmoins, cela a peu d'impact, Las Vegas ayant une économie diversifiée et n'étant pas encore centrée sur les casinos. 

En 1930, le président Herbert Hoover donne son accord pour le barrage Boulder, qui sera renommé Hoover Dam (barrage Hoover) sous l'administration Truman. Les travaux commencent en 1931, et grâce à l'afflux d'ouvriers, la population de la ville quintuple, atteignant les 25 000 habitants. Du fait de la démographie de la population, majoritairement masculine et célibataire, Las Vegas connu un essor important dans le marché des grands spectacles de divertissement, le tout financé par la mafia et par des financiers Mormons. Des casinos illégaux, gérés par la mafia, commencent à faire leur apparition.

L'année suivante, l'État du Nevada légalise localement les jeux d'argent, réalisant que le jeu serait rentable pour l'économie locale. Le comté distribue les premières licences de jeu dans la foulée, et Fremont Street devient un des hauts lieux du jeu local, avec le *Northern Club*, mais aussi le *Las Vegas Club* ou l'*Hôtel Apache*. Las Vegas devient aussi un des bastions de la mafia, les casinos permettant de blanchir de l'argent assez facilement.

En 1940, une nouvelle partie de l'U.S. Route 95 est construite, donnant à la ville deux routes d'accès principales. C'est encore aujourd'hui un des axes majeurs du Nevada.

Le 3 avril 1941, Thomas Hull, un grand propriétaire d'hôtels, ouvre l'*El Rancho Vegas* sur ce qui deviendra plus tard l'avenue mythique du *Strip*. Cinq ans plus tard, en 1946, Meyer Lansky, un grand nom de la mafia, ouvre le Flamingo, lui aussi sur le Strip. Il est alors considéré comme l'hôtel le plus luxueux au monde. Cela attire de nombreux truands, qui investiront à leur tour avec la complicité de certains banquiers Mormons. De nombreux hôtels-casinos furent ainsi créés. 

En 1951, la commission de l'énergie atomique des États-Unis choisit le site d'essais du Nevada, à 180 km de Las Vegas, pour procéder au premier essai nucléaire de l'histoire du pays. Loin des dangers et des risques, la ville de Las Vegas décida d'annoncer les explosions comme des attractions touristiques majeures, allant jusqu'à créer des chambres d'hôtel spéciales pour avoir une vue sur les nuages en champignons. L'afflux de touristes et d'employés gouvernementaux oblige le comté à créer l'aéroport Mc Carran, qui deviendra plus tard un aéroport international avec l'augmentation massive de voyageurs. Les essais nucléaires se dérouleront en plein air jusqu'en 1963, date de leur interdiction suite à la promulgation du Traité d'interdiction partielle des essais nucléaires.

Tandis que les casinos et les hôtels continuent de se développer sur le *Strip*, Howard Hughes, un héros de l'aviation américaine, décide en 1961 de s'associer au gouvernement pour racheter des casinos gangrenés par la mafia. Il devient rapidement un des hommes puissants de Las Vegas, et met en route une large vague contre la corruption et la mafia au sein de la ville, notamment grâce à l'aide du journal local *Las Vegas Sun*, qui révèle que le Shérif du comté est impliqué dans des affaires de prostitution.

L'époque de la mafia prend fin, et à partir de 1980, de nouveaux entrepreneurs arrivent et ouvrent un nouveau chapitre de la ville : l'époque des méga-hôtels. De nombreux établissements somptueux et iconiques sont construits : *Rio*, *Excalibur*, le *MGM Grand*, la *Stratosphere Tower*, le *Bellagio*, etc. Las Vegas devient un endroit commercial et familial.

Las Vegas s'est aujourd'hui imposée comme la capitale du jeu, de l'hôtellerie de luxe, et du divertissement. 

### La situation actuelle de Las Vegas

La ville de Las Vegas se trouve dans le sud de l'État du Nevada, dans le comté de Clark (Clark County). La commune s'étend sur une superficie de 352 km<sup>2</sup>. La population en 2017 était estimée à 648 000 habitants. 

Cependant, la situation démographique de Las Vegas est complexe. En effet, l'agglomération de Las Vegas ne correspond pas du tout à son aire métropolitaine. Or, ce que l'on appelle communément "Las Vegas" dépasse les frontières officielles de la ville. L'exemple le plus flagrant est le fait que le *Strip* ne fait pas partie de la ville de Las Vegas, mais des "Unincorporated towns" (des zones ne dépendant d'aucune municipalité) de Paradise et de Winchester. L'UNLV ne fait pas non plus partie de Las Vegas, mais de Paradise. 

En prenant en compte ces différentes zones, la population de ce que l'on appelle à tord "Las Vegas" approche les 2 000 000 d'habitants. Dans ce document, sauf mention contraire, c'est cette zone que l'on appellera "Las Vegas".

La ville est située dans une vallée et est entourée de montagnes. Différents parcs d'état ou nationaux sont limitrophes : *Red Rock Canyon National Park*, *Valley of Fire State Park*, *Lake Mead National Recreation Area* et *Sloan Canyon National Conservation Area*. Le climat y est évidemment désertique, ce qui est un problème majeur pour l'approvisionnement en eau. La croissance démographie entraîne des besoins de plus en plus importants, que le lac Mead (lac artificiel de 32 000 km<sup>3</sup>, 885 km de rivage, créé par le barrage Hoover) a de plus en plus de mal à satisfaire. La municipalité prend des mesures drastiques contre le gaspillage de l'eau, au point que des amendes pouvant aller jusqu'à $5 000 ont été instaurées si des fuites d'eau étaient trouvées chez un particulier. La Southern Nevada Water Authority (SNWA) envisage de construire un aqueduc pour aller chercher l'eau nécessaire à la ville à 500 km au nord de Las Vegas.

La ville de Las Vegas est composée de différents quartiers, mais deux d'entre eux sont atypiques et très dépaysants : Downtown et le Strip.

Downtown est situé dans la partie Nord de Las Vegas, c'est le quartier historique de la ville. Les premiers hôtels et casinos s'y sont installés. Le quartier est centré sur Fremont Street, l'artère principale qui parcourt Downtown. La partie Nord de cette avenue est appelée Fremont Street Experience (FSE) et est réservée aux piétons. Le quartier est en fête tous les soirs, et rassemble ainsi des centaines de personnes, touristes comme locaux. L'attraction principale est un écran géant incurvé à 27 m de haut et de 460 m recouvrant toute la rue. Différents shows sont diffusés sur cet écran, assorti d'un gros système sonore. La rue est pleine de casinos, mais aussi de différents lieux promouvant l'art sous toutes ses formes : scènes de spectacles, peintres, graffitis, mimes, sculpture, théâtre, chant, musique, etc. Ce qui en fait un haut lieu culturel de la région. La zone est très contrôlée, notamment depuis la tuerie ayant fait 59 morts et 851 blessés le 1<sup>er</sup> octobre 2017 dans Paradise. Il s'agit de la tuerie de masse la plus importante de l'histoire des États-Unis.

Le second quartier atypique est le Strip. Le Strip fait 7,2 km de long, c'est l'emblème touristique de Las Vegas, la concentration d'hôtels et de casinos y est très élevée. L'avenue est d'ailleurs reconnue comme "National Scenic Byway" par le ministère américain des transports (U.S. Department of Transportation), c'est-à-dire que la route est reconnue pour son caractère culturel et touristique. C'est d'ailleurs l'un des seuls quartiers où les infrastructures piétonnes sont très développés. On peut ainsi traverser le Strip en empruntant uniquement des passerelles reliant les différents bâtiments. L'ensemble des établissements sont à la fois des hôtels et des casinos, ce qui en fait des mini-villes. Les complexes sont presque tous basés sur des thèmes différents, afin d'attirer une clientèle variée et cibler certaines classes sociales.

## L'Université du Nevada, Las Vegas (UNLV)

J'ai effectué mon stage au sein du College of Engineering de l'Université du Nevada, Las Vegas. Véritable ville dans la ville, plus de 30 000 étudiants y font leur études pour acquérir l'un des 350 diplômes que l'école offre. La directrice actuelle est Marta Meana, instituée le 1<sup>er</sup> juillet 2018.

Comme expliqué précédemment, la région de Las Vegas a été choisie en 1951 comme lieu phare des essais nucléaires américains. L'afflux d'employés gouvernementaux a créé un changement démographique dans la population de Las Vegas. La demande en éducation étant de plus en plus importante, une université fut créée en 1957, alors considérée comme une extension régionale de l'Université de Reno, la première université publique créée au Nevada. Les premiers diplômés sortirent de l'école en 1964. L'université fut ensuite temporairement appelée *Nevada Southern University*, puis s’émancipa de l'Université de Reno en 1969, année où le nom University of Nevada, Las Vegas (UNLV) fut officialisé.

Depuis, l'Université ne cesse de grandir, étoffant régulièrement les diplômes proposés, et son rayonnement national et international s’accroît. C'est par exemple l'UNLV qui a accueilli le dernier débat présidentiel entre Hillary Clinton et Donald Trump. L'école de journalisme de l'UNLV a couvert le débat sur la chaîne locale UNLV-TV.

Le pôle de recherche est reconnue comme étant un pôle majeur aux États-Unis. Les fonds y étant alloués sont en augmentation depuis quatre ans. 61 brevets ont ainsi été déposés en 2016.

Le campus fait 144 hectares et est situé au milieu de Las Vegas, entre le Strip et l'aéroport Mc Carran. Le bâtiment dans lequel j'ai travaillé est le *Science and Engineering Building* (SEB). Le bâtiment permet aux facultés de sciences, d'ingénieurie et de médecine de collaborer sur des projets communs. Notamment grâce à des équipements modernes et innovants tels que des microsondes EPMA (analyses chimiques non-destructives), des laboratoires spécialisés dans la culture de cellules eucaryotes (reproduction de tissus), ou encore des salles blanches dédiées à l'étude des nanotechnologies. 

## Le projet et sa place dans la médecine actuelle

