# 

# 🚀 Proyecto: BarberFlow - Entregable 1

## 1. Ficha del Equipo (Info Semana 1)

*Esta sección formaliza la constitución del grupo de trabajo.*

| Nombre del Estudiante | Rol Principal | GitHub User |
| --- | --- | --- |
| Juan Pérez | Backend & DB | @juanp_dev |
| María González | Frontend & UI | @mariadev_ui |
| Carlos Ruiz | Fullstack / Lead | @carlos_coder |

---

## 2. Definición del Negocio

### 🏢 La Empresa (Cliente)

- **Nombre:** Barba Negra Grooming Lounge (Empresa Ficticia basada en procesos reales).
- **Sector:** Servicios de Estética y Cuidado Personal Masculino.

### ⚠️ El Problema

Actualmente, "Barba Negra" gestiona sus citas a través de WhatsApp y un cuaderno físico. Esto genera tres problemas graves:

1. **Cruce de turnos:** A veces dos clientes llegan a la misma hora porque el barbero olvidó anotar la cita.
2. **Pérdida de ingresos:** No hay un control real de cuánto dinero entra en efectivo al día (cuadre de caja manual y propenso a errores).
3. **Cálculo de Comisiones:** Los viernes se pierde mucho tiempo calculando cuánto le toca a cada barbero (40% comisión) manualmente.

### 💡 La Solución Propuesta

Desarrollar **"BarberFlow"**, una aplicación web responsiva que permita a los clientes autogestionar sus citas y a los administradores registrar los cobros (Caja) y calcular automáticamente las comisiones de los barberos al final de la semana.

---

## 3. Alcance del Proyecto (Scope)

### ✅ Dentro del Alcance (MVP - Producto Mínimo Viable)

*Funcionalidades críticas que estarán listas para la semana 11.*

1. **Módulo de Citas Público:** El cliente selecciona barbero, servicio y hora disponible.
2. **Agenda del Barbero:** Vista de calendario donde el barbero ve sus turnos del día.
3. **Punto de Venta (POS) Básico:** Registro de servicio completado y método de pago (Efectivo/Transferencia).
4. **Cierre de Caja:** Reporte simple de ingresos diarios y cálculo automático de comisiones por barbero.

### 🚫 Fuera del Alcance

*Cosas que NO haremos en este curso por falta de tiempo.*

1. **Pagos en Línea:** No integraremos pasarela de pagos (Stripe/Azul), el pago se registra manual en el local.
2. **Control de Inventario:** No se controlará el stock de productos (gel, cera, etc.).
3. **App Móvil Nativa:** Será una web app adaptable (PWA), no una app de PlayStore.
4. **Notificaciones SMS:** Solo usaremos correos electrónicos para confirmaciones (por costos).

---

## 4. Stack Tecnológico

- **Lenguaje:** JavaScript / TypeScript
- **Frontend:** React.js + Tailwind CSS (Para diseño rápido responsive).
- **Backend:** Node.js con Express.
- **Base de Datos:** PostgreSQL (Relacional, ideal para manejar integridad de citas).
- **Herramientas Extra:** Vercel (para deploy), GitHub Projects (para gestión de tareas).

---

## 5. Requerimientos

### ⚙️ Requerimientos Funcionales (RF)

| ID | Título | Descripción Breve | Prioridad |
| --- | --- | --- | --- |
| RF-01 | Gestión de Servicios | Admin puede crear servicios (ej: "Corte Clásico") y asignar precio y duración. | Media |
| RF-02 | Reserva de Turno | Cliente selecciona fecha/hora y el sistema valida que no se solape con otra cita. | Alta (Crítico) |
| RF-03 | Registro de Cobro | Admin marca una cita como "Finalizada" y registra el pago. | Alta |
| RF-04 | Reporte de Comisiones | El sistema genera una tabla con el total a pagar a cada barbero según sus servicios realizados. | Alta |

### 🛡️ Requerimientos No Funcionales (RNF)

1. **Mobile First:** El 90% de los clientes reservará desde el celular, la interfaz pública debe ser perfecta en móvil.
2. **Concurrencia:** El sistema debe bloquear un horario si dos personas intentan reservarlo al mismo milisegundo.
3. **Usabilidad:** El proceso de reserva no debe tomar más de 3 clics.
