<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Dr Anna Kowalska</title>

  <!-- SVG favicon jako inline data URI — zmień litery AK na swoje inicjały -->
  <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 64 64'%3E%3Crect width='64' height='64' rx='12' fill='%232C5F8A'/%3E%3Ctext x='50%25' y='54%25' dominant-baseline='middle' text-anchor='middle' font-family='Georgia,serif' font-size='26' font-weight='bold' fill='%23ffffff'%3EAK%3C/text%3E%3C/svg%3E" />

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Lora:ital,wght@0,400;0,600;1,400&family=Source+Sans+3:wght@300;400;600&display=swap" rel="stylesheet">

  <style>
    :root {
      --cream:      #FAF8F4;
      --white:      #FFFFFF;
      --ink:        #1E1E2E;
      --ink-soft:   #4A4A5A;
      --blue:       #2C5F8A;
      --blue-light: #D6E6F2;
      --gold:       #B08D57;
      --border:     #E2DDD6;
      --radius:     8px;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      background: var(--cream);
      color: var(--ink);
      font-family: 'Source Sans 3', sans-serif;
      font-weight: 300;
      line-height: 1.7;
      font-size: 17px;
    }

    nav {
      position: sticky;
      top: 0;
      z-index: 100;
      background: rgba(250,248,244,0.92);
      backdrop-filter: blur(8px);
      border-bottom: 1px solid var(--border);
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0.75rem 2.5rem;
    }
    .nav-name {
      font-family: 'Lora', serif;
      font-weight: 600;
      font-size: 1rem;
      color: var(--blue);
      letter-spacing: 0.02em;
    }
    .nav-links {
      display: flex;
      gap: 2rem;
      list-style: none;
      align-items: center;
    }
    .nav-links a {
      text-decoration: none;
      color: var(--ink-soft);
      font-size: 0.88rem;
      font-weight: 400;
      letter-spacing: 0.06em;
      text-transform: uppercase;
      transition: color 0.2s;
    }
    .nav-links a:hover { color: var(--blue); }

    .lang-toggle {
      display: flex;
      border: 1px solid var(--border);
      border-radius: 20px;
      overflow: hidden;
      font-size: 0.78rem;
    }
    .lang-toggle button {
      background: transparent;
      border: none;
      padding: 0.3rem 0.85rem;
      cursor: pointer;
      font-family: 'Source Sans 3', sans-serif;
      font-weight: 600;
      letter-spacing: 0.05em;
      color: var(--ink-soft);
      transition: background 0.2s, color 0.2s;
    }
    .lang-toggle button.active { background: var(--blue); color: #fff; }

    .hero {
      max-width: 900px;
      margin: 0 auto;
      padding: 5rem 2rem 4rem;
      display: grid;
      grid-template-columns: 200px 1fr;
      gap: 3.5rem;
      align-items: center;
    }

    .photo-wrap { position: relative; }
    .photo-wrap::before {
      content: '';
      position: absolute;
      inset: -8px -8px 8px 8px;
      border: 2px solid var(--gold);
      border-radius: var(--radius);
      z-index: 0;
    }
    .photo-wrap img, .photo-placeholder {
      position: relative;
      z-index: 1;
      width: 200px;
      height: 240px;
      object-fit: cover;
      border-radius: var(--radius);
      display: block;
    }
    .photo-placeholder {
      background: var(--blue-light);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      color: var(--blue);
      font-size: 0.78rem;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      gap: 0.5rem;
      border: 2px dashed var(--blue);
    }
    .photo-placeholder svg { opacity: 0.45; }

    .hero-text h1 {
      font-family: 'Lora', serif;
      font-size: 2.4rem;
      font-weight: 600;
      line-height: 1.2;
      color: var(--ink);
      margin-bottom: 0.35rem;
    }
    .hero-text .title {
      color: var(--blue);
      font-size: 1rem;
      font-weight: 400;
      letter-spacing: 0.03em;
      margin-bottom: 0.2rem;
    }
    .hero-text .affiliation {
      color: var(--ink-soft);
      font-size: 0.92rem;
      margin-bottom: 1.4rem;
      padding-bottom: 1.4rem;
      border-bottom: 1px solid var(--border);
    }
    .hero-text .bio {
      color: var(--ink-soft);
      font-size: 0.97rem;
      max-width: 520px;
    }
    .hero-links {
      display: flex;
      gap: 0.85rem;
      margin-top: 1.6rem;
      flex-wrap: wrap;
    }
    .btn {
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      padding: 0.55rem 1.25rem;
      border-radius: 4px;
      font-size: 0.84rem;
      font-weight: 600;
      letter-spacing: 0.04em;
      text-decoration: none;
      cursor: pointer;
      transition: all 0.2s;
    }
    .btn-primary { background: var(--blue); color: #fff; border: 1.5px solid var(--blue); }
    .btn-primary:hover { background: #1e4a6e; border-color: #1e4a6e; }
    .btn-outline { background: transparent; color: var(--blue); border: 1.5px solid var(--blue); }
    .btn-outline:hover { background: var(--blue-light); }

    .section {
      max-width: 900px;
      margin: 0 auto;
      padding: 3rem 2rem;
      border-top: 1px solid var(--border);
    }
    .section-label {
      font-size: 0.72rem;
      font-weight: 600;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 0.45rem;
    }
    .section h2 {
      font-family: 'Lora', serif;
      font-size: 1.6rem;
      font-weight: 600;
      color: var(--ink);
      margin-bottom: 1.8rem;
    }

    .tags { display: flex; flex-wrap: wrap; gap: 0.6rem; }
    .tag {
      background: var(--blue-light);
      color: var(--blue);
      padding: 0.35rem 1rem;
      border-radius: 20px;
      font-size: 0.84rem;
    }

    .pub-list { list-style: none; display: flex; flex-direction: column; gap: 1.3rem; }
    .pub-item {
      background: var(--white);
      border: 1px solid var(--border);
      border-left: 3px solid var(--blue);
      border-radius: var(--radius);
      padding: 1.2rem 1.4rem;
    }
    .pub-title {
      font-family: 'Lora', serif;
      font-size: 1rem;
      font-weight: 600;
      color: var(--ink);
      margin-bottom: 0.3rem;
    }
    .pub-meta { font-size: 0.85rem; color: var(--ink-soft); }
    .pub-meta em { color: var(--gold); font-style: normal; font-weight: 600; }
    .pub-link {
      display: inline-block;
      margin-top: 0.5rem;
      font-size: 0.8rem;
      color: var(--blue);
      text-decoration: none;
      font-weight: 600;
    }
    .pub-link:hover { text-decoration: underline; }

    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(255px, 1fr));
      gap: 1.3rem;
    }
    .project-card {
      background: var(--white);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 1.4rem;
      transition: box-shadow 0.2s, transform 0.2s;
    }
    .project-card:hover { box-shadow: 0 6px 24px rgba(44,95,138,0.1); transform: translateY(-2px); }
    .project-card h3 {
      font-family: 'Lora', serif;
      font-size: 1rem;
      font-weight: 600;
      color: var(--ink);
      margin-bottom: 0.5rem;
    }
    .project-card p { font-size: 0.88rem; color: var(--ink-soft); }
    .project-year {
      display: inline-block;
      margin-top: 0.8rem;
      font-size: 0.75rem;
      font-weight: 600;
      letter-spacing: 0.08em;
      color: var(--gold);
      text-transform: uppercase;
    }

    .contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1.8rem; }
    .contact-item { display: flex; flex-direction: column; gap: 0.2rem; }
    .contact-label {
      font-size: 0.74rem;
      font-weight: 600;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: var(--ink-soft);
    }
    .contact-value { font-size: 0.95rem; color: var(--ink); }
    .contact-value a { color: var(--blue); text-decoration: none; }
    .contact-value a:hover { text-decoration: underline; }

    footer {
      text-align: center;
      padding: 2rem;
      border-top: 1px solid var(--border);
      font-size: 0.8rem;
      color: var(--ink-soft);
    }

    @media (max-width: 640px) {
      nav { padding: 0.75rem 1rem; }
      .nav-links { gap: 0.9rem; }
      .hero { grid-template-columns: 1fr; padding: 3rem 1.5rem 2rem; gap: 2rem; }
      .photo-wrap { justify-self: center; }
      .contact-grid { grid-template-columns: 1fr; }
      .section { padding: 2.5rem 1.5rem; }
    }
  </style>
</head>
<body>

<nav>
  <span class="nav-name">Dr Anna Kowalska</span>
  <ul class="nav-links">
    <li><a href="#about"    data-pl="O mnie"    data-en="About">O mnie</a></li>
    <li><a href="#pubs"     data-pl="Publikacje" data-en="Publications">Publikacje</a></li>
    <li><a href="#projects" data-pl="Projekty"  data-en="Projects">Projekty</a></li>
    <li><a href="#contact"  data-pl="Kontakt"   data-en="Contact">Kontakt</a></li>
    <li>
      <div class="lang-toggle">
        <button id="btn-pl" class="active" onclick="setLang('pl')">PL</button>
        <button id="btn-en"                onclick="setLang('en')">EN</button>
      </div>
    </li>
  </ul>
</nav>

<section class="hero" id="about">
  <div class="photo-wrap">
    <!-- Odkomentuj i podaj ścieżkę do swojego zdjęcia: -->
    <!-- <img src="assets/photo.jpg" alt="Anna Kowalska"> -->
    <div class="photo-placeholder">
      <svg width="38" height="38" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
        <circle cx="12" cy="8" r="4"/><path d="M4 20c0-4 3.6-7 8-7s8 3 8 7"/>
      </svg>
      <span data-pl="Twoje zdjęcie" data-en="Your photo">Twoje zdjęcie</span>
    </div>
  </div>

  <div class="hero-text">
    <h1>Dr Anna Kowalska</h1>
    <p class="title"
       data-pl="Adiunkt · Zakład Językoznawstwa Kognitywnego"
       data-en="Assistant Professor · Department of Cognitive Linguistics">
      Adiunkt · Zakład Językoznawstwa Kognitywnego
    </p>
    <p class="affiliation"
       data-pl="Wydział Filologiczny, Uniwersytet Jagielloński · Kraków, Polska"
       data-en="Faculty of Philology, Jagiellonian University · Kraków, Poland">
      Wydział Filologiczny, Uniwersytet Jagielloński · Kraków, Polska
    </p>
    <p class="bio"
       data-pl="Badam kognitywne mechanizmy metafory i metonimii w dyskursie naukowym. Interesuję się też lingwistyką korpusową oraz zastosowaniami NLP w badaniach humanistycznych."
       data-en="My research focuses on cognitive mechanisms of metaphor and metonymy in academic discourse. I am also interested in corpus linguistics and NLP applications in the humanities.">
      Badam kognitywne mechanizmy metafory i metonimii w dyskursie naukowym. Interesuję się też lingwistyką korpusową oraz zastosowaniami NLP w badaniach humanistycznych.
    </p>
    <div class="hero-links">
      <a href="assets/cv.pdf" class="btn btn-primary" download>
        <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
          <path d="M12 16V4"/><path d="m6 12 6 6 6-6"/><path d="M4 20h16"/>
        </svg>
        <span data-pl="Pobierz CV" data-en="Download CV">Pobierz CV</span>
      </a>
      <a href="https://orcid.org/0000-0000-0000-0000" class="btn btn-outline" target="_blank" rel="noopener">ORCID</a>
      <a href="https://scholar.google.com" class="btn btn-outline" target="_blank" rel="noopener">Google Scholar</a>
    </div>
  </div>
</section>

<section class="section">
  <p class="section-label" data-pl="Zainteresowania" data-en="Research Interests">Zainteresowania</p>
  <h2 data-pl="Obszary badań" data-en="Research Areas">Obszary badań</h2>
  <div class="tags">
    <span class="tag" data-pl="Językoznawstwo kognitywne" data-en="Cognitive Linguistics">Językoznawstwo kognitywne</span>
    <span class="tag" data-pl="Metafora konceptualna"     data-en="Conceptual Metaphor">Metafora konceptualna</span>
    <span class="tag" data-pl="Lingwistyka korpusowa"     data-en="Corpus Linguistics">Lingwistyka korpusowa</span>
    <span class="tag" data-pl="Dyskurs akademicki"        data-en="Academic Discourse">Dyskurs akademicki</span>
    <span class="tag" data-pl="Przetwarzanie języka naturalnego" data-en="Natural Language Processing">Przetwarzanie języka naturalnego</span>
    <span class="tag" data-pl="Semantyka leksykalna"      data-en="Lexical Semantics">Semantyka leksykalna</span>
  </div>
</section>

<section class="section" id="pubs">
  <p class="section-label" data-pl="Dorobek naukowy" data-en="Academic Output">Dorobek naukowy</p>
  <h2 data-pl="Wybrane publikacje" data-en="Selected Publications">Wybrane publikacje</h2>
  <ul class="pub-list">

    <li class="pub-item">
      <p class="pub-title"
         data-pl="Metafory czasu w polskim dyskursie naukowym: badanie korpusowe"
         data-en="Temporal Metaphors in Polish Academic Discourse: A Corpus Study">
        Metafory czasu w polskim dyskursie naukowym: badanie korpusowe
      </p>
      <p class="pub-meta">
        Kowalska, A. (2024). <em data-pl="Język Polski" data-en="Język Polski">Język Polski</em>, 104(2), 45–67.
      </p>
      <a href="#" class="pub-link" data-pl="→ DOI / pełny tekst" data-en="→ DOI / full text">→ DOI / pełny tekst</a>
    </li>

    <li class="pub-item">
      <p class="pub-title"
         data-pl="Kognitywne podstawy metonimii w terminologii naukowej"
         data-en="Cognitive Foundations of Metonymy in Scientific Terminology">
        Kognitywne podstawy metonimii w terminologii naukowej
      </p>
      <p class="pub-meta">
        Kowalska, A. &amp; Nowak, P. (2023). <em>Cognitive Linguistic Studies</em>, 10(1), 112–138.
      </p>
      <a href="#" class="pub-link" data-pl="→ DOI / pełny tekst" data-en="→ DOI / full text">→ DOI / pełny tekst</a>
    </li>

    <li class="pub-item">
      <p class="pub-title"
         data-pl="Automatyczna detekcja metafor konceptualnych z użyciem modeli językowych"
         data-en="Automatic Detection of Conceptual Metaphors Using Language Models">
        Automatyczna detekcja metafor konceptualnych z użyciem modeli językowych
      </p>
      <p class="pub-meta">
        Kowalska, A. (2022). <em>Digital Scholarship in the Humanities</em>, 37(4), 890–910.
      </p>
      <a href="#" class="pub-link" data-pl="→ DOI / pełny tekst" data-en="→ DOI / full text">→ DOI / pełny tekst</a>
    </li>

  </ul>
</section>

<section class="section" id="projects">
  <p class="section-label" data-pl="Granty i projekty" data-en="Grants &amp; Projects">Granty i projekty</p>
  <h2 data-pl="Projekty badawcze" data-en="Research Projects">Projekty badawcze</h2>
  <div class="projects-grid">

    <div class="project-card">
      <h3 data-pl="MetaKorpus PL" data-en="MetaCorpus PL">MetaKorpus PL</h3>
      <p data-pl="Budowa wielomilionowego korpusu polskich tekstów naukowych z anotacją metafor. Finansowanie: NCN."
         data-en="Building a multi-million corpus of Polish academic texts with metaphor annotation. Funded by NCN.">
        Budowa wielomilionowego korpusu polskich tekstów naukowych z anotacją metafor. Finansowanie: NCN.
      </p>
      <span class="project-year">2023–2026</span>
    </div>

    <div class="project-card">
      <h3 data-pl="CogDisc — Dyskurs kognitywny" data-en="CogDisc — Cognitive Discourse">CogDisc — Dyskurs kognitywny</h3>
      <p data-pl="Międzynarodowy projekt porównawczy analizujący metafory w dyskursie akademickim w 6 językach europejskich."
         data-en="International comparative project analysing metaphors in academic discourse across 6 European languages.">
        Międzynarodowy projekt porównawczy analizujący metafory w dyskursie akademickim w 6 językach europejskich.
      </p>
      <span class="project-year">2021–2024</span>
    </div>

    <div class="project-card">
      <h3 data-pl="NLP w humanistyce" data-en="NLP in the Humanities">NLP w humanistyce</h3>
      <p data-pl="Warsztaty i materiały dydaktyczne dla humanistów z zakresu przetwarzania języka naturalnego."
         data-en="Workshops and teaching materials for humanities scholars on NLP and text analysis.">
        Warsztaty i materiały dydaktyczne dla humanistów z zakresu przetwarzania języka naturalnego.
      </p>
      <span class="project-year">2020–2022</span>
    </div>

  </div>
</section>

<section class="section" id="contact">
  <p class="section-label" data-pl="Dane kontaktowe" data-en="Contact">Dane kontaktowe</p>
  <h2 data-pl="Kontakt" data-en="Get in Touch">Kontakt</h2>
  <div class="contact-grid">
    <div class="contact-item">
      <span class="contact-label" data-pl="E-mail" data-en="E-mail">E-mail</span>
      <span class="contact-value"><a href="mailto:a.kowalska@uj.edu.pl">a.kowalska@uj.edu.pl</a></span>
    </div>
    <div class="contact-item">
      <span class="contact-label" data-pl="Dyżury" data-en="Office Hours">Dyżury</span>
      <span class="contact-value"
            data-pl="Wtorek 11:00–13:00, pok. 214"
            data-en="Tuesday 11:00–13:00, room 214">Wtorek 11:00–13:00, pok. 214</span>
    </div>
    <div class="contact-item">
      <span class="contact-label" data-pl="Adres" data-en="Address">Adres</span>
      <span class="contact-value"
            data-pl="al. Mickiewicza 9a, 31-120 Kraków"
            data-en="al. Mickiewicza 9a, 31-120 Kraków, Poland">al. Mickiewicza 9a, 31-120 Kraków</span>
    </div>
    <div class="contact-item">
      <span class="contact-label">ResearchGate</span>
      <span class="contact-value"><a href="https://www.researchgate.net" target="_blank" rel="noopener">researchgate.net/profile/…</a></span>
    </div>
  </div>
</section>

<footer>
  <span data-pl="© 2025 Anna Kowalska · Wszelkie prawa zastrzeżone"
        data-en="© 2025 Anna Kowalska · All rights reserved">
    © 2025 Anna Kowalska · Wszelkie prawa zastrzeżone
  </span>
</footer>

<script>
  function setLang(lang) {
    document.documentElement.lang = lang;
    document.querySelectorAll('[data-pl][data-en]').forEach(el => {
      el.textContent = el.dataset[lang];
    });
    document.getElementById('btn-pl').classList.toggle('active', lang === 'pl');
    document.getElementById('btn-en').classList.toggle('active', lang === 'en');
    localStorage.setItem('lang', lang);
  }

  const saved = localStorage.getItem('lang');
  if (saved && saved !== 'pl') setLang(saved);

  document.querySelectorAll('a[href^="#"]').forEach(a => {
    a.addEventListener('click', e => {
      const t = document.querySelector(a.getAttribute('href'));
      if (t) { e.preventDefault(); t.scrollIntoView({ behavior: 'smooth', block: 'start' }); }
    });
  });
</script>

</body>
</html>
