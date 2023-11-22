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

# WHOIS

## Sistema Autónomo (AS)

Para poder saber cuál es el sistema autónomo asociado a la dirección IP del dominio de la empresa, primeramente tendremos que saber cuál es dicha dirección. Para ello, nos iremos a la página "www.who.is" y buscaremos en el registro "A" del DNS de la empresa.

<p align="center">
  <img src="" alt="img21"/>
</p>

Una vez encontrada la dirección, nos iremos a una página de búsquedas de AS, concretamente a "www.stat.ripe.net". Una vez que hayamos abierto la página, colocaremos la dirección IP de la empresa en la barra de búsquedas y le daremos a "Buscar".

Según esta página, el AS de la empresa es: MAINT-AS3352, el cual corresponde con Telefónica.

<p align="center">
  <img src="" alt="img22"/>
</p>

<p align="center">
  <img src="" alt="img23"/>
</p>

## Proveedor de Servicios de Internet (ISP)

Siendo Telefónica el AS de la empresa, es muy probable que esta también sea su ISP.

## Direcciones IP

Aparte de la dirección IP hayada anteriormente con el WHOIS, con la herramienta theHarvester encontraremos las siguientes direcciones IP:

<p align="center">
  <img src="" alt="img24"/>
</p>

<p align="center">
  <img src="" alt="img25"/>
</p>

## Datos de contacto

Los datos de contacto de la empresa, los sacaremos realizando una búsqueda por Internet:

<p align="center">
  <img src="" alt="img26"/>
</p>

<p align="center">
  <img src="" alt="img27"/>
</p>

## Correos electrónicos

Con la herramienta theHarvester, podremos encontrar las siguientes direcciones de correo:

<p align="center">
  <img src="" alt="img28"/>
</p>

Dos de dichos correos parecen ser de alguien que trabaja en la empresa, seguramente nos sirvan luego para seguir recopilando información.

# Servidores DNS

En la página "www.dnsdumpster.com", podremos encontrar los servidores DNS de la empresa:

<p align="center">
  <img src="" alt="img29"/>
</p>

# Servidores de Correo

La empresa cuenta con un servidor de correos ubicado en Netherlands, el cual podremos visualizar tanto en el registro MX que mostramos anteriormente, como en los resultados obtenidos en la página "www.dnsdumpster.com".

<p align="center">
  <img src="" alt="img30"/>
</p>

<p align="center">
  <img src="" alt="img31"/>
</p>

# Subdominios

En los resultados obtenidos anteriormente con theHarvester, podremos visualizar los subdominios pertenecientes a la empresa:

<p align="center">
  <img src="" alt="img32"/>
</p>

# Información Adicional

## ASN Subdominio

Mirando los resultados proporcionados por la página "www.dnsdumpster.com", vimos que había un ASN asociado a uno de los subdominios de la empresa.

## Mapa DNS

Por último, mostraremos un mapa DNS de la empresa, el cual lo sacaremos de la páguina "www.dnsdumpster.com":

<p align="center">
  <img src="" alt="img34"/>
</p>

