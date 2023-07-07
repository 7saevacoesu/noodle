# Ejercicios packet tracer resueltos ccna2: cÃ³mo configurar y solucionar problemas de redes con routers y switches
 
Packet tracer es una herramienta de simulaciÃ³n de redes que permite diseÃ±ar, configurar y solucionar problemas de redes con routers y switches Cisco. Es muy Ãºtil para los estudiantes que quieren prepararse para el examen de certificaciÃ³n CCNA 2, que cubre los temas de arquitectura, componentes y operaciones de routers y switches en una red pequeÃ±a.
 
En este artÃ­culo, vamos a ver algunos ejercicios packet tracer resueltos ccna2 que te ayudarÃ¡n a practicar y mejorar tus habilidades de configuraciÃ³n y soluciÃ³n de problemas de redes. Estos ejercicios estÃ¡n basados en los laboratorios y actividades del curso CCNA 2: Activities & Lab Manuals Packet Tracer Instructions Answers[^2^], que puedes consultar para mÃ¡s detalles.
 
**Download File ››› [https://t.co/vYN3KbR5Wj](https://t.co/vYN3KbR5Wj)**


 
## Ejercicio 1: ConfiguraciÃ³n de interfaces IPv4 e IPv6
 
En este ejercicio, vas a configurar las interfaces IPv4 e IPv6 de dos routers y dos PCs en una red con la siguiente topologÃ­a:

    PC0 --- R1 --- R2 --- PC1

Los requisitos son los siguientes:
 
- Asigna las direcciones IPv4 e IPv6 a las interfaces de los routers y los PCs segÃºn la tabla.
- Configura el nombre de host, la contraseÃ±a de consola y la contraseÃ±a enable en los routers.
- Verifica la conectividad entre los dispositivos usando los comandos ping y traceroute.

La tabla con las direcciones es la siguiente:

| Dispositivo | Interfaz | DirecciÃ³n IPv4 | DirecciÃ³n IPv6 |
| --- | --- | --- | --- |

| R1 | G0/0 | 192.168.1.1/24 | 2001:DB8:ACAD:1::1/64 |

| R1 | S0/0/0 | 10.1.1.1/30 | 2001:DB8:ACAD:2::1/64 |

| R2 | S0/0/0 | 10.1.1.2/30 | 2001:DB8:ACAD:2::2/64 |

| R2 | G0/0 | 192.168.2.1/24 | 2001:DB8:ACAD:3::1/64 |

| PC0 | NIC | 192.168.1.10/24 | 2001:DB8:ACAD:1::10/64 |

| PC1 | NIC | 192.168.2.10/24 | 2001:DB8:ACAD:3::10/64 |

| Gateway predeterminado / DirecciÃ³n del siguiente salto (next hop) |
| --- |

| Dispositivo / Interfaz destino | DirecciÃ³n IPv4 del gateway predeterminado / DirecciÃ³n del siguiente salto (next hop) | DirecciÃ³n IPv6 del gateway predeterminado / DirecciÃ³n del siguiente salto (next hop) |
| --- | --- | --- |

| PC0 / R1 G0/0 | N/A (directamente conectado) |
| --- | --- |

| PC0 / R2 S0/0/0 | R1 S0/0/0 (10.1.1.1 /

2001:DB8:ACAD:2::1) |
| --- | --- |

| PC0 / PC1 | R1 S0/0/0 (10.1.1.1 /
2001:DB8:ACAD:2::1) |
| --- | --- |

| R1 / R2 S0/0/0 | N/A (directamente conectado) |
| --- | --- |

| R1 / PC1 | R2 S0/0/0 (10.1.1.2 /
2001:DB8:ACAD:2::2) |
| --- | --- |

| R2 / PC1 | N/A (directamente conectado) |
| --- | --- |

| PC1 / PC0 | R2 S0/0/0 (10.1.1.2 /
2001:DB8:ACAD:2::2) |
| --- | --- |

Los pasos para configurar las interfaces IPv4 e IPv6 son los siguientes:

1. En el router R1, ingresa al modo de configuraciÃ³n global con el comando `enable` y luego `configure terminal`.
2. Asigna el nombre de host R1 con el comando `hostname R1`.
3. Configura la contraseÃ±a de consola con el comando `line console 0`, seguido de `password cisco` y `login`.
4. Configura la contraseÃ±a enable con el comando `enable secret class`.
5. Sal del modo de configuraciÃ³n de lÃ­nea con el comando `exit`.
6. Configura la interfaz G0/0 con el comando `interface G0/0`, seguido de `ip address 192.168.1.1 255.255.255.0` y `ipv6 address 2001:DB8:ACAD:1::1/64`.
7. Activa la interfaz G0/0 con el comando `no shutdown`.
8. Sal del modo de configuraciÃ³n de interfaz con el comando `exit`.
9. Configura la interfaz S0/0/0 con el comando `interface S0/0/0`, seguido de `ip address 10.1.1.1 255.255.255.252` y `ipv6 address 2001:DB8:ACAD:2::1/64`.
10. Activa la interfaz S0/0/0 con el comando `no shutdown`.
11. Sal del modo de configuraciÃ³n de interfaz con el comando `exit`.
12. Guarda la configuraciÃ³n con el comando `wr`.
13. Sigue los mismos pasos para configurar las interfaces IPv4 e IPv6 del router R2, cambiando los nombres y las direcciones segÃºn la tabla.
14. En el PC0, abre la ventana de configuraciÃ³n IP y asigna las direcciones IPv4 e IPv6 segÃºn la tabla.
15. Especifica la direcciÃ³n IPv4 e IPv6 del gateway predeterminado segÃºn la tabla.
16. Sigue los mismos pasos para configurar las direcciones IPv4 e IPv6 del PC1, cambiando las direcciones segÃºn la tabla.

Para verificar la conectividad entre los dispositivos, puedes usar los siguientes comandos:

- `ping ip-address`: envÃ­a paquetes ICMP a la direcciÃ³n IP especificada y muestra si hay respuesta o no.
- `ping ipv6 ipv6-address`: envÃ­a paquetes ICMPv6 a la direcciÃ³n IPv6 especificada y muestra si hay respuesta o no.
- `traceroute ip-address`: muestra la ruta que siguen los paquetes hasta llegar a la direcciÃ³n IP 8cf37b1e13


