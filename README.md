# Sistema de Gestión Académica del Colegio

**Categoría:** Misional — *Formación Académica* 

**Versión de Python:** 3.13.9  

## Problema / Necesidad
En muchos colegios, los docentes y directivos aún registran las calificaciones de manera manual o en hojas de cálculo, lo que puede generar errores, pérdida de información o dificultad para calcular promedios y hacer seguimiento académico a los estudiantes.

Por esta razón, se propone crear un sistema académico que facilite el **registro de estudiantes, notas y el cálculo de promedios**, para apoyar la labor educativa y administrativa de la institución.



## Solución Propuesta
El sistema desarrollado es una **aplicación de consola** que permite gestionar los procesos académicos de forma organizada.  
Cuenta con distintos **roles de usuario**:
- **Rector:** supervisa el sistema general.  
- **Coordinador:** gestiona el registro de estudiantes.  
- **Profesor:** ingresa las notas y calcula promedios.
- **Estudiante:** ver notas y dtos.



##  Arquitectura del Proyecto
```
colegio-sistema/
├─ src/
│  ├─ main.py                     # Punto de entrada con menú o CLI
│  ├─ core/
│  │  ├─ auth.py                  # Login / autenticación (roles)
│  │  ├─ menu.py                  # Menú principal dinámico según el rol
│  │  └─ utils.py                 # Validaciones, IDs, logs, etc.
│  ├─ roles/
│  │  ├─ rector.py                # Funciones del rector
│  │  ├─ coordinador.py           # Funciones del coordinador
│  │  ├─ profesor.py              # Funciones del profesor
│  │  └─ estudiante.py            # Funciones del estudiante
│  ├─ modules/
│  │  ├─ models.py                # Clases: Usuario, Solicitud, Nota, etc.
│  │  ├─ data_manager.py          # Guardar/cargar datos (JSON)
│  │  ├─ reportes.py              # Generación de CSV de resultados
│  │  └─ notificaciones.py        # Mensajes automáticos / recordatorios
│  └─ data/
│     ├─ usuarios.json            # Base de datos simulada
│     ├─ solicitudes.json         # Casos o peticiones
│     ├─ profesores.json          # Profesores
|     ├─ notas.json               # Guarda notas
|     ├─ estudiantes.json         # Estudiantes
|     ├─ comunicados.json         # Mensaje, fecha
|     ├─ avisos.json              # Aviso
│     └─ reportes/
│        └─ reporte_general.csv   # Salidas generadas
├─ tests/                         # (opcional) pruebas simples
├─ requirements.txt
├─ README.md
└─ .gitignore

```


## Manual de Usuario
**Requisitos previos**
- Tener Python 3.11.2 o superior instalado.
- (Opcional) Crear y activar un entorno virtual:
  
  python -m venv venv
  venv\Scripts\activate
  
**Instalación**
- Descargar o clonar el proyecto desde GitHub.
- (Opcional) Instalar las librerías necesarias:
  
  pip install -r requirements.txt

**Ejecución**
- python -m src.main
- python src/main.py



## Temas de Python aplicados
- Funciones y modularización
- Estructuras de datos (listas, diccionarios)
- Manejo de archivos JSON
- Importación de módulos
- Condicionales y bucles
- Programación por roles y permisos



## Trabajo Colaborativo
**Integrantes:**

- Samuel Castro — *Rol:* 
### Coordinador
1. **Registrar estudiante**  
   Permite agregar un estudiante con `nombre` y `grado`.

2. **Asignar profesor**  
   Permite agregar un profesor con `nombre` y `materia`.

3. **Ver listados**  
   Muestra todos los estudiantes y profesores registrados.

4. **Eliminar estudiante / profesor**  
   Permite eliminar un estudiante o profesor mediante su `ID`.

5. **Actualizar estudiante / profesor**  
   Permite actualizar el nombre y grado de un estudiante o la información de un profesor.

6. **Enviar aviso al rector**  
   Envía un aviso que quedará registrado en `avisos.json`.

7. **Ver avisos enviados**  
   Permite revisar todos los avisos enviados al rector.

8. **Generar reporte CSV**  
   Genera un archivo `reporte_general.csv` con todos los estudiantes y profesores.

9. **Cerrar sesión**



- Saira Aragon — *Rol:*
### Rector

1. **Ver avisos de coordinadores**  
   Permite revisar todos los avisos enviados por los coordinadores.

2. **Ver listados de estudiantes y profesores**  
   Permite visualizar los datos registrados.

3. **Generar reporte CSV**  
   Genera un archivo `reporte_general.csv` con los datos de estudiantes y profesores.

4. **Enviar comunicado general**  
   Permite crear un comunicado dirigido a toda la institución (guardado en `comunicados.json`).

5. **Ver comunicados**  
   Permite visualizar todos los comunicados enviados por el rector.

6. **Actualizar comunicado**  
   Permite modificar el asunto o el mensaje de un comunicado existente.

7. **Cerrar sesión**
- Karen Gonzales — *Rol:* Estudiante (ver el registro de sus notas y datos)
- Angelica Garcia — *Rol:* Profesor (registro de notas y cálculo de promedios)

**Repositorio**
- https://github.com/samuelcastr/colegio.git



## Límites y mejoras futuras
- Implementar autenticación segura (encriptar contraseñas).
- Agregar reportes automáticos (PDF).
- Integrar una interfaz gráfica o versión web.
- Permitir filtrar promedios por materia o grado.

## Ejemplos de uso

  

