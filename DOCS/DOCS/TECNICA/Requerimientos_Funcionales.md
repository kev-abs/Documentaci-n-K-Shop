📝 ESPECIFICACIÓN DE REQUERIMIENTOS DE SOFTWARE
KSHOP – Sistema de Tienda Virtual

Estándar: IEEE 830-1998
Versión: 1.0
Fecha: 13 de febrero de 2026
Cliente: KSHOP Tienda de Ropa

## 1. INTRODUCCIÓN
## 1.1 Propósito

El propósito de este documento es describir de manera detallada los requerimientos funcionales y no funcionales del sistema KSHOP, una tienda virtual de ropa.

Este documento servirá como base formal para el desarrollo, pruebas, validación y aceptación del sistema.

## 1.2 Alcance

El sistema KSHOP permitirá:

Registro e inicio de sesión de clientes

Compra de productos en línea

Gestión de inventario

Administración de pedidos

Generación de reportes

Gestión de cupones y promociones

El sistema NO incluye:

Integración con pasarelas de pago reales (en esta fase académica)

Aplicación móvil nativa

Integración con sistemas contables externos

## 1.3 Definiciones

Cliente: Usuario que realiza compras en la plataforma.

Administrador: Usuario con permisos para gestionar el sistema.

Pedido: Orden generada tras una compra.

Inventario: Cantidad disponible de productos.

Cupón: Código promocional con descuento.

## 1.4 Referencias

Estándar IEEE 830-1998 – Software Requirements Specification

Ley 1581 de 2012 – Protección de Datos Personales (Colombia)

Buenas prácticas de desarrollo web

## 2. DESCRIPCIÓN GENERAL
## 2.1 Perspectiva del Producto

KSHOP es una aplicación web desarrollada con tecnologías estándar (HTML, CSS, Bootstrap, PHP y MySQL/SQL Server).

Funciona bajo arquitectura cliente-servidor y permite interacción en tiempo real entre usuarios y base de datos.

## 2.2 Funciones Principales

El sistema incluye:

* Gestión de usuarios

* Catálogo de productos

* Carrito de compras

* Proceso de pago

* Gestión de pedidos

* Control de inventario

* Generación de reportes

* Administración de cupones

## 2.3 Características de Usuarios
Cliente:

* Navega por el catálogo

* Agrega productos al carrito

* Realiza compras

* Consulta historial

Administrador:

* Gestiona productos

* Controla inventario

* Administra pedidos

* Genera reportes

* Gestiona promociones

## 2.4 Restricciones

* Debe desarrollarse como aplicación web.

* Debe utilizar base de datos relacional.

* Debe cumplir con la Ley 1581 de Protección de Datos.

* Tiempo estimado de desarrollo académico: 8 semanas.

## 3.Requerimientos Funcionales

--RF-001: Iniciar Sesión

Prioridad: Alta

Descripción: Permitir a los clientes y administradores autenticarse en el sistema mediante correo electrónico y contraseña.

Criterios de aceptación:

Validar que el usuario esté registrado.

Verificar contraseña correcta.

Mostrar mensaje de error si los datos son incorrectos.

Redirigir al panel correspondiente según el rol (cliente o administrador).

Registrar sesión activa.

--RF-002: Perfil de Cliente

Prioridad: Alta

Descripción: Permitir al cliente visualizar y actualizar su información personal.

Criterios de aceptación:

Mostrar datos personales registrados.

Permitir edición de nombre, teléfono y dirección.

Validar campos obligatorios.

Guardar cambios correctamente en la base de datos.

--RF-003: Cerrar Sesión

Prioridad: Alta

Descripción: Permitir al usuario cerrar sesión de manera segura.

Criterios de aceptación:

Destruir la sesión activa.

Redirigir a la página principal.

Impedir acceso a páginas privadas después del cierre.

--RF-004: Compra como Invitado

Prioridad: Media

Descripción: Permitir realizar compras sin necesidad de registrarse.

Criterios de aceptación:

Solicitar datos básicos (nombre, correo, dirección).

Permitir completar el proceso de pago.

Registrar pedido como “cliente invitado”.

--RF-005: Historial de Compras del Cliente

Prioridad: Alta

Descripción: Permitir al cliente consultar sus compras anteriores.

Criterios de aceptación:

Mostrar listado de pedidos realizados.

Visualizar fecha, total y estado.

Permitir ver detalle del pedido.

--RF-006: Creación de Listas de Deseos Personalizadas

Prioridad: Media

Descripción: Permitir al cliente guardar productos en una lista de deseos.

Criterios de aceptación:

Agregar productos a la lista.

Eliminar productos de la lista.

Mantener lista asociada al usuario.

--RF-007: Panel de Administración

Prioridad: Alta

Descripción: Permitir acceso exclusivo al administrador para gestionar el sistema.

Criterios de aceptación:

Acceso restringido por rol.

Visualizar módulos de productos, pedidos, clientes, reportes e inventario.

Interfaz diferenciada del cliente.

--RF-008: Reporte de Clientes Frecuentes

Prioridad: Media

Descripción: Generar un reporte de los clientes con mayor número de compras.

Criterios de aceptación:

Calcular cantidad total de pedidos por cliente.

Ordenar de mayor a menor.

Mostrar total de compras realizadas.

--RF-009: Catálogo de Productos en Línea

Prioridad: Alta

Descripción: Mostrar todos los productos disponibles para la venta.

Criterios de aceptación:

Mostrar imagen, nombre, precio y disponibilidad.

Permitir acceso al detalle del producto.

Actualizar automáticamente según inventario.

--RF-010: Filtro de Búsqueda Avanzada

Prioridad: Alta

Descripción: Permitir filtrar productos por categoría, precio y disponibilidad.

Criterios de aceptación:

Filtro por rango de precio.

Filtro por categoría.

Filtro por disponibilidad.

Mostrar resultados en tiempo real.

--RF-011: Registro de Productos

Prioridad: Alta

Descripción: Permitir al administrador agregar nuevos productos.

Criterios de aceptación:

Formulario con validaciones.

Subida de imagen.

Guardar en base de datos.

--RF-012: Actualización de Productos

Prioridad: Alta

Descripción: Permitir editar información de productos existentes.

Criterios de aceptación:

Modificar precio, descripción, stock.

Guardar cambios correctamente.

--RF-013: Validación de Disponibilidad

Prioridad: Alta

Descripción: Verificar que exista stock antes de permitir una compra.

Criterios de aceptación:

Bloquear compra si stock es 0.

Mostrar mensaje de producto agotado.

Actualizar stock tras cada compra.

--RF-014: Recomendaciones Personalizadas

Prioridad: Media

Descripción: Mostrar productos sugeridos según historial del cliente.

Criterios de aceptación:

Analizar compras anteriores.

Mostrar sección “Productos recomendados”.

Actualizar sugerencias dinámicamente.

--RF-015: Reseñas y Calificaciones de Productos

Prioridad: Media

Descripción: Permitir a los clientes dejar opiniones y calificaciones.

Criterios de aceptación:

Calificación de 1 a 5 estrellas.

Campo de comentario.

Mostrar promedio de calificaciones.

--RF-016: Carrito de Compras

Prioridad: Alta

Descripción: Permitir agregar, eliminar y modificar productos antes del pago.

Criterios de aceptación:

Agregar productos.

Modificar cantidades.

Calcular subtotal y total automáticamente.

--RF-017: Proceso de Pago en Línea

Prioridad: Alta

Descripción: Permitir realizar pagos electrónicos de manera segura.

Criterios de aceptación:

Selección de método de pago.

Confirmación antes de procesar pago.

Registro del pedido tras pago exitoso.

--RF-018: Gestión de Pedidos

Prioridad: Alta

Descripción: Permitir al administrador gestionar pedidos realizados.

Criterios de aceptación:

Cambiar estado del pedido.

Visualizar detalle del pedido.

Filtrar pedidos por estado.

--RF-019: Estado de Envío del Producto

Prioridad: Media

Descripción: Permitir al cliente consultar el estado del envío.

Criterios de aceptación:

Mostrar estado actual (pendiente, enviado, entregado).

Actualizar estado automáticamente.

--RF-020: Generación de Comprobante de Pago

Prioridad: Alta

Descripción: Generar comprobante digital de cada compra realizada.

Criterios de aceptación:

Incluir datos del cliente.

Detalle de productos.

Total pagado.

Permitir descarga en PDF.

--RF-021: Gestionar Devoluciones

Prioridad: Media

Descripción: Permitir al cliente solicitar devoluciones.

Criterios de aceptación:

Solicitud dentro de plazo permitido.

Validación por administrador.

Actualizar estado del pedido.

--RF-022: Gestión de Inventario

Prioridad: Alta

Descripción: Controlar entradas y salidas de productos.

Criterios de aceptación:

Actualizar stock automáticamente.

Registrar cambios manuales.

Mostrar productos con bajo inventario.

--RF-023: Alertas Automáticas

Prioridad: Media

Descripción: Notificar cuando el inventario esté bajo.

Criterios de aceptación:

Detectar productos con stock mínimo.

Mostrar alerta en panel administrador.

--RF-024: Gestión de Cupones y Descuentos

Prioridad: Media

Descripción: Permitir crear y aplicar cupones promocionales.

Criterios de aceptación:

Crear cupón con porcentaje o valor fijo.

Definir fecha de vencimiento.

Validar cupón en proceso de pago.

--RF-025: Gestión de Informes y Estadísticas

Prioridad: Alta

Descripción: Generar estadísticas generales de ventas.

Criterios de aceptación:

Mostrar ventas totales.

Mostrar productos más vendidos.

Mostrar ingresos totales.

--RF-026: Exportación de Datos

Prioridad: Media

Descripción: Permitir exportar datos de ventas e inventario.

Criterios de aceptación:

Exportar en formato Excel o CSV.

Descargar archivo automáticamente.

--RF-027: Reportes por Rango de Fecha

Prioridad: Alta

Descripción: Generar reportes filtrados por fecha.

Criterios de aceptación:

Seleccionar fecha inicio y fin.

Mostrar resultados filtrados.

Calcular totales dentro del rango.

--RF-028: Reporte de Efectividad de Cupones

Prioridad: Media

Descripción: Mostrar estadísticas de uso de cupones y promociones.

Criterios de aceptación:

Cantidad de veces usado.

Total de descuento aplicado.

Impacto en ventas.