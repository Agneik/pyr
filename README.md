# UPAX SLS GRUPO DRAGON

Repositorio que incluye los Web Services para el Proyecto de Citas Grupo Dragon

## Prerequisitos

Instalar **Flask**

```bash
pip install Flask flask_cors
```

Instalar herramientas para integración de **Oracle**
```bash
pip install cx_Oracle
```

Instalar **boto3**
```bash
pip install boto3
```

Para hacer deploy en AWS, mediante el framework [serverless](https://serverless.com/)

```bash
npm install -g serverless
```

Configura credenciales de AWS

```bash
serverless config credentials --provider aws --key YOUR_KEY_ID --secret YOUR_SECRET_KEY --profile PROFILE
```

Instala plugins de serverless

```bash
sls plugin install -n serverless-wsgi --stage DOMAIN 

sls plugin install -n serverless-python-requirements --stage DOMAIN

npm i serverless-deployment-bucket

npm i serverless-domain-manager
```

## Deploy

#### Local Deployment
```bash
sls wsgi serve
```

#### AWS Deployment
```bash
sls deploy --aws-profile YOUR_PROFILE
```

Sintáxis en archivo **serverless.yml**

**service**: upx-sls-servicename

**deploymentBucket** name: upax-serverless-api

**apiName**: upx-sls-servicename-API

**stackName**: upx-sls-servicename-cloudformation  
