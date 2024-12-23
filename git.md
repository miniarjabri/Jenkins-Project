## Integrating with GitHub

use this project: 

https://github.com/kodekloudhub/jenkins-project

![image](https://github.com/user-attachments/assets/1380821d-ba52-4b4e-8d25-ea9e76d35556)


### specify the build triggers

when Jenkins should automatically run a build

![image](https://github.com/user-attachments/assets/28ff1310-240b-4fea-8882-d34f1274ebe2)


- GitHub hook trigger for GITScm polling: github repo notify jenkins agent and the agnet will run the build

![image](https://github.com/user-attachments/assets/309f5f65-8120-4f11-836d-5a1f2cd762dc)

- select execute Shell
## GitHub Repo
- go to setting
- click on "Webhoocks"
- select "add webhook"
![image](https://github.com/user-attachments/assets/a1386cd4-349d-4e55-ab7c-906638edb194)

- in "Payload url" put the jenkins url "http://localhost:8080/github-webhook"
- content type: application server
- which event would like to trigger this webhook?

![image](https://github.com/user-attachments/assets/204e892c-39dc-4982-bade-c1d1745b7502)

![image](https://github.com/user-attachments/assets/6292fe95-a83a-49c8-8b57-1ca2c8ded715)





