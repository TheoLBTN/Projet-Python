# Projet-Python

## Modélisation des émissions polluantes du parc automobile français depuis 2011 jusqu'en 2050.

Contributeurs:
Pierre PERRIGAULT
Aymeric PERRIN
Théo LEBRETON

Notre projet se décompose en plusieurs phases. Tout d'abord, il a été nécessaire de modéliser l'évolution du parc automobile français en se focalisant uniquement sur les véhicules particuliers. Cette première modélisation étant primordiale pour pouvoir par la suite estimer les émissions polluantes rejetées par le parc.

Pour ce faire nous avons commencé par étudier les données aux travers de diverses statistiques descriptives (Stat_descriptivesV2) afin d'axer notre étude et mieux calibrer nos modèles. 

En parlant de modèles, nous avons décidé d'en réaliser deux différents:
- L'un ayant un approche beaucoup plus expérimentale en tentant de prédire les pannes (Pannes), il renvoie notamment un premier tableau (fit_pannes) donnant pour chaque type de véhicule la probabilité de tomber en panne en fonction de son âge. Le modèle cherche également à prédire les entrées de nouveaux véhicules sur le parc automobile (Modélisation_emmisions) à partir des données et des prérogatives gouvernementales comme l'interdiction de la vente de véhicules thermiques à partir de 2035.
  
- L'autre beaucoup plus mathématique, tente de "fitter" les données à l'aide d'une équation différentielle (Tendances) en cherchant à capturer la croissance des véhicules électriques; exponentielle au début puis plus faible par la suite.
  
Ces deux approches ont le même objectif final, estimer les émissions de monoxyde de carbone et d'oxyde d'azote tout deux nocifs pour la santé. Les tableaux d'émissions de particules fines des véhicules en fonction de leur carburant et de leur norme Euro utilisés ont été scrappé depuis wikipédia (Scrapping_particules_fines) et enregistrés sous format csv.