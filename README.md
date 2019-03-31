# Présentation de Angular Flex Layout via [reveal.js](https://github.com/hakimel/reveal.js/)

L'accès à la présentation se fait [**ici!**](https://stackblitz.com/github/jeremybrochard/flex-layout-demos)


Les images présentes sont issue du [guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) de [CSS-TRICKS](https://css-tricks.com/) et de [CSS layout cheat sheet](https://learn-the-web.algonquindesign.ca/topics/css-layout-cheat-sheet/#layout-mechanics).


# Déroulé de la présentation


## Introduction à Angular Flex Layout



- Module Angular
- Implémentation de FlexBox CSS + media queries via des directives
- Projet open-source créé et maintenu par l'équipe Angular
- Uniquement pour les projets Angular 4.1.x ou plus  - suit les versions de Angular (actuellement en version 7.x)
- Indépendant de Angular Material



## FlexBox CSS



- Module CSS proposant un nouveau type de layout
- *W3C Candidate Recommendation* depuis 2012 (dernière révision datant de 2018)
- Types de layout CSS :
  - Inline layout - positionnement horizontal
  - Block layout - positionnement vertical
  - Table / Grid layout  - positionnement en 2 dimensions
  - Positionned layout - positionnement fixe et absolu 
  - **Flex layout** <== <u>Nous allons parler de celui la!</u>



- Flex :
  - Proposer une manière plus efficace pour placer, aligner et définir la taille de ses éléments dans un contenant
  - Ne dépend pas d'une direction contrairement aux layouts *inline* et *block* 
  - **Flexible** : s'adapte très bien à tous type de formats 





### Notions de bases



- Conteneur et éléments Flex

  ![01-container](./assets/01-container.svg)

  ![02-items](./assets/02-items.svg)

  

  - 

![00-basic-terminology - https://css-tricks.com/snippets/css/a-guide-to-flexbox/](./assets/00-basic-terminology.svg)

- Plusieurs propriétés peuvent s'appliquer au conteneur et au éléménts Flex

- Conteneur Flex

  - Direction : ligne / colonne / ligne ou colonne inversée

  ![flex-direction](./assets/flex-direction.svg)

  - Retour à la ligne : Wrap

  ![flex-wrap](./assets/flex-wrap.svg)

  

  - Alignement sur l'axe principal / secondaire

  

  ![justify-content](./assets/justify-content.svg)

  ![align-items](./assets/align-items.svg)

- Element Flex

  - Ordre

  ![order](./assets/order.svg)

  

  - Taille de base (basis), gestion de l'agrandissement (grow), du rétrecissement (shrink)

  ![flex-grow](./assets/flex-grow.svg)

  

  - Alignement

  ![align-self](./assets/align-self.svg)



## Le module Angular Flex Layout



- Implémente les classes de FlexBox CSS sous la forme de directives à placer dans l'HTML
- Ajoute des fonctionnalités supplémentaires
- Approche JS permettant de gérer le style de manière dynamique / Bootstrap approche CSS pure mais beaucoup de classes à mémoriser
- Structure de la page dans le template : limite la "fatigue CSS"
- Très bon support du cross-platform
- Intégration native des media-queries 



### Les directives



Démo présentant :

- Les directives sur les conteneurs : 
  - Direction / Layout Wrap
  - Alignement
  - Espacement - ajout de du module Angular

- Les directives sur les éléments : 
  - Ordre
  - Taille (basis grow shrink)
  - Alignement spécifique

- Ajout du module Angular
  - FxHide et FxShow
  - NgClass et NgStyle
  - Gestion du responsive via les alias



| Breakpoint | MediaQuery                                               |
| ---------- | -------------------------------------------------------- |
| xs         | 'screen and (max-width: 599px)'                          |
| sm         | 'screen and (min-width: 600px) and (max-width: 959px)'   |
| md         | 'screen and (min-width: 960px) and (max-width: 1279px)'  |
| lg         | 'screen and (min-width: 1280px) and (max-width: 1919px)' |
| xl         | 'screen and (min-width: 1920px) and (max-width: 5000px)' |
|            |                                                          |
| lt-sm      | 'screen and (max-width: 599px)'                          |
| lt-md      | 'screen and (max-width: 959px)'                          |
| lt-lg      | 'screen and (max-width: 1279px)'                         |
| lt-xl      | 'screen and (max-width: 1919px)'                         |
|            |                                                          |
| gt-xs      | 'screen and (min-width: 600px)'                          |
| gt-sm      | 'screen and (min-width: 960px)'                          |
| gt-md      | 'screen and (min-width: 1280px)'                         |
| gt-lg      | 'screen and (min-width: 1920px)'                         |



