# Fiche de signalement Géocontrib

Ce document explique comment remplir la fiche de signalement créée dans Géocontrib pendant la phase de tests.

L'objectif de cette fiche est de transmettre aux développeurs les informations nécessaires pour comprendre, reproduire, qualifier et corriger un bug ou un comportement étrange. Plus le signalement est précis, plus il est facile de traiter le problème rapidement.

## Nom de la fiche

Le champ **Nom de la fiche** correspond au titre du signalement.

Le libellé de ce champ ne peut pas être modifié dans Géocontrib, mais il doit être compris comme le **titre court du problème**.

Il faut choisir un titre clair, qui permet de comprendre rapidement le sujet sans ouvrir toute la fiche.

Exemples :

- Le bouton de recherche ne fonctionne pas
- La carte ne s'affiche pas après chargement
- Le filtre commune ne renvoie aucun résultat
- Le texte d'aide n'est pas compréhensible

À éviter :

- Bug
- Problème
- Ça ne marche pas
- Test application

## Description succincte du problème

La description permet d'expliquer ce qui a été observé.

Elle doit contenir, si possible :

- ce que le testeur voulait faire ;
- les étapes réalisées ;
- ce qui était attendu ;
- ce qui s'est réellement produit ;
- si le problème se reproduit systématiquement ou seulement parfois.

Cette information est essentielle pour le développeur, car elle permet de reproduire le problème dans les mêmes conditions que le testeur.

Exemple :

```text
Je voulais rechercher une commune depuis le champ de recherche.
J'ai saisi "Lille", puis cliqué sur le résultat proposé.
Je m'attendais à ce que la carte se centre sur la commune.
La liste de résultats disparaît, mais la carte ne bouge pas.
Le problème se produit à chaque essai.
```

## Mail du demandeur

Le mail permet de recontacter la personne qui a signalé le problème si des précisions sont nécessaires.

Il peut être utile lorsque :

- le problème n'est pas reproductible par l'équipe de développement ;
- une capture d'écran manque ;
- les étapes décrites ne sont pas assez précises ;
- le retour concerne une demande d'amélioration à clarifier ;
- le niveau de sévérité doit être confirmé.

Cette information n'est pas utilisée pour juger le signalement, mais pour faciliter les échanges si besoin.

## Version du navigateur

La version du navigateur indique avec quel navigateur le test a été réalisé.

Exemples :

- Firefox 127
- Chrome 126
- Edge 126
- Safari 17

Cette information est importante, car certains bugs peuvent apparaître uniquement sur un navigateur ou une version précise.

Par exemple, un affichage peut fonctionner correctement sur Chrome, mais être cassé sur Firefox. Une fonctionnalité peut aussi dépendre de capacités plus ou moins bien prises en charge selon le navigateur.

Si vous ne connaissez pas la version exacte, indiquez au minimum le nom du navigateur utilisé.

## Type de support

Le type de support correspond au matériel ou au contexte utilisé pour tester l'application.

Exemples :

- ordinateur portable ;
- ordinateur fixe ;
- écran externe ;
- environnement professionnel ;
- environnement personnel.

Dans cette première version, les tests doivent être réalisés sur ordinateur. L'affichage responsive n'étant pas encore pris en charge, il est inutile de tester l'application sur smartphone ou tablette pour le moment.

Cette information aide tout de même le développeur à comprendre le contexte du test, notamment en cas de problème d'affichage, de résolution d'écran ou de comportement lié au poste utilisé.

## Type de bug ou amélioration

Ce champ permet de classer le signalement afin de l'orienter vers le bon type de traitement.

### Données

À utiliser lorsqu'une donnée semble fausse, absente, incohérente ou mal restituée.

Exemples :

- une valeur affichée semble erronée ;
- une donnée attendue n'apparaît pas ;
- un résultat ne correspond pas au filtre appliqué ;
- une information cartographique semble incorrecte.

Ce type de retour aide les développeurs et chefs de projet à distinguer un problème technique d'un problème lié à la donnée.

### Accessibilité

À utiliser pour les problèmes d'ergonomie, d'affichage ou de confort d'utilisation.

Exemples :

- un bouton est difficile à identifier ;
- un texte est peu lisible ;
- une action n'est pas intuitive ;
- un élément masque une information importante ;
- le contraste ou la taille d'un élément gêne la lecture.

Ce type de retour concerne l'expérience utilisateur et la facilité d'utilisation de l'application.

### Problème d'accès aux flux

À utiliser lorsqu'une ressource externe ne semble pas se charger correctement.

Cela peut concerner des flux ou fichiers de type WFS, CSV, JSON ou autres sources de données.

Exemples :

- une couche ne se charge pas ;
- un message d'erreur apparaît au chargement d'une donnée ;
- une liste reste vide alors qu'elle devrait être alimentée ;
- la carte ou un tableau ne reçoit aucune donnée.

Cette information est utile pour le développeur, car elle permet de rechercher un problème de connexion, de configuration, de disponibilité du service ou de format de réponse.

### Sécurité

À utiliser lorsqu'un comportement semble présenter un risque de sécurité.

Exemples :

- accès à une information qui ne devrait pas être visible ;
- affichage de données sensibles ;
- accès possible à une fonctionnalité réservée ;
- comportement inhabituel après une action liée aux droits ou aux accès.

Ce type de signalement doit être traité avec attention, car il peut concerner la confidentialité, l'intégrité des données ou les droits d'accès.

### Contenu

À utiliser pour les remarques sur les textes, logos, mentions légales ou contenus éditoriaux.

Exemples :

- faute dans un texte ;
- logo incorrect ;
- mention légale absente ;
- formulation à corriger.

Attention : dans cette version de test, le contenu n'est pas encore figé et peut être incomplet ou remplacé par du lorem ipsum. Il est donc inutile de créer une fiche uniquement pour signaler un texte provisoire ou un faux contenu déjà identifié comme temporaire.

### Idées, propositions

À utiliser pour proposer une amélioration, une nouvelle fonctionnalité ou une information complémentaire.

Exemples :

- ajouter un filtre ;
- modifier l'ordre d'affichage d'informations ;
- ajouter une aide ou une infobulle ;
- simplifier un parcours ;
- afficher une information métier supplémentaire.

Ce type de retour est utile pour alimenter les prochaines phases de conception et prioriser les évolutions.

### Autre(s)

À utiliser si aucun des types précédents ne correspond au signalement.

Il est conseillé d'expliquer clairement dans la description pourquoi le retour ne rentre pas dans une catégorie existante.

## Estimation du niveau de sévérité

La sévérité permet d'estimer l'impact du problème. Elle aide à prioriser les corrections.

Il ne s'agit pas de juger la qualité du retour, mais de comprendre l'urgence et l'importance du problème.

### Faible

À utiliser pour un problème mineur qui ne bloque pas l'utilisation.

Exemples :

- petite gêne visuelle ;
- libellé légèrement ambigu ;
- amélioration de confort ;
- comportement perfectible mais contournable facilement.

### Moyen

À utiliser pour un problème non prioritaire, à traiter selon sa sévérité réelle et le plan de charge.

Exemples :

- fonctionnalité partiellement gênante ;
- parcours peu clair mais utilisable ;
- erreur non bloquante ;
- problème contournable avec une autre action.

### Élevé

À utiliser pour un problème bloquant avec impact sur la donnée, sa diffusion ou sa communication.

Exemples :

- donnée importante absente ou erronée ;
- fonctionnalité principale inutilisable ;
- résultat métier incorrect ;
- information diffusée de manière incorrecte.

Ce niveau doit être utilisé lorsque le problème empêche un usage important de l'application ou peut entraîner une mauvaise compréhension de la donnée.

### Critique

À utiliser pour un problème bloquant avec plantage applicatif, visibilité de données sensibles ou risque de sécurité.

Exemples :

- l'application plante ou devient totalement inutilisable ;
- une donnée sensible est visible alors qu'elle ne devrait pas l'être ;
- un problème de sécurité est suspecté ;
- un accès non autorisé semble possible.

Ce niveau doit rester exceptionnel et être réservé aux situations les plus graves.

## Pièce(s) jointe(s)

Les pièces jointes permettent de mieux comprendre le problème.

Il est recommandé d'ajouter une capture d'écran dès qu'un problème visuel, un message d'erreur ou un comportement étrange est constaté.

Formats à privilégier :

- PDF ;
- JPG.

Une bonne capture d'écran doit montrer :

- la zone concernée ;
- le message d'erreur s'il y en a un ;
- le résultat obtenu ;
- si possible, l'ensemble de l'écran pour comprendre le contexte.

Les pièces jointes sont très utiles pour les développeurs, car elles permettent parfois d'identifier rapidement un problème qui serait difficile à décrire uniquement avec du texte.

## Exemple de fiche bien remplie

```text
Nom de la fiche :
Le filtre commune ne met pas à jour les résultats

Description succincte du problème :
Je sélectionne une commune dans le filtre, mais les résultats affichés ne changent pas.
Je m'attendais à voir uniquement les données liées à cette commune.
Le problème se reproduit à chaque test.

Mail du demandeur :
prenom.nom@example.fr

Version du navigateur :
Firefox 127

Type de support :
Ordinateur portable

Type de bug / Amélioration :
Données

Estimation du niveau de sévérité :
Élevé

Pièce(s) jointe(s) :
Capture d'écran au format JPG montrant le filtre sélectionné et les résultats affichés.
```

## Rappel sur le périmètre de cette version

Dans cette première version, certains éléments ne sont pas finalisés.

Il est inutile de créer une fiche de signalement pour :

- le design général non finalisé ;
- l'affichage sur smartphone ou tablette ;
- les problèmes responsive ;
- les textes provisoires ;
- les contenus incomplets ;
- les blocs de texte de type lorem ipsum.

Les signalements doivent se concentrer en priorité sur les parcours utilisateur, la compréhension générale, les fonctionnalités disponibles, les erreurs visibles et les comportements réellement bloquants ou gênants.
