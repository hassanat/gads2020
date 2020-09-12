#Google Cloud Fundamentals: Getting Started with Compute Engine
##Create a virtual machine using the gcloud command line
gcloud compute zones list | grep us-central1
gcloud config set compute/zone us-central1-b
gcloud compute instances create "my-vm-2" \
--machine-type "n1-standard-1" \
--image-project "debian-cloud" \
--image "debian-9-stretch-v20190213" \
--subnet "default"
exit
###Connect between VM instances
ping my-vm-1
ssh my-vm-1
sudo apt-get install nginx-light -y
sudo nano /var/www/html/index.nginx-debian.html
Hi from YOUR_NAME
curl http://localhost/
exit
curl http://my-vm-1/
exit