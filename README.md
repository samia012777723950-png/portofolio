<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Samia Ahmed — Business Development · SYNC Application</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,500;0,9..144,600;0,9..144,700;1,9..144,500&family=Archivo:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#10141f;
    --panel:#161c2c;
    --cream:#f2ece0;
    --muted:#9aa2ba;
    --gold:#c9a46a;
    --cold:#4f7396;
    --sage:#7c8b7e;
    --amber:#d98a4f;
    --hot:#e8543f;
    --line:rgba(242,236,224,0.12);
  }

  *{margin:0;padding:0;box-sizing:border-box;}
  html{scroll-behavior:smooth;}

  body{
    background:var(--ink);
    color:var(--cream);
    font-family:'Archivo',sans-serif;
    line-height:1.6;
    overflow-x:hidden;
    position:relative;
  }

  body::before{
    content:"";
    position:fixed;
    inset:0;
    pointer-events:none;
    opacity:0.035;
    z-index:1;
    background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='2' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
  }

  .wrap{max-width:760px;margin:0 auto;padding:0 1.5rem;position:relative;z-index:2;}

  .hero{min-height:92vh;display:flex;flex-direction:column;justify-content:center;position:relative;}
  .hero::before{
    content:"";position:absolute;top:8%;left:50%;width:520px;height:520px;
    background:radial-gradient(circle, rgba(201,164,106,0.16), transparent 70%);
    transform:translateX(-50%);z-index:-1;
  }

  .eyebrow{
    font-family:'IBM Plex Mono',monospace;font-size:0.72rem;letter-spacing:0.14em;
    text-transform:uppercase;color:var(--gold);display:inline-flex;align-items:center;gap:0.5rem;
    margin-bottom:1.75rem;opacity:0;animation:rise 0.8s ease forwards;
  }
  .eyebrow::before{content:"";width:6px;height:6px;background:var(--hot);border-radius:50%;box-shadow:0 0 8px var(--hot);}

  h1{
    font-family:'Fraunces',serif;font-weight:600;font-size:clamp(2.3rem,6.5vw,4.3rem);
    line-height:1.05;letter-spacing:-0.01em;max-width:14ch;opacity:0;
    animation:rise 0.9s ease 0.15s forwards;
  }
  h1 em{font-style:italic;font-weight:500;color:var(--amber);}

  .subhead{
    font-size:1.08rem;color:var(--muted);max-width:46ch;margin-top:1.75rem;opacity:0;
    animation:rise 0.9s ease 0.3s forwards;
  }
  .subhead strong{color:var(--cream);font-weight:600;}

  @keyframes rise{from{opacity:0;transform:translateY(16px);}to{opacity:1;transform:translateY(0);}}

  section{padding:6rem 0;position:relative;}
  section h2{font-family:'Fraunces',serif;font-weight:600;font-size:clamp(1.7rem,3.5vw,2.3rem);margin-bottom:0.6rem;}
  .section-kicker{
    font-family:'IBM Plex Mono',monospace;font-size:0.7rem;letter-spacing:0.14em;
    text-transform:uppercase;color:var(--gold);margin-bottom:0.75rem;display:block;
  }
  .section-lead{color:var(--muted);max-width:52ch;margin-bottom:3rem;font-size:1rem;}

  .pipeline-track{position:relative;padding-left:2.75rem;}
  .pipeline-line{
    position:absolute;left:0.4rem;top:0.5rem;bottom:0.5rem;width:2px;
    background:linear-gradient(to bottom, var(--cold), var(--sage), var(--gold), var(--amber), var(--hot));
  }
  .stage{
    position:relative;padding-bottom:3rem;opacity:0;transform:translateY(20px);
    transition:opacity 0.7s ease, transform 0.7s ease;
  }
  .stage.in-view{opacity:1;transform:translateY(0);}
  .stage:last-child{padding-bottom:0;}
  .stage-node{
    position:absolute;left:-2.35rem;top:0.3rem;width:11px;height:11px;border-radius:50%;
    background:var(--ink);border:2px solid var(--stage-color);
  }
  .stage:last-child .stage-node{background:var(--hot);box-shadow:0 0 12px var(--hot);}
  .stage-label{font-family:'IBM Plex Mono',monospace;font-size:0.68rem;letter-spacing:0.1em;color:var(--stage-color);display:block;margin-bottom:0.4rem;}
  .stage h3{font-family:'Fraunces',serif;font-weight:600;font-size:1.35rem;margin-bottom:0.5rem;}
  .stage p{color:var(--muted);max-width:50ch;font-size:0.97rem;}

  .foundation-body{max-width:56ch;}
  .foundation-body p{margin-bottom:1.4rem;font-size:1.02rem;}
  .foundation-body p:first-of-type{color:var(--cream);}

  .fill-in{
    display:inline-block;padding:0.05em 0.5em;border:1.5px dashed var(--hot);border-radius:4px;
    color:var(--amber);font-style:italic;background:rgba(232,84,63,0.08);white-space:nowrap;
  }
  .edit-flag{
    font-family:'IBM Plex Mono',monospace;font-size:0.72rem;color:var(--hot);letter-spacing:0.06em;
    display:inline-flex;align-items:center;gap:0.4rem;margin-top:0.5rem;padding:0.6rem 0.9rem;
    border:1px dashed rgba(232,84,63,0.4);border-radius:6px;background:rgba(232,84,63,0.06);
  }

  .why-body{max-width:56ch;font-size:1.05rem;}
  .why-body strong{color:var(--gold);font-weight:600;}

  footer{padding:5rem 0 4rem;border-top:1px solid var(--line);}
  .footer-top{display:flex;justify-content:space-between;align-items:flex-end;flex-wrap:wrap;gap:2rem;margin-bottom:2.5rem;}
  footer h2{font-size:clamp(1.6rem,4vw,2.1rem);}
  .contact-links{display:flex;flex-direction:column;gap:0.5rem;align-items:flex-start;}
  .contact-links a{
    color:var(--cream);text-decoration:none;font-size:1rem;border-bottom:1px solid var(--line);
    padding-bottom:2px;transition:border-color 0.2s ease, color 0.2s ease;
  }
  .contact-links a:hover,.contact-links a:focus-visible{color:var(--amber);border-color:var(--amber);}
  .built-for{font-family:'IBM Plex Mono',monospace;font-size:0.75rem;color:var(--muted);letter-spacing:0.04em;}

  a:focus-visible,button:focus-visible{outline:2px solid var(--amber);outline-offset:3px;}

  @media (min-width:768px){
    .wrap{padding:0 2.5rem;}
    section{padding:8rem 0;}
  }

  @media (prefers-reduced-motion: reduce){
    *{animation-duration:0.01ms !important;animation-iteration-count:1 !important;transition-duration:0.01ms !important;}
    html{scroll-behavior:auto;}
  }
</style>
</head>
<body>

<div class="wrap">

  <header class="hero">
    <span class="eyebrow">Business Development — SYNC Workshop</span>
    <h1>I started in sales.<br>I never actually <em>left</em>.</h1>
    <p class="subhead">Two years leading a sales team. Three years turning that instinct into shipped products and <strong>trade-offs I had to defend to leadership</strong>. Now I want to make the sales side official.</p>
  </header>

  <section class="pipeline" id="pipeline">
    <span class="section-kicker">Not a metaphor</span>
    <h2>My own pipeline</h2>
    <p class="section-lead">I've built lead-scoring logic for a living. Here's where five real decisions from my career would actually sit on it.</p>

    <div class="pipeline-track">
      <div class="pipeline-line"></div>

      <div class="stage" style="--stage-color:#4F7396;">
        <div class="stage-node"></div>
        <span class="stage-label">01 · COLD LEAD</span>
        <h3>Sales Team Leader</h3>
        <p>Two years leading a sales team, before product ever entered the picture. This is where the instinct started.</p>
      </div>

      <div class="stage" style="--stage-color:#7C8B7E;">
        <div class="stage-node"></div>
        <span class="stage-label">02 · QUALIFYING</span>
        <h3>Built the scoring logic myself</h3>
        <p>At Octaboo, I designed the lead-scoring behind a WhatsApp AI agent — deciding, systematically, exactly when a lead is warm enough to hand to a human.</p>
      </div>

      <div class="stage" style="--stage-color:#C9A46A;">
        <div class="stage-node"></div>
        <span class="stage-label">03 · THE PITCH</span>
        <h3>Sold a constraint as the feature</h3>
        <p>At Altech, 15+ homeowner interviews in, I repositioned "offline-only" from a technical limitation into a key trust factor for Saudi buyers.</p>
      </div>

      <div class="stage" style="--stage-color:#D98A4F;">
        <div class="stage-node"></div>
        <span class="stage-label">04 · THE OBJECTION</span>
        <h3>Told leadership to walk from 30% of ARR</h3>
        <p>At Metas, I built the model and held the line on a pivot leadership initially resisted. It paid off in engagement and retention within two sprints.</p>
      </div>

      <div class="stage" style="--stage-color:#E8543F;">
        <div class="stage-node"></div>
        <span class="stage-label">05 · CLOSED WON</span>
        <h3>Enterprise clients who stayed — and said why</h3>
        <p>At FAAINEX, two enterprise accounts specifically named "zero compliance errors" as their reason to renew. That's a retained account, not just a shipped release.</p>
      </div>
    </div>
  </section>

  <section class="foundation" id="foundation">
    <span class="section-kicker">Where it started</span>
    <h2>Before product, there was the sales floor</h2>
    <div class="foundation-body">
      <p>I spent two years as a Sales Team Leader before product ever entered the picture — handling objections, managing a pipeline, and learning that a deal doesn't close on features. It closes on trust, timing, and knowing exactly what someone's afraid to say yes to.</p>
      <p>That instinct never left. In my current Product Owner role, client conversations are still part of my week — reading a room, reframing an objection, knowing when to hold a price and when to hold the relationship instead.</p>
    </div>
  </section>

  <section class="why" id="why">
    <span class="section-kicker">The gap I'm closing</span>
    <h2>Why SYNC</h2>
    <div class="why-body">
      <p>Product taught me how to build the right thing. I want SYNC to teach me how to <strong>close the room on it</strong> — how to price a proposal properly, build a sponsorship case from scratch, and handle a "no" with a system instead of just instinct.</p>
    </div>
  </section>

  <footer>
    <div class="footer-top">
      <h2>Let's talk BD.</h2>
      <div class="contact-links">
        <a href="mailto:samhassan045@gmail.com">samhassan045@gmail.com</a>
        <a href="https://linkedin.com/in/samia-ahmed" target="_blank" rel="noopener">linkedin.com/in/samia-ahmed</a>
      </div>
    </div>
    <span class="built-for">Built specifically for SYNC's Business Development Workshop · September 2026</span>
  </footer>

</div>

<script>
  const stages = document.querySelectorAll('.stage');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('in-view');
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.2 });
  stages.forEach(s => observer.observe(s));
</script>

</body>
</html>
