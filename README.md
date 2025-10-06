# CLAROFLEX-p-vot-slide
CLAROFLEX pívot slide 
<!DOCTYPE html>
<html lang="lt">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CLAROFLEX Pivot & Slide</title>
<meta name="description" content="CLAROFLEX Pivot ir Slide – inovatyvūs, patikimi sprendimai jūsų verslui.">
<style>
  :root {
    --red:#e30613;
    --gray:#4b4b4b;
    --lightgray:#f5f5f5;
    --white:#ffffff;
  }
  *{box-sizing:border-box;margin:0;padding:0;}
  body{font-family:'Arial',sans-serif;line-height:1.5;background:var(--lightgray);color:var(--gray);}
  header{background:var(--white);display:flex;justify-content:space-between;align-items:center;padding:20px 40px;box-shadow:0 2px 6px rgba(0,0,0,0.1);position:sticky;top:0;z-index:1000;}
  header .logo{font-weight:700;font-size:1.5rem;color:var(--red);}
  nav a{margin-left:20px;text-decoration:none;color:var(--gray);font-weight:500;}
  .hero{display:flex;flex-direction:column;align-items:center;text-align:center;padding:80px 20px;background:var(--white);}
  .hero h1{font-size:2.2rem;color:var(--red);}
  .hero p{color:var(--gray);margin-top:12px;max-width:700px;}
  .btn-primary{background:var(--red);color:var(--white);border:none;border-radius:8px;padding:14px 28px;font-size:1rem;font-weight:600;margin-top:24px;cursor:pointer;transition:0.3s;}
  .btn-primary:hover{background:#b2000d;}
  section{max-width:1100px;margin:0 auto;padding:60px 20px;}
  .features{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:20px;margin-top:40px;}
  .feature{background:var(--white);padding:24px;border-radius:12px;box-shadow:0 4px 12px rgba(0,0,0,0.05);opacity:0;transform:translateY(40px);transition:all 0.8s ease;}
  .feature.show{opacity:1;transform:translateY(0);}
  .feature h3{color:var(--red);margin-bottom:10px;}
  footer{text-align:center;padding:40px;background:var(--white);color:var(--gray);font-size:0.9rem;border-top:1px solid #ddd;}
</style>
</head>
<body>

<header>
  <div class="logo">CLAROFLEX</div>
  <nav>
    <a href="#features">Privalumai</a>
    <a href="#kontaktai">Kontaktai</a>
  </nav>
</header>

<section class="hero">
  <h1>CLAROFLEX Pivot & Slide</h1>
  <p>Inovatyvūs ir patikimi sprendimai jūsų verslui. Pagerinkite efektyvumą, sumažinkite sąnaudas ir pasiūlykite savo klientams aukščiausios kokybės patirtį.</p>
  <button class="btn-primary" onclick="document.getElementById('kontaktai').scrollIntoView({behavior:'smooth'})">Užsisakyti demonstraciją</button>
</section>

<section id="features">
  <h2 style="text-align:center;color:var(--red);">Kodėl verta rinktis Pivot & Slide?</h2>
  <div class="features">
    <div class="feature">
      <h3>💎 Aukšta kokybė</h3>
      <p>Patikrinti komponentai ir griežta kokybės kontrolė užtikrina patikimumą ilgalaikėje eksploatacijoje.</p>
    </div>
    <div class="feature">
      <h3>⚙️ Lankstumas</h3>
      <p>Pivot ir Slide sprendimai pritaikomi įvairiems projektams – nuo mažų biurų iki didelio masto komercinių objektų.</p>
    </div>
    <div class="feature">
      <h3>🤝 Patikimas palaikymas</h3>
      <p>Mūsų techninė ir komercinė komanda padeda kiekviename žingsnyje, užtikrinant sklandų diegimą ir naudojimą.</p>
    </div>
  </div>
</section>

<section id="kontaktai" style="text-align:center;">
  <h2 style="color:var(--red);">Susisiekite su mumis</h2>
  <p>Norite gauti pasiūlymą ar demonstraciją? Susisiekite dabar:</p>
  <p><strong>El. paštas:</strong> <a href="mailto:ventas@claroflex.example">ventas@claroflex.example</a><br>
     <strong>Telefonas:</strong> +370 600 00000</p>
  <button class="btn-primary" onclick="alert('Ačiū! Jūsų užklausa priimta.')">Išsiųsti užklausą</button>
</section>

<footer>
  © <span id="year"></span> CLAROFLEX. Visos teisės saugomos.
</footer>

<script>
  document.getElementById('year').textContent = new Date().getFullYear();

  // Animacija fade-in
  const features = document.querySelectorAll('.feature');
  const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if(entry.isIntersecting){
        entry.target.classList.add('show');
      }
    });
  }, { threshold: 0.2 });

  features.forEach(f => observer.observe(f));
</script>

</body>
</html>