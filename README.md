# site-langues-groupe4
Projet PHP (DEV WEB) de site de langues - Groupe de 4
index.php
<?php
session_start();
?>

<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Accueil - Site de Langues</title>
    <link rel="stylesheet" href="main.css">
</head>
<body>

<div class="container">
    <h1>Bienvenue sur le site de langues !</h1>
    <p>Apprenez facilement l'anglais, le français, l'espagnol et plus encore.</p>

    <?php if (isset($_SESSION['user'])): ?>
        <p>Bonjour, <?php echo htmlspecialchars($_SESSION['user']); ?> !</p>
        <a href="cours.php" class="button">Voir les cours</a>
        <a href="logout.php" class="button">Se déconnecter</a>
    <?php else: ?>
        <a href="register.php" class="button">S'inscrire</a>
        <a href="login.php" class="button">Se connecter</a>
    <?php endif; ?>

    <h2>Langues disponibles</h2>
    <div class="langues">
        <div class="langue">
            <a href="cours.php?langue=francais">
                <img src="francais.jpg" alt="Français">
                <p>Français</p>
            </a>
        </div>
        <div class="langue">
            <a href="cours.php?langue=anglais">
                <img src="anglais.jpg" alt="Anglais">
                <p>Anglais</p>
            </a>
        </div>
        <div class="langue">
            <a href="cours.php?langue=espagnol">
                <img src="espagnol.jpg" alt="Espagnol">
                <p>Espagnol</p>
            </a>
        </div>
    </div>
</div>

</body>
</html>

dashboard.php
<?php
session_start();
if (!isset($_SESSION['email'])) {
    header("Location: login.php");
    exit();
}
?>

<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Tableau de bord</title>
    <link rel="stylesheet" href="main.css">
</head>
<body>
    <h1>Bienvenue, <?= $_SESSION['email'] ?> !</h1>
    <p>Vous êtes maintenant connecté.</p>
    <a href="logout.php">Déconnexion</a>
</body>
</html>
