# Prerequisites
* docker installed on your machine

# How to use

* Create a `.env` file
```
USERNAME=username
PASSWORD=password
```

<br/>

* docker run timowang1991/envfile-to-k8s-secret <k8s name> <k8s namespace> <base64-encoded .env string>
  * mac/linux example:
```bash
docker run timowang1991/envfile-to-k8s-secret my-secret my-namespace $(cat .env | base64) > my-secret.yaml
```
  * some other linux version may need this example:
```bash
docker run timowang1991/envfile-to-k8s-secret my-secret my-namespace $(cat .env | base64 -w 0) > my-secret.yaml
```
