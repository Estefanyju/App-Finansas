# App Finansas

**Estudiante:** Shirley *(completa tu nombre completo aquí)*

## Descripción

Aplicación nativa Android para el registro de finanzas personales. Permite al usuario registrar ingresos y gastos diarios, visualizarlos en una lista dinámica con RecyclerView, editar registros existentes y eliminarlos. Los datos se almacenan de forma persistente en SQLite.

## Funcionalidades

- **Listar transacciones** con RecyclerView y adaptador personalizado (ViewHolder).
- **Crear** nuevas transacciones (concepto, monto, tipo).
- **Editar** transacciones existentes al tocar un ítem de la lista.
- **Eliminar** transacciones desde el formulario de edición.
- **Resumen financiero** con totales de ingresos, gastos y balance.
- **Persistencia** con SQLite (CRUD completo).

## Estructura del proyecto

```
app/src/main/java/com/example/appfinansas/
├── MainActivity.java              # Pantalla principal con RecyclerView
├── TransaccionFormActivity.java   # Formulario crear/editar
├── adapter/
│   └── TransaccionAdapter.java    # Adaptador con ViewHolder
├── database/
│   └── DatabaseHelper.java        # SQLite CRUD
└── model/
    └── Transaccion.java           # Modelo de datos
```

## Base de datos

Tabla `transacciones`:

| Campo    | Tipo    | Descripción                          |
|----------|---------|--------------------------------------|
| id       | INTEGER | Primary Key, autoincremental         |
| concepto | TEXT    | Descripción breve del movimiento     |
| monto    | REAL    | Valor de la transacción              |
| tipo     | INTEGER | 1 = Ingreso, 2 = Gasto               |

## Capturas de pantalla

> Agrega tus capturas en la carpeta `docs/screenshots/` y reemplaza las rutas de abajo.

### Lista de transacciones
![Lista de transacciones](docs/screenshots/lista_transacciones.png)

### Formulario de registro
![Formulario de registro](docs/screenshots/formulario_transaccion.png)

## Requisitos

- Android Studio (Ladybug o superior recomendado)
- JDK 11+
- minSdk 24

## Cómo ejecutar

1. Clona el repositorio.
2. Abre el proyecto en Android Studio.
3. Sincroniza Gradle.
4. Ejecuta la app en un emulador o dispositivo físico.

## Tecnologías

- Java
- SQLite (SQLiteOpenHelper)
- RecyclerView
- Material Design Components
