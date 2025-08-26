
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MusicMantra - Professional Digital Music Studio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #1a1a2e;
            --secondary: #16213e;
            --accent: #e94560;
            --light: #f5f5f5;
            --dark: #0f3460;
            --success: #4caf50;
            --warning: #ff9800;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--primary);
            color: var(--light);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--secondary), var(--dark));
            padding: 15px 0;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo img {
            height: 50px;
            border-radius: 50%;
            border: 2px solid var(--accent);
        }

        .logo h1 {
            font-size: 28px;
            font-weight: 700;
            background: linear-gradient(45deg, var(--accent), #ff6b6b);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 30px;
        }

        nav a {
            color: var(--light);
            text-decoration: none;
            font-weight: 500;
            font-size: 16px;
            transition: all 0.3s ease;
            position: relative;
        }

        nav a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--accent);
            transition: width 0.3s ease;
        }

        nav a:hover::after {
            width: 100%;
        }

        .mobile-menu {
            display: none;
            font-size: 24px;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 0 20px;
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1470225620780-dba8ba36b745?ixlib=rb-4.0.3&auto=format&fit=crop&w=1950&q=80') no-repeat center center/cover;
            position: relative;
        }

        .hero-content {
            max-width: 800px;
        }

        .hero h2 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            background: linear-gradient(45deg, var(--accent), #ff6b6b);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            color: #ddd;
        }

        .hero-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }

        .social-link {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background: rgba(255, 255, 255, 0.1);
            padding: 12px 25px;
            border-radius: 30px;
            color: var(--light);
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }

        .social-link:hover {
            background: var(--accent);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(233, 69, 96, 0.3);
        }

        .social-link.youtube:hover {
            background: #FF0000;
        }

        .social-link.discord:hover {
            background: #5865F2;
        }

        .btn {
            display: inline-block;
            background: var(--accent);
            color: white;
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            font-size: 16px;
            margin: 5px;
        }

        .btn:hover {
            background: #ff6b6b;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(233, 69, 96, 0.3);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--accent);
            color: var(--accent);
        }

        .btn-outline:hover {
            background: var(--accent);
            color: white;
        }

        /* Section Styles */
        section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title h2 {
            font-size: 2.5rem;
            margin-bottom: 15px;
            position: relative;
            display: inline-block;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--accent);
            border-radius: 2px;
        }

        .section-title p {
            color: #aaa;
            max-width: 700px;
            margin: 0 auto;
        }

        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .about-text h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--accent);
        }

        .about-text p {
            margin-bottom: 20px;
            color: #ddd;
        }

        .about-image {
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.4);
        }

        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }

        /* Services Section */
        .services {
            background: var(--secondary);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .service-card {
            background: var(--primary);
            border-radius: 10px;
            padding: 30px;
            text-align: center;
            transition: all 0.3s ease;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
        }

        .service-card i {
            font-size: 3rem;
            color: var(--accent);
            margin-bottom: 20px;
        }

        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
        }

        .service-card p {
            color: #aaa;
        }

        /* Music Player Section */
        .music-player {
            background: var(--dark);
        }

        .player-container {
            background: var(--secondary);
            border-radius: 15px;
            padding: 40px;
            margin-top: 50px;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
        }

        .player-header {
            text-align: center;
            margin-bottom: 30px;
        }

        .player-header h3 {
            font-size: 1.8rem;
            color: var(--accent);
            margin-bottom: 10px;
        }

        /* Virtual Instruments */
        .instruments {
            margin-top: 40px;
        }

        .instruments-tabs {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-bottom: 30px;
        }

        .tab {
            background: var(--primary);
            border: none;
            color: var(--light);
            padding: 10px 20px;
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 600;
        }

        .tab.active {
            background: var(--accent);
            color: white;
        }

        .instrument-panel {
            background: var(--primary);
            border-radius: 10px;
            padding: 30px;
            min-height: 300px;
        }

        /* Piano Styles */
        .piano {
            display: flex;
            justify-content: center;
            margin-top: 20px;
        }

        .key {
            width: 40px;
            height: 150px;
            background: white;
            border: 1px solid #ccc;
            border-radius: 0 0 5px 5px;
            margin: 0 2px;
            cursor: pointer;
            position: relative;
            transition: all 0.1s ease;
        }

        .key.black {
            background: black;
            height: 100px;
            width: 30px;
            margin: 0 -15px;
            z-index: 2;
            border-radius: 0 0 3px 3px;
        }

        .key:active, .key.active {
            background: var(--accent);
            transform: translateY(2px);
        }

        /* Drum Styles */
        .drums {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .drum-pad {
            aspect-ratio: 1;
            background: var(--dark);
            border: 2px solid var(--accent);
            border-radius: 50%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.2s ease;
            font-weight: bold;
        }

        .drum-pad:hover {
            transform: scale(1.05);
            box-shadow: 0 5px 15px rgba(233, 69, 96, 0.3);
        }

        .drum-pad:active, .drum-pad.active {
            background: var(--accent);
            transform: scale(0.95);
        }

        .drum-pad i {
            font-size: 2rem;
            margin-bottom: 10px;
        }

        /* Guitar Styles */
        .guitar {
            margin-top: 30px;
        }

        .guitar-fretboard {
            background: #8B4513;
            border-radius: 10px;
            padding: 20px;
            box-shadow: inset 0 0 10px rgba(0, 0, 0, 0.5);
        }

        .guitar-string {
            height: 8px;
            background: linear-gradient(90deg, #ddd, #fff, #ddd);
            margin: 15px 0;
            border-radius: 4px;
            position: relative;
            cursor: pointer;
        }

        .guitar-string::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(233, 69, 96, 0);
            transition: background 0.2s ease;
            border-radius: 4px;
        }

        .guitar-string:active::before, .guitar-string.active::before {
            background: rgba(233, 69, 96, 0.5);
        }

        .guitar-frets {
            display: flex;
            justify-content: space-between;
            margin-top: 10px;
        }

        .guitar-fret {
            width: 60px;
            height: 150px;
            background: rgba(255, 255, 255, 0.1);
            border-left: 2px solid rgba(255, 255, 255, 0.3);
            position: relative;
            cursor: pointer;
        }

        .guitar-fret:last-child {
            border-right: 2px solid rgba(255, 255, 255, 0.3);
        }

        .guitar-fret:active, .guitar-fret.active {
            background: rgba(233, 69, 96, 0.3);
        }

        .guitar-controls {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }

        .guitar-btn {
            background: var(--dark);
            border: 2px solid var(--accent);
            color: var(--accent);
            padding: 8px 16px;
            border-radius: 20px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .guitar-btn:hover, .guitar-btn.active {
            background: var(--accent);
            color: white;
        }

        /* Synthesizer Styles */
        .synthesizer {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 20px;
        }

        .synth-keyboard {
            display: flex;
            justify-content: center;
            margin-top: 20px;
        }

        .synth-key {
            width: 40px;
            height: 120px;
            background: linear-gradient(to bottom, #444, #222);
            border: 1px solid #111;
            border-radius: 0 0 5px 5px;
            margin: 0 2px;
            cursor: pointer;
            position: relative;
            transition: all 0.1s ease;
            display: flex;
            align-items: flex-end;
            justify-content: center;
            padding-bottom: 10px;
            font-size: 12px;
            color: #aaa;
        }

        .synth-key.black {
            background: linear-gradient(to bottom, #222, #000);
            height: 80px;
            width: 30px;
            margin: 0 -15px;
            z-index: 2;
            border-radius: 0 0 3px 3px;
            color: #fff;
        }

        .synth-key:active, .synth-key.active {
            background: var(--accent);
            transform: translateY(2px);
            box-shadow: 0 0 10px rgba(233, 69, 96, 0.7);
        }

        .synth-controls {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
            width: 100%;
        }

        .synth-control {
            background: var(--dark);
            border-radius: 10px;
            padding: 15px;
            width: 200px;
        }

        .synth-control h4 {
            margin-bottom: 10px;
            color: var(--accent);
        }

        .synth-slider {
            width: 100%;
            margin: 10px 0;
        }

        .synth-waveform {
            display: flex;
            justify-content: space-between;
            margin-top: 10px;
        }

        .waveform-btn {
            background: var(--primary);
            border: 1px solid var(--accent);
            color: var(--accent);
            padding: 5px 10px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 12px;
            transition: all 0.2s ease;
        }

        .waveform-btn:hover, .waveform-btn.active {
            background: var(--accent);
            color: white;
        }

        /* Contact Section */
        .contact-form {
            max-width: 700px;
            margin: 0 auto;
            background: var(--secondary);
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }

        .form-group {
            margin-bottom: 25px;
        }

        .form-group label {
            display: block;
            margin-bottom: 10px;
            font-weight: 600;
            color: var(--accent);
        }

        .form-control {
            width: 100%;
            padding: 15px;
            background: var(--primary);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 5px;
            color: var(--light);
            font-size: 16px;
        }

        .form-control:focus {
            outline: none;
            border-color: var(--accent);
            box-shadow: 0 0 0 2px rgba(233, 69, 96, 0.2);
        }

        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }

        .contact-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }

        .info-card {
            background: var(--primary);
            border-radius: 10px;
            padding: 30px;
            text-align: center;
            transition: all 0.3s ease;
        }

        .info-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }

        .info-card i {
            font-size: 2.5rem;
            color: var(--accent);
            margin-bottom: 15px;
        }

        .info-card h3 {
            font-size: 1.3rem;
            margin-bottom: 10px;
        }

        /* Footer */
        footer {
            background: var(--dark);
            padding: 60px 0 20px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-column h3 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: var(--accent);
        }

        .footer-column p {
            color: #aaa;
            margin-bottom: 15px;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 10px;
        }

        .footer-links a {
            color: #aaa;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-links a:hover {
            color: var(--accent);
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: var(--primary);
            border-radius: 50%;
            color: var(--light);
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            background: var(--accent);
            transform: translateY(-3px);
        }

        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #aaa;
            font-size: 14px;
        }

        /* Responsive Styles */
        @media (max-width: 992px) {
            .about-content {
                grid-template-columns: 1fr;
            }
            
            .hero h2 {
                font-size: 2.8rem;
            }
        }

        @media (max-width: 768px) {
            nav ul {
                display: none;
            }
            
            .mobile-menu {
                display: block;
            }
            
            .hero h2 {
                font-size: 2.2rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
            
            .player-container {
                padding: 25px;
            }
            
            .hero-links {
                flex-direction: column;
                align-items: center;
            }
            
            .drums {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .synth-controls {
                flex-direction: column;
                align-items: center;
            }
        }

        @media (max-width: 576px) {
            .hero h2 {
                font-size: 1.8rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .btn {
                padding: 10px 20px;
                font-size: 14px;
            }
            
            .key, .synth-key {
                width: 30px;
                height: 100px;
            }
            
            .key.black, .synth-key.black {
                height: 70px;
                width: 25px;
            }
            
            .drums {
                grid-template-columns: 1fr;
            }
        }

        /* Notification */
        .notification {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: var(--accent);
            color: white;
            padding: 15px 25px;
            border-radius: 5px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            transform: translateY(100px);
            opacity: 0;
            transition: all 0.3s ease;
            z-index: 1000;
        }

        .notification.show {
            transform: translateY(0);
            opacity: 1;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <img src="logo.png" alt="MusicMantra Logo">
                <h1>MusicMantra</h1>
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#player">Music Player</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
            <div class="mobile-menu">
                <i class="fas fa-bars"></i>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h2>Professional Digital Music Studio</h2>
            <p>Create, play, and enjoy music with our virtual instruments and professional expertise</p>
            <a href="#player" class="btn">Play Music</a>
            <a href="#about" class="btn btn-outline">Learn More</a>
            
            <div class="hero-links">
                <a href="https://www.youtube.com/@lyricsworldofficial9710" target="_blank" class="social-link youtube">
                    <i class="fab fa-youtube"></i> YouTube Channel
                </a>
                <a href="https://discord.gg/sNAYq73J" target="_blank" class="social-link discord">
                    <i class="fab fa-discord"></i> Join Discord
                </a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-title">
                <h2>About MusicMantra</h2>
                <p>Your premier destination for professional music production and playing services</p>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>Where Music Comes to Life</h3>
                    <p>MusicMantra is a state-of-the-art digital music studio dedicated to helping artists, musicians, and music lovers bring their creative visions to life. With cutting-edge technology and a team of experienced professionals, we provide comprehensive music playing and production services tailored to your unique needs.</p>
                    <p>Founded in 2010, MusicMantra has become a trusted name in the music industry, working with both emerging artists and established professionals. Our commitment to excellence and passion for music drives everything we do.</p>
                    <p>From virtual instruments to music production, we offer a full range of services to support your musical journey.</p>
                    <a href="#contact" class="btn">Get In Touch</a>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1511671782779-c97d3d27a1d4?ixlib=rb-4.0.3&auto=format&fit=crop&w=1950&q=80" alt="Music Studio">
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="services">
        <div class="container">
            <div class="section-title">
                <h2>Our Services</h2>
                <p>Comprehensive music production and playing services to meet all your creative needs</p>
            </div>
            <div class="services-grid">
                <div class="service-card">
                    <i class="fas fa-music"></i>
                    <h3>Virtual Instruments</h3>
                    <p>Play a variety of virtual instruments including piano, drums, guitar, and synthesizer with realistic sound quality.</p>
                </div>
                <div class="service-card">
                    <i class="fas fa-sliders-h"></i>
                    <h3>Music Production</h3>
                    <p>Full production services from concept to completion, including arrangement, instrumentation, and sound design.</p>
                </div>
                <div class="service-card">
                    <i class="fas fa-headphones"></i>
                    <h3>Audio Post-Production</h3>
                    <p>Professional audio post-production for film, TV, podcasts, and other multimedia projects.</p>
                </div>
                <div class="service-card">
                    <i class="fas fa-graduation-cap"></i>
                    <h3>Music Lessons</h3>
                    <p>Learn to play various instruments with our experienced instructors through personalized lessons.</p>
                </div>
                <div class="service-card">
                    <i class="fas fa-users"></i>
                    <h3>Community</h3>
                    <p>Join our vibrant music community on YouTube and Discord to connect with fellow musicians.</p>
                </div>
                <div class="service-card">
                    <i class="fas fa-microphone-alt"></i>
                    <h3>Live Sessions</h3>
                    <p>Participate in live music sessions and workshops hosted by industry professionals. We provide coupons of various concerts through our forum in discord. So, join to fulfil your journey of music.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Music Player Section -->
    <section id="player" class="music-player">
        <div class="container">
            <div class="section-title">
                <h2>Virtual Music Studio</h2>
                <p>Play our collection of virtual instruments and create your own music</p>
            </div>
            <div class="player-container">
                <div class="player-header">
                    <h3>Choose Your Instrument</h3>
                    <p>Select an instrument below to start playing</p>
                </div>
                
                <!-- Virtual Instruments -->
                <div class="instruments">
                    <div class="instruments-tabs">
                        <button class="tab active" data-instrument="piano">Piano</button>
                        <button class="tab" data-instrument="drums">Drums</button>
                        <button class="tab" data-instrument="guitar">Guitar</button>
                        <button class="tab" data-instrument="synthesizer">Synthesizer</button>
                    </div>
                    <div class="instrument-panel" id="instrumentPanel">
                        <!-- Piano Interface -->
                        <div id="piano-interface" class="instrument-interface">
                            <div class="piano">
                                <div class="key" data-note="C4"></div>
                                <div class="key black" data-note="C#4"></div>
                                <div class="key" data-note="D4"></div>
                                <div class="key black" data-note="D#4"></div>
                                <div class="key" data-note="E4"></div>
                                <div class="key" data-note="F4"></div>
                                <div class="key black" data-note="F#4"></div>
                                <div class="key" data-note="G4"></div>
                                <div class="key black" data-note="G#4"></div>
                                <div class="key" data-note="A4"></div>
                                <div class="key black" data-note="A#4"></div>
                                <div class="key" data-note="B4"></div>
                                <div class="key" data-note="C5"></div>
                            </div>
                        </div>
                        
                        <!-- Drums Interface -->
                        <div id="drums-interface" class="instrument-interface" style="display: none;">
                            <div class="drums">
                                <div class="drum-pad" data-drum="kick">
                                    <i class="fas fa-drum"></i>
                                    <span>Kick</span>
                                </div>
                                <div class="drum-pad" data-drum="snare">
                                    <i class="fas fa-drum-steelpan"></i>
                                    <span>Snare</span>
                                </div>
                                <div class="drum-pad" data-drum="hihat">
                                    <i class="fas fa-compact-disc"></i>
                                    <span>Hi-Hat</span>
                                </div>
                                <div class="drum-pad" data-drum="crash">
                                    <i class="fas fa-compact-disc"></i>
                                    <span>Crash</span>
                                </div>
                                <div class="drum-pad" data-drum="tom1">
                                    <i class="fas fa-drum"></i>
                                    <span>Tom 1</span>
                                </div>
                                <div class="drum-pad" data-drum="tom2">
                                    <i class="fas fa-drum"></i>
                                    <span>Tom 2</span>
                                </div>
                            </div>
                        </div>
                        
                        <!-- Guitar Interface -->
                        <div id="guitar-interface" class="instrument-interface" style="display: none;">
                            <div class="guitar">
                                <div class="guitar-fretboard">
                                    <div class="guitar-string" data-string="E4"></div>
                                    <div class="guitar-string" data-string="B3"></div>
                                    <div class="guitar-string" data-string="G3"></div>
                                    <div class="guitar-string" data-string="D3"></div>
                                    <div class="guitar-string" data-string="A2"></div>
                                    <div class="guitar-string" data-string="E2"></div>
                                </div>
                                <div class="guitar-controls">
                                    <button class="guitar-btn active" data-effect="clean">Clean</button>
                                    <button class="guitar-btn" data-effect="distortion">Distortion</button>
                                    <button class="guitar-btn" data-effect="reverb">Reverb</button>
                                    <button class="guitar-btn" data-effect="delay">Delay</button>
                                </div>
                            </div>
                        </div>
                        
                        <!-- Synthesizer Interface -->
                        <div id="synthesizer-interface" class="instrument-interface" style="display: none;">
                            <div class="synthesizer">
                                <div class="synth-keyboard">
                                    <div class="synth-key" data-note="C4">C</div>
                                    <div class="synth-key black" data-note="C#4">C#</div>
                                    <div class="synth-key" data-note="D4">D</div>
                                    <div class="synth-key black" data-note="D#4">D#</div>
                                    <div class="synth-key" data-note="E4">E</div>
                                    <div class="synth-key" data-note="F4">F</div>
                                    <div class="synth-key black" data-note="F#4">F#</div>
                                    <div class="synth-key" data-note="G4">G</div>
                                    <div class="synth-key black" data-note="G#4">G#</div>
                                    <div class="synth-key" data-note="A4">A</div>
                                    <div class="synth-key black" data-note="A#4">A#</div>
                                    <div class="synth-key" data-note="B4">B</div>
                                    <div class="synth-key" data-note="C5">C</div>
                                </div>
                                <div class="synth-controls">
                                    <div class="synth-control">
                                        <h4>Oscillator</h4>
                                        <div class="synth-waveform">
                                            <button class="waveform-btn active" data-wave="sine">Sine</button>
                                            <button class="waveform-btn" data-wave="square">Square</button>
                                            <button class="waveform-btn" data-wave="sawtooth">Saw</button>
                                            <button class="waveform-btn" data-wave="triangle">Triangle</button>
                                        </div>
                                    </div>
                                    <div class="synth-control">
                                        <h4>Filter</h4>
                                        <input type="range" class="synth-slider" id="filterFreq" min="100" max="5000" value="1000">
                                        <input type="range" class="synth-slider" id="filterQ" min="0.1" max="30" value="1">
                                    </div>
                                    <div class="synth-control">
                                        <h4>Envelope</h4>
                                        <input type="range" class="synth-slider" id="attack" min="0" max="2" step="0.01" value="0.1">
                                        <input type="range" class="synth-slider" id="decay" min="0" max="2" step="0.01" value="0.2">
                                        <input type="range" class="synth-slider" id="sustain" min="0" max="1" step="0.01" value="0.7">
                                        <input type="range" class="synth-slider" id="release" min="0" max="5" step="0.01" value="0.5">
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contact Us</h2>
                <p>Get in touch to learn more about our services or join our community</p>
            </div>
            <form class="contact-form" id="contactForm">
                <div class="form-group">
                    <label for="name">Full Name</label>
                    <input type="text" id="name" class="form-control" required>
                </div>
                <div class="form-group">
                    <label for="email">Email Address</label>
                    <input type="email" id="email" class="form-control" required>
                </div>
                <div class="form-group">
                    <label for="subject">Subject</label>
                    <input type="text" id="subject" class="form-control" required>
                </div>
                <div class="form-group">
                    <label for="message">Message</label>
                    <textarea id="message" class="form-control" required></textarea>
                </div>
                <button type="submit" class="btn">Send Message</button>
            </form>
            <div class="contact-info">
                <div class="info-card">
                    <i class="fas fa-map-marker-alt"></i>
                    <h3>Visit Us</h3>
                    <p>Kageshwori Manohara-7, Harahara Mahadev<br>Kathmandu, Nepal<br>44600</p>
                </div>
                <div class="info-card">
                    <i class="fas fa-phone-alt"></i>
                    <h3>Call Us</h3>
                    <p>+977 9841256349<br>Sun-Fri: 9am-4pm</p>
                </div>
                <div class="info-card">
                    <i class="fas fa-envelope"></i>
                    <h3>Email Us</h3>
                    <p>kghol2002@gmail.com</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>MusicMantra</h3>
                    <p>Your premier destination for professional music production and playing services.</p>
                    <div class="social-links">
                        <a href="https://www.youtube.com/@lyricsworldofficial9710" target="_blank"><i class="fab fa-youtube"></i></a>
                        <a href="https://discord.gg/sNAYq73J" target="_blank"><i class="fab fa-discord"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">About Us</a></li>
                        <li><a href="#services">Services</a></li>
                        <li><a href="#player">Music Player</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Supporters</h3>
                    <ul class="footer-links">
                        <li><a href="https://www.bandlab.com/?lang=en">Bandlab</a></li>
                        <li><a href="https://www.facebook.com/profile.php?id=61552561492334">Kalinag Nepal</a></li>
                        <li><a href="https://www.facebook.com/profile.php?id=100063146003115">Thali Photo Studio</a></li>
                        <li><a href="https://www.youtube.com/@alishanshiwakotiofficial04">Alishan Shiwakoti</a></li>
                        <li><a href="https://www.youtube.com/@lyricsworldofficial9710">Lyrics World Official</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Newsletter</h3>
                    <p>Subscribe to our newsletter for the latest updates and offers.</p>
                    <form class="form-group">
                        <input type="email" class="form-control" placeholder="Your email address">
                        <button type="submit" class="btn" style="margin-top: 10px;">Subscribe</button>
                    </form>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2025 MusicMantra. All rights reserved.
                    <br>
                    Powered By: Lyrics World Official 9710
                </p>
            </div>
        </div>
    </footer>

    <!-- Notification -->
    <div class="notification" id="notification"></div>

    <script>
        // Audio context and sound generation
        let audioContext;
        let currentInstrument = 'piano';
        let synthWaveform = 'sine';
        let guitarEffect = 'clean';
        
        // Initialize audio context on first user interaction
        function initAudio() {
            if (!audioContext) {
                audioContext = new (window.AudioContext || window.webkitAudioContext)();
            }
        }

        // Note frequencies
        const noteFrequencies = {
            'C4': 261.63,
            'C#4': 277.18,
            'D4': 293.66,
            'D#4': 311.13,
            'E4': 329.63,
            'F4': 349.23,
            'F#4': 369.99,
            'G4': 392.00,
            'G#4': 415.30,
            'A4': 440.00,
            'A#4': 466.16,
            'B4': 493.88,
            'C5': 523.25,
            'B3': 246.94,
            'G3': 196.00,
            'D3': 146.83,
            'A2': 110.00,
            'E2': 82.41
        };

        // Play piano note
        function playPianoNote(note) {
            initAudio();
            const oscillator = audioContext.createOscillator();
            const gainNode = audioContext.createGain();
            
            oscillator.type = 'sine';
            oscillator.frequency.value = noteFrequencies[note];
            
            gainNode.gain.value = 0.3;
            gainNode.gain.exponentialRampToValueAtTime(0.001, audioContext.currentTime + 1);
            
            oscillator.connect(gainNode);
            gainNode.connect(audioContext.destination);
            
            oscillator.start();
            oscillator.stop(audioContext.currentTime + 1);
        }

        // Play drum sound
        function playDrumSound(drumType) {
            initAudio();
            const oscillator = audioContext.createOscillator();
            const gainNode = audioContext.createGain();
            const noiseBuffer = audioContext.createBuffer(1, audioContext.sampleRate * 0.2, audioContext.sampleRate);
            const noiseSource = audioContext.createBufferSource();
            
            // Generate noise
            const output = noiseBuffer.getChannelData(0);
            for (let i = 0; i < noiseBuffer.length; i++) {
                output[i] = Math.random() * 2 - 1;
            }
            
            noiseSource.buffer = noiseBuffer;
            
            // Set up the drum sound based on type
            if (drumType === 'kick') {
                oscillator.type = 'sine';
                oscillator.frequency.value = 60;
                gainNode.gain.value = 1;
                gainNode.gain.exponentialRampToValueAtTime(0.001, audioContext.currentTime + 0.5);
                oscillator.connect(gainNode);
                gainNode.connect(audioContext.destination);
                oscillator.start();
                oscillator.stop(audioContext.currentTime + 0.5);
            } else if (drumType === 'snare') {
                oscillator.type = 'triangle';
                oscillator.frequency.value = 200;
                gainNode.gain.value = 0.5;
                gainNode.gain.exponentialRampToValueAtTime(0.001, audioContext.currentTime + 0.2);
                oscillator.connect(gainNode);
                gainNode.connect(audioContext.destination);
                oscillator.start();
                oscillator.stop(audioContext.currentTime + 0.2);
                
                // Add noise
                const noiseGain = audioContext.createGain();
                noiseGain.gain.value = 0.5;
                noiseGain.gain.exponentialRampToValueAtTime(0.001, audioContext.currentTime + 0.2);
                noiseSource.connect(noiseGain);
                noiseGain.connect(audioContext.destination);
                noiseSource.start();
            } else if (drumType === 'hihat') {
                const noiseGain = audioContext.createGain();
                noiseGain.gain.value = 0.3;
                noiseGain.gain.exponentialRampToValueAtTime(0.001, audioContext.currentTime + 0.05);
                noiseSource.connect(noiseGain);
                noiseGain.connect(audioContext.destination);
                noiseSource.start();
            } else if (drumType === 'crash') {
                const noiseGain = audioContext.createGain();
                noiseGain.gain.value = 0.7;
                noiseGain.gain.exponentialRampToValueAtTime(0.001, audioContext.currentTime + 1);
                noiseSource.connect(noiseGain);
                noiseGain.connect(audioContext.destination);
                noiseSource.start();
            } else if (drumType === 'tom1') {
                oscillator.type = 'sine';
                oscillator.frequency.value = 150;
                gainNode.gain.value = 0.7;
                gainNode.gain.exponentialRampToValueAtTime(0.001, audioContext.currentTime + 0.3);
                oscillator.connect(gainNode);
                gainNode.connect(audioContext.destination);
                oscillator.start();
                oscillator.stop(audioContext.currentTime + 0.3);
            } else if (drumType === 'tom2') {
                oscillator.type = 'sine';
                oscillator.frequency.value = 100;
                gainNode.gain.value = 0.7;
                gainNode.gain.exponentialRampToValueAtTime(0.001, audioContext.currentTime + 0.4);
                oscillator.connect(gainNode);
                gainNode.connect(audioContext.destination);
                oscillator.start();
                oscillator.stop(audioContext.currentTime + 0.4);
            }
        }

        // Play guitar string
        function playGuitarString(string) {
            initAudio();
            const oscillator = audioContext.createOscillator();
            const gainNode = audioContext.createGain();
            const filter = audioContext.createBiquadFilter();
            
            oscillator.type = 'sawtooth';
            oscillator.frequency.value = noteFrequencies[string];
            
            filter.type = 'lowpass';
            filter.frequency.value = noteFrequencies[string] * 2;
            
            gainNode.gain.value = 0.3;
            gainNode.gain.exponentialRampToValueAtTime(0.001, audioContext.currentTime + 2);
            
            // Apply effects
            if (guitarEffect === 'distortion') {
                const distortion = audioContext.createWaveShaper();
                distortion.curve = makeDistortionCurve(50);
                distortion.oversample = '4x';
                oscillator.connect(distortion);
                distortion.connect(filter);
            } else {
                oscillator.connect(filter);
            }
            
            filter.connect(gainNode);
            gainNode.connect(audioContext.destination);
            
            oscillator.start();
            oscillator.stop(audioContext.currentTime + 2);
        }

        // Make distortion curve
        function makeDistortionCurve(amount) {
            const samples = 44100;
            const curve = new Float32Array(samples);
            const deg = Math.PI / 180;
            
            for (let i = 0; i < samples; i++) {
                const x = (i * 2) / samples - 1;
                curve[i] = ((3 + amount) * x * 20 * deg) / (Math.PI + amount * Math.abs(x));
            }
            
            return curve;
        }

        // Play synthesizer note
        function playSynthNote(note) {
            initAudio();
            const oscillator = audioContext.createOscillator();
            const gainNode = audioContext.createGain();
            const filter = audioContext.createBiquadFilter();
            
            oscillator.type = synthWaveform;
            oscillator.frequency.value = noteFrequencies[note];
            
            // Get filter values
            const filterFreq = document.getElementById('filterFreq').value;
            const filterQ = document.getElementById('filterQ').value;
            
            filter.type = 'lowpass';
            filter.frequency.value = filterFreq;
            filter.Q.value = filterQ;
            
            // Get envelope values
            const attack = parseFloat(document.getElementById('attack').value);
            const decay = parseFloat(document.getElementById('decay').value);
            const sustain = parseFloat(document.getElementById('sustain').value);
            const release = parseFloat(document.getElementById('release').value);
            
            const now = audioContext.currentTime;
            gainNode.gain.setValueAtTime(0, now);
            gainNode.gain.linearRampToValueAtTime(0.3, now + attack);
            gainNode.gain.linearRampToValueAtTime(sustain * 0.3, now + attack + decay);
            gainNode.gain.linearRampToValueAtTime(0.001, now + attack + decay + release);
            
            oscillator.connect(filter);
            filter.connect(gainNode);
            gainNode.connect(audioContext.destination);
            
            oscillator.start();
            oscillator.stop(now + attack + decay + release);
        }

        // Mobile Menu Toggle
        document.querySelector('.mobile-menu').addEventListener('click', function() {
            const nav = document.querySelector('nav ul');
            nav.style.display = nav.style.display === 'flex' ? 'none' : 'flex';
        });

        // Smooth Scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Instrument Tabs
        const tabs = document.querySelectorAll('.tab');
        const instrumentInterfaces = document.querySelectorAll('.instrument-interface');
        
        tabs.forEach(tab => {
            tab.addEventListener('click', function() {
                tabs.forEach(t => t.classList.remove('active'));
                this.classList.add('active');
                
                // Hide all instrument interfaces
                instrumentInterfaces.forEach(interface => {
                    interface.style.display = 'none';
                });
                
                // Show selected instrument interface
                const instrument = this.dataset.instrument;
                document.getElementById(`${instrument}-interface`).style.display = 'block';
                
                currentInstrument = instrument;
                showNotification(`Switched to ${instrument.charAt(0).toUpperCase() + instrument.slice(1)}`);
            });
        });

        // Piano Keys
        const pianoKeys = document.querySelectorAll('#piano-interface .key');
        
        pianoKeys.forEach(key => {
            key.addEventListener('mousedown', function() {
                const note = this.dataset.note;
                playPianoNote(note);
                this.classList.add('active');
            });
            
            key.addEventListener('mouseup', function() {
                this.classList.remove('active');
            });
            
            key.addEventListener('mouseleave', function() {
                this.classList.remove('active');
            });
        });

        // Drum Pads
        const drumPads = document.querySelectorAll('.drum-pad');
        
        drumPads.forEach(pad => {
            pad.addEventListener('mousedown', function() {
                const drum = this.dataset.drum;
                playDrumSound(drum);
                this.classList.add('active');
            });
            
            pad.addEventListener('mouseup', function() {
                this.classList.remove('active');
            });
            
            pad.addEventListener('mouseleave', function() {
                this.classList.remove('active');
            });
        });

        // Guitar Strings
        const guitarStrings = document.querySelectorAll('.guitar-string');
        
        guitarStrings.forEach(string => {
            string.addEventListener('mousedown', function() {
                const note = this.dataset.string;
                playGuitarString(note);
                this.classList.add('active');
            });
            
            string.addEventListener('mouseup', function() {
                this.classList.remove('active');
            });
            
            string.addEventListener('mouseleave', function() {
                this.classList.remove('active');
            });
        });

        // Guitar Effects
        const guitarBtns = document.querySelectorAll('.guitar-btn');
        
        guitarBtns.forEach(btn => {
            btn.addEventListener('click', function() {
                guitarBtns.forEach(b => b.classList.remove('active'));
                this.classList.add('active');
                guitarEffect = this.dataset.effect;
                showNotification(`Guitar effect: ${guitarEffect}`);
            });
        });

        // Synthesizer Keys
        const synthKeys = document.querySelectorAll('.synth-key');
        
        synthKeys.forEach(key => {
            key.addEventListener('mousedown', function() {
                const note = this.dataset.note;
                playSynthNote(note);
                this.classList.add('active');
            });
            
            key.addEventListener('mouseup', function() {
                this.classList.remove('active');
            });
            
            key.addEventListener('mouseleave', function() {
                this.classList.remove('active');
            });
        });

        // Synthesizer Waveform
        const waveformBtns = document.querySelectorAll('.waveform-btn');
        
        waveformBtns.forEach(btn => {
            btn.addEventListener('click', function() {
                waveformBtns.forEach(b => b.classList.remove('active'));
                this.classList.add('active');
                synthWaveform = this.dataset.wave;
                showNotification(`Waveform: ${synthWaveform}`);
            });
        });

        // Contact Form
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const subject = document.getElementById('subject').value;
            const message = document.getElementById('message').value;
            
            // In a real application, this would submit the form data to a server
            // For demo purposes, we'll just show a notification
            showNotification('Message sent successfully!');
            
            // Reset form
            this.reset();
        });

        // Newsletter Form
        document.querySelector('.footer-column form').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const email = this.querySelector('input[type="email"]').value;
            
            // In a real application, this would submit the email to a server
            // For demo purposes, we'll just show a notification
            showNotification('Subscribed to newsletter successfully!');
            
            // Reset form
            this.reset();
        });

        // Notification System
        function showNotification(message) {
            const notification = document.getElementById('notification');
            notification.textContent = message;
            notification.classList.add('show');
            
            setTimeout(() => {
                notification.classList.remove('show');
            }, 3000);
        }

        // Initialize
        document.addEventListener('DOMContentLoaded', function() {
            // Nothing special to initialize here
        });
    </script>
</body>
</html>
