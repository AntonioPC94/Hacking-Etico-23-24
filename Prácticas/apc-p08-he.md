# Parte 1 - SQLi

La página no permite añadir jugadores a usuarios no autenticados, un formulario nos exige que introduzcamos un usuario y contraseña válidos. 

Lo primero que haremos es comprobar que este formulario es vulnerable a una inyección y aprovecharlo para saltarnos esta protección.

a) Dad un ejemplo de combinación de usuario y contraseña que provoque un error en la consulta SQL generada por este formulario. Apartir del mensaje de error obtenido, decid cuál es la consulta SQL que se ejecuta, cuál de los campos introducidos al formulario utiliza y cuál no.

![SQLI1]()

| Tabla 1 |   |
|-------------------------|---|
| Escribo valores ... |  " |
| En el campo ...         |  users |
| Del formulario de la página ... | insert_player.php  |
| La consulta SQL que se ejecuta es ... | Invalid query: SELECT userId, password FROM users WHERE username = """. Field user introduced is: "  |
| Campos del formulario web utilizados en la consulta SQL ... | users |
| Campos del formulario web no utilizados en la consulta SQL ... | password  |

b) Gracias a la SQL Injection del apartado anterior, sabemos que este formulario es vulnerable y conocemos el nombre de los campos de la tabla “users”. Para tratar de impersonar a un usuario, nos hemos descargado un diccionario que contiene algunas de las contraseñas más utilizadas (se listan a continuación):

- password
- 123456
- 12345678
- 1234
- qwerty
- 12345678
- dragon

Dad un ataque que, utilizando este diccionario, nos permita impersonar un usuario de esta aplicación y acceder en nombre suyo. 

Tened en cuenta que no sabéis ni cuántos usuarios hay registrados en la aplicación, ni los nombres de estos.

![SQLI2]()

- Explicación del ataque: El ataque consiste en crear un payload en el “Intruder Attack” que haga objetivo a cada registro del campo “username” y devuelva como resultado el nombre de usuario que haya coincidido con alguna de las contraseñas que hemos metido en dicho payload.
- Campo de usuario con que el ataque ha tenido éxito: luis
- Campo de contraseña con que el ataque ha tenido éxito: 1234

c) Si vais a **private/auth.php**, veréis que en la función areUserAndPasswordValid”, se utiliza “SQLite3::escapeString()”, pero, aun así, el formulario es vulnerable a SQL Injections, explicad cuál es el error de programación de esta función y como lo podéis corregir.

| Tabla 2                                      |                                                                                                                                                                              |
| -------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Explicación del error ...                    | El problema está en que se está utilizando “SQLite3::escapeString()” para escapar toda la sentencia SQL, en vez de hacerlo solamente con los valores de entrada del usuario. |
| Solución: Cambiar la línea con el código ... | ``` $query = SQLite3::escapeString('SELECT userId, password FROM users WHERE username = "' . $user . '"'); ```                                                               |
| ... por la siguiente línea ...               | ``` $user_escaped = $db->escapeString($user);<br>$query = 'SELECT userId, password FROM users WHERE username = "' . $user_escaped . '"'; ```<br>                             |

d) Si habéis tenido éxito con el **_apartado b),_** os habéis autenticado utilizando elusuario “luis” (si no habéis tenido éxito, podéis utilizar la contraseña “1234” para realizar este apartado). Con el objetivo de mejorar la imagen de la jugadora “Candela Pacheco”, le queremos escribir un buen puñado de comentarios positivos, pero no los queremos hacer todos con la misma cuenta de usuario.

Para hacer esto, en primer lugar habéis hecho un ataque de fuerza bruta sobre eldirectorio del servidor web (por ejemplo, probando nombres de archivo) y habéis encontrado el archivo “add_comment.php~”. Estos archivos seguramente se han creado como copia de seguridad al modificar el archivo “.php” original directamente al servidor. En general, los servidores web no interpretan (ejecuten) los archivos “.php~” sino que los muestran como archivos de texto sin interpretar.

Esto os permite estudiar el código fuente de “add_comment.php” y encontrar una vulnerabilidad para publicar mensajes en nombre de otros usuarios. ¿Cuál es esta vulnerabilidad, y cómo es el ataque que utilizáis para explotarla?





