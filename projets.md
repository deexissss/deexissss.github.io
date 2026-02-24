---
layout: default
title: Mes Projets
---

<style>
/* --- 1. STYLE DE LA GRILLE (inchangé) --- */
.project-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 20px;
  margin-top: 30px;
}
.project-card {
  border: 1px solid #e1e4e8;
  border-radius: 10px;
  padding: 20px;
  background-color: #ffffff;
  color: #333333 !important;
  text-decoration: none;
  transition: transform 0.2s, box-shadow 0.2s;
  box-shadow: 0 4px 6px rgba(0,0,0,0.05);
  display: flex;
  flex-direction: column;
}
.project-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 15px rgba(0,0,0,0.1);
  text-decoration: none;
}
.project-card h3 { margin-top: 0; margin-bottom: 10px; font-size: 1.2em; color: #333;}
.project-card p { font-size: 0.9em; color: #666; margin-bottom: 15px; flex-grow: 1; }
.tags { font-size: 0.8em; font-weight: bold; color: #0366d6; }

/* --- 2. STYLE DES FENÊTRES MODALES (Pop-up) --- */
.modal-window {
  position: fixed;
  background-color: rgba(0, 0, 0, 0.85); /* Fond noir semi-transparent */
  top: 0; right: 0; bottom: 0; left: 0;
  z-index: 999;
  visibility: hidden;
  opacity: 0;
  pointer-events: none;
  transition: all 0.3s;
}
/* C'est ici la magie : quand l'URL se termine par #minishell, la modale s'affiche */
.modal-window:target {
  visibility: visible;
  opacity: 1;
  pointer-events: auto;
}
.modal-content {
  width: 90%;
  max-width: 700px;
  position: absolute;
  top: 50%; left: 50%;
  transform: translate(-50%, -50%);
  padding: 30px;
  background: #ffffff; /* Fond blanc pour le texte */
  color: #333333;
  border-radius: 10px;
  max-height: 80vh;
  overflow-y: auto; /* Permet de scroller si le texte est long */
}
.modal-close {
  color: #ff4c4c;
  font-size: 1.5em;
  font-weight: bold;
  position: absolute;
  right: 20px;
  top: 15px;
  text-decoration: none;
}
  /* --- 3. BOUTON RETOUR --- */
.btn-retour {
  display: inline-block;
  padding: 10px 20px;
  background-color: #f3f4f6; /* Gris très clair */
  color: #333333 !important;
  text-decoration: none;
  font-weight: bold;
  border-radius: 8px;
  border: 1px solid #d1d5db;
  transition: all 0.2s;
  margin-bottom: 20px;
}
.btn-retour:hover {
  background-color: #e5e7eb; /* Gris un peu plus foncé au survol */
  transform: translateY(-2px);
  text-decoration: none;
  box-shadow: 0 4px 6px rgba(0,0,0,0.05);
}
.modal-close:hover { color: #cc0000; text-decoration: none; }
</style>
<div>
  <a href="./index.html" class="btn-retour">
    🏠 Retour à l'accueil
  </a>
</div>
<div class="project-grid">

  <a href="#minishell" class="project-card">
    <h3>🐚 Minishell</h3>
    <p>Recréation d'un mini-shell UNIX. Gestion des processus, des pipes et des redirections.</p>
    <div class="tags">C • Bash • Unix</div>
  </a>

  <a href="#cub3d" class="project-card">
    <h3>🎮 Cub3D</h3>
    <p>Création d'un moteur 3D en Ray-Casting. Gestion des textures et collisions.</p>
    <div class="tags">C • MiniLibX • Math</div>
  </a>

</div>

<div id="minishell" class="modal-window">
  <div class="modal-content">
    <a href="#" title="Fermer" class="modal-close">✖</a>
    <h2 style="color: #333;">🐚 Minishell : En détail</h2>
    <p>Le but de ce projet 42 était de coder un vrai shell en C, en gérant de nombreux concepts fondamentaux d'Unix.</p>
    <ul>
      <li><strong>Défis :</strong> Parsing complexe des commandes, gestion de l'environnement, signaux (Ctrl-C, Ctrl-D, Ctrl-\).</li>
      <li><strong>Notions acquises :</strong> fork, execve, pipe, dup2.</li>
    </ul>
    <br>
    <a href="LIEN_VERS_TON_GITHUB_MINISHELL" target="_blank" style="background:#333; color:white; padding:10px 15px; border-radius:5px; text-decoration:none;">Voir le code source sur GitHub</a>
  </div>
</div>

<div id="cub3d" class="modal-window">
  <div class="modal-content">
    <a href="#" title="Fermer" class="modal-close">✖</a>
    <h2 style="color: #333;">🎮 Cub3D : En détail</h2>
    <p>Mon premier projet graphique à 42 ! L'objectif était de créer une vue en 3D à partir d'une carte en 2D en utilisant la technique du Ray-Casting.</p>
    <ul>
      <li><strong>Défis :</strong> Mathématiques appliquées (trigonométrie), optimisation du rendu, parsing de la carte (fichiers .cub).</li>
      <li><strong>Notions acquises :</strong> MiniLibX, gestion des événements clavier, dessin pixel par pixel.</li>
    </ul>
    <br>
    <a href="LIEN_VERS_TON_GITHUB_CUB3D" target="_blank" style="background:#333; color:white; padding:10px 15px; border-radius:5px; text-decoration:none;">Voir le code source sur GitHub</a>
  </div>
</div>
