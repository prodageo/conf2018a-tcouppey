# Comment se faire hacker bien comme il faut! par Julien Topçu
 - tcouppey
 
## Cartouche d'identification

 - Manifestation : CodeursEnSeine 2019
 - Lieu : Kindarena
 - Conférence : Comment se faire hacker bien comme il faut! 
 - Horaire de la conférence : 11h
 - Durée de la conférence : 1h
 - Conférencier(s) :
   - [Julien Topçu (Société Générale & OWASP fundation)](https://twitter.com/JulienTopcu)
 - Audience : 250 personnes
 - Auteur du billet : Théo COUPPEY
 - Mots-clés : Sécurité, Bonnes pratiques, Développement, OWASP
 - URL de l'illustration : 
 
 ![](https://mcdn.wallpapersafari.com/medium/93/78/WfPIYV.png)

## Support
 - Non re-diffusé [lien vers la même présentation (en anglais)](https://www.youtube.com/watch?v=ipM1_7uPC38)
 - Nombre de diapos du support : Non disponble (pas de diapositives mais une présentation à l'aide d'applications)
 - Plan du support : 
   - Présentation
   - Injection SQL
   - Hashage de mot de passe
   - XML External entities
   - Fishing
   - Vulnérabilité des dépendances
   - Présentation OWASP et Fin

## Résumé

  Julien Topçu présente plusieurs failles de sécurités dans les applications, parmies les plus connues, et explique les manières de s'en prémunir. Il utilise pour sa présentation une application nommée Pangloss qu'il a créé, afin d'illustrer sa conférence. Il nous présente ainsi, toujours avec une pointe d'humour, des vulnérabilités avec leurs solutions et bonnes pratiques du point de vue développeur. 

  Julien Topçu commence par présenter l'injection SQL avec le nom d'utilisateur "magique" : << 'OR '1'='1' LIMIT 1 -- >>. Il mets en évidence un problème dans la requête SQL lors de l'authentification. Viens ensuite le probème des mots de passe qui sont encodés par la plupart des entreprises comme il le dit en HRE (Human Readable Encoding a.k.a. Clear Text). Il présente alors la possibilité de hasher les mots de passe mais aussi d'en avoir un complexe. Il explique que pour de nombreuses fonctions de hashages, il existe des "Rainbow table", qui sont des dictionnaires de correspondances entre de nombreux mot de passe simple, tels que les mots du langage, et leur hash. Il propose alors des fonctions de hash avec de l'aléatoire qui peuvent donner plusieurs hash pour une même entrée. Il aborde ensuite les vulnérabilités dues au XML avec l'autorisation des ExternalEntities qui permettent l'éxecution d'application non présente dans le backend. Julien Topçu présente le ensuite le fishing et son fonctionnement avec les solutions à apporter. Il fini la présentation des vulnérabilités par une application de l'OWASP qui permet d'identifier les dépendances qui ont des vulnérabilités.

  Julien Topçu fini sa présentation en présentant l'OWASP ainsi que par un QRCode à scanner vers un "article intérressant" qui est en fait un "hack"
  
  
## Architecture et facteur qualité

  Cette conférence porte sur le 4ème factueur qualité de McCall : Integity, la Sécurité. C'est à dire que l'on vérifie et protège les accès au code et aux données de notre logiciel. Par exemple, l'injection SQL présente tout ces aspects. Une faille tel que celle-ci permet un accès non autorisé aux données (BD utilisateur/mot de passe) puis peut offrir un accès administrateur (non-autorisé) et donc un accès au code et à l'intégrité de l'application.
