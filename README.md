<!DOCTYPE html>
<html lang="en" data-theme="dark">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Pratik Raj — Portfolio</title>
<link rel="preconnect" href="https://fonts.googleapis.com"/>
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin/>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Mono:ital,wght@0,300;0,400;1,300&family=Outfit:wght@300;400;500;600&display=swap" rel="stylesheet"/>
<style>
  :root[data-theme="dark"]{--bg:#080c14;--bg2:#0d1220;--bg3:#111827;--surface:#161e2e;--border:rgba(99,179,237,0.12);--accent:#38bdf8;--accent2:#818cf8;--accent3:#34d399;--text:#e2e8f0;--text-muted:#64748b;--text-dim:#94a3b8;--glow:rgba(56,189,248,0.15);--grad1:linear-gradient(135deg,#38bdf8,#818cf8);--grad2:linear-gradient(135deg,#818cf8,#34d399)}
  :root[data-theme="light"]{--bg:#f0f4ff;--bg2:#e8eeff;--bg3:#dde5ff;--surface:#ffffff;--border:rgba(99,102,241,0.18);--accent:#2563eb;--accent2:#7c3aed;--accent3:#059669;--text:#1e293b;--text-muted:#94a3b8;--text-dim:#475569;--glow:rgba(37,99,235,0.1);--grad1:linear-gradient(135deg,#2563eb,#7c3aed);--grad2:linear-gradient(135deg,#7c3aed,#059669)}
  *,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
  html{scroll-behavior:smooth}
  body{font-family:'Outfit',sans-serif;background:var(--bg);color:var(--text);overflow-x:hidden;transition:background .4s,color .4s}
  body::before{content:'';position:fixed;inset:0;background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='4'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.04'/%3E%3C/svg%3E");pointer-events:none;z-index:0;opacity:.35}
  ::-webkit-scrollbar{width:4px}::-webkit-scrollbar-track{background:var(--bg)}::-webkit-scrollbar-thumb{background:var(--accent);border-radius:2px}
 
  nav{position:fixed;top:0;width:100%;z-index:1000;display:flex;align-items:center;justify-content:space-between;padding:1rem 6vw;backdrop-filter:blur(18px);background:rgba(8,12,20,0.82);border-bottom:1px solid var(--border);transition:background .4s}
  [data-theme="light"] nav{background:rgba(240,244,255,0.88)}
  .nav-logo{font-family:'Syne',sans-serif;font-weight:800;font-size:1.4rem;background:var(--grad1);-webkit-background-clip:text;-webkit-text-fill-color:transparent}
  .nav-links{display:flex;gap:2rem;list-style:none;align-items:center}
  .nav-links a{font-family:'DM Mono',monospace;font-size:.78rem;color:var(--text-dim);text-decoration:none;letter-spacing:.05em;text-transform:uppercase;transition:color .2s;position:relative}
  .nav-links a::after{content:'';position:absolute;bottom:-4px;left:0;width:0;height:1px;background:var(--accent);transition:width .3s}
  .nav-links a:hover{color:var(--accent)}.nav-links a:hover::after{width:100%}
  .theme-btn{background:var(--surface);border:1px solid var(--border);color:var(--text);cursor:pointer;width:38px;height:38px;border-radius:50%;display:grid;place-items:center;transition:all .3s}
  .theme-btn:hover{border-color:var(--accent)}
  .hamburger{display:none;flex-direction:column;gap:5px;cursor:pointer}
  .hamburger span{width:24px;height:2px;background:var(--text);border-radius:2px}
 
  section{position:relative;z-index:1;padding:7rem 6vw}
  .section-tag{font-family:'DM Mono',monospace;font-size:.72rem;letter-spacing:.15em;text-transform:uppercase;color:var(--accent);margin-bottom:.6rem}
  .section-title{font-family:'Syne',sans-serif;font-size:clamp(2rem,4vw,3rem);font-weight:800;line-height:1.1;margin-bottom:1.5rem}
 
  /* HERO */
  #hero{min-height:100vh;display:flex;align-items:center;padding-top:7rem;overflow:hidden}
  .hero-bg-orb{position:absolute;border-radius:50%;filter:blur(80px);pointer-events:none;opacity:.32}
  .orb1{width:500px;height:500px;background:radial-gradient(circle,#38bdf818,transparent 70%);top:-10%;right:-5%}
  .orb2{width:350px;height:350px;background:radial-gradient(circle,#818cf818,transparent 70%);bottom:10%;left:-5%}
  .hero-grid{display:grid;grid-template-columns:1fr 1fr;gap:4rem;align-items:center;width:100%;max-width:1200px;margin:0 auto}
  .hero-eyebrow{font-family:'DM Mono',monospace;font-size:.78rem;color:var(--accent3);letter-spacing:.15em;text-transform:uppercase;margin-bottom:1rem;display:flex;align-items:center;gap:.8rem}
  .hero-eyebrow::before{content:'';display:inline-block;width:30px;height:1px;background:var(--accent3)}
  h1{font-family:'Syne',sans-serif;font-size:clamp(3rem,6vw,5.5rem);font-weight:800;line-height:1;letter-spacing:-2px;margin-bottom:1.2rem}
  .name-highlight{background:var(--grad1);-webkit-background-clip:text;-webkit-text-fill-color:transparent;display:block}
  .hero-tagline{font-family:'DM Mono',monospace;font-size:.88rem;font-style:italic;color:var(--text-dim);margin-bottom:2.5rem;max-width:500px;line-height:1.7}
  .hero-btns{display:flex;gap:1rem;flex-wrap:wrap;margin-bottom:2.5rem}
  .btn-primary{padding:.85rem 2rem;border-radius:6px;background:var(--grad1);color:#fff;font-weight:600;text-decoration:none;font-size:.9rem;transition:transform .2s,box-shadow .2s;display:inline-flex;align-items:center;gap:.5rem;border:none;cursor:pointer;font-family:'Outfit',sans-serif}
  .btn-primary:hover{transform:translateY(-2px);box-shadow:0 8px 30px var(--glow)}
  .btn-outline{padding:.85rem 2rem;border-radius:6px;border:1px solid var(--border);color:var(--text);text-decoration:none;font-size:.9rem;font-weight:500;transition:all .2s;display:inline-flex;align-items:center;gap:.5rem}
  .btn-outline:hover{border-color:var(--accent);color:var(--accent);background:var(--glow)}
 
  .hero-socials{display:flex;gap:.8rem}
  .social-icon{width:44px;height:44px;border-radius:10px;border:1px solid var(--border);background:var(--surface);display:grid;place-items:center;text-decoration:none;transition:all .25s}
  .social-icon:hover{transform:translateY(-3px);box-shadow:0 6px 20px rgba(0,0,0,.2)}
  .social-icon.li:hover{border-color:#0A66C2;background:rgba(10,102,194,.1)}
  .social-icon.gh:hover{border-color:#6e7681;background:rgba(110,118,129,.1)}
  .social-icon.lc:hover{border-color:#FFA116;background:rgba(255,161,22,.1)}
  .social-icon.em:hover{border-color:#EA4335;background:rgba(234,67,53,.1)}
 
  .hero-visual{display:flex;align-items:center;justify-content:center;position:relative}
  .hero-card{width:340px;height:420px;background:var(--surface);border:1px solid var(--border);border-radius:20px;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:1.5rem;padding:2.5rem;position:relative;overflow:hidden;box-shadow:0 25px 60px rgba(0,0,0,.3)}
  .hero-card::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;background:var(--grad1)}
  .avatar-ring{width:100px;height:100px;border-radius:50%;background:var(--grad1);padding:3px;display:grid;place-items:center;animation:spin-ring 8s linear infinite}
  @keyframes spin-ring{to{transform:rotate(360deg)}}
  .avatar-inner{width:94px;height:94px;border-radius:50%;background:var(--bg3);display:grid;place-items:center;animation:counter-spin 8s linear infinite;font-size:2.6rem}
  @keyframes counter-spin{to{transform:rotate(-360deg)}}
  .hero-card-name{font-family:'Syne',sans-serif;font-size:1.4rem;font-weight:800;text-align:center}
  .hero-card-role{font-family:'DM Mono',monospace;font-size:.72rem;color:var(--accent);text-align:center;letter-spacing:.08em}
  .hero-card-stats{display:grid;grid-template-columns:repeat(3,1fr);gap:1rem;width:100%}
  .stat{text-align:center}
  .stat-num{font-family:'Syne',sans-serif;font-size:1.3rem;font-weight:800;background:var(--grad1);-webkit-background-clip:text;-webkit-text-fill-color:transparent}
  .stat-label{font-size:.65rem;color:var(--text-muted);font-family:'DM Mono',monospace;text-transform:uppercase}
  .float-badge{position:absolute;padding:.5rem 1rem;background:var(--surface);border:1px solid var(--border);border-radius:999px;font-size:.75rem;font-family:'DM Mono',monospace;color:var(--text-dim);white-space:nowrap;animation:float 3s ease-in-out infinite;box-shadow:0 8px 24px rgba(0,0,0,.2);display:flex;align-items:center;gap:.5rem}
  .float-badge.b1{top:12%;left:-15%;animation-delay:0s}
  .float-badge.b2{bottom:20%;right:-12%;animation-delay:1s}
  .float-badge.b3{bottom:5%;left:5%;animation-delay:2s}
  @keyframes float{0%,100%{transform:translateY(0)}50%{transform:translateY(-8px)}}
 
  /* ABOUT */
  #about{background:var(--bg2)}
  .about-grid{display:grid;grid-template-columns:1fr 1.5fr;gap:5rem;max-width:1100px;margin:0 auto;align-items:start}
  .about-left{position:sticky;top:6rem}
  .about-photo-frame{width:100%;aspect-ratio:1;border-radius:16px;background:var(--surface);border:1px solid var(--border);display:grid;place-items:center;font-size:5rem;position:relative;overflow:hidden}
  .about-photo-frame::after{content:'';position:absolute;inset:0;background:var(--grad1);opacity:.07}
  .about-interest-chips{display:flex;flex-wrap:wrap;gap:.6rem;margin-top:1.5rem}
  .chip{padding:.4rem 1rem;border-radius:999px;border:1px solid var(--border);background:var(--surface);font-size:.75rem;font-family:'DM Mono',monospace;color:var(--text-dim);transition:all .2s;display:inline-flex;align-items:center;gap:.4rem}
  .chip:hover{border-color:var(--accent);color:var(--accent)}
  .chip svg{width:13px;height:13px}
  .about-text p{color:var(--text-dim);line-height:1.8;margin-bottom:1.2rem}
  .about-highlight{display:flex;gap:1rem;align-items:flex-start;padding:1.2rem;border-radius:10px;background:var(--surface);border:1px solid var(--border);margin-bottom:1rem;transition:all .2s}
  .about-highlight:hover{border-color:var(--border);box-shadow:0 4px 20px rgba(0,0,0,.1)}
  .highlight-icon{width:42px;height:42px;border-radius:8px;background:var(--glow);border:1px solid var(--border);display:grid;place-items:center;flex-shrink:0}
  .highlight-icon svg{width:22px;height:22px}
  .highlight-text h4{font-family:'Syne',sans-serif;font-size:.95rem;font-weight:700;margin-bottom:.2rem}
  .highlight-text p{font-size:.82rem;color:var(--text-muted);line-height:1.5;margin:0}
 
  /* SKILLS */
  #skills{background:var(--bg)}
  .skills-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:1.5rem;max-width:1100px;margin:0 auto}
  .skill-card{padding:2rem;border-radius:14px;background:var(--surface);border:1px solid var(--border);transition:all .3s;position:relative;overflow:hidden}
  .skill-card::before{content:'';position:absolute;top:0;left:0;right:0;height:2px;transform:scaleX(0);transform-origin:left;transition:transform .4s}
  .skill-card:nth-child(1)::before{background:var(--grad1)}
  .skill-card:nth-child(2)::before{background:var(--grad2)}
  .skill-card:nth-child(3)::before{background:linear-gradient(135deg,#34d399,#38bdf8)}
  .skill-card:hover::before{transform:scaleX(1)}
  .skill-card:hover{transform:translateY(-4px);box-shadow:0 12px 40px rgba(0,0,0,.2)}
  .skill-card-icons{display:flex;gap:.8rem;margin-bottom:1.2rem;flex-wrap:wrap}
  .skill-card-icons svg{width:34px;height:34px;filter:drop-shadow(0 2px 4px rgba(0,0,0,.2))}
  .skill-card h3{font-family:'Syne',sans-serif;font-size:1rem;font-weight:700;margin-bottom:1.2rem}
  .skill-pills{display:flex;flex-wrap:wrap;gap:.5rem}
  .skill-pill{padding:.35rem .9rem;border-radius:6px;background:var(--bg3);font-size:.78rem;font-family:'DM Mono',monospace;color:var(--text-dim);border:1px solid var(--border);transition:all .2s;display:inline-flex;align-items:center;gap:.4rem}
  .skill-pill svg{width:14px;height:14px;flex-shrink:0}
  .skill-pill:hover{background:var(--glow);color:var(--accent);border-color:var(--accent)}
 
  /* PROJECTS */
  #projects{background:var(--bg2)}
  .projects-container{max-width:1100px;margin:0 auto}
  .project-card{display:grid;grid-template-columns:1fr 1.2fr;gap:3rem;align-items:center;padding:3rem;border-radius:20px;background:var(--surface);border:1px solid var(--border);position:relative;overflow:hidden;transition:all .3s}
  .project-card::after{content:'';position:absolute;inset:0;background:var(--grad1);opacity:0;transition:opacity .4s;pointer-events:none}
  .project-card:hover{transform:translateY(-4px);box-shadow:0 20px 60px rgba(0,0,0,.3)}
  .project-card:hover::after{opacity:.03}
  .project-visual{aspect-ratio:16/10;border-radius:12px;background:linear-gradient(135deg,var(--bg3) 0%,var(--bg) 100%);border:1px solid var(--border);display:flex;flex-direction:column;align-items:center;justify-content:center;gap:1rem;position:relative;overflow:hidden;padding:1.5rem}
  .project-visual-label{font-family:'DM Mono',monospace;font-size:.7rem;color:var(--text-muted);letter-spacing:.1em;text-transform:uppercase}
  .project-tech-line{position:absolute;bottom:0;left:0;right:0;height:3px;background:var(--grad1)}
  .project-number{font-family:'Syne',sans-serif;font-size:4rem;font-weight:800;color:var(--border);line-height:1;margin-bottom:.5rem}
  .project-name{font-family:'Syne',sans-serif;font-size:2rem;font-weight:800;margin-bottom:.8rem}
  .project-desc{color:var(--text-dim);line-height:1.7;margin-bottom:1.5rem;font-size:.95rem}
  .project-tags{display:flex;flex-wrap:wrap;gap:.5rem;margin-bottom:2rem}
  .project-tag{padding:.3rem .8rem;border-radius:4px;background:var(--bg);border:1px solid var(--border);font-size:.72rem;font-family:'DM Mono',monospace;color:var(--accent);display:inline-flex;align-items:center;gap:.4rem}
  .project-tag svg{width:12px;height:12px}
  .project-features{margin-bottom:2rem}
  .project-features li{color:var(--text-dim);font-size:.88rem;margin-bottom:.5rem;padding-left:1.2rem;position:relative;list-style:none}
  .project-features li::before{content:'→';position:absolute;left:0;color:var(--accent3)}
  .project-btns{display:flex;gap:1rem}
  .btn-sm{padding:.6rem 1.4rem;border-radius:6px;font-size:.82rem;font-weight:500;text-decoration:none;display:inline-flex;align-items:center;gap:.5rem;transition:all .2s}
  .btn-sm svg{width:16px;height:16px}
  .btn-sm.primary{background:var(--grad1);color:#fff}
  .btn-sm.primary:hover{transform:translateY(-2px);box-shadow:0 6px 20px var(--glow)}
  .btn-sm.ghost{border:1px solid var(--border);color:var(--text-dim);background:var(--bg)}
  .btn-sm.ghost:hover{border-color:var(--accent);color:var(--accent)}
 
  /* ACHIEVEMENTS */
  #achievements{background:var(--bg)}
  .achievements-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:1.5rem;max-width:900px;margin:0 auto}
  .achievement-card{display:flex;gap:1.2rem;align-items:flex-start;padding:2rem;border-radius:14px;background:var(--surface);border:1px solid var(--border);transition:all .3s;position:relative;overflow:hidden}
  .achievement-card::before{content:'';position:absolute;inset:0;background:var(--grad1);opacity:0;transition:opacity .3s;pointer-events:none}
  .achievement-card:hover{transform:translateY(-3px);box-shadow:0 12px 40px rgba(0,0,0,.2)}
  .achievement-card:hover::before{opacity:.04}
  .achievement-icon{width:54px;height:54px;border-radius:10px;flex-shrink:0;background:var(--glow);border:1px solid var(--border);display:grid;place-items:center}
  .achievement-icon svg{width:32px;height:32px}
  .achievement-card h3{font-family:'Syne',sans-serif;font-size:1rem;font-weight:700;margin-bottom:.4rem}
  .achievement-card p{font-size:.82rem;color:var(--text-muted);line-height:1.5}
  .achievement-badge{display:inline-block;margin-top:.8rem;padding:.25rem .7rem;border-radius:999px;background:var(--glow);border:1px solid var(--border);font-size:.65rem;font-family:'DM Mono',monospace;color:var(--accent3);letter-spacing:.08em}
 
  /* CONTACT */
  #contact{background:var(--bg2)}
  .contact-grid{display:grid;grid-template-columns:1fr 1.4fr;gap:4rem;max-width:1100px;margin:0 auto}
  .contact-info{display:flex;flex-direction:column;gap:1.5rem}
  .contact-item{display:flex;gap:1rem;align-items:center;padding:1.2rem 1.5rem;border-radius:10px;background:var(--surface);border:1px solid var(--border);text-decoration:none;color:var(--text);transition:all .25s}
  .contact-item:hover{transform:translateX(4px)}
  .contact-item.c-email:hover{border-color:#EA4335;background:rgba(234,67,53,.05)}
  .contact-item.c-li:hover{border-color:#0A66C2;background:rgba(10,102,194,.05)}
  .contact-item.c-gh:hover{border-color:#6e7681;background:rgba(110,118,129,.05)}
  .contact-item.c-lc:hover{border-color:#FFA116;background:rgba(255,161,22,.05)}
  .contact-item-icon{width:46px;height:46px;border-radius:8px;background:var(--glow);border:1px solid var(--border);display:grid;place-items:center;flex-shrink:0}
  .contact-item-icon svg{width:26px;height:26px}
  .contact-item-text span{display:block;font-size:.72rem;font-family:'DM Mono',monospace;color:var(--text-muted);text-transform:uppercase;letter-spacing:.08em;margin-bottom:.15rem}
  .contact-item-text strong{font-size:.88rem;word-break:break-all}
  .contact-form{display:flex;flex-direction:column;gap:1.2rem}
  .form-group{display:flex;flex-direction:column;gap:.5rem}
  .form-group label{font-family:'DM Mono',monospace;font-size:.72rem;color:var(--text-muted);text-transform:uppercase;letter-spacing:.08em}
  .form-group input,.form-group textarea{padding:.9rem 1.2rem;border-radius:8px;background:var(--surface);border:1px solid var(--border);color:var(--text);font-family:'Outfit',sans-serif;font-size:.9rem;transition:border-color .2s,box-shadow .2s;resize:none;outline:none}
  .form-group input:focus,.form-group textarea:focus{border-color:var(--accent);box-shadow:0 0 0 3px var(--glow)}
  .form-group textarea{min-height:130px}
 
  footer{background:var(--bg);border-top:1px solid var(--border);text-align:center;padding:2.5rem;font-family:'DM Mono',monospace;font-size:.75rem;color:var(--text-muted)}
  footer span{color:var(--accent)}
 
  .fade-up{opacity:0;transform:translateY(30px);transition:opacity .7s,transform .7s}
  .fade-up.visible{opacity:1;transform:translateY(0)}
  .fade-left{opacity:0;transform:translateX(-30px);transition:opacity .7s,transform .7s}
  .fade-left.visible{opacity:1;transform:translateX(0)}
  .fade-right{opacity:0;transform:translateX(30px);transition:opacity .7s,transform .7s}
  .fade-right.visible{opacity:1;transform:translateX(0)}
  .stagger>*{opacity:0;transform:translateY(20px);transition:opacity .5s,transform .5s}
  .stagger.visible>*:nth-child(1){opacity:1;transform:none;transition-delay:.05s}
  .stagger.visible>*:nth-child(2){opacity:1;transform:none;transition-delay:.15s}
  .stagger.visible>*:nth-child(3){opacity:1;transform:none;transition-delay:.25s}
  .stagger.visible>*:nth-child(4){opacity:1;transform:none;transition-delay:.35s}
 
  .toast{position:fixed;bottom:2rem;right:2rem;z-index:9999;padding:1rem 1.5rem;border-radius:10px;background:var(--surface);border:1px solid var(--accent3);color:var(--accent3);font-family:'DM Mono',monospace;font-size:.8rem;transform:translateY(100px);opacity:0;transition:all .4s;display:flex;align-items:center;gap:.6rem}
  .toast.show{transform:translateY(0);opacity:1}
 
  @media(max-width:900px){
    .hero-grid{grid-template-columns:1fr}.hero-visual{display:none}
    .about-grid{grid-template-columns:1fr;gap:2rem}.about-left{position:static}.about-photo-frame{max-width:200px}
    .skills-grid{grid-template-columns:1fr}.project-card{grid-template-columns:1fr;gap:2rem}
    .achievements-grid{grid-template-columns:1fr}.contact-grid{grid-template-columns:1fr}
    .nav-links{display:none;position:fixed;top:70px;left:0;right:0;flex-direction:column;background:var(--bg);padding:2rem;border-bottom:1px solid var(--border);gap:1.5rem}
    .nav-links.open{display:flex}.hamburger{display:flex}
    section{padding:5rem 5vw}
  }
</style>
</head>
<body>
 
<!-- ════ INLINE SVG LOGO LIBRARY ════ -->
<svg style="display:none" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <!-- LinkedIn official mark -->
    <symbol id="L-linkedin" viewBox="0 0 24 24">
      <rect width="24" height="24" rx="4" fill="#0A66C2"/>
      <path fill="#fff" d="M7.1 19H4.2V9.5h2.9V19zm-1.45-10.8a1.68 1.68 0 110-3.36 1.68 1.68 0 010 3.36zM19.8 19h-2.9v-4.6c0-1.1-.02-2.5-1.53-2.5-1.53 0-1.76 1.2-1.76 2.43V19H10.7V9.5h2.78v1.3h.04c.39-.73 1.33-1.5 2.73-1.5 2.92 0 3.46 1.92 3.46 4.42V19z"/>
    </symbol>
    <!-- GitHub mark -->
    <symbol id="L-github" viewBox="0 0 24 24">
      <rect width="24" height="24" rx="4" fill="#24292f"/>
      <path fill="#fff" d="M12 3.5C7.31 3.5 3.5 7.31 3.5 12c0 3.76 2.44 6.95 5.83 8.08.43.08.58-.18.58-.41v-1.45c-2.37.52-2.87-1.14-2.87-1.14-.39-1-.95-1.26-.95-1.26-.78-.53.06-.52.06-.52.86.06 1.31.88 1.31.88.76 1.3 2 .93 2.49.71.08-.55.3-.93.54-1.14-1.89-.21-3.87-.94-3.87-4.19 0-.93.33-1.68.88-2.28-.09-.21-.38-1.07.08-2.24 0 0 .71-.23 2.34.87a8.12 8.12 0 012.13-.29c.72 0 1.45.1 2.13.29 1.62-1.1 2.33-.87 2.33-.87.46 1.17.17 2.03.08 2.24.55.6.88 1.35.88 2.28 0 3.26-1.99 3.97-3.88 4.18.3.26.58.77.58 1.56v2.31c0 .23.15.5.59.41C18.07 18.95 20.5 15.76 20.5 12c0-4.69-3.81-8.5-8.5-8.5z"/>
    </symbol>
    <!-- LeetCode mark -->
    <symbol id="L-leetcode" viewBox="0 0 24 24">
      <rect width="24" height="24" rx="4" fill="#1a1a2e"/>
      <path fill="#FFA116" d="M15.7 17.5l1.4 1.4a4.72 4.72 0 01-6.68 0 4.72 4.72 0 010-6.67l3.64-3.65a4.72 4.72 0 016.68 0l.5.5-1.41 1.42-.5-.51a2.73 2.73 0 00-3.86 0l-3.64 3.65a2.73 2.73 0 003.86 3.86l.01-.01z"/>
      <path fill="#FFA116" opacity=".55" d="M8.3 6.5L6.9 5.1a4.72 4.72 0 016.68 0l.5.5-1.41 1.42-.5-.51A2.73 2.73 0 008.3 6.5z"/>
      <rect fill="#FFA116" opacity=".35" x="6.5" y="11.3" width="11" height="1.4" rx=".7"/>
    </symbol>
    <!-- Gmail -->
    <symbol id="L-gmail" viewBox="0 0 24 24">
      <rect width="24" height="24" rx="4" fill="#fff"/>
      <path fill="#EA4335" d="M4 18V8.6l8 5.6 8-5.6V18H4z" opacity=".15"/>
      <path fill="#EA4335" d="M4 8.6L12 14.2l8-5.6V7a1 1 0 00-1-1H5a1 1 0 00-1 1v1.6z"/>
      <path fill="#C5221F" d="M4 8.6V18h2V10.2L4 8.6z"/>
      <path fill="#C5221F" d="M20 8.6V18h-2V10.2l2-1.6z"/>
      <path fill="#FBBC04" d="M4 18h16a0 0 0 000 0H4a0 0 0 000 0z"/>
      <path fill="#4285F4" d="M12 14.2L4 8.6V7a1 1 0 011-1h14a1 1 0 011 1v1.6l-8 5.6z"/>
    </symbol>
    <!-- HTML5 official colors -->
    <symbol id="L-html5" viewBox="0 0 24 24">
      <path fill="#E44D26" d="M3.5 2L5 19.5 12 22l7-2.5L20.5 2z"/>
      <path fill="#F16529" d="M12 20.5V4h6.5L17 18.3z"/>
      <path fill="#EBEBEB" d="M12 10.5H8.75l-.25-2.5H12V5.5H6l.75 8.5H12zm0 5.5l-2.75-.75-.2-2H6.8l.4 4.5L12 19.2z"/>
      <path fill="#fff" d="M12 10.5v3.5h3l-.3 3-2.7.75V20.2l3.4-1 .5-5.2H12V10.5l3.5.25.25-2.75H12V5.5h6.5l-.75 10-5.75 1.75z"/>
    </symbol>
    <!-- CSS3 official colors -->
    <symbol id="L-css3" viewBox="0 0 24 24">
      <path fill="#264DE4" d="M3.5 2L5 19.5 12 22l7-2.5L20.5 2z"/>
      <path fill="#2965F1" d="M12 20.5V4h6.5L17 18.3z"/>
      <path fill="#EBEBEB" d="M12 10.5H8.5l.25 2.5H12V10.5zm-3.75-3H12V5.5H6.25l.75 8.5H12V11.5H7.5z"/>
      <path fill="#fff" d="M12 10.5v2.5h3.25l-.3 3L12 17v2.2l3.5-1 .5-5.2H12V10.5l3.5.25.25-2.75H12V5.5h6.5l-.75 10L12 17.5z"/>
    </symbol>
    <!-- JavaScript official -->
    <symbol id="L-js" viewBox="0 0 24 24">
      <rect width="24" height="24" rx="3" fill="#F7DF1E"/>
      <path fill="#323330" d="M6.8 19.2l1.55-1c.3.54.57.99 1.22.99.62 0 1.01-.25 1.01-1.22V12h1.96v6c0 2.02-1.18 2.94-2.9 2.94-1.55 0-2.46-.81-2.84-1.74zm6.2-.22l1.55-1c.4.66.93 1.14 1.86 1.14.78 0 1.28-.39 1.28-.93 0-.65-.51-.88-1.38-1.26l-.47-.2c-1.38-.59-2.3-1.33-2.3-2.89 0-1.44 1.1-2.53 2.8-2.53 1.21 0 2.08.42 2.7 1.52l-1.48 1.01c-.32-.58-.67-.81-1.22-.81-.56 0-.91.35-.91.81 0 .57.35.8 1.17 1.15l.47.2c1.62.7 2.53 1.41 2.53 3.01 0 1.72-1.35 2.66-3.16 2.66-1.77 0-2.92-.85-3.44-1.88z"/>
    </symbol>
    <!-- Node.js -->
    <symbol id="L-nodejs" viewBox="0 0 24 24">
      <path fill="#339933" d="M12 2.1L2.5 7.5v9l9.5 5.4 9.5-5.4v-9z"/>
      <path fill="#fff" opacity=".15" d="M12 2.1L2.5 7.5 12 12.9 21.5 7.5z"/>
      <path fill="#fff" d="M9.5 15.7c-.28 0-.5-.12-.64-.32l-1.9-2.46-.52.52v1.67c0 .38-.28.58-.62.58-.35 0-.62-.2-.62-.58V9.4c0-.38.27-.58.62-.58.34 0 .62.2.62.58v2.78l2.3-2.85c.18-.22.37-.32.57-.32.37 0 .67.3.67.65 0 .17-.07.33-.2.47l-1.8 2.08 2 2.58c.12.16.18.32.18.48 0 .37-.3.66-.66.66zm4.7 0c-.28 0-.45-.12-.45-.42v-3.94H12.6c-.33 0-.55-.2-.55-.5 0-.29.22-.5.55-.5h2.96c.33 0 .55.21.55.5 0 .3-.22.5-.55.5h-1.12v3.94c0 .3-.17.42-.34.42z"/>
    </symbol>
    <!-- MongoDB leaf -->
    <symbol id="L-mongodb" viewBox="0 0 24 24">
      <rect width="24" height="24" rx="4" fill="#13AA52"/>
      <path fill="#fff" d="M12 3.5s-5 6.3-5 11a5 5 0 0010 0c0-4.7-5-11-5-11z"/>
      <path fill="#13AA52" d="M12 3.5s-3.5 5.5-3.5 10.5a3.5 3.5 0 007 0C15.5 9 12 3.5 12 3.5z" opacity=".4"/>
      <rect x="11.35" y="15.5" width="1.3" height="5" rx=".65" fill="#fff"/>
    </symbol>
    <!-- Brain / DSA -->
    <symbol id="L-dsa" viewBox="0 0 24 24">
      <path fill="none" stroke="#818cf8" stroke-width="1.5" stroke-linecap="round" d="M9 2.5a4 4 0 014 4c0 1.8-1 3.3-2.5 4.1"/>
      <path fill="none" stroke="#818cf8" stroke-width="1.5" stroke-linecap="round" d="M15 2.5a4 4 0 00-4 4c0 1.8 1 3.3 2.5 4.1"/>
      <rect fill="#818cf8" x="8" y="11" width="8" height="2" rx="1"/>
      <rect fill="#818cf8" x="8.5" y="14" width="7" height="2" rx="1"/>
      <rect fill="#818cf8" x="9.5" y="17" width="5" height="2" rx="1"/>
      <rect fill="#818cf8" x="11" y="20" width="2" height="1.5" rx=".75"/>
    </symbol>
    <!-- Globe web -->
    <symbol id="L-web" viewBox="0 0 24 24">
      <circle cx="12" cy="12" r="9" fill="none" stroke="#38bdf8" stroke-width="1.6"/>
      <ellipse cx="12" cy="12" rx="3.5" ry="9" fill="none" stroke="#38bdf8" stroke-width="1.6"/>
      <line x1="3" y1="12" x2="21" y2="12" stroke="#38bdf8" stroke-width="1.6"/>
      <path d="M4.8 7.5Q12 9.5 19.2 7.5" fill="none" stroke="#38bdf8" stroke-width="1.3"/>
      <path d="M4.8 16.5Q12 14.5 19.2 16.5" fill="none" stroke="#38bdf8" stroke-width="1.3"/>
    </symbol>
    <!-- AI robot -->
    <symbol id="L-ai" viewBox="0 0 24 24">
      <rect x="3" y="8" width="18" height="12" rx="3" fill="none" stroke="#34d399" stroke-width="1.6"/>
      <circle cx="9" cy="14" r="1.7" fill="#34d399"/>
      <circle cx="15" cy="14" r="1.7" fill="#34d399"/>
      <rect x="9.5" y="17" width="5" height="1.5" rx=".75" fill="#34d399"/>
      <line x1="12" y1="8" x2="12" y2="5" stroke="#34d399" stroke-width="1.6"/>
      <circle cx="12" cy="4" r="1.5" fill="none" stroke="#34d399" stroke-width="1.5"/>
      <line x1="3" y1="12" x2="1.5" y2="12" stroke="#34d399" stroke-width="1.6" stroke-linecap="round"/>
      <line x1="21" y1="12" x2="22.5" y2="12" stroke="#34d399" stroke-width="1.6" stroke-linecap="round"/>
    </symbol>
    <!-- Moon -->
    <symbol id="L-moon" viewBox="0 0 24 24">
      <path d="M21 12.79A9 9 0 1111.21 3 7 7 0 0021 12.79z" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
    </symbol>
    <!-- Sun -->
    <symbol id="L-sun" viewBox="0 0 24 24">
      <circle cx="12" cy="12" r="5" fill="none" stroke="currentColor" stroke-width="2"/>
      <line x1="12" y1="2" x2="12" y2="4" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
      <line x1="12" y1="20" x2="12" y2="22" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
      <line x1="4.22" y1="4.22" x2="5.64" y2="5.64" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
      <line x1="18.36" y1="18.36" x2="19.78" y2="19.78" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
      <line x1="2" y1="12" x2="4" y2="12" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
      <line x1="20" y1="12" x2="22" y2="12" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
      <line x1="4.22" y1="19.78" x2="5.64" y2="18.36" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
      <line x1="18.36" y1="5.64" x2="19.78" y2="4.22" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
    </symbol>
    <!-- External link -->
    <symbol id="L-ext" viewBox="0 0 24 24">
      <path d="M18 13v6a2 2 0 01-2 2H5a2 2 0 01-2-2V8a2 2 0 012-2h6" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
      <polyline points="15,3 21,3 21,9" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
      <line x1="10" y1="14" x2="21" y2="3" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
    </symbol>
    <!-- Send -->
    <symbol id="L-send" viewBox="0 0 24 24">
      <line x1="22" y1="2" x2="11" y2="13" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
      <polygon points="22,2 15,22 11,13 2,9 22,2" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
    </symbol>
    <!-- Code braces -->
    <symbol id="L-code" viewBox="0 0 24 24">
      <polyline points="16,18 22,12 16,6" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
      <polyline points="8,6 2,12 8,18" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
    </symbol>
    <!-- Check -->
    <symbol id="L-check" viewBox="0 0 24 24">
      <polyline points="20,6 9,17 4,12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"/>
    </symbol>
  </defs>
</svg>
 
<!-- TOAST -->
<div class="toast" id="toast">
  <svg width="16" height="16"><use href="#L-check"/></svg>
  Message sent!
</div>
 
<!-- NAV -->
<nav>
  <div class="nav-logo">PR</div>
  <ul class="nav-links" id="navLinks">
    <li><a href="#about">About</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#achievements">Achievements</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <div style="display:flex;gap:.8rem;align-items:center">
    <button class="theme-btn" id="themeBtn" aria-label="Toggle theme">
      <svg width="18" height="18" id="themeIcon"><use href="#L-moon"/></svg>
    </button>
    <div class="hamburger" id="hamburger" onclick="toggleMenu()">
      <span></span><span></span><span></span>
    </div>
  </div>
</nav>
 
<!-- ════ HERO ════ -->
<section id="hero">
  <div class="hero-bg-orb orb1"></div>
  <div class="hero-bg-orb orb2"></div>
  <div class="hero-grid">
    <div class="hero-content fade-left">
          <h1>Pratik<br><span class="name-highlight">Raj</span></h1>
      <p class="hero-tagline"> Software engineer </p>
      <div class="hero-btns">
        <a href="#projects" class="btn-primary">
          <svg width="16" height="16"><use href="#L-code"/></svg>View Projects
        </a>
        <a href="#contact" class="btn-outline">
          <svg width="16" height="16"><use href="#L-gmail"/></svg>Contact Me
        </a>
      </div>
      <div class="hero-socials">
        <a href="https://linkedin.com/in/pratik-raj-42391433a" target="_blank" class="social-icon li" title="LinkedIn">
          <svg width="22" height="22"><use href="#L-linkedin"/></svg>
        </a>
        <a href="https://github.com/pratikraj423" target="_blank" class="social-icon gh" title="GitHub">
          <svg width="22" height="22"><use href="#L-github"/></svg>
        </a>
        <a href="https://leetcode.com/leetcodecom_pratik845" target="_blank" class="social-icon lc" title="LeetCode">
          <svg width="22" height="22"><use href="#L-leetcode"/></svg>
        </a>
        <a href="mailto:pratikraj4561@gmail.com" class="social-icon em" title="Email">
          <svg width="22" height="22"><use href="#L-gmail"/></svg>
        </a>
      </div>
    </div>
    <div class="hero-visual fade-right">
      <div class="hero-card">
        <div class="avatar-ring">
          <div class="avatar-inner">👨‍💻</div>
        </div>
        <div class="hero-card-name">Pratik Raj</div>
        <div class="hero-card-role">CSDS Student · 3rd Year</div>
        <div class="hero-card-stats">
          <div class="stat"><div class="stat-num">3+</div><div class="stat-label">Projects</div></div>
          <div class="stat"><div class="stat-num">AI</div><div class="stat-label">Focus</div></div>
          <div class="stat"><div class="stat-num">DSA</div><div class="stat-label">Skills</div></div>
        </div>
      </div>
      <div class="float-badge b1">
        <svg width="14" height="14"><use href="#L-check"/></svg>
        Open to Opportunities
      </div>
      <div class="float-badge b2">
        <svg width="14" height="14"><use href="#L-js"/></svg>
        JavaScript · Node.js
      </div>
      <div class="float-badge b3">
        <svg width="14" height="14"><use href="#L-ai"/></svg>
        AI Enthusiast
      </div>
    </div>
  </div>
</section>
 
<!-- ════ ABOUT ════ -->
<section id="about">
  <div class="about-grid">
    <div class="about-left fade-left">
      <div class="about-photo-frame">👨‍💻</div>
      <div class="about-interest-chips">
        <span class="chip"><svg><use href="#L-dsa"/></svg>Data Structures</span>
        <span class="chip"><svg><use href="#L-web"/></svg>Web Dev</span>
        <span class="chip"><svg><use href="#L-ai"/></svg>AI</span>
        <span class="chip">Problem Solving</span>
        <span class="chip"><svg><use href="#L-github"/></svg>Open Source</span>
      </div>
    </div>
    <div class="about-text fade-right">
      <div class="section-tag">Who I Am</div>
      <h2 class="section-title">About<br>Me</h2>
      <p>I'm a 3rd year Computer Science &amp; Data Science student with a genuine passion for coding, problem-solving, and turning ideas into real-world projects. I thrive on the challenge of building systems that actually work.</p>
      <p>My interests span Data Structures &amp; Algorithms, modern Web Development, and the rapidly evolving world of Artificial Intelligence. Every day I push myself to learn something new and stay consistent.</p>
      <div class="about-highlight fade-up">
        <div class="highlight-icon"><svg><use href="#L-dsa"/></svg></div>
        <div class="highlight-text">
          <h4>Data Structures &amp; Algorithms</h4>
          <p>Constantly sharpening problem-solving skills through competitive programming and structured practice.</p>
        </div>
      </div>
      <div class="about-highlight fade-up">
        <div class="highlight-icon"><svg><use href="#L-web"/></svg></div>
        <div class="highlight-text">
          <h4>Web Development</h4>
          <p>Building full-stack experiences from responsive frontends to robust Node.js backends with MongoDB.</p>
        </div>
      </div>
      <div class="about-highlight fade-up">
        <div class="highlight-icon"><svg><use href="#L-ai"/></svg></div>
        <div class="highlight-text">
          <h4>AI Enthusiast</h4>
          <p>Exploring the intersection of AI and real-world applications, integrating intelligent features into projects.</p>
        </div>
      </div>
    </div>
  </div>
</section>
 
<!-- ════ SKILLS ════ -->
<section id="skills">
  <div style="max-width:1100px;margin:0 auto">
    <div class="section-tag fade-up">What I Work With</div>
    <h2 class="section-title fade-up">Technical<br>Skills</h2>
    <div class="skills-grid stagger">
      <div class="skill-card">
        <div class="skill-card-icons">
          <svg width="36" height="36"><use href="#L-html5"/></svg>
          <svg width="36" height="36"><use href="#L-css3"/></svg>
          <svg width="36" height="36"><use href="#L-js"/></svg>
        </div>
        <h3>Programming Languages</h3>
        <div class="skill-pills">
          <span class="skill-pill"><svg><use href="#L-html5"/></svg>HTML5</span>
          <span class="skill-pill"><svg><use href="#L-css3"/></svg>CSS3</span>
          <span class="skill-pill"><svg><use href="#L-js"/></svg>JavaScript</span>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-card-icons">
          <svg width="36" height="36"><use href="#L-nodejs"/></svg>
          <svg width="36" height="36"><use href="#L-mongodb"/></svg>
        </div>
        <h3>Technologies &amp; Frameworks</h3>
        <div class="skill-pills">
          <span class="skill-pill"><svg><use href="#L-nodejs"/></svg>Node.js</span>
          <span class="skill-pill"><svg><use href="#L-mongodb"/></svg>MongoDB</span>
          <span class="skill-pill">REST APIs</span>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-card-icons">
          <svg width="36" height="36"><use href="#L-dsa"/></svg>
          <svg width="36" height="36"><use href="#L-leetcode"/></svg>
          <svg width="36" height="36"><use href="#L-ai"/></svg>
        </div>
        <h3>Core Concepts</h3>
        <div class="skill-pills">
          <span class="skill-pill"><svg><use href="#L-dsa"/></svg>Data Structures</span>
          <span class="skill-pill">Algorithms</span>
          <span class="skill-pill">OOP</span>
          <span class="skill-pill">Problem Solving</span>
        </div>
      </div>
    </div>
  </div>
</section>
 
<!-- ════ PROJECTS ════ -->
<section id="projects">
  <div class="projects-container">
    <div class="section-tag fade-up">What I've Built</div>
    <h2 class="section-title fade-up">Featured<br>Projects</h2>
    <div class="project-card fade-up">
      <!-- AnswerSphere custom SVG logo -->
      <div class="project-visual">
        <svg width="90" height="90" viewBox="0 0 90 90" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <linearGradient id="asG1" x1="0%" y1="0%" x2="100%" y2="100%">
              <stop offset="0%" stop-color="#38bdf8"/>
              <stop offset="100%" stop-color="#818cf8"/>
            </linearGradient>
            <linearGradient id="asG2" x1="0%" y1="0%" x2="100%" y2="100%">
              <stop offset="0%" stop-color="#818cf8"/>
              <stop offset="100%" stop-color="#34d399"/>
            </linearGradient>
            <filter id="glow"><feGaussianBlur stdDeviation="2" result="blur"/><feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge></filter>
          </defs>
          <!-- Outer orbit -->
          <circle cx="45" cy="45" r="40" fill="none" stroke="url(#asG1)" stroke-width="1.5" opacity="0.4" stroke-dasharray="6 4"/>
          <!-- Middle ring -->
          <circle cx="45" cy="45" r="30" fill="none" stroke="url(#asG2)" stroke-width="1" opacity="0.3"/>
          <!-- Chat bubble body -->
          <rect x="17" y="24" width="46" height="32" rx="10" fill="url(#asG1)" filter="url(#glow)"/>
          <!-- Tail -->
          <polygon points="26,56 20,68 40,58" fill="url(#asG1)"/>
          <!-- Typing dots -->
          <circle cx="32" cy="40" r="3.5" fill="#fff"/>
          <circle cx="45" cy="40" r="3.5" fill="#fff" opacity=".8"/>
          <circle cx="58" cy="40" r="3.5" fill="#fff" opacity=".6"/>
          <!-- AI spark star top-right -->
          <path d="M65 20 L67 14 L69 20 L75 22 L69 24 L67 30 L65 24 L59 22 Z" fill="#FFA116"/>
          <circle cx="67" cy="22" r="2" fill="#fff" opacity=".5"/>
          <!-- Small planet dots -->
          <circle cx="15" cy="55" r="3" fill="url(#asG2)" opacity=".7"/>
          <circle cx="75" cy="30" r="2" fill="url(#asG1)" opacity=".6"/>
        </svg>
        <span class="project-visual-label">Answer Sphere</span>
        <div class="project-tech-line"></div>
      </div>
      <div>
        <div class="project-number">01</div>
        <h3 class="project-name">Answer Sphere</h3>
        <p class="project-desc">A chatbot platform where users interact with AI through natural text input. Designed for a fluid, intuitive conversational experience with dynamic, context-aware responses.</p>
        <div class="project-tags">
          <span class="project-tag"><svg><use href="#L-html5"/></svg>HTML</span>
          <span class="project-tag"><svg><use href="#L-css3"/></svg>CSS</span>
          <span class="project-tag"><svg><use href="#L-js"/></svg>JavaScript</span>
          <span class="project-tag"><svg><use href="#L-ai"/></svg>AI Integration</span>
        </div>
        <ul class="project-features">
          <li>Dynamic AI-powered responses to user queries</li>
          <li>Interactive, modern chat UI with smooth animations</li>
          <li>Fully responsive across all devices</li>
        </ul>
        <div class="project-btns">
          <a href="https://github.com/pratikraj423" target="_blank" class="btn-sm primary">
            <svg><use href="#L-github"/></svg>GitHub Repo
          </a>
          <a href="#" class="btn-sm ghost">
            <svg><use href="#L-ext"/></svg>Live Demo
          </a>
        </div>
      </div>
    </div>
  </div>
</section>
 
<!-- ════ ACHIEVEMENTS ════ -->
<section id="achievements">
  <div style="max-width:900px;margin:0 auto">
    <div class="section-tag fade-up">Recognition</div>
    <h2 class="section-title fade-up">Achievements &amp;<br>Certifications</h2>
    <div class="achievements-grid stagger">
      <div class="achievement-card">
        <div class="achievement-icon">
          <!-- Simplilearn-inspired cert badge SVG -->
          <svg width="36" height="36" viewBox="0 0 36 36">
            <defs>
              <linearGradient id="cG" x1="0" y1="0" x2="1" y2="1">
                <stop offset="0%" stop-color="#FF6B35"/>
                <stop offset="100%" stop-color="#FFA116"/>
              </linearGradient>
            </defs>
            <rect x="2" y="4" width="25" height="18" rx="3" fill="url(#cG)"/>
            <rect x="5" y="8" width="15" height="2" rx="1" fill="#fff" opacity=".9"/>
            <rect x="5" y="12" width="11" height="2" rx="1" fill="#fff" opacity=".75"/>
            <rect x="5" y="16" width="7" height="2" rx="1" fill="#fff" opacity=".55"/>
            <!-- HTML5 mini badge -->
            <path d="M22 20l.8 9L27 31l4.2-2 .8-9z" fill="#E44D26"/>
            <path d="M27 30V21h3.5l-.6 7z" fill="#F16529"/>
            <path d="M27 25.5h-1.8l-.1-1.5H27v-1.5h-3.2l.4 5H27zm0 3l-1.4-.4-.1-1H24.3l.2 2.6L27 30V28.5z" fill="#EBEBEB"/>
            <path d="M27 25.5v1.8h1.6l-.2 1.6-1.4.4V30l1.8-.5.25-2.7H27V25.5l1.8.1.1-1.6H27V22.5h3.5l-.4 5.3L27 29v-1.5l1.4-.4.1-1H27z" fill="#fff"/>
          </svg>
        </div>
        <div>
          <h3>HTML Certification</h3>
          <p>Completed certified training in HTML fundamentals and best practices through Simplilearn's professional learning platform.</p>
          <div class="achievement-badge">✓ VERIFIED · SIMPLILEARN</div>
        </div>
      </div>
      <div class="achievement-card">
        <div class="achievement-icon">
          <svg width="36" height="36"><use href="#L-leetcode"/></svg>
        </div>
        <div>
          <h3>Strong Problem-Solver</h3>
          <p>Consistently practicing DSA on LeetCode and competitive platforms, developing a sharp analytical and systematic thinking mindset.</p>
          <div class="achievement-badge">↑ LEETCODE ACTIVE</div>
        </div>
      </div>
    </div>
  </div>
</section>
 
<!-- ════ CONTACT ════ -->
<section id="contact">
  <div class="contact-grid">
    <div class="fade-left">
      <div class="section-tag">Get In Touch</div>
      <h2 class="section-title">Let's<br>Connect</h2>
      <p style="color:var(--text-dim);line-height:1.7;margin-bottom:2rem;font-size:.95rem">Open for internships, collaborations, and interesting conversations. Don't hesitate to reach out!</p>
      <div class="contact-info">
        <a href="mailto:pratikraj4561@gmail.com" class="contact-item c-email">
          <div class="contact-item-icon"><svg><use href="#L-gmail"/></svg></div>
          <div class="contact-item-text"><span>Email</span><strong>pratikraj4561@gmail.com</strong></div>
        </a>
        <a href="https://linkedin.com/in/pratik-raj-42391433a" target="_blank" class="contact-item c-li">
          <div class="contact-item-icon"><svg><use href="#L-linkedin"/></svg></div>
          <div class="contact-item-text"><span>LinkedIn</span><strong>pratik-raj-42391433a</strong></div>
        </a>
        <a href="https://github.com/pratikraj423" target="_blank" class="contact-item c-gh">
          <div class="contact-item-icon"><svg><use href="#L-github"/></svg></div>
          <div class="contact-item-text"><span>GitHub</span><strong>pratikraj423</strong></div>
        </a>
        <a href="https://leetcode.com/leetcodecom_pratik845" target="_blank" class="contact-item c-lc">
          <div class="contact-item-icon"><svg><use href="#L-leetcode"/></svg></div>
          <div class="contact-item-text"><span>LeetCode</span><strong>leetcodecom_pratik845</strong></div>
        </a>
      </div>
    </div>
    <div class="fade-right">
      <div style="padding:2.5rem;border-radius:16px;background:var(--surface);border:1px solid var(--border)">
        <h3 style="font-family:'Syne',sans-serif;font-size:1.3rem;font-weight:700;margin-bottom:1.5rem">Send a Message</h3>
        <div class="contact-form">
          <div class="form-group">
            <label>Your Name</label>
            <input type="text" id="fname" placeholder="John Doe"/>
          </div>
          <div class="form-group">
            <label>Your Email</label>
            <input type="email" id="femail" placeholder="john@example.com"/>
          </div>
          <div class="form-group">
            <label>Message</label>
            <textarea id="fmessage" placeholder="Tell me about your project or opportunity..."></textarea>
          </div>
          <button class="btn-primary" style="width:100%;justify-content:center;font-size:.95rem;padding:1rem 2rem" onclick="sendMessage()">
            <svg width="18" height="18"><use href="#L-send"/></svg>
            Send Message
          </button>
        </div>
      </div>
    </div>
  </div>
</section>
 
<footer>
  <p>Designed &amp; built by <span>Pratik Raj</span> · 2025</p>
  <p style="font-size:.65rem;opacity:.6;margin-top:.3rem">Computer Science &amp; Data Science · Aspiring Developer</p>
</footer>
 
<script>
  const themeBtn = document.getElementById('themeBtn');
  const themeIcon = document.getElementById('themeIcon');
  const html = document.documentElement;
  let isDark = true;
  themeBtn.addEventListener('click', () => {
    isDark = !isDark;
    html.setAttribute('data-theme', isDark ? 'dark' : 'light');
    themeIcon.innerHTML = isDark ? '<use href="#L-moon"/>' : '<use href="#L-sun"/>';
  });
 
  function toggleMenu() { document.getElementById('navLinks').classList.toggle('open'); }
  document.querySelectorAll('.nav-links a').forEach(a =>
    a.addEventListener('click', () => document.getElementById('navLinks').classList.remove('open'))
  );
 
  const observer = new IntersectionObserver(entries =>
    entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); })
  , { threshold: 0.12 });
  document.querySelectorAll('.fade-up,.fade-left,.fade-right,.stagger').forEach(el => observer.observe(el));
 
  setTimeout(() => {
    document.querySelectorAll('#hero .fade-left, #hero .fade-right').forEach((el, i) => {
      el.style.transitionDelay = (i * 0.2) + 's';
      el.classList.add('visible');
    });
  }, 150);
 
  function sendMessage() {
    const name = document.getElementById('fname').value.trim();
    const email = document.getElementById('femail').value.trim();
    const message = document.getElementById('fmessage').value.trim();
    if (!name || !email || !message) { alert('Please fill in all fields.'); return; }
    const toast = document.getElementById('toast');
    toast.classList.add('show');
    ['fname','femail','fmessage'].forEach(id => document.getElementById(id).value = '');
    setTimeout(() => toast.classList.remove('show'), 3500);
  }
 
  const sections = document.querySelectorAll('section[id]');
  window.addEventListener('scroll', () => {
    let current = '';
    sections.forEach(s => { if (window.scrollY >= s.offsetTop - 120) current = s.getAttribute('id'); });
    document.querySelectorAll('.nav-links a').forEach(a =>
      a.style.color = a.getAttribute('href') === '#' + current ? 'var(--accent)' : ''
    );
  });
</script>
</body>
</html>
