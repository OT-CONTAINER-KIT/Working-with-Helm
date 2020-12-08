# Working-with-Helm

# Helm Lab 01

<p align="center">
  <img width="460" height="300" src="Images/helm.png">
</p>

----

<p> Helm helps you manage Kubernetes applications — Helm Charts help you define, install, and upgrade even the most complex Kubernetes application. </p>

<br>

<p> Charts are easy to create, version, share, and publish — so start using Helm and stop the copy-and-paste. </p>


## Purpose

<p> The purpose of creating this application is to provide an individual, a holistic idea of helm, helm charts, architecture, it's working, and its setup. </p>

### Preliminary

* Please work in a group

* We will let a fun service decide your teamname: http://creativityforyou.com/combomaker.html

* Select a leader of your group, they will need a public Github account and generate a token

* The leader should provide a token to the administrator, via virtual chat, slack, or email

# Architecture

<p align="center">
  <img width="460" height="300" src="Images/helm 2.png">
</p>

## Applications

```bash
* To use a publically available Helm Chart(V3)

* We will be install MySQL
```
### Guide

* To install Helm

```bash
wget https://get.helm.sh/helm-v3.0.0-linux-amd64.tar.gz

tar -xvzf helm-v3.0.0-linux-amd64.tar.gz

cd linux-amd64

mv helm /usr/bin/
```

* Add and Update Repo

```bash
helm repo add stable https://charts.helm.sh/stable

helm repo update
```

* View information about your chart(MySql)

```bash
helm show chart stable/mysql
```

* To install chart

```bash
helm install <release-name> <repo>/<name>
Use : helm install mysql stable/mysql --namespace <name given to created namspaces>
```

* To List

```bash
helm list <this will list the deployed ones in default namespace>
helm list --namespace <name given to created namspaces>
```

* To show values

```bash
helm show values stable/mysql
```

* To upgrade

```bash
helm upgrade mysql stable/mysql --namespace <name given to created namspaces>
```

* To Uninstall

```bash
helm uninstall <release-name>
Use : helm uninstall mysql
```

