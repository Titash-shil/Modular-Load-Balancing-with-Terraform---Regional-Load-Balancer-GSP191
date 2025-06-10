# Modular Load Balancing with Terraform - Regional Load Balancer || [GSP191](https://www.cloudskillsboost.google/focuses/1207?parent=catalog) ||

## # Like, comment, share & Don't forget to subscribe [Qwiklab_Explorers](https://youtube.com/@qwiklabexplorers?si=QGN7mY2Sn9iobmuz) 👍😄🤝

---
## ⚠️ **Disclaimer:**
#### This script and guide are provided for educational purposes to help you understand the lab process. Please ensure you understand the steps before using any scripts. Before using the script, I encourage you to open and review it to understand each step.The goal is to help you learn how to complete the labs effectively while following Qwiklabs' terms of service and YouTube's community guidelines.
---

 - ### Copy & Run the Commands in Cloud Shell Terminal :

```
export REGION=
```
```
gcloud auth list

gcloud config set compute/region $REGION

git clone https://github.com/GoogleCloudPlatform/terraform-google-lb
cd ~/terraform-google-lb/examples/basic

export GOOGLE_PROJECT=$(gcloud config get-value project)

terraform init

sed -i 's/us-central1/'"$REGION"'/g' variables.tf

terraform plan

terraform apply

EXTERNAL_IP=$(terraform output | grep load_balancer_default_ip | cut -d = -f2 | xargs echo -n)

echo "http://${EXTERNAL_IP}"

```
---

## Congratulations ..!!🎉  You completed the lab shortly..😃💯

## *Well done..!* 👏

## Thank you for visiting.... :) 🗯️

## [Qwiklab_Explorers](https://youtube.com/@qwiklabexplorers?si=QGN7mY2Sn9iobmuz)

## Join to our community [Digital Dominators](https://linktr.ee/digital_dominators)
