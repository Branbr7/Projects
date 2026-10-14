# BMC Health · Supply Chain

Primera propuesta interactiva. Abrir `index.html` en un navegador; no requiere instalación. Incluye navegación entre los cuatro módulos y un formulario provisional de compras que descarga un borrador JSON. No implementa autenticación, persistencia, carga de archivos ni envío de correo.

## Referencias revisadas

- Supply Chain existente: interfaz HTML/CSS/JavaScript, servidor Node.js, proxy IIS hacia localhost:5187, almacenamiento central en JSON y recepción de identidad mediante cabeceras en modo entra-proxy. La documentación incluida describe una versión anterior; debe comprobarse la configuración desplegada y la confianza en las cabeceras antes de reutilizar la autenticación.
- Vacaciones v3.6: su documentación describe React y Node.js 24+, autenticación Microsoft 365 con callback propio además de preautenticación Application Proxy, adjuntos fuera de la carpeta pública y notificaciones Microsoft 365. Propone limitar el envío al buzón mediante Exchange Application RBAC. Estos mecanismos son referencia para implementar, no evidencia de configuración validada en el nuevo portal.
- Laboratorio: pestañas Formulario y Reunion; captura de requisitos y resumen para decisiones.
- PO tracking: campos de Xero y seguimiento de entrega/finanzas. La importación debe preservar campos manuales, evitar duplicados y conservar cortes semanales.

## Acceso a formularios de SharePoint

Para cada lista, proporcionar capturas del formulario completo, incluidos desplegables, campos obligatorios y condiciones; exportación de estructura o listado de columnas con tipo y opciones; y un ejemplo ficticio o anonimizado. Una exportación Excel por sí sola no describe validaciones ni opciones completas.

Si se revisa con una sesión autorizada, hacerlo desde el navegador del usuario con su cuenta corporativa y acceso de lectura. No compartir contraseñas, cookies ni tokens. Este entorno cloud no tiene una sesión autenticada de SharePoint.

## Implementación prevista

1. Validar campos de compras con SharePoint; implementar solicitudes, adjuntos, estados, PO, entregas y cierre.
2. Incorporar logística siguiendo su formulario actual.
3. Implementar PO tracking / Incoming y carga Xero con histórico semanal.
4. Implementar laboratorio con captura y reunión.

Configurar aplicación Entra ID y Application Proxy, autorización por solicitante/responsable/administrador en el servidor, y notificaciones mediante Microsoft 365. Definir tenant, grupos, shared mailbox, permisos de envío, almacenamiento y servidor de despliegue. No reutilizar secretos ni datos productivos de los archivos de referencia.

Esta propuesta no cambia las instalaciones actuales. Los RAR, respaldos, datos de empleados e inventario no se publican en el repositorio.
