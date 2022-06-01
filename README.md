# What is this?

This docker command turns `.env` file to k8s secret object yaml file.

<img width="1078" alt="截圖 2022-06-01 下午4 43 46" src="https://user-images.githubusercontent.com/5511042/171364872-cfd32803-b294-456f-8bd7-04604806137b.png">

<br/><br/>


# Prerequisites
* docker installed on your machine

<br/><br/>

# How to use

* Create a `.env` file
```
USERNAME=username
PASSWORD=password
```

<br/><br/>

* Run command
```bash
docker run timowang1991/envfile-to-k8s-secret <k8s name> <k8s namespace> <base64-encoded .env string>
```

<br/><br/>

* Mac/Linux example:
```bash
docker run timowang1991/envfile-to-k8s-secret my-secret my-namespace $(cat .env | base64) > my-secret.yaml
```

<br/><br/>

* Some other linux version may need this example:
```bash
docker run timowang1991/envfile-to-k8s-secret my-secret my-namespace $(cat .env | base64 -w 0) > my-secret.yaml
```
