# Bitaxe-conf

## Tutorial para configurar el Bitaxe

### Requisitos

- Python

### Instalación

Instala `bitaxetool` desde pip. Si necesitas instalar pip, consulta [este enlace](https://pip.pypa.io/en/stable/installation/).

```python
pip install --upgrade bitaxetool
```

### Edición del archivo config.cvs

Edita los siguientes campos en el archivo `config.cvs`:

- Datos de SSID y contraseña del WiFi.
- Datos de la piscina donde vas a minar (por defecto es `public-pool.io`).
- Dirección de Bitcoin.

Ejemplo:

```csv
wifissid,data,string,MIWIFI
wifipass,data,string,MIPASS
stratumurl,data,string,public-pool.io
stratumport,data,u16,21496
stratumuser,data,string,bc1q262qeyyhdakrje5qaux8m2a3r4z8sw8vu5mysh.Bitaxe
```

Edicion del archivo config.cvs
-Edita:
-datos de ssid, password del wifi
-Datos de piscina donde vas a minar(por defecto es public-pool.io)
-Address de bitcoin.Nombre
-Ejemplo:
wifissid,data,string,MIWIFI
wifipass,data,string,MIPASS
stratumurl,data,string,public-pool.io
stratumport,data,u16,21496
stratumuser,data,string,bc1q262qeyyhdakrje5qaux8m2a3r4z8sw8vu5mysh.Bitaxe

### Una vez editados esos parametros, para flashear:

-Situate en la carpeta del repositorio desde consola
-Conecta el bitaxe al ordenador por USB
-Lanza el siguiente comando:

```
bitaxetool --config ./config.cvs --firmware .\esp-miner-factory-204-v2.0.7.bin
```
