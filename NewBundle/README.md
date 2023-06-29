La plataforma incluye un servidor de Autenticación basado en OAuth2 que permite a los usuarios autenticarse en la plataforma.

Es el método de autenticación recomendado para realizar autenticación contra plataforma (Oauth Server), Implementa el estandar OAuth e incluye todo el ciclo de gestión de Tokens. Además posibilita la utilización de los Dominios de Seguridad (Realms) integrados con dicha gestión.

Para ampliar la información se puede consulta la siguiente entrada:

[(Security) (ES) Gestión de tokens en autenticación OAuth2
](https://onesaitplatform.atlassian.net/wiki/spaces/OP/pages/56000785)

Como introducción básica, a continuación se incluye el ejemplo de generación de un Token OAuth2 para un usuario:

GENERACION DE TOKEN UTILIZANDO SERVIDOR OAUTH2
El endpoint que permite generar tokens Oauth2 se correspondería con:

https://<myserver>/oauth-server/oauth/token

Utilizaremos el entorno de plataforma desplegado en nuestro cloudlab para mostrar los ejemplos:

https://lab.onesaitplatform.com/oauth-server/oauth/token

Será una petición POST, y debe incluir:

Headers:
- Authorization: (onesaitplatform:onesaitplatform en base64) Son las credenciales por defecto de la plataforma.

Body:


1. grant_type: password (para peticiones User/Password)
2. username: id de usuario
3. password: contraseña de usuario