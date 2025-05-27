<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Plan - Présentation PFE</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
  <style>
    :root {
      --primary: #0056b3;
      --light: #f9fbfd;
      --dark: #2d3436;
      --accent: #00c853;
      --card-hover: #e3f2fd;
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: var(--light);
      color: var(--dark);
      line-height: 1.6;
    }

      header {
      background: #1f2937;
      color: white;
      padding: 2rem;
      text-align: center;
    }

    .container {
      max-width: 990px;
      margin: 2rem auto;
      padding: 0 1rem;
      animation: fadeIn 1s ease-in;
    }

    .card {
      background: white;
      border-radius: 12px;
      padding: 1.75rem;
      margin-bottom: 1.75rem;
      box-shadow: 0 4px 15px rgba(0,0,0,0.08);
      transition: all 0.3s ease;
    }

    .card:hover {
      transform: translateY(-4px);
      background-color: var(--card-hover);
    }

    h2 {
      display: flex;
      align-items: center;
      font-size: 1.4rem;
      color: var(--primary);
      margin-bottom: 1rem;
    }

    h2 i {
      margin-right: 10px;
    }

    ul li {
      margin-bottom: 0.5rem;
    }

    @keyframes fadeIn {
      from {opacity: 0; transform: translateY(10px);}
      to {opacity: 1; transform: translateY(0);}
    }

       .btn {
      display: inline-block;
      background: #4f46e5;
      color: white;
      padding: 0.6rem 1.2rem;
      text-decoration: none;
      border-radius: 8px;
      margin-top: 1rem;
    }
    .btn:hover {
      background: #4338ca;
    }

    footer {
      background: #f0f0f0;
    color: #000000; /* Couleur du texte */
    padding: 20px 0; /* Espacement interne */
    text-align: center; /* Alignement centralisé */
    font-size: 20px; /* Taille de police */
}

  </style>
</head>
<body>

  <header>
    <h1>🚀 Plan de la Présentation - PFE</h1>
    <p>Réseaux & Systèmes Informatiques • Année 2025</p>
  </header>

  <div class="container">
    <div class="card" id="intro">
      <h2><i class="fa-solid fa-lightbulb fa-bounce" style="color: #fbc02d;"></i> Introduction & Contexte</h2>
      <ul>
        <li><strong>Centralisation des logs :</strong> Regrouper toutes les traces d'activité pour une analyse simplifiée.</li>
        <li><strong>Détection des incidents de sécurité :</strong> Identifier rapidement les comportements suspects ou attaques potentielles.</li>
        <li><strong>Amélioration de la réponse aux attaques :</strong> Réagir efficacement et limiter l'impact des incidents détectés.</li>
      </ul>
    </div>

    <div class="card" id="probleme">
      <h2><i class="fa-solid fa-triangle-exclamation fa-shake" style="color: #e53935;"></i> Problématique</h2>
      <ul>
        <li style="white-space: nowrap;"><strong>Volume croissant des données :</strong> Les systèmes produisent des milliers de logs par seconde, ce qui complique leur analyse.</li>
        <li><strong>Détection manuelle inefficace :</strong> Identifier les incidents à la main est long et sujet à erreurs humaines.</li>
        <li><strong>Réactivité limitée :</strong> Sans centralisation, la réponse aux attaques est souvent lente et mal coordonnée.</li>
      </ul>
      <p><strong>Besoins :</strong> centraliser les logs, détecter les incidents de sécurité et améliorer la réponse aux attaques.</p>
    </div>

    <div class="card" id="methode">
      <h2><i class="fa-solid fa-gears fa-spin" style="color: #1976d2;"></i> Méthodologie & Approche</h2>
      <ul>
        <li>Création d’un environnement réseau virtuel sous <strong>EVE-NG</strong> intégrant deux pare-feux <strong>FortiGate</strong>.</li>
        <li>Établissement d’un tunnel <strong>VPN IPsec Site-to-Site</strong> pour sécuriser les échanges inter-sites.</li>
        <li>Paramétrage du service <strong>Syslog</strong> afin de rediriger les journaux d’événements vers <strong>IBM QRadar</strong>.</li>
        <li>Installation et configuration de l’agent <strong>WinCollect</strong> pour la collecte centralisée des logs Windows.</li>
        <li>Centralisation, corrélation et analyse des événements de sécurité via la plateforme <strong>IBM QRadar</strong>.</li>
      </ul>
    </div>

    <div class="card">
      <h2><i class="fas fa-robot fa-bounce" style="color: #5b6065;"></i> Automatisation avec Python</h2>
      <ul>
        <li>Script Python vérifiant l’état du pare-feu Windows toutes les 10 secondes.</li>
        <li>Réactivation automatique du pare-feu s’il est désactivé.</li>
        <li>Envoi d’une alerte par email (via SMTP) lors de toute modification détectée.</li>
        <li>Journalisation des actions dans un fichier log local pour audit.</li>
      </ul>
    </div>

    <div class="card" id="resultats">
      <h2><i class="fa-solid fa-chart-line fa-beat" style="color: #43a047;"></i> Résultats obtenus</h2>
      <ul>
        <li>Centralisation efficace et automatisée des journaux d’événements issus de différents équipements et systèmes.</li>
        <li>Détection proactive et en temps réel des tentatives d’intrusion et incidents de sécurité.</li>
        <li>Visualisation claire et hiérarchisée des alertes, facilitant la priorisation et la prise de décision rapide.</li>
      </ul>
    </div>


    
    <div class="card" id="demo">
      <h2><i class="fa-solid fa-play-circle fa-fade" style="color: #8e24aa;"></i> Démonstration</h2>
      <ul> 
       <li> Présentation vidéo en temps réel de l’interface QRadar et de ses principales fonctionnalités, incluant la topologie réseau, la collecte des logs et la réponse aux alertes détectées.</li>
      </ul>
     
    </div>



  <div class="card">
    <h2><i class="fa-solid fa-circle-check fa-bounce" style="color: #43a047;"></i> Valeur ajoutée</h2>
      <ul>
        <li>Réduction des risques de sécurité</li>
        <li>Gain de temps pour les analystes</li>
        <li>Automatisation et surveillance proactive</li>
      </ul>
    </div>


    <div class="card" id="conclusion">
      <h2><i class="fa-solid fa-flag-checkered fa-bounce" style="color: #ff9800;"></i> Conclusion & Perspectives</h2>
      <ul>
        <li>Projet réussi de mise en place d’une solution de gestion centralisée des logs avec QRadar.</li>
        <li>Perspectives : intégrer des outils SOAR pour une réponse automatique aux incidents et enrichir la détection par intelligence artificielle.</li>
      </ul>
    </div>
      <div class="card">
   
    <h2><i class="fa-solid fa-folder-open fa-beat" style="color: #f79902;"></i>&nbsp;&nbsp;Rapport & Ressources</h2>
    <a class="btn" href="c:\Users\sadok\Downloads\Rapport_PFE2025.pdf" target="_blank">📄 Télécharger le rapport PDF</a>
  </div>
</div>
  </div>

  
<footer>
    <div class="container">
        <p>Projet Final d'Études - Étudiants à l'ISET de Siliana • Réalisé par : Lamiri Sadok & Sendessni Maram</p>
        <div class="icons">
            <a href="https://www.linkedin.com/in/exemple/ "><i class="fab fa-linkedin"></i></a>
            <a href="https://github.com/exemple "><i class="fab fa-github"></i></a>
        </div>
    </div>
</footer>
  

</body>
</html>
