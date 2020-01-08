**Projet perso AFPA**

## Planificateur de voyage

### - 1 : Explication du projet
### - 2 : Contenu (fonctionnalitées)
### - 3 : Technos utilisées
### - 4 : Problèmes rencontrés

# 1 : Explication du projet

- Le projet serra une application web (avec un affichage mobile **ET** desktop) et aura pour but de simplifier la planification d'un voyage du choix des dates
jusqu'aux activitées / hotels ainsi qu'une partie de gestion de budget

- Le projet serra disponnibles dans 2 version
  - FREE :
    - 3 utilisateurs
    - Pas de gestion du budget
    - 5 Activitées max
    - 2 Choix d'hotel Max
  - PREMIUM :
    - Système de payement par paypal (Utilisation du mode sandbox)
    - Gestion de budget
    - Utilisateur illimités
    - Activitées illimitées
    - Export du plan de voyage en PDF 
    - License a vie

# 2 : Contenu (Fonctionnalitées)

  - Page d'acceuil : 
    - Présentation du projet (lien inscription, connexion cgu, cgv etc)
  - Page d'inscription/Connexion:
    - Présence de 2 forms un pour inscription, un pour conexion
  - Page d'inscription :
    - Formulaire pour nom du voyage , adresse emails pour utilisateurs supp etc...
  - Page Main du projet :
    - Composé de plusieurs boxs composé des informations suivantes:
      - 1 boxe dates
      - 1 boxe activitées en attente
      - 1 boxe activitées choisies
      - 1 boxe hotels en attentes
      - 1 boxe hotels validés 
      - 1 boxe gestion du budget
    - Chaque box a son propre y-overrflow
    - Les box de type **en attente** comporte un icone "+" permettant d'ajouter une activitée un hotel etc...
    - Chaque champs présent dans **en attente** contiendra 2 boutons afin de faire un vote (POUR OU CONTRE)
    - La box gestion de projet permet a chaque membre de définir une somme qu'il allouera au projet (aaucun transfert d'argent ici il s'agit d'une simple promesse pour le groupe)
    - La box gestion de projet comportera aussi un CHART PIE afin de lister les plus grosses dépenses (hotel, activité, restauration, transport)
    - Un bouton serra présent afin de sauvegarder le projet au format PDF afin d'obtenir les informations suivantes :
        - La fiche de route avec le ou les hotels validés, les activitées validée le budget min/max 
        - Des informations utiles sur le pays ou ce déroule le voyage ex numéro d'urgence etc ... 
        - Les horraires et moyens de contact des différentes activitées / hotels en cas de soucis
        
# 3 : Technos utilisées
 
   L'application WEB serra séparée en 2 parties distinctes 
    - Le front END , qui est l'interface utilisateur
    - Le back END , qui serra une api GET/POST effectuant des retours JSON
    - Le backEnd se ferra en utilisant le framework symfony   
    - Le front End se ferra en utilisant un framework JavaScript (ou nodeJS) a savoir ReactJS ou vue.JS  
    - Le système de mail passera par une fonction d'envoie SMTP (avec SSL) 
    - L'authentification se basera sur JWT en cookie AINSI q'une possibilitée d'activer un OTP (utilisable avec GoogleAuthentificator)
    - Le processus d'inscription comportera un captchat (ReCaptcha by Google)
    - Le css serra développé a partir du framework Bootstrap 4
    - La génération PDF serra développé a partir du module (**TROUVER UN ODULE POUR SF PERMETTANT LA GENERATION DE PDF**)
      

# 4 : Problèmes rencontrés

  - Paypal :
      - Mise en place de l'IPN de PayPal en passant par une requete Ajax
  - GoogleMaps:
      - Prise en charge de google maps afin de : 
          - Schematiser un itinéraire entre toutes les activitées
          - Lister les activitées et les hotels validés ET/OU (filtre) en attente
          
