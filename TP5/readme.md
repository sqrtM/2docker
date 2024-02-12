Accédez à votre service et actualisez plusieurs fois la page. Les informations affichées changent. Pourquoi ?
- La requête est envoyée à une instance différente du conteneur.

docker stack ls indique 6 services pour la stack vote. Observer également l’output de docker stack ps vote et de docker stack services vote. Qu’est-ce qu’un service dans la terminologie de Swarm ?
- Un service est fonctionnellement un modèle de ce qui sera instancié dans chaque nœud dans lequel il existe. Il définit l'image, la configuration, le nombre de répliques et d'autres informations relatives à la définition des tâches que le service entreprend.

Accéder aux différents front-ends de la stack grâce aux informations contenues dans les commandes précédentes. Sur le front-end lié au vote, actualiser plusieurs fois la page. Que signifie la ligne Processed by container ID […] ? Pourquoi varie-t-elle ?
- Il s'agit de l'instanciation spécifique du conteneur qui traite la requete. Elle change au fur et à mesure que la requete est traitée par différentes instanciations de l'image dans le swarm.

Accédez au service depuis un node, et depuis l’autre. Actualisez plusieurs fois la page. Les informations affichées changent. Lesquelles, et pourquoi ?
- L'adresse IP, l'adresse IP distante et le nom d'hôte sont tous modifiés. Là encore, c'est parce que la requête est traitée par un conteneur différent à chaque fois. Le modèle d'IP 10.*.*.* montre que la requête est transmise de manière interne au sein de le swarm.

spécifier quelques options d’orchestration exclusives à Docker Swarm : que fait mode: global ?
- Alors que les services répliqués se voient attribuer un nombre déterminé de répliques réparties dans l'essaim, une instance de chaque service global est attribuée à chaque nœud (en supposant que le nœud réponde aux exigences spécifiées par le service).