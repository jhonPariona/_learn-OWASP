# OWASP Ten

## [2017](https://owasp.org/www-project-top-ten/OWASP_Top_Ten_2017/)

### [A1:2017-Injection](https://owasp.org/www-project-top-ten/OWASP_Top_Ten_2017/Top_10-2017_A1-Injection.html)

Inyección SQL, [NoSQL](https://github.com/search?q=Nosql+injection), OS, LDAP

**Tools**

[SQLmap cli](https://github.com/sqlmapproject/sqlmap) |
[sqlMAP ui](https://github.com/Hood3dRob1n/SQLMAP-Web-GUI) |
[NoSQLmap](https://github.com/codingo/NoSQLMap)

**✔ Soluciones**

- Usar prepared statement(php)
- usar ORM

### A2:2017-Broken authentication

Inicio de sesion no implementadas correctamente

**Ataques**

- Fuerza bruta mediante proxis(burpsuite)

**Tools**

Hydra | 
[diccionarios](https://wiki.skullsecurity.org/Passwords) |
[zap ataque diccionarios](https://owasp.org/www-project-zap/)

**✔ Soluciones**

- Captchas 3.0 ya que ya hay una vulnerabilidad en el 2.0(audio)
- segundo factor de autenticación
- usar framework para implementar logins
- contraseñas seguras

### A3:2017-Sensitive Data Exposure

**✔ Soluciones**

- Usar certificados HTTPS
- Guardar contraseñas hasheadas con algoritmos seguros(sha256) y aplicando un salt

### A4:2017-XML External Entities(XXE)

** ✔ Soluciones**

- usar JSON
- usar parseadores de XML y validarlos

### A5:2017-Broken acces control

restricciones en lo que puede hacer o no un usuario autenticado

**LFI**
Configuracion erronea del server que permite listar archivos o ejecutar comandos

### A6:217-Security misconfiguration

Configuraciones erroneas

**Tools**

- Listar [buckets aws inseguros](https://github.com/eth0izzle/bucket-stream)

### A7:217-Cross Site Scripting

Permite inyectar HTML o Javascript

**Tipos**

- Reflejado inyecta a una url específica solo se ejecuta si se ingresa con la url con la que se hizo la inyeccion
- Persistente se inyecta en un campo de la web(comentario) y siempre se va a ejecutar
- DOM XSS

**Tools**

[XSStrike](https://github.com/s0md3v/XSStrike)

** ✔ Soluciones**

- LImpieza y validación de datos

### A8:217-Insecure Deserialización

### A9:217-Using COmponents with Known Vulnerabilities

** ✔ Soluciones**

- Estar atento a las [vulnerabilidades](https://github.com/jhonPariona/_learn-pentesting/blob/master/scanning.md#-organismos-y-p%C3%A1ginas-de-vulnerabilidades)

### A10:217-Insufficient Logging & Monitoring

Usar logs monitorizados para detectar incidentes de ataques DFIR(Digital forensics and inciden response )



