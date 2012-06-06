Nicolas Perriault - Casper JS

Bonjour, wouh, salut tout le monde, je vais vous parler de Casper "jaïïïesse", CasperJS pour les francophones, qui est donc un petit toolkit de … alors qui permet de gérer le web au doigt et à l'oeil, voilà merci pour le spoil tout à l'heure, 

Voilà qui est basé sur PhantomJS, qui est une brique open-source qui est un navigateur, donc un navigateur web, en mode headless, c'est à dire qui se pilote sans interface graphique, en ligne de commande par exemple, pour être automatisé sur des systèmes, sur des serveurs qui n'ont pas d'écran, etc.

C'est basé sur WebKit donc désolé, c'est un peu toujours la monoculture mais on en discutera plus tard, dehors si vous voulez, qui est pilotable donc en ligne de commande, donc très pratique pour scripter, automatiser les choses et qui dispose d'une API  full javascript. 

Javascript on en entend beaucoup parler, un petit peu à tort et à travers, en tout cas à toutes les sauces, on a des gens qui font des trucs hallucinants en Javascript, parfois à tort, parfois à juste titre. 

En tout cas Phantom est un logiciel qui exploite uniquement une API Javascript. Donc voici un script Phantom, alors ouais j'suis pas sur qu'on voit grand chose, j'suis un petit peu navré. 

Voilà donc en gros cette API Javascript permet par exemple de créer un objet qui est une page web, d'ouvrir donc une URL, par exemple http://www.google.fr et une fois qu'on a reçu la réponse du serveur de Google avec le code HTML, on peut faire une certain nombre de choses, par exemple checker que tout s'est bien passé et qu'il n'y a pas eu d'erreur. Et ensuite faire des assertions, etc.

On lance le script et on obtient le résultat du script qui était d'afficher le contenu texte de la balise <title>. 

On peut faire des choses extrêmement complexes, donc là comme on voit rien, j'vais juste vous dire ce que ça fait très rapidement : ça va sur le site de http://sudweb.fr et ça récupère le programme dans un tableau d'objets JSON, tout simplement.

Donc vous voyez on pilote vraiment un navigateur web en ligne de commande et en utilisant des scripts Javascript tous bêtes, donc si vous faîtes du jQuery des choses comme ça, vous savez à priori coder en Javascript et faire ça. 

Mais on a un petit problème avec PhantomJS quand même , parce que c'est une super lib' mais comment on clique, comment on interagit avec la page, comment on enchaîne les interactions, simplement, facilement, et surtout comment on vérifie des trucs et éventuellement d'où vient le vent mais ça je n'y répondrai pas.

Un petit détour en Egypte avec … les pyramides de l'enfer. Qu'est-ce que c'est que les pyramides de l'enfer, c'est la gestion de la synchronicité en Javascript, je sais pas si vous avez … ça s'adresse surtout aux codeurs …  mais vous avez tous rencontré ça théoriquement à un moment ou à un autre, on a des fonctions qui passent en argument des callbacks, tout ça s'enchaîne, il faut attendre le résultat de l'appel précédent pour décider de ce qu'on fait ensuite.

Donc ça, ça fait des choses qui partent vers la droite, et tout ce qui part vers la droite n'est pas maintenable. (rires)

Alors … c'est là qu'arrive CasperJS (applaudissements) 

CasperJS va essayer de répondre à un certain nombre de problématiques qui sont posés par Phantom en terme d'ergonomie, d'utilisabilité du code, etc. et donc c'est bien évidemment basé sur PhantomJS, et propose une API haut niveau, par dessus, qui va simplifier cette fameuse gestion de la synchronicité, des méthodes pour interagir avec la page, créer des scénarios de navigation, et effectivement tester des sites web, parce que c'est peu ça aussi un des objectifs. 

Donc au niveau de la synchronicité, voilà on a tout ferré à gauche, ça marche. Et voilà on a un petit Event Listener, c'est l'équivalent du script PhantomJS, que je vous ai affiché tout à l'heure, ça fait exactement la même chose, c'est-à-dire qu'on ne se prend plus la tête avec des callbacks, des callbacks, des callbacks, on les enchaîne très simplement avec une API qui semble d' utilisation très naturelle. 

Au niveau des clics c'est pareil, on a une méthode qu'on voit pas à l'écran mais qui s'appelle Click et qui permet de prendre en argument un sélecteur CSS, et depuis deux semaines un sélecteur XPath éventuellement, pour dire je veux cliquer sur tel bouton, on lance le script et on obtient les mêmes résultats qu'avec PhantomJS. 

Au niveau des tests, de la même manière, on peut tout à fait partir sur l'utilisation de cette API pour générer des tests qui en plus ont l'amabilité d'être colorisés et exportables sous par exemple Jenkins avec des résultats au format XUnit. 

Le site est parfaitement documenté, je dis parfaitement, j'en ai assez chié pour dire parfaitement.

Les limitations, c'est WebKit only, donc ça ne remplace pas Selenium, ça n'a pas d'interface graphique, donc c'est très difficile de se projeter, il faut s'abstraire et utiliser beaucoup en fait la console de Firebug ou un bookmarklet depuis avant hier. 

Et les gros intérêts dans les petites features intéressantes qu'apporte Casper, ça vaut réapprend Javascript ou ça vous apprend Javascript si vous connaissez pas, ça vous réapprend le DOM, c'est bien parce qu'on a beaucoup de couches d'abstractions par dessus le DOM mais remettre un peu les pieds dedans des fois c'est aussi sympa, ça vous réapprend le web parce qu'on est vraiment au plus bas niveau de ce qui se passe dans un navigateur et des échanges qu'on peut avoir en AJAX avec les serveurs, etc. et souvent à mieux connaître votre propre site.

Voilà je vous remercie (0:00).

 



