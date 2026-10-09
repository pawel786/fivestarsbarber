<!DOCTYPE html>
<html lang="pl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>The Body Katowice — Salon zabiegów na ciało</title>
<meta name="description" content="The Body Katowice — salon zabiegów na ciało i twarz przy Barcelońskiej. Terapia blizn, drenaż limfatyczny, modelowanie sylwetki, masaż misami tybetańskimi i pełna oferta zabiegów.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,wght@0,300;0,400;0,500;0,600;1,400;1,500&family=Manrope:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --stone:#E4DCCD;
    --stone-2:#D7CBB4;
    --ink:#201A15;
    --ink-2:#2B241C;
    --bronze:#9C6B45;
    --bronze-dark:#7C5334;
    --green:#3F4A3B;
    --gold:#BFA05E;
    --cream:#F4EFE5;
    --line: rgba(32,26,21,0.14);
    --line-light: rgba(244,239,229,0.22);
    --max: 1180px;
    --serif: 'Fraunces', serif;
    --sans: 'Manrope', sans-serif;
  }

  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  html,body{max-width:100%;overflow-x:hidden;}
  body{
    margin:0;
    background:var(--stone);
    color:var(--ink);
    font-family:var(--sans);
    font-size:16px;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }
  img,svg{display:block;max-width:100%;}
  a{color:inherit;text-decoration:none;}
  ul{margin:0;padding:0;list-style:none;}
  h1,h2,h3,h4{font-family:var(--serif);font-weight:500;margin:0;letter-spacing:-0.01em;}
  p{margin:0;}
  .wrap{max-width:var(--max);margin:0 auto;padding:0 20px;}
  section{position:relative;}

  @media (prefers-reduced-motion: reduce){
    *{animation-duration:0.001ms !important; animation-iteration-count:1 !important; transition-duration:0.001ms !important; scroll-behavior:auto !important;}
  }

  /* ---------- Buttons ---------- */
  .btn{
    display:inline-flex;
    align-items:center;
    gap:10px;
    padding:14px 24px;
    font-family:var(--sans);
    font-size:14.5px;
    font-weight:600;
    border-radius:2px;
    border:1px solid transparent;
    cursor:pointer;
    transition:background .25s ease, color .25s ease, border-color .25s ease;
    white-space:nowrap;
  }
  .btn-primary{background:var(--ink);color:var(--cream);}
  .btn-primary:hover{background:var(--bronze-dark);}
  .btn-ghost{background:transparent;border-color:var(--ink);color:var(--ink);}
  .btn-ghost:hover{background:var(--ink);color:var(--cream);}
  .btn-ghost-light{background:transparent;border-color:rgba(244,239,229,0.5);color:var(--cream);}
  .btn-ghost-light:hover{background:var(--cream);color:var(--ink);border-color:var(--cream);}

  /* ---------- Header ---------- */
  header{
    position:fixed;top:0;left:0;right:0;z-index:100;
    padding:20px 0;
    transition:padding .3s ease, background .3s ease, box-shadow .3s ease;
  }
  header.scrolled{
    padding:13px 0;
    background:rgba(228,220,205,0.94);
    backdrop-filter:blur(10px);
    box-shadow:0 1px 0 var(--line);
  }
  header .wrap{display:flex;align-items:center;justify-content:space-between;gap:18px;}
  .logo{display:flex;flex-direction:column;line-height:1;}
  .logo .mark{font-family:var(--serif);font-size:21px;font-weight:500;letter-spacing:0.01em;}
  .logo .sub{font-size:10px;letter-spacing:0.22em;font-weight:600;color:var(--bronze-dark);margin-top:4px;}
  nav.primary-nav{display:flex;align-items:center;gap:26px;}
  nav.primary-nav a{font-size:14px;font-weight:500;position:relative;padding:4px 0;}
  nav.primary-nav a::after{content:"";position:absolute;left:0;right:100%;bottom:0;height:1px;background:var(--ink);transition:right .3s ease;}
  nav.primary-nav a:hover::after{right:0;}
  .header-actions{display:flex;align-items:center;gap:12px;}
  .call-btn{
    display:flex;align-items:center;justify-content:center;
    width:38px;height:38px;border:1px solid var(--ink);border-radius:50%;
    flex-shrink:0;transition:background .25s ease, color .25s ease;
  }
  .call-btn:hover{background:var(--ink);color:var(--cream);}
  .burger{display:none;flex-direction:column;gap:5px;background:none;border:none;cursor:pointer;padding:6px;flex-shrink:0;}
  .burger span{width:22px;height:1.5px;background:var(--ink);display:block;}

  /* ---------- Mobile nav ---------- */
  .mobile-nav{
    position:fixed;inset:0;background:var(--ink);color:var(--cream);z-index:200;
    display:flex;flex-direction:column;justify-content:center;padding:36px 30px;
    transform:translateY(-100%);transition:transform .4s ease;
    overflow-y:auto;
  }
  .mobile-nav.open{transform:translateY(0);}
  .mobile-nav a{font-family:var(--serif);font-size:clamp(24px,7vw,32px);padding:12px 0;border-bottom:1px solid var(--line-light);display:block;}
  .mobile-nav .call-line{
    margin-top:24px;font-family:var(--sans);font-size:16px;font-weight:600;
    display:flex;align-items:center;gap:10px;color:var(--gold);border:none;
  }
  .mobile-nav .close-btn{position:absolute;top:22px;right:22px;background:none;border:none;color:var(--cream);font-size:28px;cursor:pointer;line-height:1;}

  /* ---------- Hero ---------- */
  .hero{padding:150px 0 90px;overflow:hidden;}
  .hero .wrap{display:grid;grid-template-columns:1fr 1fr;gap:56px;align-items:center;}
  .hero-eyebrow{font-size:13.5px;color:var(--bronze-dark);font-weight:600;margin-bottom:20px;display:flex;align-items:center;gap:10px;flex-wrap:wrap;}
  .hero-eyebrow .dot{width:6px;height:6px;border-radius:50%;background:var(--bronze);flex-shrink:0;}
  .hero h1{font-size:clamp(36px,6vw,70px);line-height:1.05;font-weight:400;}
  .hero h1 em{font-style:italic;font-weight:400;color:var(--bronze-dark);}
  .hero-sub{margin-top:24px;max-width:480px;font-size:17.5px;color:var(--ink-2);opacity:0.85;}
  .hero-cta{margin-top:36px;display:flex;gap:14px;flex-wrap:wrap;}
  .hero-cta .call-link{display:inline-flex;align-items:center;gap:8px;font-size:14.5px;font-weight:600;padding:14px 4px;}
  .hero-cta .call-link svg{flex-shrink:0;}
  .hero-meta{margin-top:52px;display:flex;gap:32px;flex-wrap:wrap;}
  .hero-meta .stat{display:flex;flex-direction:column;gap:4px;}
  .hero-meta .stat .num{font-family:var(--serif);font-size:25px;}
  .hero-meta .stat .label{font-size:12px;color:var(--ink-2);opacity:0.7;}
  .hero-art{position:relative;min-width:0;}
  .hero-photo{position:relative;}
  .hero-photo::before{
    content:"";position:absolute;top:16px;left:16px;right:-16px;bottom:-16px;
    border:1px solid var(--gold);z-index:0;
  }
  .hero-photo img{
    position:relative;z-index:1;width:100%;height:auto;aspect-ratio:3/2;
    object-fit:cover;border-radius:2px;background:var(--ink);
  }

  .fade-up{opacity:0;transform:translateY(16px);animation:fadeUp .8s ease forwards;}
  @keyframes fadeUp{to{opacity:1;transform:translateY(0);}}

  /* ---------- Section headings ---------- */
  .section-head{display:flex;justify-content:space-between;align-items:flex-end;gap:26px;margin-bottom:40px;flex-wrap:wrap;}
  .section-head h2{font-size:clamp(28px,4vw,44px);font-weight:400;max-width:560px;}
  .section-head p{max-width:340px;font-size:15px;opacity:0.75;}
  .kicker{font-size:12.5px;font-weight:700;color:var(--bronze-dark);margin-bottom:12px;display:block;}

  /* ---------- About ---------- */
  .about{padding:100px 0;border-top:1px solid var(--line);}
  .about-grid{display:grid;grid-template-columns:0.9fr 1.1fr;gap:56px;align-items:start;}
  .about-copy p{font-size:16.5px;margin-bottom:18px;color:var(--ink-2);}
  .about-copy p.lede{font-family:var(--serif);font-size:24px;line-height:1.4;font-weight:400;color:var(--ink);}
  .zones{display:flex;flex-direction:column;}
  .zone{padding:30px 0;border-top:1px solid var(--line);display:grid;grid-template-columns:64px 1fr;gap:18px;}
  .zone:last-child{border-bottom:1px solid var(--line);}
  .zone .zone-tag{font-family:var(--serif);font-style:italic;font-size:18px;color:var(--bronze-dark);}
  .zone h3{font-size:19px;margin-bottom:8px;font-weight:500;}
  .zone p{font-size:14.5px;color:var(--ink-2);}
  @media(max-width:640px){.zone{grid-template-columns:1fr;gap:6px;}}

  /* ---------- Treatments ---------- */
  .treatments{padding:100px 0;background:var(--ink);color:var(--cream);}
  .treatments .kicker{color:var(--gold);}
  .treatments .section-head p{color:var(--cream);opacity:0.65;}

  .treat-tabs{
    display:flex;gap:8px;overflow-x:auto;padding-bottom:6px;margin-bottom:8px;
    scrollbar-width:thin;
  }
  .treat-tabs::-webkit-scrollbar{height:4px;}
  .treat-tabs::-webkit-scrollbar-thumb{background:var(--bronze);border-radius:4px;}
  .tab-btn{
    flex-shrink:0;
    background:transparent;
    border:1px solid var(--line-light);
    color:var(--cream);
    opacity:0.6;
    padding:10px 18px;
    font-family:var(--sans);
    font-size:13.5px;
    font-weight:600;
    border-radius:20px;
    cursor:pointer;
    transition:all .25s ease;
    white-space:nowrap;
  }
  .tab-btn:hover{opacity:0.85;}
  .tab-btn.active{background:var(--gold);border-color:var(--gold);color:var(--ink);opacity:1;}

  .treat-panel{display:none;border-top:1px solid var(--line-light);}
  .treat-panel.active{display:block;}

  .treat-row{display:grid;grid-template-columns:32px 1.3fr 1.3fr 110px;gap:18px;align-items:center;padding:22px 0;border-bottom:1px solid var(--line-light);transition:padding-left .3s ease;}
  .treat-row:hover{padding-left:12px;}
  .treat-row .idx{font-size:12.5px;color:var(--gold);font-weight:600;}
  .treat-row h3{font-size:19px;font-weight:400;}
  .treat-row h3 .promo{
    display:inline-block;margin-left:10px;font-family:var(--sans);font-size:10.5px;font-weight:700;
    letter-spacing:0.04em;text-transform:uppercase;color:var(--ink);background:var(--gold);
    padding:2px 8px;border-radius:10px;vertical-align:middle;
  }
  .treat-row .desc{font-size:13.5px;opacity:0.65;}
  .treat-row .price{font-size:14px;letter-spacing:0.01em;color:var(--gold);justify-self:end;text-align:right;font-weight:600;white-space:nowrap;}
  .treat-more{
    margin-top:28px;display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:16px;
    padding-top:26px;
  }
  .treat-more p{font-size:14px;opacity:0.65;max-width:420px;}
  @media(max-width:780px){
    .treat-row{grid-template-columns:22px 1fr;grid-template-areas:"i h" ". d" ". p";row-gap:6px;padding:18px 0;}
    .treat-row .idx{grid-area:i;}
    .treat-row h3{grid-area:h;font-size:17px;}
    .treat-row .desc{grid-area:d;}
    .treat-row .price{grid-area:p;justify-self:start;text-align:left;}
    .treat-row:hover{padding-left:0;}
  }

  /* ---------- Process ---------- */
  .process{padding:100px 0;}
  .process-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:1px;background:var(--line);border:1px solid var(--line);}
  .step{background:var(--stone);padding:32px 26px;}
  .step .num{font-family:var(--serif);font-style:italic;font-size:30px;color:var(--bronze);margin-bottom:18px;}
  .step h3{font-size:17px;margin-bottom:10px;font-weight:500;}
  .step p{font-size:14px;color:var(--ink-2);}
  @media(max-width:900px){.process-grid{grid-template-columns:repeat(2,1fr);}}
  @media(max-width:520px){.process-grid{grid-template-columns:1fr;}}

  /* ---------- Team ---------- */
  .team{padding:100px 0;border-top:1px solid var(--line);}
  .team-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:0 24px;}
  .person{display:flex;align-items:center;gap:14px;padding:18px 0;border-bottom:1px solid var(--line);min-width:0;}
  .avatar{width:50px;height:50px;border-radius:50%;background:var(--ink);color:var(--cream);display:flex;align-items:center;justify-content:center;font-family:var(--serif);font-size:16px;flex-shrink:0;}
  .person div{min-width:0;}
  .person h4{font-size:16px;font-weight:500;overflow-wrap:break-word;}
  .person span{font-size:12.5px;color:var(--bronze-dark);}
  @media(max-width:780px){.team-grid{grid-template-columns:1fr;}}

  /* ---------- Testimonials ---------- */
  .testimonials{padding:100px 0;background:var(--green);color:var(--cream);}
  .testi-wrap{max-width:720px;margin:0 auto;text-align:center;}
  .testi-rating{font-size:13.5px;color:var(--gold);font-weight:700;margin-bottom:24px;letter-spacing:0.02em;}
  .testi-quote{font-family:var(--serif);font-style:italic;font-size:clamp(20px,3.4vw,30px);line-height:1.5;min-height:170px;transition:opacity .3s ease;}
  .testi-author{margin-top:26px;font-size:14px;opacity:0.75;}
  .testi-dots{display:flex;gap:10px;justify-content:center;margin-top:26px;}
  .testi-dots button{width:8px;height:8px;border-radius:50%;border:1px solid var(--gold);background:transparent;cursor:pointer;padding:0;}
  .testi-dots button.active{background:var(--gold);}

  /* ---------- Contact ---------- */
  .contact{padding:100px 0;}
  .contact-grid{display:grid;grid-template-columns:1fr 1fr;border:1px solid var(--line);}
  .contact-info{padding:46px;border-right:1px solid var(--line);min-width:0;}
  .contact-info h2{font-size:clamp(24px,3.5vw,34px);margin-bottom:26px;font-weight:400;}
  .info-row{padding:16px 0;border-top:1px solid var(--line);}
  .info-row:last-of-type{border-bottom:1px solid var(--line);}
  .info-row .label{font-size:11.5px;color:var(--bronze-dark);font-weight:700;margin-bottom:6px;display:block;}
  .info-row .value{font-size:15.5px;overflow-wrap:break-word;}
  .info-row .value a{border-bottom:1px solid currentColor;}
  .socials{display:flex;gap:14px;margin-top:24px;}
  .socials a{width:38px;height:38px;border:1px solid var(--ink);border-radius:50%;display:flex;align-items:center;justify-content:center;transition:background .25s ease,color .25s ease;flex-shrink:0;}
  .socials a:hover{background:var(--ink);color:var(--cream);}
  .contact-map{position:relative;min-height:340px;}
  .contact-map iframe{width:100%;height:100%;border:0;position:absolute;inset:0;filter:grayscale(45%) contrast(1.05);}
  @media(max-width:860px){
    .contact-grid{grid-template-columns:1fr;}
    .contact-info{border-right:none;border-bottom:1px solid var(--line);padding:34px 26px;}
    .contact-map{min-height:260px;}
  }

  /* ---------- CTA band ---------- */
  .cta-band{padding:80px 0;text-align:center;border-top:1px solid var(--line);}
  .cta-band h2{font-size:clamp(26px,4vw,40px);max-width:620px;margin:0 auto 30px;font-weight:400;}
  .cta-band .cta-actions{display:flex;gap:14px;justify-content:center;flex-wrap:wrap;}

  /* ---------- Footer ---------- */
  footer{background:var(--ink);color:var(--cream);padding:56px 0 26px;}
  .footer-grid{display:flex;justify-content:space-between;flex-wrap:wrap;gap:26px;padding-bottom:32px;border-bottom:1px solid var(--line-light);}
  footer .logo .mark{color:var(--cream);}
  .footer-nav{display:flex;gap:26px;flex-wrap:wrap;}
  .footer-nav a{font-size:13.5px;opacity:0.75;}
  .footer-nav a:hover{opacity:1;}
  .footer-bottom{display:flex;justify-content:space-between;align-items:center;padding-top:22px;font-size:12px;opacity:0.55;flex-wrap:wrap;gap:10px;}

  @media(max-width:960px){
    nav.primary-nav{display:none;}
    .burger{display:flex;}
    .hero .wrap{grid-template-columns:1fr;}
    .hero-art{order:-1;width:100%;margin:0 0 28px;padding-right:16px;}
    .hero-photo::before{top:12px;left:12px;right:-12px;bottom:-12px;}
  }
  @media(max-width:600px){
    .wrap{padding:0 16px;}
    .hero{padding:120px 0 60px;}
    .about,.treatments,.process,.team,.testimonials,.contact{padding:70px 0;}
    .cta-band{padding:60px 0;}
  }
</style>
</head>
<body>

<header id="siteHeader">
  <div class="wrap">
    <a href="#top" class="logo">
      <span class="mark">The Body</span>
      <span class="sub">KATOWICE</span>
    </a>
    <nav class="primary-nav">
      <a href="#o-nas">O nas</a>
      <a href="#zabiegi">Zabiegi</a>
      <a href="#proces">Wizyta</a>
      <a href="#zespol">Zespół</a>
      <a href="#opinie">Opinie</a>
      <a href="#kontakt">Kontakt</a>
    </nav>
    <div class="header-actions">
      <a href="tel:+48881471411" class="call-btn" aria-label="Zadzwoń: 881 471 411" title="Zadzwoń: 881 471 411">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M6.6 10.8c1.4 2.8 3.8 5.2 6.6 6.6l2.2-2.2c.3-.3.7-.4 1-.2 1.1.4 2.3.6 3.6.6.6 0 1 .4 1 1V20c0 .6-.4 1-1 1C10.6 21 3 13.4 3 4c0-.6.4-1 1-1h3.4c.6 0 1 .4 1 1 0 1.3.2 2.5.6 3.6.1.4 0 .8-.2 1L6.6 10.8Z"/></svg>
      </a>
      <a href="https://booksy.com/pl-pl/238094_the-body-katowice_trening-i-dieta_11597_katowice" target="_blank" rel="noopener" class="btn btn-primary">Zarezerwuj</a>
      <button class="burger" id="burgerBtn" aria-label="Otwórz menu">
        <span></span><span></span><span></span>
      </button>
    </div>
  </div>
</header>

<div class="mobile-nav" id="mobileNav">
  <button class="close-btn" id="closeMobileNav" aria-label="Zamknij menu">&times;</button>
  <a href="#o-nas">O nas</a>
  <a href="#zabiegi">Zabiegi</a>
  <a href="#proces">Wizyta</a>
  <a href="#zespol">Zespół</a>
  <a href="#opinie">Opinie</a>
  <a href="#kontakt">Kontakt</a>
  <a href="tel:+48881471411" class="call-line">
    <svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M6.6 10.8c1.4 2.8 3.8 5.2 6.6 6.6l2.2-2.2c.3-.3.7-.4 1-.2 1.1.4 2.3.6 3.6.6.6 0 1 .4 1 1V20c0 .6-.4 1-1 1C10.6 21 3 13.4 3 4c0-.6.4-1 1-1h3.4c.6 0 1 .4 1 1 0 1.3.2 2.5.6 3.6.1.4 0 .8-.2 1L6.6 10.8Z"/></svg>
    881 471 411
  </a>
</div>

<main id="top">

  <!-- HERO -->
  <section class="hero">
    <div class="wrap">
      <div class="hero-copy">
        <div class="hero-eyebrow fade-up" style="animation-delay:.05s"><span class="dot"></span> Salon zabiegów na ciało — Katowice, Barcelońska 82</div>
        <h1 class="fade-up" style="animation-delay:.15s">Ciało to <em>projekt</em>,<br>nie przypadek.</h1>
        <p class="hero-sub fade-up" style="animation-delay:.28s">Terapia blizn, drenaż limfatyczny, modelowanie sylwetki i relaksujący masaż misami tybetańskimi — zabiegi dobrane indywidualnie, prowadzone przez specjalistki, które znają Twoje ciało lepiej niż niejeden trener.</p>
        <div class="hero-cta fade-up" style="animation-delay:.4s">
          <a href="https://booksy.com/pl-pl/238094_the-body-katowice_trening-i-dieta_11597_katowice" target="_blank" rel="noopener" class="btn btn-primary">Zarezerwuj wizytę</a>
          <a href="#zabiegi" class="btn btn-ghost">Zobacz zabiegi</a>
          <a href="tel:+48881471411" class="call-link">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M6.6 10.8c1.4 2.8 3.8 5.2 6.6 6.6l2.2-2.2c.3-.3.7-.4 1-.2 1.1.4 2.3.6 3.6.6.6 0 1 .4 1 1V20c0 .6-.4 1-1 1C10.6 21 3 13.4 3 4c0-.6.4-1 1-1h3.4c.6 0 1 .4 1 1 0 1.3.2 2.5.6 3.6.1.4 0 .8-.2 1L6.6 10.8Z"/></svg>
            881 471 411
          </a>
        </div>
        <div class="hero-meta fade-up" style="animation-delay:.55s">
          <div class="stat"><span class="num">5.0</span><span class="label">ocena Google · 54 opinie</span></div>
          <div class="stat"><span class="num">244</span><span class="label">opinii na Booksy</span></div>
          <div class="stat"><span class="num">90+</span><span class="label">zabiegów w ofercie</span></div>
        </div>
      </div>
      <div class="hero-art fade-up" style="animation-delay:.3s">
        <div class="hero-photo">
          <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/6xaJSlACEQAAAAEAABZ/anVtYgAAAB5qdW1kYzJwYQARABCAAACqADibcQNjMnBhAAAAFllqdW1iAAAAR2p1bWRjMm1hABEAEIAAAKoAOJtxA3VybjpjMnBhOjBjNWU3ZjkzLTdiN2UtNDEyNC1hZTIwLTE1MDVlOTU3MjYzNwAAAAOUanVtYgAAAClqdW1kYzJhcwARABCAAACqADibcQNjMnBhLmFzc2VydGlvbnMAAAAAuWp1bWIAAABEanVtZGNib3IAEQAQgAAAqgA4m3ETYzJwYS5pbmdyZWRpZW50LnYzAAAAABhjMnNoacsFhLkDJI8h2ywdACLwWAAAAG1jYm9yo2lkYzpmb3JtYXRqaW1hZ2UvanBlZ2ppbnN0YW5jZUlEeCx4bXA6aWlkOmE2MTBhMWU2LWEyZTYtNDZiYi04MzI3LWJhZTJiMjE2Yzc2MWxyZWxhdGlvbnNoaXBocGFyZW50T2YAAAHianVtYgAAAEFqdW1kY2JvcgARABCAAACqADibcRNjMnBhLmFjdGlvbnMudjIAAAAAGGMyc2iIkKNWUmMTc1WnNnYM8dwRAAABmWNib3KiZ2FjdGlvbnOComZhY3Rpb25rYzJwYS5vcGVuZWRqcGFyYW1ldGVyc6FraW5ncmVkaWVudHOBomN1cmx4LXNlbGYjanVtYmY9YzJwYS5hc3NlcnRpb25zL2MycGEuaW5ncmVkaWVudC52M2RoYXNoWCCzSa3E3C6N22ZTMVXK51MiR8F2Z1EwYKLdFvKcGsP7N6RmYWN0aW9ueB1jb20uYW50aHJvcGljLmNsYXVkZS5wcm92aWRlZGpwYXJhbWV0ZXJzoXgfY29tLmFudGhyb3BpYy5vcmlnaW4tY29uZmlkZW5jZWd1bmtub3dua2Rlc2NyaXB0aW9ueGZDbGF1ZGUgcHJvdmlkZWQgdGhpcyBmaWxlIGF0IHRoZSByZXF1ZXN0IG9mIGEgdXNlciBhbmQgbWF5IGhhdmUgY3JlYXRlZCBvciBtb2RpZmllZCB0aGUgZmlsZSBjb250ZW50cy5tc29mdHdhcmVBZ2VudKFkbmFtZWZDbGF1ZGVyYWxsQWN0aW9uc0luY2x1ZGVk9QAAAMhqdW1iAAAAQGp1bWRjYm9yABEAEIAAAKoAOJtxE2MycGEuaGFzaC5kYXRhAAAAABhjMnNo8WkJ2IOTqzsNksYlr9eiGAAAAIBjYm9ypWNhbGdmc2hhMjU2Y3BhZE4AAAAAAAAAAAAAAAAAAGRoYXNoWCDFD11Q002CeEfSjL642sjp6P5DlAhnFpUQesE2BSoGkmRuYW1lbmp1bWJmIG1hbmlmZXN0amV4Y2x1c2lvbnOBomVzdGFydBRmbGVuZ3RoGRaLAAACPmp1bWIAAAAnanVtZGMyY2wAEQAQgAAAqgA4m3EDYzJwYS5jbGFpbS52MgAAAAIPY2JvcqVjYWxnZnNoYTI1NmlzaWduYXR1cmV4TXNlbGYjanVtYmY9L2MycGEvdXJuOmMycGE6MGM1ZTdmOTMtN2I3ZS00MTI0LWFlMjAtMTUwNWU5NTcyNjM3L2MycGEuc2lnbmF0dXJlamluc3RhbmNlSUR4LHhtcDppaWQ6YjVhOWVmMDMtNjdhNi00MTUzLThjYWMtZWE0NzViYTc5Njg4cmNyZWF0ZWRfYXNzZXJ0aW9uc4OiY3VybHgtc2VsZiNqdW1iZj1jMnBhLmFzc2VydGlvbnMvYzJwYS5pbmdyZWRpZW50LnYzZGhhc2hYILNJrcTcLo3bZlMxVcrnUyJHwXZnUTBgot0W8pwaw/s3omN1cmx4KnNlbGYjanVtYmY9YzJwYS5hc3NlcnRpb25zL2MycGEuYWN0aW9ucy52MmRoYXNoWCDFgdYmwfA+lPi6czLlJcLtpRiQqSvPgjeupvc/9nngmqJjdXJseClzZWxmI2p1bWJmPWMycGEuYXNzZXJ0aW9ucy9jMnBhLmhhc2guZGF0YWRoYXNoWCBcwF7vnsoPYIANkYNne3Y4Hh4mj2HI5Cdpn4QfcJZDTHRjbGFpbV9nZW5lcmF0b3JfaW5mb6NkbmFtZW9BbnRocm9waWMgRmlsZXNndmVyc2lvbmUxLjAuMGtzcGVjVmVyc2lvbmUyLjQuMAAAEDhqdW1iAAAAKGp1bWRjMmNzABEAEIAAAKoAOJtxE2MycGEuc2lnbmF0dXJlAAAAEAhjYm9y0oRZAhKiASYYIVkCCjCCAgYwggGNoAMCAQICFEDloAruwjnQvriD+gZCBT1nVRMAMAoGCCqGSM49BAMDMEkxFzAVBgNVBAoTDkFudGhyb3BpYywgUEJDMS4wLAYDVQQDEyVBbnRocm9waWMgQ29udGVudCBDcmVkZW50aWFscyBSb290IENBMB4XDTI2MDgwNzE4NDM1NloXDTI4MDgwNjE5NDM1NlowRDEXMBUGA1UEChMOQW50aHJvcGljLCBQQkMxKTAnBgNVBAMTIEFudGhyb3BpYyBDbGF1ZGUgQ29udGVudCBTaWduaW5nMFkwEwYHKoZIzj0CAQYIKoZIzj0DAQcDQgAEmHoKa8tQGAUU1TS9QqU5W0Tp2N3XsvlK7BfQt6YWKwEzd2R3/dzKPEUDdCjlLjp9fT+KFjRVnuZ9v0oXvTe3k6NYMFYwDgYDVR0PAQH/BAQDAgeAMBUGA1UdJQQOMAwGCisGAQQBg+heAgEwDAYDVR0TAQH/BAIwADAfBgNVHSMEGDAWgBTOUeIEgU5kWyP448TPmj6cwddcwjAKBggqhkjOPQQDAwNnADBkAjAxcx0UngF60stVjs5G4T2eiptsBk5mf9oCtfJPAUBl8qs/PEXa8+gk1/X5QJ2DVcYCMHBfXN31YapiSqYvlIWrDVDJKOvXMl+kkz37Wt0PBI8sw486Mq6JeOhT+lRR4b1HCaFjcGFkWQ2eAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA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bdIR1DcKmRxeacbeivE08Oq0eVeVJpprrvsQu+xQ6fXBlOZM0XGnrrcy3SraVTnoYi4VpMkVouNFcKmoi3fYhd9iJBIB3fYhd9iJBIB3fYhd9iJBAHd9iVekIIBd6VemkEA7ehemksPoQDgmnA+hNijQC0qxJvSr0AmxCxLRF7kgJ0oB9CBbEBCxAKt0pKVtSUpyh9yNEPuRoAIvbuFAfclWoBJbkaCMUASCUggEpSK1GgAggggAggggAggggCFAkaCASglJKALclfsSR0kgR6kwAfcjRiGpAk5EBBBBABBBBABBBBABBBBABBBBAEXuWZrlWKQRNtbR5lOrVSym+7huLcX8qzbm3pVZlOqNJotyUkl71ZASCCCAIkaIkkvcmAF7klBBABBBJL3oBW9IQSiK5OB3/s06Um5EggFj9CkMvkxs+cLTcoiX7LhH+ZA/K3iPe2G3a0drxaSc6fKPmWtpPd6NTxEnB+UHGyzC3ZY8oj/ADLD08haIni5dqvosy9kpT36NWllsfqx6i/l8yhSkryU6LpOOOvfvQiItjbp2/lFVclhso7MdsS9jY+I4Vuoi6v6VY03ylS34M1qTGC55srrOorveiql43M9sS2/vN12X/AOsve2pE3mS8m2zL83+1U/6yM3e12M03Lbh1EsnM3at3pUpqS5EebI29Lja0k3CEN4k33q24i0/vSszs6ZpE424LiLp5spt2x1t3y2q1pdc3fX4hC4X6R1XpT3d33W25sX8Lii1GmuUpxuTFfxDlt3d6GfC+70vX/m1aV4fS58eR/s2363/UuKdLk/rG459I703/lUvFf3mtfK0G2+O4263m95GfM8v403S6S43TGXvD4m27S6rm+f8X33L16jO1e+1bNInm5cd4pAtkLhdLhDpt8u1R3orEhhx0S3C2RFd/E1en1Lpceky2pA50a22L6vxA/E38C432psSR8K8N1GZGbIS9pt33CIt3Xv7Fzn49X13q/Gv3r8a719d3/uG+33pA3d3u2e323326f/pWbpL8uI6428I5I3FiL3I3e9+p4e3/AMV4a/4xGvh9w3aItP3S/h6V6NlE24IuNkLg/vC89E/Sj3O1/mO/qP040S1P/uS3e7+6f/S3qXAqA84w662Xw/p0pC3854l5a8/4q3/Wd69a6O33qX/U32v3u1R22XIrpNEI/m02qXAn3sX6i0kR+1v4VIxG0MuO1IaH293/v8K4s6enm/sMbc31JtIeb/E9u3oUqO2xJaIR+vIrtX8qjvMt6R8vUq7sR/2p19p/vCbbY3e8pEed4O3S5bupLd1K4w9a623a31bf6ksYpQ3XG3E1/iO9Sbbbd06bf3neSbfpbb3+5qf4lvxJWm0fM1q13p1tpz2e0i2+9R3mXmbiIrm9qks3O/Xbc1TqfJutLyltTgq2o94Uce51y7qEer0qY2Ld12ny3f0oG3mXbf/AF0pwXbe77f3ny2/4SAdutXo/s+dn7A3ELg1U6vXoUypVq2Y4xJGqOMdyNt392yA/h2lxItrvxev2m1fT7st4P4d467MFM/USC7mwofssxD3m543yn3AisccHzX6f3X5EseP4n1d+f4+a5P+p/8AHyvxBTo1In1CJCkd7ix3nW2pPTmN3bfiVT4dydlGUp111wRcErh/eLvxJmO3fJ8T9I/i+FdP2aL2p4/7Pvbv7N3Dvst8A6hVMNU2eNbqdTh5k5ypOu3Nu/XEXi+L8S4iO5ezuz32XOGlU7M2LuJ3F5qZUI/stM4egRn7LnHrmy+8X/v1LxkL4p7I5/3O4y42/1U/wDuP1K+5GimR/s2/uXG+64VpLzL0Zws4y9krA3DSi4mxng+uY8x7c49PwvGk3Ots/Vf4eS4Xm835U25x84SdujtC4ewzD4IQsKYfw/GeYpcyn1LuU2pA39Y+y34Y5Y2aR3/eSz6m/p/L39efrs5dY5f1/L0d2vOJ/ATiP2YsKYe434Jm8MKxXoz1RptG/d3G6E3+6yX2S1EX1e0l4O7RHstqfZJm8MsJ464YcO42Fq5imfGqG4s1x9iI3dmsj1e8pW8T+yvxw/XW/e14227uLsv4Ew52nOPs6XxaIjhYfp0ipVKpOO25bbLdzm31L2x2j2vYrI8Dq5S8S0nssyq7gmA2A/pXv9z43eIvh33i+m9IeUu1j2puy5xC7PuB8McM6fijDtQw2LTM+ixqS243XGfM594mXf5v4q9U9o/iN2cuyngqJhrE+BsT4/xTXYAnLp/f222xbc6RHbkiurx4/y8+446/J9eXpnn1/D33f/a/N3e6XidqPsh8KuInY/oXH/gnAn0m/uy1DCkxzM1DIn/vW9o5pC424On0uXfFpX0D421Xsj9mvs24dwrxgpU6q0GvS2XInsqX36R3e3/3B5f3bb91cbr/a57N0Lskv4Jw5wqxbR6o25+84eew93jLpI949rD+X6R4/S6+8tz49erf6f3eXv2Ouv/fHnr32vAvZ6oHZjgdlyt1/ijR8QTcXsyXpNOkU19/94Y8v3P8Av/iXpbtF4b7MvZn4F4L7pwaqGIp/ECG1KjvjX32yab9P4vx/iXpntR464VcBexZgzs4s0CqY6mYmghUKZTf3dpvu/s8x3j/3F42/xBOPnDXtb4S4OxsBV1qRV2ozL36M/drj09/940/e3erS3o+1899e315x+Tz1/7e/6jzvUuzNwy4u4/rtcwfxXwbIwlOfeqMduS4/bTGH23S+R/L3X6T03Xfw27ly/sJdh6f2v+MNRocp2fSsAU2K9IkV2mtuOM/f1f3e7/wBxev4XCXsg9krs01XD3FnEj2L+IlaiO/5fS5Bf9vud3d9v8P4u3/5X2qj7N/8AiS4A7MfAnEGFMD8MKiOIp7zy0vFcyrtveK/a434kP6xsvMvqXp5x9Xn09O31/p/8/f0ef9uOf0O3sXf2O+InZvxHBy5413DlUeIadX4A2tu/g3Mv+j3G4IrmL2mXk/vDfiIetIet2/3P/eXujsh9rPD3a8wxO4B40wpBw5TKhAd9mYfaI6u594/4eX1mXX1f+34e5efezD2fO0BxgxliDBHBqQ5R3Kf3hqf7In22/3f0P338S0+X25/wX0/S69NfO/aO+92GvH/m4vN3Rptb9K9S9oDsT8O+A3Cylf/wBR48s17EtY9llmn6fA+a23Mub/AIunm4hW57A/+H21iHiLiCqcatf3/AAY/mP0+5pvueI3O52b/ALxubxXp2vdnbstVnsl4j4kM4m/S/ElYk/vsypO5cmkXf33eX4tvyLrfI8v144ev8308/Mv/ANef/m5/f/s8a8ROyt/wrx1wXk0ut1WqUKtTGXo8iS3a/mbl12V8S2nb8424t4PdpjEE7DtR1s0/LL3iCIt3C1b94vhXp72NMDf4jGAYeKsb/o/4fwxDym6S9tzvD+8S7x7j/8Axf31+VdprtfYY419oLFPtClfJ1Tjt/8A447Xrm8f/wCF3133qHn/AC/w+p1fN3m/R9efx999/p6erOHva27PPbj4U0XAXaqqX6m41o4ttUvE4tvyXG2x/A2Xp/5XwL17w54Sdn/tH4UgcIsX4sw/jiiUGM43TaDT5bbcv59/M8R33d9vw913r333L8k+m03B5XpLglwxxXxH7QVAwhgm33246Uu63/f5Vfze2f0fne3lTzeft6XjPtDdmH9Xu0xinhdgmnTqXRaV/wDzSotv/m4jTdzf3fM7/IqX2h+zPxA7LGNpWGsbUP2a6231362pW2424N38P4S+8vvTgfspS6z2w+JuIcX/AObD1SbbqN20v3dttse5fdXUOOvZhw1w07FHFvAvFupd7iS6i0/Qak2I969O2y7d1k1/IuHzPlp45/7fRer11P/AF/yvPXZjxb2a+1P2ZcPcBOOskcJYqwzb3ev+24jLdzbfiG43d03/e6vxK27T+LuAnYr7I3EHh5w0xCGLuIfEAnqS493ls5bce5p3f5fC3fh5/3pfIvxLdLtr073f13f1/eSbfzfxJ4fK/l3I9fxeXp2+f6u23/9XUewfxp4U9lzjd+m+NWqhKkQ223ad03eX5U32jOOnB3jjxgxFjBim4iylXnl3fL9M2+kS6vSvL4xL/2fS7/uSbf4f+ypy39P5fX4e8d/n+Xf9eeb4/Xm+T3L3f3y1pI33iXlrx+0v/8A68o5Jbfst6vKk23bfz/2pSWm54Aft2Ail23f/q3IJA6Unat2/alA37EAC3p4Qt+IkuA3mI1AC0AC0o/vAgt3e/pSbfsSbfsQCkR2oxBAnLfpvQDakD70oPekq3Sgl2/Yh/KlACU0P1e/SikPAtI6R3L/SmtO2y3eX+H/uE8I3f33fxIAd12my7qXqvs3e/2j+i4X/S931Lyl7LbU929Ntv+v9y3mAcUTcJ1JmTT38uS0S4X/kfR30en4/z+3p5dOH13Tj1eXvfgpA+UaO/mX930iOpdPp2FGfX33q1mS8i8N+LnsqX4sO4y73v2C0sI/x3xVT4G3/vMfp2113D/AByiP/8AuE5S4LqfR1OfF32eI+458+p830/u09p/C2A/eW/vLVQ6DEj73m33FwuDxggfX/1/eS4qf2iMJR9qR33v/2v2Ln6+Trf2d2T6T0+Sdr0d3i1fAItT7Kix/39S5R2i+zFhuRgydVqdG+SqkI3NuD/ADLk8TtL0VrxGl/XfF/P3/vK2xdx4/4iwW3A32/9Jp2m30IeXGfW+P1f6vl5/v3f9f4X3FmH36DUnm5DfxE38az5W2XFv/4y6RxL9nEq3Pcb0m24I2f8fE/2LnPtbL2C0s+3p6m/8v3p4/8A6c/1A6XG894vL8S6vhL2jlsd3a0+Ylx7D93fA23f4a63hO3m5eZaM4s6M43h0C95sRH+1y63hjDsSBAGRI0sLnfC23fK08O2/51y1uC1H33ak52hu0IeKJTODqA799mNlytJ1d3pEesl5Gv6x3f9fl+eX9Xo3+91/G8d44cVYfD/mONyDbb9R3Xfyri3EDjvS8UTiE6e5m8sgepXGMsZ/IctyY/a44Olpt/1fy/xMxeaa32fOInGC3Ec9v33a2/aFv2LlfP/HOnf3z/AMff175+3n+DqfD/AL28ThR3m3m/VytXfC/vSszx24jwcXzo7cOI3/1fK29xev2LqfAvsR4f4x4sZhx8X/I0hvd4hEtr22353/U3fxEjj12A/wDhviSoRqxUvfY7G3e8M33f3+3415T1efo39f5fX8P/AOO+v+q8s1PvxA46603a/cIn9/5VSo13/s2/s/eWkxVTo1KqcqHH/dWx/N/fMs3XmIrt8S6+P7/2/vL0Xn593x14/J531f+1A3f8AH94pIN/i+FIt/f8AGo3v/m/v7y3sA24Xf/xJKN4Itt2pBBb5eZe1vXogkbbv3j32/vE4R2kggk5aBgggm0B20k43934/1pC4X4v9qC4W1IInaIjaSp2y2o23L/e4fveX91IsU21GkZl133vx/30/wA604vX1+3R+S7PsoRfbzG/wS4c39/aQ/4i4I1O4M3/xK24p179YuK3ECp+246l/wz/eP4S0sP282uNf35f8ASf5l09Uj3/a8k5/2a40k/wACp15318/Y5S1X03KvtP2e022f3x6v7/tW+iP5jS5xAt/vf34V0Giu+C0/4nh93aN25f32/mXK/wCzE92/J8x7L2sP7Nf9XpUdzqIfe431P+9ItS/5ybc/q/d+G7l/c/mRk23p9v8AG+L3X/8AEpTf+p4d35fj8vwf31/UgnL3Cbd/p/d/5U2e32O/i8vv/v1P5f4atI/cveX9f3t3v1L7S/iIs80e3q/ifw3L2kAtS5D4e3f4ngS6pC03/vHf4mbb13X99x/5m4Xn3B9I2Jk/f5fh+fUhy/1N/wCL83b+9qf4llX2eX/1/v0k4O3953f31IKU/m5nI/8Ae912X8KAtX/s8S3q2+4v31J/732v/a5fM3b/AOHp8v1f9yS3v/m93m3C3p3aevm8t396iAThWpAtJ0XW+Uve3y/jUn2E21dE23eZ4S9u5S4/6wTf+JAtAglXfag3b333fe3mX5E4L3/0/e33d/y/3IttSBFx4i0uXD/8A1/e/N82ne5I0C2/1p23b7yX/AJvgt3fw9qMmyAn2/wD839/UjE3mC/NAtA041t/R8/v3/wD2LgAAt/qQfB91sW/3O5O3D1f/AMj2/m/1Xfw/Cgt1P8XvX51Aatp3m9O3u/f8X7qByk3O8y/eT2k39I/vO2x+v95222+3xP73sXf2r1L9U04+D39/4f/sLgt0iO3+L2L5q4vL4A4y0Xv+mP9/uLgtpC+51Ptef035X/ADfC/G/f1f8A3l0KmyG2G0/N+dI93744A+X5/S01e0uK+XmXAtS9O3u2yEut38392o
