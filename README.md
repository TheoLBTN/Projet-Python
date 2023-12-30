# Projet-Python

## Modélisation des émissions polluantes du parc automobile français depuis 2011 jusqu'en 2050.

Contributeurs :
Pierre PERRIGAULT,
Aymeric PERRIN,
Théo LEBRETON

Nous avions pour ambition de modéliser les émissions polluantes (oxyde d'azote, monoxyde de carbone en particulier) du parc automobile français jusqu'en 2050, en suivant des règles d'évolution simples. Ce projet se base principalement sur des données de l'ADEME du parc automibile français entre 2011 et 2022, qui donne le nombre de véhicule de chaque type (Crit'Air, carburant, etc) et de chaque âge pour toutes les années considérées. Notre projet se décompose en plusieurs phases. Tout d'abord, il a été nécessaire de modéliser l'évolution du parc automobile français en se focalisant uniquement sur les véhicules particuliers. Cette première modélisation étant primordiale pour pouvoir par la suite estimer les émissions polluantes rejetées par le parc.

Pour ce faire nous avons commencé par étudier les données aux travers de diverses statistiques descriptives (Stat_descriptives) afin d'axer notre étude et mieux calibrer nos modèles. 

Concernant les modèles, nous avons décidé d'en réaliser deux différents:

- L'un, ayant une approche empirique, tente de prédire l'évolution du parc via un modèle dynamique prenant en compte les pannes de véhicules (Pannes.ipynb) ainsi que la mise sur le marché différenciée selon les Crit'Air des véhicules neufs. Il renvoie notamment un premier tableau (fit_pannes.csv) donnant pour chaque type de véhicule la probabilité de tomber en panne en fonction de son âge en utilisant la base de donnée de l'ADEME. Le modèle cherche également à prédire les entrées de nouveaux véhicules sur le parc automobile (Modélisation_emmisions.ipynb) à partir des données et des prérogatives gouvernementales comme l'interdiction de la vente de véhicules thermiques à partir de 2035. Il se sert ensuite de ces données pour estimer l'évolution du nombre de chaque classe Crit'Air de véhicules en France.
  
- L'autre, plus mathématisée, tente de "fitter" la part de Crit'Air E (véhicules électriques) à l'aide d'une équation différentielle (Tendances.ipynb) exponentielle au début puis plus faible par la suite, elle utilise également des régressions linéaires pour estimer l'évolution de la part des autres classe de véhicules et arrive comme la précédente a une estimation de l'évolution du nombre de chaque classe Crit'Air de véhicules en France.
  
Ces deux approches ont le même objectif final, estimer les émissions de monoxyde de carbone et d'oxyde d'azote toutes deux nocives pour la santé. Les tableaux d'émissions maximales de particules fines des véhicules en fonction de leur carburant et de leur norme Euro utilisés ont été scrappés depuis wikipédia (Scrapping_particules_fines.ipynb) et enregistrés sous format csv (emissions_diesel.csv et emissions_essence.csv).
