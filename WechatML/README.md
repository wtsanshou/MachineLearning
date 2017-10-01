

### Create an account in Google Cloud Platform (GCP)

Complete GCP Registration: https://cloud.google.com/free/ <--- In case you are lost here, quick guide: https://cloud.google.com/getting-started/

Go to GCP Console: https://console.cloud.google.com/home

Create a new project:

project id: kudosdata01 [This is uniquie GCP project-id, which you MUST change to your own id.]

project name: kudosdata01 [You MAY change to your own name.]

zone: asia-east1-b [Choose a data center near your location.]

Enable GCP Compute Engine API for new project, using GCP API Manager

### Start Datalab (Jupyter python notebook) using Cloud Shell

Create/Connect a GCP Compute Engine virtual machine to use Datalab: kudosdata01-vm-datalab-workshop <--- In case you are lost here, quick guide: https://cloud.google.com/datalab/docs/quickstarts

```bash
gcloud projects list

gcloud config set core/project kudosdata01 [your own unique project-id]

gcloud config set compute/zone asia-east1-b

datalab create kudosdata01-vm-datalab-workshop --zone asia-east1-b [1st time for creation]

datalab connect kudosdata01-vm-datalab-workshop [2nd time for connection]

datalab stop kudosdata01-vm-datalab-workshop [stop VM after use]
```

### Open google cloud datalab
Click on the *Web Preview* (up-arrow button at top-left), select *port 8081*, and start using Datalab.

#### create a new notebook from datalab folder, then run below two command in notebook cell:

```bash
!git clone https://github.com/telescopeuser/workshop_blog.git

## run it everytime when VM restart
%load workshop_blog/setup_cloud.py
```

## Lesson 1 

**NOTE :** using python 2


