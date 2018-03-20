---
layout: page
title: Aspects Techniques et Création de Chatbots
---

##Comment générer de tels chatbots ?

On peut séparer la technologie derrière les chatbots en deux grandes catégories. D’une part, le Machine Learning, et d’autre part l’informatiques plus classique, à base de règles fixées par le développeur.
Nous allons exposer les deux possibilités de séparément, pour ensuite voir que les meilleures solutions sont en fait basées sur un savant mélange de ses deux solutions.  

### Machine Learning

Un chatbot, finalement, c’est une sortie, en fonction d’une entrée :

- L’utilisateur envoie un message (*entrée*)
- Le chatbot répond par un autre message (*sortie*).

Pourquoi, dans ce cas, ne pass essayer d’utiliser un réseau de neurone, qui essaierait de prédire la sortie en fonction de l’entrée ?
Imaginez que vous extrayiez l’ensemble de vos messages de chats depuis plusieurs années : SMS, Facebook Messenger, WhatsApp, Telegram, Twitter, etc.. Peu importe la plateforme ! Pour chaque message que vous avez envoyé, vous établissez un couple `(entrée, sortie)` avec pour entrée, le message que vous avez reçu, et pour sortie le message par lequel vous avez répondu. Avec cette manipulation, on obtient finalement un jeu de donnée intéressant : entraînez un modèle sur ce jeu de données, et vous obtiendrez un bot capable de répondre à n’importe quel message en vous imitant !

Cet exemple est bien entendu grossièrement simplifié sur bien des aspects, et ne marcherait probablement pas très bien ! Il a le mérite, cependant, de présenter la démarche globale du Machine Learning appliquée aux chatbots, et de faire comprendre l’idée générale. Observons les avantages et inconvénients d’une telle technique :

##### Avantages :
-	Le développeur n’a pas besoin de pré-rentrer l’ensemble des réponses manuellement puisque les réponses sont générées automatiquement
-	Cette solution peu fonctionner dans des domaines très larges, et s’adapter à de nombreux jeux de données différents

##### Inconvénients :
-	Comme pour tous les modèles de réseaux de neurones, les connexions sont très obscures, et le développeur a peu de contrôle sur les réponses du chatbot
-	Cela nécessite d’avoir un jeu de données pour entraîner le modèle

### Chatbot à base de règles

La méthode aux antipodes de la précédente est de créer un chatbot à partir d’un nombre fini de règles, définies par le développeur. L’idée est d’identifier les éléments clé dans la requête de l’utilisateur puis de renvoyer une réponse prédéfinie qui dépend des paramètres tirés de la requête. Ainsi, si par exemple, vous cherchez à développer un chatbot qui donne la météo pour la date demandée par l’utilisateur il faudrait réussir à extraire la date demandée par l’utilisateur. Vous pourriez simplement rechercher, dans la demande de l’utilisateur, une liste de mots clés tels que « Demain », « Semaine prochaine », « Week-end », « Lundi », ou n’importe quel autre ancrage temporel. Une fois la date correspondante identifiée, vous pouvez faire une requête à l’API météo que vous utilisez, ce qui vous donnera , et de retourner une chaîne de caractères de la forme :

	`« Le [date-demandée] il fera [meteo-correspondante] ! [phrase-adaptée]. »`

Ainsi un résultat pourrait être :

	`« Quel temps fait-il lundi prochain ? »`

	`« Le lundi 24 Juin, il fera beau ! Ne vous couvrez pas trop ;) »`

Et voilà, le tour est joué ! Ce n’est pas très compliqué, finalement, n’est-ce pas ? Encore une fois, on sent vite les avantages et limitations d’une telle méthode :

##### Avantages :
-	Technique simple, sur le principe
-	Le développeur a une maîtrise totale sur les réponses du chatbot
-	Le résultat peu être très performant pour un but précis

##### Inconvénients :
-	Ne fonctionne généralement que pour des fonctionnalités très imitées
-	Ajouter une fonctionnalité demande systématiquement du travail supplémentaire, ne serait-ce que pour définir les réponses types
-	Le chatbot peut se faire piéger par des phrases alambiquées. Par exemple si l’utilisateur demande « Je veux savoir s’il neige demain, pour savoir si je vais skier après-demain » Faut-il donner la météo de demain ou de après-demain ?

Il est finalement assez simple d’imaginer des chatbots qui utilisent les deux technologies pour proposer une solution qui gardent le meilleur des deux mondes, et éliminent la plupart des inconvénients.

Prenons cependant le temps de présenter un exemple connu et intéressant : le phénomène Tay.ai par Microsoft :
En 2016, Microsoft a mis en ligne sur Twitter un bot, dénommé Tay, qui avait pour but de se comporter comme une adolescente et d’interagir avec les gens sur le réseau social. Il est important également de noter que Tay devait apprendre des interactions qu’elle avait avec les utilisateurs, l’idée étant qu’elle soit ainsi au fait de l’actualité, et puisse discuter de faits récents avec la Twittosphère.
Le résultat était assez impressionnant, d’une part par la vraisemblance du langage qu’elle utilisait : des expressions des grammaticalement incorrectes mais qui correspondaient très bien au langage des personnes de son « âge », et d’autre part par la diversité des conversations qu’elle pouvait avoir, et par la pertinence de ses réponses. Malheureusement, la Twittosphère s’est rapidement rendu compte que Tay était très influençable, et que l’on pouvait lui faire répéter des choses relativement facilement. Internet a donc pris un malin plaisir à lui faire dire n’importe quoi, et à pousser le bot à tweeter des choses allant de surprenantes, à vraiment pas politiquement correctes.

Cela peut faire sourire, mais il est intéressant d’analyser cet événement. On comprend bien que ce bot était principalement basé sur de l’intelligence artificielle, et devait avoir peu de règles qui régissaient ses réponses. On retrouve donc les avantages et les inconvénients décrits ci-dessus : un résultat et un langage très naturel, dans de nombreux domaines. Mais très peu de contrôle sur les réponses, ce qui peut engendrer des réponses déplacées. Finalement, il manquait à cette intelligence artificielle une notion des mots qu’elle utilisait, et la culture associée. Sans notion de racisme, sans connaissance de l’Histoire, elle ne pouvait pas savoir à quel point ses propos étaient déplacés !
