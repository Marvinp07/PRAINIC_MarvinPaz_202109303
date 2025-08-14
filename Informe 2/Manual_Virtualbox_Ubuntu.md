
# 📘 Manual de Instalación y Configuración de Ubuntu en VirtualBox

Este documento describe el procedimiento completo para instalar **Ubuntu** en una máquina virtual usando **VirtualBox** en Windows, sin eliminar el sistema operativo Windows, y detalla las configuraciones posteriores y soluciones a problemas encontrados.

---

## 1. 💻 Sobre Ubuntu

Ubuntu es una distribución de **GNU/Linux** basada en Debian, desarrollada por Canonical Ltd., diseñada para ser fácil de usar, estable y accesible para usuarios de todos los niveles.

Características principales:
- **Entorno de escritorio GNOME** (por defecto), con variantes como Kubuntu (KDE), Xubuntu (XFCE), Ubuntu MATE, entre otras.
- Lanzamientos cada 6 meses con soporte estándar, y versiones LTS (Long Term Support) cada 2 años con 5 años de soporte.
- Amplia compatibilidad con hardware y software.
- Sistema optimizado tanto para equipos modernos como para hardware más antiguo.
- Snap Store integrado para instalación fácil de aplicaciones.

**Beneficios:**
- Interfaz moderna e intuitiva para usuarios nuevos en Linux.
- Excelente soporte de hardware y controladores.
- Seguridad robusta y actualizaciones regulares.
- Comunidad muy activa y documentación extensa.
- Ecosistema empresarial sólido con soporte comercial disponible.

---

## 2. 🌐 Cómo conseguir Ubuntu

La distribución puede descargarse desde el sitio oficial:
🔗 [https://releases.ubuntu.com/jammy/](https://releases.ubuntu.com/jammy/)

**Pasos para descargar:**
1. Ingresar a la página oficial de Ubuntu.
2. Elegir la versión deseada (recomendado Ubuntu LTS para mayor estabilidad).
3. Hacer clic en **"Download"** para iniciar la descarga.
4. Descargar el archivo `.iso` (aproximadamente 4-5 GB).
5. (Opcional) Verificar la integridad de la descarga usando el hash SHA256 provisto en la web.

**Versiones recomendadas:**
- **Ubuntu 22.04 LTS** (Jammy Jellyfish) - Soporte hasta 2027
- **Ubuntu 24.04 LTS** (Noble Numbat) - Soporte hasta 2029

---

## 3. 🖥️ Instalando Ubuntu en VirtualBox

> **Objetivo:** Mantener Windows como sistema principal y ejecutar Ubuntu de forma virtualizada.

**Pasos:**
1. Descargar e instalar **VirtualBox** desde [https://www.oracle.com/es/virtualization/technologies/vm/downloads/virtualbox-downloads.html](https://www.oracle.com/es/virtualization/technologies/vm/downloads/virtualbox-downloads.html).
2. Abrir VirtualBox y hacer clic en **"Nueva"**.
3. Asignar un nombre a la máquina virtual, elegir **Tipo: Linux** y **Versión: Ubuntu (64-bit)**.
4. Asignar memoria RAM (recomendado: 4096 MB mínimo, 8192 MB para mejor rendimiento).
5. Crear un disco duro virtual (VDI) con al menos 25 GB (recomendado 40-50 GB).
6. Seleccionar el archivo `.iso` de Ubuntu en **Configuración > Almacenamiento > Controlador IDE**.
7. En **Configuración > Sistema > Procesador**, asignar al menos 2 núcleos de CPU.
8. Habilitar **Aceleración 3D** en **Configuración > Pantalla**.
9. Iniciar la máquina virtual.
10. En el instalador de Ubuntu:
    - Seleccionar idioma español.
    - Elegir **"Instalación normal"** o **"Instalación mínima"** según preferencia.
    - Configurar distribución de teclado.
    - Seleccionar **"Borrar disco e instalar Ubuntu"** (solo afecta el disco virtual).
    - Configurar zona horaria.
    - Crear usuario y contraseña.
11. Finalizar instalación y reiniciar.

---

## 4. ⚙️ Configuración Posterior

Después de la instalación, realizar:

- **Actualización del sistema:** Ir a **Configuración del sistema** y usar el **Gestor de actualizaciones** para mantener el sistema al día.

- **Instalar Guest Additions** para mejor integración con Windows (pantalla completa, carpetas compartidas, portapapeles bidireccional).

- **Configurar red:** Asegurar que la VM esté en modo **Adaptador puente** o **NAT** para conexión a Internet.

- **Configurar idioma y zona horaria** en **Configuración > Región e idioma**.

- **Instalar software necesario** desde **Ubuntu Software** o **Snap Store**.

- **Configurar carpetas compartidas** entre Windows y Ubuntu en VirtualBox.

---

## 5. 🛠️ Ayuda y Solución de Problemas

**Problemas encontrados y soluciones:**

- **No detecta el archivo ISO:** Verificar que esté seleccionado en Configuración > Almacenamiento y que el archivo no esté corrupto.

- **Pantalla pequeña o resolución fija:** Instalar Guest Additions (`Dispositivos > Insertar imagen de CD de Guest Additions`) y reiniciar.

- **Sin Internet:** Cambiar el adaptador de red a **NAT** o **Adaptador puente** en la configuración de la VM.

- **Rendimiento lento:** Aumentar RAM asignada, habilitar más núcleos de CPU y activar aceleración 3D.

- **Teclado incorrecto:** Ajustar en Configuración > Región e idioma > Distribuciones de teclado.

- **Audio no funciona:** Verificar que el controlador de audio esté configurado correctamente en VirtualBox.

- **Problemas con USB:** Instalar VirtualBox Extension Pack para soporte completo de USB.

**Fuentes de documentación utilizadas:**
- [Documentación oficial de Ubuntu](https://help.ubuntu.com/)
- [Ubuntu Desktop Guide](https://ubuntu.com/desktop/features)
- [Manual de VirtualBox](https://www.virtualbox.org/manual/)
- [Ask Ubuntu Community](https://askubuntu.com/)
- Comunidad de foros de Ubuntu y Stack Overflow.

---

✍️ **Autor:** Marvin Francisco Paz Linares 
📅 **Fecha:** 13/08/2025
