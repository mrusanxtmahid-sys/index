# <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Muktadir Ahmod Mahid - Professional Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --bg-color: #0b0f19;
            --card-bg: #131d31;
            --text-main: #f3f4f6;
            --text-muted: #9ca3af;
            --accent: #38bdf8;
            --accent-gradient: linear-gradient(135deg, #38bdf8 0%, #2563eb 100%);
            --border-color: #1e293b;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', system-ui, -apple-system, sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-main);
            line-height: 1.7;
            padding: 20px 10px;
        }

        .portfolio-container {
            max-width: 950px;
            margin: 0 auto;
            background: var(--card-bg);
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.6);
            overflow: hidden;
            border: 1px solid var(--border-color);
        }

        /* Hero Section */
        .hero {
            padding: 50px 20px;
            text-align: center;
            background: radial-gradient(circle at center, #1e293b 0%, #0b0f19 100%);
            border-bottom: 1px solid var(--border-color);
            position: relative;
        }

        .profile-img-container {
            position: relative;
            width: 150px;
            height: 150px;
            margin: 0 auto 20px auto;
        }

        .profile-img {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid var(--accent);
            box-shadow: 0 0 20px rgba(56, 189, 248, 0.4);
        }

        .hero h1 {
            font-size: 32px;
            font-weight: 800;
            margin-bottom: 8px;
            color: #ffffff;
            letter-spacing: -0.5px;
        }

        .hero p.tagline {
            font-size: 16px;
            color: var(--accent);
            font-weight: 600;
            margin-bottom: 20px;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 15px;
        }

        .social-links a {
            background: rgba(56, 189, 248, 0.1);
            color: var(--accent);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            border: 1px solid rgba(56, 189, 248, 0.2);
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            background: var(--accent);
            color: #0b0f19;
            transform: translateY(-3px);
        }

        /* Sections */
        .section {
            padding: 40px 30px;
            border-bottom: 1px solid var(--border-color);
        }

        .section:last-child {
            border-bottom: none;
        }

        .section-title {
            font-size: 20px;
            font-weight: 700;
            color: #ffffff;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .section-title i {
            color: var(--accent);
        }

        /* About Text */
        .about-text {
            color: var(--text-muted);
            font-size: 16px;
            line-height: 1.8;
        }

        /* Info Grid */
        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 15px;
        }

        .info-card {
            background: rgba(15, 23, 42, 0.6);
            padding: 16px 20px;
            border-radius: 12px;
            border: 1px solid var(--border-color);
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .info-card i {
            font-size: 20px;
            color: var(--accent);
        }

        .info-card div span {
            display: block;
            font-size: 12px;
            color: var(--text-muted);
        }

        .info-card div strong {
            font-size: 14px;
            color: #ffffff;
        }

        /* Experience Box */
        .experience-item {
            background: rgba(15, 23, 42, 0.6);
            padding: 25px;
            border-radius: 14px;
            border: 1px solid var(--border-color);
        }

        .experience-item h3 {
            font-size: 18px;
            color: #ffffff;
            margin-bottom: 4px;
        }

        .experience-item .company-time {
            font-size: 13px;
            color: var(--accent);
            margin-bottom: 15px;
            display: block;
            font-weight: 500;
        }

        .experience-item ul {
            list-style: none;
            padding-left: 0;
        }

        .experience-item li {
            position: relative;
            padding-left: 20px;
            margin-bottom: 10px;
            color: var(--text-muted);
            font-size: 14px;
        }

        .experience-item li::before {
            content: "•";
            position: absolute;
            left: 0;
            color: var(--accent);
            font-weight: bold;
        }

        /* Skills Chips */
        .skills-container {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .skill-badge {
            background: rgba(56, 189, 248, 0.08);
            color: var(--accent);
            padding: 8px 16px;
            border-radius: 30px;
            font-size: 13px;
            font-weight: 500;
            border: 1px solid rgba(56, 189, 248, 0.2);
            transition: 0.2s;
        }

        .skill-badge:hover {
            background: rgba(56, 189, 248, 0.2);
            transform: scale(1.03);
        }

        /* Languages */
        .lang-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
        }

        .lang-card {
            background: rgba(15, 23, 42, 0.6);
            padding: 15px 20px;
            border-radius: 12px;
            border: 1px solid var(--border-color);
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 25px;
            background: #080c14;
            color: var(--text-muted);
            font-size: 13px;
            border-top: 1px solid var(--border-color);
        }

        @media (max-width: 768px) {
            .section { padding: 30px 20px; }
            .hero h1 { font-size: 26px; }
        }
    </style>
</head>
<body>

    <div class="portfolio-container">
        <!-- Hero Section -->
        <header class="hero">
            <div class="profile-img-container">
                <img src="profile.jpg" alt="Muktadir Ahmod Mahid" class="profile-img" onerror="this.src='https://via.placeholder.com/150?text=Mahid'">
            </div>
            <h1>Muktadir Ahmod Mahid</h1>
            <p class="tagline">Mobile Phone Repair Technician & Heavy Equipment Expert</p>
            
            <div class="social-links">
                <a href="https://facebook.com/M59A56M74" target="_blank" title="Facebook"><i class="fa-brands fa-facebook-f"></i></a>
                <a href="https://instagram.com/muktadir5674" target="_blank" title="Instagram"><i class="fa-brands fa-instagram"></i></a>
                <a href="mailto:mahid171758@gmail.com" title="Email"><i class="fa-solid fa-envelope"></i></a>
            </div>
        </header>

        <!-- About Section -->
        <section class="section">
            <h2 class="section-title"><i class="fa-solid fa-user"></i> About Me</h2>
            <p class="about-text">
                Experienced Mobile Phone Repair Technician with over 11 years of hands-on expertise in diagnosing, troubleshooting, and servicing complex mobile hardware and software issues[cite: 1]. Possesses foundational skills in operating heavy machinery—including excavators and forklifts—as well as MIG and Arc welding[cite: 1]. A dedicated, adaptable problem-solver with a strong technical background and a commitment to precision and safety[cite: 1].
            </p>
        </section>

        <!-- Personal & Contact Info -->
        <section class="section">
            <h2 class="section-title"><i class="fa-solid id-card"></i><i class="fa-solid fa-address-card"></i> Contact & Personal Info</h2>
            <div class="info-grid">
                <div class="info-card">
                    <i class="fa-solid fa-globe"></i>
                    <div><span>Nationality</span><strong>Bangladeshi[cite: 1]</strong></div>
                </div>
                <div class="info-card">
                    <i class="fa-solid fa-venus-mars"></i>
                    <div><span>Gender</span><strong>Male[cite: 1]</strong></div>
                </div>
                <div class="info-card">
                    <i class="fa-solid fa-cake-candles"></i>
                    <div><span>Date of Birth</span><strong>01/11/2002[cite: 1]</strong></div>
                </div>
                <div class="info-card">
                    <i class="fa-solid fa-phone"></i>
                    <div><span>Phone Number 1</span><strong>(+880) 1759595674[cite: 1]</strong></div>
                </div>
                <div class="info-card">
                    <i class="fa-solid fa-phone-volume"></i>
                    <div><span>Phone Number 2</span><strong>(+880) 1616213512[cite: 1]</strong></div>
                </div>
                <div class="info-card">
                    <i class="fa-solid fa-envelope"></i>
                    <div><span>Email Address</span><strong>mahid171758@gmail.com[cite: 1]</strong></div>
                </div>
                <div class="info-card" style="grid-column: 1 / -1;">
                    <i class="fa-solid fa-location-dot"></i>
                    <div><span>Home Address</span><strong>Uttar Bharaura Sreemangal Moulvibazar, 3210 Sreemangal (Bangladesh)[cite: 1]</strong></div>
                </div>
            </div>
        </section>

        <!-- Work Experience -->
        <section class="section">
            <h2 class="section-title"><i class="fa-solid fa-briefcase"></i> Work Experience</h2>
            <div class="experience-item">
                <h3>Jahid Telecom (Self-Employed)</h3>
                <span class="company-time"><i class="fa-solid fa-location-dot"></i> Sreemangal, Bangladesh &nbsp;|&nbsp; <i class="fa-solid fa-calendar-days"></i> [10/03/2013 - Current][cite: 1]</span>
                <ul>
                    <li><strong>Technical Operations:</strong> Diagnosed and repaired complex hardware and software issues on various mobile phone brands, including micro-soldering, IC replacement, display/battery replacement, and OS flashing[cite: 1].</li>
                    <li><strong>Business Management:</strong> Managed daily shop operations, inventory, inventory sourcing, financial accounts, and pricing strategy[cite: 1].</li>
                    <li><strong>Customer Service & Sales:</strong> Communicated directly with clients to diagnose device issues, provided accurate repair estimates, and ensured high customer satisfaction[cite: 1].</li>
                    <li><strong>Quality & Safety Assurance:</strong> Maintained strict quality control for all repaired electronics and adhered to workplace safety standards[cite: 1].</li>
                </ul>
            </div>
        </section>

        <!-- Skills Section -->
        <section class="section">
            <h2 class="section-title"><i class="fa-solid fa-gears"></i> Skills & Expertise</h2>
            <div class="skills-container">
                <span class="skill-badge">Advanced Mobile Servicing</span>
                <span class="skill-badge">Electronic Equipment Maintenance</span>
                <span class="skill-badge">Hardware Troubleshooting</span>
                <span class="skill-badge">Circuit Board Repair</span>
                <span class="skill-badge">Mobile Device Servicing</span>
                <span class="skill-badge">Soldering</span>
                <span class="skill-badge">Software Diagnostics</span>
                <span class="skill-badge">Forklift Operation</span>
                <span class="skill-badge">Excavator Operation</span>
                <span class="skill-badge">Heavy Equipment Operation</span>
                <span class="skill-badge">MIG Welding</span>
                <span class="skill-badge">Arc Welding</span>
                <span class="skill-badge">Welding[cite: 1]</span>
            </div>
        </section>

        <!-- Languages -->
        <section class="section">
            <h2 class="section-title"><i class="fa-solid fa-language"></i> Language Skills</h2>
            <div class="lang-grid">
                <div class="lang-card">
                    <span style="font-size: 12px; color: var(--text-muted);">Mother Tongue</span>
                    <strong style="display: block; font-size: 15px; color: #fff;">Bengali[cite: 1]</strong>
                </div>
                <div class="lang-card">
                    <span style="font-size: 12px; color: var(--text-muted);">Other Languages</span>
                    <strong style="display: block; font-size: 15px; color: #fff;">English, Urdu, Hindi[cite: 1]</strong>
                </div>
            </div>
        </section>

        <!-- Footer -->
        <footer>
            <p>&copy; 2026 Muktadir Ahmod Mahid. All Rights Reserved.</p>
        </footer>
    </div>

</body>
</html>
