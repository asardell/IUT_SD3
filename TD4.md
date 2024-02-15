# Création d'environnement dans Snowflake

## OBJECTIFS

Voici les objectifs de ce cours :
- [ ] Créer un compte de stockage dans Azure
- [ ] Créer un compte d'essai Snowflake
- [ ] Créer un storage integration sur Snowflake pour se connecter à Azure
- [ ] Créer une database dans Snowlfake 

## TD4

1. Créer une database dans Snowlfake

```sql
USE ROLE ACCOUNTADMIN; 
--Database creation DEV -------------------
CREATE OR REPLACE DATABASE DB_IUT_SD3;
----- setup Time Travel PROD 1 day
ALTER DATABASE DB_IUT_SD3 SET DATA_RETENTION_TIME_IN_DAYS=1;
```

2. Créer un storage integration dans Snowlfake vers le storage account

```sql
CREATE STORAGE INTEGRATION SINT_IUT_SD3
  TYPE = EXTERNAL_STAGE
  STORAGE_PROVIDER = 'AZURE'
  ENABLED = TRUE
  AZURE_TENANT_ID = 'xxxx'
  STORAGE_ALLOWED_LOCATIONS = ('azure://xxxx.blob.core.windows.net/{container_name}/')
```

3. Créer un stage vers le bon dossier

```
CREATE OR REPLACE STAGE DB_IUT_SD3.PUBLIC.STAGE_NAME
  URL='azure://{storage_account_name}.blob.core.windows.net/{container_name}/'
  CREDENTIALS=(AZURE_SAS_TOKEN='xxx');
```

## Liens utiles

- https://docs.snowflake.com/en/sql-reference/sql/create-storage-integration#examples
- https://docs.snowflake.com/en/user-guide/data-load-azure-create-stage
- https://learn.microsoft.com/en-us/azure/ai-services/document-intelligence/create-sas-tokens?view=doc-intel-4.0.0
