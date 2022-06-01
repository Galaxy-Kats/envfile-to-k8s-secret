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
docker run galaxyart/envfile-to-k8s-secret <k8s name> <k8s namespace> <base64-encoded .env string>
```

<br/><br/>

* Mac/Linux example:
```bash
docker run galaxyart/envfile-to-k8s-secret my-secret my-namespace $(cat .env | base64) > my-secret.yaml
```

<br/><br/>

* Some other linux version may need this example:
```bash
docker run galaxyart/envfile-to-k8s-secret my-secret my-namespace $(cat .env | base64 -w 0) > my-secret.yaml
```
