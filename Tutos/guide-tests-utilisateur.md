# Guide de test utilisateur

Ce document propose une méthode simple pour tester l'application web pendant la première phase de retours utilisateurs.

L'objectif n'est pas de réaliser un audit technique complet, mais de vérifier si l'application est compréhensible, agréable à utiliser et cohérente pour l'utilisateur grand public ou professionnel.

## Objectifs des tests

Les tests doivent permettre de répondre à quelques questions simples :

- Est-ce que l'application est facile à prendre en main au premier usage ?
- Est-ce que les principales actions sont faciles à trouver ?
- Est-ce que le parcours utilisateur est fluide ?
- Est-ce que certains libellés, boutons ou informations semblent ambigus ?
- Est-ce que des erreurs, blocages ou comportements inattendus apparaissent ?
- Est-ce que les informations affichées semblent cohérentes avec ce que l'utilisateur cherche à faire ?

## Comment tester l'application

Il est conseillé de tester l'application comme le ferait un utilisateur lambda, sans chercher à contourner volontairement le fonctionnement prévu.

Quelques exemples de tests utiles :

1. Ouvrir l'application et observer si l'objectif général est compréhensible.
2. Parcourir les menus, boutons, filtres, cartes, tableaux ou panneaux disponibles.
3. Réaliser les actions principales proposées par l'application.
4. Vérifier si les messages affichés sont compréhensibles.
5. Tester plusieurs scénarios simples, par exemple rechercher une information, consulter un résultat, modifier un filtre ou revenir en arrière.
6. Noter les moments où l'utilisateur hésite, se trompe ou ne sait pas quoi faire.

Il est important de signaler aussi bien les bugs visibles que les difficultés de compréhension ou les comportements qui semblent étranges.

## Points d'attention pour un utilisateur lambda

Lors du test, il faut surtout observer le ressenti utilisateur :

- l'application semble-t-elle claire ?
- les termes utilisés sont-ils compréhensibles ?
- les boutons et actions sont-ils faciles à identifier ?
- le résultat obtenu correspond-il à ce qui était attendu ?
- un utilisateur non technique peut-il avancer sans aide ?
- y a-t-il des moments de confusion, d'attente ou de frustration ?

Un retour utilisateur peut être utile même s'il ne concerne pas un bug bloquant.

## Points d'attention pour un professionnel

Le professionnel peut compléter le test avec une lecture plus fonctionnelle :

- les parcours proposés correspondent-ils au besoin métier ?
- les informations importantes sont-elles visibles au bon moment ?
- les étapes sont-elles cohérentes avec l'usage attendu ?
- certains écrans ou actions manquent-ils d'explication ?
- les priorités fonctionnelles semblent-elles respectées ?
- certains comportements risquent-ils de poser problème en production ?

Les retours doivent aider à prioriser les corrections avant les prochaines phases de développement.

## Informations à fournir en cas de bug ou comportement étrange

Lorsqu'un bug, une erreur ou un comportement étrange est détecté, il faut créer une fiche de retour avec le plus d'informations possible.

Merci d'indiquer :

- le titre court du problème ;
- la date et l'heure approximative du test ;
- le navigateur utilisé, par exemple Firefox, Chrome, Edge ou Safari ;
- le système utilisé, par exemple Windows, macOS ou Linux ;
- l'adresse ou la page concernée si elle est connue ;
- les étapes précises pour reproduire le problème ;
- le résultat attendu ;
- le résultat réellement obtenu ;
- une capture d'écran si possible ;
- le niveau de gêne ressenti : faible, moyen, important ou bloquant ;
- toute information utile sur le contexte du test.

Exemple :

```text
Titre : Le bouton de recherche ne déclenche aucun résultat
Navigateur : Firefox
Système : Windows
Étapes :
1. Ouvrir l'application
2. Saisir une recherche
3. Cliquer sur le bouton de recherche
Résultat attendu : la liste des résultats s'affiche
Résultat obtenu : rien ne se passe
Gêne : importante
```

Si le problème n'est pas reproductible à chaque fois, il faut le préciser.

## Types de retours attendus

Les retours peuvent concerner :

- un bug bloquant ;
- une erreur visible ;
- une action qui ne produit aucun effet ;
- un affichage incohérent ;
- un message difficile à comprendre ;
- une lenteur importante ;
- un parcours peu clair ;
- une information manquante ;
- une suggestion d'amélioration fonctionnelle.

## Ce qui n'est pas encore à tester dans cette version

Certaines parties de l'application sont encore incomplètes ou non finalisées. Il est donc inutile de créer des fiches de bug sur ces points pour le moment.

Le design général n'est pas encore finalisé. Les couleurs, espacements, styles, pictogrammes, tailles de texte et détails visuels pourront évoluer dans une prochaine version.

L'affichage responsive n'est pas pris en charge dans cette version. Il est donc inutile de tester l'application sur smartphone ou tablette pour le moment. Les tests doivent être réalisés sur ordinateur.

Le contenu éditorial n'est pas figé et reste incomplet. Certains textes peuvent être absents, provisoires ou remplacés par du faux texte de type lorem ipsum. Il est inutile de créer une fiche de bug pour signaler ces contenus temporaires.

Les retours doivent donc se concentrer en priorité sur la compréhension générale, les parcours utilisateur, les fonctionnalités disponibles et les bugs réellement bloquants ou gênants.
