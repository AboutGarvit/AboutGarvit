<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Garvit | Developer Portfolio</title>

<meta name="description" content="Garvit's personal developer portfolio - projects, skills, interests and contact information.">

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Manrope:wght@400;500;600;700;800&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet">

<style>

/* =====================================================
   ROOT
===================================================== */

:root {
    --bg: #08090c;
    --surface: #101217;
    --surface-light: #161920;

    --text: #f4f4f5;
    --muted: #9297a3;

    --primary: #a3ff12;
    --primary-dark: #6da900;

    --border: rgba(255,255,255,.09);

    --radius: 22px;

    --container: 1180px;
}


/* =====================================================
   RESET
===================================================== */

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: "Manrope", sans-serif;
    background:
        radial-gradient(circle at 80% 10%, rgba(163,255,18,.08), transparent 30%),
        var(--bg);

    color: var(--text);
    overflow-x: hidden;
}

a {
    color: inherit;
    text-decoration: none;
}

button,
input,
textarea {
    font: inherit;
}

img {
    max-width: 100%;
    display: block;
}

::selection {
    background: var(--primary);
    color: #000;
}


/* =====================================================
   BACKGROUND
===================================================== */

.grid-background {
    position: fixed;
    inset: 0;
    z-index: -2;

    background-image:
        linear-gradient(rgba(255,255,255,.025) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,.025) 1px, transparent 1px);

    background-size: 55px 55px;

    mask-image:
        linear-gradient(to bottom, black, transparent 85%);
}

.glow {
    position: fixed;

    width: 500px;
    height: 500px;

    border-radius: 50%;

    background: rgba(163,255,18,.08);

    filter: blur(150px);

    z-index: -1;

    right: -200px;
    top: 250px;
}


/* =====================================================
   CONTAINER
===================================================== */

.container {
    width: min(92%, var(--container));
    margin: auto;
}


/* =====================================================
   NAVBAR
===================================================== */

.navbar {
    position: fixed;

    top: 20px;
    left: 50%;

    transform: translateX(-50%);

    width: min(92%, 1180px);

    height: 66px;

    display: flex;
    align-items: center;
    justify-content: space-between;

    padding: 0 12px 0 25px;

    background: rgba(12,13,17,.78);

    border: 1px solid var(--border);

    backdrop-filter: blur(20px);

    border-radius: 100px;

    z-index: 1000;
}

.logo {
    font-family: "Space Grotesk";
    font-size: 21px;
    font-weight: 700;
}

.logo span {
    color: var(--primary);
}

.nav-links {
    display: flex;
    gap: 30px;
}

.nav-links a {
    font-size: 14px;
    color: var(--muted);

    transition: .25s;
}

.nav-links a:hover {
    color: var(--text);
}

.nav-button {
    padding: 12px 22px;

    background: var(--primary);

    color: #080808;

    border-radius: 100px;

    font-size: 14px;
    font-weight: 800;

    transition: .25s;
}

.nav-button:hover {
    transform: translateY(-2px);

    box-shadow:
        0 10px 30px rgba(163,255,18,.2);
}

.menu-button {
    display: none;

    width: 43px;
    height: 43px;

    border: none;
    border-radius: 50%;

    background: var(--surface-light);

    color: white;

    cursor: pointer;

    font-size: 19px;
}


/* =====================================================
   HERO
===================================================== */

.hero {
    min-height: 100vh;

    display: flex;
    align-items: center;

    padding-top: 120px;
    padding-bottom: 60px;
}

.hero-layout {
    display: grid;

    grid-template-columns:
        minmax(0, 1.2fr)
        minmax(320px, .8fr);

    align-items: center;

    gap: 80px;
}

.status {
    display: inline-flex;

    align-items: center;

    gap: 10px;

    margin-bottom: 25px;

    padding: 8px 14px;

    border: 1px solid var(--border);

    border-radius: 100px;

    background: rgba(255,255,255,.03);

    color: var(--muted);

    font-size: 13px;
}

.status-dot {
    width: 8px;
    height: 8px;

    background: var(--primary);

    border-radius: 50%;

    box-shadow:
        0 0 15px var(--primary);
}

.hero-small {
    color: var(--muted);

    font-size: 16px;

    margin-bottom: 10px;
}

.hero h1 {
    font-family: "Space Grotesk";

    font-size: clamp(60px, 8vw, 115px);

    line-height: .88;

    letter-spacing: -7px;

    margin-bottom: 30px;
}

.hero h1 span {
    color: var(--primary);
}

.hero-description {
    max-width: 650px;

    color: var(--muted);

    line-height: 1.8;

    font-size: 17px;
}

.hero-actions {
    display: flex;

    gap: 14px;

    flex-wrap: wrap;

    margin-top: 35px;
}

.button-primary,
.button-secondary {
    padding: 15px 24px;

    border-radius: 100px;

    font-weight: 700;

    font-size: 14px;

    transition: .3s;
}

.button-primary {
    background: var(--primary);

    color: #080808;
}

.button-primary:hover {
    transform: translateY(-3px);

    box-shadow:
        0 15px 40px rgba(163,255,18,.2);
}

.button-secondary {
    border: 1px solid var(--border);

    background: rgba(255,255,255,.03);
}

.button-secondary:hover {
    border-color: var(--primary);

    color: var(--primary);
}


/* =====================================================
   HERO PROFILE
===================================================== */

.profile-wrapper {
    position: relative;

    max-width: 420px;

    margin-left: auto;
}

.profile-number {
    position: absolute;

    top: -40px;
    right: 0;

    font-family: "Space Grotesk";

    font-size: 100px;

    font-weight: 700;

    color: rgba(255,255,255,.03);

    z-index: -1;
}

.profile-card {
    padding: 12px;

    border: 1px solid var(--border);

    background: rgba(255,255,255,.025);

    border-radius: 32px;

    transform: rotate(2deg);

    transition: .4s;
}

.profile-card:hover {
    transform: rotate(0);
}

.profile-image {
    position: relative;

    height: 500px;

    border-radius: 24px;

    overflow: hidden;

    background: var(--surface);
}

.profile-image img {
    width: 100%;
    height: 100%;

    object-fit: cover;
}

.profile-overlay {
    position: absolute;

    bottom: 0;
    left: 0;
    right: 0;

    padding: 80px 25px 25px;

    background:
        linear-gradient(
            transparent,
            rgba(0,0,0,.9)
        );
}

.profile-overlay h3 {
    font-family: "Space Grotesk";

    font-size: 25px;
}

.profile-overlay p {
    color: #bbb;

    font-size: 14px;

    margin-top: 5px;
}

.floating-tag {
    position: absolute;

    padding: 10px 16px;

    background: var(--primary);

    color: #080808;

    border-radius: 100px;

    font-size: 13px;

    font-weight: 800;

    box-shadow:
        0 15px 40px rgba(0,0,0,.4);
}

.tag-one {
    left: -45px;
    top: 100px;
}

.tag-two {
    right: -30px;
    bottom: 110px;

    background: white;
}


/* =====================================================
   INFO STRIP
===================================================== */

.info-strip {
    border-top: 1px solid var(--border);
    border-bottom: 1px solid var(--border);

    padding: 25px 0;
}

.info-grid {
    display: grid;

    grid-template-columns:
        repeat(4,1fr);

    gap: 20px;
}

.info-item {
    border-right:
        1px solid var(--border);

    padding: 5px 25px;
}

.info-item:first-child {
    padding-left: 0;
}

.info-item:last-child {
    border: none;
}

.info-label {
    color: var(--muted);

    font-size: 12px;

    text-transform: uppercase;

    letter-spacing: 1.5px;

    margin-bottom: 7px;
}

.info-value {
    font-family: "Space Grotesk";

    font-size: 17px;
}


/* =====================================================
   GENERAL SECTIONS
===================================================== */

.section {
    padding: 120px 0;
}

.section-header {
    display: grid;

    grid-template-columns:
        .7fr 1.3fr;

    gap: 60px;

    margin-bottom: 70px;
}

.section-label {
    color: var(--primary);

    font-size: 13px;

    text-transform: uppercase;

    letter-spacing: 2px;
}

.section-title {
    font-family: "Space Grotesk";

    font-size: clamp(40px,5vw,70px);

    line-height: 1;

    letter-spacing: -3px;
}

.section-description {
    color: var(--muted);

    line-height: 1.8;

    margin-top: 20px;

    max-width: 700px;
}


/* =====================================================
   ABOUT
===================================================== */

.about-layout {
    display: grid;

    grid-template-columns:
        1.3fr .7fr;

    gap: 30px;
}

.about-main,
.about-side {
    background: var(--surface);

    border: 1px solid var(--border);

    border-radius: var(--radius);
}

.about-main {
    padding: 45px;
}

.about-main p {
    color: var(--muted);

    font-size: 17px;

    line-height: 1.9;

    margin-bottom: 18px;
}

.about-main strong {
    color: white;
}

.about-side {
    padding: 35px;

    display: flex;

    flex-direction: column;

    justify-content: space-between;
}

.about-side h3 {
    font-family: "Space Grotesk";

    font-size: 28px;
}

.current-list {
    margin-top: 30px;
}

.current-item {
    padding: 18px 0;

    border-bottom:
        1px solid var(--border);
}

.current-item:last-child {
    border: none;
}

.current-item span {
    color: var(--muted);

    display: block;

    font-size: 12px;

    margin-bottom: 5px;

    text-transform: uppercase;
}


/* =====================================================
   SKILLS
===================================================== */

.skills-layout {
    display: grid;

    grid-template-columns:
        repeat(2,1fr);

    gap: 20px;
}

.skill-box {
    padding: 35px;

    border: 1px solid var(--border);

    background: var(--surface);

    border-radius: var(--radius);

    transition: .3s;
}

.skill-box:hover {
    transform: translateY(-5px);

    border-color:
        rgba(163,255,18,.4);
}

.skill-number {
    color: var(--primary);

    font-family: "Space Grotesk";

    margin-bottom: 45px;
}

.skill-box h3 {
    font-family: "Space Grotesk";

    font-size: 28px;

    margin-bottom: 15px;
}

.skill-box p {
    color: var(--muted);

    line-height: 1.7;
}

.skill-tags {
    display: flex;

    flex-wrap: wrap;

    gap: 8px;

    margin-top: 25px;
}

.skill-tag {
    padding: 8px 13px;

    border: 1px solid var(--border);

    border-radius: 100px;

    color: #c7c9ce;

    font-size: 12px;
}


/* =====================================================
   PROJECTS
===================================================== */

.projects {
    display: grid;

    gap: 25px;
}

.project {
    display: grid;

    grid-template-columns:
        1.1fr .9fr;

    min-height: 380px;

    background: var(--surface);

    border: 1px solid var(--border);

    border-radius: 28px;

    overflow: hidden;

    transition: .4s;
}

.project:hover {
    transform: translateY(-5px);

    border-color:
        rgba(163,255,18,.3);
}

.project-image {
    overflow: hidden;

    min-height: 350px;
}

.project-image img {
    width: 100%;
    height: 100%;

    object-fit: cover;

    transition: .6s;
}

.project:hover img {
    transform: scale(1.05);
}

.project-content {
    padding: 45px;

    display: flex;

    flex-direction: column;

    justify-content: center;
}

.project-index {
    color: var(--primary);

    font-size: 13px;

    margin-bottom: 30px;
}

.project h3 {
    font-family: "Space Grotesk";

    font-size: 36px;

    margin-bottom: 15px;
}

.project p {
    color: var(--muted);

    line-height: 1.8;
}

.project-tech {
    display: flex;

    flex-wrap: wrap;

    gap: 8px;

    margin-top: 25px;
}

.project-tech span {
    padding: 7px 12px;

    border-radius: 100px;

    background: rgba(255,255,255,.05);

    font-size: 12px;
}


/* =====================================================
   PERSONAL
===================================================== */

.personal-grid {
    display: grid;

    grid-template-columns:
        repeat(3,1fr);

    gap: 20px;
}

.personal-card {
    position: relative;

    min-height: 270px;

    padding: 30px;

    background: var(--surface);

    border: 1px solid var(--border);

    border-radius: var(--radius);

    overflow: hidden;

    transition: .3s;
}

.personal-card:hover {
    transform: translateY(-5px);
}

.personal-icon {
    font-size: 35px;

    margin-bottom: 55px;
}

.personal-card h3 {
    font-family: "Space Grotesk";

    font-size: 25px;

    margin-bottom: 10px;
}

.personal-card p {
    color: var(--muted);

    line-height: 1.7;
}

.personal-big {
    grid-column: span 2;

    background:
        linear-gradient(
            135deg,
            #a3ff12,
            #75ba00
        );

    color: #080808;
}

.personal-big p {
    color: rgba(0,0,0,.65);
}

.quote {
    font-family: "Space Grotesk";

    font-size: 32px;

    line-height: 1.2;

    max-width: 600px;
}


/* =====================================================
   CONTACT
===================================================== */

.contact-wrapper {
    padding: 70px;

    background: var(--primary);

    color: #080808;

    border-radius: 35px;
}

.contact-top {
    display: grid;

    grid-template-columns:
        1.3fr .7fr;

    gap: 50px;

    align-items: end;
}

.contact-wrapper h2 {
    font-family: "Space Grotesk";

    font-size: clamp(50px,7vw,95px);

    line-height: .9;

    letter-spacing: -5px;
}

.contact-text {
    line-height: 1.7;

    color: rgba(0,0,0,.65);
}

.contact-list {
    display: grid;

    grid-template-columns:
        repeat(2,1fr);

    margin-top: 60px;

    border-top:
        1px solid rgba(0,0,0,.2);
}

.contact-item {
    padding: 25px 0;

    border-bottom:
        1px solid rgba(0,0,0,.2);
}

.contact-item:nth-child(odd) {
    border-right:
        1px solid rgba(0,0,0,.2);
}

.contact-item:nth-child(even) {
    padding-left: 30px;
}

.contact-item small {
    display: block;

    color: rgba(0,0,0,.55);

    margin-bottom: 8px;
}

.contact-item a {
    font-family: "Space Grotesk";

    font-size: 18px;

    font-weight: 600;
}


/* =====================================================
   FOOTER
===================================================== */

footer {
    padding: 40px 0;

    color: var(--muted);
}

.footer-content {
    display: flex;

    justify-content: space-between;

    align-items: center;

    font-size: 13px;
}


/* =====================================================
   REVEAL ANIMATION
===================================================== */

.reveal {
    opacity: 0;

    transform:
        translateY(40px);

    transition:
        opacity .7s,
        transform .7s;
}

.reveal.active {
    opacity: 1;

    transform:
        translateY(0);
}


/* =====================================================
   RESPONSIVE
===================================================== */

@media(max-width:900px) {

    .nav-links,
    .nav-button {
        display: none;
    }

    .menu-button {
        display: block;
    }

    .hero-layout {
        grid-template-columns: 1fr;

        gap: 60px;
    }

    .profile-wrapper {
        margin: auto;

        width: 100%;
    }

    .hero h1 {
        letter-spacing: -4px;
    }

    .info-grid {
        grid-template-columns:
            repeat(2,1fr);
    }

    .info-item {
        border: none;

        padding: 15px 0;
    }

    .section-header {
        grid-template-columns: 1fr;

        gap: 20px;
    }

    .about-layout,
    .project,
    .contact-top {
        grid-template-columns: 1fr;
    }

    .skills-layout {
        grid-template-columns: 1fr;
    }

    .personal-grid {
        grid-template-columns: 1fr 1fr;
    }

    .personal-big {
        grid-column: span 2;
    }

}


@media(max-width:600px) {

    .navbar {
        top: 10px;
    }

    .hero {
        padding-top: 130px;
    }

    .hero h1 {
        font-size: 62px;

        letter-spacing: -4px;
    }

    .profile-image {
        height: 420px;
    }

    .floating-tag {
        display: none;
    }

    .section {
        padding: 85px 0;
    }

    .section-title {
        font-size: 45px;
    }

    .about-main,
    .about-side,
    .skill-box,
    .project-content {
        padding: 28px;
    }

    .personal-grid {
        grid-template-columns: 1fr;
    }

    .personal-big {
        grid-column: span 1;
    }

    .contact-wrapper {
        padding: 40px 25px;
    }

    .contact-wrapper h2 {
        font-size: 55px;

        letter-spacing: -3px;
    }

    .contact-list {
        grid-template-columns: 1fr;
    }

    .contact-item:nth-child(odd) {
        border-right: none;
    }

    .contact-item:nth-child(even) {
        padding-left: 0;
    }

    .footer-content {
        flex-direction: column;

        gap: 10px;
    }

}

</style>
</head>


<body>

<div class="grid-background"></div>
<div class="glow"></div>


<!-- ==================================================
NAVBAR
================================================== -->

<nav class="navbar">

    <a href="#home" class="logo">
        About<span>Garvit.</span>
    </a>

    <div class="nav-links">

        <a href="#about">About</a>

        <a href="#skills">Skills</a>

        <a href="#projects">Projects</a>

        <a href="#personal">Personal</a>

        <a href="#contact">Contact</a>

    </div>

    <a href="#contact" class="nav-button">
        Let's Connect
    </a>

    <button class="menu-button" id="menuButton">
        ☰
    </button>

</nav>


<!-- ==================================================
HERO
================================================== -->

<section class="hero" id="home">

<div class="container">

<div class="hero-layout">


<!-- LEFT -->

<div>

    <div class="status">

        <span class="status-dot"></span>

        Developer • Student • Builder

    </div>


    <p class="hero-small">
        Hello !! This is
    </p>


    <h1>

        GARVIT<span>.</span>

    </h1>


    <p class="hero-description">

        I'm a developer who enjoys turning ideas into
        real projects. I build websites, Python applications
        and Telegram bots while continuously exploring
        new technologies and improving my development skills.

    </p>


    <div class="hero-actions">

        <a
        href="#projects"
        class="button-primary">

            Explore My Work ↗

        </a>


        <a
        href="https://github.com/AboutGarvit"
        target="_blank"
        class="button-secondary">

            GitHub

        </a>

    </div>

</div>



<!-- RIGHT PROFILE -->

<div class="profile-wrapper">

    <div class="profile-number">
        01
    </div>


    <div class="profile-card">


        <div class="profile-image">


            <!--
            =================================================

            CHANGE YOUR IMAGE HERE

            Put your image inside the same folder
            as index.html.

            Example:

            src="images/changli.jpeg"

            =================================================
            -->


            <img
            src="images/changli.jpeg"
            alt="Garvit">


            <div class="profile-overlay">

                <h3>
                    Garvit Sharma
                </h3>

                <p>
                    B.Tech CSE • Developer
                </p>

            </div>


        </div>

    </div>


    <div class="floating-tag tag-one">
        🐍 Python
    </div>


    <div class="floating-tag tag-two">
        🤖 Bot Developer
    </div>


</div>


</div>

</div>

</section>



<!-- ==================================================
INFO
================================================== -->

<section class="info-strip">

<div class="container">

<div class="info-grid">


<div class="info-item">

    <div class="info-label">
        Based In
    </div>

    <div class="info-value">
        Meerut, Uttar Pradesh
    </div>

</div>


<div class="info-item">

    <div class="info-label">
        Main Focus
    </div>

    <div class="info-value">
        Python Development
    </div>

</div>


<div class="info-item">

    <div class="info-label">
        Currently
    </div>

    <div class="info-value">
        B.Tech CSE Student
    </div>

</div>


<div class="info-item">

    <div class="info-label">
        Status
    </div>

    <div class="info-value">
        Building & Learning
    </div>

</div>


</div>

</div>

</section>



<!-- ==================================================
ABOUT
================================================== -->

<section class="section" id="about">

<div class="container">


<div class="section-header reveal">


<div>

    <span class="section-label">
        01 / About
    </span>

</div>


<div>

    <h2 class="section-title">

        A little more
        about me.

    </h2>


    <p class="section-description">

        Technology, development, gaming and curiosity
        are a big part of who I am.

    </p>

</div>


</div>



<div class="about-layout">


<div class="about-main reveal">


<p>

    I'm <strong>Garvit</strong>, a B.Tech Computer Science
    student from Meerut, Uttar Pradesh.

</p>


<p>

    I enjoy learning how technology works and then using
    that knowledge to build my own projects. A large part
    of my development journey has been focused on
    <strong>Python and Telegram bot development</strong>.

</p>


<p>

    I enjoy working on gaming bots, automation systems,
    websites and experimental projects where I can learn
    something new while creating something useful.

</p>


<p>

    Outside development, you'll usually find me exploring
    games, watching anime, reading, learning new technology
    or planning another project to build.

</p>


</div>



<div class="about-side reveal">


<div>

<h3>
Currently exploring
</h3>


<div class="current-list">


<div class="current-item">

<span>
Development
</span>

Telegram Gaming Bots

</div>


<div class="current-item">

<span>
Learning
</span>

Data Structures & Algorithms

</div>


<div class="current-item">

<span>
Academic Goal
</span>

GATE Preparation

</div>


<div class="current-item">

<span>
Interest
</span>

Open Source Projects

</div>


</div>

</div>


</div>


</div>

</div>

</section>



<!-- ==================================================
SKILLS
================================================== -->

<section class="section" id="skills">

<div class="container">


<div class="section-header reveal">


<div>

<span class="section-label">
02 / Skills
</span>

</div>


<div>

<h2 class="section-title">

Things I work
with.

</h2>


<p class="section-description">

Technologies and areas that I currently use,
learn and experiment with.

</p>

</div>


</div>



<div class="skills-layout">


<div class="skill-box reveal">

<div class="skill-number">
01
</div>

<h3>
Programming
</h3>

<p>

My primary programming focus is Python,
with additional experience in web technologies
and programming fundamentals.

</p>


<div class="skill-tags">

<span class="skill-tag">
Python
</span>

<span class="skill-tag">
C
</span>

<span class="skill-tag">
HTML
</span>

<span class="skill-tag">
CSS
</span>

<span class="skill-tag">
JavaScript
</span>

</div>

</div>



<div class="skill-box reveal">

<div class="skill-number">
02
</div>

<h3>
Telegram Development
</h3>

<p>

Building Telegram bots ranging from simple
automation tools to interactive gaming systems.

</p>


<div class="skill-tags">

<span class="skill-tag">
python-telegram-bot
</span>

<span class="skill-tag">
Pyrogram
</span>

<span class="skill-tag">
Telethon
</span>

<span class="skill-tag">
aiogram
</span>

<span class="skill-tag">
Telegram API
</span>

</div>

</div>



<div class="skill-box reveal">

<div class="skill-number">
03
</div>

<h3>
Tools
</h3>

<p>

Tools and platforms I use while developing,
testing and managing my projects.

</p>


<div class="skill-tags">

<span class="skill-tag">
VS Code
</span>

<span class="skill-tag">
Git
</span>

<span class="skill-tag">
GitHub
</span>

<span class="skill-tag">
Windows
</span>

<span class="skill-tag">
Linux
</span>

</div>

</div>



<div class="skill-box reveal">

<div class="skill-number">
04
</div>

<h3>
Currently Learning
</h3>

<p>

Computer Science concepts and technologies
that I am actively studying and improving.

</p>


<div class="skill-tags">

<span class="skill-tag">
DSA
</span>

<span class="skill-tag">
Algorithms
</span>

<span class="skill-tag">
Databases
</span>

<span class="skill-tag">
Computer Networks
</span>

<span class="skill-tag">
System Design
</span>

</div>

</div>


</div>

</div>

</section>



<!-- ==================================================
PROJECTS
================================================== -->

<section class="section" id="projects">

<div class="container">


<div class="section-header reveal">


<div>

<span class="section-label">
03 / Projects
</span>

</div>


<div>

<h2 class="section-title">

Some things
I've built.

</h2>


<p class="section-description">

A selection of development projects and ideas
I've worked on.

</p>

</div>


</div>



<div class="projects">


<!-- PROJECT 1 -->

<article class="project reveal">


<div class="project-image">

<img
src="https://images.unsplash.com/photo-1550745165-9bc0b252726f?auto=format&fit=crop&w=1200&q=80"
alt="Gaming Bot">

</div>


<div class="project-content">


<div class="project-index">

PROJECT / 01

</div>


<h3>

Telegram Gaming Bot

</h3>


<p>

An interactive Telegram game featuring player
profiles, collectible cards, deck building,
matchmaking, battles and leaderboards.

</p>


<div class="project-tech">

<span>Python</span>

<span>Telegram API</span>

<span>SQLite</span>

<span>Game Logic</span>

</div>


</div>


</article>



<!-- PROJECT 2 -->

<article class="project reveal">


<div class="project-image">

<img
src="https://images.unsplash.com/photo-1555066931-4365d14bab8c?auto=format&fit=crop&w=1200&q=80"
alt="Bot Development">

</div>


<div class="project-content">


<div class="project-index">

PROJECT / 02

</div>


<h3>

Wuthering Waves Bot

</h3>


<p>

A fan-made Telegram gaming experience inspired
by Wuthering Waves with character collections,
weapons, gacha pulls and player progression.

</p>


<div class="project-tech">

<span>Python</span>

<span>Telegram</span>

<span>Database</span>

<span>Game Systems</span>

</div>


</div>


</article>



<!-- PROJECT 3 -->

<article class="project reveal">


<div class="project-image">

<img
src="https://images.unsplash.com/photo-1461749280684-dccba630e2f6?auto=format&fit=crop&w=1200&q=80"
alt="Portfolio Website">

</div>


<div class="project-content">


<div class="project-index">

PROJECT / 03

</div>


<h3>

AboutGarvit

</h3>


<p>

My personal corner of the internet where
I showcase my projects, interests,
development journey and ways to connect.

</p>


<div class="project-tech">

<span>HTML</span>

<span>CSS</span>

<span>JavaScript</span>

<span>Responsive Design</span>

</div>


</div>


</article>


</div>

</div>

</section>



<!-- ==================================================
PERSONAL
================================================== -->

<section class="section" id="personal">

<div class="container">


<div class="section-header reveal">


<div>

<span class="section-label">
04 / Beyond Code
</span>

</div>


<div>

<h2 class="section-title">

More than
just coding.

</h2>


<p class="section-description">

Some of the things that keep life interesting
outside programming.

</p>

</div>


</div>



<div class="personal-grid">


<div class="personal-card reveal">


<div class="personal-icon">
🎮
</div>


<h3>
Gaming
</h3>


<p>

I enjoy games including Wuthering Waves,
Genshin Impact and other story-driven
and open-world experiences.

</p>


</div>



<div class="personal-card reveal">


<div class="personal-icon">
🎌
</div>


<h3>
Anime
</h3>


<p>

One Piece, Bleach, Vinland Saga,
Dr. Stone and many more.

</p>


</div>



<div class="personal-card reveal">


<div class="personal-icon">
⚽
</div>


<h3>
Sports
</h3>


<p>

Football, badminton and table tennis.
Cristiano Ronaldo is my favourite footballer.

</p>


</div>



<div class="personal-card personal-big reveal">


<div class="personal-icon">
✦
</div>


<div class="quote">

"It's not about whether I can or not.
I'm gonna do it because I want to."

</div>


<p style="margin-top:25px">

— Monkey D. Luffy

</p>


</div>



<div class="personal-card reveal">


<div class="personal-icon">
📚
</div>


<h3>
Learning
</h3>


<p>

I enjoy continuously learning about
technology, programming, computer science
and building new things.

</p>


</div>


</div>

</div>

</section>



<!-- ==================================================
CONTACT
================================================== -->

<section class="section" id="contact">

<div class="container">


<div class="contact-wrapper reveal">


<div class="contact-top">


<h2>

LET'S
CONNECT.

</h2>


<p class="contact-text">

Want to discuss development, collaborate
on something, talk about a project or
simply connect? You can find me through
the platforms below.

</p>


</div>



<div class="contact-list">


<div class="contact-item">

<small>
EMAIL
</small>

<a href="mailto:garvit999999@gmail.com">

garvit999999@gmail.com

</a>

</div>



<div class="contact-item">

<small>
LOCATION
</small>

<span>

Meerut, Uttar Pradesh

</span>

</div>



<div class="contact-item">

<small>
TELEGRAM
</small>

<a
href="https://t.me/Garvit_Sharma"
target="_blank">

@Garvit_Sharma

</a>

</div>



<div class="contact-item">

<small>
GITHUB
</small>

<a
href="https://github.com/AboutGarvit"
target="_blank">

github.com/AboutGarvit

</a>

</div>


</div>


</div>

</div>

</section>



<!-- ==================================================
FOOTER
================================================== -->

<footer>

<div class="container">

<div class="footer-content">


<p>

© <span id="year"></span> Garvit Sharma

</p>


<p>

Designed & Built by Garvit.

</p>


</div>

</div>

</footer>



<!-- ==================================================
JAVASCRIPT
================================================== -->

<script>


/* =====================================================
CURRENT YEAR
===================================================== */

document.getElementById("year").textContent =
new Date().getFullYear();



/* =====================================================
SCROLL REVEAL
===================================================== */

const revealElements =
document.querySelectorAll(".reveal");


const observer =
new IntersectionObserver(

(entries) => {

entries.forEach((entry) => {

if(entry.isIntersecting){

entry.target.classList.add("active");

observer.unobserve(entry.target);

}

});

},

{

threshold: 0.12

}

);


revealElements.forEach((element) => {

observer.observe(element);

});



/* =====================================================
MOBILE MENU
===================================================== */

const menuButton =
document.getElementById("menuButton");


menuButton.addEventListener(
"click",
() => {

const navLinks =
document.querySelector(".nav-links");


const navButton =
document.querySelector(".nav-button");


if(
navLinks.style.display === "flex"
){

navLinks.style.display = "";

navButton.style.display = "";

menuButton.textContent = "☰";

}

else {

navLinks.style.display = "flex";

navLinks.style.position = "absolute";

navLinks.style.top = "75px";

navLinks.style.left = "0";

navLinks.style.right = "0";

navLinks.style.flexDirection = "column";

navLinks.style.gap = "0";

navLinks.style.padding = "20px";

navLinks.style.background =
"rgba(12,13,17,.98)";

navLinks.style.border =
"1px solid rgba(255,255,255,.1)";

navLinks.style.borderRadius =
"22px";


navLinks
.querySelectorAll("a")
.forEach((link) => {

link.style.padding =
"14px";

});


menuButton.textContent = "✕";

}

});



/* =====================================================
CLOSE MOBILE MENU AFTER CLICK
===================================================== */

document
.querySelectorAll(".nav-links a")
.forEach((link) => {

link.addEventListener(
"click",
() => {

if(window.innerWidth <= 900){

document.querySelector(
".nav-links"
).style.display = "";

menuButton.textContent = "☰";

}

});

});



/* =====================================================
SUBTLE PROFILE PARALLAX
===================================================== */

const profileCard =
document.querySelector(".profile-card");


if(
window.matchMedia(
"(pointer: fine)"
).matches
){

document.addEventListener(
"mousemove",
(event) => {

const x =
(
event.clientX /
window.innerWidth
-
0.5
)
*
5;


const y =
(
event.clientY /
window.innerHeight
-
0.5
)
*
5;


profileCard.style.transform =
`
rotate(2deg)
translate(
${x}px,
${y}px
)
`;

});

}


</script>


</body>

</html>
