# DevOps-Project-3-tier-Application-Deployment
![image](https://github.com/singhritesh85/DevOps-Project-3-tier-Application-Deployment/assets/56765895/da9fb238-073b-4b68-8f83-90ed31ba7256)
<br><br/>
The Source Code for this project is present in the GitHub Repository https://github.com/singhritesh85/TWSThreeTierAppChallenge.git inside the directory Application-Code.
<br><br/>
1. This is a three tier application (of Things-to-Do App) in which frontend or presentation layer is React Js code which is present in the directory Application-Code/frontend in the GitHub Repo https://github.com/singhritesh85/TWSThreeTierAppChallenge.git. To deploy React Js code I have created a Jenkins Job using declarative pipeline.
2. The Backend or Application layer is Node Js code which present in the directory Application-Code/backend in the GitHub Repo https://github.com/singhritesh85/TWSThreeTierAppChallenge.git. To deploy Node Js code I have created a Jenkins Job using declarative pipeline.
3. For Database or Data layer MongoDB has been used. To deploy MongoDB I have created a Jenkins Job using declarative pipeline.
<br><br/>
As discussed above there are three Jenkins Job using which ReactJs code, NodeJs code and MongoDB have been deployed. which is also shown in the Architechture diagram above. The Jenkinsfile for ReactJs Code, NodeJs Code and MongoDB is present inside the directory Jenkins-Pipeline in this Repository. Before Running Jenkins Job for MongoDB create the password, pv (persistent volume) and pvc (persistent volume claim). To do so run the command kubectl apply -f pv.yaml, kubectl apply -f pvc.yaml and kubectl apply -f secrets.yaml. The password for MongoDB is encrypted with base64. 
<br><br/>
```
Encryption with Base64
==================================
echo "admin"|base64 -----------> Encrypt the username
ehco "password123"|base64  --------------> Encrypt the password


Decryption with Base64
==================================
echo "YWRtaW4="|base64 --decode
echo "cGFzc3dvcmQxMjM="|base64 --decode
```
