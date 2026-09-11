fivestarbarber
<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <title>FIVE STAR BARBERS — Katowice</title>
  <meta
    name="description"
    content="FIVE STAR BARBERS Katowice — precyzyjne strzyżenie, broda i najwyższy standard barberingu."
  />

  <style>
    :root {
      --black: #090909;
      --black-2: #111111;
      --black-3: #181818;
      --cream: #f2eee6;
      --muted: #aaa49b;
      --gold: #c8a66a;
      --gold-light: #e1c995;
      --line: rgba(255,255,255,.11);
      --white: #fff;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background: var(--black);
      color: var(--cream);
      font-family: Inter, Arial, sans-serif;
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: min(1180px, calc(100% - 48px));
      margin: auto;
    }

    /* NAV */

    nav {
      position: fixed;
      z-index: 50;
      top: 0;
      width: 100%;
      padding: 22px 0;
      background: linear-gradient(
        to bottom,
        rgba(0,0,0,.9),
        rgba(0,0,0,0)
      );
    }

    .nav-inner {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      font-size: 15px;
      font-weight: 800;
      letter-spacing: .22em;
    }

    .logo span {
      color: var(--gold);
    }

    .nav-links {
      display: flex;
      gap: 34px;
      font-size: 12px;
      text-transform: uppercase;
      letter-spacing: .14em;
      color: #d7d1c8;
    }

    .nav-book {
      border: 1px solid var(--gold);
      padding: 12px 18px;
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: .15em;
      color: var(--gold-light);
    }

    /* HERO */

    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      position: relative;
      overflow: hidden;
      background:
        radial-gradient(circle at 72% 45%, rgba(200,166,106,.18), transparent 30%),
        linear-gradient(120deg, #070707 20%, #151515 100%);
    }

    .hero::after {
      content: "";
      position: absolute;
      width: 620px;
      height: 620px;
      right: -160px;
      top: 15%;
      border-radius: 50%;
      border: 1px solid rgba(200,166,106,.22);
      box-shadow:
        0 0 0 80px rgba(200,166,106,.025),
        0 0 0 160px rgba(200,166,106,.018);
    }

    .hero-content {
      position: relative;
      z-index: 2;
      max-width: 760px;
      padding-top: 70px;
    }

    .eyebrow {
      display: flex;
      align-items: center;
      gap: 12px;
      color: var(--gold);
      text-transform: uppercase;
      letter-spacing: .25em;
      font-size: 11px;
      margin-bottom: 25px;
    }

    .eyebrow::before {
      content: "";
      width: 45px;
      height: 1px;
      background: var(--gold);
    }

    h1 {
      font-family: Georgia, serif;
      font-size: clamp(64px, 10vw, 138px);
      line-height: .85;
      font-weight: 400;
      letter-spacing: -.055em;
    }

    h1 strong {
      display: block;
      font-family: Inter, Arial, sans-serif;
      font-size: .43em;
      letter-spacing: .28em;
      margin-top: 24px;
      color: var(--gold-light);
      font-weight: 500;
    }

    .hero-description {
      max-width: 540px;
      margin-top: 38px;
      color: var(--muted);
      font-size: 17px;
    }

    .hero-actions {
      display: flex;
      gap: 14px;
      margin-top: 40px;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      min-height: 52px;
      padding: 0 26px;
      text-transform: uppercase;
      letter-spacing: .14em;
      font-size: 11px;
      font-weight: 700;
      transition: .3s ease;
    }

    .btn-primary {
      background: var(--gold);
      color: #090909;
    }

    .btn-primary:hover {
      background: var(--gold-light);
      transform: translateY(-2px);
    }

    .btn-outline {
      border: 1px solid var(--line);
      color: var(--cream);
    }

    .btn-outline:hover {
      border-color: var(--gold);
      color: var(--gold-light);
    }

    /* STATS */

    .stats {
      border-top: 1px solid var(--line);
      border-bottom: 1px solid var(--line);
      padding: 26px 0;
      background: #0c0c0c;
    }

    .stats-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
    }

    .stat {
      text-align: center;
      border-right: 1px solid var(--line);
    }

    .stat:last-child {
      border: 0;
    }

    .stat strong {
      display: block;
      color: var(--gold-light);
      font-family: Georgia, serif;
      font-size: 29px;
      font-weight: 400;
    }

    .stat span {
      color: var(--muted);
      font-size: 10px;
      text-transform: uppercase;
      letter-spacing: .2em;
    }

    /* SECTIONS */

    section {
      padding: 120px 0;
    }

    .section-label {
      color: var(--gold);
      text-transform: uppercase;
      letter-spacing: .22em;
      font-size: 10px;
      margin-bottom: 16px;
    }

    .section-title {
      font-family: Georgia, serif;
      font-size: clamp(42px, 6vw, 76px);
      line-height: .98;
      font-weight: 400;
      max-width: 700px;
    }

    /* SERVICES */

    .services {
      background: var(--cream);
      color: var(--black);
    }

    .services .section-label {
      color: #8c6c39;
    }

    .service-grid {
      margin-top: 60px;
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 1px;
      background: rgba(0,0,0,.15);
    }

    .service {
      background: var(--cream);
      padding: 45px;
      min-height: 240px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }

    .service-number {
      font-size: 11px;
      color: #8d877e;
      letter-spacing: .2em;
    }

    .service h3 {
      font-family: Georgia, serif;
      font-size: 31px;
      font-weight: 400;
    }

    .service p {
      color: #777168;
      max-width: 420px;
    }

    .service-price {
      font-size: 24px;
      color: #9b773d;
      margin-top: 25px;
    }

    /* MANIFEST */

    .manifest {
      background: var(--black-2);
    }

    .manifest-inner {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 100px;
      align-items: center;
    }

    .manifest-copy {
      color: var(--muted);
      font-size: 18px;
      max-width: 500px;
    }

    .manifest-copy p + p {
      margin-top: 22px;
    }

    .quote-mark {
      font-family: Georgia, serif;
      color: var(--gold);
      font-size: 100px;
      line-height: .4;
      margin-bottom: 25px;
    }

    /* REVIEWS */

    .reviews {
      background: #0c0c0c;
    }

    .review-grid {
      margin-top: 60px;
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .review {
      border: 1px solid var(--line);
      padding: 35px;
      min-height: 280px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }

    .stars {
      color: var(--gold);
      letter-spacing: 4px;
    }

    .review p {
      font-family: Georgia, serif;
      font-size: 22px;
      line-height: 1.35;
    }

    .review-author {
      color: var(--muted);
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: .15em;
    }

    /* GALLERY */

    .gallery {
      background: var(--black);
    }

    .gallery-grid {
      margin-top: 60px;
      display: grid;
      grid-template-columns: 1.3fr .7fr .9fr;
      grid-template-rows: 260px 260px;
      gap: 12px;
    }

    .gallery-item {
      position: relative;
      overflow: hidden;
      background:
        linear-gradient(
          135deg,
          #292929,
          #111
        );
    }

    .gallery-item::before {
      content: "FIVE STAR";
      position: absolute;
      left: 25px;
      bottom: 22px;
      color: rgba(255,255,255,.7);
      letter-spacing: .28em;
      font-size: 10px;
    }

    .gallery-item:nth-child(1) {
      grid-row: span 2;
      background:
        radial-gradient(circle at 50% 35%, #c7a878 0 5%, transparent 6%),
        linear-gradient(135deg,#171717,#36302a,#0b0b0b);
    }

    .gallery-item:nth-child(2) {
      background:
        linear-gradient(135deg,#242424,#121212);
    }

    .gallery-item:nth-child(3) {
      background:
        linear-gradient(135deg,#332c23,#151515);
    }

    .gallery-item:nth-child(4) {
      background:
        linear-gradient(135deg,#141414,#272727);
    }

    /* CONTACT */

    .contact {
      background: var(--cream);
      color: var(--black);
    }

    .contact-grid {
      margin-top: 55px;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 70px;
    }

    .contact-item {
      padding: 24px 0;
      border-bottom: 1px solid rgba(0,0,0,.15);
    }

    .contact-item span {
      display: block;
      color: #8b857d;
      text-transform: uppercase;
      font-size: 10px;
      letter-spacing: .2em;
      margin-bottom: 8px;
    }

    .contact-item strong {
      font-family: Georgia, serif;
      font-size: 25px;
      font-weight: 400;
    }

    .hours {
      margin-top: 20px;
    }

    .hours-row {
      display: flex;
      justify-content: space-between;
      padding: 11px 0;
      border-bottom: 1px solid rgba(0,0,0,.1);
      font-size: 14px;
    }

    /* CTA */

    .final-cta {
      text-align: center;
      padding: 150px 20px;
      background:
        radial-gradient(circle at center, rgba(200,166,106,.16), transparent 38%),
        #090909;
    }

    .final-cta h2 {
      font-family: Georgia, serif;
      font-size: clamp(45px, 7vw, 90px);
      font-weight: 400;
      line-height: .95;
    }

    .final-cta p {
      color: var(--muted);
      margin: 25px auto 35px;
      max-width: 500px;
    }

    /* FOOTER */

    footer {
      padding: 30px 0;
      border-top: 1px solid var(--line);
      color: #777;
      font-size: 11px;
    }

    .footer-inner {
      display: flex;
      justify-content: space-between;
    }

    /* MOBILE */

    @media (max-width: 800px) {

      .container {
        width: min(100% - 32px, 600px);
      }

      .nav-links {
        display: none;
      }

      .nav-book {
        padding: 10px 13px;
      }

      .hero {
        min-height: 850px;
      }

      h1 {
        font-size: 64px;
      }

      .hero-description {
        font-size: 15px;
      }

      .hero-actions {
        flex-direction: column;
      }

      .btn {
        width: 100%;
      }

      .stats-grid {
        grid-template-columns: 1fr;
        gap: 25px;
      }

      .stat {
        border-right: 0;
      }

      section {
        padding: 85px 0;
      }

      .service-grid,
      .review-grid,
      .manifest-inner,
      .contact-grid {
        grid-template-columns: 1fr;
      }

      .manifest-inner {
        gap: 45px;
      }

      .review-grid {
        gap: 12px;
      }

      .gallery-grid {
        grid-template-columns: 1fr 1fr;
        grid-template-rows: 220px 220px 220px;
      }

      .gallery-item:nth-child(1) {
        grid-row: span 2;
      }

      .footer-inner {
        flex-direction: column;
        gap: 10px;
      }
    }
  </style>
</head>

<body>

  <nav>
    <div class="container nav-inner">
      <a class="logo" href="#">FIVE <span>★</span> STAR</a>

      <div class="nav-links">
        <a href="#uslugi">Usługi</a>
        <a href="#opinie">Opinie</a>
        <a href="#kontakt">Kontakt</a>
      </div>

      <!-- Podłącz tutaj właściwy link Booksy -->
      <a class="nav-book" href="#rezerwacja">Rezerwacja</a>
    </div>
  </nav>

  <main>

    <!-- HERO -->
    <section class="hero">
      <div class="container">
        <div class="hero-content">

          <div class="eyebrow">
            Barber Shop · Katowice
          </div>

          <h1>
            FIVE STAR
            <strong>BARBERS</strong>
          </h1>

          <p class="hero-description">
            Precyzyjne strzyżenie. Dopasowany styl.
            Najwyższy standard barberingu w Katowicach.
          </p>

          <div class="hero-actions">
            <a href="#rezerwacja" class="btn btn-primary">
              Zarezerwuj wizytę
            </a>

            <a href="#uslugi" class="btn btn-outline">
              Zobacz usługi
            </a>
          </div>

        </div>
      </div>
    </section>

    <!-- STATS -->
    <div class="stats">
      <div class="container stats-grid">

        <div class="stat">
          <strong>5.0 ★</strong>
          <span>Ocena klientów</span>
        </div>

        <div class="stat">
          <strong>1800+</strong>
          <span>Opinii na Booksy</span>
        </div>

        <div class="stat">
          <strong>100%</strong>
          <span>Skupienia na detalu</span>
        </div>

      </div>
    </div>

    <!-- SERVICES -->
    <section class="services" id="uslugi">
      <div class="container">

        <div class="section-label">01 / Usługi</div>

        <h2 class="section-title">
          Dobre cięcie zaczyna się
          od właściwego detalu.
        </h2>

        <div class="service-grid">

          <article class="service">
            <span class="service-number">01</span>

            <div>
              <h3>Haircut</h3>
              <p>
                Precyzyjne strzyżenie dopasowane do kształtu
                głowy, twarzy i Twojego stylu.
              </p>
            </div>

            <div class="service-price">
              100 zł · 30 min
            </div>
          </article>

          <article class="service">
            <span class="service-number">02</span>

            <div>
              <h3>Haircut + Beard</h3>
              <p>
                Kompletna stylizacja włosów i zarostu.
                Jeden spójny look, dopracowany w każdym szczególe.
              </p>
            </div>

            <div class="service-price">
              150 zł · 60 min
            </div>
          </article>

        </div>

      </div>
    </section>

    <!-- MANIFEST -->
    <section class="manifest">
      <div class="container manifest-inner">

        <div>
          <div class="section-label">02 / Filozofia</div>

          <h2 class="section-title">
            Nie chodzi tylko
            o fryzurę.
          </h2>
        </div>

        <div class="manifest-copy">

          <div class="quote-mark">“</div>

          <p>
            Chodzi o moment, w którym patrzysz w lustro
            i dokładnie wiesz, że to jest Twój styl.
          </p>

          <p>
            FIVE STAR BARBERS to precyzja, doświadczenie
            i atmosfera, do której chce się wracać.
          </p>

        </div>

      </div>
    </section>

    <!-- REVIEWS -->
    <section class="reviews" id="opinie">
      <div class="container">

        <div class="section-label">03 / Opinie</div>

        <h2 class="section-title">
          Klienci mówią
          za nas.
        </h2>

        <div class="review-grid">

          <article class="review">
            <div class="stars">★★★★★</div>

            <p>
              „Marcin to świetny barber! Już od kilku lat
              chodzę tylko do niego.”
            </p>

            <span class="review-author">
              Łukasz · Booksy
            </span>
          </article>

          <article class="review">
            <div class="stars">★★★★★</div>

            <p>
              „Dobra atmosfera, dobre cięcie.”
            </p>

            <span class="review-author">
              Paweł · Booksy
            </span>
          </article>

          <article class="review">
            <div class="stars">★★★★★</div>

            <p>
              „Strzyżenie jak zawsze na najwyższym poziomie.”
            </p>

            <span class="review-author">
              Michał · Booksy
            </span>
          </article>

        </div>

      </div>
    </section>

    <!-- GALLERY -->
    <section class="gallery">
      <div class="container">

        <div class="section-label">04 / Atmosfera</div>

        <h2 class="section-title">
          Styl zaczyna się
          jeszcze przed fotelem.
        </h2>

        <!--
          W tych polach można później podmienić tła
          na prawdziwe zdjęcia salonu i realizacji.
        -->

        <div class="gallery-grid">

          <div class="gallery-item"></div>
          <div class="gallery-item"></div>
          <div class="gallery-item"></div>
          <div class="gallery-item"></div>

        </div>

      </div>
    </section>

    <!-- CONTACT -->
    <section class="contact" id="kontakt">
      <div class="container">

        <div class="section-label">05 / Kontakt</div>

        <h2 class="section-title">
          Widzimy się
          w Katowicach.
        </h2>

        <div class="contact-grid">

          <div>

            <div class="contact-item">
              <span>Adres</span>
              <strong>
                Zadole 15<br>
                40-719 Katowice
              </strong>
            </div>

            <div class="contact-item">
              <span>Telefon</span>
              <strong>
                +48 797 351 112
              </strong>
            </div>

            <div class="contact-item">
              <span>Godziny</span>
              <strong>
                Dziś 10:00 – 20:00
              </strong>
            </div>

          </div>

          <div>

            <p style="color:#777; margin-bottom:20px;">
              Aktualny grafik i dostępne terminy
              sprawdzisz podczas rezerwacji online.
            </p>

            <a
              href="#rezerwacja"
              class="btn btn-primary"
            >
              Sprawdź dostępne terminy
            </a>

            <div class="hours">

              <div class="hours-row">
                <span>Aktualny grafik</span>
                <strong>Booksy</strong>
              </div>

              <div class="hours-row">
                <span>Miasto</span>
                <strong>Katowice</strong>
              </div>

            </div>

          </div>

        </div>

      </div>
    </section>

    <!-- FINAL CTA -->
    <section class="final-cta" id="rezerwacja">

      <div class="container">

        <div class="section-label">
          FIVE STAR EXPERIENCE
        </div>

        <h2>
          Twój następny
          najlepszy look.
        </h2>

        <p>
          Zarezerwuj termin i oddaj swój styl
          w ręce barbera.
        </p>

        <!-- Podłącz tutaj właściwy link Booksy -->
        <a href="#" class="btn btn-primary">
          Zarezerwuj wizytę
        </a>

      </div>

    </section>

  </main>

  <footer>
    <div class="container footer-inner">

      <span>
        © FIVE STAR BARBERS · Katowice
      </span>

      <span>
        Zadole 15 · 40-719 Katowice
      </span>

    </div>
  </footer>

</body>
</html>
