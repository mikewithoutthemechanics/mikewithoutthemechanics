<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>mikewithoutthemechanics — On-site AI Engineering · KwaZulu-Natal, South Africa</title>
<meta name="description" content="Michael Graeme Kidd — Managing Partner & Chief AI Architect @ Agentcy. On-site AI engineering, workflow automation, custom internal tools and AI integrations for South African businesses." />
<script>document.documentElement.classList.add('js');</script>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500;700&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  /* ============ TOKENS ============ */
  :root{
    --ink:#0B0E0D;
    --ink-2:#121817;
    --ink-3:#18211E;
    --paper:#F7F4EF;
    --paper-2:#EDE7DD;
    --line-dark:rgba(247,244,239,.12);
    --line-light:rgba(11,14,13,.12);
    --ember:#FF5A2D;
    --ember-2:#FF8A5C;
    --sand:#E4C39B;
    --forest:#16302A;
    --mint:#68C6A8;
    --text-dark:#F1EEE9;
    --muted-dark:#9BA6A1;
    --text-light:#141A18;
    --muted-light:#5B6662;
    --r-sm:10px;
    --r-md:16px;
    --r-lg:24px;
    --r-xl:32px;
    --shadow-soft:0 22px 60px -28px rgba(0,0,0,.55);
    --shadow-card:0 30px 70px -34px rgba(0,0,0,.5);
    --ease-out:cubic-bezier(.19,1,.22,1);
    --ease-spring:cubic-bezier(.34,1.56,.64,1);
    --maxw:1220px;
  }

  *,*::before,*::after{box-sizing:border-box}
  html{scroll-behavior:smooth;-webkit-text-size-adjust:100%}
  body{
    margin:0;
    background:var(--ink);
    color:var(--text-dark);
    font-family:'Inter',system-ui,-apple-system,sans-serif;
    font-size:16px;
    line-height:1.65;
    overflow-x:hidden;
    -webkit-font-smoothing:antialiased;
  }
  img{max-width:100%;display:block}
  a{color:inherit;text-decoration:none}
  button{font-family:inherit}
  ::selection{background:var(--ember);color:#fff}

  .wrap{width:min(100% - 40px,var(--maxw));margin-inline:auto}
  .mono{font-family:'JetBrains Mono',ui-monospace,SFMono-Regular,Menlo,monospace}
  .display{font-family:'Space Grotesk','Inter',sans-serif;letter-spacing:-.025em;line-height:1.02}

  /* ============ SCROLL PROGRESS ============ */
  .scroll-progress{
    position:fixed;top:0;left:0;right:0;height:3px;z-index:120;
    background:transparent;pointer-events:none;
  }
  .scroll-progress i{
    display:block;height:100%;width:0%;
    background:linear-gradient(90deg,var(--ember),var(--sand) 60%,var(--mint));
    box-shadow:0 0 18px rgba(255,90,45,.5);
    transition:width .12s linear;
  }

  /* ============ NAV ============ */
  .nav{
    position:fixed;top:0;left:0;right:0;z-index:110;
    padding:18px 0;
    transition:padding .45s var(--ease-out),background .45s ease,border-color .45s ease,backdrop-filter .45s ease;
    border-bottom:1px solid transparent;
  }
  .nav.scrolled{
    padding:10px 0;
    background:rgba(11,14,13,.86);
    border-bottom-color:var(--line-dark);
    backdrop-filter:blur(14px) saturate(140%);
    -webkit-backdrop-filter:blur(14px) saturate(140%);
  }
  .nav-inner{display:flex;align-items:center;justify-content:space-between;gap:22px}
  .brand{display:flex;align-items:center;gap:12px;font-weight:600;letter-spacing:-.02em}
  .brand-mark{
    width:38px;height:38px;border-radius:11px;flex:none;
    background:linear-gradient(150deg,var(--ember),#D8391A 60%,#8F2312);
    display:grid;place-items:center;
    font-family:'Space Grotesk',sans-serif;font-weight:700;font-size:14px;color:#fff;
    box-shadow:0 12px 26px -12px rgba(255,90,45,.75);
    position:relative;overflow:hidden;
  }
  .brand-mark::after{
    content:"";position:absolute;inset:0;
    background:linear-gradient(115deg,transparent 30%,rgba(255,255,255,.55) 48%,transparent 62%);
    transform:translateX(-120%);animation:sweep 5.5s var(--ease-out) infinite;
  }
  @keyframes sweep{0%,60%{transform:translateX(-120%)}100%{transform:translateX(140%)}}
  .brand-txt{display:flex;flex-direction:column;line-height:1.15}
  .brand-txt b{font-size:15px}
  .brand-txt span{font-size:11px;color:var(--muted-dark);letter-spacing:.14em;text-transform:uppercase}
  .nav-links{display:flex;align-items:center;gap:6px}
  .nav-links a{
    position:relative;padding:9px 14px;border-radius:999px;font-size:14px;color:#CFD6D2;
    transition:color .3s ease,background .3s ease;
  }
  .nav-links a::after{
    content:"";position:absolute;left:14px;right:14px;bottom:5px;height:1.5px;
    background:var(--ember);transform:scaleX(0);transform-origin:left;
    transition:transform .45s var(--ease-out);
  }
  .nav-links a:hover{color:#fff;background:rgba(247,244,239,.06)}
  .nav-links a:hover::after{transform:scaleX(1)}
  .nav-cta{
    display:inline-flex;align-items:center;gap:9px;
    padding:11px 20px;border-radius:999px;font-size:14px;font-weight:600;
    background:var(--paper);color:var(--ink);
    transition:transform .5s var(--ease-spring),box-shadow .5s ease,background .3s ease;
    box-shadow:0 16px 34px -18px rgba(255,255,255,.4);
  }
  .nav-cta:hover{transform:translateY(-2px);background:#fff}
  .nav-cta .dot{width:7px;height:7px;border-radius:50%;background:var(--ember);box-shadow:0 0 0 0 rgba(255,90,45,.6);animation:pulse 2.4s infinite}
  @keyframes pulse{0%{box-shadow:0 0 0 0 rgba(255,90,45,.55)}70%{box-shadow:0 0 0 10px rgba(255,90,45,0)}100%{box-shadow:0 0 0 0 rgba(255,90,45,0)}}
  .burger{display:none;width:44px;height:44px;border-radius:12px;border:1px solid var(--line-dark);background:transparent;cursor:pointer;padding:0;place-items:center}
  .burger span{display:block;width:18px;height:1.6px;background:var(--text-dark);margin:3.6px auto;transition:transform .4s var(--ease-out),opacity .3s ease}
  .burger.open span:nth-child(1){transform:translateY(5.2px) rotate(45deg)}
  .burger.open span:nth-child(2){opacity:0}
  .burger.open span:nth-child(3){transform:translateY(-5.2px) rotate(-45deg)}
  .mobile-menu{
    position:fixed;inset:0 0 auto 0;top:0;padding:92px 22px 30px;z-index:105;
    background:rgba(11,14,13,.97);backdrop-filter:blur(18px);
    transform:translateY(-102%);transition:transform .6s var(--ease-out);
    border-bottom:1px solid var(--line-dark);
  }
  .mobile-menu.open{transform:translateY(0)}
  .mobile-menu a{display:block;padding:14px 6px;font-size:22px;font-family:'Space Grotesk',sans-serif;border-bottom:1px solid var(--line-dark);letter-spacing:-.02em}
  .mobile-menu a:last-of-type{border-bottom:none}

  /* ============ HERO ============ */
  .hero{position:relative;padding:170px 0 90px;overflow:hidden;isolation:isolate}
  .hero-bg{position:absolute;inset:0;z-index:-3;background:
    radial-gradient(1100px 620px at 78% 12%,rgba(255,90,45,.16),transparent 62%),
    radial-gradient(900px 560px at 8% 82%,rgba(104,198,168,.10),transparent 60%),
    linear-gradient(180deg,#0B0E0D 0%,#0D1211 60%,#0B0E0D 100%);}
  .hero-grid{
    position:absolute;inset:0;z-index:-2;opacity:.42;
    background-image:linear-gradient(var(--line-dark) 1px,transparent 1px),linear-gradient(90deg,var(--line-dark) 1px,transparent 1px);
    background-size:72px 72px;
    mask-image:radial-gradient(120% 90% at 50% 20%,#000 20%,transparent 78%);
    -webkit-mask-image:radial-gradient(120% 90% at 50% 20%,#000 20%,transparent 78%);
  }
  .hero-spot{
    position:absolute;width:720px;height:720px;left:0;top:0;z-index:-1;pointer-events:none;
    background:radial-gradient(circle,rgba(255,120,70,.13),transparent 66%);
    transform:translate(-50%,-50%);opacity:0;transition:opacity .7s ease;
  }
  .hero:hover .hero-spot{opacity:1}
  .hero-signal{position:absolute;inset:0;z-index:-1;width:100%;height:100%;opacity:.5;pointer-events:none}
  .hero-signal path{stroke-dasharray:1400;stroke-dashoffset:1400;animation:draw 3.2s var(--ease-out) .3s forwards}
  .hero-signal path.p2{animation-delay:.7s;opacity:.55}
  .hero-signal path.p3{animation-delay:1.1s;opacity:.32}
  @keyframes draw{to{stroke-dashoffset:0}}

  .hero-inner{display:grid;grid-template-columns:1.06fr .94fr;gap:58px;align-items:center}
  .eyebrow{
    display:inline-flex;align-items:center;gap:10px;padding:7px 8px 7px 8px;border-radius:999px;
    border:1px solid var(--line-dark);background:rgba(247,244,239,.05);
    font-size:11.5px;letter-spacing:.16em;text-transform:uppercase;color:#D7DEDA;
  }
  .eyebrow b{
    background:var(--ember);color:#fff;padding:4px 10px;border-radius:999px;font-weight:600;letter-spacing:.1em;
  }
  h1.hero-title{
    font-family:'Space Grotesk',sans-serif;font-weight:600;
    font-size:clamp(2.65rem,6.4vw,5.35rem);line-height:.98;letter-spacing:-.035em;
    margin:26px 0 22px;
  }
  h1.hero-title .accent{
    background:linear-gradient(100deg,var(--ember) 0%,var(--ember-2) 40%,var(--sand) 78%);
    -webkit-background-clip:text;background-clip:text;color:transparent;
    background-size:220% 100%;animation:shift 9s ease-in-out infinite alternate;
  }
  @keyframes shift{0%{background-position:0% 50%}100%{background-position:100% 50%}}
  .hero-lead{font-size:clamp(1.02rem,1.5vw,1.18rem);color:#C2CBC6;max-width:56ch;margin:0 0 26px}
  .hero-lead strong{color:#fff;font-weight:600}
  .focus-list{list-style:none;padding:0;margin:0 0 32px;display:grid;gap:11px;max-width:52ch}
  .focus-list li{
    display:flex;gap:12px;align-items:flex-start;font-size:.955rem;color:#B6BFBA;
    opacity:0;transform:translateX(-14px);
  }
  .focus-list li.in{opacity:1;transform:none;transition:opacity .7s var(--ease-out),transform .7s var(--ease-out)}
  .focus-list .tick{
    flex:none;width:19px;height:19px;border-radius:6px;margin-top:3px;
    border:1px solid rgba(255,90,45,.45);background:rgba(255,90,45,.13);
    display:grid;place-items:center;
  }
  .focus-list .tick svg{width:11px;height:11px;stroke:var(--ember);stroke-width:2.6;fill:none}
  .hero-actions{display:flex;flex-wrap:wrap;gap:13px;align-items:center}
  .btn{
    position:relative;display:inline-flex;align-items:center;gap:11px;
    padding:15px 26px;border-radius:999px;font-weight:600;font-size:.95rem;
    border:1px solid transparent;cursor:pointer;overflow:hidden;
    transition:transform .55s var(--ease-spring),background .35s ease,color .35s ease,border-color .35s ease,box-shadow .5s ease;
    will-change:transform;
  }
  .btn-primary{background:var(--ember);color:#fff;box-shadow:0 24px 50px -22px rgba(255,90,45,.72)}
  .btn-primary:hover{background:#FF6B41;box-shadow:0 30px 60px -20px rgba(255,90,45,.8)}
  .btn-primary::after{
    content:"";position:absolute;inset:0;
    background:linear-gradient(115deg,transparent 32%,rgba(255,255,255,.32) 50%,transparent 64%);
    transform:translateX(-130%);transition:transform .8s var(--ease-out);
  }
  .btn-primary:hover::after{transform:translateX(130%)}
  .btn-ghost{background:rgba(247,244,239,.04);color:var(--text-dark);border-color:var(--line-dark)}
  .btn-ghost:hover{background:rgba(247,244,239,.1);border-color:rgba(247,244,239,.3);transform:translateY(-2px)}
  .btn .arr{transition:transform .5s var(--ease-spring)}
  .btn:hover .arr{transform:translateX(5px)}

  /* hero visual */
  .hero-visual{position:relative;perspective:1200px}
  .visual-photo{
    position:absolute;right:-12px;top:-42px;width:74%;aspect-ratio:4/3.4;border-radius:var(--r-lg);
    overflow:hidden;box-shadow:var(--shadow-card);border:1px solid var(--line-dark);
    transform:rotate(2.6deg);
  }
  .visual-photo img{width:100%;height:100%;object-fit:cover;filter:saturate(.75) contrast(1.06)}
  .visual-photo::after{content:"";position:absolute;inset:0;background:linear-gradient(180deg,rgba(11,14,13,.12),rgba(11,14,13,.62))}
  .code-card{
    position:relative;z-index:2;border-radius:var(--r-lg);overflow:hidden;
    background:linear-gradient(170deg,rgba(24,33,30,.97),rgba(15,20,19,.98));
    border:1px solid rgba(247,244,239,.13);
    box-shadow:0 44px 90px -40px rgba(0,0,0,.85);
    transform:rotate(-1.1deg);
  }
  .code-bar{display:flex;align-items:center;gap:8px;padding:13px 16px;border-bottom:1px solid rgba(247,244,239,.09);background:rgba(247,244,239,.03)}
  .code-bar .d{width:10px;height:10px;border-radius:50%}
  .code-bar .d1{background:#FF5F57}.code-bar .d2{background:#FEBC2E}.code-bar .d3{background:#28C840}
  .code-bar .file{margin-left:8px;font-size:11.5px;color:#8B9793;letter-spacing:.06em}
  .code-body{padding:20px 18px 22px;font-family:'JetBrains Mono',monospace;font-size:12.6px;line-height:1.85;overflow-x:auto}
  .code-body pre{margin:0}
  .tk-key{color:#FF9873}
  .tk-str{color:#9FE0C6}
  .tk-fn{color:#E4C39B}
  .tk-punc{color:#6E7B76}
  .tk-com{color:#5C6A65;font-style:italic}
  .tk-var{color:#EDE8E0}
  .float-chip{
    position:absolute;z-index:3;display:flex;align-items:center;gap:10px;
    padding:11px 16px;border-radius:999px;background:rgba(247,244,239,.94);color:#121817;
    font-size:12.4px;font-weight:600;box-shadow:0 22px 44px -22px rgba(0,0,0,.7);
  }
  .float-chip .sq{width:8px;height:8px;border-radius:2px;background:var(--ember)}
  .chip-a{left:-22px;bottom:64px;animation:bobA 7s ease-in-out infinite}
  .chip-b{right:-8px;bottom:-14px;animation:bobB 8.5s ease-in-out infinite}
  @keyframes bobA{0%,100%{transform:translateY(0) rotate(-2deg)}50%{transform:translateY(-13px) rotate(-1deg)}}
  @keyframes bobB{0%,100%{transform:translateY(0) rotate(2deg)}50%{transform:translateY(-17px) rotate(1deg)}}

  .stat-strip{
    margin-top:74px;display:grid;grid-template-columns:repeat(4,1fr);gap:0;
    border-top:1px solid var(--line-dark);border-bottom:1px solid var(--line-dark);
  }
  .stat{padding:26px 24px;border-right:1px solid var(--line-dark);position:relative;overflow:hidden}
  .stat:last-child{border-right:none}
  .stat .num{font-family:'Space Grotesk',sans-serif;font-size:clamp(1.9rem,3.4vw,2.75rem);font-weight:600;letter-spacing:-.03em;line-height:1}
  .stat .num span{color:var(--ember)}
  .stat .lbl{margin-top:9px;font-size:12px;letter-spacing:.13em;text-transform:uppercase;color:var(--muted-dark)}
  .stat::before{content:"";position:absolute;left:0;top:0;width:100%;height:2px;background:linear-gradient(90deg,var(--ember),transparent);transform:scaleX(0);transform-origin:left;transition:transform .8s var(--ease-out)}
  .stat:hover::before{transform:scaleX(1)}

  /* ============ TICKER ============ */
  .ticker{background:var(--ember);color:#fff;padding:16px 0;overflow:hidden;position:relative}
  .ticker-track{display:flex;width:max-content;animation:slide 38s linear infinite}
  .ticker:hover .ticker-track{animation-play-state:paused}
  .ticker-track span{
    display:inline-flex;align-items:center;gap:22px;padding-right:22px;
    font-family:'Space Grotesk',sans-serif;font-size:clamp(1.05rem,2vw,1.55rem);font-weight:500;letter-spacing:-.015em;white-space:nowrap;
  }
  .ticker-track .sep{width:9px;height:9px;border-radius:50%;background:rgba(255,255,255,.65);flex:none}
  @keyframes slide{from{transform:translateX(0)}to{transform:translateX(-50%)}}

  /* ============ SECTION SHELL ============ */
  section{position:relative}
  .sec{padding:clamp(78px,10vw,132px) 0}
  .sec-light{background:var(--paper);color:var(--text-light)}
  .sec-light-2{background:var(--paper-2);color:var(--text-light)}
  .sec-dark{background:var(--ink);color:var(--text-dark)}
  .sec-head{max-width:820px;margin-bottom:clamp(38px,5vw,62px)}
  .kicker{display:flex;align-items:center;gap:14px;font-size:11.5px;letter-spacing:.22em;text-transform:uppercase;font-weight:600;color:var(--ember);margin-bottom:20px}
  .kicker .rule{height:1.5px;width:0;background:var(--ember);transition:width .9s var(--ease-out) .12s}
  .in .kicker .rule,.kicker.in .rule{width:52px}
  h2.sec-title{
    font-family:'Space Grotesk',sans-serif;font-weight:600;
    font-size:clamp(2.15rem,4.6vw,3.55rem);line-height:1.03;letter-spacing:-.035em;margin:0 0 20px;
  }
  .sec-sub{font-size:clamp(1.02rem,1.5vw,1.18rem);color:var(--muted-light);max-width:62ch;margin:0}
  .sec-dark .sec-sub{color:var(--muted-dark)}

  /* reveal */
  .js .reveal{opacity:0;transform:translateY(28px);transition:opacity .85s var(--ease-out),transform .85s var(--ease-out);transition-delay:var(--d,0s)}
  .js .reveal.in{opacity:1;transform:none}

  /* ============ CAPABILITIES ============ */
  .cap-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
  .cap{
    position:relative;padding:32px 28px 30px;border-radius:var(--r-lg);
    background:#fff;border:1px solid var(--line-light);overflow:hidden;
    transition:transform .6s var(--ease-out),box-shadow .6s ease,border-color .4s ease;
  }
  .cap:hover{transform:translateY(-7px);box-shadow:0 36px 70px -38px rgba(11,14,13,.5);border-color:rgba(255,90,45,.36)}
  .cap::before{
    content:"";position:absolute;left:0;top:0;height:3px;width:100%;
    background:linear-gradient(90deg,var(--ember),var(--sand));transform:scaleX(0);transform-origin:left;
    transition:transform .7s var(--ease-out);
  }
  .cap:hover::before{transform:scaleX(1)}
  .cap .idx{font-family:'JetBrains Mono',monospace;font-size:11.5px;letter-spacing:.16em;color:var(--ember);opacity:.85}
  .cap h3{font-family:'Space Grotesk',sans-serif;font-size:1.32rem;letter-spacing:-.022em;margin:16px 0 12px;font-weight:600}
  .cap p{margin:0;font-size:.95rem;color:var(--muted-light);line-height:1.72}
  .cap .means{
    margin-top:18px;padding-top:16px;border-top:1px dashed rgba(11,14,13,.16);
    display:flex;gap:10px;align-items:flex-start;font-size:.865rem;color:#28322E;
    max-height:0;opacity:0;overflow:hidden;transform:translateY(8px);
    transition:max-height .6s var(--ease-out),opacity .5s ease,transform .55s var(--ease-out),margin .5s ease,padding .5s ease;
  }
  .cap:hover .means,.cap:focus-within .means{max-height:140px;opacity:1;transform:none}
  .cap .means .arrow{flex:none;width:18px;height:18px;border-radius:50%;background:var(--forest);display:grid;place-items:center;margin-top:2px}
  .cap .means .arrow svg{width:10px;height:10px;stroke:var(--sand);stroke-width:3;fill:none}

  /* ============ VENTURES ============ */
  .ventures{display:grid;grid-template-columns:repeat(3,1fr);gap:20px}
  .venture{
    position:relative;border-radius:var(--r-lg);overflow:hidden;min-height:440px;
    display:flex;flex-direction:column;justify-content:flex-end;
    color:#fff;isolation:isolate;
    transition:transform .7s var(--ease-out),box-shadow .7s ease;
  }
  .venture:hover{transform:translateY(-9px);box-shadow:0 46px 90px -42px rgba(0,0,0,.75)}
  .venture .bg{position:absolute;inset:-12% 0;z-index:-2;overflow:hidden}
  .venture .bg img{width:100%;height:100%;object-fit:cover;transform:scale(1.06);transition:transform 1.1s var(--ease-out),filter .8s ease;filter:saturate(.72) brightness(.82)}
  .venture:hover .bg img{transform:scale(1.15);filter:saturate(1) brightness(.9)}
  .venture::after{content:"";position:absolute;inset:0;z-index:-1;background:linear-gradient(180deg,rgba(11,14,13,.05) 22%,rgba(11,14,13,.86) 82%)}
  .venture .body{padding:28px 26px 30px}
  .venture .tag{
    display:inline-flex;align-items:center;gap:8px;padding:6px 13px;border-radius:999px;
    background:rgba(255,255,255,.15);border:1px solid rgba(255,255,255,.25);
    font-size:10.8px;letter-spacing:.16em;text-transform:uppercase;font-weight:600;
    backdrop-filter:blur(6px);-webkit-backdrop-filter:blur(6px);
  }
  .venture h3{font-family:'Space Grotesk',sans-serif;font-size:1.72rem;letter-spacing:-.028em;margin:16px 0 10px;font-weight:600}
  .venture p{margin:0;font-size:.945rem;color:#D8E0DC;line-height:1.68}
  .venture .go{
    margin-top:20px;display:inline-flex;align-items:center;gap:9px;font-size:.875rem;font-weight:600;color:#fff;
  }
  .venture .go .circ{
    width:30px;height:30px;border-radius:50%;border:1px solid rgba(255,255,255,.42);
    display:grid;place-items:center;transition:background .45s ease,transform .5s var(--ease-spring),border-color .45s ease;
  }
  .venture:hover .go .circ{background:var(--ember);border-color:var(--ember);transform:translateX(5px)}
  .venture .go svg{width:12px;height:12px;stroke:#fff;stroke-width:2.4;fill:none}

  /* ============ OPEN TO ============ */
  .open-band{
    border-radius:var(--r-xl);padding:clamp(32px,4.6vw,54px);
    background:linear-gradient(135deg,var(--forest),#0E211C 55%,#1B2320);
    border:1px solid rgba(247,244,239,.1);position:relative;overflow:hidden;
  }
  .open-band::before{
    content:"";position:absolute;width:520px;height:520px;right:-140px;top:-190px;border-radius:50%;
    background:radial-gradient(circle,rgba(255,90,45,.22),transparent 66%);
  }
  .open-band .inner{position:relative;z-index:1;display:grid;grid-template-columns:.85fr 1.15fr;gap:38px;align-items:center}
  .open-band h3{font-family:'Space Grotesk',sans-serif;font-size:clamp(1.75rem,3.2vw,2.55rem);letter-spacing:-.032em;line-height:1.08;margin:0 0 14px}
  .open-band p{margin:0;color:#B6C4BE;font-size:1.02rem}
  .chips{display:flex;flex-wrap:wrap;gap:11px}
  .chip{
    padding:12px 19px;border-radius:999px;font-size:.9rem;font-weight:500;
    background:rgba(247,244,239,.07);border:1px solid rgba(247,244,239,.16);color:#E7EDEA;
    cursor:default;position:relative;overflow:hidden;
    transition:transform .5s var(--ease-spring),background .4s ease,color .4s ease,border-color .4s ease;
  }
  .chip:hover{transform:translateY(-4px);background:var(--ember);color:#fff;border-color:var(--ember)}
  .chip .mono{opacity:.62;font-size:.82em;margin-right:7px}

  /* ============ CREDENTIALS ============ */
  .tabs{display:flex;flex-wrap:wrap;gap:10px;margin-bottom:28px}
  .tab{
    padding:12px 22px;border-radius:999px;border:1px solid var(--line-light);background:transparent;
    font-size:.915rem;font-weight:600;cursor:pointer;color:var(--muted-light);
    transition:all .45s var(--ease-out);
  }
  .tab:hover{color:var(--text-light);border-color:rgba(11,14,13,.32);transform:translateY(-2px)}
  .tab.active{background:var(--ink);color:#fff;border-color:var(--ink);box-shadow:0 22px 44px -22px rgba(11,14,13,.6)}
  .panel{display:none}
  .panel.active{display:block;animation:panelIn .65s var(--ease-out)}
  @keyframes panelIn{from{opacity:0;transform:translateY(16px)}to{opacity:1;transform:none}}
  .cred-table{width:100%;border-collapse:separate;border-spacing:0;background:#fff;border-radius:var(--r-lg);overflow:hidden;border:1px solid var(--line-light)}
  .cred-table th{
    text-align:left;padding:16px 22px;font-size:11px;letter-spacing:.18em;text-transform:uppercase;
    color:var(--muted-light);font-weight:600;background:rgba(11,14,13,.035);border-bottom:1px solid var(--line-light);
  }
  .cred-table td{padding:17px 22px;border-bottom:1px solid rgba(11,14,13,.07);font-size:.945rem;vertical-align:middle}
  .cred-table tr:last-child td{border-bottom:none}
  .cred-table tbody tr{transition:background .35s ease,transform .45s var(--ease-out)}
  .cred-table tbody tr:hover{background:rgba(255,90,45,.06)}
  .cred-table .name{font-weight:600;color:var(--text-light);display:flex;align-items:center;gap:12px}
  .cred-table .name .badge{
    width:30px;height:30px;border-radius:9px;flex:none;display:grid;place-items:center;
    background:var(--paper-2);color:var(--forest);font-family:'JetBrains Mono',monospace;font-size:11px;font-weight:700;
  }
  .date-pill{display:inline-block;padding:5px 12px;border-radius:999px;font-size:.815rem;font-family:'JetBrains Mono',monospace;background:rgba(11,14,13,.06);color:#3B4642}
  .date-pill.ember{background:rgba(255,90,45,.12);color:#C1401C}

  /* ============ STACK ============ */
  .stack-grid{display:grid;grid-template-columns:repeat(5,1fr);gap:16px}
  .stack-col{
    padding:26px 22px 28px;border-radius:var(--r-lg);border:1px solid var(--line-dark);
    background:rgba(247,244,239,.035);position:relative;overflow:hidden;
    transition:background .5s ease,transform .55s var(--ease-out),border-color .5s ease;
  }
  .stack-col:hover{background:rgba(247,244,239,.075);transform:translateY(-6px);border-color:rgba(255,90,45,.35)}
  .stack-col h4{
    font-family:'JetBrains Mono',monospace;font-size:11px;letter-spacing:.17em;text-transform:uppercase;
    color:var(--sand);margin:0 0 18px;display:flex;align-items:center;gap:9px;
  }
  .stack-col h4 i{width:6px;height:6px;background:var(--ember);border-radius:2px;display:block}
  .stack-items{display:flex;flex-wrap:wrap;gap:8px}
  .stack-items span{
    padding:7px 12px;border-radius:8px;font-size:.828rem;color:#D3DCD8;
    background:rgba(247,244,239,.06);border:1px solid rgba(247,244,239,.09);
    transition:all .35s var(--ease-spring);
  }
  .stack-items span:hover{background:var(--ember);color:#fff;border-color:var(--ember);transform:translateY(-3px)}

  /* ============ REPOS ============ */
  .repos{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
  .repo{
    position:relative;display:flex;flex-direction:column;gap:14px;
    padding:26px 24px 24px;border-radius:var(--r-lg);overflow:hidden;
    background:#fff;border:1px solid var(--line-light);
    transition:transform .6s var(--ease-out),box-shadow .6s ease,border-color .5s ease;
  }
  .repo:hover{transform:translateY(-7px);box-shadow:0 40px 80px -40px rgba(11,14,13,.45);border-color:rgba(255,90,45,.32)}
  .repo .shine{
    position:absolute;inset:0;pointer-events:none;
    background:linear-gradient(118deg,transparent 34%,rgba(255,90,45,.13) 50%,transparent 66%);
    transform:translateX(-115%);transition:transform .95s var(--ease-out);
  }
  .repo:hover .shine{transform:translateX(115%)}
  .repo-top{display:flex;align-items:center;justify-content:space-between;gap:12px}
  .repo .visibility{font-size:11px;letter-spacing:.11em;text-transform:uppercase;padding:5px 11px;border:1px solid var(--line-light);border-radius:999px;color:var(--muted-light)}
  .repo .icon{width:34px;height:34px;border-radius:11px;background:var(--paper-2);display:grid;place-items:center}
  .repo .icon svg{width:17px;height:17px;stroke:var(--forest);stroke-width:1.7;fill:none}
  .repo h3{margin:0;font-family:'Space Grotesk',sans-serif;font-size:1.17rem;letter-spacing:-.022em;color:var(--text-light);word-break:break-word}
  .repo h3 a{transition:color .35s ease}
  .repo:hover h3 a{color:var(--ember)}
  .repo p{margin:0;font-size:.915rem;color:var(--muted-light);line-height:1.68;flex:1}
  .repo-meta{display:flex;align-items:center;gap:18px;flex-wrap:wrap;font-size:.835rem;color:var(--muted-light)}
  .lang{display:inline-flex;align-items:center;gap:7px;font-weight:500;color:#3B4642}
  .lang i{width:10px;height:10px;border-radius:50%;display:block}
  .repo-meta .m{display:inline-flex;align-items:center;gap:6px}
  .repo-meta svg{width:14px;height:14px;stroke:currentColor;stroke-width:1.8;fill:none}

  /* ============ ACTIVITY ============ */
  .activity-card{
    background:rgba(247,244,239,.045);border:1px solid var(--line-dark);border-radius:var(--r-xl);
    padding:clamp(24px,3.6vw,42px);
  }
  .activity-top{display:flex;flex-wrap:wrap;align-items:flex-end;justify-content:space-between;gap:22px;margin-bottom:30px}
  .activity-count{font-family:'Space Grotesk',sans-serif;font-size:clamp(2.1rem,4.4vw,3.15rem);letter-spacing:-.035em;line-height:1}
  .activity-count em{font-style:normal;color:var(--ember)}
  .activity-note{color:var(--muted-dark);font-size:.935rem;margin-top:8px}
  .legend{display:flex;align-items:center;gap:9px;font-size:.785rem;color:var(--muted-dark)}
  .legend .cells{display:flex;gap:4px}
  .legend i{width:11px;height:11px;border-radius:3px;display:block}
  .graph-scroll{overflow-x:auto;padding-bottom:10px;scrollbar-width:thin}
  .graph-inner{min-width:820px}
  .months{display:grid;grid-auto-flow:column;grid-auto-columns:minmax(0,1fr);font-size:10.6px;color:var(--muted-dark);margin-bottom:8px;letter-spacing:.06em}
  .months span{white-space:nowrap}
  .graph-body{display:flex;gap:9px}
  .days{display:grid;grid-template-rows:repeat(7,12px);gap:3.4px;font-size:9.6px;color:var(--muted-dark);align-content:start}
  .days span{height:12px;line-height:12px;display:block}
  .cells-grid{display:grid;grid-template-rows:repeat(7,12px);grid-auto-flow:column;grid-auto-columns:12px;gap:3.4px}
  .cell{
    width:12px;height:12px;border-radius:3px;background:rgba(247,244,239,.07);
    opacity:0;transform:scale(.55);
    transition:opacity .5s var(--ease-out),transform .5s var(--ease-spring),background .3s ease,box-shadow .3s ease;
  }
  .cell.shown{opacity:1;transform:none}
  .cell:hover{box-shadow:0 0 0 2px rgba(255,90,45,.6);transform:scale(1.35)}
  .cell.l1{background:rgba(255,90,45,.26)}
  .cell.l2{background:rgba(255,90,45,.5)}
  .cell.l3{background:rgba(255,110,60,.78)}
  .cell.l4{background:#FF5A2D}
  .tooltip{
    position:fixed;z-index:200;pointer-events:none;opacity:0;transform:translateY(6px);
    background:#fff;color:#121817;padding:8px 13px;border-radius:10px;font-size:12.2px;font-weight:600;
    box-shadow:0 22px 46px -18px rgba(0,0,0,.5);transition:opacity .22s ease,transform .22s ease;white-space:nowrap;
  }
  .tooltip.show{opacity:1;transform:none}
  .tooltip span{color:var(--muted-light);font-weight:500}

  .activity-split{display:grid;grid-template-columns:1.1fr .9fr;gap:22px;margin-top:30px}
  .bar-block{background:rgba(247,244,239,.045);border:1px solid var(--line-dark);border-radius:var(--r-lg);padding:26px 26px 22px}
  .bar-block h4{margin:0 0 20px;font-family:'Space Grotesk',sans-serif;font-size:1.12rem;letter-spacing:-.022em}
  .bar-row{margin-bottom:17px}
  .bar-row:last-child{margin-bottom:0}
  .bar-row .top{display:flex;justify-content:space-between;font-size:.865rem;color:#C6CFCB;margin-bottom:9px}
  .bar-row .top b{font-family:'JetBrains Mono',monospace;color:var(--sand);font-weight:600}
  .track{height:8px;border-radius:999px;background:rgba(247,244,239,.09);overflow:hidden}
  .track i{display:block;height:100%;width:0;border-radius:999px;background:linear-gradient(90deg,var(--ember),var(--ember-2));transition:width 1.25s var(--ease-out)}
  .orgs{display:flex;flex-direction:column;gap:12px}
  .org{
    display:flex;align-items:center;gap:14px;padding:15px 17px;border-radius:14px;
    background:rgba(247,244,239,.045);border:1px solid var(--line-dark);
    transition:transform .5s var(--ease-out),background .45s ease,border-color .45s ease;
  }
  .org:hover{transform:translateX(6px);background:rgba(255,90,45,.1);border-color:rgba(255,90,45,.36)}
  .org .av{width:38px;height:38px;border-radius:11px;flex:none;display:grid;place-items:center;font-family:'Space Grotesk',sans-serif;font-weight:700;font-size:13px;color:#fff}
  .org .nm{font-family:'JetBrains Mono',monospace;font-size:.875rem;font-weight:500}
  .org .rl{font-size:.785rem;color:var(--muted-dark)}

  /* ============ CTA ============ */
  .cta{position:relative;overflow:hidden;padding:clamp(84px,11vw,150px) 0;background:var(--ink)}
  .cta-bg{position:absolute;inset:0;z-index:0}
  .cta-bg img{width:100%;height:100%;object-fit:cover;opacity:.24;filter:saturate(.55) contrast(1.1)}
  .cta-bg::after{content:"";position:absolute;inset:0;background:linear-gradient(180deg,rgba(11,14,13,.86),rgba(11,14,13,.94))}
  .cta-inner{position:relative;z-index:1;text-align:center;max-width:920px;margin-inline:auto}
  .cta h2{
    font-family:'Space Grotesk',sans-serif;font-weight:600;letter-spacing:-.042em;line-height:.99;
    font-size:clamp(2.55rem,7vw,5.35rem);margin:0 0 24px;
  }
  .cta h2 .sweep{
    background:linear-gradient(100deg,var(--sand),var(--ember) 38%,#fff 62%,var(--ember) 82%,var(--sand));
    background-size:220% 100%;-webkit-background-clip:text;background-clip:text;color:transparent;
    animation:shift 8s linear infinite alternate;
  }
  .cta p{color:#C3CCC7;font-size:clamp(1.02rem,1.8vw,1.24rem);margin:0 auto 36px;max-width:60ch}
  .cta-actions{display:flex;flex-wrap:wrap;gap:14px;justify-content:center}
  .btn-sand{background:var(--sand);color:#26201A}
  .btn-sand:hover{background:#F0D4B2}

  /* ============ FOOTER ============ */
  footer{background:#080B0A;border-top:1px solid var(--line-dark);padding:46px 0 40px}
  .foot-inner{display:flex;flex-wrap:wrap;align-items:center;justify-content:space-between;gap:22px}
  .foot-motto{
    display:flex;flex-wrap:wrap;align-items:center;gap:11px;font-family:'JetBrains Mono',monospace;
    font-size:12.6px;color:var(--muted-dark);letter-spacing:.03em;
  }
  .foot-motto b{color:var(--ember);font-weight:500}
  .foot-links{display:flex;gap:8px;flex-wrap:wrap}
  .foot-links a{
    padding:9px 15px;border-radius:999px;border:1px solid var(--line-dark);font-size:.855rem;color:#C2CBC6;
    transition:all .4s var(--ease-out);
  }
  .foot-links a:hover{background:var(--ember);border-color:var(--ember);color:#fff;transform:translateY(-3px)}
  .foot-bottom{margin-top:30px;padding-top:22px;border-top:1px solid var(--line-dark);display:flex;flex-wrap:wrap;gap:12px;justify-content:space-between;font-size:.815rem;color:#69736F}

  /* ============ RESPONSIVE ============ */
  @media (max-width:1080px){
    .cap-grid{grid-template-columns:repeat(2,1fr)}
    .stack-grid{grid-template-columns:repeat(3,1fr)}
    .ventures{grid-template-columns:1fr;gap:18px}
    .venture{min-height:360px}
    .activity-split{grid-template-columns:1fr}
  }
  @media (max-width:900px){
    .nav-links,.nav-cta{display:none}
    .burger{display:grid}
    .hero{padding:132px 0 70px}
    .hero-inner{grid-template-columns:1fr;gap:64px}
    .hero-visual{max-width:520px;margin-inline:auto;width:100%}
    .stat-strip{grid-template-columns:repeat(2,1fr)}
    .stat:nth-child(2){border-right:none}
    .stat:nth-child(1),.stat:nth-child(2){border-bottom:1px solid var(--line-dark)}
    .open-band .inner{grid-template-columns:1fr;gap:26px}
    .repos{grid-template-columns:1fr}
  }
  @media (max-width:640px){
    .wrap{width:min(100% - 28px,var(--maxw))}
    .cap-grid{grid-template-columns:1fr}
    .stack-grid{grid-template-columns:1fr 1fr}
    .visual-photo{width:82%;top:-30px;right:-6px}
    .float-chip{font-size:11px;padding:9px 13px}
    .chip-a{left:-8px;bottom:52px}
    .chip-b{right:-4px;bottom:-18px}
    .cred-table thead{display:none}
    .cred-table,.cred-table tbody,.cred-table tr,.cred-table td{display:block;width:100%}
    .cred-table tr{padding:12px 4px;border-bottom:1px solid rgba(11,14,13,.08)}
    .cred-table td{border:none;padding:7px 16px}
    .cred-table td::before{content:attr(data-label);display:block;font-size:10px;letter-spacing:.15em;text-transform:uppercase;color:var(--muted-light);margin-bottom:5px}
    .btn{width:100%;justify-content:center}
    .hero-actions{flex-direction:column;align-items:stretch}
    .foot-inner{flex-direction:column;align-items:flex-start}
  }
  @media (prefers-reduced-motion:reduce){
    *,*::before,*::after{animation-duration:.001ms !important;animation-iteration-count:1 !important;transition-duration:.001ms !important;scroll-behavior:auto !important}
    .js .reveal{opacity:1 !important;transform:none !important}
  }
</style>
</head>
<body>

<div class="scroll-progress"><i id="progressBar"></i></div>

<!-- ================= NAV ================= -->
<header class="nav" id="nav">
  <div class="wrap nav-inner">
    <a class="brand" href="#top" aria-label="mikewithoutthemechanics home">
      <div class="brand-mark">MK</div>
      <div class="brand-txt">
        <b>mikewithoutthemechanics</b>
        <span>AI Engineering · ZA</span>
      </div>
    </a>
    <nav class="nav-links" aria-label="Primary">
      <a href="#capabilities">Capabilities</a>
      <a href="#ventures">Ventures</a>
      <a href="#credentials">Credentials</a>
      <a href="#stack">Stack</a>
      <a href="#activity">Activity</a>
    </nav>
    <a class="nav-cta magnetic" href="#contact"><span class="dot"></span> Start a project</a>
    <button class="burger" id="burger" aria-label="Toggle menu" aria-expanded="false">
      <span></span><span></span><span></span>
    </button>
  </div>
</header>

<div class="mobile-menu" id="mobileMenu">
  <a href="#capabilities">Capabilities</a>
  <a href="#ventures">Ventures</a>
  <a href="#credentials">Credentials</a>
  <a href="#stack">Stack</a>
  <a href="#activity">Activity</a>
  <a href="#contact">Start a project</a>
</div>

<!-- ================= HERO ================= -->
<main id="top">
<section class="hero" id="hero">
  <div class="hero-bg"></div>
  <div class="hero-grid"></div>
  <div class="hero-spot" id="heroSpot"></div>
  <svg class="hero-signal" viewBox="0 0 1440 720" preserveAspectRatio="none" aria-hidden="true">
    <defs>
      <linearGradient id="sigGrad" x1="0" y1="0" x2="1" y2="1">
        <stop offset="0%" stop-color="#FF5A2D" stop-opacity="0"/>
        <stop offset="45%" stop-color="#FF5A2D" stop-opacity=".85"/>
        <stop offset="100%" stop-color="#E4C39B" stop-opacity="0"/>
      </linearGradient>
    </defs>
    <path class="p1" d="M-40,520 C220,470 320,300 560,300 C820,300 900,520 1180,470 C1330,442 1400,380 1500,330" stroke="url(#sigGrad)" stroke-width="1.6" fill="none"/>
    <path class="p2" d="M-40,620 C260,600 380,420 620,420 C880,420 980,610 1240,560 C1370,536 1430,500 1500,470" stroke="url(#sigGrad)" stroke-width="1.3" fill="none"/>
    <path class="p3" d="M-40,410 C200,360 340,190 580,190 C840,190 940,380 1200,330 C1350,302 1420,262 1500,220" stroke="url(#sigGrad)" stroke-width="1.1" fill="none"/>
  </svg>

  <div class="wrap hero-inner">
    <div class="hero-copy">
      <div class="eyebrow reveal"><b>Agentcy</b> Managing Partner &amp; Chief AI Architect</div>

      <h1 class="hero-title kin" data-split>On-site AI engineering for businesses that <span class="accent">need to move.</span></h1>

      <p class="hero-lead reveal" style="--d:.25s">
        I'm <strong>Michael Graeme Kidd</strong> — building workflow automation, custom internal tools and
        AI integrations that fit the actual job. Based in <strong>KwaZulu-Natal, South Africa</strong>,
        deployed anywhere the work is.
      </p>

      <ul class="focus-list" id="focusList">
        <li><span class="tick"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg></span> On-site AI engineering for South African businesses</li>
        <li><span class="tick"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg></span> Workflow automation that removes operational drag</li>
        <li><span class="tick"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg></span> Custom internal tools that actually fit the job</li>
        <li><span class="tick"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg></span> AI integrations into existing systems — CRM, WhatsApp, finance</li>
      </ul>

      <div class="hero-actions">
        <a href="#contact" class="btn btn-primary magnetic">
          Book an on-site engagement
          <svg class="arr" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg>
        </a>
        <a href="#capabilities" class="btn btn-ghost magnetic">
          Explore capabilities
          <svg class="arr" width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><polyline points="6 9 12 15 18 9"/></svg>
        </a>
      </div>
    </div>

    <div class="hero-visual reveal" style="--d:.3s">
      <div class="visual-photo" data-parallax="0.05">
        <img src="https://images.unsplash.com/photo-1518770660439-4636190af475?auto=format&fit=crop&w=1100&q=80" alt="Macro shot of a circuit board representing applied AI engineering" loading="lazy">
      </div>

      <div class="code-card" data-parallax="-0.03">
        <div class="code-bar">
          <i class="d d1"></i><i class="d d2"></i><i class="d d3"></i>
          <span class="file mono">mike.config.ts</span>
        </div>
        <div class="code-body">
<pre><span class="tk-key">const</span> <span class="tk-var">mike</span> <span class="tk-punc">=</span> <span class="tk-punc">{</span>
  <span class="tk-key">role</span><span class="tk-punc">:</span> <span class="tk-str">"Managing Partner &amp; Chief AI Architect"</span><span class="tk-punc">,</span>
  <span class="tk-key">location</span><span class="tk-punc">:</span> <span class="tk-str">"KwaZulu-Natal, South Africa 🇿🇦"</span><span class="tk-punc">,</span>
  <span class="tk-key">focus</span><span class="tk-punc">:</span> <span class="tk-punc">[</span>
    <span class="tk-str">"On-site AI engineering"</span><span class="tk-punc">,</span>
    <span class="tk-str">"Workflow automation"</span><span class="tk-punc">,</span>
    <span class="tk-str">"Custom internal tools"</span><span class="tk-punc">,</span>
    <span class="tk-str">"AI systems integration"</span><span class="tk-punc">,</span>
  <span class="tk-punc">],</span>
  <span class="tk-key">ventures</span><span class="tk-punc">:</span> <span class="tk-punc">{</span>
    <span class="tk-key">Agentcy</span><span class="tk-punc">:</span> <span class="tk-str">"AI engineers on-site anywhere in ZA"</span><span class="tk-punc">,</span>
    <span class="tk-key">Integr8</span><span class="tk-punc">:</span> <span class="tk-str">"AI infrastructure &amp; automation"</span><span class="tk-punc">,</span>
    <span class="tk-key">AgencyOS</span><span class="tk-punc">:</span> <span class="tk-str">"OS for modern agencies"</span><span class="tk-punc">,</span>
  <span class="tk-punc">},</span>
  <span class="tk-key">status</span><span class="tk-punc">:</span> <span class="tk-str">"open_to_build"</span><span class="tk-punc">,</span>
<span class="tk-punc">}</span>

<span class="tk-com">// ship it, then make it fast</span>
<span class="tk-fn">deploy</span><span class="tk-punc">(</span><span class="tk-var">mike</span><span class="tk-punc">.</span><span class="tk-key">focus</span><span class="tk-punc">, {</span> <span class="tk-key">onSite</span><span class="tk-punc">:</span> <span class="tk-key">true</span> <span class="tk-punc">})</span></pre>
        </div>
      </div>

      <div class="float-chip chip-a"><i class="sq"></i> On-site · Anywhere in South Africa</div>
      <div class="float-chip chip-b"><i class="sq"></i> 1,046 contributions · last 12 months</div>
    </div>
  </div>

  <div class="wrap">
    <div class="stat-strip">
      <div class="stat reveal"><div class="num"><span data-count="1046">0</span></div><div class="lbl">Contributions / year</div></div>
      <div class="stat reveal" style="--d:.1s"><div class="num"><span data-count="3">0</span></div><div class="lbl">Active ventures</div></div>
      <div class="stat reveal" style="--d:.2s"><div class="num"><span data-count="11">0</span>+</div><div class="lbl">Certifications &amp; courses</div></div>
      <div class="stat reveal" style="--d:.3s"><div class="num"><span data-count="135">0</span></div><div class="lbl">Repositories contributed to</div></div>
    </div>
  </div>
</section>

<!-- ================= TICKER ================= -->
<div class="ticker" aria-hidden="true">
  <div class="ticker-track" id="tickerTrack">
    <span>Workflow Automation <i class="sep"></i> AI Integration <i class="sep"></i> Custom Internal Tools <i class="sep"></i> WhatsApp + CRM Systems <i class="sep"></i> Full-Stack Product Engineering <i class="sep"></i> Agency Systems <i class="sep"></i></span>
    <span>Workflow Automation <i class="sep"></i> AI Integration <i class="sep"></i> Custom Internal Tools <i class="sep"></i> WhatsApp + CRM Systems <i class="sep"></i> Full-Stack Product Engineering <i class="sep"></i> Agency Systems <i class="sep"></i></span>
  </div>
</div>

<!-- ================= CAPABILITIES ================= -->
<section class="sec sec-light" id="capabilities">
  <div class="wrap">
    <div class="sec-head reveal">
      <div class="kicker"><i class="rule"></i> Capability Matrix</div>
      <h2 class="sec-title">What I build — and what it changes for you.</h2>
      <p class="sec-sub">No dashboards for the sake of dashboards. Every engagement starts with the operational drag you can actually feel, and ends with software your team wants to use.</p>
    </div>

    <div class="cap-grid">
      <article class="cap reveal" tabindex="0">
        <div class="idx mono">01 / AUTOMATE</div>
        <h3>Workflow Automation</h3>
        <p>Map the way work really moves through your business, then remove every manual handoff that slows people down.</p>
        <div class="means"><span class="arrow"><svg viewBox="0 0 24 24"><polyline points="9 18 15 12 9 6"/></svg></span> What that means for you: hours back every week, fewer dropped balls, and processes that run whether or not someone remembers.</div>
      </article>

      <article class="cap reveal" style="--d:.08s" tabindex="0">
        <div class="idx mono">02 / INTEGRATE</div>
        <h3>AI Integration</h3>
        <p>Embed AI into the tools your team already lives in — not another login, not another dashboard to check.</p>
        <div class="means"><span class="arrow"><svg viewBox="0 0 24 24"><polyline points="9 18 15 12 9 6"/></svg></span> What that means for you: adoption that actually sticks, because the intelligence shows up where the work already happens.</div>
      </article>

      <article class="cap reveal" style="--d:.16s" tabindex="0">
        <div class="idx mono">03 / BUILD</div>
        <h3>Custom Internal Tools</h3>
        <p>Software that fits the actual job instead of forcing the job to fit the software.</p>
        <div class="means"><span class="arrow"><svg viewBox="0 0 24 24"><polyline points="9 18 15 12 9 6"/></svg></span> What that means for you: less workaround sprawl, one source of truth, and tools that match how your team thinks.</div>
      </article>

      <article class="cap reveal" tabindex="0">
        <div class="idx mono">04 / CONNECT</div>
        <h3>WhatsApp + CRM Systems</h3>
        <p>Lead capture, follow-ups and CRM sync that actually work in South Africa — where WhatsApp is the front door.</p>
        <div class="means"><span class="arrow"><svg viewBox="0 0 24 24"><polyline points="9 18 15 12 9 6"/></svg></span> What that means for you: no leads lost in a chat thread, and a pipeline that reflects reality in real time.</div>
      </article>

      <article class="cap reveal" style="--d:.08s" tabindex="0">
        <div class="idx mono">05 / SHIP</div>
        <h3>Full-Stack Product Engineering</h3>
        <p>Clean interfaces, solid APIs, and infrastructure that scales past the pilot without a rewrite.</p>
        <div class="means"><span class="arrow"><svg viewBox="0 0 24 24"><polyline points="9 18 15 12 9 6"/></svg></span> What that means for you: products that hold up under real users, real data and real deadlines.</div>
      </article>

      <article class="cap reveal" style="--d:.16s" tabindex="0">
        <div class="idx mono">06 / SYSTEMISE</div>
        <h3>Agency Systems</h3>
        <p>Tools and operating systems built specifically for creative &amp; digital agencies — not generic PM software.</p>
        <div class="means"><span class="arrow"><svg viewBox="0 0 24 24"><polyline points="9 18 15 12 9 6"/></svg></span> What that means for you: delivery, capacity and margin visible in one place, so the studio runs like a product.</div>
      </article>
    </div>
  </div>
</section>

<!-- ================= VENTURES ================= -->
<section class="sec sec-dark" id="ventures">
  <div class="wrap">
    <div class="sec-head reveal">
      <div class="kicker"><i class="rule"></i> Ventures</div>
      <h2 class="sec-title">Three companies. One operating thesis.</h2>
      <p class="sec-sub">Build the infrastructure, put engineers on-site, and give teams systems that match the way they actually work.</p>
    </div>

    <div class="ventures">
      <article class="venture reveal">
        <div class="bg"><img src="https://images.unsplash.com/photo-1522071820081-009f0129c71c?auto=format&fit=crop&w=1000&q=80" alt="Engineering team collaborating on-site" loading="lazy"></div>
        <div class="body">
          <span class="tag">Flagship</span>
          <h3>Agentcy</h3>
          <p>AI engineers on-site anywhere in South Africa. Embedded delivery teams that sit inside your operation and ship.</p>
          <a class="go" href="#contact">Work with Agentcy
            <span class="circ"><svg viewBox="0 0 24 24"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg></span>
          </a>
        </div>
      </article>

      <article class="venture reveal" style="--d:.12s">
        <div class="bg"><img src="https://images.unsplash.com/photo-1451187580459-43490279c0fa?auto=format&fit=crop&w=1000&q=80" alt="Global network infrastructure visualisation" loading="lazy"></div>
        <div class="body">
          <span class="tag">Infrastructure</span>
          <h3>Integr8 AI</h3>
          <p>AI infrastructure &amp; automation for businesses that need to move — integrations, pipelines and agents that hold up in production.</p>
          <a class="go" href="#contact">Explore Integr8
            <span class="circ"><svg viewBox="0 0 24 24"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg></span>
          </a>
        </div>
      </article>

      <article class="venture reveal" style="--d:.24s">
        <div class="bg"><img src="https://images.unsplash.com/photo-1497215728101-856f4ea42174?auto=format&fit=crop&w=1000&q=80" alt="Modern agency studio workspace" loading="lazy"></div>
        <div class="body">
          <span class="tag">Product</span>
          <h3>Agency-OS</h3>
          <p>The operating system for modern creative &amp; digital agencies — capacity, delivery and margin in one clean surface.</p>
          <a class="go" href="#contact">See Agency-OS
            <span class="circ"><svg viewBox="0 0 24 24"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg></span>
          </a>
        </div>
      </article>
    </div>

    <!-- OPEN TO -->
    <div class="open-band reveal" style="margin-top:26px">
      <div class="inner">
        <div>
          <h3>Open to the work that matters.</h3>
          <p>Short sprints, long builds, or a seat at the table as a technical co-founder. If it removes operational drag, it's interesting.</p>
        </div>
        <div class="chips">
          <div class="chip"><span class="mono">01</span>AI Consulting</div>
          <div class="chip"><span class="mono">02</span>On-site Engineering Engagements</div>
          <div class="chip"><span class="mono">03</span>Product Builds</div>
          <div class="chip"><span class="mono">04</span>Automation Projects</div>
          <div class="chip"><span class="mono">05</span>Technical Co-founder</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ================= CREDENTIALS ================= -->
<section class="sec sec-light-2" id="credentials">
  <div class="wrap">
    <div class="sec-head reveal">
      <div class="kicker"><i class="rule"></i> Credentials</div>
      <h2 class="sec-title">Certified where it counts.</h2>
      <p class="sec-sub">Formal certification and continued study across the two platforms shaping modern AI delivery.</p>
    </div>

    <div class="tabs reveal" role="tablist" aria-label="Credential providers">
      <button class="tab active" role="tab" aria-selected="true" data-tab="google">Google · Certification</button>
      <button class="tab" role="tab" aria-selected="false" data-tab="anthropic">Anthropic Education · Courses</button>
    </div>

    <div class="panel active" id="panel-google" role="tabpanel">
      <table class="cred-table">
        <thead>
          <tr><th>Credential</th><th>Issued</th><th>Valid until</th></tr>
        </thead>
        <tbody>
          <tr>
            <td data-label="Credential"><span class="name"><span class="badge">G</span> Gemini Certified Educator</span></td>
            <td data-label="Issued"><span class="date-pill">Oct 2025</span></td>
            <td data-label="Valid until"><span class="date-pill ember">Oct 2028</span></td>
          </tr>
        </tbody>
      </table>
    </div>

    <div class="panel" id="panel-anthropic" role="tabpanel">
      <table class="cred-table">
        <thead>
          <tr><th>Course</th><th>Completed</th><th>Track</th></tr>
        </thead>
        <tbody id="anthropicRows"></tbody>
      </table>
    </div>
  </div>
</section>

<!-- ================= STACK ================= -->
<section class="sec sec-dark" id="stack">
  <div class="wrap">
    <div class="sec-head reveal">
      <div class="kicker"><i class="rule"></i> Toolchain</div>
      <h2 class="sec-title">The stack behind the systems.</h2>
      <p class="sec-sub">Pragmatic choices, boring where it should be boring, modern where it creates leverage.</p>
    </div>

    <div class="stack-grid">
      <div class="stack-col reveal">
        <h4><i></i> AI &amp; Agents</h4>
        <div class="stack-items">
          <span>Claude</span><span>Gemini</span><span>OpenAI</span><span>LangGraph</span><span>RAG</span><span>MCP</span><span>Agent Skills</span><span>Vector Search</span>
        </div>
      </div>
      <div class="stack-col reveal" style="--d:.08s">
        <h4><i></i> Languages</h4>
        <div class="stack-items">
          <span>TypeScript</span><span>Python</span><span>JavaScript</span><span>SQL</span><span>Bash</span><span>HTML / CSS</span>
        </div>
      </div>
      <div class="stack-col reveal" style="--d:.16s">
        <h4><i></i> Frontend &amp; Design</h4>
        <div class="stack-items">
          <span>React</span><span>Next.js</span><span>Tailwind</span><span>Design Systems</span><span>Figma</span><span>Motion</span>
        </div>
      </div>
      <div class="stack-col reveal" style="--d:.24s">
        <h4><i></i> Backend · Data · Infra</h4>
        <div class="stack-items">
          <span>Node.js</span><span>PostgreSQL</span><span>Supabase</span><span>Docker</span><span>REST / GraphQL</span><span>Cloud Deploy</span>
        </div>
      </div>
      <div class="stack-col reveal" style="--d:.32s">
        <h4><i></i> Automation &amp; Ops</h4>
        <div class="stack-items">
          <span>WhatsApp API</span><span>CRM Sync</span><span>Webhooks</span><span>n8n</span><span>CI / CD</span><span>Observability</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ================= PINNED REPOS ================= -->
<section class="sec sec-light" id="repos">
  <div class="wrap">
    <div class="sec-head reveal">
      <div class="kicker"><i class="rule"></i> Pinned</div>
      <h2 class="sec-title">Selected work from the workbench.</h2>
      <p class="sec-sub">A slice of what ships — production deploys, personal blueprints and the experiments in between.</p>
    </div>

    <div class="repos">
      <article class="repo reveal">
        <div class="shine"></div>
        <div class="repo-top">
          <div class="icon"><svg viewBox="0 0 24 24"><path d="M4 4h16v16H4z"/><path d="M4 9h16"/><path d="M9 9v11"/></svg></div>
          <span class="visibility">Public</span>
        </div>
        <h3><a href="#repos">Michael-Graeme-Kidd---Portfolio</a></h3>
        <p>Personal portfolio site — a fast, accessible front door for the engineering work and the ventures.</p>
        <div class="repo-meta">
          <span class="lang"><i style="background:#E34F26"></i> HTML</span>
          <span class="m"><svg viewBox="0 0 24 24"><path d="M12 2v20"/><path d="M2 12h20"/></svg> Updated recently</span>
        </div>
      </article>

      <article class="repo reveal" style="--d:.12s">
        <div class="shine"></div>
        <div class="repo-top">
          <div class="icon"><svg viewBox="0 0 24 24"><circle cx="12" cy="12" r="9"/><path d="M12 7v5l3 2"/></svg></div>
          <span class="visibility">Public</span>
        </div>
        <h3><a href="#repos">punctual-plumbers-pp-edit1-prod</a></h3>
        <p>PP-EDIT1 production deploy — booking, dispatch and field-service workflow tooling built for real operations.</p>
        <div class="repo-meta">
          <span class="lang"><i style="background:#3178C6"></i> TypeScript</span>
          <span class="m"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg> Production</span>
        </div>
      </article>

      <article class="repo reveal" style="--d:.24s">
        <div class="shine"></div>
        <div class="repo-top">
          <div class="icon"><svg viewBox="0 0 24 24"><path d="M3 7l9-4 9 4-9 4-9-4z"/><path d="M3 12l9 4 9-4"/><path d="M3 17l9 4 9-4"/></svg></div>
          <span class="visibility">Public fork</span>
        </div>
        <h3><a href="#repos">retail-agentic-commerce</a></h3>
        <p>Personal fork of the Retail-Agentic-Commerce blueprint — agentic shopping flows and commerce automation.</p>
        <div class="repo-meta">
          <span class="lang"><i style="background:#3572A5"></i> Python</span>
          <span class="m"><svg viewBox="0 0 24 24"><circle cx="6" cy="6" r="3"/><circle cx="6" cy="18" r="3"/><path d="M6 9v6"/><path d="M18 6a3 3 0 1 0 0 6h-6"/></svg> Fork</span>
        </div>
      </article>
    </div>
  </div>
</section>

<!-- ================= ACTIVITY ================= -->
<section class="sec sec-dark" id="activity">
  <div class="wrap">
    <div class="sec-head reveal">
      <div class="kicker"><i class="rule"></i> Contribution Graph</div>
      <h2 class="sec-title">A year of shipping in public.</h2>
      <p class="sec-sub">Consistency over spectacle — the day-to-day engineering cadence behind the products.</p>
    </div>

    <div class="activity-card reveal">
      <div class="activity-top">
        <div>
          <div class="activity-count"><em><span data-count="1046">0</span></em> contributions in the last year</div>
          <div class="activity-note">Contributed to <strong>AgentPing</strong>, <strong>PropAgent</strong>, <strong>propagent-sequel</strong> and 132 other repositories.</div>
        </div>
        <div class="legend">
          Less
          <div class="cells">
            <i style="background:rgba(247,244,239,.07)"></i>
            <i style="background:rgba(255,90,45,.26)"></i>
            <i style="background:rgba(255,90,45,.5)"></i>
            <i style="background:rgba(255,110,60,.78)"></i>
            <i style="background:#FF5A2D"></i>
          </div>
          More
        </div>
      </div>

      <div class="graph-scroll">
        <div class="graph-inner">
          <div class="months" id="monthsRow"></div>
          <div class="graph-body">
            <div class="days">
              <span></span><span>Mon</span><span></span><span>Wed</span><span></span><span>Fri</span><span></span>
            </div>
            <div class="cells-grid" id="cellsGrid"></div>
          </div>
        </div>
      </div>
    </div>

    <div class="activity-split">
      <div class="bar-block reveal">
        <h4>Activity overview</h4>
        <div class="bar-row">
          <div class="top"><span>Commits</span><b>78%</b></div>
          <div class="track"><i data-bar="78"></i></div>
        </div>
        <div class="bar-row">
          <div class="top"><span>Pull requests</span><b>15%</b></div>
          <div class="track"><i data-bar="15"></i></div>
        </div>
        <div class="bar-row">
          <div class="top"><span>Issues</span><b>6%</b></div>
          <div class="track"><i data-bar="6"></i></div>
        </div>
        <div class="bar-row">
          <div class="top"><span>Code review</span><b>1%</b></div>
          <div class="track"><i data-bar="1"></i></div>
        </div>
      </div>

      <div class="bar-block reveal" style="--d:.12s">
        <h4>Organisations &amp; collaborators</h4>
        <div class="orgs">
          <div class="org">
            <div class="av" style="background:linear-gradient(140deg,#FF5A2D,#B93618)">BA</div>
            <div><div class="nm">@bridgeautonomousnetwork</div><div class="rl">Autonomous systems &amp; agent infrastructure</div></div>
          </div>
          <div class="org">
            <div class="av" style="background:linear-gradient(140deg,#68C6A8,#1D6152)">AN</div>
            <div><div class="nm">@anomalyco</div><div class="rl">Applied AI research &amp; delivery</div></div>
          </div>
          <div class="org">
            <div class="av" style="background:linear-gradient(140deg,#E4C39B,#A97D45)">I8</div>
            <div><div class="nm">@Integr8-ai</div><div class="rl">AI infrastructure &amp; business automation</div></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ================= CTA ================= -->
<section class="cta" id="contact">
  <div class="cta-bg">
    <img src="https://images.unsplash.com/photo-1487058792275-0ad4aaf24ca7?auto=format&fit=crop&w=1600&q=80" alt="Abstract code on screen" loading="lazy">
  </div>
  <div class="wrap cta-inner">
    <h2 class="kin" data-split>Let's build something that <span class="sweep">actually works.</span></h2>
    <p class="reveal" style="--d:.2s">Bring the operational mess. Bring the spreadsheet that runs the business. Bring the system everyone quietly hates. That's where the best work starts.</p>
    <div class="cta-actions reveal" style="--d:.3s">
      <a href="mailto:hello@agentcy.co.za" class="btn btn-primary magnetic">
        hello@agentcy.co.za
        <svg class="arr" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg>
      </a>
      <a href="#top" class="btn btn-sand magnetic">Back to top</a>
      <a href="#repos" class="btn btn-ghost magnetic">See the work</a>
    </div>
  </div>
</section>
</main>

<!-- ================= FOOTER ================= -->
<footer>
  <div class="wrap">
    <div class="foot-inner">
      <div class="foot-motto">
        <span>◈</span> <span>Built with intent ·</span> <b>mikewithoutthemechanics</b> <span>· KwaZulu-Natal, South Africa 🇿🇦</span> <span>◈</span>
      </div>
      <div class="foot-links">
        <a href="#capabilities">Capabilities</a>
        <a href="#ventures">Ventures</a>
        <a href="#credentials">Credentials</a>
        <a href="#activity">Activity</a>
        <a href="#contact">Contact</a>
      </div>
    </div>
    <div class="foot-bottom">
      <span>© <span id="year">2025</span> Michael Graeme Kidd · Agentcy · Integr8 AI · Agency-OS</span>
      <span class="mono">const status = "open_to_build"</span>
    </div>
  </div>
</footer>

<div class="tooltip" id="tooltip"></div>

<script>
(function () {
  'use strict';

  const reduceMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches;

  /* ---------- Year ---------- */
  const yearEl = document.getElementById('year');
  if (yearEl) yearEl.textContent = new Date().getFullYear();

  /* ---------- Scroll progress + nav state ---------- */
  const nav = document.getElementById('nav');
  const progressBar = document.getElementById('progressBar');
  let ticking = false;

  function onScroll() {
    const st = window.pageYOffset || document.documentElement.scrollTop;
    const docH = Math.max(document.body.scrollHeight - window.innerHeight, 1);
    const pct = Math.min(100, Math.max(0, (st / docH) * 100));
    if (progressBar) progressBar.style.width = pct + '%';
    if (nav) nav.classList.toggle('scrolled', st > 24);
    ticking = false;
  }
  window.addEventListener('scroll', function () {
    if (!ticking) { ticking = true; window.requestAnimationFrame(onScroll); }
  }, { passive: true });
  onScroll();

  /* ---------- Mobile menu ---------- */
  const burger = document.getElementById('burger');
  const mobileMenu = document.getElementById('mobileMenu');
  if (burger && mobileMenu) {
    burger.addEventListener('click', function () {
      const open = mobileMenu.classList.toggle('open');
      burger.classList.toggle('open', open);
      burger.setAttribute('aria-expanded', open ? 'true' : 'false');
      document.body.style.overflow = open ? 'hidden' : '';
    });
    mobileMenu.querySelectorAll('a').forEach(function (a) {
      a.addEventListener('click', function () {
        mobileMenu.classList.remove('open');
        burger.classList.remove('open');
        burger.setAttribute('aria-expanded', 'false');
        document.body.style.overflow = '';
      });
    });
  }

  /* ---------- Split text (kinetic headings) ---------- */
  document.querySelectorAll('[data-split]').forEach(function (el) {
    const nodes = Array.from(el.childNodes);
    el.innerHTML = '';
    let index = 0;
    nodes.forEach(function (node) {
      if (node.nodeType === 3) {
        const parts = node.textContent.split(/(\s+)/);
        parts.forEach(function (part) {
          if (!part.trim()) {
            el.appendChild(document.createTextNode(part));
            return;
          }
          const word = document.createElement('span');
          word.className = 'word';
          const inner = document.createElement('i');
          inner.textContent = part;
          inner.style.setProperty('--i', index++);
          word.appendChild(inner);
          el.appendChild(word);
        });
      } else if (node.nodeType === 1) {
        const parts = node.textContent.split(/(\s+)/);
        node.textContent = '';
        const wrapper = node;
        parts.forEach(function (part) {
          if (!part.trim()) {
            wrapper.appendChild(document.createTextNode(part));
            return;
          }
          const word = document.createElement('span');
          word.className = 'word';
          const inner = document.createElement('i');
          inner.textContent = part;
          inner.style.setProperty('--i', index++);
          word.appendChild(inner);
          wrapper.appendChild(word);
        });
        el.appendChild(wrapper);
      }
    });
    el.classList.add('kin');
    el.querySelectorAll('i').forEach(function (i) {
      i.style.display = 'inline-block';
      i.style.transform = reduceMotion ? 'none' : 'translateY(112%)';
      i.style.opacity = reduceMotion ? '1' : '0';
      i.style.transition = 'transform .95s cubic-bezier(.19,1,.22,1), opacity .9s ease';
      i.style.transitionDelay = (parseInt(i.style.getPropertyValue('--i'), 10) * 62 + 140) + 'ms';
    });
    // trigger
    const io = new IntersectionObserver(function (entries) {
      entries.forEach(function (e) {
        if (e.isIntersecting) {
          el.querySelectorAll('i').forEach(function (i) {
            i.style.transform = 'translateY(0)';
            i.style.opacity = '1';
          });
          io.unobserve(el);
        }
      });
    }, { threshold: 0.15 });
    io.observe(el);
  });

  /* ---------- Reveal on scroll ---------- */
  const revealEls = document.querySelectorAll('.reveal, .kicker');
  const revealIO = new IntersectionObserver(function (entries) {
    entries.forEach(function (e) {
      if (e.isIntersecting) {
        e.target.classList.add('in');
        revealIO.unobserve(e.target);
      }
    });
  }, { threshold: 0.12, rootMargin: '0px 0px -8% 0px' });
  revealEls.forEach(function (el) { revealIO.observe(el); });

  /* ---------- Focus list stagger ---------- */
  const focusItems = document.querySelectorAll('#focusList li');
  const focusIO = new IntersectionObserver(function (entries) {
    entries.forEach(function (e) {
      if (e.isIntersecting) {
        focusItems.forEach(function (li, i) {
          li.style.transitionDelay = (i * 110 + 260) + 'ms';
          li.classList.add('in');
        });
        focusIO.disconnect();
      }
    });
  }, { threshold: 0.2 });
  if (focusItems.length) focusIO.observe(focusItems[0].parentElement);

  /* ---------- Count up ---------- */
  function animateCount(el) {
    const target = parseFloat(el.getAttribute('data-count')) || 0;
    if (reduceMotion) { el.textContent = target.toLocaleString(); return; }
    const duration = 1650;
    const start = performance.now();
    function step(now) {
      const p = Math.min(1, (now - start) / duration);
      const eased = 1 - Math.pow(1 - p, 3);
      el.textContent = Math.round(target * eased).toLocaleString();
      if (p < 1) window.requestAnimationFrame(step);
      else el.textContent = target.toLocaleString();
    }
    window.requestAnimationFrame(step);
  }
  const countIO = new IntersectionObserver(function (entries) {
    entries.forEach(function (e) {
      if (e.isIntersecting) {
        animateCount(e.target);
        countIO.unobserve(e.target);
      }
    });
  }, { threshold: 0.5 });
  document.querySelectorAll('[data-count]').forEach(function (el) { countIO.observe(el); });

  /* ---------- Bars ---------- */
  const barIO = new IntersectionObserver(function (entries) {
    entries.forEach(function (e) {
      if (e.isIntersecting) {
        const bar = e.target;
        bar.style.width = bar.getAttribute('data-bar') + '%';
        barIO.unobserve(bar);
      }
    });
  }, { threshold: 0.35 });
  document.querySelectorAll('[data-bar]').forEach(function (el) { barIO.observe(el); });

  /* ---------- Hero cursor spotlight ---------- */
  const hero = document.getElementById('hero');
  const spot = document.getElementById('heroSpot');
  if (hero && spot && !reduceMotion && window.matchMedia('(pointer:fine)').matches) {
    hero.addEventListener('mousemove', function (e) {
      const r = hero.getBoundingClientRect();
      spot.style.left = (e.clientX - r.left) + 'px';
      spot.style.top = (e.clientY - r.top) + 'px';
    });
  }

  /* ---------- Magnetic buttons ---------- */
  if (!reduceMotion && window.matchMedia('(pointer:fine)').matches) {
    document.querySelectorAll('.magnetic').forEach(function (el) {
      el.addEventListener('mousemove', function (e) {
        const r = el.getBoundingClientRect();
        const x = e.clientX - r.left - r.width / 2;
        const y = e.clientY - r.top - r.height / 2;
        el.style.transform = 'translate(' + (x * 0.16) + 'px,' + (y * 0.22) + 'px)';
      });
      el.addEventListener('mouseleave', function () {
        el.style.transform = 'translate(0,0)';
      });
    });
  }

  /* ---------- Parallax ---------- */
  const parallaxEls = Array.from(document.querySelectorAll('[data-parallax]'));
  if (parallaxEls.length && !reduceMotion) {
    let rafId = null;
    function updateParallax() {
      const vh = window.innerHeight;
      parallaxEls.forEach(function (el) {
        const r = el.getBoundingClientRect();
        const center = r.top + r.height / 2;
        const offset = (center - vh / 2) * parseFloat(el.getAttribute('data-parallax'));
        el.style.setProperty('--py', offset.toFixed(2) + 'px');
        const base = el.classList.contains('visual-photo') ? 'rotate(2.6deg)' : (el.classList.contains('code-card') ? 'rotate(-1.1deg)' : '');
        el.style.transform = 'translate3d(0,' + offset.toFixed(2) + 'px,0) ' + base;
      });
      rafId = null;
    }
    window.addEventListener('scroll', function () {
      if (!rafId) rafId = window.requestAnimationFrame(updateParallax);
    }, { passive: true });
    window.addEventListener('resize', function () {
      if (!rafId) rafId = window.requestAnimationFrame(updateParallax);
    });
    updateParallax();
  }

  /* ---------- Tabs ---------- */
  const tabs = document.querySelectorAll('.tab');
  tabs.forEach(function (tab) {
    tab.addEventListener('click', function () {
      tabs.forEach(function (t) {
        t.classList.remove('active');
        t.setAttribute('aria-selected', 'false');
      });
      tab.classList.add('active');
      tab.setAttribute('aria-selected', 'true');
      document.querySelectorAll('.panel').forEach(function (p) { p.classList.remove('active'); });
      const target = document.getElementById('panel-' + tab.getAttribute('data-tab'));
      if (target) target.classList.add('active');
    });
  });

  /* ---------- Anthropic credential rows ---------- */
  const courses = [
    ['AI Fluency: Framework & Foundations', 'Jul 2026', 'Core'],
    ['Claude Code in Action', 'Jul 2026', 'Tooling'],
    ['Building with the Claude API', 'Jul 2026', 'Engineering'],
    ['AI Fluency for Builders', 'Jul 2026', 'Applied'],
    ['AI Fluency for Small Businesses', 'Jul 2026', 'Applied'],
    ['AI Capabilities and Limitations', 'Aug 2026', 'Core'],
    ['Introduction to agent skills', 'Aug 2026', 'Agents'],
    ['Introduction to subagents', 'Aug 2026', 'Agents'],
    ['Introduction to Model Context Protocol', 'Aug 2026', 'Protocol'],
    ['Model Context Protocol: Advanced Topics', 'Aug 2026', 'Protocol']
  ];
  const rowsHost = document.getElementById('anthropicRows');
  if (rowsHost) {
    courses.forEach(function (c, i) {
      const tr = document.createElement('tr');
      tr.innerHTML =
        '<td data-label="Course"><span class="name"><span class="badge">A</span>' + c[0] + '</span></td>' +
        '<td data-label="Completed"><span class="date-pill">' + c[1] + '</span></td>' +
        '<td data-label="Track"><span class="date-pill ember">' + c[2] + '</span></td>';
      rowsHost.appendChild(tr);
    });
  }

  /* ---------- Contribution heatmap ---------- */
  const grid = document.getElementById('cellsGrid');
  const monthsRow = document.getElementById('monthsRow');
  const tooltip = document.getElementById('tooltip');

  if (grid && monthsRow) {
    const weeks = 53;
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    // start on the Sunday of the week ~52 weeks ago
    const start = new Date(today);
    start.setDate(start.getDate() - (weeks * 7 - 1) - today.getDay());

    // deterministic pseudo-random for a stable, natural-looking graph
    let seed = 20260719;
    function rnd() {
      seed = (seed * 1664525 + 1013904223) % 4294967296;
      return seed / 4294967296;
    }

    const cellsData = [];
    let sum = 0;
    for (let w = 0; w < weeks; w++) {
      for (let d = 0; d < 7; d++) {
        const date = new Date(start);
        date.setDate(start.getDate() + w * 7 + d);
        if (date > today) { cellsData.push(null); continue; }
        const weekend = (d === 0 || d === 6);
        const base = weekend ? 2.6 : 8.4;
        let v = Math.round(Math.pow(rnd(), 1.75) * base * 2.05);
        if (rnd() > 0.93) v += Math.round(rnd() * 9);
        if (date.getMonth() === today.getMonth() && date.getFullYear() === today.getFullYear()) v += 1;
        cellsData.push({ count: v, date: date });
        sum += v;
      }
    }

    // normalise so the visible total matches 1,046 contributions
    const factor = sum > 0 ? 1046 / sum : 1;
    let running = 0;
    cellsData.forEach(function (c) {
      if (!c) return;
      c.count = Math.max(0, Math.round(c.count * factor));
      running += c.count;
    });
    // adjust the final cell so the total is exact
    if (cellsData.length && running !== 1046) {
      for (let i = cellsData.length - 1; i >= 0; i--) {
        if (cellsData[i]) {
          const diff = 1046 - running;
          cellsData[i].count = Math.max(0, cellsData[i].count + diff);
          break;
        }
      }
    }

    function level(v) {
      if (v <= 0) return 0;
      if (v <= 3) return 1;
      if (v <= 7) return 2;
      if (v <= 12) return 3;
      return 4;
    }

    const frag = document.createDocumentFragment();
    const monthLabels = [];
    let lastMonth = -1;

    cellsData.forEach(function (c, i) {
      const cell = document.createElement('div');
      cell.className = 'cell';
      if (c) {
        const lvl = level(c.count);
        if (lvl) cell.classList.add('l' + lvl);
        const label = c.count + (c.count === 1 ? ' contribution' : ' contributions') + ' on ' +
          c.date.toLocaleDateString('en-US', { month: 'long', day: 'numeric', year: 'numeric' });
        cell.setAttribute('data-label', label);
        cell.setAttribute('tabindex', '-1');
      } else {
        cell.setAttribute('data-label', 'No data');
      }
      frag.appendChild(cell);
    });
    grid.appendChild(frag);

    // month labels aligned with week columns
    for (let w = 0; w < weeks; w++) {
      const d = new Date(start);
      d.setDate(start.getDate() + w * 7);
      const m = d.getMonth();
      monthLabels.push(m !== lastMonth ? d.toLocaleDateString('en-US', { month: 'short' }) : '');
      lastMonth = m;
    }
    monthLabels.forEach(function (txt) {
      const s = document.createElement('span');
      s.textContent = txt;
      monthsRow.appendChild(s);
    });

    // staggered reveal
    const allCells = Array.from(grid.querySelectorAll('.cell'));
    const graphIO = new IntersectionObserver(function (entries) {
      entries.forEach(function (e) {
        if (!e.isIntersecting) return;
        if (reduceMotion) {
          allCells.forEach(function (c) { c.classList.add('shown'); });
        } else {
          allCells.forEach(function (c, i) {
            const col = Math.floor(i / 7);
            setTimeout(function () { c.classList.add('shown'); }, col * 13);
          });
        }
        graphIO.disconnect();
      });
    }, { threshold: 0.08 });
    graphIO.observe(grid);

    // tooltip
    if (tooltip) {
      grid.addEventListener('mousemove', function (e) {
        const cell = e.target.closest('.cell');
        if (!cell) return;
        tooltip.innerHTML = cell.getAttribute('data-label');
        tooltip.classList.add('show');
        const pad = 14;
        let x = e.clientX + pad;
        let y = e.clientY - 42;
        const tw = tooltip.offsetWidth;
        if (x + tw > window.innerWidth - 10) x = e.clientX - tw - pad;
        if (y < 8) y = e.clientY + 22;
        tooltip.style.left = x + 'px';
        tooltip.style.top = y + 'px';
      });
      grid.addEventListener('mouseleave', function () {
        tooltip.classList.remove('show');
      });
    }
  }

  /* ---------- Smooth anchor offset for fixed nav ---------- */
  document.querySelectorAll('a[href^="#"]').forEach(function (link) {
    link.addEventListener('click', function (e) {
      const id = link.getAttribute('href');
      if (!id || id === '#' || id.length < 2) return;
      const target = document.querySelector(id);
      if (!target) return;
      e.preventDefault();
      const top = target.getBoundingClientRect().top + window.pageYOffset - (nav ? nav.offsetHeight + 12 : 20);
      window.scrollTo({ top: top, behavior: reduceMotion ? 'auto' : 'smooth' });
    });
  });

  /* ---------- Cap card tap-to-reveal on touch ---------- */
  if (window.matchMedia('(hover:none)').matches) {
    document.querySelectorAll('.cap').forEach(function (card) {
      card.addEventListener('click', function () {
        card.classList.toggle('touched');
        const means = card.querySelector('.means');
        if (means) {
          const open = card.classList.contains('touched');
          means.style.maxHeight = open ? '160px' : '0';
          means.style.opacity = open ? '1' : '0';
          means.style.transform = open ? 'none' : 'translateY(8px)';
        }
      });
    });
  }

  /* ---------- Hero entry timing ---------- */
  window.requestAnimationFrame(function () {
    document.querySelectorAll('.hero .reveal').forEach(function (el) { el.classList.add('in'); });
  });

})();
</script>
</body>
</html>
