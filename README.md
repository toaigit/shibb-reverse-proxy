# SP SAML with Apache with Shibboleth and proxypass to backend server
Simple Apache with Shibboleth (SAML SP) sitting in front of tomcat/backend container.
*  Please see README.toai, SHIBB.md, SSO.md and PROXY.md for more detail
*  You also need to install gomplate and docker-compose from:
     ```
     curl -o gomplate -sSL https://github.com/hairyhenderson/gomplate/releases/download/v3.11.5/gomplate_linux-amd64 
     curl -o docker-compose -SL https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-x86_64
     chmod 755 gomplate docker-compose
     ```
