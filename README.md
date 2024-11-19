# Projet-DevOps
## install and configure Jenkins ( master and agent )
### Création d'une instance EC2 sur AWS
L'instance EC2 nous offre un serveur cloud évolutif pour héberger nos services.
#### Nom de l'instance :
![image](https://github.com/user-attachments/assets/1b7fa42f-d7fd-41b9-91ef-0cc422821bb0)
#### Configuration de l'instance :

![image](https://github.com/user-attachments/assets/cdf1d8da-4341-4d4b-8379-82ef1f0ab2c0)

![image](https://github.com/user-attachments/assets/517a1e27-c277-4553-829f-ba288a167d77)

#### Création de la paire de clés :

![image](https://github.com/user-attachments/assets/aadbf00a-8c7f-4fa9-897b-eaf639c7f4a2)

#### Configuration du stockage :

![image](https://github.com/user-attachments/assets/55e53a7f-12c1-40d0-b468-7b7ae1edeeef)

#### Lancement de l'instance :

![image](https://github.com/user-attachments/assets/523073dc-e609-4364-9bcd-cb5f3fd9661b)

#### Association d'une Elastic IP :

![image](https://github.com/user-attachments/assets/2709b8f0-deae-4af3-b0a3-2c553246b823)

#### Vérification de l'adresse IP associée :

![image](https://github.com/user-attachments/assets/099c2d92-d5c7-4f5a-ba20-5070adeadf90)

#### Connexion SSH à l'instance via MobaXterm :

![image](https://github.com/user-attachments/assets/15daee7f-3af7-41ee-8ae5-ad0e92710574)

#### Vérification finale :

![image](https://github.com/user-attachments/assets/27a96cc4-1795-4ef7-8dae-0647436fd09a)
![image](https://github.com/user-attachments/assets/c32e8834-43c6-4419-9019-380e0cbc4b4c)
#### instalation java 
sudo apt install openjdk-17-jre 
![image](https://github.com/user-attachments/assets/ee92ca85-daa3-4717-b87e-9814918ca4c2)

#### jenkins work in port 8080
![image](https://github.com/user-attachments/assets/81e55caa-20d9-4612-9a70-76c0014c2b37)
#### installer jenkins 
##### link to the page off of Jenkins
https://www.jenkins.io/doc/book/installing/linux/#debianubuntu
##### command to download Jenkins 
curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
#### le bon fonct de Jenkins
![image](https://github.com/user-attachments/assets/adfdbc0f-9893-47ef-806f-1becc324273f)
#### creation d'une nouvelle instance Jenkins-Agent
![image](https://github.com/user-attachments/assets/d8526795-d4f7-40df-abb3-56f89eb49817)
#### on va installer java et assurer la connexion sur 8080 ici aussi 
#### installation docker 
sudo apt-get install docker.io
![image](https://github.com/user-attachments/assets/98d555ef-b583-4c4b-b875-b4c006eb8299)
![image](https://github.com/user-attachments/assets/1131cd55-1a71-4d1c-a419-42c793227107)
#### inJenkins-Agent
![image](https://github.com/user-attachments/assets/506d6a4c-6293-4977-a0a2-ae3ed151822b)
#### in Jenkins-Master
![image](https://github.com/user-attachments/assets/702ecc0f-ce6c-4d2c-9db2-8753c3be89de)
#### generer key
![image](https://github.com/user-attachments/assets/bf68ca05-60c0-4fe9-adfc-c4ff9c834145)

copier pub key of master in auth of agent
![image](https://github.com/user-attachments/assets/2922b134-58c8-4486-8cf6-a5b65378ea68)
![image](https://github.com/user-attachments/assets/d7a518b4-a8ae-4bb9-8008-39ae6d5dab39)
page web Jenkins-Master
![image](https://github.com/user-attachments/assets/64d2bfb8-1054-497c-94fc-e38d23704f3b)
pass
![image](https://github.com/user-attachments/assets/65cdf149-689f-472b-a2f8-427846327641)
plugin instalation 
![image](https://github.com/user-attachments/assets/5b2667bc-89d0-4364-a632-d69b99f9e0eb)
# Jenkins
![image](https://github.com/user-attachments/assets/5637c5f2-3d13-409d-8979-ec03ae1f0bca)

#### copier private key of master jenkins when we create nodes 
![image](https://github.com/user-attachments/assets/95c58bd5-6403-4552-a775-ba901b717f71)
#### add nodes 
![image](https://github.com/user-attachments/assets/e41cb523-5c92-4fe1-8c1f-62784dbd7dae)
#### c'est ca 
![image](https://github.com/user-attachments/assets/eb2ea2a7-5bf5-40fc-b7fa-37b631d24b27)
#### adding node (Jenkins-Agent)
![image](https://github.com/user-attachments/assets/cfb98d4a-e36d-4102-95df-0d9698297404)
#### testing Jenkins fonct
![image](https://github.com/user-attachments/assets/135694c4-f572-4721-b7cf-751369a60fb7)
# Integrate maven to Jekins and add github credentials to jenkins
#### install plugin
![image](https://github.com/user-attachments/assets/8fcb0457-b67a-48e0-988c-586c79619693)
#### install maven
![image](https://github.com/user-attachments/assets/19624137-4396-40fe-9071-64e93584b0cd)
#### install jdk
![image](https://github.com/user-attachments/assets/e9ee7034-02a4-4094-b59f-ef175ac30e2f)
#### integration of github
![image](https://github.com/user-attachments/assets/200dc54d-001f-4a9c-8a2e-61644662ac9b)
# Create pipline script for build and test artifacts and create ci job on jenkins
#### import script of app from github 
![image](https://github.com/user-attachments/assets/618e9c7f-9041-4d9d-87f3-a87a4dcffa69)
