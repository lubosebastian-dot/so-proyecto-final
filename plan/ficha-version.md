# Ficha de verificación de versión - Grupo 07

*Fecha de consulta de fuentes oficiales: 19 de noviembre de 2026.*

---

## 1. VM gráfica (`g07-grafica`): Xubuntu

| Pregunta | Respuesta | Enlace oficial |
|---|---|---|
| Versión elegida y fecha de lanzamiento | Xubuntu 26.10 (versión intermedia más reciente; verificar fecha exacta de lanzamiento y comparar frente a la LTS vigente en la página oficial) | https://xubuntu.org/releases/ |
| Hasta cuándo recibe actualizaciones de seguridad | Verificar el periodo de soporte de seguridad de Xubuntu 26.10 en la documentación oficial (las versiones intermedias tienen un ciclo de soporte más corto que las LTS) | https://xubuntu.org/releases/ |
| Requisitos de hardware y funcionamiento en VirtualBox | Compatible con VirtualBox 7.x; para el proyecto se configuran 2 a 4 GB de RAM, 25 GB de disco y 2 CPU (con 128 MB de memoria de vídeo en la VM gráfica). Verificar requisitos detallados en el sitio oficial. | https://xubuntu.org/ |
| Particionado manual en el instalador | Sí, permite particionado manual para crear `/`, `swap` y `/home` sin borrar el disco con particiones automáticas. | https://xubuntu.org/ |
| Guía oficial para instalar Docker Engine | Existe guía oficial para la familia Ubuntu/Debian (en este proyecto Docker Engine se instala en la VM de consola). | https://docs.docker.com/engine/install/ubuntu/ |
| Imagen base del Dockerfile en Docker Hub | No aplica como imagen base del Dockerfile del Grupo 07 (corresponde Alpine). | https://hub.docker.com/ |

---

## 2. VM de consola (`g07-consola`): Rocky Linux

| Pregunta | Respuesta | Enlace oficial |
|---|---|---|
| Versión elegida y fecha de lanzamiento | Rocky Linux 10 (rama estable más reciente; verificar versión menor y fecha de lanzamiento en la documentación oficial) | https://docs.rockylinux.org/ |
| Hasta cuándo recibe actualizaciones de seguridad | Verificar las fechas de soporte activo y soporte de seguridad en la documentación oficial de Rocky Linux | https://docs.rockylinux.org/ |
| Requisitos de hardware y funcionamiento en VirtualBox | Compatible con VirtualBox 7.x; se configura con disco de 25 GB, 2 CPU y 2 GB de RAM al instalarla (3 GB en el Sprint 3 para Kubernetes). | https://docs.rockylinux.org/ |
| Particionado manual en el instalador | Sí, mediante particionado personalizado para crear `/`, `swap`, `/home` y `/var` (mínimos de referencia: `/` 5 GB, `/var` 10 GB, `swap` 1 GB y `/home` 1 GB). | https://docs.rockylinux.org/ |
| Guía oficial para instalar Docker Engine | Sí, mediante la guía oficial de Docker Engine para distribuciones basadas en RHEL / Rocky Linux. | https://docs.docker.com/engine/install/rhel/ |
| Imagen base del Dockerfile en Docker Hub | No aplica como imagen base del Dockerfile del Grupo 07 (corresponde Alpine). | https://hub.docker.com/ |

---

## 3. Imagen base del Dockerfile: Alpine Linux

| Pregunta | Respuesta | Enlace oficial |
|---|---|---|
| Versión elegida y fecha de lanzamiento | Alpine Linux (rama estable más reciente; verificar versión/tag y fecha de lanzamiento en el sitio oficial) | https://alpinelinux.org/releases/ |
| Hasta cuándo recibe actualizaciones de seguridad | Verificar la fecha de fin de soporte de la rama elegida en la tabla oficial de releases de Alpine | https://alpinelinux.org/releases/ |
| Requisitos de hardware y funcionamiento en VirtualBox | Imagen base ligera de contenedor ejecutada sobre Docker Engine en `g07-consola` dentro de VirtualBox; usa `apk` para instalar `git`, `curl`, editor y compilador. | https://docs.docker.com/engine/install/ |
| Particionado manual en el instalador | No aplica a una imagen base de contenedor. | https://alpinelinux.org/releases/ |
| Guía oficial para instalar Docker Engine | Docker Engine se instala en la VM de consola (`g07-consola`) siguiendo la documentación oficial de Docker. | https://docs.docker.com/engine/install/ |
| Imagen base en Docker Hub | Sí, imagen oficial `alpine` disponible en Docker Hub. | https://hub.docker.com/_/alpine |

