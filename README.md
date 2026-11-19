# Proyecto Infraestructura Corporativa Segmentada — TechnoMarket Ltda.

### Asignatura: Taller-de-administracion-de-sistemas
### Profesor: Gonzalo Mendoza
### Paralelo: 301
### Equipo: 5

| Integrante | Responsabilidades |
| :--- | :--- |
| Felipe Gamboa | Administracion servicio DHCP |
| Francisca Matamala | Diseño de red e infraestructura |
| Macarena Mogollón | Configuracion de infraestructura  |

Proyecto de rediseño e implementación de infraestructura de red corporativa desarrollado para la asignatura Taller de Administración de Sistemas. El objetivo es migrar una red plana hacia una arquitectura segmentada, escalable y segura que interconecte la Casa Matriz (Santiago) con la Sucursal (Valparaíso).

Además de la infraestructura base obligatoria (segmentación por departamentos, enrutamiento inter-VLAN, enlace WAN entre sedes, OSPF, DHCP centralizado con Relay y DNS interno), este proyecto implementa la Variante del **Equipo 5: HTTP en VLAN de servidores:**

**Condición técnica:** Aislar servidor HTTP en VLAN propia y regular acceso desde al menos tres
VLAN de clientes.
**Evidencias:** Acceso por DNS desde dos redes autorizadas y rechazo desde una tercera; modificar
autorización.

### Topología de Red y Direccionamiento

La infraestructura divide el bloque principal 192.168.0.0/24 mediante VLSM entre ambas sedes, reservando la subred 192.168.0.128/26 (192.168.0.129 - 192.168.0.190) para futuras expansiones (tercera sucursal). La interconexión entre sedes utiliza la red WAN 10.0.0.0/30 bajo el protocolo OSPF Área 0.

