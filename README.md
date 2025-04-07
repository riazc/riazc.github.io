<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Estate Nexus - Premium Property Investment Solutions</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    /* Modern Reset & Base Styles */
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { 
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; 
      line-height: 1.6;
      color: #333;
      background-color: #f9f9f9;
    }
    
    /* Animations */
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    
    /* Scrollbar */
    ::-webkit-scrollbar { width: 10px; }
    ::-webkit-scrollbar-track { background: #f1f1f1; }
    ::-webkit-scrollbar-thumb { background: #888; border-radius: 5px; }
    ::-webkit-scrollbar-thumb:hover { background: #555; }
    
    /* Header */
    header {
      background: linear-gradient(135deg, #1a2a6c, #b21f1f, #fdbb2d);
      color: #fff;
      padding: 15px 0;
      position: sticky;
      top: 0;
      z-index: 100;
      box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    }
    header .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .logo {
      font-size: 1.8em;
      font-weight: bold;
      letter-spacing: 1px;
      display: flex;
      align-items: center;
    }
    .logo i {
      margin-right: 10px;
      font-size: 1.2em;
    }
    nav ul {
      list-style: none;
      display: flex;
    }
    nav ul li {
      margin-left: 25px;
      position: relative;
    }
    nav ul li a {
      color: #fff;
      text-decoration: none;
      font-weight: 500;
      padding: 5px 0;
      transition: all 0.3s ease;
    }
    nav ul li a:hover {
      color: #fdbb2d;
    }
    nav ul li a::after {
      content: '';
      position: absolute;
      width: 0;
      height: 2px;
      background: #fdbb2d;
      left: 0;
      bottom: 0;
      transition: width 0.3s ease;
    }
    nav ul li a:hover::after {
      width: 100%;
    }
    .mobile-menu-btn {
      display: none;
      background: none;
      border: none;
      color: white;
      font-size: 1.5em;
      cursor: pointer;
    }
    
    /* Hero Section */
    .hero {
      background: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)), url('main-page.jpg') no-repeat center center/cover;
      height: 80vh;
      color: #fff;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 0 20px;
      position: relative;
    }
    .hero-content {
      animation: fadeIn 1.2s ease-out;
      max-width: 800px;
    }
    .hero h1 {
      font-size: 3.5em;
      margin-bottom: 20px;
      text-shadow: 2px 2px 8px rgba(0,0,0,0.5);
    }
    .hero p {
      font-size: 1.4em;
      margin-bottom: 30px;
      text-shadow: 1px 1px 4px rgba(0,0,0,0.5);
    }
    .cta {
      padding: 12px 30px;
      background: #e8491d;
      color: #fff;
      text-decoration: none;
      font-size: 1.1em;
      border-radius: 50px;
      font-weight: bold;
      transition: all 0.3s ease;
      display: inline-block;
      box-shadow: 0 4px 15px rgba(232, 73, 29, 0.4);
    }
    .cta:hover {
      background: #ff5a30;
      transform: translateY(-3px);
      box-shadow: 0 6px 20px rgba(232, 73, 29, 0.6);
    }
    .stats-bar {
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      background: rgba(0,0,0,0.7);
      display: flex;
      justify-content: center;
      padding: 15px 0;
    }
    .stat-item {
      text-align: center;
      padding: 0 40px;
      border-right: 1px solid rgba(255,255,255,0.2);
    }
    .stat-item:last-child {
      border-right: none;
    }
    .stat-item h3 {
      font-size: 2em;
      margin-bottom: 5px;
      color: #fdbb2d;
    }
    .stat-item p {
      font-size: 0.9em;
      opacity: 0.8;
    }
    
    /* Sections */
    section {
      padding: 80px 20px;
      max-width: 1200px;
      margin: 0 auto;
    }
    section h2 {
      font-size: 2.5em;
      margin-bottom: 20px;
      text-align: center;
      position: relative;
      padding-bottom: 15px;
    }
    section h2::after {
      content: '';
      position: absolute;
      width: 80px;
      height: 3px;
      background: #e8491d;
      bottom: 0;
      left: 50%;
      transform: translateX(-50%);
    }
    
    /* About Section */
    .about {
      display: flex;
      flex-wrap: wrap;
      gap: 40px;
      align-items: center;
      background: white;
      border-radius: 15px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.05);
      padding: 40px;
      margin-top: -50px;
      position: relative;
      z-index: 10;
    }
    .about-img {
      flex: 1;
      min-width: 300px;
      position: relative;
    }
    .about-img img {
      max-width: 100%;
      height: auto;
      border-radius: 10px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    }
    .about-img::before {
      content: '';
      position: absolute;
      width: 100%;
      height: 100%;
      border: 3px solid #e8491d;
      border-radius: 10px;
      top: 15px;
      left: 15px;
      z-index: -1;
    }
    .about .text {
      flex: 1;
      min-width: 300px;
    }
    .about .text h2 {
      text-align: left;
    }
    .about .text h2::after {
      left: 0;
      transform: none;
    }
    .about .text p {
      margin-bottom: 20px;
      font-size: 1.1em;
      line-height: 1.8;
    }
    .about-features {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      margin-top: 20px;
    }
    .feature-item {
      flex: 1 1 calc(50% - 20px);
      display: flex;
      align-items: center;
      margin-bottom: 15px;
    }
    .feature-item i {
      font-size: 1.5em;
      color: #e8491d;
      margin-right: 10px;
    }
    
    /* Services Section */
    .services {
      text-align: center;
      background-color: #f9f9f9;
    }
    .service-items {
      display: flex;
      flex-wrap: wrap;
      gap: 30px;
      justify-content: center;
      margin-top: 50px;
    }
    .service-item {
      flex: 1 1 calc(33.333% - 30px);
      background: white;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.05);
      transition: all 0.3s ease;
      position: relative;
      overflow: hidden;
    }
    .service-item:hover {
      transform: translateY(-10px);
      box-shadow: 0 15px 30px rgba(0,0,0,0.1);
    }
    .service-item i {
      font-size: 2.5em;
      color: #e8491d;
      margin-bottom: 20px;
      transition: all 0.3s ease;
    }
    .service-item:hover i {
      transform: scale(1.2);
    }
    .service-item h3 {
      margin-bottom: 15px;
      font-size: 1.5em;
    }
    .service-item p {
      color: #666;
      line-height: 1.7;
    }
    .service-item::before {
      content: '';
      position: absolute;
      width: 100%;
      height: 5px;
      background: #e8491d;
      bottom: 0;
      left: 0;
      transform: scaleX(0);
      transform-origin: right;
      transition: transform 0.3s ease;
    }
    .service-item:hover::before {
      transform: scaleX(1);
      transform-origin: left;
    }
    
    /* Properties Section */
    .properties {
      background-color: white;
    }
    .properties h2 {
      margin-bottom: 50px;
    }
    .property-slider {
      display: flex;
      flex-wrap: wrap;
      gap: 30px;
      justify-content: center;
    }
    .property-card {
      flex: 1 1 calc(33.333% - 30px);
      min-width: 300px;
      background: white;
      border-radius: 10px;
      overflow: hidden;
      box-shadow: 0 5px 15px rgba(0,0,0,0.05);
      transition: all 0.3s ease;
    }
    .property-card:hover {
      transform: translateY(-10px);
      box-shadow: 0 15px 30px rgba(0,0,0,0.1);
    }
    .property-img {
      height: 250px;
      overflow: hidden;
      position: relative;
    }
    .property-img img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.5s ease;
    }
    .property-card:hover .property-img img {
      transform: scale(1.1);
    }
    .property-tag {
      position: absolute;
      top: 15px;
      right: 15px;
      background: #e8491d;
      color: white;
      padding: 5px 10px;
      font-size: 0.8em;
      border-radius: 3px;
    }
    .property-info {
      padding: 20px;
    }
    .property-price {
      color: #e8491d;
      font-size: 1.5em;
      font-weight: bold;
      margin-bottom: 10px;
    }
    .property-location {
      color: #666;
      font-size: 0.9em;
      margin-bottom: 15px;
      display: flex;
      align-items: center;
    }
    .property-location i {
      margin-right: 5px;
    }
    .property-details {
      display: flex;
      justify-content: space-between;
      border-top: 1px solid #eee;
      padding-top: 15px;
    }
    .property-detail {
      display: flex;
      align-items: center;
      font-size: 0.9em;
    }
    .property-detail i {
      margin-right: 5px;
      color: #666;
    }
    
    /* Testimonials Section */
    .testimonials {
      background-color: #f9f9f9;
      text-align: center;
    }
    .testimonial-items {
      display: flex;
      flex-wrap: wrap;
      gap: 30px;
      justify-content: center;
      margin-top: 50px;
    }
    .testimonial-item {
      flex: 1 1 calc(33.333% - 30px);
      min-width: 300px;
      background: white;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.05);
      text-align: left;
      position: relative;
    }
    .testimonial-item::before {
      content: '\201C';
      font-size: 80px;
      position: absolute;
      top: -20px;
      left: 10px;
      color: rgba(232, 73, 29, 0.1);
      font-family: Georgia, serif;
    }
    .testimonial-content {
      font-style: italic;
      margin-bottom: 20px;
      line-height: 1.7;
      color: #555;
    }
    .testimonial-author {
      display: flex;
      align-items: center;
    }
    .testimonial-author img {
      width: 60px;
      height: 60px;
      border-radius: 50%;
      margin-right: 15px;
      object-fit: cover;
    }
    .author-info h4 {
      margin-bottom: 5px;
    }
    .author-info p {
      color: #666;
      font-size: 0.9em;
    }
    .testimonial-stars {
      color: #fdbb2d;
      margin-top: 10px;
    }
    
    /* Contact Section */
    .contact {
      background-color: white;
      display: flex;
      flex-wrap: wrap;
      gap: 40px;
      align-items: center;
    }
    .contact-info {
      flex: 1;
      min-width: 300px;
    }
    .contact-info h2 {
      text-align: left;
    }
    .contact-info h2::after {
      left: 0;
      transform: none;
    }
    .contact-info p {
      margin-bottom: 20px;
      line-height: 1.7;
    }
    .contact-details {
      margin-top: 30px;
    }
    .contact-detail {
      display: flex;
      align-items: center;
      margin-bottom: 15px;
    }
    .contact-detail i {
      width: 40px;
      height: 40px;
      background: #f0f0f0;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-right: 15px;
      color: #e8491d;
      font-size: 1.2em;
    }
    .contact-social {
      display: flex;
      gap: 15px;
      margin-top: 30px;
    }
    .contact-social a {
      width: 40px;
      height: 40px;
      background: #f0f0f0;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #333;
      font-size: 1.2em;
      transition: all 0.3s ease;
    }
    .contact-social a:hover {
      background: #e8491d;
      color: white;
      transform: translateY(-3px);
    }
    .contact form {
      flex: 1;
      min-width: 300px;
      background: #f9f9f9;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.05);
    }
    .form-group {
      margin-bottom: 20px;
    }
    .form-group label {
      display: block;
      margin-bottom: 8px;
      font-weight: 500;
    }
    .form-group input,
    .form-group textarea,
    .form-group select {
      width: 100%;
      padding: 12px 15px;
      border: 1px solid #ddd;
      border-radius: 5px;
      font-family: inherit;
      font-size: 1em;
      transition: border 0.3s ease;
    }
    .form-group input:focus,
    .form-group textarea:focus,
    .form-group select:focus {
      border-color: #e8491d;
      outline: none;
    }
    .form-row {
      display: flex;
      gap: 20px;
    }
    .form-row .form-group {
      flex: 1;
    }
    .contact form button {
      padding: 12px 25px;
      background: #e8491d;
      color: #fff;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-size: 1em;
      font-weight: 500;
      transition: all 0.3s ease;
      display: inline-block;
    }
    .contact form button:hover {
      background: #ff5a30;
      transform: translateY(-3px);
    }
    .contact form button i {
      margin-left: 8px;
    }
    
    /* Newsletter */
    .newsletter {
      background: linear-gradient(135deg, #1a2a6c, #b21f1f, #fdbb2d);
      color: white;
      padding: 60px 20px;
      text-align: center;
    }
    .newsletter-content {
      max-width: 700px;
      margin: 0 auto;
    }
    .newsletter h2 {
      margin-bottom: 20px;
    }
    .newsletter h2::after {
      background: white;
    }
    .newsletter p {
      margin-bottom: 30px;
      opacity: 0.9;
    }
    .newsletter-form {
      display: flex;
      max-width: 500px;
      margin: 0 auto;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      border-radius: 50px;
      overflow: hidden;
    }
    .newsletter-form input {
      flex: 1;
      padding: 15px 20px;
      border: none;
      font-size: 1em;
    }
    .newsletter-form input:focus {
      outline: none;
    }
    .newsletter-form button {
      background: #e8491d;
      color: white;
      border: none;
      padding: 0 30px;
      cursor: pointer;
      font-size: 1em;
      transition: all 0.3s ease;
    }
    .newsletter-form button:hover {
      background: #ff5a30;
    }
    
    /* Footer */
    footer {
      background: #222;
      color: #fff;
      padding: 60px 20px 20px;
    }
    .footer-content {
      max-width: 1200px;
      margin: 0 auto;
      display: flex;
      flex-wrap: wrap;
      gap: 40px;
      margin-bottom: 40px;
    }
    .footer-column {
      flex: 1;
      min-width: 200px;
    }
    .footer-column h3 {
      margin-bottom: 20px;
      position: relative;
      padding-bottom: 10px;
      font-size: 1.3em;
    }
    .footer-column h3::after {
      content: '';
      position: absolute;
      width: 40px;
      height: 2px;
      background: #e8491d;
      bottom: 0;
      left: 0;
    }
    .footer-column p {
      margin-bottom: 15px;
      color: #bbb;
      line-height: 1.7;
    }
    .footer-links {
      list-style: none;
    }
    .footer-links li {
      margin-bottom: 10px;
    }
    .footer-links li a {
      color: #bbb;
      text-decoration: none;
      transition: all 0.3s ease;
      display: flex;
      align-items: center;
    }
    .footer-links li a:hover {
      color: #e8491d;
      padding-left: 5px;
    }
    .footer-links li a i {
      margin-right: 8px;
      font-size: 0.8em;
    }
    .footer-bottom {
      text-align: center;
      padding-top: 20px;
      border-top: 1px solid rgba(255,255,255,0.1);
    }
    .footer-bottom p {
      color: #bbb;
      font-size: 0.9em;
    }
    .footer-bottom a {
      color: #bbb;
      text-decoration: none;
      margin: 0 5px;
      transition: color 0.3s ease;
    }
    .footer-bottom a:hover {
      color: #e8491d;
    }
    
    /* Back to Top Button */
    .back-to-top {
      position: fixed;
      bottom: 20px;
      right: 20px;
      width: 40px;
      height: 40px;
      background: #e8491d;
      color: white;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.2em;
      text-decoration: none;
      opacity: 0;
      visibility: hidden;
      transition: all 0.3s ease;
      z-index: 99;
    }
    .back-to-top.show {
      opacity: 1;
      visibility: visible;
    }
    .back-to-top:hover {
      background: #ff5a30;
      transform: translateY(-3px);
    }
    
    /* Responsive Adjustments */
    @media (max-width: 992px) {
      .hero h1 {
        font-size: 2.8em;
      }
      .stats-bar {
        flex-wrap: wrap;
      }
      .stat-item {
        flex: 1 1 calc(50% - 20px);
        margin-bottom: 15px;
      }
      .service-item,
      .property-card,
      .testimonial-item {
        flex: 1 1 calc(50% - 30px);
      }
    }
    
    @media (max-width: 768px) {
      .mobile-menu-btn {
        display: block;
      }
      nav ul {
        position: absolute;
        top: 100%;
        left: 0;
        width: 100%;
        background: #333;
        flex-direction: column;
        align-items: center;
        padding: 20px 0;
        clip-path: polygon(0 0, 100% 0, 100% 0, 0 0);
        transition: all 0.3s ease;
      }
      nav ul.active {
        clip-path: polygon(0 0, 100% 0, 100% 100%, 0 100%);
      }
      nav ul li {
        margin: 15px 0;
      }
      .hero h1 {
        font-size: 2.5em;
      }
      .service-item,
      .property-card,
      .testimonial-item {
        flex: 1 1 100%;
      }
      .form-row {
        flex-direction: column;
        gap: 0;
      }
    }
    
    @media (max-width: 576px) {
      .hero h1 {
        font-size: 2em;
      }
      .hero p {
        font-size: 1.1em;
      }
      .stat-item {
        flex: 1 1 100%;
        border-right: none;
        border-bottom: 1px solid rgba(255,255,255,0.2);
        padding: 15px 0;
      }
      .stat-item:last-child {
        border-bottom: none;
      }
      .about,
      .contact {
        padding: 30px 20px;
      }
    }
  </style>
</head>
<body>
  <!-- Header -->
  <header>
    <div class="container">
      <div class="logo"><i class="fas fa-building"></i>Estate Nexus</div>
      <button class="mobile-menu-btn" id="mobileMenuBtn"><i class="fas fa-bars"></i></button>
      <nav>
        <ul id="mainMenu">
          <li><a href="#hero"><i class="fas fa-home"></i> Home</a></li>
          <li><a href="#about"><i class="fas fa-info-circle"></i> About</a></li>
          <li><a href="#services"><i class="fas fa-concierge-bell"></i> Services</a></li>
          <li><a href="#properties"><i class="fas fa-building"></i> Properties</a></li>
          <li><a href="#contact"><i class="fas fa-envelope"></i> Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="hero" id="hero">
    <div class="hero-content">
      <h1>Exclusive Property Investment Solutions</h1>
      <p>Connecting discerning investors with premium real estate opportunities since 2018.</p>
      <a href="#properties" class="cta">View Featured Properties <i class="fas fa-arrow-right"></i></a>
    </div>
    <div class="stats-bar">
      <div class="stat-item">
        <h3>500+</h3>
        <p>Properties Sourced</p>
      </div>
      <div class="stat-item">
        <h3>850+</h3>
        <p>Happy Investors</p>
      </div>
      <div class="stat-item">
        <h3>£125M+</h3>
        <p>Investment Value</p>
      </div>
      <div class="stat-item">
        <h3>96%</h3>
        <p>Client Satisfaction</p>
      </div>
    </div>
  </section>

  <!-- About Us Section -->
  <section id="about">
    <div class="about">
      <div class="about-img">
        <img src="600x400.jpg" alt="About Estate Nexus">
      </div>
      <div class="text">
        <h2>About Estate Nexus</h2>
        <p>At Estate Nexus, we bridge the gap between premium real estate opportunities and forward-thinking investors. Our expert team of property specialists has over 25 years of combined experience in identifying, vetting, and securing high-yield investment properties across the UK and beyond.</p>
        <p>We understand that property investment is more than just a transaction—it's a strategic wealth-building decision that requires careful consideration, thorough research, and expert guidance.</p>
        <div class="about-features">
          <div class="feature-item">
            <i class="fas fa-check-circle"></i>
            <span>Thoroughly Vetted Properties</span>
          </div>
          <div class="feature-item">
            <i class="fas fa-check-circle"></i>
            <span>Exclusive Off-Market Deals</span>
          </div>
          <div class="feature-item">
            <i class="fas fa-check-circle"></i>
            <span>Transparent Fee Structure</span>
          </div>
          <div class="feature-item">
            <i class="fas fa-check-circle"></i>
            <span>End-to-End Support</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Services Section -->
  <section id="services" class="services">
    <h2>Our Premium Services</h2>
    <div class="service-items">
      <div class="service-item">
        <i class="fas fa-search"></i>
        <h3>Property Sourcing</h3>
        <p>Access exclusive residential and commercial property investments that match your specific investment criteria and financial goals.</p>
      </div>
      <div class="service-item">
        <i class="fas fa-chart-line"></i>
        <h3>Investment Analysis</h3>
        <p>Comprehensive property analysis including cash flow projections, ROI calculations, and market comparables to inform your decisions.</p>
      </div>
      <div class="service-item">
        <i class="fas fa-hands-helping"></i>
        <h3>Acquisition Support</h3>
        <p>End-to-end support throughout the acquisition process, from initial viewing to completion, ensuring a smooth transaction.</p>
      </div>
      <div class="service-item">
        <i class="fas fa-tools"></i>
        <h3>Refurbishment Management</h3>
        <p>Coordination of property refurbishments to maximize rental yields and capital
