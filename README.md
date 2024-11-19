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


