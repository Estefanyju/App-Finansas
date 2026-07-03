# App Finansas

**Estudiante:** Estefany Julieth Sanchez Rojas*

## Descripción

Aplicación nativa Android para el registro de finanzas personales. Permite al usuario registrar ingresos y gastos diarios, visualizarlos en una lista dinámica con RecyclerView, editar registros existentes y eliminarlos. Los datos se almacenan de forma persistente en SQLite.

## Prueba de funcionalidad

<img width="420" height="755" alt="image" src="https://github.com/user-attachments/assets/34fa58b8-b091-42e1-a690-aa2f55e43b0f" />
<img width="451" height="805" alt="image" src="https://github.com/user-attachments/assets/d3963b94-0c02-4573-b9f8-e4c9ca78902f" />
<img width="447" height="810" alt="image" src="https://github.com/user-attachments/assets/294d8c0e-9769-4bf8-884c-928467d8d500" />
<img width="450" height="795" alt="image" src="https://github.com/user-attachments/assets/8711d018-f9ae-41a2-b4bb-9463a76e75cd" />
<img width="456" height="792" alt="image" src="https://github.com/user-attachments/assets/b74c039c-a92d-4550-82a3-0ed6c4341f43" />
<img width="447" height="792" alt="image" src="https://github.com/user-attachments/assets/a75aaf3b-eeb1-430e-8740-9cfdaa1b9be7" />
<img width="442" height="782" alt="image" src="https://github.com/user-attachments/assets/ee51631a-9c9b-4590-8ea7-54a59cfe34f1" />







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
