# site-langues-groupe4
Projet PHP (DEV WEB) de site de langues - Groupe de 4

langue.php
<?php
session_start();
if (!isset($_SESSION['user_id'])) {
    header("Location: login.php");
    exit();
}

$langue = $_GET['langue'] ?? '';

$cours = [
    'francais' => ['Grammaire', 'Vocabulaire', 'Compréhension orale'],
    'anglais' => ['Grammar', 'Vocabulary', 'Listening'],
    'espagnol' => ['gramática', 'vocabulario', 'comprensión oral']
];

if (!array_key_exists($langue, $cours)) {
    header("Location: cours.php");
    exit();
}
?>

<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Cours de <?= htmlspecialchars($langue) ?></title>
    <link rel="stylesheet" href="main.css">
</head>
<body>
    <div class="container">
        <h1>Cours de <?= ucfirst($langue) ?></h1>
        <ul>
            <?php foreach ($cours[$langue] as $c): ?>
                <li><?= htmlspecialchars($c) ?></li>
            <?php endforeach; ?>
        </ul>
        <a href="cours.php">← Retour</a>
    </div>
</body>
</html>


cours.php
<?php
session_start();
if (!isset($_SESSION['user_id'])) {
    header("Location: login.php");
    exit();
}
?>

<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Choix des langues</title>
    <link rel="stylesheet" href="main.css">
</head>
<body>
    <div class="container">
        <h1>Bienvenue, <?php echo htmlspecialchars($_SESSION['user_nom']); ?> !</h1>
        <h2>Choisissez une langue :</h2>
        <div class="langues">
            <div class="langue">
                <a href="langue.php?langue=francais">
                    <img src="francais.jpg" alt="Français">
                    <p>Français</p>
                </a>
            </div>
            <div class="langue">
                <a href="langue.php?langue=anglais">
                    <img src="anglais.jpg" alt="Anglais">
                    <p>Anglais</p>
                </a>
            </div>
            <div class="langue">
                <a href="langue.php?langue=espagnol">
                    <img src="espagnol.jpg" alt="espagnol">
                    <p>Arabe</p>
                </a>
            </div>
        </div>
        <a class="button" href="logout.php">Se déconnecter</a>
    </div>
</body>
</html>
