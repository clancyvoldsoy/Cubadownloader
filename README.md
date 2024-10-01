# Cubadownloader
Guía para descargar archivos de internet sin necesidad de usar una VPN constantemente. Obviamente esto solamente es útil para archivos de tamaño promedio Se recomienda tener los conocimientos básicos para interactuar con una shell de Linux. Utilizaremos Google Colab y `collabxterm` para acceder a nuestra carpeta de Google Drive y descargar los archivos directamente allí.

## Pasos a Seguir

### 1. Acceder al Link de Descarga con VPN

1. **Conéctate a una VPN**: Utiliza tu VPN preferida para acceder desde el navegador al link de descarga del archivo que necesitas.
2. **Obtén el Link de Descarga**: Copia el link de descarga del archivo.
![image](https://github.com/user-attachments/assets/7c18fd29-72d6-41ac-bba5-d74de5503079)

### 2.Shell en Google Colab

1. **Abrimos Google Colab**: Ve a Google Colab en https://colab.research.google.com .
2. **Crear un Nuevo Notebook**: Haz clic en `File > New Notebook`.
3. **Instalar `collabxterm`**: Ejecuta el siguiente comando en una celda de código para instalar `collabxterm`:
    ```python
    !pip install colab-xterm
    ```
4. **Iniciar `collabxterm`**: Ejecuta el siguiente comando para iniciar una terminal:
    ```python
    %load_ext colabxterm
    %xterm
    ```
![image](https://github.com/user-attachments/assets/49df5aec-4728-47e2-8017-3cdaa67f1b81)


### 3. Acceder a tu Carpeta de Google Drive

1. **Montar Google Drive**: Toca donde dice +Code, te saldrá un recuadro nuevo para agregar código, ahí ejecuta el siguiente comando en la terminal para montar tu Google Drive:
    ```bash
    from google.colab import drive
    drive.mount('/content/drive')
    ```
    ![image](https://github.com/user-attachments/assets/61a61865-47f8-49fc-af25-6c6865fab93b)

2. **Navegar a tu Carpeta de Google Drive**: Cambia el directorio a la carpeta de Google Drive donde deseas guardar el archivo:
    ```bash
    cd /content/drive/MyDrive
    ```
![image](https://github.com/user-attachments/assets/cb8e699f-d06d-43f2-8df7-2be0e7782713)

### 4. Descargar el Archivo con `wget`

1. **Descargar el Archivo**: Utiliza `wget` para descargar el archivo directamente a tu carpeta de Google Drive:
    ```bash
    wget  "URL_DEL_ARCHIVO"
    ```
![image](https://github.com/user-attachments/assets/990ba13e-52c2-4156-9c3a-cb78cb935c0c)

### 5. Descargar el Archivo desde Google Drive
![image](https://github.com/user-attachments/assets/60e33340-535a-4d38-8cec-b712d446802d)

1. **Acceder a Google Drive**: Ve a Google Drive en tu navegador.
2. **Descargar el Archivo**: Navega a la carpeta donde guardaste el archivo y descárgalo a tu dispositivo.

## Notas
  
- **OJO**: Asegúrate de desconectarte de la VPN una vez que hayas obtenido el link de descarga para evitar un uso innecesario de la VPN.
- **Aclaración**: Quiero aclarar por si tienen la duda, nada de lo que descargues a traves de Google Colab va a consumir datos, ya que esto es un host remoto, solo consumirá datos la descarga que hagas en el navegador desde Google Drive hasta tu dispositivo.
- **Espacio en Google Drive**: Verifica que tienes suficiente espacio en tu Google Drive para almacenar el archivo. De lo contrario, crea una nueva cuenta de Google para estos fines
- **Plus**: Puedes descargar torrents también con este método, instalas el aria2, te vas a torrentgalaxy (por ejemplo) y descargas usando los magnets.
- ![image](https://github.com/user-attachments/assets/d5fd03ac-25ab-4a89-9e78-b258dba47bde)

  **Besitos en el chikistrikis**

