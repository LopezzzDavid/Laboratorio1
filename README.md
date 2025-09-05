# Práctica de Laboratorio  
**Creación de Memorias USB Booteables con Rufus y Ventoy**  
**Universidad Santo Tomás**  
**Fecha:** 23 de agosto de 2025  
**Integrantes:** **David Saniago lopez , David Felipe Diaz, Jonathan David Diaz** 

---

## Índice  
1. [Conceptos Fundamentales](#conceptos-fundamentales)  
   1. [Proceso de Booteo con Rufus](#proceso-de-booteo-con-rufus)  
   2. [Proceso de Booteo con Ventoy](#proceso-de-booteo-con-ventoy)  
   3. [Bootloader y GRUB](#bootloader-y-grub)  
   4. [Sistemas de Archivos Compatibles](#sistemas-de-archivos-compatibles)  
   5. [Estructura de Particiones](#estructura-de-particiones)  
2. [Descarga e Inserción de Imágenes](#descarga-e-inserción-de-imágenes)  
   1. [Descarga de Imágenes ISO](#descarga-de-imágenes-iso)  
   2. [Proceso en Rufus (Ubuntu)](#proceso-en-rufus-ubuntu)  
   3. [Proceso en Ventoy (Ubuntu y Windows)](#proceso-en-ventoy-ubuntu-y-windows)  
3. [Instalación de Ubuntu](#instalación-de-ubuntu)  
   1. [Generación de Particiones](#generación-de-particiones)  
   2. [Proceso de Instalación Paso a Paso](#proceso-de-instalación-paso-a-paso)  
4. [Conclusiones](#conclusiones)  

---

## 1. Conceptos Fundamentales  

### 1.1. Proceso de Booteo con Rufus  
1. Descargar **Rufus**.  
2. Abrir Rufus y seleccionar:  
   - Dispositivo USB  
   - Imagen ISO (Ubuntu en este caso)  
   - Esquema de partición (MBR o GPT)  
   - Sistema de destino (BIOS o UEFI)  
3. Rufus formatea la memoria y graba la ISO.  
4. Al reiniciar, el PC detecta la memoria y carga el sistema.  

> **Nota:** Rufus solo admite una ISO por memoria.  

---

### 1.2. Proceso de Booteo con Ventoy  
1. Instalar **Ventoy** en una memoria USB.  
2. Ventoy crea una partición especial con un **bootloader**.  
3. Copiar varias imágenes ISO dentro de la memoria.  
4. Al reiniciar, se muestra un menú para elegir la ISO.  

> **Nota:** Ventoy admite múltiples ISOs en una sola memoria.  

---

### 1.3. Bootloader y GRUB  
- **Bootloader:** Programa inicial que permite arrancar un sistema operativo.  
- **GRUB:** Bootloader ampliamente usado en Linux, permite seleccionar entre varios sistemas.  

---

### 1.4. Sistemas de Archivos Compatibles  
- **FAT32:** Usado en USB, pero con límite de 4 GB por archivo.  
- **exFAT:** Similar a FAT32, sin límite de 4 GB.  
- **NTFS:** Propio de Windows, soporta archivos grandes.  
- **ext4:** Usado en Linux, eficiente y robusto.  

---

### 1.5. Estructura de Particiones  
- **MBR (Master Boot Record):** Hasta 4 particiones primarias, máximo 2 TB.  
- **GPT (GUID Partition Table):** Hasta 128 particiones, soporta discos grandes y UEFI.  

---

## 2. Descarga e Inserción de Imágenes  

### 2.1. Descarga de Imágenes ISO  
- Ubuntu: [Página oficial](https://ubuntu.com/download/desktop)  
- Windows: [Página oficial](https://www.microsoft.com/software-download/windows10)  

---

### 2.2. Proceso en Rufus (Ubuntu)  
1. Seleccionar la memoria USB.  
2. Cargar la ISO de Ubuntu.  
3. Configurar GPT o MBR según la BIOS.  
4. Iniciar la escritura.  

---

### 2.3. Proceso en Ventoy (Ubuntu y Windows)  
1. Instalar Ventoy en la memoria USB.  
2. Copiar las ISOs de Ubuntu y Windows en la memoria.  
3. Reiniciar y elegir la ISO desde el menú de Ventoy.  

---

## 3. Instalación de Ubuntu  

### 3.1. Generación de Particiones  
- Iniciar desde la memoria booteable.  
- Seleccionar “Instalar Ubuntu”.  
- Crear particiones:  
  - `/` (raíz, mínimo 20 GB)  
  - `swap` (memoria de intercambio)  
  - `/home` (archivos de usuario)  

---

### 3.2. Proceso de Instalación Paso a Paso  
1. Pantalla de bienvenida e idioma.  
2. Selección del tipo de instalación.  
3. Configuración de particiones.  
4. Instalación y copia de archivos.  
5. Reinicio y primer inicio de sesión.  

---

## 4. Conclusiones  

- **Rufus:** Rápido y sencillo, ideal para una sola ISO.  
- **Ventoy:** Flexible, soporta múltiples ISOs en una memoria.  
- El **bootloader** es esencial para iniciar cualquier sistema operativo.  
- La elección de particiones depende de la BIOS/UEFI y del tamaño del disco.  

### 4.1 Conclusiones – Instalación Ubuntu  
- La instalación de Ubuntu es clara y guiada, incluso para principiantes.  
- La correcta creación de particiones es crítica para un sistema estable.  
- El instalador permite personalizar la instalación según las necesidades.  
- Una vez copiados los archivos y reiniciado, el sistema arranca de manera fluida.  
- Ubuntu ofrece un proceso de instalación intuitivo, estable y adaptable.  
