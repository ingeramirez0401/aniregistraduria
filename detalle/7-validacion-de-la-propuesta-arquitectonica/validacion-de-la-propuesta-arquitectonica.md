---
title: Arquitectura de la Aplicación - Validación de la Propuesta Arquitectónica
has_children: false
more-content: true
ordered: true
parent: ANI Registraduria 
toc: true
---

# Validación de la Propuesta Arquitectónica.

<!-- Describa cómo se validará el cumplimiento de los Drivers Arquitectónicos. Por ejemplo, para dar cumplimiento al Escenario xxx que se refiere a Rendimiento, se va a construir una prueba de concepto que simulara el escenario descrito con el objetivo de garantizar su cumplimiento. Recuerde que no es necesario construir siempre una nueva Prueba de Concepto, reutilice Pruebas de concepto de soluciones anteriores. Sólo en casos muy reducidos y sólo cuando este muy seguro del cumplimiento de un Driver Arquitectónico, refiérase a su experiencia previa, la cual tendrá que ser sustentada en la Revisión Interna de Arquitectura y por supuesto con el Cliente. De igual manera, se puede hacer referencia a las pruebas de concepto ya realizadas y que han sido documentadas de forma detallada dentro de las bitácoras respectivas. La idea no es repetir aquellas pruebas que ya han sido realizadas por otro equipo previamente y que buscan validar el mismo contexto -->

[Regresar al principal](../../plantilla-arquitectura-aplicacion.html)

##   **Autenticar en el sistema**

Para el cumplimiento de este escenario de calidad el cual apunta al atributo de calidad de seguridad se realizara lo siguiente:

En primer lugar el acceso a la plataforma solo se permitirá a través del directorio activo de EPM por medio de VPN ya que esta plataforma será de uso exclusivo por medio de integración API con las aplicaciones propias de EPM que requieran hacer uso del módulo de consultas de la Registraduría.

##   **Gestión de Solicitudes**

Para el cumplimiento de este escenario de calidad el cual apunta al atributo de calidad de seguridad se realizará lo siguiente:

**Escenario Exitoso:** Se generarán un par de llaves para encriptado y desencriptado mediante protocolo RSA que junto a un usuario de consultas entregado por la Registraduría se combinarán para realizar las solicitudes de consulta sobre el servicio expuesto por la Entidad. Este par de llaves deben ser pares correctos y deben ser generados por la Registraduría mediante el convenio de integración con EPM.

**Escenario No Exitoso:** Si el par de llaves o el usuario de consulta no son correctos o la contraseña del usuario se encuentra vencida no se debe poder permitir ninguna consulta al servicio expuesto por la Entidad.

