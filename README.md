<html lang="en">
<head>
<meta charset="UTF-8">
<title>Danny Baylen</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600&family=Inter:wght@300;400;600&display=swap" rel="stylesheet">

<!-- Icons -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<style>
body {
  margin:0;
  font-family:'Inter', sans-serif;
  background: linear-gradient(to bottom, #000000, #1a1a1a, #3a3a3a);
  color:white;
  text-align:center;
}

/* HEADER */
header {
  background:url("images/header.jpg") center/cover no-repeat;
  padding:40px 20px;
  position:relative;
}

/* overlay */
header::after {
  content:"";
  position:absolute;
  inset:0;
  background:rgba(0,0,0,0.65);
  z-index:0;
}

header * {
  position:relative;
  z-index:1;
}

h1 {
  font-family:'Cinzel', serif;
  letter-spacing:6px;
  font-weight:600;
}

/* SOCIAL ICONS */
.social-top a {
  color:red;
  margin:0 12px;
  font-size:28px;
  text-decoration:none;
  transition:0.3s;
}

.social-top a:hover {
  text-shadow:0 0 10px red, 0 0 25px red;
  transform:scale(1.15);
}

/* NAV */
nav a {
  color:white;
  margin:0 12px;
  text-decoration:none;
  font-size:14px;
  opacity:0.8;
}

nav a:hover {
  opacity:1;
}

/* CONTACT BUTTON */
.contact-btn {
  display:inline-block;
  margin-top:15px;
  padding:10px 22px;
  border:1px solid white;
  border-radius:25px;
  color:white;
  text-decoration:none;
}

.contact-btn:hover {
  box-shadow:0 0 12px white;
}

/* SECTIONS */
section {
  padding:60px 20px;
}

.fade {
  opacity:0;
  transform:translateY(30px);
  transition:1s ease;
}
.fade.show {
  opacity:1;
  transform:translateY(0);
}

/* RECENT RELEASES */
.releases {
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
  gap:20px;
}

/* GALLERY */
.gallery {
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
  gap:15px;
  padding:20px;
}

.gallery img {
  width:100%;
  border-radius:8px;
}

/* VIDEOS */
.video-grid {
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
  gap:20px;
}

/* FOOTER */
footer {
  border-top:1px solid #333;
  padding:30px;
  font-size:14px;
}

iframe {
  border-radius:12px;
}

@media(max-width:600px){
  h1 {font-size:26px;}
}
</style>
</head>

<body>

<header>
  <div class="social-top">
    <a href="https://www.tiktok.com/@yesdanny"><i class="fab fa-tiktok"></i></a>
    <a href="https://www.youtube.com/c/DannyBaylen"><i class="fab fa-youtube"></i></a>
    <a href="https://www.instagram.com/dannybaylen/?hl=en"><i class="fab fa-instagram"></i></a>
    <a href="https://open.spotify.com/artist/1sEDsEf0zV8EWIl5ZwirGS"><i class="fab fa-spotify"></i></a>
    <a href="https://music.apple.com/ca/artist/danny-baylen/1745303435"><i class="fab fa-apple"></i></a>
  </div>

  <h1>DANNY BAYLEN</h1>

  <nav>
    <a href="#releases">RELEASES</a>
    <a href="#videos">VIDEOS</a>
    <a href="#gallery">PHOTOS</a>
  </nav>

  <a href="mailto:dannybaybusiness@gmail.com?subject=Booking%20Inquiry&body=Hi%20Danny," class="contact-btn">
    CONTACT
  </a>
</header>

<!-- RECENT RELEASES -->
<section id="releases" class="fade">
<h2>RECENT RELEASES</h2>

<div class="releases">
  <!-- Replace these with your Spotify embed track links -->
  <iframe src="<iframe data-testid="embed-iframe" style="border-radius:12px" src="https://open.spotify.com/embed/album/4vYp0KvPQHBsz7OBSjI1qw?utm_source=generator" width="100%" height="152" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>" width="100%" height="152" allow="encrypted-media"></iframe>
  <iframe src="<iframe data-testid="embed-iframe" style="border-radius:12px" src="https://open.spotify.com/embed/album/6aAF3r7pp1AUCxfkaabZrY?utm_source=generator" width="100%" height="152" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>" width="100%" height="152" allow="encrypted-media"></iframe>
</div>
</section>

<!-- ALL MUSIC -->
<section class="fade">
<h2>ALL MUSIC</h2>
<iframe src="https://open.spotify.com/embed/artist/1sEDsEf0zV8EWIl5ZwirGS?theme=0"
width="90%" height="380" allow="encrypted-media"></iframe>
</section>

<!-- VIDEOS -->
<section id="videos" class="fade">
<h2>VIDEOS</h2>
<div class="video-grid">
  <iframe src="https://www.youtube.com/embed/4GQ9soRIelU" width="100%" height="315" allowfullscreen></iframe>
  <iframe src="https://www.youtube.com/embed/VV155sd5uA8" width="100%" height="315" allowfullscreen></iframe>
</div>
</section>

<!-- GALLERY -->
<section id="gallery" class="fade">
<h2>PHOTOS</h2>
<div class="gallery">
  <img src="images/photo1.jpg">
  <img src="images/photo2.jpg">
  <img src="images/photo3.jpg">
  <img src="images/photo4.jpg">
</div>
</section>

<footer>
<p>© 2026 Danny Baylen</p>
</footer>

<script>
const fades = document.querySelectorAll(".fade");
const observer = new IntersectionObserver(entries=>{
  entries.forEach(entry=>{
    if(entry.isIntersecting){
      entry.target.classList.add("show");
    }
  });
});
fades.forEach(f=>observer.observe(f));
</script>

</body>
</html>
