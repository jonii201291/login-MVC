<h1 align="center">Login MVC en PHP</h1>

Este proyecto implementa un sistema básico de inicio de sesión en PHP siguiendo el patrón MVC (Modelo – Vista – Controlador).

El usuario introduce sus credenciales en un formulario y se valida contra la base de datos.

Si el login es correcto, se redirige al listado interno.

<b>Funcionalidades</b>

Inicio de sesión con usuario y contraseña

Control de acceso mediante sesión

Redirección al interior si el usuario está autenticado

Logout para cerrar sesión

Estructura del proyecto

config/Database.php → conexión con MySQL usando PDO

controllers/AuthController.php → controlador de autenticación

models/User.php → modelo Usuario (consulta en BD)

views/login.php → vista del formulario de login

index.php → enrutador principal

Vista (Login)

Archivo principal: views/login.php

Contiene el formulario HTML con estilos y validación.

<form action="index.php?action=authenticate" method="POST">
    <input type="text" name="idusuario" required>
    <input type="password" name="password" required>
    <button type="submit">Ingresar</button>
</form>


Controlador

Archivo: controllers/AuthController.php

Se encarga de mostrar la vista y autenticar.

if ($this->userModel->login($username, $password)) {
    $_SESSION['idusuario'] = $username;
    header("Location: index.php?action=index");
}


Modelo

Archivo: models/User.php

Realiza la consulta a la base de datos.

$query = "SELECT * FROM usuario WHERE idusuario = ? AND password = ?";


Ejecución

Colocar el proyecto en htdocs (XAMPP)

Abrir en el navegador:

http://localhost/login-mvc/
