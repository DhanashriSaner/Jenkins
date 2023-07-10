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



