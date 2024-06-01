<h3 align="center"> Crea un form de login animado con html, css y javascript!!!</h3>
<p>Segui los pasos y vas a llegar al resultado. No olvides que tambien podes forkearte o descargar el proyecto y modificarlo a tu gusto. Aca te dejo el codigo: </p>

<h4>Codigo HTML</h4>

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <link rel="stylesheet" type="text/css" href="styles.css">
    <link href="https://fonts.googleapis.com/css?family=Poppins:600&display=swap" rel="stylesheet">
    <script src="https://kit.fontawesome.com/a81368914c.js"></script>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Animated Login Form</title>
</head>

<body>
    <div class="container">
        <div class="login-content">
            <form action="index.html">
                <img src="./logoAvatar.png" alt="avatar">
                <h2>
                    Bienvenid<span class="span">@</span>s
                </h2>
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
                <a href="#">Olvidaste tu Contraseña</a>
                <input type="submit" class="btn" value="Iniciar sesión">
            </form>
        </div>
    </div>


    <script src="main.js"></script>
</body>
</html>
```

<h4>Codigo CSS</h4>

```css
*{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

body{
    font-family: 'poppins', sans-serif;
    overflow: hidden;
    background-image: linear-gradient(to bottom right,
    #000000, #8904a4);
}

.container{
    margin: 0 auto;
    width: 100vh;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.login-content{
    display: flex;
    width: 75%;
    justify-content: flex-start;
    align-items: center;
    text-align: center;
}

form{
    margin: 0 auto;
    width: 360px;
}

.login-content img{
    height: 100px;
    animation: moverOpacificar 2s linear forwards;
}

.login-content h2{
    margin: 15px 0;
    color: #d0c6c6;
    font-size: 2.9rem;
    animation: moverOpacificar 2s linear forwards;
}

.span{
    background-image: linear-gradient(to right,
    #f09433, #e6683c, #dc2743, #cc2366,
    #bc1888, #a818a8, #9228d8, #7a3dd8,
    #6d4edc);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
}

.login-content .div-form{
    position: relative;
    display: grid;
    grid-template-columns: 7% 93%;
    margin: 25px 0;
    padding: 5px 0;
    border-bottom: 2px solid #d9d9d9;
}

.login-content .div-form .user{
    margin-top: 0;
}

.i{
    color: #d9d9d9;
    display: flex;
    justify-content: center;
    align-items: center;
}

.i i{
    transition: .3s;
}

.div-form > div{
    position: relative;
    height: 45px;
}

.div-form > .div > h5{
    position: absolute;
    left: 10px;
    top: 50%;
    transform: translateY(-50%);
    color: #999;
    font-size: 18px;
    transition: .3s;
}

.div-form:before, .div-form:after{
    content: "";
    position: absolute;
    bottom: -2px;
    width: 0%;
    height: 2px;
    background-color: #0c86c8;
    transition: .4s;
}

.div-form:before{
    right: 50%;
}

.div-form:after{
    left: 50%;
}

.div-form.focus:before, .div-form.div-form.focus:after{
    width: 50%;
}

.div-form.focus > div> h5{
    top: -5px;
    font-size: 15px;
}

.div-form.focus > .i > i{
    color: #0c86c8;
}

.div-form > div > input{
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    border: none;
    outline: none;
    background: none;
    padding: 0.5rem 0.7rem;
    font-size: 1.2rem;
    color: #fff;
    font-family: 'poppins', sans-serif;
}

.div-form .password{
    margin-bottom: 4px;
}

a{
    display: block;
    text-decoration: none;
    text-align: right;
    color: #999;
    font-size: 0.9rem;
    transition: .3s;
}

a:hover{
    color: #53aad9;
}

.btn{
    display: block;
    width: 100%;
    height: 50px;
    border-radius: 25px;
    outline: none;
    border: none;
    background-image: linear-gradient(to right, 
    black ,#0c86c8, black);
    background-size: 200%;
    font-size: 1.2rem;
    color: #fff;
    font-family: 'poppins', sans-serif;
    text-transform: uppercase;
    margin: 1rem 0;
    cursor: pointer;
    transition: .5s;
}

.btn:hover{
    background-position: right;
}

@keyframes moverOpacificar{
    0%{
        left: 0;
        opacity: 0;
        transform: translateY(-100%);
    }
    50%{
        left: 50%;
        opacity: 0.5;
    }
    100%{
        left: 100%;
        opacity: 1;
    }
}
```

<h4>Codigo JavaScript</h4>

```javascript
const inputs = document.querySelectorAll(".input");

function addClass() {
  let parent = this.parentNode.parentNode;
  parent.classList.add("focus");
}

function removeClass() {
  let parent = this.parentNode.parentNode;
  if (this.value == "") {
    parent.classList.remove("focus");
  }
}

inputs.forEach((input) => {
  input.addEventListener("focus", addClass);
  input.addEventListener("blur", removeClass);
});

```

<h3>Si seguiste todos los pasos este deberia ser el resultado</h3>

https://github.com/jonadeveloper/TutoformLoginLogout/assets/59519580/adfcec88-71b1-4067-99a4-c1f130c1c2f2


