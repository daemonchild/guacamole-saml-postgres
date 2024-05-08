# guacamole-saml-postgres
Apache Guacamole, Postgres and SAML authentication

You need:

1) An Azure account with permissions to build an Enterprise Application.
2) A FQDN for your Guacamole application.

**Optional**: An nginx proxy with SSL. (Like this: https://github.com/daemonchild/nginx-guacamole-proxy)

Copy the sample environment file to .env.
Edit the .env file. You will need details from your SAML provider.


``` 
# docker-compose build
# docker-compose -d up
```

Then connect to port 8080.
