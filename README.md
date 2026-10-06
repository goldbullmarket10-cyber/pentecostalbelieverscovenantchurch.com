# pentecostalbelieverscovenantchurch.com
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Pentecostal Believers Covenant Church</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    scroll-behavior:smooth;
}

body{
    font-family:Arial,Helvetica,sans-serif;
    color:white;
    background:#020817;
    overflow-x:hidden;
}

/* =========================
   ANIMATED LIVE BACKGROUND
========================= */

.background{
    position:fixed;
    inset:0;
    overflow:hidden;
    z-index:-10;
    background:
        radial-gradient(circle at 20% 20%,#063b65 0%,transparent 30%),
        radial-gradient(circle at 80% 30%,#25105c 0%,transparent 32%),
        radial-gradient(circle at 50% 100%,#003d45 0%,transparent 35%),
        linear-gradient(135deg,#010510,#071a35,#09051f);
    background-size:200% 200%;
    animation:backgroundMove 12s ease-in-out infinite;
}

@keyframes backgroundMove{
    0%{
        background-position:0% 50%;
    }
    50%{
        background-position:100% 50%;
    }
    100%{
        background-position:0% 50%;
    }
}

/* Floating glowing circles */

.glow{
    position:absolute;
    border-radius:50%;
    filter:blur(35px);
    opacity:.45;
}

.glow1{
    width:300px;
    height:300px;
    background:#00aaff;
    top:5%;
    left:-100px;
    animation:float1 10s ease-in-out infinite alternate;
}

.glow2{
    width:280px;
    height:280px;
    background:#7b2cff;
    top:30%;
    right:-80px;
    animation:float2 12s ease-in-out infinite alternate;
}

.glow3{
    width:250px;
    height:250px;
    background:#00d9a5;
    bottom:-80px;
    left:25%;
    animation:float3 14s ease-in-out infinite alternate;
}

.glow4{
    width:180px;
    height:180px;
    background:#009dff;
    top:65%;
    right:25%;
    animation:float4 9s ease-in-out infinite alternate;
}

@keyframes float1{
    from{transform:translate(0,0) scale(1);}
    to{transform:translate(180px,120px) scale(1.3);}
}

@keyframes float2{
    from{transform:translate(0,0) scale(1);}
    to{transform:translate(-150px,100px) scale(1.2);}
}

@keyframes float3{
    from{transform:translate(0,0) scale(1);}
    to{transform:translate(130px,-150px) scale(1.3);}
}

@keyframes float4{
    from{transform:translate(0,0);}
    to{transform:translate(-120px,-100px);}
}

/* Animated particles */

.particle{
    position:absolute;
    width:5px;
    height:5px;
    background:#65d8ff;
    border-radius:50%;
    box-shadow:0 0 15px #65d8ff;
    animation:particleMove linear infinite;
}

.p1{left:8%;top:90%;animation-duration:12s;}
.p2{left:18%;top:70%;animation-duration:16s;}
.p3{left:30%;top:95%;animation-duration:13s;}
.p4{left:42%;top:80%;animation-duration:18s;}
.p5{left:55%;top:92%;animation-duration:14s;}
.p6{left:68%;top:75%;animation-duration:17s;}
.p7{left:80%;top:90%;animation-duration:11s;}
.p8{left:92%;top:70%;animation-duration:15s;}
.p9{left:50%;top:60%;animation-duration:20s;}
.p10{left:25%;top:50%;animation-duration:19s;}

@keyframes particleMove{
    0%{
        transform:translateY(0) translateX(0);
        opacity:0;
    }

    15%{
        opacity:1;
    }

    50%{
        transform:translateY(-400px) translateX(80px);
        opacity:.8;
    }

    100%{
        transform:translateY(-850px) translateX(-100px);
        opacity:0;
    }
}

/* Dark overlay for readability */

.background-overlay{
    position:absolute;
    inset:0;
    background:rgba(1,5,16,.35);
}

/* =========================
   NAVIGATION
========================= */

nav{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    z-index:1000;
    padding:18px 7%;
    background:rgba(1,7,20,.75);
    backdrop-filter:blur(15px);
    border-bottom:1px solid rgba(255,255,255,.1);
}

.nav-container{
    max-width:1200px;
    margin:auto;
    display:flex;
    align-items:center;
    justify-content:space-between;
}

.brand{
    font-size:18px;
    font-weight:bold;
    letter-spacing:1px;
}

.brand span{
    color:#49d0ff;
}

nav ul{
    display:flex;
    gap:25px;
    list-style:none;
}

nav a{
    color:white;
    text-decoration:none;
    font-size:14px;
    transition:.3s;
}

nav a:hover{
    color:#49d0ff;
}

/* =========================
   HERO
========================= */

.hero{
    min-height:100vh;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    padding:130px 20px 80px;
}

.hero-content{
    max-width:900px;
}

.hero small{
    color:#55d5ff;
    font-weight:bold;
    letter-spacing:4px;
    text-transform:uppercase;
}

.hero h1{
    font-size:clamp(40px,7vw,78px);
    line-height:1.05;
    margin:20px 0;
    text-shadow:0 5px 35px rgba(0,0,0,.7);
}

.hero h1 span{
    display:block;
    color:#50d2ff;
}

.hero p{
    max-width:720px;
    margin:0 auto 35px;
    line-height:1.8;
    color:#dce9f7;
    font-size:17px;
}

.buttons{
    display:flex;
    justify-content:center;
    gap:15px;
    flex-wrap:wrap;
}

.btn{
    display:inline-block;
    padding:15px 27px;
    border-radius:30px;
    text-decoration:none;
    font-weight:bold;
    transition:.3s;
}

.primary{
    background:#4bd0ff;
    color:#02101d;
    box-shadow:0 0 25px rgba(75,208,255,.35);
}

.secondary{
    border:1px solid rgba(255,255,255,.4);
    color:white;
    background:rgba(255,255,255,.05);
}

.btn:hover{
    transform:translateY(-4px);
}

/* =========================
   SECTIONS
========================= */

section{
    padding:95px 7%;
}

.container{
    max-width:1100px;
    margin:auto;
}

.section-title{
    text-align:center;
    margin-bottom:45px;
}

.section-title h2{
    font-size:38px;
    margin-bottom:12px;
}

.section-title p{
    color:#b8c9dc;
}

/* =========================
   ABOUT
========================= */

.about-card{
    background:rgba(255,255,255,.07);
    border:1px solid rgba(255,255,255,.12);
    border-radius:25px;
    padding:40px;
    backdrop-filter:blur(18px);
    box-shadow:0 20px 60px rgba(0,0,0,.2);
    line-height:1.9;
    color:#dce8f7;
}

/* =========================
   SERVICES
========================= */

.services{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:25px;
}

.service-card{
    padding:35px;
    background:rgba(255,255,255,.07);
    border:1px solid rgba(255,255,255,.1);
    border-radius:22px;
    backdrop-filter:blur(18px);
    transition:.4s;
}

.service-card:hover{
    transform:translateY(-8px);
    border-color:#4bd0ff;
    box-shadow:0 15px 40px rgba(0,0,0,.3);
}

.service-icon{
    font-size:38px;
    margin-bottom:18px;
}

.service-card h3{
    margin-bottom:12px;
}

.service-card p{
    color:#b9c9dc;
    line-height:1.7;
}

/* =========================
   FOUNDER
========================= */

.founder{
    text-align:center;
}

.founder-card{
    max-width:600px;
    margin:auto;
    padding:40px;
    border-radius:25px;
    background:rgba(255,255,255,.07);
    border:1px solid rgba(255,255,255,.1);
    backdrop-filter:blur(18px);
}

.founder-icon{
    width:90px;
    height:90px;
    border-radius:50%;
    margin:0 auto 20px;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:35px;
    background:linear-gradient(135deg,#45d1ff,#704cff);
    box-shadow:0 0 35px rgba(70,190,255,.35);
}

.founder-card h3{
    font-size:27px;
    margin-bottom:8px;
}

.founder-card p{
    color:#b9c9dc;
}

/* =========================
   CONTACT
========================= */

.contact-grid{
    display:grid;
    grid-template-columns:1fr 1.2fr;
    gap:30px;
}

.contact-info,
.contact-form{
    background:rgba(255,255,255,.07);
    border:1px solid rgba(255,255,255,.1);
    border-radius:25px;
    padding:35px;
    backdrop-filter:blur(18px);
}

.contact-info h3,
.contact-form h3{
    margin-bottom:25px;
    font-size:25px;
}

.contact-item{
    margin-bottom:22px;
    line-height:1.6;
}

.contact-item strong{
    display:block;
    color:#4bd0ff;
    margin-bottom:6px;
}

.contact-item a{
    color:white;
    text-decoration:none;
}

.contact-item a:hover{
    color:#4bd0ff;
}

/* =========================
   MESSAGE FORM
========================= */

form{
    display:flex;
    flex-direction:column;
    gap:15px;
}

input,
textarea{
    width:100%;
    padding:16px;
    border-radius:12px;
    border:1px solid rgba(255,255,255,.15);
    background:rgba(0,0,0,.3);
    color:white;
    outline:none;
    font-size:15px;
}

input:focus,
textarea:focus{
    border-color:#4bd0ff;
    box-shadow:0 0 12px rgba(75,208,255,.15);
}

textarea{
    min-height:150px;
    resize:vertical;
}

.submit-btn{
    border:none;
    padding:16px;
    border-radius:30px;
    background:#4bd0ff;
    color:#02101d;
    font-weight:bold;
    cursor:pointer;
    font-size:15px;
}

/* =========================
   SOCIAL MEDIA
========================= */

.facebook-btn{
    display:inline-block;
    margin-top:8px;
    padding:12px 20px;
    border-radius:25px;
    background:#1877f2;
    color:white !important;
    font-weight:bold;
}

/* =========================
   WHATSAPP
========================= */

.whatsapp{
    position:fixed;
    right:20px;
    bottom:20px;
    width:60px;
    height:60px;
    border-radius:50%;
    background:#25D366;
    color:white;
    display:flex;
    align-items:center;
    justify-content:center;
    text-decoration:none;
    font-size:28px;
    z-index:999;
    box-shadow:0 8px 30px rgba(0,0,0,.45);
    animation:whatsappPulse 2s infinite;
}

@keyframes whatsappPulse{
    0%{
        box-shadow:0 0 0 0 rgba(37,211,102,.6);
    }
    70%{
        box-shadow:0 0 0 18px rgba(37,211,102,0);
    }
    100%{
        box-shadow:0 0 0 0 rgba(37,211,102,0);
    }
}

/* =========================
   FOOTER
========================= */

footer{
    text-align:center;
    padding:40px 20px;
    background:rgba(0,0,0,.35);
    color:#9fb0c4;
}

footer strong{
    color:white;
}

footer a{
    color:#4bd0ff;
    text-decoration:none;
}

.social{
    margin-top:15px;
}

/* =========================
   MOBILE
========================= */

@media(max-width:700px){

    nav{
        padding:15px 5%;
    }

    .brand{
        font-size:14px;
    }

    nav ul{
        display:none;
    }

    .hero{
        padding-top:130px;
    }

    .hero h1{
        font-size:43px;
    }

    .hero p{
        font-size:15px;
    }

    section{
        padding:75px 5%;
    }

    .section-title h2{
        font-size:31px;
    }

    .services{
        grid-template-columns:1fr;
    }

    .contact-grid{
        grid-template-columns:1fr;
    }

    .about-card,
    .founder-card,
    .contact-info,
    .contact-form{
        padding:25px;
    }

    .glow1{
        width:200px;
        height:200px;
    }

    .glow2{
        width:200px;
        height:200px;
    }

    .glow3{
        width:180px;
        height:180px;
    }
}
</style>
</head>

<body>

<!-- LIVE ANIMATED BACKGROUND -->

<div class="background">

    <div class="background-overlay"></div>

    <div class="glow glow1"></div>
    <div class="glow glow2"></div>
    <div class="glow glow3"></div>
    <div class="glow glow4"></div>

    <div class="particle p1"></div>
    <div class="particle p2"></div>
    <div class="particle p3"></div>
    <div class="particle p4"></div>
    <div class="particle p5"></div>
    <div class="particle p6"></div>
    <div class="particle p7"></div>
    <div class="particle p8"></div>
    <div class="particle p9"></div>
    <div class="particle p10"></div>

</div>


<!-- NAVIGATION -->

<nav>

<div class="nav-container">

<div class="brand">
PBCC <span>CHURCH</span>
</div>

<ul>
<li><a href="#home">Home</a></li>
<li><a href="#about">About Us</a></li>
<li><a href="#services">Services</a></li>
<li><a href="#founder">Founder</a></li>
<li><a href="#contact">Contact</a></li>
</ul>

</div>

</nav>


<!-- HOME -->

<section class="hero" id="home">

<div class="hero-content">

<small>Welcome to</small>

<h1>
Pentecostal Believers
<span>Covenant Church</span>
</h1>

<p>
A Christ-centered church committed to spreading the Gospel of Jesus Christ
and helping people grow in faith
</p>

<div class="buttons">

<a href="#about" class="btn primary">
Discover More
</a>

<a href="#contact" class="btn secondary">
Contact Us
</a>

</div>

</div>

</section>


<!-- ABOUT -->

<section id="about">

<div class="container">

<div class="section-title">

<h2>About Us</h2>

<p>
Discover who we are and what we believe
</p>

</div>

<div class="about-card">

<p>
Pentecostal Believers Covenant Church is a Christ-centered church committed
to spreading the Gospel of Jesus Christ and helping people grow in faith
</p>

<br>

<p>
We are a place of worship prayer fellowship and spiritual transformation
where everyone is welcomed to encounter God and discover their purpose
</p>

</div>

</div>

</section>


<!-- SERVICES -->

<section id="services">

<div class="container">

<div class="section-title">

<h2>Our Services</h2>

<p>
Join us in worship prayer fellowship and the Word of God
</p>

</div>

<div class="services">

<div class="service-card">

<div class="service-icon">🙏</div>

<h3>Sunday Worship Service</h3>

<p>
Every Sunday at <strong>8:00 AM</strong>
</p>

<p>
Come and experience powerful worship prayer praise and the Word of God
</p>

</div>


<div class="service-card">

<div class="service-icon">📖</div>

<h3>Wednesday Service</h3>

<p>
Every Wednesday at <strong>4:00 PM</strong>
</p>

<p>
Join us for fellowship spiritual growth prayer and the teaching of God's Word
</p>

</div>

</div>

</div>

</section>


<!-- FOUNDER -->

<section id="founder">

<div class="container founder">

<div class="section-title">

<h2>Our Founder</h2>

<p>
The founder of Pentecostal Believers Covenant Church
</p>

</div>

<div class="founder-card">

<div class="founder-icon">
✝
</div>

<h3>Bishop Mohammed Naga</h3>

<p>
Founder of Pentecostal Believers Covenant Church
</p>

</div>

</div>

</section>


<!-- CONTACT -->

<section id="contact">

<div class="container">

<div class="section-title">

<h2>Contact Us</h2>

<p>
We would love to hear from you
</p>

</div>


<div class="contact-grid">


<!-- CONTACT INFORMATION -->

<div class="contact-info">

<h3>Get In Touch</h3>


<div class="contact-item">

<strong>Church Location</strong>

Gomari Old Airport

</div>


<div class="contact-item">

<strong>WhatsApp</strong>

<a href="https://wa.me/2347085837971" target="_blank">

+234 708 583 7971

</a>

</div>


<div class="contact-item">

<strong>Email</strong>

<a href="mailto:pentecostalbelieverscovenantchurch@gmail.com">

pentecostalbelieverscovenantchurch@gmail.com

</a>

</div>


<div class="contact-item">

<strong>Facebook</strong>

<a
class="facebook-btn"
href="https://www.facebook.com/profile.php?id=61550565295279"
target="_blank"
rel="noopener"
>

Visit Our Facebook Page

</a>

</div>

</div>


<!-- MESSAGE / TESTIMONY FORM -->

<div class="contact-form">

<h3>Send Us a Message</h3>

<form onsubmit="sendMessage(event)">

<input
type="text"
id="name"
placeholder="Full Name"
required
>

<input
type="email"
id="email"
placeholder="Email Address"
required
>

<textarea
id="message"
placeholder="Message / Testimony"
required
></textarea>

<button
type="submit"
class="submit-btn"
>

Send Message

</button>

</form>

</div>

</div>

</div>

</section>


<!-- FLOATING WHATSAPP -->

<a
class="whatsapp"
href="https://wa.me/2347085837971"
target="_blank"
rel="noopener"
title="Chat with us on WhatsApp"
>

☏

</a>


<!-- FOOTER -->

<footer>

<p>
<strong>Pentecostal Believers Covenant Church</strong>
</p>

<p>
Gomari Old Airport
</p>

<div class="social">

<a
href="https://www.facebook.com/profile.php?id=61550565295279"
target="_blank"
rel="noopener"
>

Facebook

</a>

</div>

<p style="margin-top:20px">

© 2026 Pentecostal Believers Covenant Church

</p>

</footer>


<!-- WEBSITE JAVASCRIPT -->

<script>

function sendMessage(event){

event.preventDefault();

const name =
document.getElementById("name").value;

const email =
document.getElementById("email").value;

const message =
document.getElementById("message").value;


/*
Prepare visitor's message
for the church WhatsApp
*/

const text =
"NEW MESSAGE FROM PBCC WEBSITE\n\n" +
"Full Name: " + name + "\n" +
"Email: " + email + "\n\n" +
"Message / Testimony:\n" +
message;


const whatsappURL =
"https://wa.me/2347085837971?text=" +
encodeURIComponent(text);


window.open(
whatsappURL,
"_blank"
);

}

</script>

</body>
</html>
