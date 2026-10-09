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
  h1,h2,h3,h4{
    font-family:var(--serif);
    font-weight:500;
    margin:0;
    letter-spacing:-0.01em;
  }
  p{margin:0;}
  .wrap{max-width:var(--max);margin:0 auto;padding:0 20px;}
  section{position:relative;}

  @media (prefers-reduced-motion: reduce){
    *{
      animation-duration:0.001ms !important;
      animation-iteration-count:1 !important;
      transition-duration:0.001ms !important;
      scroll-behavior:auto !important;
    }
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

  .btn-primary{
    background:var(--ink);
    color:var(--cream);
  }

  .btn-primary:hover{background:var(--bronze-dark);}

  .btn-ghost{
    background:transparent;
    border-color:var(--ink);
    color:var(--ink);
  }

  .btn-ghost:hover{
    background:var(--ink);
    color:var(--cream);
  }

  .btn-ghost-light{
    background:transparent;
    border-color:rgba(244,239,229,0.5);
    color:var(--cream);
  }

  .btn-ghost-light:hover{
    background:var(--cream);
    color:var(--ink);
    border-color:var(--cream);
  }

  /* ---------- Header ---------- */
  header{
    position:fixed;
    top:0;
    left:0;
    right:0;
    z-index:100;
    padding:20px 0;
    transition:padding .3s ease, background .3s ease, box-shadow .3s ease;
  }

  header.scrolled{
    padding:13px 0;
    background:rgba(228,220,205,0.94);
    backdrop-filter:blur(10px);
    box-shadow:0 1px 0 var(--line);
  }

  header .wrap{
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:18px;
  }

  .logo{
    display:flex;
    flex-direction:column;
    line-height:1;
  }

  .logo .mark{
    font-family:var(--serif);
    font-size:21px;
    font-weight:500;
    letter-spacing:0.01em;
  }

  .logo .sub{
    font-size:10px;
    letter-spacing:0.22em;
    font-weight:600;
    color:var(--bronze-dark);
    margin-top:4px;
  }

  nav.primary-nav{
    display:flex;
    align-items:center;
    gap:26px;
  }

  nav.primary-nav a{
    font-size:14px;
    font-weight:500;
    position:relative;
    padding:4px 0;
  }

  nav.primary-nav a::after{
    content:"";
    position:absolute;
    left:0;
    right:100%;
    bottom:0;
    height:1px;
    background:var(--ink);
    transition:right .3s ease;
  }

  nav.primary-nav a:hover::after{right:0;}

  .header-actions{
    display:flex;
    align-items:center;
    gap:12px;
  }

  .call-btn{
    display:flex;
    align-items:center;
    justify-content:center;
    width:38px;
    height:38px;
    border:1px solid var(--ink);
    border-radius:50%;
    flex-shrink:0;
    transition:background .25s ease, color .25s ease
    
