---
title: Arquitectura de la Aplicación - Restricciones Técnicas
has_children: false
more-content: true
ordered: true
parent: ANI Registraduria 
toc: true
---

# Restricciones Técnicas.

[Regresar al principal](../../plantilla-arquitectura-aplicacion.html)

- API Management Interno: Los servicios RESTFULL deben ser expuestos en el ambiente interno de API Management de EPM.

- Azure Key Vault: El uso de secretos para las cadenas de conexión, conexión al API Management y datos sensibles en el proyecto se deben realizar mediante el servicio Azure KeyVault.

- Application Insights: Se debe utilizar Application Insights para todo el control y monitoreo de la aplicación.

- Integración con sistemas externos: El servicio se debe integrar al sistema externo suministrado por la Registraduría Nacional del Estado Civil.

- Cifrado de la información: Se debe implementar un mecanismo de encriptado y desencriptado de información acorde a los lineamientos y estándares exigidos por la Registraduría Nacional del Estado Civil.
- La Aplicación debe ser Native Cloud en Azure: Toda la infraestructura que se use para modernizar la aplicación de Registraduría se debe implementar en la nube de Azure.

- Herramientas de control, evaluación y seguridad del Código: Se utilizarán las siguientes herramientas GIT, SonarQube y Fortify respectivamente.

- Fácil integración: Se debe desarrollar una aPlicación de tipo API que permita ser consumida por las aplicaciones internas de EPM.