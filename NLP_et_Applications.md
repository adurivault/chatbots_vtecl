---
layout: page
title: NLP et Applications
---

Commençons par aborder les chatbots depuis un point de vue très large : le Natural Language Processing (NLP). Ce terme désigne l’ensemble des disciplines de l’informatique qui ont pour but d'étudier le langage tel qu’on le parle au quotidien.

## Une complexité insoupçonnée.

Plusieurs centaines de fois par jour, nous entendons ou lisons des phrases, puis en recréons mentalement pour y répondre. Cela nous semble d’une simplicité telle que nous n’y pensons même pas, et pourtant il est important de prendre conscience de la complexité du processus mental qui a lieu à chaque fois. Une version simplifiée de ce processus pourrait être résumée comme suit :
 - Reconnaître des syllabes au milieu d’un signal sonore, et les isoler
 - Assembler ces syllabes entre elles pour en faire des mots
 - Identifier le mot correct parmi l’ensemble des mots qui ont la même sonorité » (vers, verre, vert, etc.)
 - Assembler ces mots pour en faire des groupes de mots qui ont un sens collectif
 - Assembler ces groupes de mots pour en extraire des phrases
 - Comprendre comment ces groupes de mots s’organisent les uns aves les autres pour comprendre le sens global de la phrase

À chacune de ces étapes, on fait intervenir inconsciemment une grande quantité d’information sur le monde extérieur : notre connaissance des mots de la langue française, notre connaissance du monde pour faire un lien entre les mots et leur signification, ou encore le contexte de la phrase.
Si l’on souhaite reproduire ce processus de manière informatique, et attribuer une signification à une phrase donnée, le nombre de combinaisons est gigantesque, et il est bien entendu impossible de toutes les parcourir pour trouver la meilleure solution. Et puis après tout, même si on disposait d’un algorithme permettant de parcourir une sorte d’ensemble des significations possibles pour une phrase, cela serait inutile sans un critère pertinent pour les qualifier.

## Un exemple intéressant

L’exemple suivant met en évidence une des difficultés pour identifier le sens d’une phrase :

	`« Viens, on va manger, mamie.»`

	`« Viens, on va manger mamie.»`

Une virgule modifiée, et la phrase passe d’une simple proposition à une situation macabre. Cet exemple est lié à la ponctuation, mais de nombreux paramètres rendent l’interprétation d’une phrase extrêmement pour une machine. Lorsque nous interprétons, en tant qu’humain, la signification d’une phrase, nous intégrons sans nous en rendre compte l’ensemble des connaissances du monde, de la société, du contexte, que nous avons acquis jusqu’à cet instant. Cela nous permet de détecter l’ironie, le sarcasme, les phrases qui n’ont aucun sens, ou de faire la différence entre deux sens radicalement différents en fonction du contexte.
Vous commencez à prendre conscience de la difficulté et des écueils du NLP ? Finalement, pas la peine de rentrer plus dans les détails, je pense vous avoir convaincu de la complexité de ce domaine, et en particulier de la difficulté de créer une machine capable de comprendre le langage naturel, et encore plus d’interagir avec un humain.

## Mais alors, comment on fait ?
Les techniques pour traiter ce genre de problème sont très diverses, et vont d’un chatbot élémentaire se basant sur des règles simples pour choisir un réponse, à des systèmes d’une très grande complexité, comme la plateforme Watson d’IBM qui repose en grande partie sur des réseaux de neurones. J’aborde ce sujet plus en détails dans la section [Aspects Théoriques et Création de Chatbots](/Aspects_Techniques/), mais ici nous allons d’abord exposer certaines applications du NLP, avec un point de vu bien plus large que la seule application des chatbots.

## Applications [[1]](http://www.expertsystem.com/natural-language-processing-applications/)

### Traduction
La traduction automatique faite par des plateformes telles que Google Translate, est bien entendu une discipline du NLP. Des avancées spectaculaire ont été faite ces dernières années, en passant sur des technologies à base de réseaux de neurones.

### Génération de Langage nature
Ce domaine  a pour but de traduire des données brutes informatiques, sous la forme de phrases grammaticalement correctes et intelligibles par un être humain.

### Analyse de sentiments
Analyser les sentiments qui ressortent d’une phrase ou d’un texte, est un défi très complexe, mais qui permet de faire des choses très intéressantes. En analysant les tweets sur un sujet particulier, on peut par exemple sonder l’opinion publique à propos de ce sujet.

### Reconnaissance automatique de la parole
Les sous-titres générés automatiquement sur Youtube utilisent du NLP pour analyser la structure de la phrase et choisir la solution la plus probable pour la retranscrire sous forme écrite.

### Synthèse de la parole
Réciproquement, l’opération inverse de la reconnaissance automatique de la parole, est la transformation de texte en parole. Ce domaine utilise de s techniques de NLP pour prononcer les phrases avec une intonation correcte et intelligible. C’est ce genre de système que l’on retrouve derrière des systèmes comme Siri ou Google Assistant.
