# Ficha de verificación de versión - Grupo 07

*Fecha de consulta de fuentes oficiales: 19 de noviembre de 2026.*

---

## 1. VM gráfica (`g07-grafica`): Xubuntu

| Pregunta | Respuesta | Enlace oficial |
|---|---|---|
| Versión elegida y fecha de lanzamiento | Xubuntu 26.10 (versión intermedia más reciente), lanzada el 15 de octubre de 2026. | https://xubuntu.org/releases/ |
| Hasta cuándo recibe actualizaciones de seguridad | Hasta el 15 de julio de 2027 (9 meses de soporte oficial por ser una versión intermedia) | https://xubuntu.org/releases/ |
| Requisitos de hardware y funcionamiento en VirtualBox | Compatible con VirtualBox 7.x. Es una distribución ligera (Lightweight) cuyos requisitos mínimos son procesador de 64 bits, 1 GB de RAM y 8.6 GB de disco (recomendados: doble núcleo a 1.5 GHz, 2 GB de RAM y 20 GB de disco). La configuración del proyecto (2 a 4 GB de RAM, 25 GB de disco, 2 CPU y 128 MB de vídeo) supera lo recomendado. | https://xubuntu.org/download/ |
| Particionado manual en el instalador | Sí, permite particionado manual para crear `/`, `swap` y `/home` sin borrar el disco con particiones automáticas. | https://xubuntu.org/ |
| Guía oficial para instalar Docker Engine | Sí. Existe guía oficial para Ubuntu 26.10 (64-bit), sistema base de Xubuntu 26.10, con instrucciones de instalación mediante repositorio apt, paquetes .deb o script. | https://docs.docker.com/engine/install/ubuntu/ |
| Imagen base del Dockerfile en Docker Hub | No aplica Ubuntu/Xubuntu como imagen base del Dockerfile del contenedor (corresponde Alpine, disponible como imagen oficial en Docker Hub). | https://hub.docker.com/ |

---

## 2. VM de consola (`g07-consola`): Rocky Linux

| Pregunta | Respuesta | Enlace oficial |
|---|---|---|
| Versión elegida y fecha de lanzamiento | Rocky Linux 10 (rama estable más reciente, con release menor 10.3 lanzada el 16 de noviembre de 2026; rama 10 lanzada inicialmente el 11 de junio de 2025). | https://docs.rockylinux.org/10/releases/ |
| Hasta cuándo recibe actualizaciones de seguridad | Recibe soporte activo hasta el 31 de mayo de 2030 y actualizaciones de seguridad hasta el 31 de mayo de 2035. | https://docs.rockylinux.org/10/releases/ |
| Requisitos de hardware y funcionamiento en VirtualBox | Requisitos mínimos oficiales: arquitectura x86_64-v3, 2 CPU, 2 GB de RAM y 20 GB de almacenamiento. Funciona correctamente en VirtualBox 7.x; se configura con disco de 25 GB, 2 CPU y 2 GB de RAM iniciales (aumentando a 3 GB en el Sprint 3 para Kubernetes). | https://docs.rockylinux.org/10/guides/installation/ |
| Particionado manual en el instalador | Sí, mediante la opción de almacenamiento personalizado (*Custom*) del instalador Anaconda, permitiendo configurar `/`, `swap`, `/home` y `/var` (mínimos de referencia: `/` 5 GB, `/var` 10 GB, `swap` 1 GB y `/home` 1 GB). | https://docs.rockylinux.org/10/guides/installation/ |
| Guía oficial para instalar Docker Engine | Sí, mediante la guía oficial de Docker Engine para distribuciones basadas en RHEL / Rocky Linux utilizando el gestor de paquetes `dnf` y el repositorio oficial de Docker. | https://docs.docker.com/engine/install/rhel/ |
| Imagen base del Dockerfile en Docker Hub | No aplica como imagen base del Dockerfile del Grupo 07 (corresponde Alpine Linux). | https://hub.docker.com/ |

## 3. Imagen base del Dockerfile: Alpine Linux

| Pregunta | Respuesta | Enlace oficial |
|---|---|---|
| Versión elegida y fecha de lanzamiento | Alpine Linux v3.24 (`alpine:3.24`, rama estable más reciente iniciada el 9 de junio de 2026; versión puntual 3.24.4 lanzada el 5 de noviembre de 2026). | https://alpinelinux.org/releases/ |
| Hasta cuándo recibe actualizaciones de seguridad | Recibe actualizaciones de seguridad hasta el 1 de junio de 2028. | https://alpinelinux.org/releases/ |
| Requisitos de hardware y funcionamiento en VirtualBox | Imagen minimalista de contenedor (aprox. 8 MB) que corre sobre Docker Engine dentro de `g07-consola` en VirtualBox; utiliza el gestor de paquetes `apk` para instalar `git`, `curl`, editor y compilador. | https://wiki.alpinelinux.org/wiki/Alpine_Linux_package_management |
| Particionado manual en el instalador | No aplica a una imagen base de contenedor en Docker. | https://alpinelinux.org/about/ |
| Guía oficial para instalar Docker Engine | Docker Engine se instala en el sistema anfitrión de contenedores (`g07-consola` con Rocky Linux) siguiendo la documentación oficial de Docker. | https://docs.docker.com/engine/install/ |
| Imagen base en Docker Hub | Sí, existe la imagen oficial `alpine` mantenida en Docker Hub con etiquetas por versión estable (`alpine:3.24` / `alpine:latest`). | https://hub.docker.com/_/alpine |

