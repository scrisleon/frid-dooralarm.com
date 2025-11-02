<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fridge Door Alarm</title>
    <style>
        /* === Global Styles === */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        body {
            background-color: #f5faff;
            color: #222;
            line-height: 1.6;
        }

        /* === Header === */
        header {
            background-color: #0077cc;
            color: #fff;
            padding: 10px 10%;
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
        }

        .logo-container {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo-container img {
            width: 45px;
            height: 45px;
            object-fit: contain;
        }

        .logo-container h1 {
            font-size: 1.5em;
            font-weight: 600;
        }

        nav a {
            color: #fff;
            margin-left: 20px;
            text-decoration: none;
            font-weight: 500;
            transition: 0.3s;
        }

        nav a:hover {
            color: #ffdd55;
        }

        /* === Hero Section === */
        .hero {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            padding: 80px 10%;
            background: linear-gradient(to bottom right, #cbe9ff, #e6f7ff);
        }

        .hero h2 {
            font-size: 2.5em;
            margin-bottom: 20px;
            color: #004b80;
        }

        .hero p {
            max-width: 600px;
            font-size: 1.1em;
            margin-bottom: 30px;
            color: #333;
        }

        .btn {
            display: inline-block;
            background-color: #0077cc;
            color: white;
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            transition: background-color 0.3s;
        }

        .btn:hover {
            background-color: #005fa3;
        }

        /* === Features Section === */
        .features {
            padding: 80px 10%;
            background-color: #ffffff;
            text-align: center;
        }

        .features h2 {
            font-size: 2em;
            color: #004b80;
            margin-bottom: 40px;
        }

        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .feature-box {
            background: white;
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .feature-box:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 12px rgba(0,0,0,0.15);
        }

        .feature-box h3 {
            color: #0077cc;
            margin-bottom: 15px;
            font-size: 1.3em;
        }

        .feature-box p {
            color: #555;
            font-size: 1em;
        }

        /* === Easy Setup Guide === */
        .setup-guide {
            background-color: #e8f4ff;
            padding: 80px 10%;
            text-align: center;
        }

        .setup-guide h2 {
            color: #004b80;
            font-size: 2em;
            margin-bottom: 40px;
        }

        .steps {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            justify-content: center;
            align-items: stretch;
        }

        .step {
            background: white;
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .step:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 12px rgba(0,0,0,0.15);
        }

        .step-number {
            background-color: #0077cc;
            color: white;
            font-size: 1.3em;
            width: 45px;
            height: 45px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 15px;
        }

        .step h3 {
            color: #0077cc;
            margin-bottom: 10px;
        }

        .step p {
            color: #444;
            font-size: 1em;
        }

        /* === Footer === */
        footer {
            background-color: #0077cc;
            color: white;
            padding: 50px 10% 30px;
            margin-top: 60px;
        }

        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 30px;
        }

        .footer-column h3 {
            margin-bottom: 15px;
            font-size: 1.2em;
            border-left: 4px solid #ffdd55;
            padding-left: 8px;
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 10px;
        }

        .footer-column ul li a {
            color: #fff;
            text-decoration: none;
            transition: 0.3s;
        }

        .footer-column ul li a:hover {
            color: #ffdd55;
        }

        .footer-column p {
            margin-bottom: 8px;
        }

        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 10px;
        }

        .social-icons a {
            display: inline-flex;
            width: 35px;
            height: 35px;
            background-color: white;
            color: #0077cc;
            border-radius: 50%;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            font-size: 18px;
            font-weight: bold;
            transition: all 0.3s ease;
        }

        .social-icons a:hover {
            background-color: #ffdd55;
            color: #004b80;
        }

        .footer-bottom {
            text-align: center;
            border-top: 1px solid rgba(255,255,255,0.3);
            margin-top: 30px;
            padding-top: 20px;
            font-size: 0.9em;
        }

        @media (max-width: 600px) {
            header {
                flex-direction: column;
                text-align: center;
            }
            nav {
                margin-top: 10px;
            }
            .hero h2 {
                font-size: 2em;
            }
        }
        /* === New Setup Timeline Layout === */
.setup-guide {
    background: linear-gradient(to bottom, #e6f7ff, #ffffff);
    padding: 80px 10%;
    text-align: center;
}

.setup-guide h2 {
    color: #004b80;
    font-size: 2.2em;
    margin-bottom: 60px;
    position: relative;
}

.setup-timeline {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    position: relative;
}

.timeline-step {
    background: white;
    border-radius: 12px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    padding: 25px;
    width: 220px;
    text-align: center;
    position: relative;
    transition: transform 0.3s, box-shadow 0.3s;
}

.timeline-step:hover {
    transform: translateY(-5px);
    box-shadow: 0 6px 14px rgba(0,0,0,0.15);
}

.icon {
    font-size: 2em;
    background-color: #0077cc;
    color: white;
    width: 60px;
    height: 60px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 15px;
}

.timeline-line {
    flex-grow: 1;
    height: 3px;
    background-color: #0077cc;
    margin: 0 15px;
    border-radius: 2px;
}

.timeline-step h3 {
    color: #0077cc;
    font-size: 1.2em;
    margin-bottom: 8px;
}

.timeline-step p {
    color: #444;
    font-size: 0.95em;
}

/* Responsive Timeline */
@media (max-width: 800px) {
    .setup-timeline {
        flex-direction: column;
        gap: 25px;
    }
    .timeline-line {
        width: 3px;
        height: 40px;
        margin: 0 auto;
    }
}
/* === Meet the Developers Section === */
.developers {
    background-color: #f5faff;
    padding: 80px 10%;
    text-align: center;
}

.developers h2 {
    color: #004b80;
    font-size: 2em;
    margin-bottom: 15px;
}

.developers .intro-text {
    color: #444;
    font-size: 1.1em;
    max-width: 600px;
    margin: 0 auto 50px;
}

.team-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 40px;
    justify-content: center;
    align-items: stretch;
}

.team-member {
    background: white;
    border-radius: 12px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    padding: 30px;
    transition: transform 0.3s, box-shadow 0.3s;
}

.team-member:hover {
    transform: translateY(-6px);
    box-shadow: 0 8px 16px rgba(0,0,0,0.15);
}

.team-member img {
    width: 120px;
    height: 120px;
    border-radius: 50%;
    object-fit: cover;
    margin-bottom: 15px;
    border: 3px solid #0077cc;
}

.team-member h3 {
    color: #0077cc;
    margin-bottom: 5px;
    font-size: 1.3em;
}

.team-member .role {
    font-weight: bold;
    color: #ffbb33;
    margin-bottom: 12px;
}

.team-member .bio {
    color: #555;
    font-size: 0.95em;
    line-height: 1.5;
}

/* Responsive adjustments */
@media (max-width: 600px) {
    .developers h2 {
        font-size: 1.7em;
    }
    .team-member img {
        width: 100px;
        height: 100px;
    }
}


    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <div class="logo-container">
            <img src="chill guard.jpg" alt="Fridge Door Alarm Logo">
            <h1>Fridge Door Alarm</h1>
        </div>
        <nav>
            <a href="#features">Features</a>
            <a href="#setup">Setup</a>
            <a href="#contact">Contact</a>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <h2>Never Leave Your Fridge Door Open Again!</h2>
        <p>Introducing the <strong></strong> — a small, smart device that alerts you when your fridge door is left open, helping you save energy and keep your food fresh.</p>
        <a href="#buy" class="btn">Order Now</a>
    </section>

    <!-- Features Section -->
    <section id="features" class="features">
        <h2>Our Amazing Features</h2>
        <div class="feature-grid">
            <div class="feature-box">
                <h3>🔔 Instant Alerts</h3>
                <p>Get notified the moment your fridge door stays open too long.</p>
            </div>
            <div class="feature-box">
                <h3>🧠 Smart Sensor</h3>
                <p>Automatically detects temperature and door position with precision.</p>
            </div>
            <div class="feature-box">
                <h3>🔋 Long Battery Life</h3>
                <p>Energy-efficient design means months of use on a single charge.</p>
            </div>
            <div class="feature-box">
                <h3>📱 Easy Setup</h3>
                <p>Attach and forget — no complicated installation required.</p>
            </div>
        </div>
    </section>
<!-- Easy Setup Guide (New Layout) -->
<section id="setup" class="setup-guide">
    <h2>Easy Setup Guide</h2>
    <div class="setup-timeline">
        <div class="timeline-step">
            <div class="icon">📦</div>
            <div class="text">
                <h3>Step 1: Unbox the Device</h3>
                <p>Open the package and make sure all items are included — device, adhesive pad, and battery.</p>
            </div>
        </div>
        <div class="timeline-line"></div>
        <div class="timeline-step">
            <div class="icon">🧲</div>
            <div class="text">
                <h3>Step 2: Attach to Your Fridge</h3>
                <p>Peel the adhesive pad and place the device near the fridge door edge.</p>
            </div>
        </div>
        <div class="timeline-line"></div>
        <div class="timeline-step">
            <div class="icon">⚡</div>
            <div class="text">
                <h3>Step 3: Power On</h3>
                <p>Insert the battery and turn on the switch — a small light confirms activation.</p>
            </div>
        </div>
        <div class="timeline-line"></div>
        <div class="timeline-step">
            <div class="icon">✅</div>
            <div class="text">
                <h3>Step 4: Test & Enjoy</h3>
                <p>Open your fridge door and wait a few seconds — the alarm will alert you perfectly!</p>
            </div>
        </div>
    </div>
</section>
<!-- Meet the Developers Section -->
<section class="developers">
    <h2>Meet the Developers</h2>
    <p class="intro-text">Every great product has a great team behind it. Meet the creative minds who built the  Fridge Door Alarm!</p>

    <div class="team-grid">
        <!-- The Hacker -->
        <div class="team-member">
            <img src="data:image/jpeg;base64,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" alt="The Hacker - Tech Genius">
            <h3>Patrick Villa</h3>
            <p class="role">💻 The Hacker</p>
            <p class="bio">The coding wizard who engineered the brains of the Fridge Door Alarm — ensuring smooth performance, reliable sensors, and smart connectivity.</p>
        </div>

        <!-- The Hipster -->
        <div class="team-member">
            <img src="https://scontent.fmnl13-3.fna.fbcdn.net/v/t1.15752-9/569158873_1537442484068332_6653759067538372145_n.jpg?stp=dst-jpg_s640x640_tt6&_nc_cat=102&ccb=1-7&_nc_sid=0024fc&_nc_eui2=AeExkKq0_QitIyDuWjKxFKeVc4AphwwchG9zgCmHDByEbz8DiygX9VCYHE_BOOigeprRtkDRuBShxxoirYdoTcro&_nc_ohc=7RLKnTthK9UQ7kNvwG7PczE&_nc_oc=Adldz2OJHbH8-DInsxxSGBZcnQXThas_v_uVpL5QIhrHdX38hjxzX6JnfE8MVDTsBD60ZUik49IqVwb6EJmDwW0J&_nc_ad=z-m&_nc_cid=0&_nc_zt=23&_nc_ht=scontent.fmnl13-3.fna&oh=03_Q7cD3wGLJ7Oy0e7YUNdhMWtAO9OV3EMew911UmsZ8-v4BX-I3g&oe=692E5439" alt="The Hipster - Design Visionary">
            <h3>Cyril Pacamaman</h3>
            <p class="role">🎨 The Hipster</p>
            <p class="bio">The creative force behind the clean design and friendly interface — making technology look beautiful and easy to use.</p>
        </div>

        <!-- The Hustler -->
        <div class="team-member">
            <img src="https://scontent.fcgy1-1.fna.fbcdn.net/v/t1.15752-9/566642775_1753828202672430_5272758324512813635_n.jpg?stp=dst-jpg_s480x480_tt6&_nc_cat=105&ccb=1-7&_nc_sid=0024fc&_nc_eui2=AeEiPEsmL1NRjOym8goI0afg9mWtv5r1reD2Za2_mvWt4CqA9DukrGZZTlHiIoSvliD8Nk2ASoXo63v5RxyICKYV&_nc_ohc=1Zfb1X5rCE0Q7kNvwE55lBu&_nc_oc=AdlvKVj26k6wFOEGws4sXqL4IRbtxSuYJvLI_5o7ehfjXpZT54Mc_mfphMX9pXxmoir8MexXkrW0egq9xNuUWjBF&_nc_ad=z-m&_nc_cid=0&_nc_zt=23&_nc_ht=scontent.fcgy1-1.fna&oh=03_Q7cD3wG1O0nfAkA6mP9RaC_4NwJgEWifsOOVAiPfJ5tLCMAlZg&oe=692E6387" alt="The Hustler - Marketing Strategist">
            <h3>Crisleon Santillan</h3>
            <p class="role">💼 The Hustler</p>
            <p class="bio">The energetic go-getter who brings the Fridge Door Alarm to homes worldwide through innovation, storytelling, and strategy.</p>
        </div>
    </div>
</section>
<!-- Product Information Section -->
<section id="product-info" style="padding:80px 10%; background-color:#ffffff; text-align:center;">
    <h2 style="font-size:2em; color:#004b80; margin-bottom:40px; border-bottom:3px solid #ffdd55; display:inline-block; padding-bottom:5px;">Product Information</h2>

    <div style="display:flex; flex-wrap:wrap; justify-content:center; gap:30px; margin-top:40px;">
        <!-- Technical Specifications -->
        <div style="flex:1; min-width:300px; background-color:#fff8e1; border-radius:10px; padding:25px; box-shadow:0 4px 10px rgba(0,0,0,0.1); text-align:left;">
            <h3 style="font-size:1.5em; color:#444; margin-bottom:20px;">💡 Technical Specifications</h3>
            <hr style="border:none; border-top:2px solid #ffdd55; margin-bottom:20px;">
            <p style="margin-bottom:12px; font-weight:bold;">✅ Solar Panel: <span style="font-weight:normal;">5V 1W Polycrystalline</span></p>
            <p style="margin-bottom:12px; font-weight:bold;">✅ Battery: <span style="font-weight:normal;">3.7V 2000mAh Li-ion</span></p>
            <p style="margin-bottom:12px; font-weight:bold;">✅ PIR Range: <span style="font-weight:normal;">Up to 5 meters</span></p>
            <p style="margin-bottom:12px; font-weight:bold;">✅ Controller: <span style="font-weight:normal;">Arduino Uno</span></p>
        </div>

        <!-- Environmental Benefits -->
        <div style="flex:1; min-width:300px; background-color:#f9fff5; border-radius:10px; padding:25px; box-shadow:0 4px 10px rgba(0,0,0,0.1); text-align:left;">
            <h3 style="font-size:1.5em; color:#444; margin-bottom:20px;">🌱 Environmental Benefits</h3>
            <hr style="border:none; border-top:2px solid #9ccc65; margin-bottom:20px;">
            <p style="margin-bottom:12px;">❄️ Prevents Food Spoilage</p>
            <p style="margin-bottom:12px;">💡 Save's energy</p>
            <p style="margin-bottom:12px;">💰 Cuts Electricity Costs</p>
            <p style="margin-bottom:12px;">🔔 Smart Alerts</p>
            <p style="margin-bottom:12px;">🧠 Smart Automation</p>
        </div>
    </div>
</section>
    <section id="faq" style="padding:80px 10%; background-color:#ffffff; text-align:center; font-family:Arial, sans-serif;">
    <div class="container" style="max-width:900px; margin:0 auto;">
        <div class="section-title-container text-center" style="margin-bottom:40px;">
            <h2 style="font-size:2em; color:#004b80; margin-bottom:10px;">Frequently Asked Questions</h2>
            <p style="color:#666; font-size:1.1em;">Everything you need to know about our Fridge Door Alarm</p>
        </div>

        <div class="accordion" id="faqAccordion" style="text-align:left;">
            <!-- Question 1 -->
            <div class="accordion-item" style="border:0; margin-bottom:1rem; box-shadow: 0 2px 4px rgba(0,0,0,0.1); border-radius:5px;">
                <h2 class="accordion-header" id="headingOne" style="margin:0;">
                    <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne"
                        aria-expanded="true" aria-controls="collapseOne"
                        style="width:100%; background-color:#0077cc; color:#222; font-weight:bold; font-size:1.1em; padding:1rem; border:none; border-radius:5px 5px 0 0; text-align:left; cursor:pointer; outline:none;">
                        How does the automatic closing system work?
                    </button>
                </h2>
                <div id="collapseOne" class="accordion-collapse collapse show" aria-labelledby="headingOne" data-bs-parent="#faqAccordion" style="padding:1rem; background-color:#fff; border-top:none; border-radius:0 0 5px 5px;">
                    <div class="accordion-body" style="color:#555; font-size:1em; line-height:1.5;">
                        The Fridge Door Alarm uses a smart sensor to detect when the door is left open for too long.
                        After a short delay, a motorized arm gently closes the door, keeping your food fresh and conserving energy.
                    </div>
                </div>
            </div>

            <!-- Question 2 -->
            <div class="accordion-item" style="border:0; margin-bottom:1rem; box-shadow: 0 2px 4px rgba(0,0,0,0.1); border-radius:5px;">
                <h2 class="accordion-header" id="headingTwo" style="margin:0;">
                    <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseTwo"
                        aria-expanded="false" aria-controls="collapseTwo"
                        style="width:100%; background-color:#ffffff; background-color:#0077cc; color:#222; font-weight:bold; font-size:1.1em; padding:1rem; border:none; border-radius:5px; text-align:left; cursor:pointer; outline:none;">
                        Does it alert before closing automatically?
                    </button>
                </h2>
                <div id="collapseTwo" class="accordion-collapse collapse" aria-labelledby="headingTwo" data-bs-parent="#faqAccordion" style="padding:1rem; background-color:#fff; border-radius:5px;">
                    <div class="accordion-body" style="color:#555; font-size:1em; line-height:1.5;">
                        Yes. The alarm will beep a few times before closing, giving you time to safely close it yourself or remove your hand.
                    </div>
                </div>
            </div>

            <!-- Question 3 -->
            <div class="accordion-item" style="border:0; margin-bottom:1rem; box-shadow: 0 2px 4px rgba(0,0,0,0.1); border-radius:5px;">
                <h2 class="accordion-header" id="headingThree" style="margin:0;">
                    <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseThree"
                        aria-expanded="false" aria-controls="collapseThree"
                        style="width:100%; background-color:#ffffff; background-color:#0077cc;  color:#222; font-weight:bold; font-size:1.1em; padding:1rem; border:none; border-radius:5px; text-align:left; cursor:pointer; outline:none;">
                        Can it be installed on any fridge model?
                    </button>
                </h2>
                <div id="collapseThree" class="accordion-collapse collapse" aria-labelledby="headingThree" data-bs-parent="#faqAccordion" style="padding:1rem; background-color:#fff; border-radius:5px;">
                    <div class="accordion-body" style="color:#555; font-size:1em; line-height:1.5;">
                        The device is designed to fit most standard refrigerator doors and can be easily attached using the included adhesive mount.
                    </div>
                </div>
            </div>

            <!-- Question 4 -->
            <div class="accordion-item" style="border:0; margin-bottom:1rem; box-shadow: 0 2px 4px rgba(0,0,0,0.1); border-radius:5px;">
                <h2 class="accordion-header" id="headingFour" style="margin:0;">
                    <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseFour"
                        aria-expanded="false" aria-controls="collapseFour"
                        style="width:100%; background-color:#ffffff;  background-color:#0077cc; color:#222; font-weight:bold; font-size:1.1em; padding:1rem; border:none; border-radius:5px; text-align:left; cursor:pointer; outline:none;">
                        How long does the battery last?
                    </button>
                </h2>
                <div id="collapseFour" class="accordion-collapse collapse" aria-labelledby="headingFour" data-bs-parent="#faqAccordion" style="padding:1rem; background-color:#fff; border-radius:5px;">
                    <div class="accordion-body" style="color:#555; font-size:1em; line-height:1.5;">
                        On a full charge, the battery can last up to two weeks with normal daily use.
                    </div>
                </div>
            </div>

            <!-- Question 5 -->
            <div class="accordion-item" style="border:0; margin-bottom:1rem; box-shadow: 0 2px 4px rgba(0,0,0,0.1); border-radius:5px;">
                <h2 class="accordion-header" id="headingFive" style="margin:0;">
                    <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseFive"
                        aria-expanded="false" aria-controls="collapseFive"
                        style="width:100%; background-color:#ffffff;  background-color:#0077cc; color:#222; font-weight:bold; font-size:1.1em; padding:1rem; border:none; border-radius:5px; text-align:left; cursor:pointer; outline:none;">
                        Is it safe for kids and pets?
                    </button>
                </h2>
                <div id="collapseFive" class="accordion-collapse collapse" aria-labelledby="headingFive" data-bs-parent="#faqAccordion" style="padding:1rem; background-color:#fff; border-radius:5px;">
                    <div class="accordion-body" style="color:#555; font-size:1em; line-height:1.5;">
                        Absolutely. The auto-close mechanism is gentle and includes safety sensors to prevent accidents or injuries.
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

  

    <!-- Footer -->
    <footer id="contact">
        <div class="footer-container">
            <div class="footer-column">
                <h3>Contact Us</h3>
                <p>📧 Email: <a href="mailto:support@smartfridgealarm.com" style="color:white; text-decoration:underline;">support@smartfridgealarm.com</a></p>
                <p>📞 Phone: <a href="tel:+1234567890" style="color:white; text-decoration:underline;">+1 234 567 890</a></p>
                <p>📍 Location: 123 CoolTech Avenue, New York, USA</p>
            </div>

            <div class="footer-column">
                <h3>Quick Links</h3>
                <ul>
                    <li><a href="#features">Features</a></li>
                    <li><a href="#setup">Setup Guide</a></li>
                    <li><a href="#contact">Contact</a></li>
                    <li><a href="#">Privacy Policy</a></li>
                </ul>
            </div>

            <div class="footer-column">
                <h3>Follow Us</h3>
                <p>Stay connected for updates and news:</p>
                <div class="social-icons">
                    <a href="https://facebook.com" target="_blank" title="Facebook">f</a>
                    <a href="https://tiktok.com" target="_blank" title="TikTok">🎵</a>
                    <a href="mailto:support@smartfridgealarm.com" title="Gmail">G</a>
                </div>
            </div>
        </div>

        <div class="footer-bottom">
            <p>Fridge Door Alarm | All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
