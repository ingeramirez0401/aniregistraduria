---
title: Arquitectura de la Aplicación - Anexos
has_children: false
more-content: true
ordered: true
parent: ANI Registraduria 
toc: true
---

# Anexos.

<!-- 
A continuación documente la información correspondiente a los anexos relacionados con su propuesta arquitectónica
-->

[Regresar al principal](../../plantilla-arquitectura-aplicacion.html)

Las siguientes son las herramientas utilizadas por la solución:

- Visual Studio .Net [Licenciamiento IG]: Para la implementación del Backend.

- Draw.io [Licenciamiento Free]: Modelar los diseños de la arquitectura.

- Microsoft Office [Licenciamiento IG]:
MS. Excel para la generación de los resultados de salida.
Gestión de la documentación del proyecto.

- Microsoft SharePoint [Licenciamiento nube IG y EPM]: Para gestionar y centralizar la documentación del proyecto.

Las siguientes son las tecnologías utilizadas por la solución:

<ul style="text-align: justify">
    <li>Azure DevOps [Licenciamiento EPM e IG]:
        <ul>
            <li>Gestión de las Historias de Usuario</li>
            <li>Back-Log del marco de trabajo Scrum.</li>
            <li>Gestión de Bugs.</li>
            <li>Control de versión del código.</li>
            <li>Pipeline para:
                <ul>
                    <li>Compilación (Builds)</li>
                    <li>Despliegue (Release)</li>
                </ul>
            </li>
            <li>Librerías para el manejo de variables delicadas.</li>
            <li>Plan de pruebas:
                <ul>
                    <li>Casos de pruebas.</li>
                </ul>
            </li>
            <li>Azure Portal [licenciamiento nube de IG y EPM]:
                <ul>
                    <li>Gestionar los servicios:
                        <ul>
                            <li>Key Vault</li>
                            <li>Application Insights</li>
                            <li>Active Directory</li>
                            <li>Api Management</li>
                            <li>Resource Group</li>
                        </ul>
                    </li>
                </ul>
            </li>
        </ul>
    </li>
    <li>Browser
        <ul>
            <li>Chrome</li>
            <li>Firefox</li>
        </ul>
    </li>
    <li>.NET 5: Generar el Back-End de la aplicación.</li>
</ul>

### Anexo 02: Documentos relacionados

[Visygas.drawio](../../recursos/documents/reg.drawio)

[ListaChequeoLineaBaseVisygas.xlsx](../../recursos/documents/ListaChequeoLineaBaseAni.xlsx)

[ListaChequeoPracticasModernasVisygas.xlsx](../../recursos/documents/ListaChequeoPracticasModernasAni.xlsx)

[ListaChequeoSeguridadVisygas.xlsx](../../recursos/documents/ListaChequeoSeguridadAni.xlsx)

### Anexo 03: Vocabulario

- No Aplica.

### Anexo 04: Referencias de apoyo

- <a href="https://aplicaciones.epm.com.co/interno/alejandriadocumentacion/pages/Experimentacion/Backend/Application%20Insights/AplicationInsights.html" target="_blank">Application Insights</a>

- <a href="https://aplicaciones.epm.com.co/interno/alejandriadocumentacion/pages/GuiasYLineamiento/Interoperabilidad/Monitoreo/Lineamientos/AgregarAI_ApiManagement.html" target="_blank">Prueba de Concepto Application Insights en Api Management</a>