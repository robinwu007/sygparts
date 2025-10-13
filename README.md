<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SYGPARTS | Auto & Motorcycle Parts Solutions</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #1a2a4f;
            --secondary: #d4af37;
            --accent: #2a5a8c;
            --light: #f5f5f5;
            --dark: #121212;
            --gray: #e0e0e0;
            --text: #333333;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--light);
            color: var(--text);
            line-height: 1.6;
        }
        
        /* Header & Navigation */
        header {
            background-color: var(--primary);
            padding: 1rem 5%;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: var(--shadow);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo h1 {
            color: white;
            font-size: 1.8rem;
            margin-left: 10px;
        }
        
        .logo span {
            color: var(--secondary);
        }
        
        .logo-icon {
            background-color: var(--secondary);
            color: var(--primary);
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            font-size: 1.2rem;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            position: relative;
            margin-left: 1.5rem;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            padding: 8px 15px;
            border-radius: 4px;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
        }
        
        nav ul li a::after {
            content: '\f107';
            font-family: 'Font Awesome 5 Free';
            font-weight: 900;
            margin-left: 5px;
            font-size: 0.8rem;
        }
        
        nav ul li a:hover,
        nav ul li a.active {
            background-color: var(--secondary);
            color: var(--primary);
        }
        
        /* Dropdown menu */
        .dropdown-menu {
            position: absolute;
            top: 100%;
            left: 0;
            background-color: white;
            min-width: 200px;
            box-shadow: var(--shadow);
            border-radius: 5px;
            opacity: 0;
            visibility: hidden;
            transform: translateY(10px);
            transition: all 0.3s ease;
            z-index: 100;
        }
        
        .dropdown-menu li {
            margin: 0;
            width: 100%;
        }
        
        .dropdown-menu a {
            color: var(--text);
            padding: 10px 15px;
            display: block;
            border-bottom: 1px solid var(--gray);
        }
        
        .dropdown-menu a::after {
            content: '';
        }
        
        .dropdown-menu a:hover {
            background-color: var(--primary);
            color: white;
        }
        
        nav ul li:hover .dropdown-menu {
            opacity: 1;
            visibility: visible;
            transform: translateY(0);
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1494976388531-d1058494cdd8?ixlib=rb-4.0.3&auto=format&fit=crop&w=1200&q=80');
            background-size: cover;
            background-position: center;
            height: 100vh;
            display: flex;
            align-items: center;
            text-align: center;
            color: white;
            padding: 0 5%;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h2 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--secondary);
            color: var(--primary);
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            border: 2px solid var(--secondary);
        }
        
        .btn:hover {
            background-color: transparent;
            color: var(--secondary);
        }
        
        .btn-outline {
            background-color: transparent;
            color: var(--secondary);
            margin-left: 15px;
        }
        
        .btn-outline:hover {
            background-color: var(--secondary);
            color: var(--primary);
        }
        
        /* Sections */
        section {
            padding: 5rem 5%;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
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
            background-color: var(--secondary);
        }
        
        .section-title p {
            max-width: 700px;
            margin: 1rem auto 0;
            color: #666;
        }
        
        /* About Section */
        .about-content {
            display: flex;
            align-items: center;
            gap: 3rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-text h3 {
            color: var(--primary);
            margin-bottom: 1rem;
            font-size: 1.8rem;
        }
        
        .about-text p {
            margin-bottom: 1.5rem;
        }
        
        .about-features {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1.5rem;
            margin-top: 2rem;
        }
        
        .feature {
            display: flex;
            align-items: flex-start;
        }
        
        .feature-icon {
            background-color: rgba(42, 90, 140, 0.1);
            color: var(--accent);
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            font-size: 1.2rem;
        }
        
        .feature-text h4 {
            margin-bottom: 5px;
            color: var(--primary);
        }
        
        .about-image {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        /* Products Section */
        .products {
            background-color: #f8f9fa;
        }
        
        .product-filters {
            display: flex;
            justify-content: center;
            margin-bottom: 2rem;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .filter-btn {
            background-color: white;
            border: 2px solid var(--gray);
            padding: 8px 20px;
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
        }
        
        .filter-btn.active,
        .filter-btn:hover {
            background-color: var(--primary);
            color: white;
            border-color: var(--primary);
        }
        
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .product-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: transform 0.3s ease;
            position: relative;
        }
        
        .product-card:hover {
            transform: translateY(-10px);
        }
        
        .product-image {
            height: 200px;
            overflow: hidden;
            position: relative;
        }
        
        .product-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .product-card:hover .product-image img {
            transform: scale(1.1);
        }
        
        .product-badge {
            position: absolute;
            top: 10px;
            right: 10px;
            background-color: var(--secondary);
            color: var(--primary);
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
        }
        
        .product-info {
            padding: 1.5rem;
        }
        
        .product-category {
            color: var(--accent);
            font-size: 0.9rem;
            font-weight: 600;
            text-transform: uppercase;
            margin-bottom: 5px;
        }
        
        .product-name {
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: var(--primary);
        }
        
        .product-description {
            color: #666;
            font-size: 0.95rem;
            margin-bottom: 15px;
        }
        
        .product-meta {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 1rem;
        }
        
        .product-vehicle {
            display: flex;
            align-items: center;
            color: #666;
            font-size: 0.9rem;
        }
        
        .product-vehicle i {
            margin-right: 5px;
            color: var(--accent);
        }
        
        /* Blog Section */
        .blog-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .blog-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: transform 0.3s ease;
        }
        
        .blog-card:hover {
            transform: translateY(-5px);
        }
        
        .blog-image {
            height: 200px;
            overflow: hidden;
        }
        
        .blog-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .blog-card:hover .blog-image img {
            transform: scale(1.05);
        }
        
        .blog-content {
            padding: 1.5rem;
        }
        
        .blog-meta {
            display: flex;
            color: #777;
            font-size: 0.9rem;
            margin-bottom: 10px;
        }
        
        .blog-date {
            margin-right: 15px;
        }
        
        .blog-author {
            color: var(--accent);
        }
        
        .blog-title {
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: var(--primary);
        }
        
        .blog-excerpt {
            color: #666;
            margin-bottom: 15px;
        }
        
        .read-more {
            color: var(--secondary);
            text-decoration: none;
            font-weight: 600;
            display: inline-flex;
            align-items: center;
        }
        
        .read-more i {
            margin-left: 5px;
            transition: transform 0.3s ease;
        }
        
        .read-more:hover i {
            transform: translateX(5px);
        }
        
        /* Contact Section */
        .contact {
            background-color: #f8f9fa;
        }
        
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 3rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
        }
        
        .contact-method {
            display: flex;
            align-items: flex-start;
            margin-bottom: 2rem;
        }
        
        .contact-icon {
            background-color: rgba(42, 90, 140, 0.1);
            color: var(--accent);
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            font-size: 1.2rem;
        }
        
        .contact-details h4 {
            margin-bottom: 5px;
            color: var(--primary);
        }
        
        .contact-details p, 
        .contact-details a {
            color: #666;
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .contact-details a:hover {
            color: var(--accent);
        }
        
        .social-links {
            display: flex;
            margin-top: 1rem;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: var(--primary);
            color: white;
            border-radius: 50%;
            margin-right: 10px;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background-color: var(--secondary);
            transform: translateY(-3px);
        }
        
        .contact-form {
            background-color: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: var(--shadow);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
            color: var(--primary);
        }
        
        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid var(--gray);
            border-radius: 5px;
            font-size: 1rem;
            transition: border-color 0.3s ease;
        }
        
        .form-control:focus {
            outline: none;
            border-color: var(--accent);
        }
        
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        .submit-btn {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 12px 30px;
            border-radius: 30px;
            font-weight: 600;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        
        .submit-btn:hover {
            background-color: var(--secondary);
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: #bbb;
            padding: 4rem 5% 2rem;
        }
        
        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .footer-col h4 {
            color: white;
            margin-bottom: 1.5rem;
            font-size: 1.3rem;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-col h4::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 2px;
            background-color: var(--secondary);
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 12px;
        }
        
        .footer-links a {
            color: #bbb;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .footer-links a:hover {
            color: var(--secondary);
            padding-left: 5px;
        }
        
        .footer-text {
            margin-bottom: 15px;
        }
        
        .newsletter-form {
            display: flex;
            margin-top: 15px;
        }
        
        .newsletter-input {
            flex: 1;
            padding: 12px;
            border: none;
            border-radius: 5px 0 0 5px;
        }
        
        .newsletter-btn {
            background-color: var(--secondary);
            color: var(--dark);
            border: none;
            padding: 0 20px;
            border-radius: 0 5px 5px 0;
            font-weight: 600;
            cursor: pointer;
        }
        
        .copyright {
            text-align: center;
            padding-top: 2rem;
            margin-top: 2rem;
            border-top: 1px solid #333;
            font-size: 0.9rem;
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .about-content {
                flex-direction: column;
            }
            
            .hero h2 {
                font-size: 2.8rem;
            }
        }
        
        @media (max-width: 768px) {
            nav ul {
                display: none;
                position: absolute;
                top: 70px;
                left: 0;
                width: 100%;
                background-color: var(--primary);
                flex-direction: column;
                padding: 1rem 0;
                box-shadow: var(--shadow);
            }
            
            nav ul.show {
                display: flex;
            }
            
            nav ul li {
                margin: 0;
                text-align: center;
                width: 100%;
            }
            
            nav ul li a {
                display: block;
                padding: 12px;
                border-radius: 0;
                justify-content: center;
            }
            
            .dropdown-menu {
                position: static;
                display: none;
                width: 100%;
                box-shadow: none;
                opacity: 1;
                visibility: visible;
                transform: none;
            }
            
            nav ul li:hover .dropdown-menu {
                display: block;
            }
            
            .dropdown-menu a {
                text-align: center;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .hero h2 {
                font-size: 2.2rem;
            }
            
            .btn {
                display: block;
                margin: 10px auto;
                max-width: 250px;
            }
            
            .btn-outline {
                margin-left: 0;
            }
        }
        
        @media (max-width: 576px) {
            .section-title h2 {
                font-size: 2rem;
            }
            
            .about-features {
                grid-template-columns: 1fr;
            }
            
            .product-grid,
            .blog-grid {
                grid-template-columns: 1fr;
            }
            
            .hero {
                height: 80vh;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="header-container">
            <div class="logo">
                <div class="logo-icon">
                    <i class="fas fa-cogs"></i>
                </div>
                <h1>SYG<span>PARTS</span></h1>
            </div>
            <nav>
                <button class="mobile-menu-btn" id="mobileMenuBtn">
                    <i class="fas fa-bars"></i>
                </button>
                <ul id="navMenu">
                    <li><a href="#" class="active">Home</a></li>
                    
                    <li>
                        <a href="#about">About</a>
                        <ul class="dropdown-menu">
                            <li><a href="#">Company History</a></li>
                            <li><a href="#">Our Team</a></li>
                            <li><a href="#">Quality Assurance</a></li>
                            <li><a href="#">Certifications</a></li>
                        </ul>
                    </li>
                    
                    <li>
                        <a href="#products">Products</a>
                        <ul class="dropdown-menu">
                            <li>
                                <a href="#">Auto Parts <i class="fas fa-chevron-right"></i></a>
                                <ul class="dropdown-menu nested">
                                    <li><a href="#">Engine Components</a></li>
                                    <li><a href="#">Chassis Parts</a></li>
                                    <li><a href="#">Lighting Systems</a></li>
                                    <li><a href="#">Bumpers & Body</a></li>
                                    <li><a href="#">Accessories</a></li>
                                </ul>
                            </li>
                            <li>
                                <a href="#">Motorcycle Parts <i class="fas fa-chevron-right"></i></a>
                                <ul class="dropdown-menu nested">
                                    <li><a href="#">Headlight Assemblies</a></li>
                                    <li><a href="#">Tail Lights</a></li>
                                    <li><a href="#">Turn Signals</a></li>
                                    <li><a href="#">LED Conversion Kits</a></li>
                                </ul>
                            </li>
                            <li><a href="#">New Arrivals</a></li>
                            <li><a href="#">Special Offers</a></li>
                        </ul>
                    </li>
                    
                    <li>
                        <a href="#blog">Blog</a>
                        <ul class="dropdown-menu">
                            <li><a href="#">Industry News</a></li>
                            <li><a href="#">Product Guides</a></li>
                            <li><a href="#">Installation Tips</a></li>
                            <li><a href="#">Maintenance Advice</a></li>
                        </ul>
                    </li>
                    
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h2>Complete Auto,Motorcycle,Agricultural machinery Parts Solutions</h2>
            <p>Your trusted partner for high-quality parts with OEM standards.</p>
            <div>
                <a href="#products" class="btn">Explore Products</a>
                <a href="#contact" class="btn btn-outline">Request Catalog</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="section-title">
            <h2>About SYGPARTS</h2>
            <p>Your one-stop solution for all automotive,motorcycle and agricultural machinery parts since 2010</p>
        </div>
        <div class="about-content">
            <div class="about-text">
                <h3>Comprehensive Automotive Solutions</h3>
                <p>SYGPARTS specializes in providing a complete range of high-quality automotive,motorcycle and agricultural machinery spare parts & accessories solutions. With our extensive industry experience and commitment to excellence, we serve as a trusted partner for businesses worldwide.</p>
                <p>Our product portfolio includes engine components, chassis parts, lighting systems, bumpers, body parts, and a wide range of accessories for all major vehicle makes and models.</p>
                
                <div class="about-features">
                    <div class="feature">
                        <div class="feature-icon">
                            <i class="fas fa-globe"></i>
                        </div>
                        <div class="feature-text">
                            <h4>Global Distribution</h4>
                            <p>Serving clients in 60+ countries worldwide</p>
                        </div>
                    </div>
                    <div class="feature">
                        <div class="feature-icon">
                            <i class="fas fa-certificate"></i>
                        </div>
                        <div class="feature-text">
                            <h4>Quality Certified</h4>
                            <p>ISO 9001 certified manufacturing facilities</p>
                        </div>
                    </div>
                    <div class="feature">
                        <div class="feature-icon">
                            <i class="fas fa-boxes"></i>
                        </div>
                        <div class="feature-text">
                            <h4>Extensive Inventory</h4>
                            <p>Over 15,000 SKUs ready for immediate shipment</p>
                        </div>
                    </div>
                    <div class="feature">
                        <div class="feature-icon">
                            <i class="fas fa-headset"></i>
                        </div>
                        <div class="feature-text">
                            <h4>Technical Support</h4>
                            <p>Expert assistance for product selection and installation</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="about-image">
                <img src="https://images.unsplash.com/photo-1592198084033-aade902d1aae?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="SYGPARTS Warehouse">
            </div>
        </div>
    </section>

    <!-- Products Section -->
    <section id="products" class="products">
        <div class="section-title">
            <h2>Our Product Lines</h2>
            <p>Comprehensive range of automotive,motorcycle and agricultural machinery parts</p>
        </div>
        
        <div class="product-filters">
            <button class="filter-btn active">All Products</button>
            <button class="filter-btn">Auto Parts</button>
            <button class="filter-btn">Motorcycle Parts</button>
            <button class="filter-btn">Agricultural machinery Parts</button>
            <button class="filter-btn">Engine Components</button>
            <button class="filter-btn">New Arrivals</button>
        </div>
        
        <div class="product-grid">
            <!-- Product 1 -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://images.unsplash.com/photo-1553440569-bcc63803a83d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Engine Parts">
                    <div class="product-badge">Auto Engine</div>
                </div>
                <div class="product-info">
                    <div class="product-category">Engine Components</div>
                    <h3 class="product-name">Engine Control Module</h3>
                    <p class="product-description">OEM-compatible ECM for various vehicle models with advanced diagnostics capabilities.</p>
                    <div class="product-meta">
                        <div class="product-vehicle">
                            <i class="fas fa-car"></i> Toyota, Honda, Ford
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Product 2 -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://images.unsplash.com/photo-1551216223-37c8d1dbec5c?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Motorcycle Headlight">
                    <div class="product-badge">Motorcycle</div>
                </div>
                <div class="product-info">
                    <div class="product-category">Lighting Systems</div>
                    <h3 class="product-name">LED Headlight Assembly</h3>
                    <p class="product-description">7-inch waterproof LED headlight with halo ring for improved visibility and style.</p>
                    <div class="product-meta">
                        <div class="product-vehicle">
                            <i class="fas fa-motorcycle"></i> Universal Fit
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Product 3 -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://images.unsplash.com/photo-1583121274602-3e2820c69888?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Chassis Parts">
                    <div class="product-badge">Auto Chassis</div>
                </div>
                <div class="product-info">
                    <div class="product-category">Suspension System</div>
                    <h3 class="product-name">Complete Strut Assembly</h3>
                    <p class="product-description">Premium quality strut assemblies for smooth ride and precise handling.</p>
                    <div class="product-meta">
                        <div class="product-vehicle">
                            <i class="fas fa-car"></i> Sedans, SUVs
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Product 4 -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://images.unsplash.com/photo-1618843479313-40f8afb4b4d8?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Auto Lighting">
                    <div class="product-badge">Auto Lighting</div>
                </div>
                <div class="product-info">
                    <div class="product-category">Lighting Systems</div>
                    <h3 class="product-name">HID Conversion Kit</h3>
                    <p class="product-description">High-intensity discharge conversion kit with 6000K white light output.</p>
                    <div class="product-meta">
                        <div class="product-vehicle">
                            <i class="fas fa-car"></i> Universal Fit
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Product 5 -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://images.unsplash.com/photo-1618843479313-40f8afb4b4d8?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Auto Lighting">
                    <div class="product-badge">Auto Lighting</div>
                </div>
                <div class="product-info">
                    <div class="product-category">Wheels & Tires</div>
                    <h3 class="product-name">Agricultural wheels</h3>
                    <p class="product-description">IATF16949 Certified System.</p>
                    <div class="product-meta">
                        <div class="product-vehicle">
                            <i class="fas fa-car"></i> Universal Fit
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <div style="text-align: center; margin-top: 3rem;">
            <a href="#" class="btn">View Full Product Catalog</a>
        </div>
    </section>
    
    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="section-title">
            <h2>Contact Us</h2>
            <p>Get in touch for product inquiries, technical support, or partnership opportunities</p>
        </div>
        
        <div class="contact-container">
            <div class="contact-info">
                <div class="contact-method">
                    <div class="contact-icon">
                        <i class="fas fa-map-marker-alt"></i>
                    </div>
                    <div class="contact-details">
                        <h4>Our Location</h4>
                        <p>123 Industrial Park, Guangzhou, China 510000</p>
                    </div>
                </div>
                
                <div class="contact-method">
                    <div class="contact-icon">
                        <i class="fas fa-phone-alt"></i>
                    </div>
                    <div class="contact-details">
                        <h4>Phone & WhatsApp</h4>
                        <p>+86 20 8888 7777</p>
                        <p>+86 138 0013 8000 (WhatsApp)</p>
                    </div>
                </div>
                
                <div class="contact-method">
                    <div class="contact-icon">
                        <i class="fas fa-envelope"></i>
                    </div>
                    <div class="contact-details">
                        <h4>Email</h4>
                        <p>sales@sygparts.com</p>
                        <p>support@sygparts.com</p>
                    </div>
                </div>
                
                <div class="contact-method">
                    <div class="contact-icon">
                        <i class="fas fa-clock"></i>
                    </div>
                    <div class="contact-details">
                        <h4>Business Hours</h4>
                        <p>Monday-Friday: 9:00 AM - 6:00 PM (GMT+8)</p>
                        <p>Saturday: 10:00 AM - 4:00 PM</p>
                        <p>Sunday: Closed</p>
                    </div>
                </div>
                
                <div class="social-links">
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-whatsapp"></i></a>
                </div>
            </div>
            
            <div class="contact-form">
                <form id="contactForm">
                    <div class="form-group">
                        <label for="name">Full Name *</label>
                        <input type="text" id="name" class="form-control" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="email">Email Address *</label>
                        <input type="email" id="email" class="form-control" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="phone">Phone Number</label>
                        <input type="tel" id="phone" class="form-control">
                    </div>
                    
                    <div class="form-group">
                        <label for="subject">Subject *</label>
                        <select id="subject" class="form-control" required>
                            <option value="">Select an option</option>
                            <option value="product">Product Inquiry</option>
                            <option value="quote">Request Quote</option>
                            <option value="support">Technical Support</option>
                            <option value="partnership">Partnership</option>
                            <option value="other">Other</option>
                        </select>
                    </div>
                    
                    <div class="form-group">
                        <label for="message">Your Message *</label>
                        <textarea id="message" class="form-control" required></textarea>
                    </div>
                    
                    <button type="submit" class="submit-btn">Send Message</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-container">
            <div class="footer-col">
                <h4>SYGPARTS</h4>
                <p class="footer-text">Your trusted partner for premium automotive and motorcycle parts solutions since 2010. Quality products with worldwide distribution.</p>
                <div class="social-links">
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                </div>
            </div>
            
            <div class="footer-col">
                <h4>Product Categories</h4>
                <ul class="footer-links">
                    <li><a href="#">Engine Components</a></li>
                    <li><a href="#">Chassis & Suspension</a></li>
                    <li><a href="#">Lighting Systems</a></li>
                    <li><a href="#">Body & Exterior</a></li>
                    <li><a href="#">Electrical Parts</a></li>
                    <li><a href="#">Motorcycle Parts</a></li>
                </ul>
            </div>
            
            <div class="footer-col">
                <h4>Quick Links</h4>
                <ul class="footer-links">
                    <li><a href="#">Home</a></li>
                    <li><a href="#about">About Us</a></li>
                    <li><a href="#products">Products</a></li>
                    <li><a href="#blog">Blog</a></li>
                    <li><a href="#contact">Contact</a></li>
                    <li><a href="#">FAQ</a></li>
                </ul>
            </div>
            
            <div class="footer-col">
                <h4>Get Our Catalog</h4>
                <p class="footer-text">Subscribe to receive our latest product catalog and special offers</p>
                <form class="newsletter-form">
                    <input type="email" placeholder="Your Email" class="newsletter-input" required>
                    <button type="submit" class="newsletter-btn">Subscribe</button>
                </form>
            </div>
        </div>
        
        <div class="copyright">
            <p>&copy; 2023 SYGPARTS. All Rights Reserved. | Comprehensive Auto & Motorcycle Parts Solutions</p>
        </div>
    </footer>

    <script>
        // Mobile Menu Toggle
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const navMenu = document.getElementById('navMenu');
        
        mobileMenuBtn.addEventListener('click', () => {
            navMenu.classList.toggle('show');
        });
        
        // Smooth Scrolling for Anchor Links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    window.scrollTo({
                        top: target.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // Close mobile menu if open
                    navMenu.classList.remove('show');
                }
            });
        });
        
        // Product Filtering
        const filterBtns = document.querySelectorAll('.filter-btn');
        
        filterBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                // Remove active class from all buttons
                filterBtns.forEach(b => b.classList.remove('active'));
                
                // Add active class to clicked button
                btn.classList.add('active');
                
                // In a real implementation, you would filter products here
                // For this demo, we're just changing the button state
            });
        });
        
        // Contact Form Submission
        const contactForm = document.getElementById('contactForm');
        contactForm.addEventListener('submit', (e) => {
            e.preventDefault();
            alert('Thank you for your message! We will contact you shortly.');
            contactForm.reset();
        });
        
        // Nested dropdowns for desktop
        const nestedDropdowns = document.querySelectorAll('.nested');
        nestedDropdowns.forEach(dropdown => {
            dropdown.style.display = 'none';
            
            const parentLink = dropdown.parentNode.querySelector('a');
            parentLink.addEventListener('click', (e) => {
                e.preventDefault();
                dropdown.style.display = dropdown.style.display === 'block' ? 'none' : 'block';
            });
        });
    </script>
</body>
</html>
