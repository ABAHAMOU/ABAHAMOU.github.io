<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CACS Africa · Chambre Africaine du Commerce et des Services</title>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;0,9..144,500;0,9..144,600;0,9..144,700;1,9..144,500;1,9..144,600&family=Space+Grotesk:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --ink-900:#0a1628;
    --ink-700:#0f2840;
    --ink-600:#1a3d5c;
    --paper:#f0f4f8;
    --paper-card:#e4eaf2;
    --paper-line:#c8d6e5;
    --sky:#4A90D9;
    --sky-dim:#357ABD;
    --sky-light:#7BB3E6;
    --sky-glow:rgba(74,144,217,0.3);
    --teal:#6fa8a0;
    --cream-text:#f0f6ff;
    --cream-text-dim:#b8ccdd;
    --ink-text:#142433;
    --ink-text-dim:#4a5e6e;
    --radius-lg:26px;
    --radius-md:16px;
    --ease:cubic-bezier(.22,.68,0,1);
    --font-display:'Fraunces',serif;
    --font-body:'Space Grotesk',sans-serif;
    --font-mono:'IBM Plex Mono',monospace;
  }
  *{margin:0;padding:0;box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    background:var(--paper);
    color:var(--ink-text);
    font-family:var(--font-body);
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
    overflow-x:hidden;
  }
  a{color:inherit;text-decoration:none;}
  img{max-width:100%;display:block;}
  .wrap{max-width:1240px;margin:0 auto;padding:0 2rem;}
  ::selection{background:var(--sky);color:#fff;}
  :focus-visible{outline:2px solid var(--sky);outline-offset:3px;}

  /* ===== ANIMATIONS ===== */
  @keyframes fadeInUp {
    from { opacity: 0; transform: translateY(40px); }
    to { opacity: 1; transform: translateY(0); }
  }
  @keyframes fadeInDown {
    from { opacity: 0; transform: translateY(-30px); }
    to { opacity: 1; transform: translateY(0); }
  }
  @keyframes fadeInLeft {
    from { opacity: 0; transform: translateX(-40px); }
    to { opacity: 1; transform: translateX(0); }
  }
  @keyframes fadeInRight {
    from { opacity: 0; transform: translateX(40px); }
    to { opacity: 1; transform: translateX(0); }
  }
  @keyframes scaleIn {
    from { opacity: 0; transform: scale(0.8); }
    to { opacity: 1; transform: scale(1); }
  }
  @keyframes float {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-10px); }
  }
  @keyframes pulse {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.05); }
  }
  @keyframes shimmer {
    0% { background-position: -200% center; }
    100% { background-position: 200% center; }
  }
  @keyframes slideUp {
    from { opacity: 0; transform: translateY(60px); }
    to { opacity: 1; transform: translateY(0); }
  }
  @keyframes rotateIn {
    from { opacity: 0; transform: rotate(-10deg) scale(0.9); }
    to { opacity: 1; transform: rotate(0) scale(1); }
  }
  @keyframes typing {
    from { width: 0; }
    to { width: 100%; }
  }
  @keyframes blink {
    50% { border-color: transparent; }
  }
  @keyframes gradientShift {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
  }
  @keyframes revealText {
    from { opacity: 0; transform: translateY(20px) scale(0.95); }
    to { opacity: 1; transform: translateY(0) scale(1); }
  }

  .animate-fade-up {
    opacity: 0;
    animation: fadeInUp 0.8s var(--ease) forwards;
  }
  .animate-fade-down {
    opacity: 0;
    animation: fadeInDown 0.8s var(--ease) forwards;
  }
  .animate-fade-left {
    opacity: 0;
    animation: fadeInLeft 0.8s var(--ease) forwards;
  }
  .animate-fade-right {
    opacity: 0;
    animation: fadeInRight 0.8s var(--ease) forwards;
  }
  .animate-scale {
    opacity: 0;
    animation: scaleIn 0.8s var(--ease) forwards;
  }
  .animate-float {
    animation: float 3s ease-in-out infinite;
  }
  .animate-pulse {
    animation: pulse 2s ease-in-out infinite;
  }
  .animate-shimmer {
    background: linear-gradient(90deg, transparent 0%, rgba(255,255,255,.1) 50%, transparent 100%);
    background-size: 200% 100%;
    animation: shimmer 3s ease-in-out infinite;
  }
  .animate-slide-up {
    opacity: 0;
    animation: slideUp 0.9s var(--ease) forwards;
  }
  .animate-rotate {
    opacity: 0;
    animation: rotateIn 0.8s var(--ease) forwards;
  }
  .animate-gradient {
    background-size: 200% 200%;
    animation: gradientShift 4s ease-in-out infinite;
  }
  .animate-reveal {
    opacity: 0;
    animation: revealText 0.8s var(--ease) forwards;
  }

  /* Delay classes */
  .delay-1 { animation-delay: 0.1s; }
  .delay-2 { animation-delay: 0.2s; }
  .delay-3 { animation-delay: 0.3s; }
  .delay-4 { animation-delay: 0.4s; }
  .delay-5 { animation-delay: 0.5s; }
  .delay-6 { animation-delay: 0.6s; }
  .delay-7 { animation-delay: 0.7s; }
  .delay-8 { animation-delay: 0.8s; }
  .delay-9 { animation-delay: 0.9s; }
  .delay-10 { animation-delay: 1s; }

  .eyebrow{
    font-family:var(--font-mono);
    font-size:.72rem;
    letter-spacing:.14em;
    text-transform:uppercase;
    display:inline-flex;
    align-items:center;
    gap:.55rem;
    color:var(--sky-dim);
    margin-bottom:1rem;
  }
  .eyebrow::before{
    content:"";
    width:22px;height:1px;
    background:var(--sky-dim);
    display:inline-block;
  }
  section.on-ink .eyebrow{color:var(--sky-light);}
  section.on-ink .eyebrow::before{background:var(--sky-light);}

  h1,h2,h3{font-family:var(--font-display);font-weight:600;letter-spacing:-.01em;}

  .route-divider{
    display:flex;align-items:center;gap:.8rem;
    padding:2.4rem 0 0;
    color:var(--ink-text-dim);
  }
  section.on-ink .route-divider{color:var(--cream-text-dim);}
  .route-divider .dash-line{
    flex:1;height:1px;
    background:repeating-linear-gradient(90deg,currentColor 0 6px,transparent 6px 12px);
    opacity:.5;
  }
  .route-divider i{font-size:.7rem;color:var(--sky-dim);}

  /*  NAV */
.nav{
  position:sticky;top:0;z-index:999;
  background: linear-gradient(135deg, #0f2840 0%, #1a3d5c 100%);
  border-bottom:1px solid rgba(255,255,255,.08);
  animation: fadeInDown 0.6s var(--ease) forwards;
}
.nav .wrap{display:flex;align-items:center;justify-content:space-between;padding:1.1rem 2rem;}
.nav-links a:not(.btn-adh){color:rgba(255,255,255,.7);}
.nav-links a:not(.btn-adh):hover{color:#fff;}
.brand .mark{color:#fff;}
.brand .mark span{color:var(--sky-light);}
.brand .sub{color:rgba(255,255,255,.5);}
.hamburger{color:#fff;}
  .brand{
    display:flex;
    align-items:center;
    gap:.8rem;
    line-height:1;
  }
  .brand .logo-img{
    width: 100px;
    height:55px;
    object-fit:contain;
    transition: transform 0.4s var(--ease);
  }
  .brand .logo-img:hover{
    transform: scale(1.05) rotate(-2deg);
  }
  
  .brand .mark{
    font-family:var(--font-display);
    font-weight:700;
    font-size:1.3rem;
    color:var(--ink-900);
    letter-spacing:-.01em;
    line-height:1.1;
  }
  .brand .mark span{color:var(--sky-dim);}
  .brand .sub{
    font-family:var(--font-mono);
    font-size:.55rem;
    letter-spacing:.08em;
    text-transform:uppercase;
    color:var(--ink-text-dim);
    line-height:1.2;
  }
  .nav-links{display:flex;align-items:center;gap:2rem;list-style:none;}
  .nav-links a:not(.btn-adh){
    font-size:.86rem;color:var(--ink-text-dim);position:relative;padding-bottom:3px;
    transition:color .25s var(--ease);
  }
  .nav-links a:not(.btn-adh)::after{
    content:"";position:absolute;left:0;bottom:0;width:0;height:1px;background:var(--sky-dim);
    transition:width .3s var(--ease);
  }
  .nav-links a:not(.btn-adh):hover{color:var(--ink-900);}
  .nav-links a:not(.btn-adh):hover::after{width:100%;}
  .btn-adh{
    font-family:var(--font-mono);font-size:.72rem;letter-spacing:.06em;text-transform:uppercase;
    background:var(--sky);color:#fff!important;
    padding:.65rem 1.4rem;border-radius:40px;
    display:inline-flex;align-items:center;gap:.5rem;
    transition:all .3s var(--ease);
    position:relative;
    overflow:hidden;
  }
  .btn-adh::before{
    content:'';
    position:absolute;
    top:0;left:-100%;
    width:100%;height:100%;
    background:linear-gradient(90deg,transparent,rgba(255,255,255,.2),transparent);
    transition:left .5s var(--ease);
  }
  .btn-adh:hover::before{left:100%;}
  .btn-adh:hover{background:var(--sky-dim);transform:translateY(-2px) scale(1.02);}
  .hamburger{display:none;background:none;border:none;font-size:1.5rem;color:var(--ink-900);cursor:pointer;}

  /* ===== BUTTONS ===== */
  .btn-primary{
    font-family:var(--font-mono);font-size:.78rem;letter-spacing:.06em;text-transform:uppercase;
    background:var(--sky);color:#fff;
    padding:.95rem 2rem;border-radius:40px;border:none;cursor:pointer;
    display:inline-flex;align-items:center;gap:.6rem;
    transition:all .3s var(--ease);
    box-shadow:0 10px 30px rgba(74,144,217,.3);
    position:relative;
    overflow:hidden;
  }
  .btn-primary::before{
    content:'';
    position:absolute;
    top:0;left:-100%;
    width:100%;height:100%;
    background:linear-gradient(90deg,transparent,rgba(255,255,255,.2),transparent);
    transition:left .5s var(--ease);
  }
  .btn-primary:hover::before{left:100%;}
  .btn-primary:hover{transform:translateY(-3px) scale(1.02);box-shadow:0 16px 40px rgba(74,144,217,.4);}
  .btn-ghost{
    font-family:var(--font-mono);font-size:.78rem;letter-spacing:.06em;text-transform:uppercase;
    background:transparent;color:var(--cream-text);
    padding:.9rem 1.9rem;border-radius:40px;border:1px solid rgba(255,255,255,.25);
    display:inline-flex;align-items:center;gap:.6rem;
    transition:all .3s var(--ease);
  }
  .btn-ghost:hover{border-color:var(--sky);background:rgba(74,144,217,.12);transform:translateY(-2px);}
  section:not(.on-ink) .btn-ghost{color:var(--ink-900);border-color:rgba(10,22,40,.2);}
  section:not(.on-ink) .btn-ghost:hover{border-color:var(--sky-dim);background:rgba(74,144,217,.08);}

  /*  HERO SLIDER  */
  .hero-slider{
    position:relative;
    height:100vh;
    min-height:600px;
    max-height:800px;
    overflow:hidden;
    background:var(--ink-900);
  }
  .slider-track{
    display:flex;
    width:100%;
    height:100%;
    transition:transform .8s cubic-bezier(.22,.68,0,1);
  }
  .slide{
    flex:0 0 100%;
    height:100%;
    position:relative;
    background-size:cover;
    background-position:center;
  }
  .slide::before{
    content:"";
    position:absolute;inset:0;
    background:linear-gradient(135deg,rgba(10,22,40,.7) 0%,rgba(10,22,40,.3) 100%);
  }
  .slide-overlay{
    position:absolute;inset:0;
    display:flex;align-items:center;
    padding:0 2rem;
  }
  .slide-overlay .wrap{
    display:grid;
    grid-template-columns:1.1fr .9fr;
    gap:3rem;
    align-items:center;
    width:100%;
  }
  .slide-content h1{
    font-size:clamp(2.6rem,5vw,4.2rem);
    line-height:1.04;
    color:var(--cream-text);
    margin-bottom:1.4rem;
    animation: fadeInUp 0.8s var(--ease) forwards;
    animation-delay: 0.3s;
    opacity:0;
  }
  .slide-content h1 em{font-style:italic;color:var(--sky-light);font-weight:500;}
  .slide-content p{
    font-size:1.08rem;
    color:var(--cream-text-dim);
    max-width:40ch;
    margin-bottom:2.2rem;
    animation: fadeInUp 0.8s var(--ease) forwards;
    animation-delay: 0.5s;
    opacity:0;
  }
  .slide-actions{
    display:flex;gap:1rem;flex-wrap:wrap;margin-bottom:3rem;
    animation: fadeInUp 0.8s var(--ease) forwards;
    animation-delay: 0.7s;
    opacity:0;
  }
  .slide-stats{
    display:flex;gap:2.4rem;flex-wrap:wrap;
    border-top:1px solid rgba(255,255,255,.1);padding-top:1.6rem;
    animation: fadeInUp 0.8s var(--ease) forwards;
    animation-delay: 0.9s;
    opacity:0;
  }
  .slide-stats div{display:flex;flex-direction:column;}
  .slide-stats .num{font-family:var(--font-display);font-size:1.9rem;color:var(--sky-light);font-weight:600;}
  .slide-stats .lbl{font-family:var(--font-mono);font-size:.68rem;letter-spacing:.08em;text-transform:uppercase;color:var(--cream-text-dim);}

  .slider-controls{
    position:absolute;
    bottom:2.5rem;
    left:50%;
    transform:translateX(-50%);
    display:flex;
    gap:1.2rem;
    z-index:10;
  }
  .slider-dot{
    width:12px;height:12px;
    border-radius:50%;
    background:rgba(255,255,255,.3);
    border:2px solid transparent;
    cursor:pointer;
    transition:all .4s var(--ease);
  }
  .slider-dot.active{
    background:var(--sky);
    border-color:rgba(255,255,255,.5);
    transform:scale(1.2);
  }
  .slider-dot:hover{background:var(--sky-light);transform:scale(1.1);}
  .slider-arrows{
    position:absolute;
    top:50%;
    transform:translateY(-50%);
    z-index:10;
    display:flex;
    justify-content:space-between;
    width:100%;
    padding:0 1.5rem;
    pointer-events:none;
  }
  .slider-arrows button{
    pointer-events:all;
    background:rgba(255,255,255,.08);
    border:1px solid rgba(255,255,255,.15);
    color:var(--cream-text);
    width:50px;height:50px;
    border-radius:50%;
    font-size:1.3rem;
    cursor:pointer;
    transition:all .3s var(--ease);
    backdrop-filter:blur(4px);
  }
  .slider-arrows button:hover{
    background:var(--sky);
    border-color:var(--sky);
    transform:scale(1.1);
  }
  .slider-arrows button:disabled{
    opacity:.3;
    cursor:not-allowed;
    transform:none;
  }

  /*  SECTION SHELL */
  section{padding:5.5rem 0;}
  section.on-ink{background:var(--ink-900);color:var(--cream-text);}
  .sec-head{display:flex;justify-content:space-between;align-items:flex-end;gap:2rem;margin-bottom:2.6rem;flex-wrap:wrap;}
  .sec-head h2{
    font-size:clamp(1.9rem,3vw,2.6rem);
    animation: fadeInUp 0.8s var(--ease) forwards;
    opacity:0;
  }
  section.on-ink .sec-head h2{color:var(--cream-text);}
  .sec-head p{
    max-width:40ch;color:var(--ink-text-dim);font-size:.95rem;
    animation: fadeInUp 0.8s var(--ease) forwards;
    animation-delay: 0.3s;
    opacity:0;
  }
  section.on-ink .sec-head p{color:var(--cream-text-dim);}

  /*  DISPATCH (NEWS) */
  .dispatch-grid{display:grid;grid-template-columns:1fr 1fr;gap:2.4rem;}
  .dispatch-card{
    background:var(--ink-700);border:1px solid rgba(255,255,255,.06);border-radius:var(--radius-lg);
    overflow:hidden;transition:all .4s var(--ease);
  }
  .dispatch-card:hover{
    transform:translateY(-10px) scale(1.01);
    border-color:rgba(74,144,217,.4);
    box-shadow:0 20px 60px rgba(0,0,0,.3);
  }
  .dispatch-card img{
    width:100%;height:230px;object-fit:cover;
    transition:transform .6s var(--ease);
  }
  .dispatch-card:hover img{transform:scale(1.05);}
  .dispatch-body{padding:1.8rem;}
  .dispatch-body p{
    animation: revealText 0.8s var(--ease) forwards;
    animation-delay: 0.4s;
    opacity:0;
  }
  .dispatch-tag{
    font-family:var(--font-mono);font-size:.65rem;letter-spacing:.1em;text-transform:uppercase;
    color:var(--sky-light);border:1px solid rgba(74,144,217,.35);padding:.25rem .8rem;border-radius:30px;
    display:inline-block;margin-bottom:1rem;
    transition:all .3s var(--ease);
  }
  .dispatch-card:hover .dispatch-tag{
    background:rgba(74,144,217,.1);
    border-color:var(--sky);
  }
  .dispatch-body h3{
    font-size:1.3rem;margin-bottom:.7rem;color:var(--cream-text);
    animation: fadeInUp 0.8s var(--ease) forwards;
    animation-delay: 0.2s;
    opacity:0;
  }
  .dispatch-body p{color:var(--cream-text-dim);font-size:.92rem;}

  /*  ABOUT (stamp cards) */
  .stamp-grid{display:grid;grid-template-columns:1fr 1fr;gap:2.4rem;}
  .stamp-card{
    position:relative;background:var(--paper-card);border-radius:var(--radius-md);
    padding:2.4rem 2.2rem;transition:all .4s var(--ease);
    border-left:4px solid var(--sky);
  }
  .stamp-card:hover{
    transform:translateY(-8px) scale(1.01);
    box-shadow:0 20px 50px rgba(0,0,0,.08);
  }
  .stamp-card p{
    animation: revealText 0.8s var(--ease) forwards;
    animation-delay: 0.4s;
    opacity:0;
  }
  .stamp-card i{
    font-size:1.6rem;color:var(--sky-dim);margin-bottom:1rem;display:block;
    transition:transform .4s var(--ease);
  }
  .stamp-card:hover i{transform:scale(1.2) rotate(-5deg);}
  .stamp-card h3{
    font-size:1.25rem;margin-bottom:.7rem;color:var(--ink-900);
    animation: fadeInUp 0.8s var(--ease) forwards;
    animation-delay: 0.2s;
    opacity:0;
  }
  .stamp-card p{color:var(--ink-text-dim);font-size:.93rem;}
  .stamp-foot{
    margin-top:1.3rem;font-family:var(--font-mono);font-size:.68rem;letter-spacing:.08em;
    text-transform:uppercase;color:var(--sky-dim);
  }

  /*  MISSIONS  */
  .mission-layout{display:grid;grid-template-columns:.9fr 1.1fr;gap:3rem;align-items:center;}
  .mission-figure{position:relative;border-radius:var(--radius-lg);overflow:hidden;border:1px solid rgba(255,255,255,.08);}
  .mission-figure img{
    width:100%;height:100%;object-fit:cover;display:block;
    transition:transform .8s var(--ease);
  }
  .mission-figure:hover img{transform:scale(1.05);}
  .mission-figure figcaption{
    position:absolute;left:0;right:0;bottom:0;padding:1.1rem 1.4rem;
    background:linear-gradient(0deg,rgba(10,22,40,.92),transparent);
    font-family:var(--font-mono);font-size:.66rem;letter-spacing:.08em;text-transform:uppercase;color:var(--cream-text-dim);
  }
  .mission-list{display:flex;flex-direction:column;}
  .mission-card{
    display:grid;grid-template-columns:44px 1fr;gap:1.2rem;
    padding:1.5rem 0;border-bottom:1px dashed rgba(255,255,255,.08);
    transition:all .4s var(--ease);
  }
  .mission-list .mission-card:last-child{border-bottom:none;}
  .mission-card:hover{
    padding-left:.8rem;
    transform:translateX(6px);
  }
  .mission-card p{
    animation: revealText 0.8s var(--ease) forwards;
    animation-delay: 0.4s;
    opacity:0;
  }
  .mission-card i{
    font-size:1.15rem;color:var(--sky-light);width:44px;height:44px;
    border:1px solid rgba(74,144,217,.3);border-radius:50%;
    display:flex;align-items:center;justify-content:center;
    transition:all .4s var(--ease);
  }
  .mission-card:hover i{
    background:rgba(74,144,217,.15);
    transform:scale(1.1) rotate(-5deg);
    border-color:var(--sky-light);
  }
  .mission-card h3{
    font-size:1.05rem;margin-bottom:.4rem;color:var(--cream-text);
    font-family:var(--font-body);font-weight:600;
    animation: fadeInUp 0.8s var(--ease) forwards;
    animation-delay: 0.2s;
    opacity:0;
  }
  .mission-card p{font-size:.88rem;color:var(--cream-text-dim);}

  /* SERVICES  */
  .ledger{border-top:1px solid var(--paper-line);}
  .ledger-row{
    display:grid;grid-template-columns:90px 1.1fr 1.6fr auto;gap:1.6rem;align-items:center;
    padding:1.5rem 0;border-bottom:1px solid var(--paper-line);
    transition:all .4s var(--ease);
    border-radius:8px;
  }
  .ledger-row:hover{
    background:rgba(74,144,217,.06);
    transform:translateX(8px) scale(1.005);
    padding-left:1rem;
  }
  .ledger-row p{
    animation: revealText 0.8s var(--ease) forwards;
    animation-delay: 0.4s;
    opacity:0;
  }
  .ledger-code{
    font-family:var(--font-mono);font-size:.8rem;color:var(--sky-dim);letter-spacing:.04em;
    transition:all .3s var(--ease);
  }
  .ledger-row:hover .ledger-code{color:var(--sky);transform:scale(1.05);}
  .ledger-row h3{
    font-size:1.08rem;color:var(--ink-900);
    animation: fadeInUp 0.8s var(--ease) forwards;
    animation-delay: 0.2s;
    opacity:0;
  }
  .ledger-row p{font-size:.87rem;color:var(--ink-text-dim);}
  .ledger-tag{
    font-family:var(--font-mono);font-size:.62rem;letter-spacing:.08em;text-transform:uppercase;
    color:var(--sky-dim);border:1px solid rgba(74,144,217,.3);padding:.3rem .8rem;border-radius:30px;
    white-space:nowrap;justify-self:end;
    transition:all .3s var(--ease);
  }
  .ledger-row:hover .ledger-tag{
    background:rgba(74,144,217,.08);
    border-color:var(--sky);
    transform:scale(1.05);
  }

  /*  EVENTS (log timeline)  */
  .log{position:relative;padding-left:2.6rem;}
  .log::before{
    content:"";position:absolute;left:5px;top:6px;bottom:6px;width:2px;
    background:repeating-linear-gradient(180deg,var(--sky) 0 6px,transparent 6px 13px);
  }
  .log-entry{
    position:relative;padding-bottom:2.6rem;display:grid;grid-template-columns:1fr;gap:1.4rem;
    transition:all .3s var(--ease);
  }
  .log-entry:hover{transform:translateX(6px);}
  .log-entry p{
    animation: revealText 0.8s var(--ease) forwards;
    animation-delay: 0.4s;
    opacity:0;
  }
  .log-entry.has-img{grid-template-columns:1fr 190px;align-items:center;}
  .log-entry:last-child{padding-bottom:0;}
  .log-entry::before{
    content:"";position:absolute;left:-2.6rem;top:4px;width:11px;height:11px;border-radius:50%;
    background:var(--sky);box-shadow:0 0 0 4px var(--paper),0 0 0 5px var(--sky-light);
    transition:all .4s var(--ease);
  }
  .log-entry:hover::before{
    transform:scale(1.3);
    box-shadow:0 0 0 6px var(--paper),0 0 0 8px var(--sky);
  }
  section.on-ink .log-entry::before{box-shadow:0 0 0 4px var(--ink-900),0 0 0 5px var(--sky);}
  section.on-ink .log-entry:hover::before{box-shadow:0 0 0 6px var(--ink-900),0 0 0 8px var(--sky);}
  .log-date{font-family:var(--font-mono);font-size:.72rem;letter-spacing:.06em;text-transform:uppercase;color:var(--sky-dim);margin-bottom:.4rem;display:block;}
  .log-entry h3{
    font-size:1.2rem;margin-bottom:.5rem;color:var(--ink-900);
    animation: fadeInUp 0.8s var(--ease) forwards;
    animation-delay: 0.2s;
    opacity:0;
  }
  section.on-ink .log-entry h3{color:var(--cream-text);}
  .log-entry p{color:var(--ink-text-dim);font-size:.92rem;max-width:62ch;}
  section.on-ink .log-entry p{color:var(--cream-text-dim);}
  .log-thumb{
    width:190px;height:130px;border-radius:14px;overflow:hidden;border:1px solid var(--paper-line);
    background:var(--paper-card);
    transition:all .4s var(--ease);
  }
  .log-entry:hover .log-thumb{transform:scale(1.03) rotate(-1deg);}
  section.on-ink .log-thumb{border-color:rgba(255,255,255,.1);background:var(--ink-700);}
  .log-thumb img{width:100%;height:100%;object-fit:cover;transition:transform .6s var(--ease);}
  .log-entry:hover .log-thumb img{transform:scale(1.08);}

  /*  MEMBERS  */
  .marquee{
    position:relative;overflow:hidden;
    -webkit-mask-image:linear-gradient(90deg,transparent,#000 6%,#000 94%,transparent);
    mask-image:linear-gradient(90deg,transparent,#000 6%,#000 94%,transparent);
  }
  .marquee-track{display:flex;gap:1.4rem;width:max-content;}
  @media(prefers-reduced-motion:no-preference){
    .marquee-track{animation:marquee 46s linear infinite;}
    .marquee:hover .marquee-track{animation-play-state:paused;}
  }
  @keyframes marquee{from{transform:translateX(0);}to{transform:translateX(-50%);}}
  .logo-tile{
    flex:0 0 auto;width:168px;height:100px;background:rgba(255,255,255,.04);
    border-radius:var(--radius-md);
    display:flex;align-items:center;justify-content:center;padding:1.2rem;
    border:1px solid rgba(255,255,255,.06);
    transition:all .4s var(--ease);
  }
  .logo-tile:hover{
    transform:translateY(-8px) scale(1.04);
    border-color:var(--sky);
    box-shadow:0 10px 30px rgba(74,144,217,.15);
  }
  .logo-tile img{
    max-width:100%;max-height:100%;object-fit:contain;
    filter:brightness(0) invert(1) opacity(.6);
    transition:all .4s var(--ease);
  }
  .logo-tile:hover img{
    filter:brightness(0) invert(1) opacity(1);
    transform:scale(1.05);
  }
  .logo-tile.text-tile{flex-direction:column;gap:.3rem;}
  .logo-tile.text-tile strong{font-family:var(--font-display);font-size:1rem;color:var(--cream-text);text-align:center;line-height:1.15;}
  .logo-tile.text-tile span{font-family:var(--font-mono);font-size:.58rem;letter-spacing:.06em;text-transform:uppercase;color:var(--cream-text-dim);}

  /*  CTA BANDS  */
  .cta-band{
    background:linear-gradient(135deg,var(--ink-900) 0%,var(--ink-600) 100%);
    border-radius:34px;padding:3.6rem 3rem;text-align:center;color:var(--cream-text);
    position:relative;overflow:hidden;
    transition:all .4s var(--ease);
  }
  .cta-band:hover{transform:scale(1.005);box-shadow:0 20px 60px rgba(0,0,0,.15);}
  .cta-band::before{
    content:"";position:absolute;inset:0;
    background:radial-gradient(circle at 80% 20%,rgba(74,144,217,.15),transparent 55%);
    pointer-events:none;
  }
  .cta-band p{
    animation: revealText 0.8s var(--ease) forwards;
    animation-delay: 0.4s;
    opacity:0;
  }
  .cta-band h2{
    font-size:clamp(1.9rem,3.4vw,2.8rem);margin-bottom:.8rem;color:var(--cream-text);position:relative;
    animation: fadeInUp 0.8s var(--ease) forwards;
    animation-delay: 0.2s;
    opacity:0;
  }
  .cta-band p{max-width:52ch;margin:0 auto 2rem;color:var(--cream-text-dim);position:relative;}
  .cta-band .btn-primary{position:relative;}

  .membership-cta{text-align:center;padding:1rem 0 0;}
  .membership-cta .btn-primary{font-size:.86rem;padding:1.1rem 3rem;}
  .membership-cta p{
    font-family:var(--font-mono);font-size:.7rem;letter-spacing:.08em;text-transform:uppercase;
    color:var(--ink-text-dim);margin-bottom:1.2rem;
    animation: revealText 0.8s var(--ease) forwards;
    animation-delay: 0.2s;
    opacity:0;
  }

  /*  FOOTER  */
  .footer{background:var(--ink-900);color:var(--cream-text-dim);padding:4.5rem 0 2rem;border-radius:44px 44px 0 0;margin-top:2rem;}
  .footer .wrap{display:grid;grid-template-columns:1.6fr 1fr 1fr 1fr;gap:3rem;}
  .footer h4{font-family:var(--font-mono);font-size:.72rem;letter-spacing:.1em;text-transform:uppercase;color:var(--sky-light);margin-bottom:1.2rem;}
  .footer .mark{font-family:var(--font-display);font-size:1.5rem;color:var(--cream-text);margin-bottom:.7rem;}
  .footer p{
    font-size:.88rem;line-height:1.9;
    animation: revealText 0.8s var(--ease) forwards;
    animation-delay: 0.3s;
    opacity:0;
  }
  .footer a{
    font-size:.88rem;line-height:1.9;
    transition:all .3s var(--ease);
    display:inline-block;
  }
  .footer a:hover{color:var(--sky-light);transform:translateX(4px);}
  .footer .social{display:flex;gap:.6rem;margin:1.2rem 0 1.4rem;}
  .footer .social a{
    width:38px;height:38px;border-radius:50%;border:1px solid rgba(255,255,255,.08);
    display:flex;align-items:center;justify-content:center;
    transition:all .3s var(--ease);
  }
  .footer .social a:hover{
    border-color:var(--sky);
    background:rgba(74,144,217,.15);
    transform:translateY(-4px) scale(1.1);
    color:var(--sky-light);
  }
  .newsletter{display:flex;gap:.5rem;}
  .newsletter input{
    flex:1;padding:.7rem 1.1rem;border-radius:30px;border:1px solid rgba(255,255,255,.08);
    background:rgba(255,255,255,.03);color:var(--cream-text);font-family:var(--font-body);font-size:.85rem;
    transition:all .3s var(--ease);
  }
  .newsletter input:focus{
    border-color:var(--sky);
    outline:none;
    box-shadow:0 0 20px rgba(74,144,217,.1);
    transform:scale(1.01);
  }
  .newsletter input::placeholder{color:var(--cream-text-dim);}
  .newsletter button{
    background:var(--sky);border:none;color:#fff;padding:.7rem 1.3rem;border-radius:30px;
    font-family:var(--font-mono);font-size:.72rem;text-transform:uppercase;cursor:pointer;
    transition:all .3s var(--ease);
  }
  .newsletter button:hover{
    background:var(--sky-dim);
    transform:scale(1.05);
  }
  .footer .copy{grid-column:1/-1;border-top:1px solid rgba(255,255,255,.06);padding-top:2rem;text-align:center;font-size:.78rem;font-family:var(--font-mono);color:#5e7183;}

  /* RESPONSIVE  */
  @media(max-width:980px){
    .slide-overlay .wrap{grid-template-columns:1fr;}
    .slide-content{text-align:center;}
    .slide-content p{margin-left:auto;margin-right:auto;}
    .slide-actions{justify-content:center;}
    .slide-stats{justify-content:center;}
    .mission-layout{grid-template-columns:1fr;}
    .mission-figure{height:220px;}
    .footer .wrap{grid-template-columns:1fr 1fr;}
    .slider-arrows{display:none;}
  }
  @media(max-width:768px){
    .hamburger{display:block;}
    .nav-links{
      position:absolute;top:100%;left:0;right:0;background:var(--paper);
      flex-direction:column;align-items:flex-start;gap:1rem;padding:1.6rem 2rem;
      border-bottom:1px solid var(--paper-line);display:none;
    }
    .nav-links.open{display:flex;}
    .hero-slider{height:80vh;min-height:500px;}
    .slide-content h1{font-size:clamp(2rem,8vw,2.8rem);}
    .dispatch-grid,.stamp-grid{grid-template-columns:1fr;}
    .log-entry.has-img{grid-template-columns:1fr;}
    .log-thumb{width:100%;height:170px;}
    .ledger-row{grid-template-columns:1fr;gap:.5rem;}
    .ledger-tag{justify-self:start;}
    section{padding:3.6rem 0;}
    .cta-band{padding:2.6rem 1.6rem;}
    .footer .wrap{grid-template-columns:1fr;}
    .slider-dot{width:10px;height:10px;}
    .slider-controls{gap:.8rem;bottom:1.5rem;}
    .brand .logo-img{width:70px;height:40px;}
    .brand .mark{font-size:1.1rem;}
    .brand .sub{font-size:.5rem;}
  }
</style>
</head>
<body>

<nav class="nav">
  <div class="wrap">
    <div class="brand">
      <img src="https://www.cacsafrica.org/assets/images/brand/logo.png" alt="CACS Africa Logo" class="logo-img animate-float">
    </div>
    <button class="hamburger" id="hamburger" aria-label="Menu"><i class="fas fa-bars"></i></button>
    <ul class="nav-links" id="navLinks">
      <li><a href="#accueil">Accueil</a></li>
      <li><a href="#a-propos">À propos</a></li>
      <li><a href="#missions">Missions</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#events">Évènements</a></li>
      <li><a href="#adherents">Adhérents</a></li>
      <li><a href="#" class="btn-adh">Adhésion <i class="fas fa-arrow-right"></i></a></li>
    </ul>
  </div>
</nav>

<!-- first SLIDER  -->
<section class="hero-slider" id="accueil">
  <div class="slider-track" id="sliderTrack"></div>
  <div class="slider-arrows">
    <button id="prevSlide" aria-label="Précédent"><i class="fas fa-chevron-left"></i></button>
    <button id="nextSlide" aria-label="Suivant"><i class="fas fa-chevron-right"></i></button>
  </div>
  <div class="slider-controls" id="sliderControls"></div>
</section>

<!--  ACTUALITÉ  -->
<section class="on-ink" id="actualite">
  <div class="wrap">
    <div class="route-divider"><i class="fas fa-anchor"></i><span class="dash-line"></span></div>
    <div class="sec-head">
      <div>
        <h2 class="animate-fade-up">Dernières escales</h2>
      </div>
      <p class="animate-fade-up delay-2">La CACS élargit son réseau d'antennes vers l'Afrique de l'Est.</p>
    </div>
    <div class="dispatch-grid">
      <div class="dispatch-card animate-fade-up delay-3">
        <img src="https://www.cacsafrica.org/assets/images/media/ii.jpg" alt="Table ronde du Burundi">
        <div class="dispatch-body">
          <span class="dispatch-tag"><i class="fas fa-handshake"></i> MOU signé</span>
          <h3>La CACS à la table ronde du Burundi</h3>
          <p>Les 5 et 6 décembre 2024 à Bujumbura, la CACS a pris part à la table ronde organisée par le gouvernement burundais et signé un accord de coopération avec la Chambre Fédérale de Commerce et de l'Industrie du Burundi, pour promouvoir les projets du PND 2040-2060 auprès des deux réseaux économiques.</p>
        </div>
      </div>
      <div class="dispatch-card animate-fade-up delay-5">
        <img src="https://www.cacsafrica.org/assets/images/media/ll.png" alt="Antenne de Bujumbura">
        <div class="dispatch-body">
          <span class="dispatch-tag"><i class="fas fa-map-marker-alt"></i> 5ème antenne</span>
          <h3>Ouverture d'une antenne à Bujumbura</h3>
          <p>L'accord prévoit l'ouverture d'une antenne CACS à Bujumbura — la cinquième du réseau et la première en Afrique de l'Est, pour soutenir la collaboration économique et les projets de développement à long terme entre les deux entités.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!--  À PROPOS  -->
<section id="a-propos">
  <div class="wrap">
    <div class="sec-head">
      <div>
        <h2 class="animate-fade-up">À propos de la Chambre</h2>
      </div>
      <p class="animate-fade-up delay-2">Une initiative privée qui fertilise les échanges depuis les Provinces du sud.</p>
    </div>
    <div class="stamp-grid">
      <div class="stamp-card animate-fade-left delay-3">
        <i class="fas fa-seedling"></i>
        <h3>Une plateforme de création de valeur</h3>
        <p>La CACS facilite l'implantation des entreprises du continent — notamment celles de la sous-région ouest-africaine — et fait fructifier leurs intérêts dans le terreau exceptionnellement fécond des Provinces du sud du Maroc.</p>
        <div class="stamp-foot">Init. 2021 — Registre CACS</div>
      </div>
      <div class="stamp-card animate-fade-right delay-5">
        <i class="fas fa-water"></i>
        <h3>Dakhla, porte océanique</h3>
        <p>Port atlantique, zone franche et infrastructures d'envergure mondiale font de Dakhla un hub logistique à l'horizon 2030 — déjà appuyé par 22 représentations diplomatiques et consulaires.</p>
        <div class="stamp-foot">22 représentations — Horizon 2030</div>
      </div>
    </div>
  </div>
</section>

<!--  MISSIONS  -->
<section class="on-ink" id="missions">
  <div class="wrap">
    <div class="route-divider"><i class="fas fa-compass"></i><span class="dash-line"></span></div>
    <div class="sec-head">
      <div>
        <div class="eyebrow">Cap fixé</div>
        <h2 class="animate-fade-up">Nos missions</h2>
      </div>
      <p class="animate-fade-up delay-2">Quatre caps qui orientent chaque action de la Chambre.</p>
    </div>
    <div class="mission-layout">
      <figure class="mission-figure animate-scale delay-3">
        <img src="https://www.cacsafrica.org/assets/images/media/afrique.png" alt="Carte du continent africain">
        <figcaption>Réseau CACS — 22 pays représentés</figcaption>
      </figure>
      <div class="mission-list">
        <div class="mission-card animate-fade-left delay-4">
          <i class="fas fa-handshake"></i>
          <div>
            <h3>Promouvoir</h3>
            <p>Les relations commerciales et industrielles entre acteurs marocains et africains.</p>
          </div>
        </div>
        <div class="mission-card animate-fade-left delay-5">
          <i class="fas fa-building"></i>
          <div>
            <h3>Faciliter</h3>
            <p>L'implantation et le développement des entreprises marocaines en Afrique, et inversement.</p>
          </div>
        </div>
        <div class="mission-card animate-fade-left delay-6">
          <i class="fas fa-chart-line"></i>
          <div>
            <h3>Renforcer</h3>
            <p>La compétitivité des entreprises via formation, conseil, incubation et accélération.</p>
          </div>
        </div>
        <div class="mission-card animate-fade-left delay-7">
          <i class="fas fa-globe"></i>
          <div>
            <h3>Développer</h3>
            <p>Le potentiel international des entreprises africaines et marocaines.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!--  SERVICES  -->
<section id="services">
  <div class="wrap">
    <div class="sec-head">
      <div>
        <div class="eyebrow">Registre des prestations</div>
        <h2 class="animate-fade-up">Nos services</h2>
      </div>
      <p class="animate-fade-up delay-2">Six escales pour accompagner une entreprise, de la prospection au réseau.</p>
    </div>
    <div class="ledger">
      <div class="ledger-row animate-slide-up delay-3">
        <span class="ledger-code">SVC · 01</span>
        <h3>Découvrir &amp; prospecter</h3>
        <p>Accompagnement dès la prospection, accès aux opportunités d'investissement identifiées sur le continent.</p>
        <span class="ledger-tag">Prospection</span>
      </div>
      <div class="ledger-row animate-slide-up delay-4">
        <span class="ledger-code">SVC · 02</span>
        <h3>S'implanter</h3>
        <p>Offre modulable : conseil stratégique, intelligence économique, accompagnement personnalisé.</p>
        <span class="ledger-tag">Implantation</span>
      </div>
      <div class="ledger-row animate-slide-up delay-5">
        <span class="ledger-code">SVC · 03</span>
        <h3>Recruter</h3>
        <p>Expertise et support dans le recrutement de talents locaux et internationaux.</p>
        <span class="ledger-tag">Talents</span>
      </div>
      <div class="ledger-row animate-slide-up delay-6">
        <span class="ledger-code">SVC · 04</span>
        <h3>Communiquer</h3>
        <p>Supports de communication mis à disposition pour assurer la visibilité de votre entreprise.</p>
        <span class="ledger-tag">Visibilité</span>
      </div>
      <div class="ledger-row animate-slide-up delay-7">
        <span class="ledger-code">SVC · 05</span>
        <h3>Renforcer les capacités</h3>
        <p>Formation continue et amélioration de l'employabilité des jeunes talents africains.</p>
        <span class="ledger-tag">Formation</span>
      </div>
      <div class="ledger-row animate-slide-up delay-8">
        <span class="ledger-code">SVC · 06</span>
        <h3>Réseauter</h3>
        <p>Africa Business Days et Africa Executive Meetings pour multiplier les occasions de networking.</p>
        <span class="ledger-tag">Networking</span>
      </div>
    </div>
  </div>
</section>

<!--  ÉVÉNEMENTS  -->
<section class="on-ink" id="events">
  <div class="wrap">
    <div class="route-divider"><i class="fas fa-book-open"></i><span class="dash-line"></span></div>
    <div class="sec-head">
      <div>
        <div class="eyebrow">Journal de bord</div>
        <h2 class="animate-fade-up">Nos évènements</h2>
      </div>
      <p class="animate-fade-up delay-2">Des ponts d'excellence, consignés au fil des escales.</p>
    </div>
    <div class="log">
      <div class="log-entry animate-fade-up delay-3">
        <div>
          <span class="log-date">Déc. 2024 — Bujumbura</span>
          <h3>Table ronde du Burundi</h3>
          <p>Participation à la table ronde organisée par le gouvernement du Burundi et signature d'un MOU de coopération avec la Chambre Fédérale de Commerce et d'Industrie du Burundi (CFCIB).</p>
        </div>
      </div>
      <div class="log-entry has-img animate-fade-up delay-4">
        <div>
          <span class="log-date">13 Fév. 2025 — N'Djamena</span>
          <h3>Rencontre de N'Djamena</h3>
          <p>Rencontre de haut niveau à l'hôtel Ledger sur l'Initiative Atlantique Royale, réunissant ambassadeurs et représentants de plusieurs pays africains.</p>
        </div>
        <div class="log-thumb"><img src="https://www.cacsafrica.org/assets/images/media/conf_3.png" alt="Rencontre de N'Djamena"></div>
      </div>
      <div class="log-entry has-img animate-fade-up delay-5">
        <div>
          <span class="log-date">2025 — Casablanca</span>
          <h3>Convention CFCIM × CACS</h3>
          <p>Une convention relie la CACS et la Chambre Française de Commerce et d'Industrie du Maroc, croisant les adhésions et mutualisant les événements de promotion.</p>
        </div>
        <div class="log-thumb"><img src="https://www.cacsafrica.org/assets/images/media/cf.jpg" alt="Convention CFCIM et CACS"></div>
      </div>
      <div class="log-entry has-img animate-fade-up delay-6">
        <div>
          <span class="log-date">2025 — Rabat</span>
          <h3>Convention ALEM</h3>
          <p>Partenariat entre l'Association des Lauréats Étrangers du Maroc et la CACS, sous le parrainage de l'Agence Marocaine de la Coopération Internationale.</p>
        </div>
        <div class="log-thumb"><img src="https://www.cacsafrica.org/assets/images/media/ASLEMCar.jpg" alt="Convention ALEM"></div>
      </div>
      <div class="log-entry has-img animate-fade-up delay-7">
        <div>
          <span class="log-date">2025 — Dakhla</span>
          <h3>Partenariat stratégique Dakhla</h3>
          <p>Un partenariat entre la Région de Dakhla Oued Eddahab et la CACS confie à cette dernière la conduite du marketing territorial.</p>
        </div>
        <div class="log-thumb"><img src="https://www.cacsafrica.org/assets/images/media/signature.jpg" alt="Signature du partenariat stratégique Dakhla"></div>
      </div>
      <div class="log-entry animate-fade-up delay-8">
        <div>
          <span class="log-date">Édition 2025 — Itinérant</span>
          <h3>Africa Business Days</h3>
          <p>Business rounds organisés en alternance à Dakhla, Laâyoune, Marrakech, Safi, Tanger et Oujda.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!--  ADHÉRENTS  -->
<section class="on-ink" id="adherents">
  <div class="wrap">
    <div class="route-divider"><i class="fas fa-scroll"></i><span class="dash-line"></span></div>
    <div class="sec-head">
      <div>
        <div class="eyebrow">Registre des adhérents</div>
        <h2 class="animate-fade-up">Ils nous font confiance</h2>
      </div>
      <p class="animate-fade-up delay-2">Un réseau d'entreprises et de chambres partenaires à travers le continent.</p>
    </div>
    <div class="marquee animate-scale delay-3">
      <div class="marquee-track" id="logoTrack"></div>
    </div>
  </div>
</section>

<!--  AFRICA BUSINESS DAYS CTA  -->
<section id="africa-days">
  <div class="wrap">
    <div class="cta-band animate-scale">
      <div class="eyebrow" style="justify-content:center;">Édition 2025</div>
      <h2><i class="fas fa-calendar-check"></i> Africa Business Days</h2>
      <p>Rencontres d'affaires de haut niveau à Dakhla — investissements, partenariats stratégiques et mise en réseau des acteurs économiques du continent.</p>
      <a href="#" class="btn-primary"><i class="fas fa-ticket-alt"></i> Réserver ma place</a>
    </div>
  </div>
</section>

<!--  MEMBERSHIP CTA  -->
<div class="wrap membership-cta">
  <p class="animate-fade-up">Rejoindre le réseau</p>
  <a href="#" class="btn-primary animate-pulse"><i class="fas fa-user-plus"></i> Demande d'adhésion</a>
</div>

<!--  FOOTER  -->
<footer class="footer">
  <div class="wrap">
    <div class="animate-fade-up delay-2">
      <div class="mark">CACS Africa</div>
      <p>Chambre Africaine du Commerce et des Services · Initiative privée depuis 2021.<br>
      <i class="fas fa-map-marker-alt"></i> Av Mohamed Fadel Semlali, Hay Rahma, Dakhla — Maroc</p>
      <p><i class="fas fa-envelope"></i> cacsafrica.dakhla@gmail.com<br><i class="fas fa-phone"></i> +212 663-632455</p>
      <div class="social">
        <a href="#" aria-label="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
        <a href="#" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
        <a href="#" aria-label="Facebook"><i class="fab fa-facebook-f"></i></a>
        <a href="#" aria-label="YouTube"><i class="fab fa-youtube"></i></a>
      </div>
      <div class="newsletter">
        <input type="email" placeholder="Adresse email">
        <button>S'abonner</button>
      </div>
    </div>
    <div class="animate-fade-up delay-3">
      <h4>Menu</h4>
      <a href="#accueil">Accueil</a><br>
      <a href="#a-propos">À propos</a><br>
      <a href="#missions">Nos missions</a><br>
      <a href="#services">Nos services</a><br>
      <a href="#events">Nos évènements</a><br>
      <a href="#adherents">Nos adhérents</a>
    </div>
    <div class="animate-fade-up delay-4">
      <h4>Évènements</h4>
      <a href="#africa-days">Africa Business Days</a><br>
      <a href="#">Presse</a><br>
      <a href="#">FAQ</a>
    </div>
    <div class="animate-fade-up delay-5">
      <h4>Contact</h4>
      <p><i class="fas fa-phone"></i> +212 663-632455</p>
      <p><i class="fas fa-envelope"></i> cacsafrica.dakhla@gmail.com</p>
      <p><i class="fas fa-clock"></i> Lun–Ven, 8h30–18h</p>
    </div>
    <div class="copy animate-fade-up delay-6">© 2026 CACS Africa — Tous droits réservés.</div>
  </div>
</footer>

<script>
(function(){
  // Mobile nav
  const hamburger = document.getElementById('hamburger');
  const navLinks = document.getElementById('navLinks');
  hamburger.addEventListener('click', (e)=>{ e.stopPropagation(); navLinks.classList.toggle('open'); });
  navLinks.querySelectorAll('a').forEach(a=>a.addEventListener('click', ()=>{
    if(window.innerWidth<=768) navLinks.classList.remove('open');
  }));
  document.addEventListener('click', (e)=>{
    if(window.innerWidth<=768 && !hamburger.contains(e.target) && !navLinks.contains(e.target)){
      navLinks.classList.remove('open');
    }
  });

  // Scroll reveal with IntersectionObserver
  const animateElements = document.querySelectorAll('.animate-fade-up, .animate-fade-left, .animate-fade-right, .animate-scale, .animate-slide-up, .animate-rotate, .animate-reveal');
  
  if('IntersectionObserver' in window){
    const observer = new IntersectionObserver((entries)=>{
      entries.forEach(entry => {
        if(entry.isIntersecting){
          entry.target.style.opacity = '1';
          observer.unobserve(entry.target);
        }
      });
    }, { threshold: 0.15 });
    
    animateElements.forEach(el => {
      el.style.opacity = '0';
      observer.observe(el);
    });
  } else {
    animateElements.forEach(el => el.style.opacity = '1');
  }

  // ===== HERO SLIDER =====
  const slides = [
    {
      img: 'https://www.cacsafrica.org/assets/images/media/jj.jpg',
      title: 'L\'Afrique<br>fait escale<br><em>à Dakhla.</em>',
      desc: 'La CACS relie les acteurs économiques marocains et africains depuis la porte océanique du continent — conseil, implantation, réseau, sur cinq antennes.'
    },
    {
      img: 'https://www.cacsafrica.org/assets/images/media/cc.jpg',
      title: 'Connecter<br>les marchés<br><em>d\'Afrique.</em>',
      desc: 'Faciliter les échanges commerciaux et industriels entre les acteurs marocains et africains pour un développement économique durable.'
    },
    {
      img: 'https://www.cacsafrica.org/assets/images/media/dd.jpg',
      title: 'L\'excellence<br>en <em>partenariat.</em>',
      desc: 'Des conventions stratégiques avec les chambres de commerce et les institutions pour renforcer la coopération panafricaine.'
    },
    {
      img: 'https://www.cacsafrica.org/assets/images/media/ee.jpg',
      title: 'Le hub<br><em>Atlantique.</em>',
      desc: 'Dakhla, porte océanique du continent, zone franche et infrastructures d\'envergure mondiale pour un hub logistique hors pair.'
    },
    {
      img: 'https://www.cacsafrica.org/assets/images/media/ff.jpg',
      title: 'L\'innovation<br>au <em>service</em><br>de l\'Afrique.',
      desc: 'Accompagner les entreprises dans leur transformation et leur compétitivité sur le marché africain et international.'
    },
    {
      img: 'https://www.cacsafrica.org/assets/images/media/gg.jpg',
      title: 'Construire<br><em>l\'avenir</em><br>ensemble.',
      desc: 'Unir les forces économiques du continent pour créer des opportunités d\'investissement et de croissance.'
    },
    {
      img: 'https://www.cacsafrica.org/assets/images/media/hh.jpg',
      title: 'Le réseau<br>des <em>leaders.</em>',
      desc: 'Africa Business Days — des rencontres d\'affaires de haut niveau pour connecter les décideurs du continent.'
    },
    {
      img: 'https://www.cacsafrica.org/assets/images/media/ii.jpg',
      title: 'Partenariats<br><em>stratégiques.</em>',
      desc: 'Des accords de coopération avec les institutions africaines pour promouvoir les projets de développement.'
    },
    {
      img: 'https://www.cacsafrica.org/assets/images/media/jj.png',
      title: 'Dakhla,<br>cap sur <em>l\'Afrique.</em>',
      desc: 'Une position stratégique au carrefour des routes maritimes et aériennes du continent.'
    },
    {
      img: 'https://www.cacsafrica.org/assets/images/media/kk.png',
      title: 'L\'excellence<br><em>africaine.</em>',
      desc: 'Promouvoir les talents et les entreprises africaines sur la scène internationale.'
    },
    {
      img: 'https://www.cacsafrica.org/assets/images/media/ll.png',
      title: '5ème antenne<br><em>à Bujumbura.</em>',
      desc: 'Le réseau CACS s\'étend en Afrique de l\'Est pour renforcer la collaboration économique.'
    },
    {
      img: 'https://www.cacsafrica.org/assets/images/media/mm.png',
      title: 'L\'Afrique<br><em>se connecte.</em>',
      desc: 'Un réseau de 22 pays représentés pour faciliter les échanges et les investissements.'
    },
    {
      img: 'https://www.cacsafrica.org/assets/images/media/oo.png',
      title: 'L\'avenir<br>est <em>africain.</em>',
      desc: 'Ensemble, bâtissons un avenir prospère pour le continent grâce au commerce et à la coopération.'
    }
  ];

  let currentSlide = 0;
  const track = document.getElementById('sliderTrack');
  const controls = document.getElementById('sliderControls');
  const prevBtn = document.getElementById('prevSlide');
  const nextBtn = document.getElementById('nextSlide');
  let autoPlayInterval;

  function buildSlides() {
    track.innerHTML = slides.map((slide, index) => `
      <div class="slide" style="background-image:url('${slide.img}')" data-index="${index}">
        <div class="slide-overlay">
          <div class="wrap">
            <div class="slide-content">
              <h1>${slide.title}</h1>
              <p>${slide.desc}</p>
              <div class="slide-actions">
                <a href="#a-propos" class="btn-primary"><i class="fas fa-compass"></i> Découvrir</a>
                <a href="#adherents" class="btn-ghost"><i class="fas fa-arrow-right"></i> Adhérents</a>
              </div>
              <div class="slide-stats">
                <div><span class="num">22</span><span class="lbl">Pays représentés</span></div>
                <div><span class="num">5</span><span class="lbl">Antennes africaines</span></div>
                <div><span class="num">$7Mds+</span><span class="lbl">Investissements catalysés</span></div>
              </div>
            </div>
            <div></div>
          </div>
        </div>
      </div>
    `).join('');

    controls.innerHTML = slides.map((_, i) => `
      <button class="slider-dot ${i === 0 ? 'active' : ''}" data-index="${i}" aria-label="Slide ${i+1}"></button>
    `).join('');

    controls.querySelectorAll('.slider-dot').forEach(dot => {
      dot.addEventListener('click', () => {
        goToSlide(parseInt(dot.dataset.index));
      });
    });
  }

  function goToSlide(index) {
    currentSlide = index;
    const slideWidth = 100;
    track.style.transform = `translateX(-${currentSlide * slideWidth}%)`;
    controls.querySelectorAll('.slider-dot').forEach((dot, i) => {
      dot.classList.toggle('active', i === currentSlide);
    });
    prevBtn.disabled = currentSlide === 0;
    nextBtn.disabled = currentSlide === slides.length - 1;
  }

  function nextSlide() {
    if (currentSlide < slides.length - 1) {
      goToSlide(currentSlide + 1);
    } else {
      goToSlide(0);
    }
  }

  function prevSlide() {
    if (currentSlide > 0) {
      goToSlide(currentSlide - 1);
    } else {
      goToSlide(slides.length - 1);
    }
  }

  function startAutoPlay() {
    if (autoPlayInterval) clearInterval(autoPlayInterval);
    autoPlayInterval = setInterval(nextSlide, 5000);
  }

  function stopAutoPlay() {
    if (autoPlayInterval) {
      clearInterval(autoPlayInterval);
      autoPlayInterval = null;
    }
  }

  buildSlides();
  goToSlide(0);
  startAutoPlay();

  prevBtn.addEventListener('click', () => { stopAutoPlay(); prevSlide(); startAutoPlay(); });
  nextBtn.addEventListener('click', () => { stopAutoPlay(); nextSlide(); startAutoPlay(); });

  const slider = document.querySelector('.hero-slider');
  slider.addEventListener('mouseenter', stopAutoPlay);
  slider.addEventListener('mouseleave', startAutoPlay);

  let touchStartX = 0;
  let touchEndX = 0;
  slider.addEventListener('touchstart', (e) => {
    touchStartX = e.changedTouches[0].screenX;
  });
  slider.addEventListener('touchend', (e) => {
    touchEndX = e.changedTouches[0].screenX;
    const diff = touchStartX - touchEndX;
    if (Math.abs(diff) > 50) {
      stopAutoPlay();
      if (diff > 0) { nextSlide(); } else { prevSlide(); }
      startAutoPlay();
    }
  });

  document.addEventListener('keydown', (e) => {
    if (e.key === 'ArrowLeft') { stopAutoPlay(); prevSlide(); startAutoPlay(); }
    if (e.key === 'ArrowRight') { stopAutoPlay(); nextSlide(); startAutoPlay(); }
  });

  // ===== MEMBERS LOGO MARQUEE =====
  const logos = [
    ['Fenie Brossette','https://www.feniebrossette.ma/wp-content/uploads/2025/05/Logo-FB-1.png'],
    ['Holark','https://www.cacsafrica.org/assets/images/brand/HOLARK.png'],
    ['iOffice','https://www.cacsafrica.org/assets/images/brand/IOFFICE.png'],
    ['Mofi Équipements','https://www.cacsafrica.org/assets/images/brand/MOFI%20EQUIPEMENTS.png'],
    ['Codex','https://www.cacsafrica.org/assets/images/brand/CODEX.png'],
    ['CMIM','https://www.cacsafrica.org/assets/images/brand/CMIM.png'],
    ['Sensyo','https://www.cacsafrica.org/assets/images/brand/sensyo.png'],
    ['LDS','https://www.cacsafrica.org/assets/images/brand/LDS.png'],
    ['Ruben Maroc','https://www.cacsafrica.org/assets/images/brand/ruben_maroc.png'],
    ['Wamer','https://www.cacsafrica.org/assets/images/brand/WAMER%20.png'],
    ['Marcon Maroc','https://www.cacsafrica.org/assets/images/brand/MARCON%20MAROC%20.png'],
    ['ArcHub','https://www.cacsafrica.org/assets/images/brand/ARCHUB.png'],
    ['Yool','https://www.cacsafrica.org/assets/images/brand/yool.png'],
  ];
  const buildTile = ([name,src])=>`
    <div class="logo-tile"><img src="${src}" alt="${name}" loading="lazy"></div>
  `;
  const textTile = `
    <div class="logo-tile text-tile"><strong>Bureau<br>Veritas</strong><span>Certification</span></div>
  `;
  const tiles = logos.map(buildTile).join('') + textTile;
  document.getElementById('logoTrack').innerHTML = tiles + tiles;
})();
</script>
</body>
</html>
