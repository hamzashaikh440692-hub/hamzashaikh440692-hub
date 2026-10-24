<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Hamza Shaikh – Frontend Developer</title>
<meta name="description" content="Portfolio of Hamza Shaikh, a web development student learning frontend and full-stack development.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Instrument+Serif:ital@0;1&family=DM+Sans:wght@400;500;700&display=swap" rel="stylesheet">
<style>
:root{
  --night:#15121f; --night2:#1d1930; --text:#f3eefb; --muted:#b4abc9;
  --lilac:#b9a4ff; --peach:#ffb8a1; --mint:#9be8d0;
  --glass:rgba(255,255,255,.06); --edge:rgba(255,255,255,.14);
  --serif:"Instrument Serif",Georgia,"Times New Roman",serif;
  --sans:"DM Sans",system-ui,-apple-system,"Segoe UI",sans-serif;
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{font-family:var(--sans);color:var(--text);background:var(--night);line-height:1.7;font-size:17px;overflow-x:hidden}
a{color:inherit}
:focus-visible{outline:2px solid var(--mint);outline-offset:4px;border-radius:6px}
.wrap{max-width:980px;margin:0 auto;padding:0 26px;position:relative;z-index:1}

/* dreamy aurora background */
.aurora{position:fixed;inset:0;z-index:0;pointer-events:none;overflow:hidden}
.orb{position:absolute;border-radius:50%;filter:blur(90px);opacity:.5;animation:drift 22s ease-in-out infinite alternate}
.o1{width:480px;height:480px;background:var(--lilac);top:-120px;left:-100px}
.o2{width:420px;height:420px;background:var(--peach);top:30%;right:-140px;animation-delay:-8s;opacity:.35}
.o3{width:460px;height:460px;background:var(--mint);bottom:-180px;left:25%;animation-delay:-14s;opacity:.28}
@keyframes drift{to{transform:translate(70px,50px) scale(1.15)}}

/* nav */
header{position:fixed;top:16px;left:0;right:0;z-index:10;display:flex;justify-content:center;padding:0 16px}
nav{display:flex;gap:6px;padding:6px;border-radius:999px;background:rgba(21,18,31,.6);backdrop-filter:blur(14px);border:1px solid var(--edge)}
nav a{padding:8px 18px;border-radius:999px;text-decoration:none;color:var(--muted);font-size:.95rem;font-weight:500;transition:background .2s,color .2s}
nav a:hover{background:var(--glass);color:var(--text)}

/* hero */
.hero{min-height:100vh;display:flex;align-items:center;text-align:center}
.hero .wrap{padding-top:120px;padding-bottom:80px}
.hello{color:var(--muted);font-size:1.05rem;margin-bottom:18px}
h1{font-family:var(--serif);font-weight:400;font-size:clamp(3.4rem,13vw,8.5rem);line-height:.95;letter-spacing:-.02em}
h1 em{color:var(--lilac)}
.role{margin:26px auto 0;max-width:30em;font-size:1.2rem;color:var(--muted)}
.cta{display:flex;gap:14px;justify-content:center;margin-top:36px;flex-wrap:wrap}
.btn{padding:13px 28px;border-radius:999px;text-decoration:none;font-weight:700;border:1px solid var(--edge);transition:transform .2s,background .2s}
.btn.main{background:linear-gradient(120deg,var(--lilac),var(--peach));color:#1b1530;border-color:transparent}
.btn.soft{background:var(--glass);backdrop-filter:blur(8px)}
.btn:hover{transform:translateY(-3px)}

/* sections */
section{padding:90px 0}
h2{font-family:var(--serif);font-weight:400;font-size:clamp(2.2rem,5vw,3.4rem);line-height:1.1;margin-bottom:14px}
.sub{color:var(--muted);max-width:34em;margin-bottom:38px}
.glass{background:var(--glass);border:1px solid var(--edge);border-radius:24px;backdrop-filter:blur(14px)}

.about{padding:42px;display:grid;grid-template-columns:1.5fr 1fr;gap:44px}
.about p+p{margin-top:16px}
.about p{color:var(--muted)}
.facts{list-style:none;display:grid;gap:18px}
.facts li{padding-left:16px;border-left:2px solid var(--lilac)}
.facts b{display:block;font-family:var(--serif);font-weight:400;font-size:1.4rem;color:var(--text)}
.facts span{color:var(--muted);font-size:.95rem}

.chips{display:flex;flex-wrap:wrap;gap:12px}
.chip{padding:10px 22px;border-radius:999px;background:var(--glass);border:1px solid var(--edge);font-weight:500}
.chip.soon{border-style:dashed;color:var(--muted)}

.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(280px,1fr));gap:20px}
.card{padding:28px;text-decoration:none;display:flex;flex-direction:column;gap:8px;transition:transform .25s,border-color .25s,background .25s}
.card:hover{transform:translateY(-6px);border-color:var(--lilac);background:rgba(255,255,255,.1)}
.card h3{font-family:var(--serif);font-weight:400;font-size:1.7rem}
.card p{color:var(--muted);flex:1;font-size:.98rem}
.card small{color:var(--mint);font-weight:700}

.contact{text-align:center;padding:60px 40px}
.contact .cta{margin-top:26px}
footer{position:relative;z-index:1;text-align:center;padding:36px 20px 50px;color:var(--muted);font-size:.92rem}

.card .links{display:flex;gap:18px;margin-top:6px}
.card .links a{color:var(--mint);font-weight:700;text-decoration:none}
.card .links a:hover{text-decoration:underline}
.card .lang{color:var(--muted);font-size:.85rem}
@media(max-width:760px){
  .about{grid-template-columns:1fr;padding:28px}
  nav a{padding:8px 12px;font-size:.88rem}
  section{padding:64px 0}
}
@media(prefers-reduced-motion:reduce){
  html{scroll-behavior:auto}.orb{animation:none}.btn,.card{transition:none}
}
</style>
</head>
<body>

<div class="aurora" aria-hidden="true">
  <div class="orb o1"></div><div class="orb o2"></div><div class="orb o3"></div>
</div>

<header>
  <nav aria-label="Main">
    <a href="#top">Home</a>
    <a href="#about">About</a>
    <a href="#skills">Skills</a>
    <a href="#projects">Projects</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<main id="top">
  <section class="hero">
    <div class="wrap">
      <p class="hello">Hello, I’m</p>
      <h1>Hamza <em>Shaikh</em></h1>
      <p class="role">A web development student building clean, responsive websites, and growing into a full-stack developer.</p>
      <div class="cta">
        <a class="btn main" href="#projects">View my work</a>
        <a class="btn soft" href="https://github.com/hamzashaikh440692-hub" target="_blank" rel="noopener">GitHub</a>
      </div>
    </div>
  </section>

  <section id="about">
    <div class="wrap">
      <div class="glass about">
        <div>
          <h2>About me</h2>
          <p>I’m a student who loves building things with code. I enjoy creating clean, responsive websites, and I keep improving by building projects and finishing assignments.</p>
          <p>Right now I’m learning HTML, CSS, Git and GitHub, and exploring something new every day. I’m open to learning, collaborating and taking on new projects.</p>
        </div>
        <ul class="facts">
          <li><b>Frontend developer</b><span>in training</span></li>
          <li><b>HTML, CSS, Git</b><span>what I’m learning now</span></li>
          <li><b>Full-stack</b><span>where I’m headed</span></li>
        </ul>
      </div>
    </div>
  </section>

  <section id="skills">
    <div class="wrap">
      <h2>Skills &amp; tools</h2>
      <p class="sub">What I use today, and what I’m working toward.</p>
      <div class="chips">
        <span class="chip">HTML5</span>
        <span class="chip">CSS3</span>
        <span class="chip">Git</span>
        <span class="chip">GitHub</span>
        <span class="chip">VS Code</span>
        <span class="chip soon">JavaScript – next</span>
        <span class="chip soon">Full-stack – goal</span>
      </div>
    </div>
  </section>

  <section id="projects">
    <div class="wrap">
      <h2>Projects</h2>
      <p class="sub">My assignments and practice work. Each card opens the code on GitHub.</p>
      <div class="grid" id="projectGrid"></div>
    </div>
  </section>

  <section id="contact">
    <div class="wrap">
      <div class="glass contact">
        <h2>Let’s connect</h2>
        <p class="sub" style="margin:0 auto">I’m happy to collaborate, learn from others and work on new projects.</p>
        <div class="cta">
          <a class="btn main" href="https://github.com/hamzashaikh440692-hub" target="_blank" rel="noopener">GitHub</a>
          <a class="btn soft" href="https://instagram.com/not._.h4amza" target="_blank" rel="noopener">Instagram</a>
          <a class="btn soft" href="https://facebook.com/not._.h4amza" target="_blank" rel="noopener">Facebook</a>
          <!-- Add your email: <a class="btn soft" href="mailto:YOUR_EMAIL@gmail.com">Email</a> -->
        </div>
      </div>
    </div>
  </section>
</main>

<footer>© <span id="yr"></span> Hamza Shaikh</footer>

<script>
  var user = "hamzashaikh440692-hub";

  // Your repos. Edit the descriptions as you like.
  var projects = [
    {repo:"assignment-1",  title:"Assignment 1",  desc:"HTML assignment."},
    {repo:"assignment-2",  title:"Assignment 2",  desc:"HTML assignment."},
    {repo:"assignment-3",  title:"Assignment 3",  desc:"Multi-page website with home, menu, about and contact pages."},
    {repo:"assignment-4",  title:"Assignment 4",  desc:"HTML assignment."},
    {repo:"assignment-5",  title:"Assignment 5",  desc:"HTML assignment."},
    {repo:"assignment-6",  title:"Assignment 6",  desc:"HTML assignment."},
    {repo:"assignment-7",  title:"Assignment 7",  desc:"Page with social media icons (Instagram, Twitter, YouTube)."},
    {repo:"assignment-8",  title:"Assignment 8",  desc:"HTML assignment with three page versions."},
    {repo:"assignment-12", title:"Assignment 12", desc:"HTML assignment."},
    {repo:"assignment-13", title:"Assignment 13", desc:"Image-rich page with header, feedback and form sections."},
    {repo:"assignment-14", title:"Assignment 14", desc:"Page built with photos, logo and custom header."},
    {repo:"assignment-15", title:"Assignment 15", desc:"Photo page using AVIF images."},
    {repo:"assignment-16", title:"Assignment 16", desc:"Using grid to complete Assignment."},
  ];

  var grid = document.getElementById("projectGrid");
  var known = {};
  projects.forEach(function(p){ known[p.repo] = p; });

  function prettyName(name){
    return name.replace(/[-_]+/g, " ").replace(/\b\w/g, function(c){ return c.toUpperCase(); });
  }

  function link(text, href){
    var a = document.createElement("a");
    a.textContent = text; a.href = href; a.target = "_blank"; a.rel = "noopener";
    return a;
  }

  function render(list){
    grid.innerHTML = "";
    list.forEach(function(p){
      var card = document.createElement("div");
      card.className = "card glass";
      var h = document.createElement("h3"); h.textContent = p.title;
      var d = document.createElement("p"); d.textContent = p.desc;
      var links = document.createElement("div"); links.className = "links";
      if (p.live) links.appendChild(link("Live demo", p.live));
      links.appendChild(link("Code on GitHub", p.code));
      card.appendChild(h); card.appendChild(d); card.appendChild(links);
      grid.appendChild(card);
    });
  }

  function fromKnown(p){
    return {
      title: p.title, desc: p.desc,
      live: "https://" + user + ".github.io/" + p.repo + "/",
      code: "https://github.com/" + user + "/" + p.repo
    };
  }

  render(projects.map(fromKnown));

  // Also pulls any other public repo you create later
  fetch("https://api.github.com/users/" + user + "/repos?per_page=100")
    .then(function(r){ if(!r.ok) throw new Error("GitHub API error"); return r.json(); })
    .then(function(repos){
      var skip = [user.toLowerCase(), user.toLowerCase() + ".github.io"];
      var list = repos
        .filter(function(r){ return !r.fork && skip.indexOf(r.name.toLowerCase()) === -1; })
        .sort(function(a, b){ return a.name.localeCompare(b.name, undefined, {numeric:true}); })
        .map(function(r){
          var k = known[r.name];
          return {
            title: k ? k.title : prettyName(r.name),
            desc: r.description || (k ? k.desc : "Repository on GitHub."),
            live: r.has_pages ? "https://" + user + ".github.io/" + r.name + "/" : "",
            code: r.html_url
          };
        });
      if (list.length) render(list);
    })
    .catch(function(){ /* keep the list above */ });

  document.getElementById("yr").textContent = new Date().getFullYear();
</script>
</body>
</html>
