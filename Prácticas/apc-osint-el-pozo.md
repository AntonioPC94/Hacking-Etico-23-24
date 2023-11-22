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

En esta actividad, realizaremos OSINT pasivo a la empresa El Pozo. Para ello, usaremos algunas técnicas y herramientas de OSINT vistas en clase. En general usaré las siguientes herramientas y páginas web:

- theHarvester
- www.who.is
- www.stat.ripe.net: Para averiguar cuál es el AS de la empresa.
- www.dnsdumpster.com

# WHOIS

## Sistema Autónomo (AS)

Para poder saber cuál es el sistema autónomo asociado a la dirección IP del dominio de ElPozo, primeramente tendremos que saber cuál es dicha dirección. Para ello, nos iremos al WHOIS y buscaremos en el registro "A" del DNS la dirección IP que estamos buscando.

<p align="center">
  <img src="" alt="img21"/>
</p>

Una vez encontrada la dirección, nos iremos a una página de búsqueda de AS, concretamente a "www.stat.ripe.net". Una vez que hayamos abierto la página, colocaremos la dirección IP de ElPozo en la barra de búsqueda y le daremos a "Buscar".

Según esta página, el AS de ElPozo es: MAINT-AS3352, el cual corresponde con Telefónica.

<p align="center">
  <img src="" alt="img22"/>
</p>

<p align="center">
  <img src="" alt="img23"/>
</p>

## Proveedor de Servicios de Internet (ISP)

Siendo Telefónica el AS de la empresa, es muy probable que esta también sea su ISP.

## Direcciones IP

Aparte de la dirección IP que mostré antes con el WHOIS, con la herramienta theHarvester he podido encontrar las siguientes:

<p align="center">
  <img src="" alt="img24"/>
</p>

## Datos de contacto:

Los datos de contacto de la empresa, los sacaremos realizando una búsqueda por Internet:


## Correos electrónicos:

# Servidores DNS

# Servidores de Correo

# Subdominios

# Información Adicional


