<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kathula Srikanth Portfolio</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Poppins',sans-serif;
    scroll-behavior:smooth;
}

body{
    background:#0a0f1f;
    color:white;
    overflow-x:hidden;
}

/* Animated Background */
body::before{
    content:'';
    position:fixed;
    width:200%;
    height:200%;
    background:
    radial-gradient(circle,#00ffff22 2px,transparent 2px);
    background-size:60px 60px;
    animation:moveBg 20s linear infinite;
    z-index:-1;
}

@keyframes moveBg{
    from{transform:translate(0,0);}
    to{transform:translate(-60px,-60px);}
}

/* Navbar */
nav{
    position:fixed;
    top:0;
    width:100%;
    background:rgba(10,15,31,.9);
    backdrop-filter:blur(10px);
    padding:15px 8%;
    display:flex;
    justify-content:space-between;
    align-items:center;
    z-index:1000;
}

.logo{
    color:#00ffff;
    font-size:24px;
    font-weight:700;
}

nav ul{
    display:flex;
    gap:20px;
    list-style:none;
}

nav a{
    color:white;
    text-decoration:none;
    transition:.3s;
}

nav a:hover{
    color:#00ffff;
}

/* Hero */
.hero{
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    text-align:center;
    flex-direction:column;
    padding:100px 20px 50px;
}

.profile{
    width:180px;
    height:180px;
    border-radius:50%;
    background:linear-gradient(45deg,#00ffff,#00ff88);
    display:flex;
    justify-content:center;
    align-items:center;
    font-size:65px;
    font-weight:bold;
    color:#000;
    animation:float 4s ease-in-out infinite;
    box-shadow:0 0 30px #00ffff;
}

@keyframes float{
    0%,100%{transform:translateY(0);}
    50%{transform:translateY(-20px);}
}

.hero h1{
    font-size:3.5rem;
    margin-top:25px;
}

.hero span{
    color:#00ffff;
}

.hero p{
    margin-top:15px;
    color:#ccc;
    max-width:700px;
}

.btn{
    margin-top:25px;
    display:inline-block;
    padding:14px 35px;
    background:#00ffff;
    color:#000;
    text-decoration:none;
    border-radius:30px;
    font-weight:600;
    transition:.3s;
}

.btn:hover{
    transform:scale(1.1);
    box-shadow:0 0 25px #00ffff;
}

/* Sections */
section{
    padding:80px 8%;
}

.section-title{
    text-align:center;
    font-size:2.5rem;
    color:#00ffff;
    margin-bottom:40px;
}

.about{
    max-width:900px;
    margin:auto;
    text-align:center;
    line-height:1.9;
    color:#ddd;
}

/* Skills */
.skills-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:25px;
}

.card{
    background:#131b33;
    padding:30px;
    border-radius:20px;
    text-align:center;
    transition:.4s;
    border:1px solid rgba(255,255,255,.1);
}

.card:hover{
    transform:translateY(-10px);
    box-shadow:0 0 25px #00ffff;
}

.card h3{
    margin-bottom:15px;
    color:#00ffff;
}

/* Contact */
.contact-box{
    max-width:600px;
    margin:auto;
    background:#131b33;
    padding:35px;
    border-radius:20px;
    text-align:center;
    line-height:2;
    transition:.4s;
}

.contact-box:hover{
    box-shadow:0 0 25px #00ffff;
}

/* Footer */
footer{
    text-align:center;
    padding:20px;
    background:#070b15;
    color:#aaa;
}

/* Animation */
.fade{
    animation:fadeUp 1s ease;
}

@keyframes fadeUp{
    from{
        opacity:0;
        transform:translateY(40px);
    }
    to{
        opacity:1;
        transform:translateY(0);
    }
}

/* Mobile */
@media(max-width:768px){

.hero h1{
    font-size:2.3rem;
}

nav ul{
    gap:10px;
    font-size:14px;
}

.profile{
    width:140px;
    height:140px;
    font-size:50px;
}
}
</style>
</head>
<body>

<nav>
    <div class="logo">KS Portfolio</div>
    <ul>
        <li><a href="#about">About</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#contact">Contact</a></li>
    </ul>
</nav>

<section class="hero fade">
    <div class="profile">KS</div>

    <h1>Kathula <span>Srikanth</span></h1>

    <p>
        B.Tech Graduate • Web Designer • Database Management Enthusiast
        creating modern, responsive and user-friendly web experiences.
    </p>

    <a href="#contact" class="btn">Hire Me</a>
</section>

<section id="about" class="fade">
    <h2 class="section-title">About Me</h2>

    <div class="about">
        <p>
            Hello! I'm <strong>Kathula Srikanth</strong>, a B.Tech graduate
            passionate about web design and database management.
            I enjoy building attractive websites, creating smooth user
            experiences, and managing data efficiently.
            My goal is to develop innovative digital solutions while
            continuously learning new technologies.
        </p>
    </div>
</section>

<section id="skills" class="fade">
    <h2 class="section-title">My Skills</h2>

    <div class="skills-grid">

        <div class="card">
            <h3>🌐 Web Design</h3>
            <p>HTML, CSS, Responsive Design, UI/UX Design</p>
        </div>

        <div class="card">
            <h3>🗄 Database Management</h3>
            <p>MySQL, Data Modeling, Database Optimization</p>
        </div>

        <div class="card">
            <h3>💻 Frontend Development</h3>
            <p>Interactive Interfaces, Animations, Modern Layouts</p>
        </div>

    </div>
</section>

<section id="contact" class="fade">
    <h2 class="section-title">Contact Me</h2>

    <div class="contact-box">
        <h3>Let's Work Together</h3>
        <p>📞 8106119545</p>
        <p>📧 srikanthyadav0820@gmail.com</p>
    </div>
</section>

<footer>
    © 2026 Kathula Srikanth | All Rights Reserved
</footer>

</body>
</html>