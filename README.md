# Jenkins-Project
## 1.Setting up the environnment
1.1. Create EC2 instance

![image](https://github.com/user-attachments/assets/3c433439-b591-47c2-8235-3b83f408167c)

1.2. Installing Jenkins

use commands here: https://www.jenkins.io/doc/tutorials/tutorial-for-installing-jenkins-on-AWS/

![image](https://github.com/user-attachments/assets/19b520a2-3735-44bb-b15e-72bb9ff87e3d)

1.3. URL : http://54.167.60.197:8080 

![image](https://github.com/user-attachments/assets/de08b0f0-7d71-4d73-96f0-c07f714323a9)

## 2.Create Our "Hello World" Jenkins Project
![image](https://github.com/user-attachments/assets/dc38a732-3ab9-4570-a3b1-3c9b72097796)

### advanced project settings : 
choose Pipeline scripts from SCM (if we have a Jenkins file in our repository)
![image](https://github.com/user-attachments/assets/7acc3c05-c457-49aa-b7d6-85db79245eb4)

type script:
```shell 
pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
```
- run on any of our agents
- differents stages for testing, deplying, building...
- every stage has different steps
### click on "build now"
![image](https://github.com/user-attachments/assets/c46b3f45-66e9-4dac-866e-7df6bbc4f8e3)
