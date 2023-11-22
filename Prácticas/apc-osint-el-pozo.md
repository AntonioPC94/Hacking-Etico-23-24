# OSINT Pasivo: El Pozo

<p align="center">
  <img src="https://github.com/AntonioPC94/Hacking-Etico-23-24/blob/bf04887aea7feae1f0621fe7a3d4b347c575248d/Pr%C3%A1cticas/img/img20.png" alt="img20"/>
</p>

Trabajo realizado por: Antonio Peñalver Caro

#

# Índice

1. [Introducción](#introducción)
2. [WHOIS](#whois)
3. [Servidores DNS](#servidores-dns)
4. [Servidores de Correo](#servidores-de-correo)
5. [Subdominios](#subdominios)
6. [Información Adicional](información-adicional)

# Introducción

En esta actividad, realizaremos OSINT pasivo a la empresa de El Pozo. Para ello, usaremos algunas técnicas y herramientas de OSINT vistas en clase. En general, usaremos las siguientes herramientas y páginas web:

- theHarvester
- www.who.is
- www.stat.ripe.net: Para averiguar cuál es el AS de la empresa.
- www.dnsdumpster.com
- www.rocketreach.co: Para averiguar información sobre los trabajadores de la empresa.
- www.linkedin.com

# WHOIS

## Sistema Autónomo (AS)

Para poder saber cuál es el sistema autónomo asociado a la dirección IP del dominio de la empresa, primeramente tendremos que saber cuál es dicha dirección. Para ello, nos iremos a la página "www.who.is" y buscaremos en el registro "A" del DNS de la empresa.

<p align="center">
  <img src="https://github.com/AntonioPC94/Hacking-Etico-23-24/blob/14c89571d59e72141be0db816971857ff470f57d/Pr%C3%A1cticas/img/img21.png" alt="img21"/>
</p>

Una vez encontrada la dirección, nos iremos a una página de búsquedas de AS, concretamente a "www.stat.ripe.net". Una vez que hayamos abierto la página, colocaremos la dirección IP de la empresa en la barra de búsquedas y le daremos a "Buscar".

Según esta página, el AS de la empresa es: MAINT-AS3352, el cual corresponde con Telefónica.

<p align="center">
  <img src="https://github.com/AntonioPC94/Hacking-Etico-23-24/blob/14c89571d59e72141be0db816971857ff470f57d/Pr%C3%A1cticas/img/img22.png" alt="img22"/>
</p>

<p align="center">
  <img src="https://github.com/AntonioPC94/Hacking-Etico-23-24/blob/14c89571d59e72141be0db816971857ff470f57d/Pr%C3%A1cticas/img/img23.png" alt="img23"/>
</p>

## Proveedor de Servicios de Internet (ISP)

Siendo Telefónica el AS de la empresa, es muy probable que esta también sea su ISP.

## Direcciones IP

Aparte de la dirección IP hayada anteriormente con el WHOIS, con la herramienta theHarvester encontraremos las siguientes direcciones IP:

<p align="center">
  <img src="https://github.com/AntonioPC94/Hacking-Etico-23-24/blob/14c89571d59e72141be0db816971857ff470f57d/Pr%C3%A1cticas/img/img24.png" alt="img24"/>
</p>

<p align="center">
  <img src="https://github.com/AntonioPC94/Hacking-Etico-23-24/blob/14c89571d59e72141be0db816971857ff470f57d/Pr%C3%A1cticas/img/img25.png" alt="img25"/>
</p>

## Datos de contacto

Los datos de contacto de la empresa, los sacaremos realizando una búsqueda por Internet:

<p align="center">
  <img src="https://github.com/AntonioPC94/Hacking-Etico-23-24/blob/14c89571d59e72141be0db816971857ff470f57d/Pr%C3%A1cticas/img/img26.png" alt="img26"/>
</p>

<p align="center">
  <img src="https://github.com/AntonioPC94/Hacking-Etico-23-24/blob/14c89571d59e72141be0db816971857ff470f57d/Pr%C3%A1cticas/img/img27.png" alt="img27"/>
</p>

## Correos electrónicos

Con la herramienta theHarvester, podremos encontrar las siguientes direcciones de correo:

<p align="center">
  <img src="https://github.com/AntonioPC94/Hacking-Etico-23-24/blob/14c89571d59e72141be0db816971857ff470f57d/Pr%C3%A1cticas/img/img28.png" alt="img28"/>
</p>

Dos de dichos correos parecen ser de alguien que trabaja en la empresa, seguramente nos sirvan luego para seguir recopilando información.

# Servidores DNS

En la página "www.dnsdumpster.com", podremos encontrar los servidores DNS de la empresa:

<p align="center">
  <img src="https://github.com/AntonioPC94/Hacking-Etico-23-24/blob/13d92528c544e86ad31adce43931a7fd1978d25f/Pr%C3%A1cticas/img/img29.png" alt="img29"/>
</p>

# Servidores de Correo

La empresa cuenta con un servidor de correos ubicado en Netherlands, el cual podremos visualizar tanto en el registro MX que mostramos anteriormente, como en los resultados obtenidos en la página "www.dnsdumpster.com".

<p align="center">
  <img src="https://github.com/AntonioPC94/Hacking-Etico-23-24/blob/14c89571d59e72141be0db816971857ff470f57d/Pr%C3%A1cticas/img/img30.png" alt="img30"/>
</p>

<p align="center">
  <img src="https://github.com/AntonioPC94/Hacking-Etico-23-24/blob/14c89571d59e72141be0db816971857ff470f57d/Pr%C3%A1cticas/img/img31.png" alt="img31"/>
</p>

# Subdominios

En los resultados obtenidos anteriormente con theHarvester, podremos visualizar los subdominios pertenecientes a la empresa:

<p align="center">
  <img src="https://github.com/AntonioPC94/Hacking-Etico-23-24/blob/14c89571d59e72141be0db816971857ff470f57d/Pr%C3%A1cticas/img/img32.png" alt="img32"/>
</p>

# Información Adicional

## ASN Subdominio

Mirando los resultados proporcionados por la página "www.dnsdumpster.com", vimos que había un ASN asociado a dos de los subdominios de la empresa. Dicho ASN, era el proveedor de servidores virtuales privados: Digital Ocean. Casualmente, la localización de dicho ASN, coincide con la del servidor de correos de la empresa.

<p align="center">
  <img src="" alt="img33"/>
</p>

## Correo electrónico empleado/a

Como comentamos anteriormente, nos encontramos con un par de correos electrónicos que parecían ser de uno de los empleados de la empresa. Entonces, para poder recabar información sobre dicha persona, colocamos el nombre y el apellido junto con el nombre de la empresa en Google.

En el primer resultado de búsqueda, localizamos una página llamada "www.rocketreach.co", la cual indicaba que el 85% de los empleados de la empresa ElPozo, usaban el siguiente formato de correo electrónico para elaborar el suyo propio de empresa:

nombre.primerapellido@elpozo.com

<p align="center">
  <img src="" alt="img34"/>
</p>

Accedimos a dicha página y a la derecha de la misma, vimos los perfiles de los distintos empleados que tenian un correo de empresa creado con dicho formato. 
A raíz de ese descubrimiento, pudimos observar que la información mostrada en dicha página, era extraída de sitios web como LinkedIn. Ya que dichos trabajadores, tienen esa información pública en dicha web.

Para poder acceder a toda la información, nos registramos en la página web "www.rocketreach.co" y "www.linkedin.com" con el Sock Puppet que creamos en prácticas anteriores.

### Juan Cánovas Fuertes

  <p align="center">
    <img src="" alt="img35"/>
  </p>

  - Estudios: Seminario anual especializado en la cadena agroalimentaria. Licenciatura en dirección y administración de empresas, Dirección general y RRHH. Máster de             administración de negocios y dirección comercial y marketing.
  - Puesto: Director Comercial Frescos.
  - Skills: Estrategia empresarial. Plan de negocio. Negociación.
  - Correo Empresa: juan.fuertes@elpozo.com
  - Correo Personal: juancanovas82@gmail.com
  - LinkedIn: https://www.linkedin.com/in/juan-c%C3%A1novas-fuertes-14702027/

### Julián González García

  - Puesto: Director de Marketing
  - Skills: Publicidad en Internet. Marketing en Internet. Estrategia. Estrategia empresarial. Estudios de mercado.
  - Correo Empresa: julian.gonzalez@elpozo.com
  - LinkedIn: https://www.linkedin.com/in/juli%C3%A1n-gonz%C3%A1lez-garc%C3%ADa-4ba78476/

### Mariano García Pérez

  - Puesto: Director Comercial
  - Skills: PowerPoint. Management. Photoshop. English. Business Strategy. Business Development. Etc.
  - Correo Empresa: mariano.perez@elpozo.com
  - Correo Empresa 2: mariano@elpozo.com
  - LinkedIn: https://www.linkedin.com/in/mariano-garcia-perez-01803626/

### Eric Duhamel

 <p align="center">
    <img src="" alt="img36"/>
  </p>
  
  - Puesto: Sales Manager Europe and Americas
  - Skills: Sales Management. International Sales. Negotiation. Marketing Strategy. New Business Development. Etc. 
  - Correo Empresa: ericxavier.duhamel@elpozo.com
  - Correo Personal: yourlimu@yahoo.com
  - Otros correos: itelnet2000@yahoo.com // mysynaura@yahoo.com // juanpablo.olalla@elpozo.com
  - LinkedIn: https://www.linkedin.com/in/eric-duhamel-b847351/
  - Facebook: https://www.facebook.com/eric.duhamel.96/?show_switched_toast=0&show_invite_to_follow=0&show_switched_tooltip=0&show_podcast_settings=0&                            show_community_review_changes=0&show_community_rollback=0&show_follower_visibility_disclosure=0

## Mapa DNS

Por último, mostraremos un mapa DNS de la empresa, el cual lo sacaremos de la páguina "www.dnsdumpster.com":

<p align="center">
  <img src="" alt="img34"/>
</p>

