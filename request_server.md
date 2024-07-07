EIga No Neko est une interface utilisateur utilisable où les server vidéo (appeller Node) discute via une API.

Lors de l'accée d'un utilisateur à eiganonneko.com, il vas emetre à tout les Node une demande, par exemple la page d'acceuil. Elle vas emetre une information à un server Node de la liste Publique, et vas lui demander de lui retourner le format /channels.json pour obtenire la liste des differente chaine du serveur vidéo.

L'API EigaNoNeko est expliquer par le prinicpe de Emeteur et Recepteur.
L'emeteur  vas obligatoirement renvoyer un fichier JSON. Ce lui devras contenir l'interface du fichier donnée dans la requette POST "model" qui peut-etre "channels.json", "channel.json", "watch.json". Une fois recçus par l'API eiganoneko.com celle si sont traduis et adapter, elle sont ensuite renvoyer à l'utilisateur qui accede à la page d'acceuil (par exemple).
Le récepteur sont des page qui sont emise en amont par l'API EigaNoNeko, et les requette peuvent etre demander par l'utilisateur ou bien etre executer dans des temps régulier par l'API. Quand un Node reçois une information du recepteur, il doit retourne auccune valeur. Le Recpteur envoie uniquement des information statistique ou bien des information de connection.


Request liste :
/channels - GET
/channel - POST
/watch - POST


/emeteur -> Emetre un fichier JSON à l'interface utilisateur
/recepteur -> Recevoir des information de l'API.