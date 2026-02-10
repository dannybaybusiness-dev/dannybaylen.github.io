<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Danny Baylen</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- Font -->
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600&display=swap" rel="stylesheet">

<!-- Icons -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<style>
body {
  margin:0;
  font-family:'Inter', sans-serif;
  background:black;
  color:white;
  text-align:center;
}

header {
  padding:30px 20px;
  border-bottom:1px solid #222;
}

h1 {
  letter-spacing:6px;
  font-weight:400;
}

.social-top {
  margin-bottom:15px;
}

.social-top a {
  color:white;
  margin:0 10px;
  font-size:20px;
  text-decoration:none;
  opacity:0.8;
}

.social-top a:hover {
  opacity:1;
}

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

.contact-btn {
  display:inline-block;
  margin-top:15px;
  padding:10px 22px;
  border:1px solid white;
  border-radius:25px;
  text-decoration:none;
  color:white;
  font-size:14px;
}

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

audio {
  width:90%;
  max-width:400px;
}

.gallery {
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
  gap:15px;
  padding:20px;
}

.gallery img {
  width:100%;
  border-radius:6px;
}

.video-grid {
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
  gap:20px;
}

footer {
  border-top:1px solid #222;
  padding:30px;
  font-size:14px;
}

@media(max-width:600px){
  h1 {font-size:26px;}
}
</style>
</head>

<body>

<header>

  <!-- SOCIAL ICONS TOP -->
  <div class="social-top">
    <a href="https://www.tiktok.com/@yesdanny"><i class="fab fa-tiktok"></i></a>
    <a href="https://www.youtube.com/c/DannyBaylen"><i class="fab fa-youtube"></i></a>
    <a href="https://www.instagram.com/dannybaylen/?hl=en"><i class="fab fa-instagram"></i></a>
    <a href="https://open.spotify.com/artist/1sEDsEf0zV8EWIl5ZwirGS"><i class="fab fa-spotify"></i></a>
    <a href="https://music.apple.com/ca/artist/danny-baylen/1745303435"><i class="fab fa-apple"></i></a>
  </div>

  <h1>DANNY BAYLEN</h1>

  <nav>
    <a href="#music">MUSIC</a>
    <a href="#videos">VIDEOS</a>
    <a href="#gallery">PHOTOS</a>
  </nav>

  <!-- CONTACT BUTTON -->
  <a href="mailto:dannybaybusiness@gmail.com" class="contact-btn">CONTACT</a>

</header>

<section id="music" class="fade">
  <h2>MUSIC</h2>
  <audio controls>
    <source src="your-song.mp3" type="audio/mpeg">
  </audio>
</section>

<section id="videos" class="fade">
  <h2>VIDEOS</h2>
  <div class="video-grid">
    <iframe src="https://www.youtube.com/embed/4GQ9soRIelU" width="100%" height="315" allowfullscreen></iframe>
    <iframe src="https://www.youtube.com/embed/VV155sd5uA8" width="100%" height="315" allowfullscreen></iframe>
  </div>
</section>

<section id="gallery" class="fade">
  <h2>PHOTOS</h2>
  <div class="gallery">
    <img src="photo1.jpg">
    <img src="photo2.jpg">
    <img src="photo3.jpg">
    <img src="photo4.jpg">
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
