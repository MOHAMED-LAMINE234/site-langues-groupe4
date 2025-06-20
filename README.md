# site-langues-groupe4
Projet PHP (DEV WEB) de site de langues - Groupe de 4

main.css
/* BASE RESET */
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* BODY */
body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background: #eef2f7;
  color: #2c3e50;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

/* CONTENEUR PRINCIPAL */
.container {
  max-width: 900px;
  margin: 40px auto;
  padding: 30px 25px;
  background: #ffffff;
  border-radius: 14px;
  box-shadow: 0 8px 20px rgba(44, 62, 80, 0.1);
}

/* TITRES */
h1, h2, h3 {
  font-weight: 700;
  margin-bottom: 18px;
  color: #34495e;
}

/* NAVIGATION */
nav {
  background: #34495e;
  padding: 18px 40px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  border-radius: 0 0 14px 14px;
  position: sticky;
  top: 0;
  z-index: 100;
}

nav .logo {
  color: #ecf0f1;
  font-weight: 800;
  font-size: 1.9rem;
  letter-spacing: 2px;
}

nav ul {
  list-style: none;
  display: flex;
  gap: 28px;
  align-items: center;
  padding-left: 0;
}

nav ul li a {
  color: #ecf0f1;
  font-weight: 600;
  font-size: 1.1rem;
  text-decoration: none;
  transition: color 0.3s ease;
}

nav ul li a:hover,
nav ul li a:focus {
  color: #1abc9c;
  outline: none;
}

/* Boutons dans la nav */
nav ul li a.login-btn {
  background: transparent;
  border: 2px solid #ecf0f1;
  color: #ecf0f1;
  padding: 8px 22px;
  border-radius: 30px;
  font-weight: 700;
  transition: background 0.3s ease, color 0.3s ease;
}

nav ul li a.login-btn:hover,
nav ul li a.login-btn:focus {
  background: #ecf0f1;
  color: #34495e;
  outline: none;
  text-decoration: none;
}

nav ul li a.signup-btn {
  background: #1abc9c;
  color: #fff;
  padding: 10px 22px;
  border-radius: 30px;
  box-shadow: 0 6px 18px rgba(26, 188, 156, 0.4);
  font-weight: 700;
  transition: background 0.35s ease, box-shadow 0.35s ease, transform 0.35s ease;
}

nav ul li a.signup-btn:hover,
nav ul li a.signup-btn:focus {
  background: #16a085;
  box-shadow: 0 10px 30px rgba(22, 160, 133, 0.6);
  transform: translateY(-3px);
  outline: none;
  text-decoration: none;
}

/* BOUTONS STYLÉS (pour boutons et liens avec class .btn ou .button) */
button,
.btn,
.button {
  display: inline-block;
  background: #1abc9c;
  border: none;
  color: #fff;
  padding: 14px 30px;
  font-size: 1.15rem;
  font-weight: 700;
  border-radius: 35px;
  cursor: pointer;
  box-shadow: 0 6px 18px rgba(26, 188, 156, 0.4);
  transition: background 0.35s ease, box-shadow 0.35s ease, transform 0.35s ease;
  user-select: none;
  text-transform: uppercase;
  letter-spacing: 1.2px;
  text-align: center;
  text-decoration: none;
}

button:hover,
.btn:hover,
.button:hover,
button:focus,
.btn:focus,
.button:focus {
  background: #16a085;
  box-shadow: 0 10px 30px rgba(22, 160, 133, 0.6);
  transform: translateY(-3px);
  outline: none;
  text-decoration: none;
}

button:disabled,
.btn:disabled,
.button:disabled {
  background: #7f8c8d;
  box-shadow: none;
  cursor: not-allowed;
  transform: none;
}

/* FORMULAIRES */
form {
  max-width: 440px;
  margin: 0 auto 40px;
  display: flex;
  flex-direction: column;
}

label {
  font-weight: 600;
  margin-bottom: 7px;
  color: #2c3e50;
}

input[type="text"],
input[type="email"],
input[type="password"],
select,
textarea {
  padding: 12px 15px;
  margin-bottom: 20px;
  border: 2px solid #bdc3c7;
  border-radius: 12px;
  font-size: 1rem;
  transition: border-color 0.3s ease;
}

input[type="text"]:focus,
input[type="email"]:focus,
input[type="password"]:focus,
select:focus,
textarea:focus {
  border-color: #1abc9c;
  outline: none;
  background-color: #e0f7f4;
}

/* GRILLE DES COURS */
.course-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(210px, 1fr));
  gap: 24px;
  margin-top: 30px;
}

.course-card {
  background: #f9fcfb;
  border-radius: 18px;
  box-shadow: 0 6px 18px rgba(26, 188, 156, 0.15);
  overflow: hidden;
  cursor: pointer;
  display: flex;
  flex-direction: column;
  transition: box-shadow 0.3s ease, transform 0.3s ease;
}

.course-card:hover {
  box-shadow: 0 15px 40px rgba(22, 160, 133, 0.35);
  transform: translateY(-8px);
}

.course-card img {
  width: 100%;
  height: 110px;
  object-fit: cover;
  border-radius: 18px 18px 0 0;
  transition: transform 0.3s ease;
}

.course-card:hover img {
  transform: scale(1.05);
}

.course-card h3 {
  padding: 16px 20px;
  font-size: 1.2rem;
  color: #149174;
  flex-grow: 1;
}

/* LANGUES (ajouté pour ta section langue avec images) */
.langues {
  display: flex;
  gap: 20px;
  justify-content: center;
  margin-top: 25px;
  flex-wrap: wrap;
}

.langue {
  text-align: center;
  flex: 1 1 150px;
  max-width: 200px;
  cursor: pointer;
  transition: transform 0.3s ease;
}

.langue a {
  color: #2c3e50;
  text-decoration: none;
  display: block;
  border-radius: 14px;
  overflow: hidden;
  box-shadow: 0 6px 18px rgba(26, 188, 156, 0.15);
  background: #f9fcfb;
  padding-bottom: 12px;
}

.langue img {
  width: 100%;
  height: 110px;
  object-fit: cover;
  border-radius: 14px 14px 0 0;
  transition: transform 0.3s ease;
}

.langue:hover,
.langue:focus-within {
  transform: translateY(-6px);
}

.langue:hover img,
.langue:focus-within img {
  transform: scale(1.05);
}

.langue p {
  margin-top: 12px;
  font-weight: 700;
  font-size: 1.1rem;
  color: #149174;
}

/* FOOTER */
footer {
  margin-top: auto;
  background: #ecf0f1;
  padding: 22px 40px;
  text-align: center;
  color: #7f8c8d;
  font-size: 0.9rem;
  border-top: 2px solid #bdc3c7;
  border-radius: 14px 14px 0 0;
}

/* RESPONSIVE */
@media (max-width: 720px) {
  nav ul {
    gap: 18px;
  }

  .container {
    padding: 25px 20px;
    margin: 20px auto;
  }

  form {
    max-width: 100%;
  }

  .course-grid {
    grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
    gap: 16px;
  }

  .langues {
    gap: 16px;
  }
}

@media (max-width: 400px) {
  .course-grid {
    grid-template-columns: 1fr;
  }

  .langues {
    flex-direction: column;
    align-items: center;
  }
}






db.php
<?php
$host = "localhost";
$user = "root";
$password = "root"; // Mot de passe MAMP
$database = "inscription_langues"; // ← le bon nom ici

$conn = new mysqli($host, $user, $password, $database);

if ($conn->connect_error) {
    die("Erreur de connexion : " . $conn->connect_error);
}
?>
