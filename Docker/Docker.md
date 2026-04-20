---
id: MOC-DOCKER-01
titulo: Arquitectura y Primeros Pasos
tags:
---
# Contexto Historico
Anteriormente, los servidores solo podían correr una aplicación a la vez. Windows y Linux no tenían la capacidad de ejecutar múltiples aplicaciones en el mismo servidor de forma segura. Como consecuencia, cada que un negocio o empresa necesitaba un nuevo servicio, debía comprar un nuevo servidor

## Virtual Machines
Las maquina virtuales (ó VM por sus siglas en inglés) permitieron correr múltiples aplicaciones en un solo servidor. Sin embargo esto no es perfecto, cada VM consumía CPU y RAM del servidor, limitando la capacidad del servidor. Además, cada Sistema Operativo presente en cada una de las VM necesitaba mantenimiento, monitoreo y, en algunas casos, licencias.

Otras problemáticas relacionadas con las VMs eran los tiempos de arranque que solían ser lentos y la poca portabilidad al momento de migrar y mover las cargas de trabajo (workloads) entre el hipervisor y las plataformas en la nube.

# Contenedores
Para abordar las deficiencias presentes en las VM, muchas empresas recurrieron al uso de contenedores.

A diferencia de las VM, los contenedores no requieren su propio sistema operativo. De hecho, todos los contenedores en un solo host comparten el Sistema Operativo del host. Gracias a esto se disminuye la demande de recursos, consumiendo menos RAM, CPU y almacenamiento.

Los contenedores, además, se ejecutan rápido y son más portables que una VM.