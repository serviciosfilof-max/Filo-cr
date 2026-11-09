FILO GESTIÓN

Documento maestro de relevamiento y reconstrucción técnica

Versión 1.0 — 9 de noviembre de 2026

1. Objetivo del proyecto

Construir una plataforma propia para empresas constructoras y de mantenimiento, independiente de Base44, con propiedad del código fuente y posibilidad de comercialización mediante suscripciones.

Objetivos:

- Aplicación web y Android.
- Multiempresa.
- Información independiente y protegida por empresa.
- Administración centralizada de suscripciones.
- Escalabilidad comercial.

2. Módulo Gastos

Formulario: Nuevo gasto

Campos:

- Fecha.
- Categoría:
  - Materiales.
  - Mano de obra.
  - Jornales.
  - Herramientas.
  - Transporte.
  - Alquiler de equipos.
  - Combustible.
  - Seguros.
  - Subcontratistas.
  - Otros.
- Obra o gasto general.
- Materiales o detalles.
- Cantidad.
- Unidad de medida.
- Agregar renglón.
- Total gastado.
- Proveedor.
- Estado de pago: pagado / pendiente.
- Medio de pago: efectivo / transferencia / cheque / otros.
- Comprobante: remito / factura / ticket.
- Descripción.
- Notas.

Acciones:

- Cancelar.
- Guardar gasto.

3. Módulo Contabilidad y Finanzas

3.1 Registrar cobro

Campos:

- Importe recibido.
- Fecha de cobro.
- Tipo: adelanto / cobro parcial / saldo final.
- Medio de pago: efectivo / transferencia / cheque / otros.
- Obra: selector de todas las obras registradas.
- Quién pagó.
- Concepto.
- Comprobante opcional.
- Archivo o fotografía del comprobante.
- Observaciones.

Acción: Guardar cobro o cancelar.

3.2 Balance financiero

Filtros de período:

- Mes anterior.
- Últimos 90 días.
- Este año.
- Todo.

Filtro por obra:

- Todas las obras.
- Una obra específica.

Al seleccionar una obra, mostrar su balance individual. Al seleccionar todas, mostrar el balance general de Construcciones Filo.

3.3 Indicadores financieros

- Presupuesto contratado.
- Dinero efectivamente cobrado.
- Adelantos recibidos.
- Saldo pendiente de cobro.
- Gastos totales.
- Pagos pendientes.
- Flujo de caja del período.
- Dinero disponible en caja.
- Resultado estimado.
- Resultado real.
- Acumulado.

3.4 Informes y gráficos

- Gastos por rubro.
- Rentabilidad por obra.
- Obras con importes pendientes de cobro.
- Acceso a ver obra.
- Historial de ingresos.
- Descarga de informes CSV.
- Descarga de informes PDF.

4. Configuración de la empresa

4.1 Datos de la empresa

- Nombre comercial.
- CUIT.
- Razón social.
- Propietario de la cuenta.
- Correo electrónico.
- Dirección comercial.
- Teléfono.
- Rubro.
- Subir logo para documentación comercial.

4.2 Control de asistencia

- Horario inicial.
- Tolerancia de llegada en minutos.
- Solicitar ubicación al marcar.
- Exigencia de permisos.
- Solicitar fotografías.
- Verificación de asistencia.
- Autorización del trabajador.

Acción: Guardar cambios.

4.3 Invitaciones

- Generar código de invitación.
- Copiar código.
- Compartir código con trabajadores.

4.4 Plan y suscripción

Plan actual:

- Básico.
- Hasta 5 trabajadores.

Información:

- Estado de acceso.
- Inicio de prueba.
- Fecha de inicio.
- Próxima renovación.

Funciones incluidas:

- Obras.
- Equipos.
- Asistencia QR.
- Partes diarios.
- Gastos.
- Contabilidad.

La contratación, los cambios de plan y las renovaciones son gestionados por FILO GESTIÓN. El estado se actualiza cuando el pago queda confirmado.

5. Panel de administración de FILO GESTIÓN

Este panel es independiente del panel operativo de cada empresa.

No debe permitir acceder a las obras ni a los datos comerciales de las empresas clientes.

5.1 Indicadores generales

- Cantidad de empresas.
- Actividades.
- Empresas en prueba.
- Membresías.
- Integrantes por empresa.
- Facturación mensual.
- Suscripciones sin acceso o bloqueadas.

5.2 Empresas y suscripciones

Información por empresa:

- Nombre.
- Correo electrónico.
- Cantidad de integrantes.
- Servicio o rubro.
- Plan contratado.
- Estado de suscripción.
- Nivel de acceso.
- Próxima renovación.
- Estado de la cuenta.

5.3 Planes comerciales observados

- Básico: $15.000.
- Profesional: $35.000.
- Empresarial: $70.000.

Estos valores son los observados durante el relevamiento y deben ser configurables.

5.4 Estados de suscripción

- En prueba.
- Activa.
- Vencida.
- Suspendida.
- Cancelada.

5.5 Niveles de acceso

- Acceso completo.
- Acceso limitado.
- Sin acceso.

5.6 Estado de cuenta

- Activa.
- Suspendida.
- Baja.

Se observó la leyenda «Cargar manualmente», pero no se confirmó que sea un botón o una función operativa.

6. Arquitectura técnica propuesta

Objetivo: independencia tecnológica y propiedad del código.

- Frontend: Flutter / FlutterFlow.
- Backend: Supabase.
- Base de datos: PostgreSQL.
- Autenticación: Supabase Auth.
- Archivos: almacenamiento privado.
- Código fuente: GitHub privado.
- Aplicaciones: web y Android.

La arquitectura debe contemplar aislamiento de datos por empresa, roles de usuario, permisos y seguridad.

7. Reglas fundamentales

1. Cada empresa tiene sus propios trabajadores, obras, clientes y movimientos.
2. Los gastos y cobros deben estar vinculados a la empresa correspondiente.
3. Cada obra debe tener su balance financiero individual.
4. Los indicadores generales deben consolidar todas las obras.
5. Los planes deben controlar la cantidad de trabajadores permitidos.
6. Los estados de suscripción deben actualizarse mediante confirmación de pago.
7. El administrador general gestiona las suscripciones sin acceder a información comercial de los clientes.
8. Los comprobantes deben poder adjuntarse y consultarse.
9. Los informes deben poder exportarse.
10. El sistema debe estar preparado para sumar nuevas empresas sin mezclar información.

8. Próximas etapas

Etapa 1 — Relevamiento

- Completar el inventario de módulos.
- Identificar pantallas y formularios.
- Documentar las reglas de negocio.

Etapa 2 — Migración

- Revisar el proyecto actual de Base44.
- Inspeccionar el repositorio GitHub.
- Identificar componentes reutilizables.
- Recuperar y migrar los datos.

Etapa 3 — Desarrollo

- Crear backend propio.
- Configurar base de datos multiempresa.
- Reconstruir frontend.
- Implementar permisos y suscripciones.

Etapa 4 — Pruebas

- Validar gastos y cobros.
- Validar balances.
- Probar aislamiento entre empresas.
- Probar planes y vencimientos.

Etapa 5 — Comercialización

- Publicar versión web.
- Preparar aplicación Android.
- Implementar contratación y pagos.
- Lanzar planes comerciales.

---

OBJETIVO FINAL: FILO GESTIÓN debe convertirse en un producto tecnológico propio, comercializable y escalable, cuyo código y arquitectura podamos controlar sin depender de Base44.

Estado del documento: Primera versión del relevamiento. Pendiente de contrastar con el proyecto y el código existente.
