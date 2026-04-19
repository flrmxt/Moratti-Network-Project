# Moratti-Network-Project

Este repositorio contiene la arquitectura de red completa hecha por **Moratti**, una empresa dominicana de relojería de lujo inteligente que integra artesanía con tecnologías blockchain y NFC. 

## 👥 Equipo de Proyecto
* **Project Leader:** Silfredo Mitchell Vargas Fernandez
* **Assistant Leader:** Enyer Osmar Roa Zarzuela
* **Engineering Team:** * Brayan Ariel Carrasco De León
    * Alessandro Ciavaglia Mejia
    * Cesar Augusto Rivera Pantaleon
    * Jorge Enmanuel Sime Matos
* **Documentation & Deliverables:** * Matthews James Guzman
    * Michael Manuel Cotes Aquino

## 🌐 Resumen de la Topología
La red utiliza una arquitectura jerárquica de tres capas distribuida en tres sedes geográficas interconectadas mediante un backbone seguro:

| Sede | Función | Área OSPF |
| :--- | :--- | :--- |
| **Santo Domingo** | Central (Core, Distribución y Gestión) | Área 1 |
| **Santiago** | Atelier de Manufactura y Data Center | Área 2 |
| **La Romana** | Boutique Remota y Ventas | Área 3 |
| **Backbone VPN** | Interconexión GRE/IPSec | Área 0 |

## 🛠️ Tecnologías Implementadas
* **Enrutamiento:** OSPF Multi-área para optimizar la tabla de ruteo.
* **Alta Disponibilidad:** HSRP (Hot Standby Router Protocol) en el core de Santo Domingo.
* **Seguridad WAN:** Túneles GRE protegidos con **IPSec (AES-256)** para garantizar la integridad de los datos de fabricación y patentes.
* **Seguridad LAN:** Implementación de DHCP Snooping, Dynamic ARP Inspection (DAI) y Port-Security.
* **Servicios:** Cluster de servidores (DNS, Web, DHCP, Mail y RADIUS para autenticación centralizada).

## 📂 Estructura del Repositorio
* `/Scripts`: Configuraciones finales de routers y switches (.cfg).
* `/Documentation`: Documentación técnica detallada, plan de direccionamiento VLSM y manuales de verificación.

---
*Este proyecto fue desarrollado como parte de la formación técnica en el ITLA.*
