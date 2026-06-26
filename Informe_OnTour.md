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

