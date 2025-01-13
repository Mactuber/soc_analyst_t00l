# soc_analyst_t00l

**Herramienta para los servicios en SOC prestados por analistas de Nivel 1.**

Este conjunto de scripts ha sido diseñado para agilizar la gestión y análisis de un alto volumen de IPs, dominios, URLs o hashes en un entorno SOC. Utiliza las APIs de **VirusTotal**, **AbuseIP** e **IPVoid** para distinguir si estos elementos son maliciosos o no. Los resultados se reportan de forma ordenada, permitiendo a los analistas procesar rápidamente los datos y tomar decisiones informadas.

## Objetivo de los Scripts

Cada uno de los scripts incluidos en esta herramienta tiene como objetivo realizar una evaluación de las entidades (IPs, dominios, URLs o hashes) en función de los siguientes criterios:

- **Maliciosos**: Identifica si la entidad está asociada a actividades sospechosas o amenazas conocidas.
- **No maliciosos**: Determina si la entidad no presenta riesgos conocidos en las plataformas de análisis.

La salida de cada script estará organizada para facilitar la interpretación de los resultados.

## Requisitos

Para poder utilizar esta herramienta, necesitarás lo siguiente:

1. **Cuenta en las plataformas de las APIs**:
   - **VirusTotal**: Regístrate en [VirusTotal](https://www.virustotal.com) para obtener una clave API.
   - **AbuseIP**: Regístrate en [AbuseIP](https://www.abuseipdb.com) para obtener una clave API.
   - **IPVoid**: Regístrate en [IPVoid](https://www.ipvoid.com) para obtener una clave API.

2. **Configurar las claves API en los scripts**:
   - Una vez que hayas obtenido las claves API, deberás integrarlas en los scripts correspondientes para que funcionen correctamente.

## Instrucciones de Uso

### 1. Preparar los scripts

Los scripts están diseñados para ser ejecutados desde PowerShell. Para utilizarlos, sigue estos pasos:

1. Descarga los scripts desde este repositorio.
2. Modifica las claves API dentro de los scripts:
   - En cada script, busca las líneas donde se definen las claves API para VirusTotal, AbuseIP y IPVoid.
   - Sustituye las claves de ejemplo con tus claves API obtenidas al registrarte en las plataformas mencionadas.

### 2. Ejecutar los scripts

Los scripts están inicialmente en formato `.txt`. Para ejecutarlos, sigue estos pasos:

1. Cambia la extensión del archivo de `.txt` a `.ps1`.
   - Por ejemplo, si el archivo se llama `domains_ipvoid_vt.txt`, renómbralo a `domains_ipvoid_vt.ps1`.

2. Ejecuta el script desde un terminal de PowerShell:

   ```powershell
   .\domains_ipvoid_vt.ps1

### 3. Interpretar la salida

La salida de los scripts estará organizada y te proporcionará la siguiente información:

   - IP/Dominio/URL/Hash: La entidad que se está analizando.
   - Resultado de VirusTotal: Un análisis de la entidad con la API de VirusTotal.
   - Resultado de AbuseIP: Un análisis de la entidad con la API de AbuseIP.
   - Resultado de IPVoid: Un análisis de la entidad con la API de IPVoid.
   - Clasificación: Indicación de si la entidad es maliciosa o no, según los resultados de las APIs

### 4. Ejemplo de ejecución

![script 1 IPs](/Images/script_ips1.png)
![script 2 IPs](/Images/script_ips2.png)
![script dominios](/Images/scripts_domains.png)
![script de hashes](/Images/scripts_hashes.png)
![script de URLs](/Images/scripts_urls.png)
