---
title: |
  | La théorie et la pratique des expériences de terrain : 
  | Une introduction des journées d'apprentissage du réseau EGAP
author: Jake Bowers,^[L'ordre des noms d'auteurs est généré de manière aléatoire. https://jakebowers.org] Maarten Voors,^[https://sites.google.com/site/maartenvoors/] et Nahomi Ichino^[https://nahomi.github.io/]
date: '20-01-2022'
site: bookdown::bookdown_site
knit: "bookdown::render_book"
documentclass: book
bibliography: learningdays-book.bib
link-citations: yes
colorlinks: yes
github-repo: egap/theory_and_practice_of_field_experiments
description: "Les journées d'apprentissage du réseau EGAP, inférence causale, expériences aléatoires, expériences de terrain, conception expérimentale, conception de recherche"
fontsize: 12pt
geometry: margin=1in
graphics: yes
clean: no
---







# Introduction

Durant la dernière décennie, [Evidence in Governance and Politics (EGAP)](https://egap.org/) a organisé une série d'ateliers, [les journées d'apprentissage](https://egap.org/learning-days/), dans le but de renforcer les compétences en recherche expérimentale en sciences sociales parmi les chargés de recherche -- chercheurs et praticiens -- en Afrique et Amérique Latine.  En partageant entre participants, méthodes pratiques et méthodes statistiques pour mener des expériences de terrain aléatoires, les journées d'apprentissage visent à créer et entretenir des réseaux de chercheurs dans le monde et à faciliter des liens solides et productifs entre ces chercheurs et les membres de EGAP.

Les journées d'apprentissage sont une combinaison d'ateliers de conception, de présentations de travaux de recherche, d'utilisation de logiciel statistique et de conférences thématiques par un petit groupe d'instructeurs, principalement des professeurs et des doctorants du réseau de EGAP. Les ateliers abordent les méthodes de conception et d'analyse pour des expériences de terrain aléatoires plutôt que des expériences aléatoires en laboratoire ou des études non-aléatoires.

**Ce livre** rassemble les matériaux développés pour les journées d'apprentissage. La version actuelle du livre est écrite principalement pour **des instructeurs et des organisateurs** d'ateliers et de cours similaires à l'intention de chargés de recherche --- professeurs, chercheurs postdoctorals, doctorants, évaluateurs d'ONG et d'agences gouvernementales, etc. --- qui réaliseront des études aléatoires de programmes liés aux institutions, à la gouvernance et au développement. Une grande partie des matériaux sera également utile comme rappel pour les participants des journées d'apprentissage précédentes.

Ce livre est une revue complète des méthodes d'inférence causale pour les chercheurs qui développent une conception de recherche expérimentale. Ce livre est organisé en **modules** et comprend des sujets tels que l'inférence causale, la randomisation, les tests d'hypothèses, les estimandes, les estimateurs, la puissance statistique, la mesure, les menaces pour la validité interne et l'éthique de l'expérimentation. Les modules apparaissent dans l'ordre jugé le plus utile. Cependant, les modules sont liés et peuvent être réorganisés afin de correspondre à vos besoins en tant qu'instructeur. En annexe, il y a des matériaux préparatoires comprenant un [glossaire des termes](glossary-of-terms.html) et une [introduction à R et RStudio](introduction-to-r-and-rstudio.html).

Ce livre comprend des **slides** sur le contenu principal, le [formulaire de conception de recherche de EGAP](researchdesignform.html) et des **références** d'exemples de recherche et des slides utilisées pendant les journées d'apprentissage précédentes. Ces matériaux renforcent le travail de EGAP sur la méthodologie, résumé dans les [guides de méthodes de EGAP](https://egap.org/methods-guides/). Comparé aux journées d'apprentissage précédentes, nous avons ajouté plus de matériaux sur les tests d'hypothèses, l'estimation et la puissance statistique. De nouveaux modules sur le processus de conception de recherche, la mesure et les considérations éthiques sont désormais disponibles. Les slides et les modules présentés ici contiennent trop d'informations pour être couverts en une seule semaine, la durée habituelle d'un atelier. Cependant, nous avons décidé de conserver toutes les informations, afin d'aider les instructeurs à adapter leurs cours à leurs publics réspectifs.

## Comment utiliser le livre

Pour profiter au maximum de ce livre, veuillez installer [R](https://cran.r-project.org/) et [RStudio](https://www.rstudio.com/products/rstudio/download/) sur votre ordinateur. En fait, les slides supposent que vous utilisiez R Markdown pour les adapter à vos besoins.

Pour commencer avec R, voir le module [Introduction à R et RStudio](introduction-to-r-and-rstudio.html).

Vous pouvez copier ce livre ou des parties de celui-ci (des slides, etc.) soit en utilisant le bouton de téléchargement (Download) sur la première page de <https://github.com/egap/theory_and_practice_of_field_experiments_french>, soit directement sur github en "forkant" ce repertoire.

Tant que vous citiez EGAP, vous pouvez utiliser ces matériaux. Veuillez consulter la licence Creative Commons Attribution-ShareAlike 4.0 International pour les termes exacts.

## Nous apprécions vos retours !

Si vous avez des questions, des retours, ou si vous avez organisé votre propre événement, contactez-nous !
Il suffit de créer une issue sur [Github](https://github.com/egap/theory_and_practice_of_field_experiments_french/issues) ou faire des commentaires en utilisant hypothes.is dans votre navigateur et de nous le faire savoir par e-mail, admin@egap.org. Nous parcourons régulièrement vos commentaires.

## Remerciements

Les matériaux dans ce livre ont été développés au cours des dernières journées d'apprentissage par divers instructeurs.
Ceux-ci incluent (par ordre alphabétique) Jake Bowers, Jasper Cooper, Ana De la O, Lindsay Dolan, Natalia Garbiras Díaz, Macartan Humphreys, Nahomi Ichino, Salif Jaiteh, Gareth Nellis, Dan Nielson, Rafael Piñeiro, Fernando Rosenblatt, Tara Slough, Peter van der Windt et Maarten Voors.  Nous remercions Natalia Garbiras Díaz, Macartan Humphreys, Anghella Brigeth Rosero Rodriguez, et Tara Slough en particulier pour leurs commentaires sur une première version du livre.

Chez EGAP, Matt Lisiecki, Ingrid Lee, Goldie Negelev, Max Mendez-Back et d'autres ont apporté un soutien formidable. Les journées d'apprentissage ont été généreusement financées par la Fondation Hewlett et soutenues par des institutions du monde entier, notamment l'African School of Economics (Bénin), l'Université de Diego Portales (Chili), l'Université de los Andes (Colombie), le Ghana Center for Democratic Development (Ghana) , Mercy Corps (Guatemala), Invest in Knowledge (Malawi), NYU Abu Dhabi (EAU), et l'Université catholique de l'Uruguay (Uruguay).

<!--chapter:end:index.Rmd-->


# Processus de conception de recherche

Ce livre vise à vous aider à comprendre et à concevoir des expériences de terrain aléatoires.  Avant d'entrer dans le détail de la conception de recherche, nous avons besoin d'une bonne question de recherche - une question qui fera progresser les connaissances ou aidera à prendre une décision politique, ou les deux. Il n'y a pas de recette simple pour trouver ou développer une bonne question scientifique ou politique, mais nos théories sont importantes pour articuler les bonnes questions qui sous-tendent une recherche percutante. Après avoir formulé notre question, nous développons la meilleure conception possible dans les limites de nos moyens, en utilisant notre connaissance de l'inférence causale et des statistiques présentées dans les modules qui suivent.

Ce module présente le [formulaire de conception de recherche EGAP](https://egap.github.io/learningdays-resources/Exercises/design-form.Rmd), une liste de contrôle pour vous guider à travers les nombreuses étapes du processus de recherche. Les journées d'apprentissage sont organisées autour du formulaire de conception de recherche. Nous vous incitons à utiliser le logiciel [DeclareDesign](https://declaredesign.org) pour explorer les implications des différents choix que nous pourrions faire pour nos conceptions de recherche. Enfin, ce module aborde les plans de pré-analyse et de pré-enregistrement. Lorsque nous planifions nos analyses et rendons ces plans publics, nous améliorons nos chances de convaincre les autres avec nos résultats.

## Contenu

- Une **bonne question de recherche** fait progresser la science et/ou est une question dont la réponse éclairera une décision politique.

- Certaines **conceptions de recherche** sont meilleures pour répondre à certaines questions. Nous voulons choisir la conception qui répond le mieux à nos questions clés compte tenu des contraintes et de nos moyens.

- Les questions que nous posons découlent --- souvent implicitement --- de nos valeurs et de notre compréhension du fonctionnement du monde. Ces **théories** rendent nos questions pertinentes. Et les expériences que nous réalisons nous renseignent sur la théorie. Ainsi, nous espérons que les preuves et les données issues de ces conceptions de recherche amélioreront notre compréhension.

- Composants de base d'une conception de recherche

- Présentation des composants de base de [formulaire de conception de recherche EGAP](https://egap.github.io/learningdays-resources/Exercises/design-form.html).

- Introduction du package [DeclareDesign](https://declaredesign.org) pour la conception de recherche.

- L'évolution des sciences sociales s'oriente vers **la revue des conceptions, au lieu de la revue des résultats**.

- **Le pré-enregistrement** -- ce que c'est, pourquoi et comment nous devons le faire.


## Slides

Vous trouverez ci-dessous des slides avec le contenu de base de notre conférence sur la conception de recherche. Vous pouvez les utiliser directement ou les copier localement avant de les éditer.

- [Code source en R Markdown](https://egap.github.io/learningdays-resources/Slides/researchdesignform-slides.Rmd)

- [Version PDF](https://egap.github.io/learningdays-resources/Slides/researchdesignform-slides.pdf)

- [Version HTML](https://egap.github.io/learningdays-resources/Slides/researchdesignform-slides.html)

Vous pouvez aussi lire les slides des précédentes journées d'apprentissage du réseau EGAP:

 - [Présentation de DeclareDesign aux journées d'apprentissage du réseau EGAP à l'Université catholique d'Uruguay, Montevideo, mars 2018](https://egap.github.io/learningdays-resources/Slides/Examples/declare_design-montevideo.pdf)

 - [Présentation de DeclareDesign aux journées d'apprentissage du réseau EGAP à Salima, Malawi, février 2017](https://egap.github.io/learningdays-resources/Slides/Examples/declare_design-malawi.pdf)

 - [Présentation de DeclareDesign  aux journées d'apprentissage du réseau EGAP à l'Université Diego Portales à Santiago, Chili, mai 2016](https://egap.github.io/learningdays-resources/Slides/Examples/declare_design-santiago.pdf)

Vous pouvez également voir les slides des discussions de conception lors des précédentes journées d'apprentissage du réseau EGAP, où les présentateurs se concentrent sur les problématiques relatives à la conception de recherche, plutôt qu'aux résultats:

 - [Discussion de conception aux journées d'apprentissage du réseau EGAP à l'African School of Economics, Benin, mars 2018](https://egap.github.io/learningdays-resources/Slides/Examples/research_design_2-benin.pdf)

 - [Discussion de conception 1 aux journées d'apprentissage du réseau EGAP à l'Université catholique d'Uruguay, Montevideo, mars 2018](https://egap.github.io/learningdays-resources/Slides/Examples/research_design_1-montevideo.pdf)

 - [Discussion de conception 2 aux journées d'apprentissage du réseau EGAP à l'Université catholique d'Uruguay, Montevideo, mars 2018](https://egap.github.io/learningdays-resources/Slides/Examples/research_design_2-montevideo.pdf)

 - [Discussion de conception 3 aux journées d'apprentissage du réseau EGAP à l'Université catholique d'Uruguay, Montevideo, mars 2018](https://egap.github.io/learningdays-resources/Slides/Examples/research_design_3-montevideo.pdf)

 - [Discussion de conception 1 aux journées d'apprentissage du réseau EGAP à l'Université Diego Portales à Santiago, Chili, mai 2016](https://egap.github.io/learningdays-resources/Slides/Examples/research_design_1-santiago.pdf)

 - [Discussion de conception 2 aux journées d'apprentissage du réseau EGAP à l'Université Diego Portales à Santiago, Chili, mai 2016](https://egap.github.io/learningdays-resources/Slides/Examples/research_design_2-santiago.pdf)

 - [Discussion de conception 3 aux journées d'apprentissage du réseau EGAP à l'Université Diego Portales à Santiago, Chili, mai 2016](https://egap.github.io/learningdays-resources/Slides/Examples/research_design_3-santiago.pdf)

 - [Discussion de conception aux journées d'apprentissage du réseau EGAP à Guatemala City, Guatemala, août 2017](https://egap.github.io/learningdays-resources/Slides/Examples/research_design-guatemala.pdf)

## Formulaire de conception et pré-enregistrement

- [Formulaire de conception de recherche EGAP](https://egap.github.io/learningdays-resources/Exercises/design-form.html). Une liste de contrôle que nous avons créée pour les journées d'apprentissage pour vous guider à travers les étapes du processus de recherche.
     - [Version Docx](https://egap.github.io/learningdays-resources/Exercises/design-form.docx)

     - [Version PDF](https://egap.github.io/learningdays-resources/Exercises/design-form.pdf)

     - [Version HTML](https://egap.github.io/learningdays-resources/Exercises/design-form.html)

- Liens vers les répertoires pour pré-enregistrement/plans de pré-analyse :

    - Le registre EGAP, hébergé par OSF (https://egap.org/registry/)

    - Le registre AEA RCT (https://www.socialscienceregistry.org/)

    - OSF (https://osf.io/registries)

- Exemples d'autres pré-enregistrements/plans de pré-analyse :

    - SMS au Mozambique du [gouvernement fédéral américain](https://oes.gsa.gov/projects/sms-mozambique/)

    - Caméras portatives pour les policiers du [Lab @ DC](https://osf.io/472zh)

## Ressources

### Guide des méthodes EGAP

- Guide des méthodes EGAP [10 choses à savoir sur les plans de pré-analyse](https://egap.org/resource/10-things-to-know-about-pre-analysis-plans/)

- Guide des méthodes EGAP [10 choses à savoir sur la mesure dans les expériences](https://egap.org/resource/10-things-to-know-about-measurement-in-experiments/)


### Livres, chapitres et articles

- [Pré-enregistrement comme outil pour renforcer l'évaluation fédérale](https://oes.gsa.gov/assets/files/preregistration-as-a-tool-in-federal-evaluation.pdf). Le livre blanc de l'Office of Evaluation Sciences du gouvernement américain. Vous pouvez également voir leurs exemples de plans de pré-analyse pour [toutes leurs expériences de terrain](https://oes.gsa.gov/work/).

- [@christensen_transparent_2019]. Le livre résume les nouvelles approches de la recherche en sciences sociales sur la transparence et la reproductibilité.

- [@gerber_field_2012].  Le chapitre 12 comprend quelques exemples de designs de recherche expérimentale.

### Outils

- [DeclareDesign](https://declaredesign.org/), un ensemble complet d'outils logiciels passionnants pour décrire, évaluer et mener des recherches empiriques.


<!--chapter:end:researchdesignform.Rmd-->


# Inférence causale {.tabset}

Une grande partie des sciences sociales porte sur la causalité. On peut se demander si [l'inscription des électeurs augmente la participation politique](https://egap.org/resource/electoral-administration-in-kenya/), si [la responsabilisation bottom-up peut améliorer les perspectives en matière de santé](https://egap.org/resource/does-bottom-up-accountability-work-evidence-from-uganda/), ou si [les récits personnels des migrants aident à réduire les attitudes préjudiciables à leur égard](https://egap.org/resource/brief-70-how-personal-narratives-reduce-negative-attitudes-towards-immigrants-in-kenya/).

Au cours de la dernière décennie, les sciences sociales sont devenues beaucoup plus strictes quant à la formulation des assertions causales, en s'appuyant sur une longue histoire de travaux sur la causalité remontant aux classiques de [Fisher et Rubin](#causalinference-classics). On recourt davantage aux expériences ; la randomisation est devenue la norme de référence pour répondre aux questions causales.

Dans ce module, nous introduisons l'approche contrefactuelle de l'inférence causale et comment des affirmations basées sur des assertions causales peuvent être interprétées. Nous présentons le modèle des résultats potentiels et la manière dont l'assignation aléatoire nous aide à faire des assertions sur ce qui se serait passé en l'absence de la politique publique, de l'action ou du programme que nous étudions. Nous discutons des trois hypothèses de base pour l'inférence causale : l'assignation aléatoire des sujets au traitement, la non-interférence et l'exclusion.

## Contenu

 - Qu'entendons-nous par **"cause"** ? Et pourquoi est-il important d'être clair sur le sens des assertions causales ?

 - Une introduction aux **résultats potentiels** comme une façon de penser aux états contrefactuels du monde.

 - La **randomisation** nous aide à comprendre les assertions causales contrefactuelles d'une manière particulièrement utile.

 - Les trois principales **hypothèses de base** pour l'inférence causale : l'assignation aléatoire des sujets au traitement, la non-interférence et l'exclusion.

 - Comparaison des études aléatoires avec les études d'observation.

 - La randomisation apporte une validité interne élevée, mais elle ne peut pas assurer la **validité externe**.

 - Votre question causale est liée à votre [conception de recherche](the-research-design-process.html).

## Slides

Vous trouverez ci-dessous des slides avec le contenu de base de notre conférence sur la causalité. Vous pouvez les utiliser directement ou les copier localement avant de les éditer.

- [Code source en R Markdown](https://egap.github.io/learningdays-resources/Slides/causalinference-slides.Rmd)

- [Version PDF](https://egap.github.io/learningdays-resources/Slides/causalinference-slides.pdf)

- [Version HTML](https://egap.github.io/learningdays-resources/Slides/causalinference-slides.html)

Vous pouvez aussi lire les slides des précédentes journées d'apprentissage du réseau EGAP :

 - [Présentation de l'inférence causale aux journées d'apprentissage du réseau EGAP à l'African School of Economics, Abomey-Calavi, juin 2019](https://egap.github.io/learningdays-resources/Slides/Examples/causality-benin.pdf)

 - [Présentation de l'inférence causale aux journées d'apprentissage du réseau EGAP à l'Université des Andes, Bogotá, avril 2019](https://egap.github.io/learningdays-resources/Slides/Examples/causality-bogota.pdf)

 - [Présentation de l'inférence causale aux journées d'apprentissage du réseau EGAP à l'Université catholique d'Uruguay, Montevideo, mars 2018](https://egap.github.io/learningdays-resources/Slides/Examples/causality-montevideo.pdf)

 - [Présentation de l'inférence causale aux journées d'apprentissage du réseau EGAP à Guatemala City, Guatemala, août 2017](https://egap.github.io/learningdays-resources/Slides/Examples/causality-guatemala.pdf)

 - [Présentation à l'introduction sur les expériences aux journées d'apprentissage du réseau EGAP à Guatemala City, Guatemala, août 2017](https://egap.github.io/learningdays-resources/Slides/Examples/intro_experiments-guatemala.pdf)

 - [Présentation de l'inférence causale aux journées d'apprentissage du réseau EGAP à Salima, Malawi, février 2017](https://egap.github.io/learningdays-resources/Slides/Examples/causality-malawi.pdf)

 - [Présentation de l'inférence causale aux journées d'apprentissage du réseau EGAP à l'Université Diego Portales à Santiago, Chili, mai 2016](https://egap.github.io/learningdays-resources/Slides/Examples/causality-santiago.pdf)

## Ressources

### Guide des méthodes EGAP

- Guide des méthodes EGAP [10 choses à savoir sur l'inférence causale](https://egap.org/resource/10-things-to-know-about-causal-inference/)

- Guide des méthodes EGAP [10 stratégies pour déterminer si X a causé Y](https://egap.org/resource/10-strategies-figuring-out-if-x-caused-y/)

- Guide des méthodes EGAP [10 choses à savoir sur les mécanismes](https://egap.org/resource/10-things-mechanisms/)

- Guide des méthodes EGAP [10 choses à savoir sur la validité externe](https://egap.org/resource/10-things-to-know-about-external-validity/)

### Livres, chapitres et articles {#causalinference-cites}

#### Classiques {#causalinference-classics}

- [@fisher_design_1935]. Fisher introduit l'idée de la randomisation et des tests d'hypothèses pour étudier l'inférence causale.

- [@rubin:1974]. Rubin introduit l'idée de résultats potentiels et relie la conceptualisation contrefactuelle de la causalité à l'inférence statistique.

#### Revue actuelle

- [@brady2008causation].

- [@gerber_field_2012, Chapitre 1]. Ce livre est une excellente ressource pour de nombreux sujets de la conception expérimentale.

- [@morgan_counterfactuals_2007, Chapitre 1]. Ce livre comprend de bons examples de raisonnement pour faire des assertions causales à partir de données d'observation.

- [@glennerster_running_2013]. Ceci est une excellente introduction pour mener des expériences de terrain, illustrée par nombreux exemples.

### Notes d'orientation des politiques publiques EGAP

Quelques exemples de questions causales :

- [Note d'orientation des politiques publiques EGAP 38 : Les campagnes d'éducation des électeurs à la radio sont-elles efficaces pour décourager les électeurs de voter pour des partis ou candidats qui s'engagent dans l'achat de voix ?](https://egap.org/resource/brief-38-diminishing-the-effectiveness-of-vote-buying-through-voter-education/)

- [Note d'orientation des politiques publiques EGAP 51 : Les technologies de l'information et de communication gratuites et anonymes peuvent-elles renforcer la responsabilité locale et améliorer les prestations de services publics ?](https://egap.org/resource/does-information-technology-improve-public-service-delivery-lessons-from-uganda/)

- [Note d'orientation des politiques publiques EGAP 58 : La responsabilisation bottom-up peut-elle améliorer les perspectives en matière de santé ?](https://egap.org/resource/does-bottom-up-accountability-work-evidence-from-uganda/)

- [Note d'orientation des politiques publiques EGAP 69 : Une surveillance citoyenne bottom-up améliore-t-elle les prestations de services publics ?](https://egap.org/resource/brief-69-bottom-up-accountability-and-public-service-provision-in-brazil/)



<!--chapter:end:causalinference.Rmd-->


# Randomisation {.tabset}

Le module sur [l'inférence causale](causal-inference.html) aborde le rôle important de la randomisation pour tirer des inférences valides à partir d'une comparaison des groupes traités et non traités. Dans ce module, nous passons de la théorie aux cas concrets pour votre conception de recherche.

Nous introduisons quatre façons courantes de randomiser le traitement -- simple, complète, par bloc, et en grappe (cluster) -- et nous expliquons quand ces différents types de randomisation sont disponibles et appropriés.  Nous couvrons également plusieurs conceptions courantes, y compris les conceptions factorielles et les conceptions incitatives.  Le module fournit des conseils sur l'implémentation, y compris les bonnes pratiques pour vérifier l'homogénéité et assurer la reproductibilité.

## Contenu

- Qu'est-ce que la **randomisation** ? L'assignation aléatoire **n'est pas** la même chose que l'échantillonnage aléatoire.

- Quatre façons courantes de randomiser le traitement :

    - **Simple** : assigner de manière aléatoire les unités au traitement (comme un tirage au sort).

    - **Complète** : au sein d'une liste d'unités éligibles, assigner un nombre fixe d'unités au traitement (comme un tirage d'une urne sans remise).

    - **Par bloc (ou stratifiée)** : assigner un traitement dans des strates ou des blocs spécifiques, comme si vous meniez une expérience dans chaque bloc.
      
    - **Par grappe (cluster)** : assigner des groupes d'observation (grappes ou clusters) à la même condition de traitement.
    
    
- Quelques conceptions courantes :
    
    - **Accès randomisé** : randomiser la disponibilité du traitement.
    
    - **Accès randomisé differé** : randomiser le timing de l'accès au traitement.
    
    - **Factorielle** : randomiser les unités en combinant les bras de traitement.
    
    - **Incitative** : randomiser l'incitation à prendre le traitement.

- Comment vérifier si votre randomisation a produit des groupes homogènes sur les caractéristiques observables ? En règle générale, nous effectuons des tests de randomisation, également appelés tests d'homogénéité. On peut, par exemple, utiliser le test omnibus $d^2$ de `xBalance` dans le package `RItools` (car c'est une inférence de randomisation) ou on peut approximer ce résultat avec un test $F$.

- La randomisation a **des limites**.  Nous en discutons ici et nous vous orientons vers le module sur [les menaces](threats-to-internal-validity-of-randomized-experiments.html) pour en savoir plus.

## Slides

Vous trouverez ci-dessous des slides avec le contenu de base de notre conférence sur la randomisation. Vous pouvez les utiliser directement ou les copier localement avant de les éditer.

- [Code source en R Markdown](https://egap.github.io/learningdays-resources/Slides/randomization-slides.Rmd)

- [Version PDF](https://egap.github.io/learningdays-resources/Slides/randomization-slides.pdf)

- [Version HTML](https://egap.github.io/learningdays-resources/Slides/randomization-slides.html)

Les fichiers liés montrent comment [faire une randomisation reproducible en R](https://egap.github.io/learningdays-resources/Exercises/randomization-exercises.Rmd).
Vous pouvez également voir plus d'exemples de randomisation en R ici : [10 choses à savoir sur la randomisation](https://egap.org/resource/10-things-to-know-about-randomization/).

Vous pouvez aussi lire les slides des précédentes journées d'apprentissage du réseau EGAP :

- [Présentation des problèmes de conception aux journées d'apprentissage du réseau EGAP à l'African School of Economics, Abomey-Calavi, juin 2019 (la première section passe en revue les conceptions de randomisation)](https://egap.github.io/learningdays-resources/Slides/Examples/threats-benin.pdf)

- [Présentation de la randomisation aux journées d'apprentissage du réseau EGAP à l'Université des Andes, Bogotá, avril 2019](https://egap.github.io/learningdays-resources/Slides/Examples/randomization-bogota.pdf)

- [Présentation de la randomisation aux journées d'apprentissage du réseau EGAP à l'Université catholique d'Uruguay, Montevideo, mars 2018](https://egap.github.io/learningdays-resources/Slides/Examples/randomization-montevideo.pdf)

- [Présentation de la randomisation aux journées d'apprentissage du réseau EGAP à Guatemala City, Guatemala, août 2017](https://egap.github.io/learningdays-resources/Slides/Examples/randomization-guatemala.pdf)

- [Présentation de la randomisation aux journées d'apprentissage du réseau EGAP à Salima, Malawi, février 2017](https://egap.github.io/learningdays-resources/Slides/Examples/randomization-malawi.pdf)

- [Présentation de la randomisation aux journées d'apprentissage du réseau EGAP à l'Université Diego Portales à Santiago, Chili, mai 2016](https://egap.github.io/learningdays-resources/Slides/Examples/randomization-santiago.pdf)


## Ressources

### Guide des méthodes EGAP

- Guide des méthodes EGAP [10 choses à savoir sur la randomisation](https://egap.org/resource/10-things-to-know-about-randomization/)

- Guide des méthodes EGAP [10 choses à savoir sur la randomisation par grappe (cluster)](https://egap.org/resource/10-things-to-know-about-cluster-randomization/)

### Livres, chapitres et articles

- [Procédures opérationnelles standard pour le laboratoire de Don Green à l'Université de Columbia](https://github.com/acoppock/Green-Lab-SOP). Un ensemble complet de procédures et de règles empiriques pour mener des études expérimentales.

- [@glennerster_running_2013]. Chapitre 2 sur la randomisation.

- [@gerber_field_2012]. Chapitre 2 : Inférence causale et expérimentation

### Notes d'orientation des politiques publiques EGAP

*Conceptions factorielles*

- [Note d'orientation des politiques publiques EGAP 57 : Comment les médias influencent les normes sociales : la preuve au Mexique](https://egap.org/resource/how-media-influence-social-norms-evidence-from-mexico/)

- [Note d'orientation des politiques publiques EGAP 58 : La responsabilisation bottom-up fonctionne-t-elle  ?](https://egap.org/resource/does-bottom-up-accountability-work-evidence-from-uganda/)

*Randomiser l'accès*

- [Note d'orientation des politiques publiques EGAP 24 : Réduire l'accaparation par les élites dans les îles Salomon](https://egap.org/resource/brief-24-reducing-elite-capture-in-the-solomon-islands/)

*Accès randomisé differé*

  - [Note d'orientation des politiques publiques EGAP 35 : Réduire la récidive parmi les détenus libérés](https://egap.org/resource/brief-35-reducing-reconvictions-among-released-prisoners/)

  - [Note d'orientation des politiques publiques EGAP 60 : Réduire le soutien des jeunes à la violence grâce à la formation et aux transferts de cash en Afghanistan](https://egap.org/resource/reducing-youth-support-for-violence-through-training-and-cash-transfers-in-afghanistan/)

*Randomisation par grappe (cluster)*

  - [Note d'orientation des politiques publiques EGAP 22 : Pousser au vote](https://egap.org/resource/brief-22-getting-out-the-vote/)

*Randomisation combinée par grappe et par bloc*

  - [Note d'orientation des politiques publiques EGAP 54 : Révélations de malversations des politicens en place](https://egap.org/resource/evidence-from-mexico-the-effect-of-incumbent-malfeasance-revelations/)

  - [Note d'orientation des politiques publiques EGAP 56 : Signaler la corruption](https://egap.org/resource/reporting-corruption-in-nigeria-testing-the-effects-of-norms-nudges/)


### Outils

- [RItools](https://cran.r-project.org/web/packages/RItools/index.html), un ensemble d'outils pour l'inférence de randomisation, y compris le test d'homogénéité.


### Courtes vidéos explicatives

 - [Randomisation vs. échantillonnage aléatoire](https://www.youtu.be/02A61b3hxvA)
 
 - [Randomisation par grappe vs. par bloc](https://www.youtu.be/bL2U9z8hX1k)
 

<!--chapter:end:randomization.Rmd-->


# Tests d'hypothèses {.tabset}

Ce n'est pas possible d'observer directement les effets causaux à cause du *problème fondamental de l'inférence causale* ([module de l'inférence causale](causal-inference.html)).
Comment pouvons-nous en savoir plus sur ces *effets causaux non observés* en utilisant ce que nous observons ?
Dans une expérience aléatoire, nous pouvons évaluer des *suppositions* ou des *hypothèses* sur les effets causaux non observés.
Pour ce faire, nous comparons ce que nous observons dans une expérience à ce que nous observerions si nous pouvions répéter la manipulation expérimentale et que la supposition ou l'hypothèse était vraie.

Dans ce module, nous présentons les tests d'hypothèses, leur lien avec l'inférence causale, les $p$-valeurs et ce qu'il faut faire lorsque nous avons plusieurs hypothèses à tester.

## Contenu

- Qu'est-ce qu'une **bonne hypothèse** ?

- La relation entre les tests d'hypothèses et l'inférence causale.

- **Tests d'hypothèses**.

     - L'hypothèse nulle.

     - Estimateurs vs. statistiques de test.

     - Dans une expérience, une distribution de référence pour un test d'hypothèse provient de la conception expérimentale et de la randomisation.

     - Les $p$-valeurs et comment interpréter les résultats des tests d'hypothèses.

- Un bon test d'hypothèse doit (1) rarement mettre en doute la vérité (c'est-à-dire avoir un taux de faux positifs contrôlé et faible) et (2) distinguer facilement le signal du bruit (c'est-à-dire mettre souvent en doute les contrevérités ; avoir une puissance statistique élevée) .

- Comment saurons-nous si notre test d'hypothèse performe bien ? (Se référer au [module d'analyse de puissance statistique](statistical-power-and-design-diagnosands.html)).

    - Taux de faux positifs.
    
    - Couverture correcte de l'intervalle de confiance.

    - Évaluer le taux de faux positifs d'un test d'hypothèse pour une conception et un choix de statistique de test donnés;
      cas d'un essai aléatoire par grappe (cluster) avec utilisation de l'erreur type robuste pour grappe.

- Soyez prudent lorsque vous testez **de nombreuses hypothèses**, par exemple quand vous avez plus de deux bras de traitement ou que vous évaluez les effets d'un traitement sur plusieurs résultats. Nous devons veiller à **ajuster les $p$-valeurs ou les intervalles de confiance** pour refléter le nombre de tests ou d'intervalles produits.

## Slides

Vous trouverez ci-dessous des slides avec le contenu de base de notre conférence sur les tests d'hypothèses. Vous pouvez les utiliser directement ou les copier localement avant de les éditer.

 - [Code source en R Markdown](https://egap.github.io/learningdays-resources/Slides/hypothesistesting-slides.Rmd)

 - [Version PDF](https://egap.github.io/learningdays-resources/Slides/hypothesistesting-slides.pdf)

 - [Version HTML](https://egap.github.io/learningdays-resources/Slides/hypothesistesting-slides.html)

Vous pouvez aussi lire les slides des précédentes journées d'apprentissage du réseau EGAP :

 - [Présentation des tests d'hypothèses aux journées d'apprentissage du réseau EGAP à l'African School of Economics, Abomey-Calavi, juin 2019](https://egap.github.io/learningdays-resources/Slides/Examples/hypothesistesting-benin.pdf)

 - [Présentation des tests d'hypothèses aux journées d'apprentissage du réseau EGAP à l'Université des Andes, Bogotá, avril 2019](https://egap.github.io/learningdays-resources/Slides/Examples/hypothesistesting-bogota.pdf)

 - [Présentation des tests d'hypothèses aux journées d'apprentissage du réseau EGAP à l'Université catholique d'Uruguay, Montevideo, mars 2018](https://egap.github.io/learningdays-resources/Slides/Examples/hypothesistesting-montevideo.pdf)

 - [Présentation des tests d'hypothèses aux journées d'apprentissage du réseau EGAP à Guatemala City, Guatemala, août 2017](https://egap.github.io/learningdays-resources/Slides/Examples/hypothesistesting-guatemala.pdf)

 - [Présentation des tests d'hypothèses aux journées d'apprentissage du réseau EGAP à Salima, Malawi, février 2017](https://egap.github.io/learningdays-resources/Slides/Examples/hypothesistesting-malawi.pdf)

 - [Présentation des tests d'hypothèses aux journées d'apprentissage du réseau EGAP à l'Université Diego Portales à Santiago, Chili, mai 2016](https://egap.github.io/learningdays-resources/Slides/Examples/hypothesistesting-santiago.pdf)


## Ressources

### Guide des méthodes EGAP

  - Guide des méthodes EGAP [10 choses à savoir sur les tests d'hypothèses](https://egap.org/resource/10-things-to-know-about-hypothesis-testing/)

  - Guide des méthodes EGAP [10 choses à savoir sur les comparaisons multiples](https://egap.org/resource/10-things-to-know-about-multiple-comparisons/)

### Livres, chapitres et articles

 - [@gerber_field_2012]. Chapitre 3 : Distributions d'échantillonnage, inférence statistique et tests d'hypothèses.
 
 - [@rosenbaum2010design]. Chapitre 2 : Inférence causale dans les expériences aléatoires.
 
 - [@rosenbaum2017observation]. Partie I : Expériences aléatoires.


<!--chapter:end:hypothesistesting.Rmd-->


# Estimandes et estimateurs {.tabset}

Les expériences aléatoires génèrent de bonnes suppositions sur le résultat moyen sous traitement et le résultat moyen sous contrôle. Cela nous permet d'avoir des estimateurs sans biais de l'effet moyen du traitement.  Nous pouvons également utiliser la randomisation pour décrire comment les estimations générées par un estimateur peuvent varier d'une expérience à l'autre en utilisant l'erreur type et les intervalles de confiance.

Dans ce module, nous introduisons plusieurs types d'estimandes. Le choix de l'estimande est une décision scientifique et politique -- sur quelle quantité aimerions-nous en savoir plus ?  De plus, nous voulons sélectionner un estimateur approprié pour cet estimande dans le cadre de la conception de recherche. Nous discutons de la façon dont les estimateurs sont appliqués aux données pour générer un estimande et comment caractériser sa variabilité.


## Contenu

- Un **effet causal**, $\tau_i$, est une comparaison des résultats potentiels non observés pour chaque unité $i$.  Par exemple, cela peut être une différence ou un ratio entre résultats potentiels non observés.

- Pour en savoir plus sur $\tau_{i}$, on peut traiter $\tau_{i}$ comme un **estimande** ou une quantité cible à estimer (voir ce module)
ou comme une quantité cible sur laquelle émettre une hypothèse ([voir le module des tests d'hypothèses](hypothesis-testing.html)).

- Beaucoup de gens se concentrent sur **l'effet moyen du traitement (Average Treatment Effect / ATE)**, $\bar{\tau}=\sum_{i=1}^n
   \tau_{i}$, en partie parce qu'il permet **d'estimer** facilement.

- Un **estimateur** est une recette pour calculer une supposition sur la valeur d'un estimande. Par exemple, la différence entre la moyenne des résultats observés pour $m$ unités traitées et la moyenne des résultats observés pour $N-m$ unités non traitées est un estimateur de $\bar{\tau}$.

- Différentes randomisations produiront différentes valeurs du même estimateur ciblant le même estimande. **L'erreur type** résume cette variabilité au sein d'un estimateur.

- Un **intervalle de confiance** de $100(1-\alpha)$% est un ensemble d'hypothèses qui ne peuvent être rejetées au niveau $\alpha$. Nous avons tendance à rapporter des intervalles de confiance contenant des hypothèses sur les valeurs de notre estimande et à utiliser notre estimateur comme statistique de test.

- Les estimateurs devraient (1) éviter les erreurs systématiques dans leur estimation de l'estimande (être sans biais) ; (2) peu varier dans leurs suppositions d'une expérience à l'autre (être précis ou efficace) ; et peut-être idéalement (3) converger vers l'estimande quand ils utilisent de plus en plus d'informations (être cohérent).

 - **Analyser en randomisant** dans le contexte de l'estimation signifie que (1) nos erreurs types devraient mesurer la variabilité de la randomisation et (2) nos estimateurs devraient cibler des estimandes définis en termes de résultats potentiels.

 - Nous **ne contrôlons pas** les covariables lorsque nous analysons les données d'expériences aléatoires. Pourtant les covariables peuvent rendre notre estimation plus **précise**. C'est ce qu'on appelle **l'ajustement de covariance**. L'ajustement de covariance dans les expériences aléatoires diffère du contrôle des variables dans les études d'observation.

 - Une intervention politique (comme une lettre qui incite à l'exercice) peut *avoir l'intention* de changer un comportement par **une dose active** (exercice réel). Nous pouvons étudier l'effet causal de l'intention en envoyent les lettres de façon aléatoire. C'est ce qu'on appele **l'effet d'intention de traiter** (intent to treat effect, **ITT**).
 
 - Nous pouvons étudier l'effet causal de l'exercice réel en utilisant l'assignation aléatoire de lettres comme **instrument** de la dose active (l'exercice lui-même) afin d'apprendre davantage sur l'effet causal de l'exercice **chez ceux qui changeraient leur comportement après avoir reçu la lettre**. Cette version de l'effet causal moyen est souvent connue sous le nom **d'effet moyen local du traitement** ou d'effet causal moyen pour ceux qui se conforment au traitement (complier average causal effect, CACE).


## Slides

Vous trouverez ci-dessous des slides avec le contenu de base pour cette section.

- [Code source en R Markdown](https://egap.github.io/learningdays-resources/Slides/estimation-slides.Rmd)

- [Version PDF](https://egap.github.io/learningdays-resources/Slides/estimation-slides.pdf)

- [Version HTML](https://egap.github.io/learningdays-resources/Slides/estimation-slides.html)

Vous pouvez aussi lire les slides des précédentes journées d'apprentissage du réseau EGAP:

 - [Présentation de l'estimation aux journées d'apprentissage du réseau EGAP à l'African School of Economics, Abomey-Calavi, juin 2019](https://egap.github.io/learningdays-resources/Slides/Examples/estimation-benin.pdf)

 - [Présentation de l'estimation aux journées d'apprentissage du réseau EGAP à l'Université des Andes, Bogotá, avril 2019](https://egap.github.io/learningdays-resources/Slides/Examples/estimation-bogota.pdf)

 - [Présentation de l'estimation aux journées d'apprentissage du réseau EGAP à l'Université catholique d'Uruguay, Montevideo, mars 2018](https://egap.github.io/learningdays-resources/Slides/Examples/estimation-montevideo.pdf)

 - [Présentation de l'estimation aux journées d'apprentissage du réseau EGAP à l'Université Diego Portales à Santiago, Chili, mai 2016](https://egap.github.io/learningdays-resources/Slides/Examples/estimation-santiago.pdf)

Vous pouvez également voir les problèmes d'estimation de l'effet de la dose active d'un traitement dans ces slides (ainsi que les problèmes causés par les données manquantes dans les résultats pour l'estimation de l’effet causal moyen) :

- [Présentation des problèmes de conception aux journées d'apprentissage du réseau EGAP à l'African School of Economics, Abomey-Calavi, juin 2019 (la première section passe en revue les conceptions de randomisation)](https://egap.github.io/learningdays-resources/Slides/Examples/threats-benin.pdf)

- [Présentation des effets de débordement et de l'attrition aux journées d'apprentissage du réseau EGAP à Guatemala City, Guatemala, août 2017](https://egap.github.io/learningdays-resources/Slides/Examples/spillovers_attrition-guatemala.pdf)

- [Présentation des menaces aux journées d'apprentissage du réseau EGAP à Guatemala City, Guatemala, août 2017](https://egap.github.io/learningdays-resources/Slides/Examples/threats-guatemala.pdf)

- [Présentation des complications aux journées d'apprentissage du réseau EGAP à Salima, Malawi, février 2017](https://egap.github.io/learningdays-resources/Slides/Examples/complications-malawi.pdf)

- [Présentation des menaces aux journées d'apprentissage du réseau EGAP à l'Université Diego Portales à Santiago, Chili, mai 2016 (la section du milieu examine l'ITT et la non-conformité)](https://egap.github.io/learningdays-resources/Slides/Examples/threats-santiago.pdf)


## Ressources

### Guide des méthodes EGAP

 - Guide des méthodes EGAP [Les 10 types d'effets de traitement à connaître](https://egap.org/resource/10-types-of-treatment-effect-you-should-know-about/)

 - Guide des méthodes EGAP [10 choses à savoir sur l'ajustement de covariable](https://egap.org/resource/10-things-to-know-about-covariate-adjustment/)

 - Guide des méthodes EGAP [10 choses à savoir sur les données manquantes](https://egap.org/resource/10-things-to-know-about-missing-data/)

 - Guide des méthodes EGAP [10 choses à savoir sur l'effet moyen local du traitement](https://egap.org/resource/10-things-to-know-about-the-local-average-treatment-effect/)

 - Guide des méthodes EGAP [10 choses à savoir sur les effets de débordement](https://egap.org/resource/10-things-to-know-about-spillovers/)

### Livres, chapitres et articles

 - [@gerber_field_2012]. Chapitre 2.7 sur l'exclusion et la non-interférence, Chapitre 3, Chapitre 5 sur la non-conformité unilatérale, Chapitre 6 sur la non-conformité bilatérale, Chapitre 7 sur l'attrition, Chapitre 8 sur l'interférence entre les unités expérimentales.

 - [@bowers2020causality].


### Outils

- [DeclareDesign](https://declaredesign.org)

- [Le package estimatr en R](https://declaredesign.org/r/estimatr/)


<!--chapter:end:estimation.Rmd-->

---
output:
  pdf_document: default
  html_document: default
---

# Puissance statistique et diagnostics de conception {.tabset}

Avant de commencer une étude, nous aimerions savoir si notre conception a la puissance statistique nécessaire pour détecter un effet s'il existe.  Il est difficile d'apprendre d'une étude qui n'a pas une puissance statistique suffisante. Sans une puissance statistique suffisante, nous ne savons pas si un résultat nul signifie qu'il n'y a pas eu d'effet, ou que nous n'avons pas réussi à détecter un effet non nul qui existe. Une analyse de puissance statistique peut vous aider à améliorer votre conception et à mieux répartir vos ressources. Cela peut même vous aider à décider de ne pas mener l'étude.

Dans ce module, nous introduisons la puissance statistique, les approches de base pour calculer la puissance par calcul analytique ou par simulation, et comment les caractéristiques de conception telles que les blocs, l'ajustement des covariables et les grappes (clusters) ont un impact sur la puissance statistique.

## Contenu

 - **La puissance statistique** est la capacité d'une étude à détecter un effet s'il existe.
 
 - **L'analyse de puissance** s'effectue avant la réalisation d'une étude.  Cela aide à déterminer l'échantillon dont on a besoin ou les effets que l'on peut détecter. C'est une étape essentielle dans la conception de recherche et cela aide à communiquer sur sa conception.

 - Méthodes courantes de calcul de puissance :
 
      - Calculs de puissance **analytique** (en utilisant une formule)
 
      - **Simulations** (par exemple, en utilisant DeclareDesign)

 - **L'ajustement des covariables** et **des blocs** peut augmenter la puissance statistique.

 - Pour les **conceptions par grappe** il faut tenir compte de la corrélation intra-grappe (la variance intra-grappe par rapport à la variance globale).
 
 - La puissance statistique est étroitement liée à [la conception de l'étude](the-research-design-process.html), aux [tests d'hypothèses](hypothesis-testing.html) et à [l'estimation](estimands-and-estimators.html).

## Slides
Vous trouverez ci-dessous des slides avec le contenu de base de notre conférence sur la puissance statistique. Vous pouvez les utiliser directement ou les copier localement avant de les éditer.

 - [Code source en R Markdown](https://egap.github.io/learningdays-resources/Slides/power-slides.Rmd)

 - [Version PDF](https://egap.github.io/learningdays-resources/Slides/power-slides.pdf)

 - [Version HTML](https://egap.github.io/learningdays-resources/Slides/power-slides.html)

Vous pouvez aussi lire les slides des précédentes journées d'apprentissage du réseau EGAP :

 - [Présentation de la puissance statistique des journées d'apprentissage du réseau EGAP à l'African School of Economics, Abomey-Calavi, juin 2019](https://egap.github.io/learningdays-resources/Slides/Examples/power-benin.pdf)

 - [Présentation de la puissance statistique des journées d'apprentissage du réseau EGAP à l'Université des Andes, Bogotá, avril 2019](https://egap.github.io/learningdays-resources/Slides/Examples/power-bogota.pdf)

 - [Présentation de la puissance statistique des journées d'apprentissage du réseau EGAP à l'Université catholique d'Uruguay, Montevideo, mars 2018](https://egap.github.io/learningdays-resources/Slides/Examples/power-montevideo.pdf)

 - [Présentation de la puissance statistique des journées d'apprentissage du réseau EGAP à Guatemala City, Guatemala, août 2017](https://egap.github.io/learningdays-resources/Slides/Examples/power-guatemala.html)

 - [Présentation de la puissance statistique des journées d'apprentissage du réseau EGAP à Salima, Malawi, février 2017](https://egap.github.io/learningdays-resources/Slides/Examples/power-malawi.pdf)

 - [Présentation de la puissance statistique des journées d'apprentissage du réseau EGAP à l'Université Diego Portales à Santiago, Chili, mai 2016](https://egap.github.io/learningdays-resources/Slides/Examples/power-santiago.pdf)


## Ressources

### Guide des méthodes EGAP

 - Guide des méthodes EGAP [10 choses à savoir sur la puissance statistique](https://egap.org/resource/10-things-you-need-know-about-statistical-power/)

 - Guide des méthodes EGAP [10 choses à savoir sur l'ajustement des covariables](https://egap.org/resource/10-things-to-know-about-covariate-adjustment/)
 
 - Guide des méthodes EGAP [10 choses que vos résulats nuls peuvent signifier](https://egap.org/resource/10-things-your-null-result-might-mean/)

### Notes d'orientation des politiques publiques EGAP et plans de pré-analyse

Quelques exemples d'analyse de puissance statistique dans les conceptions de recherche :

 - [Plan de pré-analyse. La responsabilisation peut transformer la santé : une réplication et une extension de Bjorkman et Svensson (2009)](https://osf.io/qxwmu/)
 
 - [Note d'orientation des politiques publiques EGAP 58 : La responsabilisation bottom-up peut-elle améliorer les perspectives en matière de santé ?](https://egap.org/resource/does-bottom-up-accountability-work-evidence-from-uganda/)


### Outils
 - Analyse de puissance statistique interactive
 
      - [Calculateur de puissance statistique EGAP](https://egap.shinyapps.io/power-app/)
 
      - [rpsychologist](https://rpsychologist.com/d3/NHST/)

 - Packages en R pour l'analyse de puissance statistique
 
      - [pwr](https://cran.r-project.org/web/packages/pwr/index.html)
 
      - [DeclareDesign](https://cran.r-project.org/web/packages/DeclareDesign/index.html), voir aussi <https://declaredesign.org/>


<!--chapter:end:statisticalpower.Rmd-->


# Mesure {.tabset}

Pour estimer des effets et tester des hypothèses, nous utilisons souvent un résultat mesuré à l'aide de données quantitatives provenant d'enquêtes, de jeux comportementaux ou d'archives administratives. Pour les questions causales, nous utilisons généralement des données de résultats immédiats et finaux et de mécanismes de base. Nous utilisons des données de base pour identifier les sous-groupes pertinents, ajuster nos estimations ou randomiser notre traitement par bloc. Les mesures doivent être valides et fiables. Sachez que les données peuvent être bruitées (erreur aléatoire) et/ou biaisées (erreur systématique).

Ce module traite *que mesurer* et *comment mesurer*. Il montre à quel point une bonne mesure est liée à la [conception de recherche](https://egap.github.io/learningdays-resources/Exercises/design-form.Rmd) et à la [puissance statistique](statistical-power-and-design-diagnosands.html).

## Contenu

 - Lorsque nous représentons un attribut d'une unité par un nombre, une lettre, un mot ou un symbole d'une manière systématique (par exemple, dans une case d'un simple dataset), nous **mesurons**.

 - Une mesure **valide** d'un concept ou d'un phénomène d'intérêt doit clairement représenter cette entité sous-jacente et souvent abstraite.

 - Une mesure **fiable** d'un concept donnerait la même valeur pour l'unité de mesure (par exemple, une personne ou un village) si les conditions ne changent pas.

 - Nous pouvons évaluer nos théories de mesure en utilisant plusieurs approches pour mesurer les résultats, les covariables ou les différences entre unités en fonction des différents rendus des mécanismes causaux.

 - Pour votre [conception de recherche](https://egap.github.io/learningdays-resources/Exercises/design-form.Rmd), une mesure invalide peut rendre difficile la distinction efficace des explications alternatives de la relation entre le traitement et les résultats.

 - Une mesure non fiable peut diminuer [la puissance statistique](statistical-power-and-design-diagnosands.html).
 
 - Une mesure difficile peut nécessiter une étude pilote centrée sur la mesure elle-même.

## Slides

Vous trouverez ci-dessous des slides avec le contenu de base de notre conférence sur la mesure. Vous pouvez les utiliser directement ou les copier localement avant de les éditer.

 - [Code source en R Markdown](https://egap.github.io/learningdays-resources/Slides/measurement-slides.Rmd)

 - [Version PDF](https://egap.github.io/learningdays-resources/Slides/measurement-slides.pdf)

 - [Version HTML](https://egap.github.io/learningdays-resources/Slides/measurement-slides.html)

## Ressources

### Guide des méthodes EGAP

- Guide des méthodes EGAP [10 choses à savoir sur la mesure dans les expériences](https://egap.org/resource/10-things-to-know-about-measurement-in-experiments/)

- Guide des méthodes EGAP [10 choses à savoir sur la conception de sondage](https://egap.org/resource/10-things-to-know-about-survey-design/)

- Guide des méthodes EGAP [10 choses à savoir sur l'implémentation de sondage](https://egap.org/resource/10-things-to-know-about-survey-implementation/)

### Livres, chapitres et articles

 - [@adcocoll:2001]

 - [@scacco_can_2018]
 
 - [@shadish2002experimental]

 - [@vicente_is_2014]

### Notes d'orientation des politiques publiques EGAP

*Grâce à des données d'enquête à plusieurs échelles*

 - [Note d'orientation des politiques publiques EGAP 58 : La responsabilisation bottom-up fonctionne-t-elle ?](https://egap.org/resource/does-bottom-up-accountability-work-evidence-from-uganda/)

*Grâce aux sms*

 - [Note d'orientation des politiques publiques EGAP 27 : Technologies de l'information et de la communication et politiciens en Uganda](https://egap.org/resource/brief-27-ict-and-politicians-in-uganda/)

 - [Note d'orientation des politiques publiques EGAP 56 : Signaler la corruption au Nigéria](https://egap.org/resource/reporting-corruption-in-nigeria-testing-the-effects-of-norms-nudges/)

*Grâce aux données administratives*

 - [Note d'orientation des politiques publiques EGAP 16 : Effets de débordement des observateurs électoraux au Ghana](https://egap.org/resource/brief-16-spillover-effects-of-observers-in-ghana/)

 - [Note d'orientation des politiques publiques EGAP 67 : Administration électorale au Kenya](https://egap.org/resource/electoral-administration-in-kenya/)

<!--chapter:end:measurement.Rmd-->


# Menaces affectant la validité interne des expériences aléatoires {.tabset}

Les expériences randomisées peuvent se heurter à des problèmes qui compromettent leur capacité à démontrer les effets causaux, c'est-à-dire menacer leur validité interne.
Certaines unités peuvent être exclues des résultats et cette absence peut être due au traitement : soit les unités n'ont pas reçu le traitement qui leur était assigné ou elles ont subi des effets de débordement d'un voisin traité.

Dans ce module, nous abordons certaines menaces courantes et les bonnes pratiques pour les éviter ou les contourner.

## Contenu {.tabset}

 - Passez en revue les trois hypothèses de base discutées dans le module sur [l'inférence causale](causal-inference.html).

 - Nous avons dit "analysez en randomisant" dans le module sur les [estimandes et estimateurs](estimands-and-estimators.html). N'oubliez pas que vous avez randomisé **l'assignation** du traitement. Vous n'avez pas randomisé si le traitement est reçu, ni si une unité participe à la collecte de données.

 - **Les données manquantes dans les résultats (i.e. l'attrition)** sont particulièrement problématiques si le pattern des données absentes est causé par le traitement lui-même. C'est un problème très courant.

     - Ne supprimez pas les observations de votre analyse pour lesquelles il manque des données.

     - Vous pourriez **borner** les estimations des effets du traitement.

 - **Non-conformité**. L'effet de l'assignation du traitement n'est pas le même que l'effet du traitement reçu. Parfois, les unités ne se conformeront pas au choix de traitement qui leur a été assigné.

     - La conformité unilatérale signifie que certaines unités assignées au traitement ne prennent pas le traitement, et toutes les unités assignées au contrôle ne prennent pas le traitement.
     
     - L'effet moyen local du traitement (local average treamtent effect, LATE), aussi connu sous le nom d’effet causal moyen pour ceux qui se conforment au traitement (complier average causal effect, CACE), est l'effet moyen pour les unités qui prennent le traitement lorsqu'elles sont assignées au traitement. Si l'hypothèse de monotonie et la restriction d'exclusion sont remplies, il est possible d'estimer l'effet moyen local du traitement en cas de non-conformité.

 - **Les "effets de débordement" ou les interférences entre unités** constituent une violation de l'une des hypothèses fondamentales de l'[inférence causale](causalinference.html).

      - Cependant, cela peut ne pas être un problème si vous êtes intéressé par les effets de débordement et/ou si vous avez conçu votre recherche en le prenant tenant en compte.

 - **L'effet Hawthorne** se produit lorsque les sujets se comportent différemment parce qu'ils sont observés.

- **La non-exclusion**. Traiter différemment les unités des groupes de traitement et de contrôle, par exemple avec des processus de collecte de données différents ou une attention particulière pour les unités traitées, peut perturber l'interprétation des résultats expérimentaux.

     - Si l'effet Hawthorne est présent pour le groupe de traitement mais pas pour le groupe de contrôle, il y a une violation de l'hypothèse d'exclusion.



## Slides

Vous trouverez ci-dessous des slides avec le contenu de base de notre conférence sur les menaces à la validité interne des expériences aléatoires. Vous pouvez les utiliser directement ou les copier localement avant de les éditer.

 - [Code source en R Markdown](https://egap.github.io/learningdays-resources/Slides/threats-slides.Rmd)

 - [Version PDF](https://egap.github.io/learningdays-resources/Slides/threats-slides.pdf)

 - [Version HTML](https://egap.github.io/learningdays-resources/Slides/threats-slides.html)

Vous pouvez également voir les slides utilisées lors des précédentes journées d'apprentissage du réseau EGAP :

- [Présentation des menaces aux journées d'apprentissage du réseau EGAP à l'African School of Economics, Abomey-Calavi, juin 2019 (la première section passe en revue les différentes conceptions de randomisation)](https://egap.github.io/learningdays-resources/Slides/Examples/threats-benin.pdf)

- [Présentation sur l'attrition et les données manquantes aux journées d'apprentissage du réseau EGAP à l'Universidad Diego Portales à Santiago, Chili, mai 2016](https://egap.github.io/learningdays-resources/Slides/Examples/threats-santiago.pdf)

## Ressources

### Guide des méthodes EGAP

- Guide des méthodes EGAP [10 choses à savoir sur les données manquantes](https://egap.org/resource/10-things-to-know-about-missing-data/)

- Guide des méthodes EGAP [Les 10 types d'effets de traitement à connaître](https://egap.org/resource/10-types-of-treatment-effect-you-should-know-about/)

- Guide des méthodes EGAP [10 choses à savoir sur l'effet moyen local du traitement](https://egap.org/resource/10-things-to-know-about-the-local-average-treatment-effect/)

### Livres, chapitres et articles

- [Procédures opérationnelles standard pour le laboratoire de Don Green à l'Université de Columbia](https://github.com/acoppock/Green-Lab-SOP). Un ensemble complet de procédures et de règles de base pour mener des études expérimentales.
- [@gerber_field_2012]. Chapitres 5 à 8 traitent de non-conformité, d'attrition et d'interférence.

### Note d'orientation des politiques publiques EGAP

- [Note d'orientation EGAP 11 : Observateurs électoraux et fraude au Ghana ](https://egap.org/resource/brief-11-election-observers-and-fraud-in-ghana/)

- [Note d'orientation EGAP 16 : Effets de débordement des observateurs électoraux au Ghana](https://egap.org/resource/brief-16-spillover-effects-of-observers-in-ghana/)

<!--chapter:end:threats.Rmd-->


# Considérations éthiques {.tabset}

*Une expérience aléatoire implique qu'un groupe d'humains change la vie d'un autre groupe d'humains.* Ceux qui travaillent pour le gouvernement le font naturellement --- leur travail même est de fournir à leur peuple de la nourriture, un abri, la sécurité, la justice, etc.
Les universitaires, dont les travaux n'ont généralement pas d'impacts immédiats sur le public, doivent également se rappeler d'examiner attentivement comment leurs recherches pourraient changer la vie des personnes exposées à l'intervention, ainsi que de celles qui ne l'ont pas été. Lorsqu'une personne influence la vie d'une autre, l'influenceur a la responsabilité de ne pas nuire à la personne influencée.

Ce module traite des sujets de base sur l'éthique de la recherche, tels que le respect de la vie privée et l'autonomie ; les principes de base comme le respect des personnes, la bienveillance et la justice ; et comment le consentement éclairé aide à communiquer ces principes aux participants de l'étude.

## Contenu

 - La recherche doit peser les **bénéfices potentiels** des connaissances à tirer de la recherche par rapport aux **dommages potentiels** qu'elle peut causer aux sujets humains.

 - Que ressentiriez-vous si vous étiez un sujet de recherche dans votre étude ? Dans le groupe de contrôle ? Dans le groupe de traitement ? Un membre de statut relativement élevé dans la communauté ? Un membre de statut relativement bas dans la communauté ?

 - Principes clés : **resepect de la vie privée** et **autonomie**.

 - Principes de base du rapport Belmont : **respect des personnes, bienveillance, justice**.

 - **Consentement éclairé** : Pouvez-vous garantir que les sujets de recherche ont la liberté de refuser de participer et/ou d'abandonner l'étude s'ils le souhaitent ? Pouvez-vous vous assurer que les sujets de recherche peuvent signaler les problèmes qui pourraient survenir ?

 - Défis de la recherche expérimentale en sciences sociales en général :

    - Beaucoup plus de personnes peuvent profiter (ou souffrir) de votre intervention que ceux participant directement à votre étude

    - Modifier les résultats des élections ou changer la corruption peuvent entraîner de grands changements sociétaux. Est-ce aller au-delà du domaine de la recherche ?

## Slides

Vous trouverez ci-dessous des slides avec le contenu de base pour cette section.

 - [Code source en R Markdown](https://egap.github.io/learningdays-resources/Slides/ethics-slides.Rmd)

 - [Version PDF](https://egap.github.io/learningdays-resources/Slides/ethics-slides.pdf)

 - [Version HTML](https://egap.github.io/learningdays-resources/Slides/ethics-slides.html)

## Ressources

- [Principes de recherche et travaux sur l'éthique de EGAP](https://egap.org/ethics/)

- [Principes et lignes directrices pour la recherche sur des sujets humains de APSA](https://connect.apsanet.org/hsr/principles-and-guidance/)

- [Le rapport Belmont](https://www.hhs.gov/ohrp/regulations-and-policy/belmont-report/index.html)

- [Les comités de revue éthique institutionnels aux USA](https://www.youtube.com/watch?v=U8fme1boEbE)

- [Exemple : Éthique de la recherche à l'Université d'Oxford au Royaume-Uni](https://researchsupport.admin.ox.ac.uk/governance/ethics)

- [Exemple : Éthique pour les chercheurs dans l'UE](https://ec.europa.eu/research/participants/data/ref/fp7/89888/ethics-for-researchers_en.pdf)

- [Exemple : Éthique de la recherche à l'Université catholique du Chile](http://eticayseguridad.uc.cl/)

### Livres, chapitres et articles

- [@Asieduetal2021ethics]

- [@Evans2021ethics] <!--[pdf](https://www.cgdev.org/sites/default/files/WP565-Evans-Ethical-issues-and-RCTs.pdf) -->

### Articles et plans de pré-analyse

Exemples de plans de pré-analyse et d'articles sur les considérations éthiques :

- [Plan de pré-analyse : les effets des bons non-alimentaires dans un contexte humanitaire, le cas du programme de réponse rapide aux mouvements de population au Congo](https://osf.io/eutx7/)

- [Article : Appendix E.1 Lutter contre la violence à l'égard des femmes en encourageant la dénonciation : une expérience dans les médias de masse en Ouganda rural](http://jasper-cooper.com/papers/Green_et_al.pdf)

<!--chapter:end:ethics.Rmd-->


\cleardoublepage 

# (APPENDIX) Appendix {-}

# Glossaire des termes{.tabset}

Ci-dessous voici les termes principaux, fréquemment utilisés dans le livre et plus généralement quand on parle d'expériences de terrain aléatoires.

## Concepts clés

Voir le module sur [l'inférence causale](causal-inference.html), [les estimandes et estimateurs](estimands-and-estimators.html).

- **Résultat potentiel $Y_i(T)$** Le résultat $Y$ que l'unité $i$ *aurait* sous la condition de traitement $T$. Ceux-ci sont considérés comme des quantités fixes pour un moment précis.
  $T$ peut être 0 pour le contrôle ou 1 pour le traitement s'il n'y a qu'un seul type de traitement. Voir le module sur [l'inférence causale](causal-inference.html).

- **Effet du traitement $\tau_i$ pour l'unité $i$** Le contraste entre les résultats potentiels sous les deux conditions de traitement pour l'unité $i$.
  L'effet du traitement est généralement défini comme la différence entre les résultats potentiels sous traitement et sous contrôle, $Y_i(1)-Y_i(0)$.
  Voir le module sur [l'inférence causale](causal-inference.html).

- **Problème fondamental de l'inférence causale** dans le cadre contrefactuel. On ne peut pas observer à la fois $Y_i(1)$ et $Y_i(0)$ pour une unité donnée, donc on ne peut pas obtenir $\tau_i$ directement.
  Voir le module sur [l'inférence causale](causal-inference.html).

- **Estimande** Ce que vous visez à estimer. Un exemple d'un estimande est l'effet moyen du traitement.
  Dans l'inférence causale contrefactuelle, l'effet moyen du traitement est fonction des résultats potentiels, et non des résultats observés.
  Voir le module sur les [estimandes et estimateurs](estimands-and-estimators.html).

- **Estimateur** Comment on devine la valeur de l'estimande à partir des données dont on dispose (les données observées).
  Un exemple d'estimateur est la différence des moyennes. Voir le module sur les [estimandes et estimateurs](estimands-and-estimators.html).

- **Effet moyen du traitement (Average treatment effect, ATE)** La moyenne de l'effet du traitement pour tous les individus de votre groupe de sujets.
  C'est un type d'**estimande**. Si on définit $\tau_i$ comme étant $Y_i(1)-Y_i(0)$, alors l'effet moyen du traitement est $\overline{Y_i(1)-Y_i(0)}$, ce qui équivaut aussi à $\overline{{Y}_i(1)}-\overline{{Y}_i(0)}$.
  Notez qu'on n'utilise pas le style de notation $E[Y_i (1)]$ ici parce que $E[]$ signifie "moyenne sur des opérations répétées," quand $\overline{Y}$ signifie "moyenne sur un ensemble d'observations".
  Voir le module sur [l'inférence causale](causal-inference.html) et le module sur les [estimandes et estimateurs](estimands-and-estimators.html).

- **Échantillonnage aléatoire** Sélection de sujets dans une population avec des probabilités connues strictement comprises entre 0 et 1.

- **Une experience avec $k$ bras de traitement** Une experience qui comprend $k$ conditions de traitement
  (y compris le contrôle). Voir le module sur [la randomisation](randomization.html).

- **Assignation aléatoire** Assignation des sujets à des conditions expérimentales avec des probabilités connues strictement comprises entre 0 et 1.
  Cela équivaut à un échantillonnage aléatoire sans remise à partir des résultats potentiels.
  Il existe plusieurs stratégies d'assignation aléatoire : simple, complète, par grappe (cluster), par bloc, ou une combinaison de blocs et grappes.
  Voir le module sur [la randomisation](randomization.html).

- **Validité externe** Les résultats de votre étude vous renseignent sur des contextes en dehors de votre échantillon --- dans d'autres endroits ou pour d'autres interventions.

## Inférence statistique

Voir les modules sur [les tests d'hypothèses](hypothesis-testing.html) et [la puissance statistique](statistical-power-and-design-diagnosands.html).

- **Hypothèse** Une affirmation simple, claire et falsifiable sur le monde.
  Dans l'inférence causale contrefactuelle, une hypothèse est une déclaration sur une relation pour les résultats potentiels,
  comme $H_0: Y_i(T_i=0) = Y_i(T_i=1) + \tau_i$ pour l'hypothèse que le résultat potentiel sous traitement est le résultat potentiel sous contrôle plus un certain effet pour chaque unité $i$.
  Voir le module sur [les tests d'hypothèses](hypothesis-testing.html).

- **Hypothèse nulle**  Une conjecture sur le monde que vous pouvez rejeter après avoir vu les données.
  Voir le module sur [les tests d'hypothèses](hypothesis-testing.html).

- **Hypothèse nulle stricte d'absence d'effet** L'hypothèse nulle selon laquelle il n'y a aucun effet du traitement pour aucun sujet.
  Cela signifie $Y_i(1)=Y_i(0)$ pour tout $i$. On pourrait écrire ceci comme $H_0: Y_i(T_i=0) = Y_i(T_i=1)$.
  Voir le module sur [les tests d'hypothèses](hypothesis-testing.html).

- **$p$-valeur** La probabilité de voir une statistique de test aussi grande (en valeur absolue) ou plus grande que la statistique de test calculée à partir des données observées.
  Voir le module sur [les tests d'hypothèses](hypothesis-testing.html).

- **Test unilatéral ou bilatéral** Lorsque vous vous attendez fortement à ce que l'effet soit positif ou négatif, vous pouvez effectuer un test unilatéral.
   Lorsque vous n'avez pas d'attente, effectuez un test bilatéral. Un test unilatéral a plus de puissance qu'un test bilatéral pour la même expérience.
   Voir le module sur [les tests d'hypothèses](hypothesis-testing.html).

- **Écart type** Racine carrée de l'écart quadratique moyen par rapport à la moyenne d'une variable. C'est une mesure de la dispersion d'une statistique.
  $SD_x=\sqrt{\frac{1}{n}\sum_{i=1}^n(x_i-\bar{x})^2}$

- **Taux de faux positifs/Erreur de type I d'un test** Un test d'hypothèse qui fonctionne bien rejette une hypothèse concernant un véritable effet causal pas plus de $\alpha$ % du temps.
  Le taux de faux positifs est le taux pour lequel le test met en doute une hypothèse qui est en réalité vraie.
  C'est le taux pour lequel le test incitera l'analyste à dire "statistiquement significatif" alors qu'en fait, il n'y a pas de relation causale.
  Voir le module sur [les tests d'hypothèses](hypothesis-testing.html).

- **Distribution d'échantillonnage** La distribution des estimations (par exemple, les estimations de l'ATE) pour toutes les assignations de traitement possibles.
  Pour l'inférence statistique basée sur la conception des expériences randomisées, la distribution des estimations d'un estimateur est générée à partir d'une randomisation.
  Beaucoup appellent cela une "distribution d'échantillonnage" parce que les manuels utilisent souvent l'idée d'échantillons répétés d'une population plutôt que de randomisations répétées pour décrire ce type de variation.

- **Erreur type** L'écart type de la distribution d'échantillonnage. Une erreur type plus élevée signifie que nos estimations sont plus sensibles aux variations d'échantillonnage.
  Voir le module sur les [estimandes et estimateurs](estimands-and-estimateurs.html).

- **Couverture d'un intervalle de confiance** Un intervalle de confiance qui fonctionne bien contient le véritable effet causal $100 ( 1 - \alpha)$ % du temps.
  Un intervalle de confiance a une *couverture incorrecte* lorsqu'il exclut le vrai paramètre moins de $100 (1 - \alpha)$ % du temps.
  Par exemple, un intervalle de confiance à 95 % est censé exclure le vrai paramètre seulement moins de 5 % du temps.

- **Puissance statistique d'un test** Probabilité qu'un test d'effet causal détectera un effet de traitement statistiquement significatif si l'effet existe.
  Voir le module sur la [puissance statistique](statistical-power-and-design-diagnosands.html).
  Cela dépend :
    - du nombre d'observations dans chaque bras de l'expérience
    - de la taille de l'effet (généralement mesuré en unités standardisées)
    - du bruit sur la variable de résultat
    - le niveau de signification ($\alpha$, par convention)
    - d'autres facteurs, y compris la proportion de vos unités qui sont assignées à différentes conditions de traitement.

- **Corrélation intra-grappe** (intra-cluster correlation, ICC) Dans quelle mesure les résultats potentiels des unités sont corrélés au sein des grappes par rapport à l'ensemble des grappes. Une corrélation intra-grappe plus élevée nuit à la puissance.

- **Non biaisé** Un estimateur est sans biais si vous *attendez* qu'il renvoie le bon résultat. Cela signifie que si vous deviez exécuter l'expérience plusieurs fois,
  l'estimation peut parfois être trop élevée ou trop faible, mais elle sera correcte en moyenne. Voir le module sur les [estimandes et estimateurs](estimands-and-estimateurs.html).

- **Biais** Le biais est la différence entre la valeur moyenne de l'estimateur sur l'ensemble de sa distribution d'échantillonnage et la valeur fixe unique de l'estimande.
  Voir le module sur les [estimandes et estimateurs](estimands-and-estimateurs.html).

- **Cohérence d'un estimateur** Un estimateur qui produit des réponses qui se rapprochent de plus en plus de la vraie valeur de l'estimande à mesure que la taille de l'échantillon augmente est un *estimateur cohérent* de cette estimande. Un estimateur cohérent peut être sans biais ou non.
  Voir le module sur les [estimandes et estimateurs](estimands-and-estimateurs.html).

- **Précision/efficacité d'un estimateur** La variation ou la largeur de la distribution d'échantillonnage d'un estimateur. Voir le module sur les [estimandes et estimateurs](estimands-and-estimateurs.html).

## Stratégies de randomisation

Voir le module sur [la randomisation](randomization.html).

- **Simple** Un tirage au sort indépendant pour chaque unité. Vous n'êtes pas assuré que votre expérience aura un nombre spécifique d'unités traitées.

- **Complète** Assigner $m$ sur $N$ unités au traitement. Vous savez combien d'unités seront traitées dans votre expérience et chaque unité a une probabilité de $m/N$ d'être traitée. Le nombre de façons dont le traitement peut être assigné (i.e. nombre de permutations d'assignation de traitement) est $\frac{N!}{m!(N-m)!}$.

- **Bloc** Divisez d'abord l'échantillon en blocs, puis randomisez séparément dans chaque bloc. Un bloc est un ensemble d'unités au sein duquel vous effectuez une assignation aléatoire.

- **Grappe (Cluster)** Les grappes d'unités sont assignés de manière aléatoire à une condition de traitement. Une grappe est un ensemble d'unités qui sera toujours assigné au même statut de traitement.

- **Combinaison par grappe et par bloc** Premièrement formez les blocs (de grappe). Ensuite, dans chaque bloc, assignez de manière aléatoire les grappes à une condition de traitement en utilisant une randomisation complète.

## Conceptions factorielles

Voir le module sur [la randomisation](randomization.html).

- **Conception factorielle** Une conception avec plus d'un traitement, chaque traitement étant assigné indépendamment. La conception factorielle le plus simple est un 2 par 2.

- **Effet marginal conditionnel** L'effet du traitement, conditionnel au maintien de l'autre pour une valeur fixe.
  Par exemple: $Y_i(T_1=1|T_2=0)-Y_i(T_1=0|T_2=0)$ est l'effet marginal de $T_1$ conditionnel à $T_2=0$.

- **Effet marginal moyen** Effet principal de chaque traitement dans une conception factorielle.
  C'est la moyenne des effets marginaux conditionnels pour toutes les conditions de l'autre traitement, pondérée par la proportion de l'échantillon qui a été assignée à chaque condition.

- **Effet d'interaction** Dans une conception factorielle, nous pouvons également estimer les effets d'interaction.
    - Pas d'effet d'interaction : un traitement n'amplifie ni ne diminue l'effet de l'autre traitement.
    - Effet d'interaction multiplicatif : l'effet d'un traitement dépend de la condition d'assignation de l'unité à un autre traitment.
      Cela signifie qu'un traitement amplifie ou réduit l'effet de l'autre. L'effet de deux traitements ensemble n'est *pas* la somme de l'effet de chaque traitement.

## Menaces

Voir le module sur les [menaces](threats-to-internal-validity-of-randomized-experiments.html).

- **Effet Hawthorne** lorsqu'un sujet réagit différemment quand il est observé.

- **Effet de débordement** lorsqu'un sujet répond au statut de traitement d'un autre sujet.
   Exemple : ma santé dépend du statut de vaccination de mon voisin, ainsi que de mon statut.

- **Attrition** Lorsque les résultats pour certains sujets ne sont pas mesurés.
   Cela peut être causé, par exemple, par des personnes qui migrent, refusent de répondre aux enquêtes finales ou meurent.
   Ceci est particulièrement problématique pour l'inférence lorsque l'attrition est corrélée avec le statut du traitement.

- **Conformité** Le statut de traitement d'une unité correspond à la condition de traitement qui lui a été assignée.
   Exemple de non-conformité : une unité assignée au traitement ne le prend pas.
   Exemple de conformité : une unité assignée au contrôle ne prend pas de traitement.

- **Types de conformité** Il existe quatre types d'unités en termes de conformité :
     - **Conformistes** Unités qui prendraient un traitement si elles étaient assignées au traitement et qui ne seraient pas traitées si elles étaient assignées au contrôle.
     - **Toujours preneurs** Unités qui prendraient un traitement si elles étaient assignées au traitement et si elles étaient assignées au contrôle.
     - **Jamais preneurs** Unités qui ne seraient pas traitées si elles étaient assignées au traitement et si elles étaient assignées au contrôle.
     - **Non-conformistes** Unités qui ne seraient pas traitées si elles étaient assignées au traitement et qui prendraient un traitement si elles étaient assignées au contrôle.

- **Non-conformité unilatérale** L'expérience n'a que des sujets "conformistes" et *soit* des "toujours preneurs" ou des "jamais preneurs".
  Habituellement, nous pensons à la non-conformité unilatérale comme n'ayant que des sujets "jamais-preneurs" et "conformistes", ce qui signifie que l'effet moyen local du traitement est l'effet du traitement sur les unités traitées.

- **Non-conformité bilatérale** L'expérience peut avoir les quatre groupes latents.

- **Conception incitative** Une expérience qui randomise $T$ (assignation de traitement), et nous mesurons $D$ (si l'unité prend le traitement) et $Y$ (le résultat).
  On peut estimer l'effet d'intention de traiter (intent to treat effect, ITT), l'effet moyen local du traitement (Local average treatment effect, LATE) aussi connu sous le nom d'effet causal moyen pour ceux qui se conforment au traitement (complier average causal effect, CACE). Cela nécessite trois hypothèses.
     - **Monotonicité** Hypothèse qu'il n'y a pas de sujets non-conformistes ou bien pas de conformistes.
       Habituellement, nous supposons qu'il n'y a pas de non-conformistes, ce qui signifie que l'effet de l'assignation sur la prise du traitement est soit positif, soit nul mais pas négatif.
     - **Première étape** Hypothèse qu'il y a un effet de $T$ sur $D$.
     - **Restriction d'exclusion** Hypothèse selon laquelle $T$ affecte $Y$ uniquement à travers $D$. C'est généralement l'hypothèse la plus problématique.

- **Effet d'intention de traiter (intent to treat effect, ITT)** L'effet de $T$ (assignation de traitement) sur $Y$.

- **Effet moyen local du traitement (Local average treatment effect, LATE)** L'effet de $D$ (prise de traitement) sur $Y$ pour les conformistes.
  Également connu sous le nom d'effet causal moyen pour ceux qui se conforment au traitement (complier average causal effect, CACE).
  Si l'hypothèse de monotonie et la restriction d'exclusion sont remplies, le LATE est égal à l'ITT divisé par la proportion conformiste de votre échantillon.

- **Expérience aval** Une étude de conception incitative qui profite de la randomisation de $T$ d'une étude précédente.
  Le résultat de cette étude précédente est le $D$ dans l'expérience aval.

<!--chapter:end:glossary.Rmd-->


# Introduction à R et RStudio {.tabset}

Tout au long du livre, nous incluons du code R pour l'estimation, la simulation et la création d'exemples. Nous avons utilisé RStudio pour créer les slides. Pour les personnaliser à vos propres fins, nous supposons que vous utiliserez R Markdown. Ci-dessous, voici les guides pour configurer R et RStudio sur votre ordinateur, ainsi que quelques commandes de base fréquemment utilisées.

## R et RStudio

R est un environnement logiciel libre utilisé couramment pour l'analyse statistique et le calcul. Étant donné que les participants aux journées d'apprentissage arrivent avec un bagage statistique et des outils différents, nous utilisons R pour nous assurer que tout le monde se comprend. Nous recommendons l'utilisation de R de manière générale pour sa flexibilité, sa richesse et son support complet, principalement via des forums en ligne.

RStudio est un environnement de développement intégré gratuit et open source avec une interface utilisateur qui rend R beaucoup plus convivial. R Markdown est une fonctionnalité de RStudio qui permet de présenter facilement du code, des résultats et du texte au format .pdf, .html ou .doc.

## Télécharger R et RStudio

### Télécharger R

R est téléchargeable gratuitement sur CRAN. Cliquer sur le lien correspondant à votre système d'exploitation :

- Pour **Windows** : [https://cran.r-project.org/bin/windows/base/](https://cran.r-project.org/bin/windows/base/)
- Pour **Mac OS X** : [https://cran.r-project.org/bin/macosx/](https://cran.r-project.org/bin/macosx/).
    - Sélectionner `R-4.0.4.pkg` pour OS X 10.13 et plus.
    - Sélectionner `R-3.6.3.nnpkg` pour OS X 10.11-10.12.
    - Sélectionner `R-3.3.3.nnpkg` pour OS X 10.19-10.10.
    - Sélectionner `R-3.2.1-snowleopard.pkg` pour OS X 10.6-10.8.

### Télécharger RStudio

RStudio peut être téléchargé gratuitement sur le site Web de RStudio, [https://www.rstudio.com/products/rstudio/download/](https://www.rstudio.com/products/rstudio/download/). Dans le tableau, cliquez sur le bouton bleu "Download" en haut de la colonne de gauche, "Licence Open Source RStudio Desktop", comme illustré ci-dessous dans la figure B.1. Après avoir cliqué, vous verrez une liste d'options de téléchargement, comme illustré à la Figure B.2.


- Pour **Windows**, sélectionner `Windows 10/8/7`.
- Pour **Mac OS X**, sélectionner `Mac OS X 10.13+`.


\begin{figure}
\includegraphics[width=0.8\linewidth]{C:/Data_Perso/theory_and_practice_of_field_experiments_french/Book/Images/new_rstudio} \caption{Sélectionner "Download" dans la colonne "RStudio Desktop Open Source License".}(\#fig:rstudiopng)
\end{figure}

\begin{figure}
\includegraphics[width=0.8\linewidth]{Images/rstudio_download} \caption{Sélectionner le lien "Windows 10/8/7" pour Windows ou "Mac OS X 10.13+" pour Mac.}(\#fig:rstudiodownload)
\end{figure}

## L'interface RStudio

Lorsque vous ouvrez RStudio pour la première fois, trois fenêtres doivent être visibles, comme illustré dans la Figure B.3 ci-dessous.

- Console (à gauche)
- Accounting (en haut à droite) : cela inclue les onglets Environment et History
- Miscellaneous (en bas à droite)

\begin{figure}
\includegraphics[width=0.8\linewidth]{Images/rstudio_intro} \caption{Lorsque vous ouvrez RStudio, il y a trois fenêtres visibles : la Console (à gauche), Accounting (en haut à droite), et Miscellaneous (en bas à droite).}(\#fig:rstudiointro)
\end{figure}

### La console

Vous pouvez exécuter toutes les opérations dans la console. Par exemple, si vous saisissez `4 + 4` et appuyez sur la touche Enter, la console renvoie `[1] 8`.

Pour s'assurer que tout le monde est prêt à utiliser R lors des journées d'apprentissage, nous demandons aux participants d'exécuter une ligne de code dans la console pour télécharger plusieurs packages R. Les packages sont des fragments de code reproducibles qui permettent une analyse plus efficace dans R. Pour exécuter ce bout de code, copiez-le dans la console et appuyez sur votre touche `Enter`. Vous devez être connecté à internet pour télécharger des packages.


```r
install.packages(c(
  "ggplot2", "dplyr", "AER", "arm", "MASS", "sandwich",
  "lmtest", "estimatr", "coin", "randomizr", "DeclareDesign"
))
```

Si le téléchargement est réussi, votre console ressemblera à la figure B.4, sauf que les URL seront différentes en fonction de votre emplacement.

\begin{figure}
\includegraphics[width=0.4\linewidth]{Images/console2a} \caption{La console après avoir exécuté les trois lignes de code répertoriées ci-dessus.}(\#fig:console2)
\end{figure}

### L'éditeur

Afin d'écrire et sauvegarder du code reproductible, nous allons ouvrir une quatrième fenêtre, l'éditeur, en cliquant sur l'icône avec une page blanche et un signe plus, dans le coin supérieur gauche de l'interface RStudio et en sélectionnant `R Script`, comme illustré à la figure B.5.

\begin{figure}
\includegraphics[width=0.6\linewidth]{Images/new_script} \caption{Créez un nouveau script R et ouvrez la fenêtre `éditeur` en sélectionnant `R Script` dans le menu déroulant.}(\#fig:newscript)
\end{figure}

Une fois le script R ouvert, il devrait y avoir quatre fenêtres dans l'interface RStudio, maintenant avec l'ajout de la fenêtre Éditeur. Nous pouvons exécuter une arithmétique simple en entrant une formule dans l'éditeur et en appuyant sur `Ctrl + Entrée` (Windows) ou `Commande + Entrée` (Mac). La formule et la "réponse" apparaîtront dans la console, comme illustré à la Figure B.6.

\begin{figure}
\includegraphics[width=0.6\linewidth]{Images/first_addition} \caption{Une expression arithmétique est saisie dans l'éditeur et évaluée dans la console. Les cases rouges sont ajoutées pour une visibilité accrue.}(\#fig:firstaddition)
\end{figure}

R peut être utilisé pour toute opération arithmétique, y compris, mais sans s'y limiter, l'addition (`+`), la soustraction (`-`), la multiplication scalaire (`*`), la division (`/`) et l'exponentielle (`^` ).

### Accounting

Au-delà des fonctions de base, nous pouvons également stocker des valeurs, des données et des fonctions dans l'environnement global. Pour affecter une valeur à une variable, utilisez l'opérateur `<-`. Toutes les valeurs, fonctions et données stockées apparaîtront dans l'onglet Environment de la fenêtre Accounting. Dans la Figure B.7, nous affectons la valeur $3 \times \frac{6}{14}$ à la variable `t`, et pouvons voir qu'elle est stockée sous Values.

Nous chargeons également un jeu de données. Ici, "ChickWeight" est un dataset intégré à R ; la plupart des datasets seront chargés à partir du Web ou d'autres fichiers sur votre ordinateur via une autre méthode. Nous pouvons voir que ChickWeight contient 578 observations de 4 variables et est stocké dans l'onglet Environment. En cliquant sur le nom ChickWeight, un onglet s'ouvrira avec le dataset dans la fenêtre de votre éditeur.

\begin{figure}
\includegraphics[width=0.6\linewidth]{Images/save_data} \caption{La valeur 3 * (6/14) est affectée à la variable t (en rouge) et le dataset ChickWeight est ajouté à l'environnement global (en bleu).}(\#fig:savedata)
\end{figure}

Les ateliers des journées d'apprentissage utilisent de nombreux outils dans R pour analyser et visualiser les données. Pour l'instant, nous pouvons apprendre quelques outils de base pour examiner les données. La fonction `head()` nous permet de voir les six premières lignes des données. `summary()` résume chacune des colonnes du dataset et `dim()` fournit les dimensions du dataset avec d'abord le nombre de lignes puis de colonnes.


```r
head(ChickWeight) # Les 6 premières observations du dataset
```

```
  weight Time Chick Diet
1     42    0     1    1
2     51    2     1    1
3     59    4     1    1
4     64    6     1    1
5     76    8     1    1
6     93   10     1    1
```

```r
summary(ChickWeight) # Résumé de toutes les variables
```

```
     weight         Time          Chick     Diet   
 Min.   : 35   Min.   : 0.0   13     : 12   1:220  
 1st Qu.: 63   1st Qu.: 4.0   9      : 12   2:120  
 Median :103   Median :10.0   20     : 12   3:120  
 Mean   :122   Mean   :10.7   10     : 12   4:118  
 3rd Qu.:164   3rd Qu.:16.0   17     : 12          
 Max.   :373   Max.   :21.0   19     : 12          
                              (Other):506          
```

```r
dim(ChickWeight) # Dimensions du dataset dans l'ordre "ligne" puis "colonne"
```

```
[1] 578   4
```

Contrairement à d'autres logiciels statistiques, R permet aux utilisateurs de stocker simultanément plusieurs ensembles de données, éventuellement de dimensions différentes. Cette fonctionnalité rend R assez flexible pour l'analyse à l'aide de plusieurs méthodes.

### Divers

R fournit une suite d'outils, allant des fonctions intégrées aux packages pour tracer graphiques, modèles, estimations, etc. La dernière fenêtre Divers permet une visualisation rapide des graphiques dans RStudio. La Figure B.8 montre une courbe dans cette fenêtre. Pendant les Leaning Days, on discutera de la manière de représenter les données.

\begin{figure}
\includegraphics[width=0.6\linewidth]{Images/graph} \caption{Un exemple de courbe avec le dataset `ChickWeight` en R.}(\#fig:graph)
\end{figure}

## Apprendre à utiliser R

### Ressources en ligne

Il existe de nombreuses ressources en ligne utiles pour vous aider à commencer avec R. Nous vous recommandons deux sources :

- Code School, qui fonctionne entièrement sur votre navigateur [https://www.codeschool.com/courses/try-r](https://www.codeschool.com/courses/try-r).
- Coursera, via un cours de programmation R en ligne organisé par l'Université Johns Hopkins :
    i. Allez sur [https://www.coursera.org](https://www.coursera.org)
    ii. Créez un compte (c'est gratuit !)
    iii. Inscrivez-vous pour "R Programming at Johns Hopkins University" (instructeur : Roger Peng) sous la rubrique "Cours"
    iv. Lisez les documents et regardez les vidéos de la première semaine. Les vidéos de la première semaine durent environ 2 heures 30 au total.
    
### Exercise de base

Voici quelques fragments de code pour vous familiariser avec certaines pratiques de base de R. Nous vous recommandons de vous entraîner en tapant les fragments de code dans votre éditeur, puis en les évaluant.

#### Configuration d'une session R

En général, nous lisons d'autres fichiers tels que des données ou des fonctions dans R et publions des résultats tels que des graphiques ou des tableaux dans des fichiers en dehors de la session R. Pour ce faire, nous devons donner à R une "adresse" où il peut localiser de tels fichiers. Il peut être plus efficace de le faire en définissant un répertoire de travail, i.e. un chemin d'accès au répertoire dans lequel les fichiers pertinents sont stockés. Nous pouvons identifier le répertoire de travail actuel en utilisant `getwd()` et le définir en utilisant `setwd()`. Notez que la syntaxe de ces chemins de fichiers varie selon le système d'exploitation.


```r
getwd()
```


```r
setwd("~TaraLyn/EGAP Learning Days Admin/Workshop 2018_2 (Uruguay)/")
```

Vous devrez peut-être installer des packages autres que ceux répertoriés ci-dessus pour exécuter certaines fonctions. Pour installer les packages, nous utilisons `install.packages("")`, en remplissant le nom du package entre les marques "", comme suit. Vous n'avez besoin d'installer les packages qu'une seule fois.


```r
install.packages("randomizr")
```

Une fois qu'un package est installé, il peut être chargé et accessible en utilisant `library()` où le nom du package est inséré entre parenthèses (sans guillemets).


```r
library(randomizr)
```

Pour effacer de la mémoire de R, les données, fonctions ou valeurs stockées qui apparaissent dans l'onglet de comptabilité, utilisez `rm(list = ls())`. Il peut être utile de définir un nombre aléatoire pour garantir que la réplication est possible dans une session R différente, en particulier lorsque nous travaillons avec des méthodes basées sur la simulation.


```r
rm(list = ls())
set.seed(2018) # pour la reproductibilité
```

#### Les basiques

Nous allons maintenant explorer quelques commandes de base. Afin d'affecter un scalaire (i.e. un élément unique) à une variable, nous utilisons la commande `<-` comme discuté précédemment :


```r
# "<-"  est la commande d'affectation ; ça sert à définir les choses. eg :
(a <- 5)
```

```
[1] 5
```

Nous pouvons également vouloir affecter un vecteur d'éléments à une variable. Ici, nous utilisons la même commande `<-`, mais nous nous concentrons sur la façon de créer le vecteur.


```r
# ":"  est utilisé pour définir une chaîne d'entiers
(b <- 1:10)
```

```
 [1]  1  2  3  4  5  6  7  8  9 10
```

```r
# utilisez c() pour faire un vecteur avec n'importe quoi dedans
(v <- c(1, 3, 2, 4, pi))
```

```
[1] 1.000 3.000 2.000 4.000 3.142
```

On peut alors se référer aux éléments d'un vecteur en désignant leur position à l'intérieur de parenthèses `[]`.


```r
# Extrait les éléments d'un vecteur :
b[1] # Retourne la position 1
```

```
[1] 1
```

```r
b[5:4] # Retourne les positions 5 et 4, dans cet ordre
```

```
[1] 5 4
```

```r
b[-1] # Retourne tout sauf le premier élément
```

```
[1]  2  3  4  5  6  7  8  9 10
```

```r
# Retourne tous les nombres indiqués comme "TRUE"
b[c(TRUE, FALSE, TRUE, FALSE, FALSE, TRUE, TRUE, FALSE, FALSE, FALSE)]
```

```
[1] 1 3 6 7
```

```r
# Attribue une nouvelle valeur à l'élément particulier d'un vecteur
b[5] <- 0
```

Il existe un ensemble de fonctions pré-existantes qui peuvent être appliquées à des vecteurs comme `b`.


```r
sum(b) # Somme de tous les éléments
```

```
[1] 50
```

```r
mean(b) # Moyenne de tous les éléments
```

```
[1] 5
```

```r
max(b) # Maximum de tous les éléments
```

```
[1] 10
```

```r
min(b) # Minimum de tous les éléments
```

```
[1] 0
```

```r
sd(b) # Écart type de tous les éléments
```

```
[1] 3.496
```

```r
var(b) # Variance de tous les éléments
```

```
[1] 12.22
```

On peut aussi appliquer des transformations arithmétiques à tous les éléments d'un vecteur :


```r
b^2 # Carré de la variable
```

```
 [1]   1   4   9  16   0  36  49  64  81 100
```

```r
b^.5 # Racine carré de la variable
```

```
 [1] 1.000 1.414 1.732 2.000 0.000 2.449 2.646 2.828 3.000 3.162
```

```r
log(b) # Log de la variable
```

```
 [1] 0.0000 0.6931 1.0986 1.3863   -Inf 1.7918 1.9459 2.0794 2.1972 2.3026
```

```r
exp(b) # Exponentielle de la variable
```

```
 [1]     2.718     7.389    20.086    54.598     1.000   403.429  1096.633  2980.958  8103.084 22026.466
```

Enfin, nous pouvons évaluer les affirmations logiques (c'est-à-dire "la condition X est-elle vraie ?") sur tous les éléments d'un vecteur :


```r
b == 2 # égal à
```

```
 [1] FALSE  TRUE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
```

```r
b < 5 # plus petit que
```

```
 [1]  TRUE  TRUE  TRUE  TRUE  TRUE FALSE FALSE FALSE FALSE FALSE
```

```r
b >= 5 # plus grand ou égal à
```

```
 [1] FALSE FALSE FALSE FALSE FALSE  TRUE  TRUE  TRUE  TRUE  TRUE
```

```r
b <= 5 | b / 4 == 2 # | signifie OU
```

```
 [1]  TRUE  TRUE  TRUE  TRUE  TRUE FALSE FALSE  TRUE FALSE FALSE
```

```r
b > 2 & b < 9 # & signifie ET
```

```
 [1] FALSE FALSE  TRUE  TRUE FALSE  TRUE  TRUE  TRUE FALSE FALSE
```

```r
is.na(b) # Indique si la donnée est manquante
```

```
 [1] FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
```

```r
# Donne les indices des éléments dont la valeur répond à la condition
which(b < 5)
```

```
[1] 1 2 3 4 5
```

La logique de base de ces commandes s'applique à des structures de données beaucoup plus complexes que les scalaires et les vecteurs. La compréhension de ces fonctionnalités de base vous aidera à mieux comprendre les sujets abordés au cours des journées d'apprentissage.

<!--chapter:end:intro_to_r.Rmd-->




<div id="refs"></div>

<!--chapter:end:references.Rmd-->

