# OWASP Ten

## 📁 Diapos

[Escaneo vulnerabilidades](https://drive.google.com/open?id=1YiZm06JGiYAoOUujAMF5F6HaUAHTZIRv)

## 🛠 Maquinas de prueba

### [DVWA](https://github.com/ethicalhack3r/DVWA)

Web hecha en php con vulnerabilidades para practicar

- Correr con docker `docker run --rm -it -p 80:80 vulnerables/web-dvwa`
- abrir navegador escribir `localhost` o `172.17.0.2`
- Por defecto tiene la seguridad en alta tenemos que cambiarla a baja para poder probar los fallos(DVWA security)

### [XVNA](https://github.com/vegabird/xvna)

Web hecha en node con vulnerabilidades

- En su [youtube](https://www.youtube.com/watch?v=jAOGlf4eoic&list=PLl3MvLA31T7LCIP7Lzlc9EDVURD6wEt5J) tiene videos de como explotar cada vulnerabilidad

### [Diva Android](https://github.com/payatu/diva-android)

App de android con vulnerabilidades

### [damnvulnerableiosapp](http://damnvulnerableiosapp.com/)

App en ios con vulnerabilidades

## ✨ [2017](https://owasp.org/www-project-top-ten/OWASP_Top_Ten_2017/)

### 🚀 [A1:2017-Injection](https://owasp.org/www-project-top-ten/OWASP_Top_Ten_2017/Top_10-2017_A1-Injection.html)

Inyección SQL, [NoSQL](https://github.com/search?q=Nosql+injection), OS, LDAP

**Tools**

[SQLmap cli](https://github.com/sqlmapproject/sqlmap) |
[sqlMAP ui](https://github.com/Hood3dRob1n/SQLMAP-Web-GUI) |
[NoSQLmap](https://github.com/codingo/NoSQLMap)

**✔ Soluciones**

- Usar prepared statement(php)
- Validación es mejor en el backend en el frontend podria ser por usabilidad pero no es seguro ya que el user puede desactivarlas.
- Usar ORMS ya que ya contienen soluciones frente a estos problemas.
- Usar Querys parametrizadas, ..
- siempre usar inputs validation nunca confiar en lo que el usuario nos podria enviar

### 🚀 A2:2017-Broken authentication

Inicio de sesion no implementadas correctamente

**Ataques**

- Fuerza bruta mediante proxis(burpsuite)

**Tools**

Hydra | 
[diccionarios](https://wiki.skullsecurity.org/Passwords) |
[zap ataque diccionarios](https://owasp.org/www-project-zap/) |
[WPForce para wordpress](https://github.com/n00py/WPForce)

**✔ Soluciones**

- Captchas 3.0 ya que ya hay una vulnerabilidad en el 2.0(audio)
- segundo factor de autenticación
- usar framework para implementar logins
- contraseñas seguras
- usar frameworks como spring security
- Forzar la autenticación para todas las urls
- No es recomendable las preguntas seguras
- No admitir jwt sin firmar
- El secreto compartido de jwt debe de ser muy seguro sino se puede romper con jhon the ripper

### 🚀 A3:2017-Sensitive Data Exposure

**✔ Soluciones**

- Usar certificados HTTPS
- Guardar contraseñas hasheadas con algoritmos seguros(sha256) y aplicando un salt
- Se debe de usar https
- no es recomendado MD5, mejor es sha256
- pbkdf2 es mejor para guardar contraseñas


### 🚀 A4:2017-XML External Entities(XXE)

** ✔ Soluciones**

- usar parseadores de XML y validarlos
- Usar mejor JSON(No tiene Entity)
- Si usamos XML y no usamos Entity desactivarlos.

### CSRF Cross site request forgery

- caad vez que se haga una peticion usar un nuevo token
- no usar token statico
- usar frameworks que ya implementas estas soluciones

### 🚀 A5:2017-Broken acces control

restricciones en lo que puede hacer o no un usuario autenticado

**LFI**
Configuracion erronea del server que permite listar archivos o ejecutar comandos

**Enumeración de usuarios**

autenticar para poder enumerar usuarios(proteger quien puede enumerar usuarios o el tiempo en q se hace esaas peticiones)

** ✔ Soluciones**

- No devolver informacion que no se va a pintar en el front

### 🚀 A6:217-Security misconfiguration

Configuraciones erroneas

**Tools**

- Listar [buckets aws inseguros](https://github.com/eth0izzle/bucket-stream)
- quien tiene autorizacion de hacer aciones en nuestros enpoints
- Dejar solo lo neesario para la producción
- Controlar accesos, numero de logins que pueden hacer los usuarios
- subir el codigo en modo debug

### 🚀 A7:217-Cross Site Scripting

Permite inyectar HTML o Javascript

**Tipos**

- Reflejado inyecta a una url específica solo se ejecuta si se ingresa con la url con la que se hizo la inyeccion
- Persistente se inyecta en un campo de la web(comentario) y siempre se va a ejecutar
- DOM XSS

**Tools**

[XSStrike](https://github.com/s0md3v/XSStrike)

** ✔ Soluciones**

- LImpieza y validación de datos

### 🚀 A8:217-Insecure Deserialización

### 🚀 A9:217-Using COmponents with Known Vulnerabilities

** ✔ Soluciones**

- Estar atento a las [vulnerabilidades](https://github.com/jhonPariona/_learn-pentesting/blob/master/scanning.md#-organismos-y-p%C3%A1ginas-de-vulnerabilidades)

### 🚀 A10:217-Insufficient Logging & Monitoring

Usar logs monitorizados para detectar incidentes de ataques DFIR(Digital forensics and inciden response )



