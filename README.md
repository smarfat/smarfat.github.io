<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>S. M. Arfatur Rahman - Professional Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        /* Reset and base styles */
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
        
        /* Background gradient */
        body { 
            background: linear-gradient(135deg, #1a2a6c, #2c3e50); 
            color: #ecf0f1; 
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        /* Container for centering content */
        .container { 
            max-width: 1200px; 
            margin: 0 auto; 
            padding: 20px; 
        }
        
        /* Header section */
        header { 
            text-align: center; 
            padding: 40px 0; 
            position: relative;
        }
        
        /* Profile image container with animation */
        .profile-img { 
            width: 400px; 
            height: 400px; 
            border-radius: 50%; 
            border: 8px solid #3498db; 
            margin: 0 auto 30px; 
            overflow: hidden;
            box-shadow: 0 0 30px rgba(52, 152, 219, 0.6);
            animation: float 6s ease-in-out infinite;
            transition: transform 0.5s;
        }
        
        .profile-img:hover {
            transform: scale(1.05);
            border-color: #2ecc71;
        }
        
        /* Floating animation for profile image */
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0px); }
        }
        
        /* Profile image styling */
        .profile-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .profile-img:hover img {
            transform: scale(1.1);
        }
        
        /* Name styling */
        h1 { 
            font-size: 3.5rem; 
            margin-bottom: 10px; 
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            animation: fadeIn 1s ease-in;
        }
        
        /* Subtitle styling */
        .subtitle { 
            font-size: 1.5rem; 
            color: #3498db; 
            margin-bottom: 30px;
            animation: fadeIn 1.2s ease-in;
        }
        
        /* Introduction text */
        .intro { 
            max-width: 800px; 
            margin: 0 auto 40px; 
            font-size: 1.2rem; 
            text-align: center;
            animation: fadeIn 1.4s ease-in;
        }
        
        /* Highlight text */
        .highlight { 
            background: rgba(52, 152, 219, 0.2); 
            padding: 5px 10px; 
            border-radius: 4px; 
            font-weight: bold;
            display: inline-block;
            transition: all 0.3s;
        }
        
        .highlight:hover {
            background: rgba(46, 204, 113, 0.3);
            transform: scale(1.05);
        }
        
        /* Call to action buttons */
        .cta-container { 
            display: flex; 
            justify-content: center; 
            gap: 20px; 
            flex-wrap: wrap;
            margin-bottom: 40px;
        }
        
        .cta-btn { 
            display: inline-block; 
            padding: 15px 30px; 
            background: #3498db; 
            color: white; 
            text-decoration: none; 
            border-radius: 50px; 
            font-weight: bold; 
            transition: all 0.3s; 
            box-shadow: 0 4px 15px rgba(52, 152, 219, 0.4);
            position: relative;
            overflow: hidden;
            z-index: 1;
            cursor: pointer;
        }
        
        .cta-btn:before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 0%;
            height: 100%;
            background: #2980b9;
            transition: all 0.3s;
            z-index: -1;
        }
        
        .cta-btn:hover { 
            transform: translateY(-3px); 
            box-shadow: 0 6px 20px rgba(52, 152, 219, 0.6);
        }
        
        .cta-btn:hover:before {
            width: 100%;
        }
        
        /* Navigation links */
        .nav-links { 
            display: flex; 
            justify-content: center; 
            gap: 30px; 
            margin-top: 40px; 
            flex-wrap: wrap;
        }
        
        .nav-links a { 
            color: #ecf0f1; 
            text-decoration: none; 
            font-weight: bold; 
            transition: all 0.3s;
            padding: 10px 15px;
            border-radius: 5px;
            position: relative;
            cursor: pointer;
        }
        
        .nav-links a:before {
            content: "";
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 3px;
            background: #3498db;
            transition: width 0.3s;
        }
        
        .nav-links a:hover, .nav-links a.active { 
            color: #3498db;
            transform: translateY(-3px);
        }
        
        .nav-links a:hover:before, .nav-links a.active:before {
            width: 100%;
        }
        
        /* Footer */
        footer { 
            text-align: center; 
            padding: 20px; 
            margin-top: 40px; 
            border-top: 1px solid #34495e;
            animation: fadeIn 2s ease-in;
        }
        
        /* Fade in animation */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* Interactive background particles */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            pointer-events: none;
        }
        
        .particle {
            position: absolute;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 50%;
            animation: particle-float 15s infinite linear;
        }
        
        @keyframes particle-float {
            from { transform: translateY(100vh) translateX(0); }
            to { transform: translateY(-100px) translateX(100px); }
        }
        
        /* Section styling */
        .section {
            display: none;
            animation: fadeIn 0.5s ease-in-out;
        }
        
        .section.active {
            display: block;
        }
        
        /* Education section styles */
        .education-card { 
            background: rgba(44, 62, 80, 0.7); 
            border-radius: 15px; 
            padding: 25px; 
            margin-bottom: 30px; 
            box-shadow: 0 10px 20px rgba(0,0,0,0.2); 
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
            animation: slideUp 0.8s ease-out;
        }
        
        .education-card:hover { 
            transform: translateY(-5px); 
            box-shadow: 0 15px 30px rgba(0,0,0,0.3);
        }
        
        .edu-header { 
            display: flex; 
            justify-content: space-between; 
            align-items: center; 
            margin-bottom: 15px; 
            flex-wrap: wrap;
        }
        
        .degree { 
            font-size: 1.5rem; 
            font-weight: bold; 
            color: #3498db; 
        }
        
        .year { 
            background: #3498db; 
            color: white; 
            padding: 5px 15px; 
            border-radius: 20px; 
            font-weight: bold;
        }
        
        .institution { 
            font-size: 1.2rem; 
            margin-bottom: 10px; 
        }
        
        .details { 
            display: flex; 
            justify-content: space-between; 
            flex-wrap: wrap; 
        }
        
        .detail-item { 
            margin-bottom: 10px; 
        }
        
        .detail-label { 
            font-weight: bold; 
            color: #3498db; 
        }
        
        .result { 
            font-size: 1.1rem; 
            font-weight: bold; 
            color: #2ecc71; 
        }
        
        @keyframes slideUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .education-card:before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: #3498db;
            border-radius: 15px 0 0 15px;
        }
        
        /* Skills section styles */
        .skills-container { 
            display: grid; 
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); 
            gap: 25px; 
            margin-bottom: 40px; 
        }
        
        .skill-category { 
            background: rgba(44, 62, 80, 0.7); 
            border-radius: 15px; 
            padding: 25px; 
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
            animation: slideUp 0.8s ease-out;
        }
        
        .skill-category:hover { 
            transform: translateY(-5px); 
            box-shadow: 0 15px 30px rgba(0,0,0,0.3);
        }
        
        .category-title { 
            font-size: 1.5rem; 
            color: #3498db; 
            margin-bottom: 20px; 
            text-align: center;
            position: relative;
        }
        
        .category-title:after {
            content: "";
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 50px;
            height: 3px;
            background: #3498db;
            border-radius: 3px;
        }
        
        .skill-item { 
            display: flex; 
            align-items: center; 
            margin-bottom: 15px; 
            position: relative;
        }
        
        .skill-icon { 
            color: #3498db; 
            margin-right: 15px; 
            font-size: 1.2rem; 
            width: 30px; 
            text-align: center;
            transition: all 0.3s;
        }
        
        .skill-item:hover .skill-icon {
            color: #2ecc71;
            transform: scale(1.2);
        }
        
        .skill-name { 
            font-weight: bold; 
            flex-grow: 1;
        }
        
        .expert-badge { 
            background: #e74c3c; 
            color: white; 
            font-size: 0.7rem; 
            padding: 2px 6px; 
            border-radius: 10px; 
            margin-left: 10px;
            animation: pulse 2s infinite;
        }
        
        .skill-bar { 
            height: 8px; 
            background: #34495e; 
            border-radius: 4px; 
            margin-top: 5px; 
            overflow: hidden; 
            position: relative;
        }
        
        .skill-level { 
            height: 100%; 
            background: linear-gradient(90deg, #3498db, #2ecc71); 
            border-radius: 4px; 
            width: 100%;
            position: relative;
            overflow: hidden;
        }
        
        .skill-level:after {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.4), transparent);
            animation: shimmer 2s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }
        
        @keyframes shimmer {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }
        
        /* Experience section styles */
        .timeline { 
            position: relative; 
            padding: 20px 0; 
        }
        
        .timeline::before { 
            content: ''; 
            position: absolute; 
            top: 0; 
            left: 50%; 
            width: 4px; 
            height: 100%; 
            background: #3498db; 
            transform: translateX(-50%);
            animation: growLine 2s ease-in-out;
        }
        
        .timeline-item { 
            position: relative; 
            margin-bottom: 50px; 
        }
        
        .timeline-content { 
            background: rgba(44, 62, 80, 0.7); 
            border-radius: 15px; 
            padding: 25px; 
            width: 45%; 
            box-shadow: 0 10px 20px rgba(0,0,0,0.2); 
            transition: all 0.3s;
            animation: slideIn 0.8s ease-out;
        }
        
        .timeline-content:hover { 
            transform: translateY(-5px); 
            box-shadow: 0 15px 30px rgba(0,0,0,0.3);
        }
        
        .timeline-item:nth-child(odd) .timeline-content { 
            margin-left: auto; 
        }
        
        .timeline-item:nth-child(even) .timeline-content { 
            margin-right: auto; 
        }
        
        .timeline-dot { 
            position: absolute; 
            top: 30px; 
            width: 20px; 
            height: 20px; 
            background: #3498db; 
            border-radius: 50%; 
            left: 50%; 
            transform: translateX(-50%); 
            border: 4px solid #1a2a6c;
            animation: pulse 2s infinite;
        }
        
        .job-header { 
            display: flex; 
            justify-content: space-between; 
            align-items: center; 
            margin-bottom: 15px; 
            flex-wrap: wrap;
        }
        
        .job-title { 
            font-size: 1.5rem; 
            font-weight: bold; 
            color: #3498db; 
        }
        
        .company { 
            font-size: 1.2rem; 
            margin-bottom: 10px; 
        }
        
        .duration { 
            background: #3498db; 
            color: white; 
            padding: 5px 15px; 
            border-radius: 20px; 
            font-weight: bold;
        }
        
        .responsibilities { 
            margin-top: 15px; 
        }
        
        .responsibilities h4 { 
            margin-bottom: 10px; 
            color: #2ecc71; 
        }
        
        .responsibilities ul { 
            padding-left: 20px; 
        }
        
        .responsibilities li { 
            margin-bottom: 8px; 
            position: relative;
            padding-left: 5px;
        }
        
        @keyframes slideIn {
            from { opacity: 0; transform: translateX(-30px); }
            to { opacity: 1; transform: translateX(0); }
        }
        
        @keyframes growLine {
            from { height: 0; }
            to { height: 100%; }
        }
        
        /* About section styles */
        .about-container { 
            display: flex; 
            gap: 30px; 
            margin-bottom: 40px; 
            flex-wrap: wrap;
        }
        
        .profile-section { 
            flex: 1; 
            min-width: 300px; 
            animation: slideLeft 0.8s ease-out;
        }
        
        .section-title { 
            font-size: 1.8rem; 
            color: #3498db; 
            margin-bottom: 20px; 
            text-align: center;
        }
        
        .info-section { 
            flex: 2; 
            min-width: 300px; 
            animation: slideRight 0.8s ease-out;
        }
        
        .info-card { 
            background: rgba(44, 62, 80, 0.7); 
            border-radius: 15px; 
            padding: 25px; 
            margin-bottom: 30px; 
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }
        
        .info-card:hover { 
            transform: translateY(-5px); 
            box-shadow: 0 15px 30px rgba(0,0,0,0.3);
        }
        
        .info-card h3 { 
            color: #2ecc71; 
            margin-bottom: 15px; 
            font-size: 1.3rem;
            position: relative;
        }
        
        .info-card h3:after {
            content: "";
            position: absolute;
            bottom: -8px;
            left: 0;
            width: 50px;
            height: 3px;
            background: #2ecc71;
            border-radius: 3px;
        }
        
        .info-card p { 
            margin-bottom: 15px; 
        }
        
        @keyframes slideLeft {
            from { opacity: 0; transform: translateX(-30px); }
            to { opacity: 1; transform: translateX(0); }
        }
        
        @keyframes slideRight {
            from { opacity: 0; transform: translateX(30px); }
            to { opacity: 1; transform: translateX(0); }
        }
        
        .info-card:before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: #2ecc71;
            border-radius: 15px 0 0 15px;
        }
        
        /* Contact section styles */
        .contact-container { 
            display: flex; 
            gap: 30px; 
            margin-bottom: 40px; 
            flex-wrap: wrap;
        }
        
        .contact-info { 
            flex: 1; 
            min-width: 300px; 
            animation: slideLeft 0.8s ease-out;
        }
        
        .contact-form { 
            flex: 1; 
            min-width: 300px; 
            animation: slideRight 0.8s ease-out;
        }
        
        .info-card h3 { 
            color: #3498db; 
            margin-bottom: 20px; 
            font-size: 1.5rem; 
            text-align: center;
            position: relative;
        }
        
        .info-card h3:after {
            content: "";
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 50px;
            height: 3px;
            background: #3498db;
            border-radius: 3px;
        }
        
        .contact-item { 
            display: flex; 
            align-items: center; 
            margin-bottom: 20px; 
            transition: all 0.3s;
        }
        
        .contact-item:hover {
            transform: translateX(5px);
        }
        
        .contact-icon { 
            color: #3498db; 
            font-size: 1.5rem; 
            margin-right: 15px; 
            width: 30px; 
            text-align: center;
            transition: all 0.3s;
        }
        
        .contact-item:hover .contact-icon {
            color: #2ecc71;
            transform: scale(1.2);
        }
        
        .contact-text { 
            font-size: 1.1rem; 
        }
        
        .form-group { 
            margin-bottom: 20px; 
        }
        
        .form-group label { 
            display: block; 
            margin-bottom: 8px; 
            font-weight: bold; 
            color: #3498db;
        }
        
        .form-group input, .form-group textarea { 
            width: 100%; 
            padding: 12px; 
            border-radius: 8px; 
            border: none; 
            background: rgba(52, 73, 94, 0.7); 
            color: #ecf0f1; 
            font-size: 1rem;
            transition: all 0.3s;
        }
        
        .form-group input:focus, .form-group textarea:focus {
            outline: none;
            background: rgba(52, 73, 94, 0.9);
            box-shadow: 0 0 10px rgba(52, 152, 219, 0.5);
        }
        
        .form-group textarea { 
            resize: vertical; 
            min-height: 120px; 
        }
        
        .submit-btn { 
            background: #3498db; 
            color: white; 
            border: none; 
            padding: 12px 30px; 
            border-radius: 50px; 
            font-weight: bold; 
            cursor: pointer; 
            transition: all 0.3s; 
            display: block; 
            margin: 0 auto;
            position: relative;
            overflow: hidden;
            z-index: 1;
        }
        
        .submit-btn:before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 0%;
            height: 100%;
            background: #2980b9;
            transition: all 0.3s;
            z-index: -1;
        }
        
        .submit-btn:hover { 
            transform: translateY(-3px); 
            box-shadow: 0 6px 20px rgba(52, 152, 219, 0.6);
        }
        
        .submit-btn:hover:before {
            width: 100%;
        }
        
        .address-section { 
            margin-top: 15px; 
        }
        
        .address-title { 
            font-weight: bold; 
            color: #2ecc71; 
            margin-bottom: 10px;
            display: flex;
            align-items: center;
        }
        
        .address-title i {
            margin-right: 10px;
        }
        
        .info-card:before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: #3498db;
            border-radius: 15px 0 0 15px;
        }
        
        .map-container {
            height: 200px;
            border-radius: 10px;
            overflow: hidden;
            margin-top: 15px;
            position: relative;
        }
        
        .map-placeholder {
            width: 100%;
            height: 100%;
            background: rgba(52, 73, 94, 0.5);
            display: flex;
            align-items: center;
            justify-content: center;
            color: #3498db;
            font-size: 1.2rem;
        }
        
        /* Success message styling */
        .success-message {
            position: fixed;
            top: 20px;
            left: 50%;
            transform: translateX(-50%);
            background: #2ecc71;
            color: white;
            padding: 15px 30px;
            border-radius: 50px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
            z-index: 1000;
            animation: fadeIn 0.5s;
        }
        
        /* Interactive background */
        .interactive-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            opacity: 0.1;
            pointer-events: none;
        }
        
        /* Mobile responsiveness */
        @media (max-width: 768px) {
            .profile-img {
                width: 300px;
                height: 300px;
            }
            
            h1 {
                font-size: 2.5rem;
            }
            
            .timeline::before {
                left: 30px;
            }
            
            .timeline-content {
                width: calc(100% - 60px);
                margin-left: 60px !important;
            }
            
            .timeline-dot {
                left: 30px;
            }
        }
    </style>
</head>
<body>
    <!-- Interactive background -->
    <canvas class="interactive-bg" id="interactiveBg"></canvas>
    
    <!-- Interactive background particles -->
    <div class="particles" id="particles"></div>
    
    <div class="container">
        <!-- Header section with navigation -->
        <header>
            <!-- Profile image container -->
            <div class="profile-img">
                <!-- Replace with your actual photo -->
                <img src="pp_size_photo.jpg" alt="S. M. Arfatur Rahman">
            </div>
            
            <!-- Name and title -->
            <h1>S. M. Arfatur Rahman</h1>
            <div class="subtitle">Territory Manager | Data Enthusiast | Sales & Marketing Professional</div>
            
            <!-- Introduction text -->
            <p class="intro">
                Dynamic and performance-oriented professional with <span class="highlight">6+ years experience</span> in <span class="highlight">Sales, Marketing, 
                and Territory Management.</span> I have a proven track record of driving business growth, building strong client relationships, and leading high-performance teams across competitive markets. With experience in organizations such as <span class="highlight">Square Food & Beverage Limited,</span> <span class="highlight">Japan Tobacco International</span>, <span class="highlight">bKash Limited</span>, and <span class="highlight">Genex Infosys Ltd.</span>, I bring a blend of strategic insight, leadership, and customer-focused execution. I am committed to continuous learning and delivering impactful results for forward-thinking organizations.
            </p>
            
            <!-- Call to action buttons -->
            <div class="cta-container">
                
                <a class="cta-btn" data-section="contact">Contact</a>
            </div>
            
            <!-- Navigation menu -->
            <nav class="nav-links">
                <a class="nav-link active" data-section="home"><i class="fas fa-home"></i> Home</a>
                <a class="nav-link" data-section="education"><i class="fas fa-graduation-cap"></i> Education</a>
                <a class="nav-link" data-section="skills"><i class="fas fa-cogs"></i> Skills</a>
                <a class="nav-link" data-section="experience"><i class="fas fa-briefcase"></i> Experience</a>
                <a class="nav-link" data-section="about"><i class="fas fa-user"></i> About</a>
                <a class="nav-link" data-section="contact"><i class="fas fa-envelope"></i> Contact</a>
            </nav>
        </header>
        
        <!-- Home Section -->
        <section id="home" class="section active">
            <!-- Home content can be added here if needed -->
        </section>
        
        <!-- Education Section -->
        <section id="education" class="section">
            <h1 style="text-align: center; font-size: 3rem; margin-bottom: 20px; text-shadow: 2px 2px 4px rgba(0,0,0,0.3);">Education Background</h1>
            <div class="subtitle" style="text-align: center; font-size: 1.3rem; color: #3498db; margin-bottom: 30px;">Academic Qualifications & Achievements</div>
            
            <!-- Bachelor's degree -->
            <div class="education-card">
                <div class="edu-header">
                    <div class="degree">Bachelor of Business Studies (B.B.S)</div>
                    <div class="year">2018</div>
                </div>
                <div class="institution">Govt. City College, Chattogram | National University</div>
                <div class="details">
                    <div class="detail-item">
                        <span class="detail-label">Result:</span> 
                        <span class="result">CGPA 2.80 (Out of 4.00)</span>
                    </div>
                    <div class="detail-item">
                        <span class="detail-label">Group:</span> Business Studies
                    </div>
                </div>
            </div>
            
            <!-- Higher Secondary Certificate -->
            <div class="education-card">
                <div class="edu-header">
                    <div class="degree">Higher Secondary Certificate (H.S.C)</div>
                    <div class="year">2014</div>
                </div>
                <div class="institution">Govt. City College, Chattogram | Chattogram Board</div>
                <div class="details">
                    <div class="detail-item">
                        <span class="detail-label">Result:</span> 
                        <span class="result">GPA 4.10 (Out of 5.00)</span>
                    </div>
                    <div class="detail-item">
                        <span class="detail-label">Group:</span> Business Studies
                    </div>
                </div>
            </div>
            
            <!-- Secondary School Certificate -->
            <div class="education-card">
                <div class="edu-header">
                    <div class="degree">Secondary School Certificate (S.S.C)</div>
                    <div class="year">2012</div>
                </div>
                <div class="institution">Keshua High School | Chattogram Board</div>
                <div class="details">
                    <div class="detail-item">
                        <span class="detail-label">Result:</span> 
                        <span class="result">GPA 4.94 (Out of 5.00)</span>
                    </div>
                    <div class="detail-item">
                        <span class="detail-label">Group:</span> Business Studies
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Skills Section -->
        <section id="skills" class="section">
            <h1 style="text-align: center; font-size: 3rem; margin-bottom: 20px; text-shadow: 2px 2px 4px rgba(0,0,0,0.3);">Professional Skills</h1>
            <div class="subtitle" style="text-align: center; font-size: 1.3rem; color: #3498db; margin-bottom: 30px;">Core Competencies & Expertise Areas</div>
            
            <div class="skills-container">
                <!-- Sales & Marketing Skills -->
                <div class="skill-category">
                    <div class="category-title"><i class="fas fa-chart-line"></i> Sales & Marketing</div>
                    
                    <div class="skill-item">
                        <div class="skill-icon"><i class="fas fa-bullseye"></i></div>
                        <div>
                            <div class="skill-name">Sales Strategy <span class="expert-badge">Expert</span></div>
                            <div class="skill-bar"><div class="skill-level"></div></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-icon"><i class="fas fa-ad"></i></div>
                        <div>
                            <div class="skill-name">Brand Management <span class="expert-badge">Expert</span></div>
                            <div class="skill-bar"><div class="skill-level"></div></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-icon"><i class="fas fa-users"></i></div>
                        <div>
                            <div class="skill-name">CRM <span class="expert-badge">Expert</span></div>
                            <div class="skill-bar"><div class="skill-level"></div></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-icon"><i class="fas fa-handshake"></i></div>
                        <div>
                            <div class="skill-name">Channel Sales <span class="expert-badge">Expert</span></div>
                            <div class="skill-bar"><div class="skill-level"></div></div>
                        </div>
                    </div>
                </div>
                
                <!-- Strategic Skills -->
                <div class="skill-category">
                    <div class="category-title"><i class="fas fa-lightbulb"></i> Strategic Skills</div>
                    
                    <div class="skill-item">
                        <div class="skill-icon"><i class="fas fa-search"></i></div>
                        <div>
                            <div class="skill-name">Market Research <span class="expert-badge">Expert</span></div>
                            <div class="skill-bar"><div class="skill-level"></div></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-icon"><i class="fas fa-chart-pie"></i></div>
                        <div>
                            <div class="skill-name">Data Analysis <span class="expert-badge">Expert</span></div>
                            <div class="skill-bar"><div class="skill-level"></div></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-icon"><i class="fas fa-calendar-alt"></i></div>
                        <div>
                            <div class="skill-name">Event Marketing <span class="expert-badge">Expert</span></div>
                            <div class="skill-bar"><div class="skill-level"></div></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-icon"><i class="fas fa-map-marked-alt"></i></div>
                        <div>
                            <div class="skill-name">Territory Management <span class="expert-badge">Expert</span></div>
                            <div class="skill-bar"><div class="skill-level"></div></div>
                        </div>
                    </div>
                </div>
                
                <!-- Professional Skills -->
                <div class="skill-category">
                    <div class="category-title"><i class="fas fa-user-tie"></i> Professional Skills</div>
                    
                    <div class="skill-item">
                        <div class="skill-icon"><i class="fas fa-comments"></i></div>
                        <div>
                            <div class="skill-name">Communication <span class="expert-badge">Expert</span></div>
                            <div class="skill-bar"><div class="skill-level"></div></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-icon"><i class="fas fa-user-friends"></i></div>
                        <div>
                            <div class="skill-name">Team Leadership <span class="expert-badge">Expert</span></div>
                            <div class="skill-bar"><div class="skill-level"></div></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-icon"><i class="fas fa-tasks"></i></div>
                        <div>
                            <div class="skill-name">Pressure Management <span class="expert-badge">Expert</span></div>
                            <div class="skill-bar"><div class="skill-level"></div></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-icon"><i class="fas fa-laptop"></i></div>
                        <div>
                            <div class="skill-name">MS Office <span class="expert-badge">Expert</span></div>
                            <div class="skill-bar"><div class="skill-level"></div></div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Experience Section -->
        <section id="experience" class="section">
            <h1 style="text-align: center; font-size: 3rem; margin-bottom: 20px; text-shadow: 2px 2px 4px rgba(0,0,0,0.3);">Professional Experience</h1>
            <div class="subtitle" style="text-align: center; font-size: 1.3rem; color: #3498db; margin-bottom: 30px;">Career Journey & Key Achievements</div>
            
            <div class="timeline">
                <!-- Current job -->
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <div class="timeline-content">
                        <div class="job-header">
                            <div class="job-title">Territory Manager</div>
                            <div class="duration">Jul 2024 - Present</div>
                        </div>
                        <div class="company">Square Food and Beverage Limited</div>
                        <div class="responsibilities">
                            <h4>Key Responsibilities:</h4>
                            <ul>
                                <li>Managing sales and distribution operations in assigned territory</li>
                                <li>Leading team to achieve monthly sales targets and market expansion goals</li>
                                <li>Building strong relationships with distributors, retailers, and key stakeholders</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <!-- Previous job 1 -->
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <div class="timeline-content">
                        <div class="job-header">
                            <div class="job-title">Trade Marketing Supervisor</div>
                            <div class="duration">Mar 2022 - Jun 2024</div>
                        </div>
                        <div class="company">Japan Tobacco International</div>
                        <div class="responsibilities">
                            <h4>Key Responsibilities:</h4>
                            <ul>
                                <li>Implemented trade marketing strategies to boost product visibility and sales</li>
                                <li>Monitored retail activities, POS deployment, and market trends for strategic insights</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <!-- Previous job 2 -->
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <div class="timeline-content">
                        <div class="job-header">
                            <div class="job-title">Senior Merchant Development Officer</div>
                            <div class="duration">Oct 2020 - Jan 2022</div>
                        </div>
                        <div class="company">Peoplescape Limited (Agency of bKash Ltd.)</div>
                        <div class="responsibilities">
                            <h4>Key Responsibilities:</h4>
                            <ul>
                                <li>Onboarded and trained merchants for bKash services in target areas</li>
                                <li>Ensured merchant retention through regular follow-ups and performance analysis</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <!-- Previous job 3 -->
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <div class="timeline-content">
                        <div class="job-header">
                            <div class="job-title">Call Center Executive & Team Mentor</div>
                            <div class="duration">Jul 2018 - Jun 2020</div>
                        </div>
                        <div class="company">Genex Infosys Ltd. (Robi Axiata Ltd)</div>
                        <div class="responsibilities">
                            <h4>Key Responsibilities:</h4>
                            <ul>
                                <li>Handled customer queries and complaints efficiently, ensuring high satisfaction</li>
                                <li>Mentored new agents, improving call quality and team productivity</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- About Section -->
        <section id="about" class="section">
            <h1 style="text-align: center; font-size: 3rem; margin-bottom: 20px; text-shadow: 2px 2px 4px rgba(0,0,0,0.3);">About Me</h1>
            <div class="subtitle" style="text-align: center; font-size: 1.3rem; color: #3498db; margin-bottom: 30px;">Professional Profile & Career Aspirations</div>
            
            <div class="about-container">
                <!-- Profile section -->
                <div class="profile-section">
                    <!-- Profile image container -->
                    <div class="profile-img">
                        <!-- Replace with your actual photo -->
                        <img src="pp_size_photo.jpg" alt="S. M. Arfatur Rahman">
                    </div>
                    
                    <!-- Section title -->
                    <div class="section-title">S. M. Arfatur Rahman</div>
                    
                    <!-- Personal details card -->
                    <div class="info-card">
                        <h3><i class="fas fa-user-circle"></i> Personal Details</h3>
                        <p><strong>Date of Birth:</strong> 30th December 1995</p>
                        <p><strong>Nationality:</strong> Bangladeshi</p>
                        <p><strong>Religion:</strong> Islam</p>
                        <p><strong>Blood Group:</strong> O+ (Positive)</p>
                        <p><strong>Marital Status:</strong> Single</p>
                    </div>
                </div>
                
                <!-- Info section -->
                <div class="info-section">
                    <!-- About me card -->
                    <div class="info-card">
                        <h3><i class="fas fa-info-circle"></i> About Me</h3>
                        <p> I am <b style="color: rgb(26, 139, 92);">S. M. Arfatur Rahman.</b> a dynamic and performance-driven professional with extensive experience in <b style="color: rgb(26, 139, 92);">Sales</b>, <b style="color: rgb(26, 139, 92);">Marketing</b>, <b style="color: rgb(26, 139, 92);"> Trade Marketing</b>, <b style="color: rgb(26, 139, 92);">Territory Sales Management</b>. Over the years, I have worked with reputed organizations, <b style="color: rgb(26, 139, 92);">leading teams, expanding markets, and building strong client relationships.</b> My passion lies in driving <b style="color: rgb(26, 139, 92);">business growth</b> through <b style="color: rgb(26, 139, 92);">strategic planning, effective communication, and leadership.</b> </p>
                        <p>My background includes working with reputed organizations where I led field teams, developed merchant networks, executed promotional activities, and ensured market expansion. I bring proven expertise in communication, negotiation, and leadership, along with the ability to work under pressure and meet deadlines. I am committed to continuous learning and delivering impactful results in every role I take on.</p>
                    </div>
                    
                    <!-- Career objective card -->
                    <div class="info-card">
                        <h3><i class="fas fa-bullseye"></i> Career Objective</h3>
                        <p>To leverage my expertise in <b style="color: aquamarine;">Sales, Marketing, and Territory Management</b> to contribute to the success of a forward-thinking organization. I aim to utilize my leadership, customer relationship management, and strategic insights to achieve business growth while enhancing my professional development through new challenges and opportunities.</p>
                    </div>
                    
                    <!-- Professional summary card -->
                    <div class="info-card">
                        <h3><i class="fas fa-chart-line"></i> Professional Summary</h3>
                        <p>Results-driven professional with proven expertise in <b style="color: aquamarine;">Sales, Marketing, Trade Marketing, and Customer Support.</b> Skilled in leading teams, managing territories, and achieving sales targets in highly competitive markets. Known for strong leadership, strategic thinking, and excellent communication skills, I bring a track record of building relationships with clients, distributors, and stakeholders. Experienced in working with organizations such as <b style="color: aquamarine;">Square Food & Beverage Limited, Japan Tobacco International, bKash Limited, and Genex Infosys Ltd.</b>, I have consistently delivered business growth and customer satisfaction. I am focused on sharpening my strategic insights to contribute meaningfully to the success and expansion of forward-looking organizations.</p>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Contact Section -->
        <section id="contact" class="section">
            <h1 style="text-align: center; font-size: 3rem; margin-bottom: 20px; text-shadow: 2px 2px 4px rgba(0,0,0,0.3);">Contact Me</h1>
            <div class="subtitle" style="text-align: center; font-size: 1.3rem; color: #3498db; margin-bottom: 30px;">Get In Touch & Personal Details</div>
            
            <div class="contact-container">
                <!-- Contact information section -->
                <div class="contact-info">
                    <!-- Personal information card -->
                    <div class="info-card">
                        <h3><i class="fas fa-address-card"></i> Personal Information</h3>
                        <div class="contact-item">
                            <div class="contact-icon"><i class="fas fa-user"></i></div>
                            <div class="contact-text">S. M. Arfatur Rahman</div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon"><i class="fas fa-male"></i></div>
                            <div class="contact-text">Father: S. M. Anwarul Islam</div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon"><i class="fas fa-female"></i></div>
                            <div class="contact-text">Mother: S. M. Rashida Yeasmin</div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon"><i class="fas fa-id-card"></i></div>
                            <div class="contact-text">NID: 4656245877</div>
                        </div>
                    </div>
                    
                    <!-- Address card -->
                    <div class="info-card">
                        <h3><i class="fas fa-map-marker-alt"></i> Address</h3>
                        
                        <!-- Permanent address section -->
                        <div class="address-section">
                            <div class="address-title">
                                <i class="fas fa-home"></i> Permanent Address:
                            </div>
                            <div class="contact-item">
                                <div class="contact-icon"><i class="fas fa-map-pin"></i></div>
                                <div class="contact-text">
                                    Village: Keshua<br>
                                    P.O: Keshua<br>
                                    P.S: Chandanaish<br>
                                    District: Chittagong
                                </div>
                            </div>
                        </div>
                        
                        <!-- Current address section -->
                        <div class="address-section">
                            <div class="address-title">
                                <i class="fas fa-map-marker-alt"></i> Current Address:
                            </div>
                            <div class="contact-item">
                                <div class="contact-icon"><i class="fas fa-map-pin"></i></div>
                                <div class="contact-text">
                                    House: Moslem Housing<br>
                                    Road: Nagra Zilla Porishod Road<br>
                                    District: Netrokona
                                </div>
                            </div>
                        </div>
                        
                        <!-- Map placeholder -->
                        <div class="map-container">
                            <div class="map-placeholder">
                                <i class="fas fa-map-marked-alt"></i> Map View
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Contact form section -->
                <div class="contact-form">
                    <!-- Contact details card -->
                    <div class="info-card">
                        <h3><i class="fas fa-envelope"></i> Contact Details</h3>
                        <div class="contact-item">
                            <div class="contact-icon"><i class="fas fa-envelope"></i></div>
                            <div class="contact-text">smarfaturrahman@gmail.com</div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon"><i class="fas fa-phone"></i></div>
                            <div class="contact-text">01837896060</div>
                        </div>
                    </div>
                    
                    <!-- Message form card -->
                    <div class="info-card">
                        <h3><i class="fas fa-paper-plane"></i> Send Message</h3>
                        <form id="contactForm">
                            <div class="form-group">
                                <label for="name">Your Name</label>
                                <input type="text" id="name" required>
                            </div>
                            <div class="form-group">
                                <label for="email">Your Email</label>
                                <input type="email" id="email" required>
                            </div>
                            <div class="form-group">
                                <label for="message">Message</label>
                                <textarea id="message" required></textarea>
                            </div>
                            <button type="submit" class="submit-btn">Send Message</button>
                        </form>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Footer -->
        <footer>
            <p>&copy; 2025 S. M. Arfatur Rahman. All rights reserved.</p>
        </footer>
    </div>
    
    <script>
        // Function to show/hide sections based on navigation clicks
        function showSection(sectionId) {
            // Hide all sections
            const sections = document.querySelectorAll('.section');
            sections.forEach(section => {
                section.classList.remove('active');
            });
            
            // Show selected section
            const selectedSection = document.getElementById(sectionId);
            if (selectedSection) {
                selectedSection.classList.add('active');
            }
            
            // Update active navigation link
            const navLinks = document.querySelectorAll('.nav-link');
            navLinks.forEach(link => {
                link.classList.remove('active');
            });
            
            // Find and activate the clicked nav link
            navLinks.forEach(link => {
                if (link.getAttribute('data-section') === sectionId) {
                    link.classList.add('active');
                }
            });
            
            // Scroll to top of page
            window.scrollTo(0, 0);
        }
        
        // Add event listeners to all navigation links and CTA buttons
        document.addEventListener('DOMContentLoaded', function() {
            // Get all navigation links and CTA buttons
            const navLinks = document.querySelectorAll('.nav-link');
            const ctaButtons = document.querySelectorAll('.cta-btn');
            
            // Add click event to navigation links
            navLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    const sectionId = this.getAttribute('data-section');
                    showSection(sectionId);
                });
            });
            
            // Add click event to CTA buttons
            ctaButtons.forEach(button => {
                button.addEventListener('click', function(e) {
                    e.preventDefault();
                    const sectionId = this.getAttribute('data-section');
                    showSection(sectionId);
                });
            });
            
            // Contact form submission
            const contactForm = document.getElementById('contactForm');
            if (contactForm) {
                contactForm.addEventListener('submit', function(e) {
                    e.preventDefault();
                    
                    // Get form values
                    const name = document.getElementById('name').value;
                    const email = document.getElementById('email').value;
                    const message = document.getElementById('message').value;
                    
                    // Simple validation
                    if (name && email && message) {
                        // Show success message
                        const successMessage = document.createElement('div');
                        successMessage.className = 'success-message';
                        successMessage.textContent = `Thank you, ${name}! Your message has been sent successfully.`;
                        
                        document.body.appendChild(successMessage);
                        
                        // Remove message after 3 seconds
                        setTimeout(() => {
                            successMessage.style.animation = 'fadeOut 0.5s';
                            setTimeout(() => {
                                document.body.removeChild(successMessage);
                            }, 500);
                        }, 3000);
                        
                        // Reset form
                        this.reset();
                    }
                });
            }
            
            // Create floating particles for background
            const particlesContainer = document.getElementById('particles');
            if (particlesContainer) {
                const particleCount = 30;
                
                for (let i = 0; i < particleCount; i++) {
                    const particle = document.createElement('div');
                    particle.classList.add('particle');
                    
                    // Random size between 5px and 15px
                    const size = Math.random() * 10 + 5;
                    particle.style.width = `${size}px`;
                    particle.style.height = `${size}px`;
                    
                    // Random position
                    particle.style.left = `${Math.random() * 100}%`;
                    
                    // Random animation delay
                    particle.style.animationDelay = `${Math.random() * 15}s`;
                    
                    // Random opacity
                    particle.style.opacity = Math.random() * 0.5 + 0.1;
                    
                    particlesContainer.appendChild(particle);
                }
            }
            
            // Interactive background animation
            const canvas = document.getElementById('interactiveBg');
            if (canvas) {
                const ctx = canvas.getContext('2d');
                
                // Set canvas size
                canvas.width = window.innerWidth;
                canvas.height = window.innerHeight;
                
                // Handle window resize
                window.addEventListener('resize', function() {
                    canvas.width = window.innerWidth;
                    canvas.height = window.innerHeight;
                });
                
                // Create particles
                const particles = [];
                const particleCount = 50;
                
                for (let i = 0; i < particleCount; i++) {
                    particles.push({
                        x: Math.random() * canvas.width,
                        y: Math.random() * canvas.height,
                        radius: Math.random() * 3 + 1,
                        speedX: Math.random() * 1 - 0.5,
                        speedY: Math.random() * 1 - 0.5,
                        color: `rgba(52, 152, 219, ${Math.random() * 0.5 + 0.1})`
                    });
                }
                
                // Animation function
                function animate() {
                    ctx.clearRect(0, 0, canvas.width, canvas.height);
                    
                    particles.forEach(particle => {
                        // Update position
                        particle.x += particle.speedX;
                        particle.y += particle.speedY;
                        
                        // Boundary check
                        if (particle.x < 0 || particle.x > canvas.width) particle.speedX *= -1;
                        if (particle.y < 0 || particle.y > canvas.height) particle.speedY *= -1;
                        
                        // Draw particle
                        ctx.beginPath();
                        ctx.arc(particle.x, particle.y, particle.radius, 0, Math.PI * 2);
                        ctx.fillStyle = particle.color;
                        ctx.fill();
                    });
                    
                    requestAnimationFrame(animate);
                }
                
                animate();
            }
        });
    </script>
</body>
</html>
