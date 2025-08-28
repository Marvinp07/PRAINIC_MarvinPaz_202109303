# 🖥️ Uso de la Terminal - Consola

## 📂 Para navegar entre archivos y directorios

**Entra a una ruta en un directorio actual:**
```bash
cd ruta 
```

**Regresa un directorio:**
```bash
cd ..
```

---

## 👀 Para ver el contenido de un directorio

```bash
ls 
```

**Lista detallada:**
```bash
ls -la
```

---

## 📁 Para crear carpetas en un directorio

```bash
mkdir "Nombre de la carpeta" 
```

---

## 📋 Para copiar archivos y carpetas de un directorio a otro

**Para copiar 1 archivo:**
```bash
cp ruta/origen/archivo1 ruta/destino/
```

**Para copiar varios archivos:**
```bash
cp /ruta/origen/* /ruta/destino/
```

**Para copiar varios archivos con subrutas:**
```bash
cp -r /ruta/origen/ /ruta/destino/
```

---

## ✂️ Para mover archivos y carpetas de un directorio a otro

**Para mover un archivo:**
```bash
mv /ruta/origen/archivo.txt /ruta/destino/
```

**Para mover varios archivos con subrutas:**
```bash
mv /ruta/origen/carpeta/ /ruta/destino/
```

---

## 🗑️ Para eliminar archivos y carpetas de un directorio

**Para eliminar un archivo:**
```bash
rm /ruta/del/archivo.txt
```

**Para eliminar múltiples archivos de cierto tipo:**
```bash
rm /ruta/*.log
```

**Para eliminar una carpeta con todo su contenido:**
```bash
rm -r /ruta/del/directorio/
```

---

## 👨‍💻 Para ingresar como Superusuario a la terminal

```bash
sudo -i
```

```bash
sudo su
```

---

## 🔐 Para actualizar los permisos a los archivos o directorios

**Para cambiar permisos a un archivo:**
```bash
chmod 755 archivo.txt
```

**Para cambiar permisos a un directorio:**
```bash
chmod -R 755 /ruta/carpeta/
```

---

## 📝 Para crear/editar un archivo de texto desde la terminal

```bash
nano archivo.txt
```

---

## 📦 Para instalar paquetes desde la terminal

```bash
sudo apt install "nombre del paquete"
```

---

## 🔄 Para actualizar paquetes desde la terminal

**Actualiza paquetes disponibles:**
```bash
sudo apt update
```

**Actualiza paquetes instalados:**
```bash
sudo apt upgrade
```

---

## 🗑️ Para eliminar paquetes desde la terminal

```bash
sudo apt remove nombre-paquete
```

```bash
sudo apt purge nombre-paquete
```


----    
# Guía de Instalación y Configuración de Apache2

## 1. Instalar el Servidor Web Apache2

Actualizar el sistema e instalar Apache2.


```bash
sudo apt update
sudo apt install apache2
```

## 2. Verificar que el Servicio Esté Activo

Comprobar el estado del servicio Apache2.

```bash
sudo systemctl status apache2
```

**Verificación adicional:**
- Abrir el navegador y navegar a `http://localhost`
- Comprobar que Apache muestra la página por defecto

## 3. Cambiar el Puerto por Defecto

Modificar la configuración para que Apache se ejecute en el puerto 8080 en lugar del puerto 80.

**Archivos a revisar y modificar:**

### `/etc/apache2/ports.conf`
- Cambiar `Listen 80` por `Listen 8080`

### `/etc/apache2/sites-available/000-default.conf`
- Cambiar `<VirtualHost *:80>` por `<VirtualHost *:8080>`

## 4. Modificar la Página de Apache

Personalizar la página principal de Apache.

**Pasos:**
1. Acceder al directorio `/var/www/html/`
2. Modificar el archivo `index.html` con su nombre y número de carnet

```bash
cd /var/www/html/
sudo nano index.html
```

## 5. Mostrar la Página con los Cambios

Aplicar y verificar todos los cambios realizados.

**Reiniciar el servidor:**
```bash
sudo systemctl restart apache2
```

**Verificar los cambios:**
- Abrir el navegador y navegar a `http://localhost:8080`
- Confirmar que se muestra la página modificada con su información personal

---

**Nota:** Se deve tener permisos de administrador (sudo) para ejecutar todos los comandos mencionados.

---
✍️ Autores: Carlos Mauricio Blanco Valencia

✍️ Autores: Marvin Francisco Paz Linares

📅 Fecha: 28/08/2025