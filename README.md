# TP-ALGO-SECU-B

---

**Analyseur de logs de serveur Web**

*Vous êtes un administrateur de serveur web et, dans le cadre de vos responsabilités de cybersécurité, vous souhaitez analyser les logs de votre serveur pour détecter toute activité suspecte.*

**Étape 1 : Initialisation**

  logs : 
  ```pseudo
  logs = [
    {date: 2023-09-01 12:23, ip: "192.168.1.1", request: "GET /index.html", status: 200},
    {date: 2023-09-01 12:28, ip: "192.168.1.2", request: "GET /admin", status: 403},
    ...
  ]
  ```

**Étape 2 : Analyse des logs**

1. Écrivez une fonction qui retourne le nombre total de requêtes faites sur le serveur.
2. Écrivez une fonction qui retourne le nombre de requêtes réussies (status 200) et celles qui ont échoué (par exemple, status 404 ou 403).
3. Écrivez une fonction qui retourne les IP qui ont fait plus de X requêtes (vous pouvez choisir X comme seuil, par exemple 100).
4. Écrivez une fonction qui retourne les IP qui ont tenté d'accéder à certaines pages sensibles, comme "/admin", "/uploads", "/config".

**Étape 3 : Fonctions d'analyse**

- Créez une fonction pour extraire toutes les IP uniques du journal.
  
  ```pseudo
  fonction extraireIPUniques(logs):
      ...
      RETOURNER IPsUniques
  ```

- Créez une fonction pour compter le nombre de requêtes par IP.

  ```pseudo
  fonction compterRequetesParIP(logs, ipCible):
      ...
      RETOURNER nombreDeRequetes
  ```

- Créez une fonction qui prend en paramètre un code de statut et renvoie le nombre de requêtes ayant ce statut.

  ```pseudo
  fonction compterRequetesParStatus(logs, statusCode):
      ...
      RETOURNER nombreDeRequetesAvecStatus
  ```

**Étape 4 : Mesures préventives**

1. Écrivez une fonction qui retourne chaque IP qui a tenté d'accéder à la page "/admin" plus de 3 fois, affichez un message d'alerte.
2. Écrivez une fonction qui retourne toute IP ayant plus de 200 requêtes en moins de 10 minutes, affichez un message d'alerte.

**Étape 5 : Rapport**

- Générez un rapport de synthèse à la fin de l'analyse qui affiche:
  - Le nombre total de requêtes
  - Le nombre de requêtes réussies vs échouées
  - Les IP suspectes

---

**Analyse de la force des mots de passe**

**Contexte** :
Vous travaillez comme développeur pour un site web. Vous devez vérifier la force des mots de passe que les utilisateurs souhaitent utiliser.

**Consignes** :
```
caractèresSpéciaux = ['&', '!', '#', '*', '$', '^', '@', '%']

```

1. Créez une fonction qui prend un mot de passe comme argument et retourne sa force sur une échelle de 1 à 5, où 1 est très faible et 5 est très fort.
2. Les critères de force sont les suivants :
    - Niveau 1 : Uniquement des lettres minuscules.
    - Niveau 2 : Lettres minuscules et majuscules.
    - Niveau 3 : Lettres et chiffres.
    - Niveau 4 : Lettres, chiffres et au moins un caractère spécial.
    - Niveau 5 : Plus de 12 caractères, lettres, chiffres et au moins un caractère spécial.
3. Affichez un message à l'utilisateur selon la force du mot de passe.
4. Testez votre fonction avec différents mots de passe et pour chaque mot de passe, afficher " "La force du mot de passe "..." est : "....

---
