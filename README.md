# artharjan.github.io
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Artharjan | Financial Awareness</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Fraunces:ital,wght@0,500;0,600;0,700;1,500&family=Poppins:wght@400;500;600&family=Yatra+One&display=swap');

:root{
  --cream: #FBF6EE;
  --navy: #1B2E4A;
  --terracotta: #C1552F;
  --sage: #5C7A6B;
  --peach: #E8A184;
  --sage-tint: #E0E8E3;
  --peach-tint: #FAE7DB;
  --rule: rgba(27,46,74,0.14);
}

*{box-sizing:border-box;}
html{scroll-behavior:smooth;}
body{
  margin:0;
  background:var(--cream);
  color:var(--navy);
  font-family:'Poppins', sans-serif;
  line-height:1.65;
}
@media (prefers-reduced-motion: reduce){ *{animation:none !important; transition:none !important;} }
a{color:inherit;}
.wrap{max-width:1080px; margin:0 auto; padding:0 28px;}

/* Mark */
.mark{
  width:48px; height:48px; border-radius:50%;
  background:var(--terracotta);
  display:flex; align-items:center; justify-content:center;
  font-family:'Yatra One', serif; color:var(--cream); font-size:1.35rem;
  flex-shrink:0;
}
.mark.on-navy{ background:var(--terracotta); }

/* Header */
header{
  position:sticky; top:0; z-index:50; background:var(--cream);
  border-bottom:1px solid var(--rule);
}
.header-inner{
  display:flex; align-items:center; justify-content:space-between;
  padding:16px 28px; max-width:1080px; margin:0 auto;
}
.brand{ display:flex; align-items:center; gap:12px; font-family:'Fraunces', serif; font-weight:600; font-size:1.3rem; }
nav{display:flex; gap:28px; font-size:0.92rem;}
nav a{ text-decoration:none; color:var(--navy); padding-bottom:3px; border-bottom:1px solid transparent; }
nav a:hover, nav a:focus-visible{ border-color:var(--terracotta); outline:none; }
.nav-toggle{display:none; background:none; border:none; font-size:1.5rem; cursor:pointer; color:var(--navy);}
@media(max-width:720px){
  nav{display:none;}
  .nav-toggle{display:block;}
  nav.open{
    display:flex; flex-direction:column; position:absolute; top:100%; left:0; right:0;
    background:var(--cream); padding:16px 28px; border-bottom:1px solid var(--rule); gap:14px;
  }
}

/* Hero */
.hero{ padding:72px 0 56px; position:relative; overflow:hidden; }
.hero-label{
  font-family:'Poppins', sans-serif; font-weight:500; font-size:0.8rem; color:var(--terracotta);
  text-transform:uppercase; letter-spacing:0.12em; margin-bottom:16px;
}
.hero h1{
  font-family:'Fraunces', serif; font-weight:600; font-size:clamp(2.2rem, 5.5vw, 3.6rem);
  line-height:1.15; margin:0 0 20px; max-width:760px;
}
.hero h1 em{ font-style:normal; color:var(--terracotta); }
.hero p.lede{ font-size:1.15rem; max-width:600px; color:var(--navy); opacity:0.85; margin:0 0 32px; }
.cta-row{display:flex; gap:16px; flex-wrap:wrap;}
.btn{
  font-family:'Poppins', sans-serif; font-weight:600; font-size:0.95rem;
  padding:14px 28px; border-radius:8px; text-decoration:none; display:inline-block;
  border:1.5px solid var(--terracotta); transition:all 0.15s ease;
}
.btn-solid{ background:var(--terracotta); color:var(--cream); }
.btn-solid:hover{ background:#a8461f; border-color:#a8461f; }
.btn-outline{ background:transparent; color:var(--terracotta); }
.btn-outline:hover{ background:rgba(193,85,47,0.08); }
.bleed-circle{
  position:absolute; border-radius:50%; z-index:-1;
}

/* Sections */
.section{ padding:64px 0; }
.section-label{
  font-family:'Poppins', sans-serif; font-weight:500; font-size:0.85rem; color:var(--sage);
  text-transform:uppercase; letter-spacing:0.1em; margin-bottom:10px;
}
.section h2{ font-family:'Fraunces', serif; font-weight:600; font-size:2rem; margin:0 0 36px; }

/* Verticals */
.verticals{ display:grid; grid-template-columns:1fr 1fr; gap:28px; }
@media(max-width:760px){ .verticals{grid-template-columns:1fr;} }
.vcard{ padding:32px 28px; border-radius:16px; }
.vcard.one{ background:var(--peach-tint); }
.vcard.two{ background:var(--sage-tint); }
.vcard h3{ font-family:'Fraunces', serif; font-size:1.5rem; margin:0 0 12px; }
.vcard p{ font-size:0.98rem; opacity:0.85; margin:0 0 18px; }
.chip-list{ display:flex; flex-direction:column; gap:10px; margin-bottom:20px; }
.chip{
  padding:12px 18px; border-radius:8px; font-weight:600; font-size:0.95rem; color:var(--cream);
}
.vcard.one .chip:nth-child(1){ background:var(--terracotta); }
.vcard.one .chip:nth-child(2){ background:var(--sage); }
.vcard.one .chip:nth-child(3){ background:var(--navy); }
.vcard.two .dot-list{ list-style:none; padding:0; margin:0 0 20px; }
.vcard.two .dot-list li{ padding-left:22px; position:relative; margin-bottom:10px; font-weight:500; }
.vcard.two .dot-list li::before{
  content:""; position:absolute; left:0; top:8px; width:9px; height:9px; border-radius:50%; background:var(--terracotta);
}
.vcard-cta{
  font-family:'Poppins', sans-serif; font-weight:600; font-size:0.9rem; color:var(--navy);
  text-decoration:none; border-bottom:2px solid var(--terracotta);
}

/* About */
.about-grid{ display:grid; grid-template-columns:1.3fr 1fr; gap:44px; align-items:start; }
@media(max-width:760px){ .about-grid{grid-template-columns:1fr;} }
.about-text p{ font-size:1rem; opacity:0.85; margin:0 0 16px; }
.stat-box{ background:var(--navy); border-radius:16px; padding:28px; color:var(--cream); }
.stat-row{ display:flex; justify-content:space-between; padding:10px 0; border-bottom:1px dotted rgba(251,246,238,0.25); font-size:0.92rem; }
.stat-row:last-child{ border-bottom:none; }
.stat-row b{ font-weight:600; }

/* Contact */
.contact-card{
  background:var(--peach-tint); border-radius:20px; padding:40px; max-width:640px; position:relative;
}
.field{ margin-bottom:22px; }
.field label{
  display:block; font-family:'Poppins', sans-serif; font-weight:500; font-size:0.78rem;
  text-transform:uppercase; letter-spacing:0.06em; color:var(--navy); opacity:0.7; margin-bottom:6px;
}
.field input, .field textarea{
  width:100%; background:var(--cream); border:1.5px solid transparent; border-radius:8px;
  font-family:'Poppins', sans-serif; font-size:1rem; padding:12px 14px; color:var(--navy);
}
.field input:focus, .field textarea:focus{ outline:none; border-color:var(--terracotta); }
.field textarea{ resize:vertical; min-height:100px; }
.form-status{ margin-top:14px; font-size:0.9rem; font-weight:600; color:var(--navy); }

footer{
  border-top:1px solid var(--rule); padding:32px 0; margin-top:20px;
  font-family:'Poppins', sans-serif; font-size:0.85rem; color:var(--navy); opacity:0.7;
  display:flex; justify-content:space-between; flex-wrap:wrap; gap:10px;
}
</style>
</head>
<body>

<header>
  <div class="header-inner">
    <div class="brand"><span class="mark">अ</span> Artharjan</div>
    <button class="nav-toggle" id="navToggle" aria-label="Toggle menu" aria-expanded="false">☰</button>
    <nav id="mainNav">
      <a href="#verticals">What we do</a>
      <a href="#about">About</a>
      <a href="#contact">Get in touch</a>
    </nav>
  </div>
</header>

<main>
  <section class="hero wrap">
    <div class="bleed-circle" style="width:280px; height:280px; background:var(--peach-tint); top:-100px; right:-100px;"></div>
    <div class="hero-label">Financial Awareness · A New Chapter</div>
    <h1>Helping Indians make sense of <em>money</em> — one honest conversation at a time.</h1>
    <p class="lede">Artharjan started with one goal: help every Indian understand money, plainly and honestly. What began offline is now becoming a structured practice in personal coaching and institutional financial awareness.</p>
    <div class="cta-row">
      <a href="#contact" class="btn btn-solid">Get in touch</a>
      <a href="#verticals" class="btn btn-outline">See what we do</a>
    </div>
  </section>

  <section class="section wrap" id="verticals">
    <div class="section-label">What we do</div>
    <h2>Two ways we work</h2>
    <div class="verticals">
      <div class="vcard one">
        <h3>1-on-1 Coaching</h3>
        <p>Learn exactly what you want to learn. Every path is built around your goals, not a fixed syllabus.</p>
        <div class="chip-list">
          <div class="chip">Options trading</div>
          <div class="chip">Intraday</div>
          <div class="chip">Long-term investing</div>
        </div>
        <a href="#contact" class="vcard-cta">Enquire about coaching →</a>
      </div>
      <div class="vcard two">
        <h3>Financial Awareness Sessions</h3>
        <p>Structured sessions for schools, colleges, and organisations — built to grow financial literacy across communities.</p>
        <ul class="dot-list">
          <li>Schools</li>
          <li>Colleges</li>
          <li>Teams &amp; institutions</li>
        </ul>
        <a href="#contact" class="vcard-cta">Book a session →</a>
      </div>
    </div>
  </section>

  <section class="section wrap" id="about">
    <div class="section-label">Our story</div>
    <h2>Where it all started</h2>
    <div class="about-grid">
      <div class="about-text">
        <p>For years, Artharjan was offline conversations — one person, one honest answer at a time. No jargon, no sales pitches, just real answers to real money questions.</p>
        <p>Now that same honesty is moving online, reaching more people while keeping the same approach that built trust in the first place.</p>
        <p><em>[Add your personal story here — how Artharjan started, and what keeps you doing it.]</em></p>
      </div>
      <div class="stat-box">
        <div class="stat-row"><span>Years active</span><b>[ADD NUMBER]</b></div>
        <div class="stat-row"><span>Sessions conducted</span><b>[ADD NUMBER]</b></div>
        <div class="stat-row"><span>Institutions reached</span><b>[ADD NUMBER]</b></div>
        <div class="stat-row"><span>Coaching clients</span><b>[ADD NUMBER]</b></div>
      </div>
    </div>
  </section>

  <section class="section wrap" id="contact">
    <div class="section-label">Get in touch</div>
    <h2>Let's talk money — the useful kind</h2>
    <form class="contact-card" id="contactForm">
      <div class="field">
        <label for="name">Name</label>
        <input type="text" id="name" name="name" required>
      </div>
      <div class="field">
        <label for="email">Email</label>
        <input type="email" id="email" name="email" required>
      </div>
      <div class="field">
        <label for="interest">I'm interested in</label>
        <input type="text" id="interest" name="interest" placeholder="1-on-1 coaching / literacy session / other">
      </div>
      <div class="field">
        <label for="message">Message</label>
        <textarea id="message" name="message" required></textarea>
      </div>
      <button type="submit" class="btn btn-solid">Send message</button>
      <div class="form-status" id="formStatus"></div>
    </form>
  </section>
</main>

<footer class="wrap">
  <span>Artharjan · Financial Awareness</span>
  <span>artharjan2000@gmail.com</span>
</footer>

<script>
  const toggle = document.getElementById('navToggle');
  const nav = document.getElementById('mainNav');
  toggle.addEventListener('click', () => {
    const isOpen = nav.classList.toggle('open');
    toggle.setAttribute('aria-expanded', isOpen);
  });

  const CONTACT_EMAIL = "artharjan2000@gmail.com";

  document.getElementById('contactForm').addEventListener('submit', function(e){
    e.preventDefault();
    const name = document.getElementById('name').value;
    const email = document.getElementById('email').value;
    const interest = document.getElementById('interest').value;
    const message = document.getElementById('message').value;

    const subject = encodeURIComponent("Artharjan enquiry from " + name);
    const body = encodeURIComponent(
      "Name: " + name + "\n" +
      "Email: " + email + "\n" +
      "Interested in: " + interest + "\n\n" +
      "Message:\n" + message
    );

    window.location.href = "mailto:" + CONTACT_EMAIL + "?subject=" + subject + "&body=" + body;
    document.getElementById('formStatus').textContent = "Opening your email app now…";
  });
</script>

</body>
</html>
