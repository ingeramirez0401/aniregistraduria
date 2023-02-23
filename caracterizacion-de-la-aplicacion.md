---
title: Arquitectura de la Aplicación - Encuesta de Caracterización Aplicaciones
has_children: false
more-content: true
ordered: true
parent: ANI Registraduria 
toc: true
---

# Encuesta de Caracterización Aplicaciones.

[Regresar al principal](../../plantilla-arquitectura-aplicacion.html)

## Objetivo
Obtener la información técnica y de negocio necesarios para definir los atributos de calidad y drivers de arquitectura necesarios para proporcionar una visión general del sistema y un marco de referencia para el diseño y desarrollo arquitectónico de la solución.

## Justificación
Definir el marco de referencia en la que los arquitectos de software, al momento de diseñar o concebir las nuevas alternativas de solución, dispongan de información suficiente y así consideren la mayor cantidad de tecnologías, componentes y consideraciones para que la aplicación sea lo más ajustada en resolver las necesidades del negocio.

## Preguntas de la encuesta de caracterización
### Restricciones

#### - Técnicas
* ¿Qué Stack tecnológico hay disponible en la Organización?
  * Componentes que nos ofrece Azure Cloud como nube primaria. (AKS, Services Plan, Api Management, Azure Function, Redis, Blob Storage, Servicios Azure.
* ¿Qué Frameworks de desarrollo o experiencia de usuario se puede utilizar?
  * .Net 5, .Net Core 3.1, Node Js, TypeScript. No aplica experiencia de usuario.
* ¿En que ambiente se debe desplegar la aplicación (Nube - Azure, AWS, Google, OnPremise).
  * Se debe desplegar en la nube de Azure.
* ¿Qué disponibilidad de Licencias del Software tenemos?.
  * Licencias de Visual Studio y plan de suscripción de Azure.
* ¿Qué restricciones de Presupuesto tenemos?
  * No se designará un valor hasta que sea aceptada la estimación de modernización.
* ¿Se cuenta con algún presupuesto para infraestructura?
  * Todos los recursos que se requieran deben estar ya aprobados por infraestructura y si hay uno nuevo se debe pedir la aprobación por los encargados dentro del presupuesto del proyecto.
* ¿Qué transacciones por unidad de tiempo se pueden llegar a presentar?
  * De 30 a 50 transacciones diarias.
* ¿Cuál es tamaño de los mensajes?
  * Tamaño del archivo de mensajes depende de los mensajes de cada aplicación, se tiene contemplado que entre 2Mb y 100Mb por archivo de mensajes.

#### - Negocio

* ¿Qué presupuesto estimado se tiene para implementar la solución?.
  * El presupuesto se presentó de acuerdo a la estimación de alto nivel aportada por IG en el alcance planteado.
* ¿Cuáles son las personas de negocio involucradas en la solución?
  * Todos los analistas de aplicaciones nuevas.
* ¿Se tiene una metodología de trabajo en especial?
  * Se usará Marco Ágil.
* ¿Cuál es la fecha de Deadline de la solución?
  * Se tiene estimado a muy alto nivel que la duración sea de aproximadamente 5 meses de trabajo.

### Atributos de calidad
#### - Fiabilidad

* ¿Qué debe suceder cuando algunos de los componentes de la solución están fuera de servicio?
  * Se crea un flujo de revisión a través de un catálogo de servicio, dirigido al personal de soporte de TI.
  * El cliente informa al equipo a cargo de los servidores que la aplicación está fuera de servicio.
* ¿Qué información le debo presentar al usuario cuando ocurre un error en el proceso?
  * Se debe mostrar un mensaje indicando el error para ser escalado al área correspondiente.
* ¿Qué debe hacer el sistema cuando ocurre un error durante una transacción? RollBack?
  * Se debe tener un número de reintentos para terminar la transacción y de no ser así se debe tener control de los procesos que hayan fallado para ser notificados.
* ¿Público objetivo de la aplicación? (pública, interna, contratista)
  * Está diseñado para ser consumido por aplicaciones internas de la compañía o filiales.
* ¿Cuánto tiempo van a estar los usuarios en el sistema?
  * El tiempo es dependiendo de la consulta o gestión que vayan a realizar.

#### - Diagnosticable

* ¿Los logs se encuentran centralizados en algún sistema?
  * Los logs se deben centralizar en el servicio de Application Insights y el Componente de Auditoria.
* ¿Qué herramienta se implementará para el monitoreo de la aplicación y la infraestructura?
  * Se debe utilizar los lineamientos de la compañía, en este caso con "Application Insights".
* ¿Cómo se deben manejar las notificaciones cuando se presente algún error del sistema o no esté funcionando la solución?
  * El sistema tendrá establecidos dichas notificaciones de error según la situación que se esté presentando, generando un texto claro del error y las opciones de solución (como línea de TI, catálogo o buzón establecido).
* ¿Se posee algún mecanismo para saber el estado de la aplicación y el sistema?
  * Se debe utilizar los lineamientos de la compañía en este caso con "Application Insights".

#### - Seguridad

* ¿Cómo se maneja la autenticación y autorización de la aplicación?
  * Se dispondrá de un usuario interno en el que la contraseña debe ser actualizada dado un tiempo determinado por el equipo de seguridad y el acceso al sistema solo será de manera interna mediante permisos por VPN.
* ¿La aplicación deberá manejar perfiles con diferentes niveles de autorización?
  * Sí, un rol administrador y consultor.
* ¿El sistema debe tener algún proceso de auditoría?
  * Sí aplica.
* ¿Qué tipo de información se va a consultar?
  * Consulta individual y masiva de cédulas de identificación.

#### - Rendimiento

* ¿Cuál debe de ser el tiempo de respuesta medio de los servicios de la aplicación?
  * Dependiendo del tamaño de la consulta que puede tardar entre 5 a 10 segundos.
* ¿Tiempo de carga medio de la aplicación?
  * Sin caché 20 segundos y con caché 10 segundos.
* ¿En cuánto tiempo se espera una respuesta?
  * Dependiendo del tamaño de la consulta que puede tardar entre 1 a 10 segundos.

#### - Escalabilidad

* ¿Cuántos usuarios se tiene actualmente?
  * Inicialmente, se contemplan dos usuarios de consulta y uno administrador.
* ¿Cuántos usuarios esperan atender a mediano y largo plazo?
  * Tener una capacidad para atender hasta más de 1000 usuarios.
* ¿Cómo se maneja el estado de la aplicación?
  * Mediante el equipo encargado en EPM, se activarán las notificaciones de Application Insights al grupo de Registraduría que se asigne.
* ¿El sistema posee caché distribuida?
  * No aplica.

#### - Disponibilidad

* ¿La aplicación se usa 24/7 o tiene horario muerto?
  * Aún no se define con el cliente.
* ¿Cuáles son las horas pico de uso del sistema?
  * No se tiene contempladas horas pico.
* ¿El sistema será de uso local o internacional?
  * Será de uso local.
* ¿En qué momentos los usuarios van a acceder a la aplicación?
  * En cualquier momento.

#### - Usabilidad

* ¿Se tiene definido algún proceso de identidad corporativa?
  * No aplica para esta aplicación.
* ¿La aplicación deberá escalar gráficamente a diferentes dispositivos?
  * No aplica
* ¿Se debe tener conexión a internet para usar la aplicación?
  * Si
* ¿En qué dispositivos debe correr?
  * Es un API. No depende de un entorno de ejecución.
* ¿Cuál es la versión del sistema operativo de estos dispositivos?
  * No aplica.
* ¿Si es web en qué navegadores debe correr?
  * No aplica.
* ¿Qué tipo de usuario va a usar la aplicación? (roles, jerarquía)
  * Administradores: Son los usuarios que disponen de acceso a todas las consultas de la aplicación y adicional serán los que cuentan con los permisos necesarios para cambiar el usuario de consulta de la Registraduría cuando sea notificado.
  * Consultores: Son los usuarios que pueden generar las consultas individuales y masivas de cédula de identificación.

#### - Accesibilidad

* ¿La aplicación debe posicionarse en navegadores?
  * No
* ¿La aplicación será usada por personas con capacidades diferentes?
  * No.

#### - Interoperabilidad

* ¿Con qué sistemas externos hay comunicación y cuál es la calidad y estándares de estos?
  * Registraduría: Es la plataforma externas donde serán generadas las consultas de cédula de identidad. Esta integración se realiza mediante un servicio WSDL expuesto con acceso controlado por IP.
* ¿Estos sistemas externos tienen algún grado de obsolescencia tecnológica?
  * Se debe validar con los dueños de la aplicación.

#### - Mantenibilidad

* ¿Qué tanto puede cambiar la aplicación o evolucionar?
  * Dependiendo de las necesidades de las aplicaciones cliente, No se tienen contempladas evoluciones cercanas.
* Normas que debe cumplir. (Resoluciones, NTC, Leyes)
  * Se debe cumplir con la norma NT5854.

#### - Lista de Chequeo Línea Base.
[Descargar](../../recursos/documents/ListaChequeoLineaBaseAni.xlsx)

#### - Lista de Chequeo Prácticas Modernas.
[Descargar](../../recursos/documents/ListaChequeoPracticasModernasAni.xlsx)

#### - Lista de Chequeo Seguridad.
[Descargar](../../recursos/documents/ListaChequeoSeguridadAni.xlsx)
