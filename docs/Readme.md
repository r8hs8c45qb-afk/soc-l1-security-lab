🛡️ Laboratorio de Seguridad SOC L1

Este proyecto consiste en el despliegue de un laboratorio de seguridad perimetral y monitoreo de eventos (SOC) utilizando un entorno virtualizado con tres nodos principales:

Kali Linux (Atacante): Nodo utilizado para simulaciones de intrusión y escaneo de vulnerabilidades.
Parrot OS (Analista): Estación de trabajo configurada para el análisis de tráfico y respuesta ante incidentes.
Ubuntu Server (Servidor/Colector): Nodo central encargado de la recolección de logs y servicios críticos.
🎯 Objetivos del Proyecto

Configuración de una red interna segura para el tráfico de telemetría.
Implementación de servicios de recolección de logs mediante Rsyslog.
Simulación de ataques y validación de la capacidad de detección del sistema.
Documentación técnica de incidentes y resolución de problemas (Troubleshooting).
🚀 Pruebas de Concepto (PoC) y Detección en Tiempo Real

Para validar el funcionamiento del laboratorio y la correcta centralización de logs, se simuló un escenario de intrusión desde la máquina atacante hacia el servidor central.

1. Detección de Logs de Seguridad (Blue Team)

Tras habilitar el servicio sshd y configurar el monitoreo, el colector de logs en Ubuntu Server registró satisfactoriamente los intentos de conexión. En la captura se observa el flujo de telemetría capturado en tiempo real mediante syslog. Detección de Logs

2. Acceso Remoto Exitoso (Red Team)

Simulación de una intrusión completada desde Kali Linux. Esta prueba validó no solo la conectividad de red, sino también la capacidad del analista para identificar cuándo una sesión remota ha sido establecida con éxito en el sistema víctima. Éxito de Intrusión

🛠️ Resolución de Desafíos Técnicos (Troubleshooting)

Durante el despliegue se identificaron y resolvieron los siguientes incidentes críticos:

Gestión de Red: Corrección del error No route to host mediante la re-identificación de IPs dinámicas tras cambios en el servicio DHCP del entorno virtual.
Habilitación de Servicios: Instalación y despliegue manual de openssh-server tras detectar estados de Connection refused durante las pruebas de escaneo inicial.
Este proyecto demuestra habilidades en Linux, Networking, Gestión de Logs y Resolución de problemas técnicos.

🛡️ Laboratorio de Redes Seguras: pfSense Firewall & Suricata IDS Este proyecto documenta el despliegue de una infraestructura de red segura utilizando pfSense como firewall perimetral y Suricata como sistema de detección de intrusos (IDS). El objetivo es crear un entorno controlado (Sandbox) para la monitorización y análisis de amenazas en tiempo real. 🚀 Hitos Técnicos Alcanzados

Configuración de Red y Firewall (pfSense) • Segmentación LAN/WAN: Configuración de interfaces para aislar la red interna (LAN) del tráfico externo (WAN). • Asignación Estática: Implementación de la interfaz LAN con direccionamiento IPv4 estático (192.168.1.1/24). • Servicios de Red: Configuración de Gateway y reglas de filtrado para permitir la salida controlada a Internet desde la red interna.
Implementación de IDS (Suricata) • Instalación y Despliegue: Configuración del motor Suricata específicamente sobre la interfaz LAN (em1) para monitorizar el tráfico de los clientes. • Gestión de Firmas: Activación de reglas de Emerging Threats (como emerging-scan y emerging-malware) para detectar intentos de reconocimiento y actividad maliciosa. • Seguridad Activa: Configuración del sensor en modo de ejecución continua (Estado: Running) con políticas de registro de logs de alertas habilitadas. Validación y Prueba de Concepto (Ubuntu) Cliente Interno: Despliegue de una máquina Ubuntu Desktop dentro de la red LAN protegida. Auditoría de Tráfico: Ejecución de pruebas de detección mediante firmas conocidas utilizando el comando: curl http://testmyids.com Estructura de Evidencias (Capturas) Para documentar este proyecto, se han generado las siguientes evidencias:
Configuracion_Interfaz_LAN.png: Muestra la asignación de la IP 192.168.1.1 en pfSense.
Suricata_Status_Running_LAN.png: Captura del servicio Suricata activo con el check verde en la interfaz LAN.
Logging_Configuration_IDS.png: Ajustes de "Send Alerts to System Log" para la recolección de eventos.
Prueba_Conectividad_Ubuntu.png: Terminal de Ubuntu ejecutando el tráfico de prueba de intrusión.
Validacion_Logs_Suricata.png: Vista de Logs View confirmando que el archivo de alertas se carga y procesa correctamente. 🛠️ Tecnologías Utilizadas • pfSense Community Edition (Firewall/Router) • Suricata (IDS/IPS Engine) • Ubuntu Desktop (Client Endpoint) • Virtualización (Entorno Sandbox seguro) 👨‍💻 Conclusión Técnica Este laboratorio demuestra la capacidad para diseñar una arquitectura de red robusta, gestionar reglas de firewall y desplegar herramientas de monitorización de seguridad de nivel empresarial. La integración de Suricata permite pasar de una seguridad pasiva a una defensa proactiva, siendo capaz de identificar patrones de ataque antes de que afecten a los activos finales.
