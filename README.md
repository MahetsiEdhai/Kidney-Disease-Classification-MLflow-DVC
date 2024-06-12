# Kidney-Disease-Classification-MLflow-DVC
---

## Workflows

1. Update config.yaml
2. Update secrets.yaml [Optional]
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src config
6. Update the components
7. Update the pipeline 
8. Update the main.py
9. Update the dvc.yaml
10. app.py

# How to run? (¿cómo ejecutarlo?)
### STEPS: (PASOS:)

Clone the repository (clonamos el repositorio)

```bash
https://github.com/MahetsiEdhai/Kidney-Disease-Classification-MLflow-DVC
```
### STEP 01- Create a conda environment after opening the repository (creamos entorno en conda y despues abrimos el repositorio)

```bash
conda create -n cnncls python=3.8 -y
```

```bash
conda activate cnncls
```


### STEP 02- install the requirements (instalamos los requirimientos)
```bash
pip install -r requirements.txt
```

```bash
# Finally run the following command
python app.py
```

Now,
```bash
open up you local host and port
```






## MLflow

- [Documentation](https://mlflow.org/docs/latest/index.html)

- [MLflow tutorial](https://youtu.be/qdcHHrsXA48?si=bD5vDS60akNphkem)

##### cmd
- mlflow ui

### dagshub
[dagshub](https://dagshub.com/)

MLFLOW_TRACKING_URI=https://dagshub.com/entbappy/Kidney-Disease-Classification-MLflow-DVC.mlflow \
MLFLOW_TRACKING_USERNAME=entbappy \
MLFLOW_TRACKING_PASSWORD=6824692c47a369aa6f9eac5b10041d5c8edbcef0 \
python script.py

Run this to export as env variables:

```bash

export MLFLOW_TRACKING_URI=https://dagshub.com/entbappy/Kidney-Disease-Classification-MLflow-DVC.mlflow

export MLFLOW_TRACKING_USERNAME=entbappy 

export MLFLOW_TRACKING_PASSWORD=6824692c47a369aa6f9eac5b10041d5c8edbcef0

```


### DVC cmd

1. dvc init
2. dvc repro
3. dvc dag


## About MLflow & DVC

MLflow

 - Its Production Grade (su grado de producció)
 - Trace all of your expriements (Rastrear todos tus experimentos)
 - Logging & taging your model (Registro y etiquetado de tu modelo)


DVC 

 - Its very lite weight for POC only (Es muy ligero, solo para POC (Proof of Concept))
 - lite weight expriements tracker (Ligero rastreador de experimentos)
 - It can perform Orchestration (Creating Pipelines)  (Puede realizar Orquestación (Creación de pipelines))



# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console. (Inicia sesión en la consola de AWS.)

## 2. Create IAM user for deployment (Crea un usuario IAM para implementación)

	#with specific access (con acceso especifico)

	1. EC2 access : It is virtual machine (Acceso a EC2: Es una máquina virtual.)

	2. ECR: Elastic Container registry to save your docker image in aws (ECR: Registro de contenedores elástico para guardar tu imagen de Docker en AWS.)


	#Description: About the deployment (Descripción: Acerca de la implementación)

	1. Build docker image of the source code (Construye la imagen de Docker del código fuente.)

	2. Push your docker image to ECR (Sube tu imagen de Docker a ECR.)

	3. Launch Your EC2  (Inicia tu instancia EC2.)

	4. Pull Your image from ECR in EC2 (Descarga tu imagen desde ECR en EC2.)

	5. Lauch your docker image in EC2 (Ejecuta tu imagen de Docker en EC2.)

	#Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Create ECR repo to store/save docker image (Crear repositorio ECR para almacenar/guardar imágenes Docker.)
    - Save the URI: 566373416292.dkr.ecr.us-east-1.amazonaws.com/chicken

	
## 4. Create EC2 machine (Ubuntu) (Crear máquina EC2 (Ubuntu).)

## 5. Open EC2 and Install docker in EC2 Machine: (Abre EC2 e instala Docker en la máquina EC2.)
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner: (Configura EC2 como un runner autohospedado.)
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets: (Configura secrets en GitHub)

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = us-east-1

    AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

    ECR_REPOSITORY_NAME = simple-app

---
---
## Josué Olvera (m4h3t51)
---
