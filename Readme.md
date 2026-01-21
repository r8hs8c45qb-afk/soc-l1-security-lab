# 🛡️ Laboratorio de Seguridad SOC L1

Este proyecto consiste en el despliegue de un laboratorio de seguridad perimetral y monitoreo de eventos (SOC) utilizando un entorno virtualizado con tres nodos principales:

* **Kali Linux (Atacante):** Nodo utilizado para simulaciones de intrusión y escaneo de vulnerabilidades.
* **Parrot OS (Analista):** Estación de trabajo configurada para el análisis de tráfico y respuesta ante incidentes.
* **Ubuntu Server (Servidor/Colector):** Nodo central encargado de la recolección de logs y servicios críticos.

## 🎯 Objetivos del Proyecto
1.  Configuración de una red interna segura para el tráfico de telemetría.
2.  Implementación de servicios de recolección de logs mediante **Rsyslog**.
3.  Simulación de ataques y validación de la capacidad de detección del sistema.
4.  Documentación técnica de incidentes y resolución de problemas (Troubleshooting).

---

## 🚀 Pruebas de Concepto (PoC) y Detección en Tiempo Real

Para validar el funcionamiento del laboratorio y la correcta centralización de logs, se simuló un escenario de intrusión desde la máquina atacante hacia el servidor central.

### 1. Detección de Logs de Seguridad (Blue Team)
Tras habilitar el servicio `sshd` y configurar el monitoreo, el colector de logs en **Ubuntu Server** registró satisfactoriamente los intentos de conexión. En la captura se observa el flujo de telemetría capturado en tiempo real mediante `syslog`.
![Detección de Logs](./deteccion-ataque-sshd-syslog.png)

### 2. Acceso Remoto Exitoso (Red Team)
Simulación de una intrusión completada desde **Kali Linux**. Esta prueba validó no solo la conectividad de red, sino también la capacidad del analista para identificar cuándo una sesión remota ha sido establecida con éxito en el sistema víctima.
![Éxito de Intrusión](./evidencia-exito-intrusion-ssh.png)

## 🛠️ Resolución de Desafíos Técnicos (Troubleshooting)

Durante el despliegue se identificaron y resolvieron los siguientes incidentes críticos:
* **Gestión de Red:** Corrección del error `No route to host` mediante la re-identificación de IPs dinámicas tras cambios en el servicio DHCP del entorno virtual.
* **Habilitación de Servicios:** Instalación y despliegue manual de `openssh-server` tras detectar estados de `Connection refused` durante las pruebas de escaneo inicial.

---
*Este proyecto demuestra habilidades en Linux, Networking, Gestión de Logs y Resolución de problemas técnicos.*
