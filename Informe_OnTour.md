1- ANÁLISIS DEL PROBLEMA


 Actores: Apoderados
 Problemas: Falta de transparencia y acceso a la información. No tienen copias del contrato de la gira, desconocen los abonos realizados, su saldo por pagar y el detalle de los seguros. Deben agendar reuniones o enviar correos para poder informarse.
 Solución(es) o Funcionalidad(es): Desarrollo de un "Dashboard Apoderado" (portal de autoservicio) que permita visualizar el estado de cuenta en tiempo real (meta, aportes y saldo), descargar documentos en PDF (contrato y póliza de seguro) y recibir notificaciones automáticas por cada depósito realizado.

 Actores: Ejecutivo de Ventas
 Problemas: Procesos manuales e ineficientes. Pierden mucho tiempo respondiendo consultas individuales de los apoderados (por correo o reuniones) y deben enviar de forma manual los comprobantes de depósito cuando se realizan actividades comunes para juntar fondos.
 Solución(es) o Funcionalidad(es): Módulo de gestión centralizada que permita registrar contratos, asignar seguros y subir documentos digitales. Además, un sistema de notificaciones que envíe correos automáticamente a los apoderados y representantes cuando se registre un pago, eliminando el trabajo manual.













2- Diseño de Prototipo


Navegación del sistema

Flujo Principal: Perfil Apoderado
 Pantalla 1 (Inicio de Sesión) ➔ El usuario ingresa RUT y Contraseña de apoderado El sistema lo redirige a la Pantalla 2 (Dashboard Apoderado) Ruta Financiera: Clic en botón "Ver detalle de aportes" ➔ Pantalla 3 (Historial de Depósitos) Ruta Documental: Clic en menú "Mis Documentos" ➔ Navega hacia la Pantalla 4 (Descarga de Contrato) y/o la Pantalla 5 (Descarga de Póliza). 




Flujo Secundario: Perfil Ejecutivo de Ventas
 Pantalla 1 (Inicio de Sesión) ➔ El usuario ingresa credenciales de ejecutivo ➔ El sistema lo redirige directamente a la Pantalla 6 (Administración de Contratos). Desde esta pantalla: Puede seleccionar un colegio/curso para subir sus documentos y asignar seguros, alimentando de información al Dashboard de los apoderados.



 Flujo Terciario: Perfil Dueño de la Agencia 
Pantalla 1 (Inicio de Sesión) ➔ El usuario ingresa credenciales de administrador/dueño ➔ El sistema lo redirige a la Pantalla 7 (Reporte de Avance). Desde esta pantalla: Visualiza los gráficos consolidados de todos los contratos activos a nivel general. 




Justificación de la Solución 

Claridad del diseño: Se utilizó una interfaz minimalista, con un uso adecuado de espacios en blanco (whitespace) y tipografías legibles. La información financiera en el Dashboard (Meta, Saldos) se presenta en tarjetas destacadas, lo que reduce la carga cognitiva del usuario y permite entender el estado de cuenta en un solo vistazo.

Navegación: Se implementó un ruteo intuitivo basado en la "regla de los 3 clics". El usuario (Apoderado, Ejecutivo o Dueño) puede acceder a cualquier funcionalidad crítica, como descargar un contrato o ver el historial, de forma directa desde el menú lateral o desde accesos rápidos en la pantalla principal, evitando perderse en la plataforma.

Cobertura de funcionalidades: El prototipo abarca el 100% de los requerimientos solicitados en el caso "OnTour". Se incluye el inicio de sesión centralizado, el Dashboard para el apoderado (con sus 4 métricas exigidas), la vista de historial de depósitos, los módulos de descarga de documentos (Contrato y Póliza), y las herramientas de gestión para los ejecutivos y el dueño.

Aplicación de buenas prácticas de diseño: Se aplicaron principios de Diseño Centrado en el Usuario (UX/UI) y Jerarquía Visual. Los elementos más importantes (como el Saldo Pendiente o el Porcentaje de Avance) tienen mayor peso visual. Además, se mantuvo consistencia en los colores (basados en la identidad de "OnTour"), la iconografía y la ubicación de los botones de llamada a la acción (como "Descargar PDF"), lo que genera confianza y transparencia en los apoderados.













3 - Aplicación de Calidad (ISO 25010) 



Usabilidad: Navegación intuitiva y visual: Se centraliza toda la información en un "Dashboard" limpio. El uso de gráficos circulares (porcentaje de avance) y tarjetas grandes para los saldos permite que apoderados de cualquier edad entiendan su estado de cuenta en un solo vistazo. 

Fiabilidad Información automatizada y trazable: El saldo no es ingresado a mano, sino que es calculado matemáticamente por el sistema en base a los comprobantes validados del "Historial de Depósitos", eliminando el margen de error humano del ejecutivo. 

Seguridad Control de Acceso (Login obligatorio): Se implementa un sistema de autenticación mediante RUT y contraseña. Cada apoderado tiene permisos restringidos y solo puede visualizar la información financiera y descargar la póliza de su respectivo pupilo, protegiendo la privacidad de los datos. 

Eficiencia Accesos directos (Regla de los 3 clics): Se estructuró el flujo para que cualquier consulta crítica (ver saldo, ir al historial o descargar un PDF) esté disponible inmediatamente en la pantalla principal, reduciendo drásticamente el tiempo de navegación. 

Mantenibilidad Diseño Modular: La arquitectura de la interfaz separa claramente los módulos (Apoderado, Ejecutivo, Dueño). Esto permite que si a futuro la agencia OnTour quiere agregar, por ejemplo, un botón de "Pago Webpay", se pueda integrar en el Dashboard sin romper el resto del sistema. 


4- Historias de Usuarios y Criterios de Aceptación
(Actividad 4 y 5)


HU01: Visualización del Estado de Cuenta del Alumno
Como apoderado, 
Quiero consultar el reporte de estado de cuenta de mi pupilo,

Para visualizar los aportes efectuados y conocer con exactitud el saldo que falta por completar para lograr la meta económica.

Criterios de Aceptación:

CA01: El sistema debe mostrar el monto total de los abonos individuales efectuados por el apoderado hasta la fecha.

CA02: El sistema debe calcular y mostrar dinámicamente el saldo pendiente por pagar según el valor del paquete turístico.

CA03: El sistema debe reflejar el descuento o monto rebajado proporcionalmente gracias a las actividades de recaudación del fondo común del curso.

HU02: Consulta de Contrato y Descarga en PDF
Como apoderado,

Quiero acceder a la consulta digital del contrato de prestación de servicios de la gira de estudio,

Para revisar los servicios adicionales contratados (hotelería, museos) y descargar un respaldo legal en formato PDF.

Criterios de Aceptación:

CA01: El sistema debe desplegar el detalle completo de los servicios básicos y adicionales asociados al curso.

CA02: La interfaz debe proveer un botón funcional que permita generar y descargar el contrato en un archivo formato .pdf.

CA03: El documento PDF generado debe especificar el monto de la reserva pagada por el colegio y la meta económica total.

HU03: Notificaciones por Correo de Depósitos Individuales 
Como apoderado,
Quiero recibir una notificación automática en mi correo electrónico cada vez que se realice un abono,
Para tener la tranquilidad y el comprobante de que mi dinero fue registrado correctamente en la cuenta de mi hijo.

Criterios de Aceptación:

CA01: El sistema debe enviar un correo electrónico de confirmación de forma automática e inmediata tras registrar un depósito individual exitoso.

CA02: El cuerpo del correo debe indicar: nombre del alumno, monto depositado, fecha de la transacción y saldo restante.

CA03: El sistema debe adjuntar o generar un número de comprobante único por cada depósito notificado.

HU04: Control de Recaudación por Curso
Como ejecutivo de ventas de la agencia,

Quiero consultar los montos totales depositados por un curso determinado,

Para monitorear el cumplimiento financiero del contrato y gestionar cobranzas u orientaciones a los representantes.

Criterios de Aceptación:

CA01: El sistema debe permitir buscar e identificar al curso filtrando por institución educativa (colegio) y nivel.

CA02: El panel debe mostrar la sumatoria total consolidada de los depósitos individuales más los depósitos comunes del curso.
CA03: El sistema debe contrastar el monto recaudado frente a la meta fijada y expresar el avance como un porcentaje (%).

HU05: Descarga de Póliza de Seguro Colectivo
Como apoderado,

Quiero descargar la póliza de seguro de mi respectivo pupilo,

Para conocer el detalle de las coberturas médicas y de asistencia ante cualquier eventualidad durante el viaje.

Criterios de Aceptación:

CA01: El sistema debe generar internamente el documento individual vinculando los datos del pupilo al seguro colectivo negociado por la agencia.

CA02: El archivo debe quedar disponible de forma permanente para su visualización y descarga en formato PDF dentro del portal del apoderado.

CA03: El documento debe exhibir claramente el nombre de la empresa aseguradora externa y los datos de contacto en caso de siniestro.

6- Casos de prueba
ID Caso
Criterio de Aceptación Relacionado
Datos de Entrada
Resultado Esperado
Resultado Obtenido
Estado
CP01
HU01 - CA01 (Mostrar abonos)
Login apoderado con abonos registrados de $450.000.
El Dashboard despliega la cifra exacta de "$450.000" en la tarjeta de Saldo Acumulado
Conforme al diseño
Exitoso
CP02
HU01 - CA02 (Calcular saldo pendiente)
Paquete: $600.000. Abonos: $600.000.
La tarjeta de Saldo Pendiente muestra automáticamente un valor de "$0".

La tarjeta se descuadra y muestra un valor negativo (-$1).
Fallido
CP03
HU01 - CA03 (Descuento fondo común)
Aplicación de beneficio por rifa del curso: $50.000.
El sistema resta correctamente los $50.000 del total.
Conforme al diseño
Exitoso
CP04
HU02 - CA01 (Despliegue de servicios)
Clic en menú "Mis Documentos" -> Ver contrato.
Se despliega en pantalla la lista de hoteles, itinerarios de museos y transportes incluidos.
Conforme al diseño
Exitoso
CP05
HU02 - CA02 (Descarga PDF contrato)
Clic en el botón "Descargar PDF" en la sección de Contrato.
Se procesa y descarga localmente un archivo .pdf completamente legible y con estructura oficial.
El navegador bloquea la descarga y el archivo baja dañado (0 KB). 
Fallido
CP06
HU03 - CA01 (Envío automático correo)
Registro manual de transferencia bancaria por $50.000.
Envío automático de correo electrónico informativo al buzón registrado del apoderado en < 10 segundos.
Conforme al diseño
Exitoso
CP07
HU03 - CA02 (Cuerpo de notificación)
Recepción de correo de abono exitoso.
El correo contiene explícitamente: nombre completo del alumno, monto, fecha de transacción y saldo restante.
El correo llega con los datos financieros, pero falta el N° de comprobante único.
Fallido
CP08
HU04 - CA01 (Filtro por Curso)
Filtro de búsqueda en portal Ejecutivo: Colegio "A", Curso "4° Medio B".
El sistema limpia la grilla y muestra únicamente la información financiera del curso seleccionado.
Conforme al diseño
Exitoso
CP09
HU04 - CA03 (Porcentaje de avance)
Meta del curso: $20.000.000. Recaudado: $10.000.000.
El indicador visual del ejecutivo muestra exactamente un "50%" de avance financiero.
Conforme al diseño
Exitoso
CP10
HU05 - CA02 (Descarga de Póliza)
Clic en menú "Mis Documentos" -> "Descargar Póliza".
El sistema genera el documento PDF individualizado que detalla la aseguradora externa y teléfonos de emergencia.
Conforme al diseño
Exitoso


Actividad 7(es el 8 según el PDF): Registro de defectos

ID Defecto
Caso Relacionado
Descripción de la Falla
Severidad
Estado
DEF01
CP05
Al presionar "Descargar PDF" en navegadores móviles, la descarga se bloquea o el archivo se genera sin extensión legible.
Alta
Abierto
DEF02
CP02
Si el saldo pendiente llega a $0, la tarjeta del Dashboard muestra un valor negativo (-$1) por un error de redondeo de decimales.
Media
Corregido
DEF03
CP07
El correo de notificación automática omite incluir el número único de comprobante solicitado en los criterios.
Baja
Asignado



