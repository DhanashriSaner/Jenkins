# Jenkins

### Step 1) Clone the repository
```
https://github.com/LondheShubham153/django-notes-app.git
```
### Step 2) Update the system
```
sudo apt-get update
```
### Step 3) Install Docker
```
sudo apt install docker.io
```
### Step 4) Check the Docker version and run the following command
```
Docker --version
```
```
Docker ps
```
We will face permission denied issue, let's solve it by running the below command

```
sudo usermod -aG docker $USER
```
Then reboot the system
```
sudo reboot
```

### Step 5) Build the Docker Image from Dockerfile
```
docker build -t notes-app .
```

## Jenkins

![image](https://github.com/DhanashriSaner/Jenkins/assets/88526990/9538597e-5dad-4e25-a46f-1cfb91f6f334)

## Installation of Jenkins

### Step 6) Install JDK
```
sudo apt update
```

```
sudo apt install openjdk-17-jre
```

**check java version**

```
java -version
```
### Step 7) Install Jenkins for Linux(Ubuntu)
```
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
```

## Interview Question

#### 1) What is the meaning of processing triggers for man-db?

![image](https://github.com/DhanashriSaner/Jenkins/assets/88526990/5a9dbed3-0bfe-4d9b-ade1-10d2bfd4d140)


**mandb** is used to initialize or manually update index database caches.

#### 2) On which Ports the Jenkins runs as default?
**Solution** The default Jenkins installation runs on ports 8080 and 8443

### Check whether Jenkins is working or not

```
service jenkins status
```
![image](https://github.com/DhanashriSaner/Jenkins/assets/88526990/a8cfe691-f3ab-49b7-a27f-ac91ceff8a09)

### Pipeline Code

```
pipeline{
    agent any
    
    stages{
        stage("Code"){
            steps{
                echo "Clonning the Code"    
            }
        }
        stage("Build"){
            steps{
                echo "Building the Image"   
            }    
        }
        stage("Push to Docker Hub"){
            steps{
                echo "Pushing the image to Docker Hub"    
            }    
        }
        stage("Deploy"){
            steps{
                echo "Deploying the Container"    
            }    
        }
    }
}
```

![image](https://github.com/DhanashriSaner/Jenkins/assets/88526990/9ba5ac24-ae46-4333-b9a0-9eb979c7a4f1)

## Error 
**Jenkins User is not present inside Docker Group**

![image](https://github.com/DhanashriSaner/Jenkins/assets/88526990/fb7e8542-d153-4f6d-9a99-626c3ab2e476)

### Solution
**Use the below command to add Jenkins user**
```
sudo apt usermod -aG docker $USER
```

