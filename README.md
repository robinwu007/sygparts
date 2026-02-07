<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SYGPARTS | Global Auto Parts Supply Chain Solution Provider</title>
    <meta name="description" content="One-stop full supply chain solutions for European, American, Japanese, Korean, and Chinese car parts. Your professional sourcing partner in China.">
    <meta property="og:title" content="SYGPARTS - Professional Auto Parts Supply Chain">
    <meta property="og:image" content="https://images.unsplash.com/photo-1486006396113-ad7302ff67f7?auto=format&fit=crop&w=800&q=80">
    
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">

    <style>
        :root {
            --primary: #0f172a; /* 深邃蓝-专业感 */
            --secondary: #fbbf24; /* 工业黄-点睛之笔 */
            --accent: #3b82f6;
            --light: #f8fafc;
            --text: #334155;
            --dark: #020617;
            --gray: #e2e8f0;
            --shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1);
        }

        /* 沿用并优化你提供的基础样式 */
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Inter', sans-serif; }
        body { background-color: var(--light); color: var(--text); line-height: 1.6; }

        header {
            background-color: var(--primary);
            padding: 1rem 5%;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: var(--shadow);
            border-bottom: 2px solid var(--secondary);
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }

        .logo h1 { color: white; font-size: 1.8rem; font-weight: 700; }
        .logo span { color: var(--secondary); }

        nav ul { display: flex; list-style: none; }
        nav ul li { margin-left: 1.5rem; }
        nav ul li a { color: white; text-decoration: none; font-weight: 500; transition: 0.3s; font-size: 0.95rem; }
        nav ul li a:hover { color: var(--secondary); }

        /* Hero Section - 解决一站式方案的视觉 */
        .hero {
            background: linear-gradient(rgba(15, 23, 42, 0.85), rgba(15, 23, 42, 0.85)), 
                        url('https://images.unsplash.com/photo-1486006396113-ad7302ff67f7?auto=format&fit=crop&w=1600&q=80');
            background-size: cover;
            background-position: center;
            height: 90vh;
            display: flex;
            align-items: center;
            text-align: center;
            color: white;
            padding: 0 5%;
        }

        .hero-content { max-width: 900px; margin: 0 auto; }
        .hero h2 { font-size: 3.5rem; margin-bottom: 1.5rem; line-height: 1.2; }
        .hero h2 span { color: var(--secondary); }
        .hero p { font-size: 1.25rem; margin-bottom: 2.5rem; color: #cbd5e1; }

        .btn {
            display: inline-block;
            background-color: var(--secondary);
            color: var(--primary);
            padding: 15px 40px;
            border-radius: 4px;
            text-decoration: none;
            font-weight: 700;
            text-transform: uppercase;
            transition: 0.3s;
        }
        .btn:hover { transform: translateY(-3px); box-shadow: 0 10px 15px -3px rgba(251, 191, 36, 0.3); }

        /* Solutions Section - 强化车系覆盖 */
        section { padding: 6rem 5%; }
        .section-title { text-align: center; margin-bottom: 4rem; }
        .section-title h2 { font-size: 2.5rem; color: var(--primary); margin-bottom: 1rem; }
        .section-title .bar { width: 80px; height: 4px; background: var(--secondary); margin: 0 auto; }

        .solution-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .solution-card {
            background: white;
            padding: 2rem;
            text-align: center;
            border-radius: 8px;
            box-shadow: var(--shadow);
            border-top: 4px solid var(--primary);
            transition: 0.3s;
        }
        .solution-card:hover { border-top-color: var(--secondary); transform: translateY(-5px); }
        .solution-card i { font-size: 2.5rem; color: var(--accent); margin-bottom: 1rem; }

        /* Parts Showcase - 版权合规的图片展示 */
        .parts-gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        .part-item {
            position: relative;
            height: 250px;
            overflow: hidden;
            border-radius: 8px;
        }
        .part-item img {
            width: 100%; height: 100%; object-fit: cover;
            filter: grayscale(20%); transition: 0.5s;
        }
        .part-item:hover img { transform: scale(1.1); filter: grayscale(0%); }
        .part-label {
            position: absolute; bottom: 0; left: 0; right: 0;
            background: linear-gradient(transparent, rgba(0,0,0,0.8));
            color: white; padding: 20px;
        }

        /* 信任感区块 */
        .trust-banner {
            background-color: var(--primary);
            color: white;
            text-align: center;
            padding: 4rem 5%;
        }

        /* Footer */
        footer { background-color: var(--dark); color: #94a3b8; padding: 4rem 5% 2rem; }
        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem; max-width: 1200px; margin: 0 auto;
        }
        .footer-col h4 { color: white; margin-bottom: 1.5rem; }
        .whatsapp-float {
            position: fixed; bottom: 30px; right: 30px;
            background: #25d366; color: white;
            width: 60px; height: 60px; border-radius: 50%;
            display: flex; align-items: center; justify-content: center;
            font-size: 30px; box-shadow: 0 4px 10px rgba(0,0,0,0.3);
            z-index: 2000; text-decoration: none;
        }

        @media (max-width: 768px) {
            .hero h2 { font-size: 2.2rem; }
            nav ul { display: none; }
        }
    </style>
</head>
<body>

    <header>
        <div class="header-container">
            <div class="logo">
                <h1>SYG<span>PARTS</span></h1>
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#solutions">Solutions</a></li>
                    <li><a href="#products">Products</a></li>
                    <li><a href="#about">Supply Chain</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section id="home" class="hero">
        <div class="hero-content">
            <h2>China's Leading <span>Auto Parts</span> Supply Chain Integrator</h2>
            <p>One-stop solution for European, American, Japanese, Korean, and Chinese vehicles. We integrate China's top supply chain resources to solve all your parts challenges.</p>
            <div class="hero-btns">
                <a href="#contact" class="btn">Get a Quote</a>
            </div>
        </div>
    </section>

    <section id="solutions">
        <div class="section-title">
            <h2>Comprehensive Solutions</h2>
            <div class="bar"></div>
            <p>No matter the part, no matter the brand - we have the solution.</p>
        </div>
        <div class="solution-grid">
            <div class="solution-card">
                <i class="fas fa-car-side"></i>
                <h4>European Cars</h4>
                <p>VW, BMW, Mercedes, Audi, etc.</p>
            </div>
            <div class="solution-card">
                <i class="fas fa-truck-pickup"></i>
                <h4>American Cars</h4>
                <p>Ford, GM, Jeep, Chrysler, etc.</p>
            </div>
            <div class="solution-card">
                <i class="fas fa-shuttle-van"></i>
                <h4>Asian Cars</h4>
                <p>Toyota, Honda, Hyundai, Kia, etc.</p>
            </div>
            <div class="solution-card">
                <i class="fas fa-charging-station"></i>
                <h4>Chinese Brands</h4>
                <p>BYD, Geely, Chery, GWM (Full EV Range)</p>
            </div>
        </div>
    </section>

    <div class="trust-banner">
        <h3>Why Partner with SYGPARTS?</h3>
        <p style="margin-top: 15px; color: #94a3b8; max-width: 800px; margin-inline: auto;">We are your eyes in China. We consolidate orders from multiple factories, perform strict quality inspections, and provide professional logistics - saving you time and cost.</p>
    </div>

    <section id="products">
        <div class="section-title">
            <h2>Global Supply Capability</h2>
            <div class="bar"></div>
        </div>
        <div class="parts-gallery">
            <div class="part-item">
                <img src="https://images.unsplash.com/photo-1635437536607-b8572f443763?auto=format&fit=crop&w=600&q=80" alt="Engine Parts">
                <div class="part-label"><h4>Engine Systems</h4></div>
            </div>
            <div class="part-item">
                <img src="https://images.unsplash.com/photo-1599256621730-535171e28e50?auto=format&fit=crop&w=600&q=80" alt="Brake Systems">
                <div class="part-label"><h4>Brake & Suspension</h4></div>
            </div>
            <div class="part-item">
                <img src="https://images.unsplash.com/photo-1619642751034-765dfdf7c58e?auto=format&fit=crop&w=600&q=80" alt="Body Parts">
                <div class="part-label"><h4>Body & Lighting</h4></div>
            </div>
            <div class="part-item">
                <img src="https://images.unsplash.com/photo-1621905252507-b35482cd84b0?auto=format&fit=crop&w=600&q=80" alt="EV Components">
                <div class="part-label"><h4>New Energy EV Parts</h4></div>
            </div>
        </div>
    </section>

    <section id="contact" style="background: #f1f5f9;">
        <div class="contact-container" style="display: grid; grid-template-columns: 1fr 1fr; gap: 50px; max-width: 1200px; margin: 0 auto;">
            <div>
                <h2 style="font-size: 2rem; color: var(--primary);">Start Your Sourcing Today</h2>
                <p style="margin: 20px 0;">Looking for a specific part or need a full supply chain partner? Send us your inquiry list (OE numbers, car models), and we'll handle the rest.</p>
                <ul style="list-style: none;">
                    <li style="margin-bottom: 15px;"><i class="fas fa-check-circle" style="color: var(--secondary); margin-right: 10px;"></i> Professional Sourcing Service</li>
                    <li style="margin-bottom: 15px;"><i class="fas fa-check-circle" style="color: var(--secondary); margin-right: 10px;"></i> Quality Inspection Report</li>
                    <li style="margin-bottom: 15px;"><i class="fas fa-check-circle" style="color: var(--secondary); margin-right: 10px;"></i> Consolidated Shipping</li>
                </ul>
            </div>
            <div style="background: white; padding: 30px; border-radius: 8px; box-shadow: var(--shadow);">
                <form>
                    <input type="text" placeholder="Your Name" style="width: 100%; padding: 12px; margin-bottom: 15px; border: 1px solid var(--gray);">
                    <input type="email" placeholder="Your Email" style="width: 100%; padding: 12px; margin-bottom: 15px; border: 1px solid var(--gray);">
                    <textarea placeholder="Tell us what parts you need (Car Model/Year/OE Number)" style="width: 100%; padding: 12px; height: 120px; border: 1px solid var(--gray); margin-bottom: 15px;"></textarea>
                    <button type="button" class="btn" style="width: 100%; border: none; cursor: pointer;">Send Inquiry</button>
                </form>
            </div>
        </div>
    </section>

    <footer>
        <div class="footer-container">
            <div class="footer-col">
                <h4>SYGPARTS</h4>
                <p>Your expert partner in China's auto parts supply chain. Integrating resources for global success.</p>
            </div>
            <div class="footer-col">
                <h4>Quick Links</h4>
                <ul style="list-style: none;">
                    <li><a href="#" style="color: #94a3b8; text-decoration: none;">European Series</a></li>
                    <li><a href="#" style="color: #94a3b8; text-decoration: none;">Japanese Series</a></li>
                    <li><a href="#" style="color: #94a3b8; text-decoration: none;">China EV Parts</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h4>Connect</h4>
                <div style="font-size: 1.5rem; display: flex; gap: 15px;">
                    <a href="#" style="color: white;"><i class="fab fa-linkedin"></i></a>
                    <a href="#" style="color: white;"><i class="fab fa-facebook"></i></a>
                    <a href="#" style="color: white;"><i class="fab fa-instagram"></i></a>
                </div>
            </div>
        </div>
        <div style="text-align: center; margin-top: 3rem; padding-top: 2rem; border-top: 1px solid #1e293b; font-size: 0.8rem;">
            &copy; 2026 SYGPARTS. All Rights Reserved.
        </div>
    </footer>

    <a href="https://wa.me/你的号码" class="whatsapp-float" target="_blank">
        <i class="fab fa-whatsapp"></i>
    </a>

</body>
</html>
