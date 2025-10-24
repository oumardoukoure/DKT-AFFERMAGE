<!doctype html>
<html lang="fr">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Location Toyota — [Ton Nom ou Entreprise]</title>
  <meta name="description" content="Location de voitures Toyota — modèles disponibles, galerie photos et contact." />

  <style>
    /* RESET BASIQUE */
    * { box-sizing: border-box; margin: 0; padding: 0; }
    html,body { height:100%; font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial; color:#1b1b1b; background:#f7f8fb; }

    /* CONTAINER */
    .container { max-width:1100px; margin:32px auto; padding:20px; }

    /* HEADER */
    header { display:flex; align-items:center; justify-content:space-between; gap:16px; }
    .brand { display:flex; align-items:center; gap:12px; text-decoration:none; color:inherit; }
    .logo { width:56px; height:56px; border-radius:10px; overflow:hidden; display:inline-block; background:#e9eef9; display:flex; align-items:center; justify-content:center; font-weight:700; color:#2b5bbd; }
    nav { display:flex; gap:12px; }
    nav a { text-decoration:none; color:#2b2b2b; padding:8px 12px; border-radius:8px; }
    nav a:hover { background:rgba(43,91,189,0.10); color:#2b5bbd; }

    /* HERO */
    .hero { background:linear-gradient(90deg, #fff, #f3f7ff); margin:20px 0; padding:24px; border-radius:14px; display:grid; grid-template-columns:1fr 360px; gap:20px; align-items:center; }
    .hero h1 { font-size:28px; margin-bottom:8px; }
    .hero p { color:#555; margin-bottom:12px; }

    /* QUICK CAR LIST */
    .cars { display:flex; gap:12px; flex-wrap:wrap; }
    .car { background:#fff; border-radius:12px; overflow:hidden; width:calc(33.333% - 8px); box-shadow:0 6px 18px rgba(20,20,60,0.06); }
    .car img { width:100%; display:block; height:160px; object-fit:cover; }
    .car .info { padding:12px; }
    .car h4 { margin-bottom:6px; }
    .car small { color:#666; display:block; margin-bottom:8px; }
    .price { font-weight:700; color:#1b5bd6; }

    /* GALERIE */
    .gallery { margin-top:22px; display:grid; grid-template-columns:repeat(3,1fr); gap:12px; }
    .gallery img { width:100%; height:200px; object-fit:cover; border-radius:10px; cursor:pointer; box-shadow:0 8px 20px rgba(20,20,60,0.07); }

    /* CONTACT / FORM */
    .contact-grid { display:grid; grid-template-columns:1fr 420px; gap:18px; margin-top:22px; }
    .card { background:#fff; padding:16px; border-radius:12px; box-shadow:0 6px 18px rgba(20,20,60,0.04); }
    form label { display:block; font-size:13px; margin-bottom:6px; color:#333; }
    form input, form select, form textarea { width:100%; padding:10px 12px; border-radius:8px; border:1px solid #e1e6f0; margin-bottom:10px; font-size:14px; }
    .btn { display:inline-block; background:#2b5bbd; color:#fff; padding:10px 14px; border-radius:10px; text-decoration:none; border:none; cursor:pointer; font-weight:600; }
    .coords { line-height:1.6; color:#333; }

    /* FOOTER */
    footer { margin-top:28px; text-align:center; color:#666; font-size:14px; }

    /* MODAL IMAGE */
    .modal { position:fixed; inset:0; display:none; align-items:center; justify-content:center; background:rgba(10,10,30,0.6); z-index:60; }
    .modal .inner { max-width:900px; width:95%; border-radius:12px; overflow:hidden; background:#000; }
    .modal img { width:100%; height:auto; display:block; }

    /* RESPONSIVE */
    @media (max-width:980px){
      .hero { grid-template-columns:1fr; }
      .contact-grid { grid-template-columns:1fr; }
      .cars .car { width:calc(50% - 8px); }
      .gallery { grid-template-columns:repeat(2,1fr); }
    }
    @media (max-width:560px){
      .cars .car { width:100%; }
      .gallery { grid-template-columns:1fr; }
      header { flex-direction:column; align-items:flex-start; gap:10px; }
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <a class="brand" href="#">
        <div class="logo">TYT</div>
        <div>
          <strong>Location Toyota</strong><br>
          <small>Confort • Fiabilité • Service local</small>
        </div>
      </a>

      <nav aria-label="Navigation principale">
        <a href="#models">Modèles</a>
        <a href="#gallery">Galerie</a>
        <a href="#contact">Contact</a>
      </nav>
    </header>

    <section class="hero" aria-labelledby="hero-title">
      <div>
        <h1 id="hero-title">Louez une Toyota — simple et rapide</h1>
        <p>Choisissez parmi nos modèles récents : city car, berline, SUV — assurances disponibles, kilométrage modulable. Réservation en ligne ou par téléphone.</p>

        <div class="card" style="margin-top:12px;">
          <h3 style="margin-bottom:8px;">Réservation rapide</h3>
          <form id="quick-book">
            <label for="model">Modèle</label>
            <select id="model" required>
              <option value="Toyota Yaris">Toyota Yaris — citadine</option>
              <option value="Toyota Corolla">Toyota Corolla — berline</option>
              <option value="Toyota RAV4">Toyota RAV4 — SUV</option>
            </select>

            <label for="from">Du</label>
            <input id="from" type="date" required />

            <label for="to">Au</label>
            <input id="to" type="date" required />

            <button class="btn" type="submit">Demander un devis</button>
          </form>
        </div>
      </div>

      <aside class="card">
        <h4>Contact & coordonnées</h4>
        <p class="coords">
          <!-- REMPLACE ICI: TES COORDONNÉES -->
          <strong>[Ton Nom / Nom de l’entreprise]</strong><br>
          Téléphone : <a href="tel:+33000000000">+33 0 00 00 00 00</a><br>
          Email : <a href="mailto:contact@example.com">contact@example.com</a><br>
          Adresse : 123 Rue Exemple, 75000 Paris
        </p>

        <div style="margin-top:10px;">
          <strong>Horaires</strong>
          <p style="color:#666; margin-top:6px;">Lun–Ven 9h–18h • Sam 9h–13h</p>
        </div>
      </aside>
    </section>

    <main>
      <section id="models">
        <h2 style="margin-bottom:12px;">Nos modèles populaires</h2>
        <div class="cars">
          <article class="car" aria-labelledby="car1">
            <img src="https://images.unsplash.com/photo-1542365887-8ee0c20d3f31?auto=format&fit=crop&w=1200&q=60" alt="Toyota Yaris - citadine">
            <div class="info">
              <h4 id="car1">Toyota Yaris</h4>
              <small>Citadine, parfaite pour la ville</small>
              <div><span class="price">35 €/jour</span></div>
            </div>
          </article>

          <article class="car" aria-labelledby="car2">
            <img src="https://images.unsplash.com/photo-1549921296-3b6f1d1d2d2b?auto=format&fit=crop&w=1200&q=60" alt="Toyota Corolla - berline">
            <div class="info">
              <h4 id="car2">Toyota Corolla</h4>
              <small>Berline spacieuse et confortable</small>
              <div><span class="price">55 €/jour</span></div>
            </div>
          </article>

          <article class="car" aria-labelledby="car3">
            <img src="https://images.unsplash.com/photo-1503376780353-7e6692767b70?auto=format&fit=crop&w=1200&q=60" alt="Toyota RAV4 - SUV">
            <div class="info">
              <h4 id="car3">Toyota RAV4</h4>
              <small>SUV, idéal pour les voyages</small>
              <div><span class="price">75 €/jour</span></div>
            </div>
          </article>
        </div>
      </section>

      <section id="gallery" style="margin-top:22px;">
        <h2 style="margin-bottom:12px;">Galerie</h2>
        <div class="gallery" aria-live="polite">
          <!-- images — clique pour agrandir -->
          <img src="https://images.unsplash.com/photo-1493238792000-8113da705763?auto=format&fit=crop&w=1200&q=60" alt="Toyota - vue de profil" data-full="https://images.unsplash.com/photo-1493238792000-8113da705763?auto=format&fit=crop&w=2000&q=80">
          <img src="https://images.unsplash.com/photo-1502877338535-766e1452684a?auto=format&fit=crop&w=1200&q=60" alt="Toyota - intérieur" data-full="https://images.unsplash.com/photo-1502877338535-766e1452684a?auto=format&fit=crop&w=2000&q=80">
          <img src="https://images.unsplash.com/photo-1497294815431-9365093b7331?auto=format&fit=crop&w=1200&q=60" alt="Toyota - sur la route" data-full="https://images.unsplash.com/photo-1497294815431-9365093b7331?auto=format&fit=crop&w=2000&q=80">
          <img src="https://images.unsplash.com/photo-1525609004556-c46c7d6cf023?auto=format&fit=crop&w=1200&q=60" alt="Toyota - parking" data-full="https://images.unsplash.com/photo-1525609004556-c46c7d6cf023?auto=format&fit=crop&w=2000&q=80">
          <img src="https://images.unsplash.com/photo-1502877338535-766e1452684a?auto=format&fit=crop&w=1200&q=60" alt="Toyota - volant" data-full="https://images.unsplash.com/photo-1502877338535-766e1452684a?auto=format&fit=crop&w=2000&q=80">
          <img src="https://images.unsplash.com/photo-1511919884226-fd3cad34687c?auto=format&fit=crop&w=1200&q=60" alt="Toyota - paysage" data-full="https://images.unsplash.com/photo-1511919884226-fd3cad34687c?auto=format&fit=crop&w=2000&q=80">
        </div>
      </section>

      <section id="contact" style="margin-top:22px;">
        <h2 style="margin-bottom:12px;">Contactez-nous / Réservation</h2>
        <div class="contact-grid">
          <div class="card" aria-labelledby="contact-info">
            <h3 id="contact-info">Coordonnées</h3>
            <p class="coords">
              <!-- REMPLACE ICI: TES COORDONNÉES (même que plus haut) -->
              <strong>[Ton Nom / Nom de l’entreprise]</strong><br>
              Téléphone : <a href="tel:+33000000000">+33 0 00 00 00 00</a><br>
              Email : <a href="mailto:contact@example.com">contact@example.com</a><br>
              Adresse : 123 Rue Exemple, 75000 Paris
            </p>

            <h4 style="margin-top:10px;">Services</h4>
            <ul style="color:#666; margin-top:6px;">
              <li>Livraison / récupération possible (sur devis)</li>
              <li>Assurance incluse / options supplémentaires</li>
              <li>Location courte et longue durée</li>
            </ul>
          </div>

          <form id="contact-form" class="card" aria-label="Formulaire de contact">
            <label for="name">Nom complet</label>
            <input id="name" type="text" placeholder="Prénom Nom" required>

            <label for="email">Email</label>
            <input id="email" type="email" placeholder="email@example.com" required>

            <label for="phone">Téléphone</label>
            <input id="phone" type="tel" placeholder="+33 6 12 34 56 78" required>

            <label for="message">Message / Détails réservation</label>
            <textarea id="message" rows="4" placeholder="Dates, modèle souhaité, options..." required></textarea>

            <button class="btn" type="submit">Envoyer la demande</button>
            <p id="form-feedback" style="margin-top:10px;color:green;display:none;">Merci — votre demande a été préparée (voir console pour détails).</p>
          </form>
        </div>
      </section>
    </main>

    <footer>
      © <span id="year"></span> Location Toyota — Tous droits réservés.
    </footer>
  </div>

  <!-- MODAL IMAGE -->
  <div id="img-modal" class="modal" role="dialog" aria-hidden="true">
    <div class="inner" role="document">
      <img id="modal-img" src="" alt="">
    </div>
  </div>

  <script>
    // Mise à jour année
    document.getElementById('year').textContent = new Date().getFullYear();

    // Galerie - clic pour agrandir
    document.querySelectorAll('.gallery img').forEach(img => {
      img.addEventListener('click', () => {
        const modal = document.getElementById('img-modal');
        const modalImg = document.getElementById('modal-img');
        const full = img.dataset.full || img.src;
        modalImg.src = full;
        modalImg.alt = img.alt || 'Photo agrandie';
        modal.style.display = 'flex';
        modal.setAttribute('aria-hidden','false');
      });
    });
    document.getElementById('img-modal').addEventListener('click', (e)=>{
      if (e.target.id === 'img-modal' || e.target.id === 'modal-img') {
        e.currentTarget.style.display = 'none';
        e.currentTarget.setAttribute('aria-hidden','true');
      }
    });

    // Formulaire "quick-book"
    document.getElementById('quick-book').addEventListener('submit', (e)=>{
      e.preventDefault();
      const model = document.getElementById('model').value;
      const from = document.getElementById('from').value;
      const to = document.getElementById('to').value;
      // Validation basique dates
      if (!from || !to || new Date(to) < new Date(from)) {
        alert('Veuillez choisir des dates valides (la date de fin doit être après la date de début).');
        return;
      }
      // Ici : à remplacer par envoi réel (email / API). Pour l’instant on affiche une confirmation.
      alert(`Demande reçue\nModèle: ${model}\nDu: ${from}\nAu: ${to}\nNous vous contacterons sous peu.`);
      // Désactiver submit pendant 2s
      e.target.querySelector('button').disabled = true;
      setTimeout(()=> e.target.querySelector('button').disabled = false, 1500);
    });

    // Contact form -> simulation d'envoi (affiche données dans la console)
    document.getElementById('contact-form').addEventListener('submit', (e)=>{
      e.preventDefault();
      const data = {
        name: document.getElementById('name').value,
        email: document.getElementById('email').value,
        phone: document.getElementById('phone').value,
        message: document.getElementById('message').value,
        submittedAt: new Date().toISOString()
      };
      // == SIMULATION d'envoi ==
      console.log('Nouvelle demande de contact / réservation:', data);
      // afficher un message d'info pour l'utilisateur
      const fb = document.getElementById('form-feedback');
      fb.style.display = 'block';
      fb.textContent = "Merci — votre demande a été envoyée. Nous vous contacterons bientôt.";
      // reset form
      e.target.reset();
      // cacher feedback après 5s
      setTimeout(()=> fb.style.display = 'none', 5000);
    });
  </script>
</body>
</html>