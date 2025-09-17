# itti-metabase-self-tools

Configurar el healthcheck en `/api/health`

Las principales envs a agregar son las de conexión a la base de datos, y el puerto en el que corre jetty (8080 por defecto).

```shell
MB_DB_TYPE=postgres
MB_DB_DBNAME=metabase
MB_DB_PORT=5432
MB_DB_USER=metabase_app
MB_DB_PASS=A8skW9b0CsMhm7lcLo2nPX
MB_DB_HOST=prod-strategysql-pgsql-sa-east-1-primary.cr8quyycoj4n.sa-east-1.rds.amazonaws.com

#Puerto 8080 por defecto
MB_JETTY_PORT=8080

#SMTP
MB_EMAIL_FROM_ADDRESS=
MB_EMAIL_SMTP_HOST=
MB_EMAIL_SMTP_PASSWORD=
MB_EMAIL_SMTP_PORT=
MB_EMAIL_SMTP_SECURITY=
MB_EMAIL_SMTP_USERNAME=

#Clave de encriptado de databases
MB_ENCRYPTION_SECRET_KEY=
```

Genera la clave de encriptado con:

```shell
openssl rand -base64 32
```

[https://www.metabase.com/docs/latest/configuring-metabase/environment-variables](https://www.metabase.com/docs/latest/configuring-metabase/environment-variables)

[https://www.metabase.com/docs/latest/configuring-metabase/email](https://www.metabase.com/docs/latest/configuring-metabase/email)

---
Para más detalles, consulta la documentación interna de redash (variables y configuración) o contacta al equipo Plataforma itti Arquitectura.
