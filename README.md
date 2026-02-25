# U1 - Proyecto integrador de formulario
Este proyecto es una aplicación realizada con **Flet (Python)** que implementa un formulario con validaciones avanzadas y diferentes controles de entrada.Este proyecto consiste en el desarrollo de una aplicación interactiva construida con Flet, un framework de Python que permite crear interfaces gráficas modernas y multiplataforma.
El objetivo principal del proyecto es implementar un formulario completo de registro con validaciones avanzadas, controles diversos y una presentación visual clara y fácil de usar.

La aplicación está diseñada para recopilar información básica de un usuario, validar los datos ingresados y mostrar los resultados de forma organizada dentro de una ventana modal.
Además, se incorporan notificaciones visuales para indicar al usuario cuando la información ha sido enviada correctamente o cuando existe algún error en los campos.

Uno de los aspectos más importantes del proyecto es la implementación de validaciones en tiempo real, las cuales verifican que los campos no estén vacíos, que el formato del correo electrónico sea correcto y que todos los elementos requeridos hayan sido seleccionados.
El botón de envío se habilita o deshabilita dinámicamente dependiendo de si las validaciones se cumplen, brindando retroalimentación inmediata al usuario.

Cuando el usuario presiona el botón Enviar, el programa realiza una validación final y, si todo está correcto, muestra una notificación tipo SnackBar indicando que el envío fue exitoso.
Al mismo tiempo, los datos se guardan y se agregan en una sección interna de registros, que posteriormente se muestran dentro de un AlertDialog (ventana modal).
Este cuadro modal presenta los datos recopilados en un diseño limpio y organizado, permitiendo al usuario revisar la información de manera clara.
Adicionalmente, el formulario se limpia automáticamente después del envío para permitir nuevos registros.

El proyecto no solo demuestra la implementación técnica del formulario, sino también el manejo interactivo de ventanas, validaciones, componentes visuales y almacenamiento rápido dentro de la interfaz.
De esta manera, se convierte en un ejemplo completo de cómo utilizar Flet para crear aplicaciones modernas que combinan funcionalidad, diseño y experiencia de usuario.

Además, la aplicación está configurada para ejecutarse tanto en modo escritorio como directamente dentro del navegador web, lo que demuestra la versatilidad de Flet y facilita la portabilidad del proyecto para presentaciones o entornos educativos.

En resumen, este proyecto integra múltiples elementos tecnológicos para crear una aplicación eficiente, dinámica y visualmente atractiva, cumpliendo con los requisitos esenciales de un formulario profesional con validaciones, modales y controles interactivos, ideal para fines académicos o como base para sistemas más complejos en el futuro.

---
### El objetivo es mostrar el uso de: 

✔ Validación de entradas vacías

✔ Validación de formato de email

✔ Control Dropdown

✔ Control Radio Button

✔ Ventana modal (AlertDialog) para mostrar datos enviados

✔ SnackBars para notificaciones

✔ Filtros de texto (solo números)

### El formulario solicita al usuario ingresar:
- Nombre
- Número de control (solo números)
- Correo electrónico (se valida formato con regex)
- Carrera (Dropdown)
- Semestre (Dropdown)
- Género (Radio buttons)
- 
## 1. Instalar Flet dentro del entorno virtual

Con el entorno activado, escribe:
`
pip install flet
`
Para verificar que se instaló:
`
pip list
`
Debe aparecer:
`
flet   X.X.X`
# Crear un entorno virtual (Windows, Linux o Mac)

Un entorno virtual sirve para aislar las dependencias del proyecto.

Windows
# ✔ Paso 1: Abrir la terminal

Puedes usar:

PowerShell

CMD

Terminal de VS Code (recomendado)

# ✔ Paso 2: Crear entorno virtual

Escribe:

`python -m venv venv`

Esto crea una carpeta llamada venv/.

# ✔ Paso 3: Activar el entorno virtual

En PowerShell:

`venv\Scripts\Activate`

En CMD:

`venv\Scripts\activate.bat`

Verás algo así en la terminal:

`(venv) C:\ruta-del-proyecto>`

Eso significa que el entorno ya está activo.

## Linux / MacOS

### Paso 1: Crear entorno virtual
`python3 -m venv venv`
### Paso 2: Activarlo
`source venv/bin/activate`

La terminal mostrará:

`(venv) user@pc:~/proyecto$`

### 3. Crear tu archivo principal (main.py)

Ejemplo:
`
import flet as ft
def main(page: ft.Page):
    page.add(ft.Text("Hola Flet desde navegador!"))
ft.app(target=main, view=ft.WEB_BROWSER)`

### 4. Ejecutar la aplicación Flet

Con el entorno virtual activado, escribe:
`
python main.py
`
Si usas Linux/Mac:
`
python3 main.py`
### 5. Opciones para ejecutar Flet
A) Ejecutar en navegador web

Este es el que quieres:

`ft.app(target=main, view=ft.WEB_BROWSER)`

La aplicación se abrirá automáticamente en tu navegador
Corre como una página web
Muy útil para presentaciones o proyectos escolares

B) Ejecutar como app de escritorio

Si deseas una ventana estilo aplicación:
`
ft.app(target=main)
`
Esto abre la app con el runtime de Flet, similar a una aplicación de escritorio.

### 6. Desactivar el entorno virtual (cuando termines)

En cualquier sistema operativo:
`
deactivate
`
Tu terminal volverá al estado normal.
---
## En general 

<img width="599" height="307" alt="{B0D95E24-B121-4135-AB53-ACB5A9C2B3CC}" src="https://github.com/user-attachments/assets/dbf5e562-0afc-484f-9108-dc1538a29657" />

### El formulario solicita al usuario ingresar:
- Nombre
- Número de control (solo números)
- Correo electrónico (se valida formato con regex)
- Carrera (Dropdown)
- Semestre (Dropdown)
- Género (Radio buttons)

  
  ### Cuando el usuario presiona Enviar:
- Se valida que todos los campos estén completos.
- Se valida el formato correcto del email.

  <img width="396" height="447" alt="image" src="https://github.com/user-attachments/assets/60f10bef-8197-4400-806d-77cae370f5bc" />

  ### Si todo es correcto:
- Se muestra un SnackBar verde indicando éxito.
- Se agregan los datos a una lista interna del sistema.
- Se muestra un AlertDialog con los datos registrados.

<img width="1260" height="680" alt="image" src="https://github.com/user-attachments/assets/6b356612-d252-4a2d-83f1-97727a7976a5" />

  ### Si existe un error:
- Se muestra un SnackBar rojo indicando la falla.

# Validaciones Incluidas
### No permite enviar campos vacíos

<img width="456" height="672" alt="image" src="https://github.com/user-attachments/assets/c0d0b253-aebd-407c-8d5c-e90fe925e9ba" />

Se verifica que cada campo tenga texto antes de enviar.

### El email se valida usando una expresión regular

`re.match(r"^[^@\s]+@[^@\s]+\.[^@\s]+$", txt_email.value)`

### Número de control acepta solo números`

Gracias a:

`keyboard_type=ft.KeyboardType.NUMBER
input_filter=ft.NumbersOnlyInputFilter()`

### Dropdown para seleccionar carrera y semestre
### RadioGroup para seleccionar el género

## Muestra de datos enviados en una ventana modal

Se utiliza un AlertDialog que contiene un ListView con los registros guardados.

# Importaciones principales
`import re
import flet as ft
`

`re`

Es un módulo de Python que permite trabajar con expresiones regulares, usado para validar el formato del email.

`flet`

Es el framework usado para crear aplicaciones gráficas con Python.

Configuración inicial de la página
`page.title = "Registro - Formulario"
page.padding = 30
page.bgcolor = "#FDFBE3"`

Define título, padding y color de fondo.

## Campos del formulario

Campo de texto: Nombre
`txt_nombre = ft.TextField(label="Nombre", border_color="#4D2A32")`

Campo de Número de Control — Solo números
`keyboard_type=ft.KeyboardType.NUMBER
input_filter=ft.NumbersOnlyInputFilter()`

Esto obliga a escribir únicamente números en el campo.

## Validación del Email
`re.match(r"^[^@\s]+@[^@\s]+\.[^@\s]+$", txt_email.value or "")`

La expresión regular verifica:
- Parte antes del @
- Parte después del @
- Un punto seguido de dominio
- Sin espacios

## ▼ Dropdowns
### Semestre
Genera automáticamente opciones del 1 al 6:

`options=[ft.dropdown.Option(str(i)) for i in range(1, 7)]`
### Carrera
Opciones estáticas.

## Género — RadioGroup
`genero_group = ft.RadioGroup(
    content=ft.Row([
        ft.Radio(value="Masculino", ...),
        ft.Radio(value="Femenino", ...)
    ])
)`

## Vista de datos guardados
`datos_guardados = ft.ListView(...)`

Aquí se agregan los registros ya enviados.

## Ventana Modal (AlertDialog)
`dialog_datos = ft.AlertDialog(...)`

Sirve para mostrar los datos guardados al usuario al final.

## Función de validación en tiempo real
`def validar_todo(e=None):`

Cambia el color del botón Enviar según si los datos están completos:
- Verde: listo para enviar
- Gris: incompleto o email inválido

## Función guardar

Es la más importante:
- Valida los campos uno por uno
- Muestra un SnackBar verde si todo es correcto
- Agrega el registro al ListView
- Abre la ventana modal
- Limpia los campos
Si hay error, muestra un SnackBar rojo.

## Botón Guardar
`btn_guardar = ft.Button(
    content=ft.Text("Enviar"),
    bgcolor="grey",
    on_click=guardar
)`

## Estructura visual final en la pantalla
`page.add(ft.Column([...]))`
---
# Ejecución final
`ft.run(main)`
---
# Codigo completo
```
import re 
import flet as ft

def main(page: ft.Page):
    page.title = "Registro - Formulario"
    page.padding = 30
    page.bgcolor = "#FDFBE3"

    # Campos del formulario 
    txt_nombre = ft.TextField(
        label="Nombre",
        border_color="#4D2A32"
    )

    # SOLO NÚMEROS
    txt_control = ft.TextField(
        label="Numero de Control",
        border_color="#4D2A32",
        keyboard_type=ft.KeyboardType.NUMBER,#cambia el teclado para que solo muestre números
        input_filter=ft.NumbersOnlyInputFilter()  # Solo números, es el que se ingrese solo numeros
    )

    txt_email = ft.TextField(
        label="Email",
        border_color="#4D2A32"
    )

    dd_semestre = ft.Dropdown(#son las listas despegables que se pueden seleccionar
        label="Semestre",
        border_color="#4D2A32",
        options=[ft.dropdown.Option(str(i)) for i in range(1, 7)]
    )

    dd_carrera = ft.Dropdown(
        label="Carrera",
        border_color="#4D2A32",
        options=[
            ft.dropdown.Option("Ingenieria en Sistemas Computacionales"),
            ft.dropdown.Option("Ingenieria Civil"),
            ft.dropdown.Option("Ingenieria Industrial"),
            ft.dropdown.Option("Contador"),
            ft.dropdown.Option("Electronica"),
        ]
    )

    # Género - Radio Buttons
    genero_group = ft.RadioGroup(
        content=ft.Row([
            ft.Radio(value="Masculino", label="Masculino", active_color="#4D2A32"),
            ft.Radio(value="Femenino", label="Femenino", active_color="#4D2A32")
        ], spacing=20)
    )

    # -------- SECCION DE DATOS GUARDADOS --------
    datos_guardados = ft.ListView(# crea la lista donde se van a mostrar los datos guardados
        expand=True,
        spacing=10,
        padding=10
    )

    titulo_datos = ft.Text("Datos Guardados", size=20, weight=ft.FontWeight.BOLD, color="#4D2A32")

    # Diálogo para mostrar datos guardados
    dialog_datos = ft.AlertDialog(
        title=ft.Text("Datos Guardados"),
        content=ft.Container(
            content=datos_guardados,
            width=600,
            height=400
        ),
        actions=[
            ft.TextButton("Cerrar", on_click=lambda e: cerrar_dialog(e))
        ]
    )

    def cerrar_dialog(e):
        dialog_datos.open = False
        page.update()

# -------- FUNCION PARA VALIDAR TODO --------
    def validar_todo(e=None):
        if (
            txt_nombre.value
            and txt_control.value
            and re.match(r"^[^@\s]+@[^@\s]+\.[^@\s]+$", txt_email.value or "") 
            and dd_carrera.value
            and dd_semestre.value
            and genero_group.value
        ):
            btn_guardar.bgcolor = "green"
        else:
            btn_guardar.bgcolor = "grey"

        page.update()

    # Asignar on_change después de que todo está inicializado
    txt_nombre.on_change = validar_todo
    txt_control.on_change = validar_todo
    txt_email.on_change = validar_todo
    dd_semestre.on_change = validar_todo
    dd_carrera.on_change = validar_todo
    genero_group.on_change = validar_todo

# -------- DIALOGO --------
    def guardar(e):
        # Validar todos los campos manualmente
        email_valido = txt_email.value and "@" in txt_email.value and "." in txt_email.value
        
        if (
            txt_nombre.value and txt_nombre.value.strip()
            and txt_control.value and txt_control.value.strip()
            and email_valido
            and dd_carrera.value
            and dd_semestre.value
            and genero_group.value
        ):
            snack = ft.SnackBar(# se encarga de mostrar la barra verde que dice la indicacion
                ft.Text("Envio exitoso - Se han guardado los datos correctamente"),
                bgcolor="green"
            )
            page.overlay.append(snack)
            snack.open = True 
            
            # Agregar datos a la sección de datos guardados
            registro = ft.Container(
                content=ft.Column([
                    ft.Text(f"Nombre: {txt_nombre.value}", size=12, weight=ft.FontWeight.BOLD),
                    ft.Text(f"Control: {txt_control.value}", size=12),
                    ft.Text(f"Email: {txt_email.value}", size=12),
                    ft.Text(f"Carrera: {dd_carrera.value}", size=12),
                    ft.Text(f"Semestre: {dd_semestre.value}", size=12),
                    ft.Text(f"Género: {genero_group.value}", size=12),
                ], spacing=5),
                padding=10,
                bgcolor="#E8D5C4",
                border_radius=10,
                border=ft.Border.all(1, "#4D2A32")
            )
            datos_guardados.controls.append(registro)
            
            # Abrir el diálogo para mostrar los datos guardados
            dialog_datos.open = True
            page.overlay.append(dialog_datos)
            
            # Limpiar todos los campos
            txt_nombre.value = ""
            txt_control.value = ""
            txt_email.value = ""
            dd_carrera.value = None
            dd_semestre.value = None
            genero_group.value = None
            btn_guardar.bgcolor = "grey"
            
            page.update()
        else:
            snack = ft.SnackBar(
                ft.Text("Error - Por favor completa todos los campos correctamente"),
                bgcolor="red"
            )
            page.overlay.append(snack)
            snack.open = True
            page.update()
        
    btn_guardar = ft.Button(#boton  de guardar
        content=ft.Text("Enviar", color="black"),
        bgcolor="grey",
        expand=True,
        on_click=guardar,
    )

    page.add(
        ft.Column(
            [
                ft.Text("Formulario de Registro", size=24, weight=ft.FontWeight.BOLD, color="#4D2A32"),
                txt_nombre,
                txt_control,
                txt_email,
                ft.Row([
                    ft.Column([dd_carrera], expand=True),
                    ft.Column([dd_semestre], expand=True)
                ], spacing=10),
                ft.Row([
                    ft.Text("Género:", size=14),
                    genero_group
                ], spacing=10, vertical_alignment=ft.CrossAxisAlignment.CENTER),
                btn_guardar
            ],
            spacing=15,
            expand=False,
            width=400
        )
    )


ft.run(main)
```
---
# Para ejecutar el programa 
## Ejecutar Flet en modo ESCRITORIO

Este es el modo predeterminado.

En la terminal:

`python main.py`

Se abrirá una ventana independiente como aplicación.

## Ejecutar Flet en un NAVEGADOR WEB

Para esto debes modificar la última línea del programa.

Cambia:

`ft.app(target=main)`

Por:

`ft.app(target=main, view=ft.WEB_BROWSER)`

Ahora ejecuta:

`python main.py`
---
# Ejecucion mostrada

<img width="396" height="447" alt="image" src="https://github.com/user-attachments/assets/4c2b80c4-cbeb-4f20-8fbd-a2e7d26f20c6" />

<img width="1260" height="680" alt="image" src="https://github.com/user-attachments/assets/3d0c8fab-6eb7-4c75-a520-5d1e7443d309" />


