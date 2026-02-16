<h1 align="center">Login MVC en PHP</h1>

Este proyecto implementa un sistema básico de inicio de sesión en PHP siguiendo el patrón MVC (Modelo – Vista – Controlador).

-El usuario introduce sus credenciales en un formulario y se valida contra la base de datos.

-Si el login es correcto, se redirige al listado interno.

-Gu

<h3>Funcionalidades</h3>

-Inicio de sesión con usuario y contraseña

-Control de acceso mediante sesión

-Redirección al interior si el usuario está autenticado

-Logout para cerrar sesión

<h3 align="center">Estructura del proyecto</h3>

config/Database.php → conexión con MySQL usando PDO

controllers/AuthController.php → controlador de autenticación

models/User.php → modelo Usuario (consulta en BD)

views/login.php → vista del formulario de login

index.php → enrutador principal

<h3>Configuración</h3>

-

<img width="1463" height="650" alt="image" src="https://github.com/user-attachments/assets/69e2d6fb-14de-4afc-a5f5-57c200c4199d" />


<h3>Vista (Login)</h3>

-Archivo principal: views/login.php

-Contiene el formulario HTML con estilos y validación.

<img width="512" height="827" alt="image" src="https://github.com/user-attachments/assets/8dfe719c-0285-4f8a-aa55-2d4d04e3c715" />


<h3>Controlador</h3>

-Archivo: controllers/AuthController.php

-Se encarga de mostrar la vista y autenticar.

-Los usuarios y contraseñas añadidos deben seguir un patrón de validación, en este caso, al crearlo el usuario debe tener entre 3 y 20 caracteres alfanuméricos y la contraseña a partir de 9, teniendo que contar con letras en mayúsculas, minúsculas, números y caracteres especiales.

<img width="1176" height="851" alt="image" src="https://github.com/user-attachments/assets/250e1651-8c3c-40ca-bf97-5e72012a6379" />

<h3>Modelo</h3>

Archivo: models/User.php

Realiza la consulta a la base de datos.

<img width="941" height="882" alt="image" src="https://github.com/user-attachments/assets/5e090105-60c1-42d9-96af-173c85e5ff4f" />

<h3>Ejecución</h3>

En XAMPP comenzar Apache y SQL.

Abrir en el navegador:

http://localhost/login-mvc/
