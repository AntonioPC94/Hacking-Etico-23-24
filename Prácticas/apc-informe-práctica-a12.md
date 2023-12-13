# Identificación de Sistemas con NMAP

<p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/e823629d1ce58acb731dd645b37e3b5a8512f738/Pr%C3%A1cticas/img/img31.png"/>
</p>

Trabajo realizado por: Antonio Peñalver Caro

#

1. **Identifica la IP del equipo objetivo.**

<p align="left">
<img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/e823629d1ce58acb731dd645b37e3b5a8512f738/Pr%C3%A1cticas/img/img32.png" width="30%" /> 
</p>

<div style="display: flex; justify-content: space-between;">
    <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/e823629d1ce58acb731dd645b37e3b5a8512f738/Pr%C3%A1cticas/img/img33.png" width="40%"/>
</div>

#

2. **Identifica el sistema operativo del equipo objetivo.**

<p align="left">
<img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/e823629d1ce58acb731dd645b37e3b5a8512f738/Pr%C3%A1cticas/img/img34.png" width="30%" /> 
</p>

<div style="display: flex; justify-content: space-between;">
    <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/e823629d1ce58acb731dd645b37e3b5a8512f738/Pr%C3%A1cticas/img/img35.png" width="40%"/>
</div>

#

3. **Identifica puertos/servicios abiertos (TCP/UDP).**

**TCP**

<p align="left">
<img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/e823629d1ce58acb731dd645b37e3b5a8512f738/Pr%C3%A1cticas/img/img36.png" width="30%" /> 
</p>

<div style="display: flex; justify-content: space-between;">
    <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/e823629d1ce58acb731dd645b37e3b5a8512f738/Pr%C3%A1cticas/img/img37.png" width="40%"/>
</div>

**UDP**

<p align="left">
<img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/745d0fed88846a610789d4812ef8704d175e5ef2/Pr%C3%A1cticas/img/img38.png" width="30%" /> 
</p>

<div style="display: flex; justify-content: space-between;">
    <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/e823629d1ce58acb731dd645b37e3b5a8512f738/Pr%C3%A1cticas/img/img39.png" width="40%"/>
</div>

- No existe respuesta por parte de ningún puerto UDP.

#

4. **Identifica las versiones de los servicios detectados.**

<p align="left">
<img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/745d0fed88846a610789d4812ef8704d175e5ef2/Pr%C3%A1cticas/img/img40.png" width="30%" /> 
</p>

<div style="display: flex; justify-content: space-between;">
    <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/745d0fed88846a610789d4812ef8704d175e5ef2/Pr%C3%A1cticas/img/img41.png" width="40%"/>
</div>

#

5. **Comprueba si existen usuarios con contraseñas vacías (NSE).

<div style="display: flex; justify-content: space-between;">
<p align="left">
<img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/745d0fed88846a610789d4812ef8704d175e5ef2/Pr%C3%A1cticas/img/img42.png" width="30%"/> 
</p>
</div>

- No existen usuarios con contraseñas vacías.

#

6. **Comprueba las vulnerabilidades existentes en el equipo (NSE).

<p align="left">
<img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/745d0fed88846a610789d4812ef8704d175e5ef2/Pr%C3%A1cticas/img/img46.png" width="30%" /> 
</p>

<div style="display: flex; justify-content: space-between;">
    <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/745d0fed88846a610789d4812ef8704d175e5ef2/Pr%C3%A1cticas/img/img47.png" width="40%"/>
</div>

#

7. **Comprueba si dispone de servicios web habilitados (NSE).

<p align="left">
<img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/745d0fed88846a610789d4812ef8704d175e5ef2/Pr%C3%A1cticas/img/img48.png" width="35%"/>
</p>

<div style="display: flex; justify-content: space-between;">
    <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/745d0fed88846a610789d4812ef8704d175e5ef2/Pr%C3%A1cticas/img/img49.png" width="30%" />
    <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/745d0fed88846a610789d4812ef8704d175e5ef2/Pr%C3%A1cticas/img/img50.png" width="40%"/>
</div>
  
8. **Ejecuta scripts por defecto de nmap para ampliar la información (NSE).

<p align="left">
<img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/745d0fed88846a610789d4812ef8704d175e5ef2/Pr%C3%A1cticas/img/img51.png" width="35%"/> 
</p>

<div style="display: flex; justify-content: space-between;">
    <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/745d0fed88846a610789d4812ef8704d175e5ef2/Pr%C3%A1cticas/img/img52.png" width="35%" />
    <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/745d0fed88846a610789d4812ef8704d175e5ef2/Pr%C3%A1cticas/img/img54.png" width="30%"/>
    <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/745d0fed88846a610789d4812ef8704d175e5ef2/Pr%C3%A1cticas/img/img55.png" width="30%"/>
</div>

#

9. **Cualquier otra información que consideres relevante de incorporar en el informe.

- La siguiente información fue sacada a raíz del lanzamiento de los script "auth" de NMap.

<div style="display: flex; justify-content: space-between;">
    <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/745d0fed88846a610789d4812ef8704d175e5ef2/Pr%C3%A1cticas/img/img43.png" width="30%" />
    <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/745d0fed88846a610789d4812ef8704d175e5ef2/Pr%C3%A1cticas/img/img44.png" width="35%"/>
    <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/745d0fed88846a610789d4812ef8704d175e5ef2/Pr%C3%A1cticas/img/img45.png" width="30%"/>
</div>

#

10. **Realizar un informe técnico describiendo toda la información recopilada durante la realización del escáner manual.
