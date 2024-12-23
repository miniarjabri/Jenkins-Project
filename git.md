## Integrating with GitHub

use this project: 

https://github.com/kodekloudhub/jenkins-project

![image](https://github.com/user-attachments/assets/1380821d-ba52-4b4e-8d25-ea9e76d35556)


## 1. Set Up Jenkins
- specify the build triggers: when Jenkins should automatically run a build

![image](https://github.com/user-attachments/assets/28ff1310-240b-4fea-8882-d34f1274ebe2)


- GitHub hook trigger for GITScm polling: github repo notify jenkins agent and the agnet will run the build

![image](https://github.com/user-attachments/assets/309f5f65-8120-4f11-836d-5a1f2cd762dc)

- select execute Shell
## 2. GitHub Repo
- go to setting
- click on "Webhoocks"
- select "add webhook"
![image](https://github.com/user-attachments/assets/a1386cd4-349d-4e55-ab7c-906638edb194)

- in "Payload url" put the jenkins url "http://localhost:8080/github-webhook"
- content type: application server
- which event would like to trigger this webhook?

![image](https://github.com/user-attachments/assets/204e892c-39dc-4982-bade-c1d1745b7502)

## 3. Build 
(only once )

![image](https://github.com/user-attachments/assets/bd73d8d8-9555-4d29-a0f4-ebdf38b40a25)


![image](https://github.com/user-attachments/assets/6292fe95-a83a-49c8-8b57-1ca2c8ded715)


## 3. Change Code
- git add .
- git commit -m "changed code"
- git push origin main

- Jenkins:
- ![image](https://github.com/user-attachments/assets/aba0b58a-1ce3-4147-8d07-a0c4812337fb)

## **1. Début de l'exécution**
- **`Started by GitHub push`** :
  - Ce job a été déclenché automatiquement par un **push GitHub**.
  - Jenkins est configuré pour surveiller un dépôt GitHub et exécuter un pipeline dès qu'un commit est poussé.

- **`Running as SYSTEM`** :
  - Le job est exécuté sous l’utilisateur système Jenkins. Cela indique que Jenkins utilise ses permissions par défaut pour exécuter les scripts et accéder aux fichiers.

---

## **2. Construction dans le workspace**
- **`Building in workspace /var/lib/jenkins/workspace/Flask-pipeline`** :
  - Jenkins utilise un dossier dédié (workspace) pour exécuter les étapes du pipeline.
  - Ce répertoire contient :
    - Les fichiers clonés du dépôt GitHub.
    - Les fichiers générés par le pipeline.

---

## **3. Git : récupération du code source**
- **`Fetching changes from the remote Git repository`** :
  - Jenkins se connecte au dépôt GitHub (`https://github.com/kodeloudhub/jenkins-project`) et télécharge les dernières modifications.

- **`Checking out Revision`** :
  - Jenkins extrait une version spécifique du dépôt (basée sur la branche `main`).

---

## **4. Exécution du pipeline**
- **`[Flask-pipeline] $ /bin/sh -xe /tmp/jenkins...`** :
  - Jenkins exécute un script Shell pour cette étape.
  - Ce script semble être défini dans le pipeline (par exemple, un fichier `build.sh` ou une étape dans un Jenkinsfile).

- **Contenu du script exécuté** :
  - Une commande simple est exécutée : `echo 'Hello from Jenkins'`.
  - La sortie montre que le script s’est exécuté correctement, et le message "Hello from Jenkins" est affiché.

---

## **5. Résultat final**
- **`Finished: SUCCESS`** :
  - Le job s’est terminé avec succès. Cela indique que toutes les étapes du pipeline ont été exécutées sans erreur.

---

## **Résumé : Ce que montre cette capture**
- Un job Jenkins a été déclenché par un push GitHub.
- Jenkins a correctement récupéré les changements depuis le dépôt GitHub.
- Un script simple (écho d’un message) a été exécuté.
- Le job s’est terminé sans problème.

---

## **Prochaines étapes possibles**
1. **Configurer des étapes supplémentaires dans le pipeline** :
   - Compilation d’un projet.
   - Lancement de tests unitaires.
   - Déploiement d’une application (par exemple, Flask).

2. **Vérifier les notifications** :
   - Configurer des alertes par email ou Slack pour informer en cas de succès ou d’échec.

3. **Améliorer le pipeline** :
   - Ajouter un fichier `Jenkinsfile` pour définir un pipeline plus complexe en utilisant une syntaxe déclarative ou scriptée.





