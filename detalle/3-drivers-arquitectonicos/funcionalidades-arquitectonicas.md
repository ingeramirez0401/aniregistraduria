---
title: Arquitectura de la Aplicación - Funcionalidades Arquitectónicas
has_children: false
more-content: true
ordered: true
parent: ANI Registraduria 
toc: true
---

# Funcionalidades Arquitectónicas.

[Regresar al principal](../../plantilla-arquitectura-aplicacion.html)

## **Consulta Individual de Cédulas de Identidad**

La aplicación debe permitir la consulta de cédulas de manera individual por medio de un servicio expuesto por la Registraduría.

Esta funcionalidad afecta la arquitectura debido a que se debe realizar el consumo de un endpoint expuesto por la Registraduría.

## **Consulta Masiva de Cédulas de Identidad**

La aplicación debe permitir la consulta de cédulas de manera masiva por medio de un servicio expuesto por la Registraduría.

Esta funcionalidad afecta la arquitectura debido a que se debe realizar el consumo de un endpoint expuesto por la Registraduría.

## **Cambio de Clave de usuario de consulta**

Esta funcionalidad se utiliza para gestionar el cambio de clave de los diferentes actores que realizan uso del servicio de consulta de contraseñas, se contempla el uso de dos usuarios, uno que se utilizará de manera interna y otro que se utilizará para usuarios externos a EPM.

Esta funcionalidad impacta la arquitectura debido a que se debe incorporar una funcionalidad que permita consumir el servicio de Registraduría y realizar el cambio de contraseña según los parámetros requeridos.

Esta funcionalidad también impacta la arquitectura porque se requiere crear un servicio REST para el consumo del usuario.

## **Notificación para cambio de clave**

La aplicación debe permitir la notificación a los usuarios para realizar el cambio de clave de manera oportuna

Esta funcionalidad afecta la arquitectura debido a que se debe realizar el consumo de notificaciones expuesto en Azure.

Esta funcionalidad impacta la arquitectura debido a que se debe crear una funcionalidad que realice el consumo del servicio de notificación de manera periódica al cumplirse un determinado plazo de vencimiento de cambio de contraseña.
