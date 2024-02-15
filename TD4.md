# Création d'environnement dans Snowflake

## OBJECTIFS

Voici les objectifs de ce cours :
- [ ] Créer un compte de stockage dans Azure
- [ ] Créer un compte d'essai Snowflake
- [ ] Créer un storage integration sur Snowflake pour se connecter à Azure
- [ ] Créer une database dans Snowlfake 

## TD4

1. Créer une database dans Snowlfake

```
USE ROLE ACCOUNTADMIN; 
--Database creation DEV -------------------
CREATE OR REPLACE DATABASE DB_IUT_SD3;
----- setup Time Travel PROD 1 day
ALTER DATABASE DB_IUT_SD3 SET DATA_RETENTION_TIME_IN_DAYS=1;
```

1. Créer une database dans Snowlfake


## Liens utiles

- https://docs.snowflake.com/en/sql-reference/sql/create-storage-integration#examples
- https://docs.snowflake.com/en/user-guide/data-load-azure-create-stage
