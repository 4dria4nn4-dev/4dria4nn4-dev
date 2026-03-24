
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
