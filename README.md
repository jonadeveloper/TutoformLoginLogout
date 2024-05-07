<h3 align="center"> Crea un form de login animado con html, css y javascript!!!</h3>
<p>Segui los pasos y vas a llegar al resultado. No olvides que tambien podes forkearte o descargar el proyecto y modificarlo a tu gusto. . Aca te dejo el codigo: </p>

```html
<!DOCTYPE html>
<html>

<head>
    <title>Animated Login Form</title>
    <link rel="stylesheet" type="text/css" href="styles.css">
    <link href="https://fonts.googleapis.com/css?family=Poppins:600&display=swap" rel="stylesheet">
    <script src="https://kit.fontawesome.com/a81368914c.js"></script>
    <meta name="viewport" content="width=device-width, initial-scale=1">
</head>

<body>
    <div class="container">
        <div class="login-content">
            <form action="index.html">
                <img src="img/logoAvatar.png">
                <h2 class="title">Bienvenid<span class="span">@</span>s</h2>
                <div class="div-form user">
                    <div class="i">
                        <i class="fas fa-user"></i>
                    </div>
                    <div class="div">
                        <h5>Nombre de usuario</h5>
                        <input type="text" class="input" required>
                    </div>
                </div>
                <div class="div-form password">
                    <div class="i">
                        <i class="fas fa-lock"></i>
                    </div>
                    <div class="div">
                        <h5>Contraseña</h5>
                        <input type="password" class="input" required>
                    </div>
                </div>
                <a href="#">¿Olvidaste tu contraseña?</a>
                <input type="submit" class="btn" value="Iniciar sesión">
            </form>
        </div>
    </div>
    <script type="text/javascript" src="main.js"></script>
</body>

</html>
```
