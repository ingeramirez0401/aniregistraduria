---
title: Arquitectura de la Aplicación - Decisiones Arquitectónicas
has_children: false
more-content: true
ordered: true
parent: ANI Registraduria 
toc: true
---

# Decisiones Arquitectónicas

<!--
Describa cada una de las Decisiones Arquitectónicas que se toman para dar respuesta a los Drivers Arquitectónicos Planteados. Prefiera el uso de Patrones Arquitectónicos para solucionar problemas recurrentes. Use referencias Bibliográficas cuando sea apropiado para describir los Patrones y Tácticas a utilizar.
-->

[Regresar al principal](../../plantilla-arquitectura-aplicacion.html)

Se identifican las siguientes alternativas:

- Alternativa 1: Aplicación Enterprise Java Beans (EJB).

- Alternativa 2: Aplicación Java Spring Framework.

- Alternativa 3: Aplicación .NET Core API.

Los valores de las alternativas en la toma de decisiones van de 0 a 5, siendo 5 el nivel más óptimo.

Se valoran diferentes criterios entre atributos de calidad de la aplicación, esfuerzo en el desarrollo de la aplicación y costos del mismo, riesgos y cumplimiento de los lineamientos organizacionales, fue necesario detallar las decisiones arquitectónicas por cada contexto de subdominio.

[TomaDesicion.xlsx](../../recursos/documents/TomaDesicion.xlsx)

Para dar solución a las expectativas de calidad del proyecto, descritas anteriormente en la sección de Drivers Arquitectónicos, se han tomado las siguientes decisiones a nivel de arquitectura las cuales tiene como base las siguientes características:

#### Alternativa 3: Aplicación .NET Core API.

.NetCore es un marco multiplataforma de código abierto, con él es posible crear aplicaciones modernas habilitadas para la nube y servicios web, esto mediante el lenguaje de programación c#. Para su utilización se cuenta con un conjunto de herramientas de desarrollo facilitadas por Microsoft, las cuales están disponibles para diferentes sistemas operativos.


**Se decide:**

- Al realizar el análisis del archivo TomaDecisión.xlsx, las ventajas, desventajas y los costos aproximados por cada alternativa propuesta, se llega a la conclusión que la opción que mas se acomoda y suple todas las necesidades del proyecto de ANI Registraduría es: Alternativa 3: Aplicación .NET Core API.

- Se toma esta decisión inicialmente debido a que el negocio requería realizar una actualización de su capacidad técnica con la versión actual de la aplicación. Sin embargo, en socializaciones y pruebas de concepto se evidencia el potencial de esta alternativa, teniendo en cuenta que cuenta con un sin fin de elementos y tecnologías emergentes que permiten un mayor desempeño de la aplicación. Por otro lado se tuvo en cuenta que EPM se encuentra modernizando sus aplicaciones y en su mayoría se han enfocado en tecnología .NET y finalmente se determina que el servicio de integración de Registraduría no tiene ningún impedimento para integrarse a un API desarrollada con .NET Core.