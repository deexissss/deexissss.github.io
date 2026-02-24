---
layout: default
title: Mes Projets
---
<style>
/* Style de la grille pour aligner les projets */
.project-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 20px;
  margin-top: 30px;
}

/* Style de chaque carte de projet */
.project-card {
  border: 1px solid #e1e4e8;
  border-radius: 10px;
  padding: 20px;
  background-color: #ffffff; /* Fond blanc pour les cartes */
  color: #333333; /* Texte foncé */
  text-decoration: none;
  transition: transform 0.2s, box-shadow 0.2s;
  box-shadow: 0 4px 6px rgba(0,0,0,0.05);
  display: flex;
  flex-direction: column;
}

/* Effet de survol (quand on passe la souris) */
.project-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 15px rgba(0,0,0,0.1);
  text-decoration: none;
  color: inherit;
}

/* Style des titres et textes dans la carte */
.project-card h3 {
  margin-top: 0;
  margin-bottom: 10px;
  font-size: 1.2em;
}
.project-card p {
  font-size: 0.9em;
  color: #666;
  margin-bottom: 15px;
  flex-grow: 1;
}

/* Style des petites icônes/tags en bas de la carte */
.tags {
  font-size: 0.8em;
  font-weight: bold;
  color: #0366d6;
}
</style>

<div class="project-grid">

  <a href="./minishell.html" class="project-card">
    <h3>🐚 Minishell</h3>
    <p>Recréation d'un mini-shell UNIX. Gestion des processus, des pipes et des redirections.</p>
    <div class="tags">C • Bash • Unix</div>
  </a>

  <a href="./cub3d.html" class="project-card">
    <h3>🎮 Cub3D</h3>
    <p>Création d'un moteur 3D en Ray-Casting. Gestion des textures et collisions.</p>
    <div class="tags">C • MiniLibX • Math</div >
  </a>

  <a href="./webserv.html" class="project-card">
    <h3>🌐 Webserv</h3>
    <p>Écriture d'un serveur HTTP complet en C++ 98 capable de gérer plusieurs connexions.</p>
    <div class="tags">C++ • Réseau • HTTP</div>
  </a>

</div>
