# Spring-cloud-eureka-configuration-server

Ce projet vise à mettre en place un serveur de configuration dans une architecture microservice. Pour ce faire, il est nécessaire d'avoir un serviceDiscovery de lancé, plusieurs services ainsi que des clients.

L'ensemble des fichiers de configuration sont stockés dans un repository sur le git (scf-config-repository-master). Le serveur de configuration est lié a ce repository Git et fournis les fichiers de config en fonction des requetes HTTP recus.

Il y a 3 paramètres définissant les endpoints d'un serveur de configuration : 
  1/ application : Correspond au nom du service.
  2/ profile : Correspond au profil voulu (ex : dev, prod ou autre)
  3/ label : (optionnal) le label correspond à la branche Git du repository de stockage des fichiers de configuration (scf-config-repository-master)
  
  Vous pouvez soit demander la configuration sous format JSON ou bien sous format .yml/.properties
