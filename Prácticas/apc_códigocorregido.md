# Índice

1. [register.php](#register-php)
2. [insert_player.php](#)

# register.php

``` <!doctype html>
<html lang="es">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport"
              content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
        <meta http-equiv="X-UA-Compatible" content="ie=edge">
        <meta http-equiv="Content-Security-Policy" content="default-src 'self'; script-src 'self'; style-src 'self' 'unsafe-inline'; img-src 'self'">
        <link rel="stylesheet" href="css/style.css">
        <title>Práctica RA3 - Players list</title>
    </head>
    <body>
        <header>
            <h1>Register</h1>
        </header>
        <main class="player">
            <form action="register.php" method="post">
                <input type="hidden" name="csrf_token" value="token_csrf_generado_servidor">
                <label>Username:</label>
                <input type="text" name="username" required>
                <label>Password:</label>
                <input type="password" name="password" required minlength="8">
                <input type="submit" value="Send">
            </form>
            <form action="logout.php" method="post">
                <input type="submit" name="Logout" value="Logout" class="logout">
            </form>
            <a href="list_players.php">Back to list</a>
        </main>
        <footer class="listado">
            <img src="images/logo-iesra-cadiz-color-blanco.png" alt="Logo IESRA">
            <h4>Puesta en producción segura</h4>
            <p>Please <a href="http://www.donate.co?amount=100&amp;destination=ACMEScouting/">donate</a></p>
        </footer>
    </body>
</html>
 ```

# insert_player.php

``` <!doctype html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport"
          content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="css/style.css">
    <title>Práctica RA3 - Authentication page</title>
    <meta http-equiv="Content-Security-Policy" content="default-src 'self'; img-src 'self'; script-src 'self'; style-src 'self' 'unsafe-inline';">
</head>
<body>
<header class="auth">
    <h1>Authentication page</h1>
</header>
<main class="auth">
    <div class="message">
        This page requires you to be logged in.<br>
    </div>
    <section>
        <div>
            <h2>Login</h2>
            <form action="login.php" method="post">
                <label>User</label>
                <input type="text" name="username" required>
                <label>Password</label>
                <input type="password" name="password" required>
                <input type="submit" value="Login">
            </form>
        </div>

        <div>
            <h2>Logout</h2>
            <form action="logout.php" method="post">
                <input type="submit" name="Logout" value="Logout">
            </form>
        </div>
    </section>
</main>
<footer>
    <h4>Puesta en producción segura</h4>
    <p>Please <a href="http://www.donate.co?amount=100&destination=ACMEScouting/">donate</a></p>
</footer>
</body>
</html>
 ```



