# 🛡️ Laboratorio de Seguridad SOC L1

Laboratorio personal de ciberseguridad diseñado para simular una infraestructura empresarial mediante virtualización en Apple Silicon (M-Series).

## 🚀 Objetivo
Diseñar y documentar un entorno defensivo (Blue Team) capaz de centralizar eventos de seguridad para su análisis.

## 🏗️ Arquitectura del Laboratorio
El entorno consta de tres nodos principales comunicados en una red privada:

1. **Kali Linux**: Herramientas de ataque y generación de tráfico.
2. **Parrot Security**: Nodo de análisis y forense.
3. **Ubuntu Server**: Servidor central de logs (Syslog Collector).

## 📊 Hitos Técnicos Logrados
* **Virtualización ARM64**: Despliegue exitoso en UTM sobre arquitectura Apple Silicon.
* **Troubleshooting de SIEM**: Resolución de conflictos de arquitectura y memoria RAM al intentar desplegar Wazuh.
* **Centralización de Logs**: Implementación de un colector Rsyslog en puerto 514 para recibir eventos de los nodos atacantes.



---
*Este proyecto demuestra habilidades en Linux, Networking, Gestión de Logs y Resolución de problemas técnicos.*
