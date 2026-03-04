<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Well Yuen Garments Ltd | Global Manufacturing Excellence</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Plus+Jakarta+Sans:wght@300;400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary-dark: #12141d;
            --accent-gold: #c5a059;
            --text-gray: #6c757d;
            --soft-bg: #fdfdfd;
        }

        body { font-family: 'Plus Jakarta Sans', sans-serif; background-color: var(--soft-bg); color: var(--primary-dark); }
        h1, h2, h3 { font-family: 'Playfair Display', serif; }

        /* Navigation */
        .navbar { background: rgba(18, 20, 29, 0.95); backdrop-filter: blur(10px); padding: 20px 0; }
        .navbar-brand { font-weight: 700; letter-spacing: 2px; font-size: 1.5rem; }
        .nav-link { font-size: 0.9rem; text-transform: uppercase; letter-spacing: 1px; margin-left: 20px; color: #fff !important; }

        /* Hero Section */
        .hero-split { height: 90vh; display: flex; align-items: center; background: var(--primary-dark); color: white; overflow: hidden; position: relative; }
        .hero-content { z-index: 2; }
        .hero-image { 
            position: absolute; right: 0; top: 0; width: 50%; height: 100%; 
            background: url('https://images.unsplash.com/photo-1551135049-8a33b5883817?auto=format&fit=crop&q=80&w=1200'); 
            background-size: cover; clip-path: polygon(10% 0, 100% 0, 100% 100%, 0% 100%);
        }

        /* Bento Grid Style for Factories */
        .factory-card { background: white; border: 1px solid #eee; padding: 40px; height: 100%; transition: 0.4s; }
        .factory-card:hover { border-color: var(--accent-gold); box-shadow: 0 20px 40px rgba(0,0,0,0.05); }
        .tag { color: var(--accent-gold); font-weight: 600; font-size: 0.8rem; text-transform: uppercase; letter-spacing: 2px; display: block; margin-bottom: 10px; }

        /* Stats Section */
        .stat-number { font-size: 3rem; font-family: 'Playfair Display'; color: var(--accent-gold); margin-bottom: 0; }
        .stat-label { font-size: 0.8rem; text-transform: uppercase; color: var(--text-gray); letter-spacing: 1px; }

        /* Section Headlines */
        .section-title { position: relative; padding-bottom: 20px; margin-bottom: 40px; }
        .section-title::after { content: ''; position: absolute; left: 0; bottom: 0; width: 60px; height: 3px; background: var(--accent-gold); }

        .btn-gold { background: var(--accent-gold); color: white; border-radius: 0; padding: 15px 35px; border: none; font-weight: 600; }
        .btn-gold:hover { background: #b08d4a; color: white; }
    </style>
</head>
<body>

    <nav class="navbar navbar-expand-lg navbar-dark sticky-top">
        <div class="container">
            <a class="navbar-brand" href="#">WELL YUEN</a>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link" href="#about">Heritage</a></li>
                    <li class="nav-item"><a class="nav-link" href="#facilities">Facilities</a></li>
                    <li class="nav-item"><a class="nav-link" href="#innovation">Innovation</a></li>
                    <li class="nav-item"><a class="nav-link" href="#contact">Inquiry</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <header class="hero-split">
        <div class="container hero-content">
            <div class="row">
                <div class="col-lg-6">
                    <span class="tag" style="color: #fff;">ESTABLISHED 1991</span>
                    <h1 class="display-2 mb-4">Precision Manufacturing for Global Brands</h1>
                    <p class="lead mb-5 text-white-50">30+ years of excellence in high-quality denim, knitwear, and functional sports apparel. Exporting to 20+ countries with advanced smart-factory solutions.</p>
                    <a href="#contact" class="btn btn-gold">PARTNER WITH US</a>
                </div>
            </div>
        </div>
        <div class="hero-image d-none d-lg-block"></div>
    </header>

    <section id="about" class="py-5 bg-white">
        <div class="container py-5">
            <div class="row g-5 align-items-center">
                <div class="col-lg-4">
                    <div class="stat-item mb-5">
                        <p class="stat-number">30+</p>
                        <p class="stat-label">Years Industrial Experience</p>
                    </div>
                    <div class="stat-item mb-5">
                        <p class="stat-number">20+</p>
                        <p class="stat-label">International Markets Served</p>
                    </div>
                    <div class="stat-item">
                        <p class="stat-number">BSCI</p>
                        <p class="stat-label">Certified Social Compliance</p>
                    </div>
                </div>
                <div class="col-lg-8 border-start ps-lg-5">
                    <h2 class="section-title">Our Professional Legacy</h2>
                    <p class="fs-5 text-muted mb-4">Well Yuen Garments Ltd. is a premier clothing manufacturer and exporter in China. We specialize in jackets, coats, jeans, sweaters, and all kinds of knitted & woven garments.</p>
                    <p class="text-muted">Our experienced merchandiser team is deeply familiar with global market requirements regarding fabric innovation, price competitiveness, and strict on-time delivery. We bridge the gap between complex design requirements and high-efficiency production.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="facilities" class="py-5">
        <div class="container py-5">
            <h2 class="section-title text-center mx-auto mb-5" style="max-width: 600px;">Regional Production Centers</h2>
            <div class="row g-4 mt-4">
                <div class="col-md-6">
                    <div class="factory-card">
                        <span class="tag">Regional Hub</span>
                        <h3>Guangdong Facility</h3>
                        <p class="text-muted mt-3">Our specialized center for **Denim and Cardigans**. Equipped with specialized lines for heavy woven denim and delicate knit structures.</p>
                    </div>
                </div>
                <div class="col-md-6">
                    <div class="factory-card">
                        <span class="tag">Regional Hub</span>
                        <h3>Fujian Hub</h3>
                        <p class="text-muted mt-3">Dedicated to **Woven and Knits**. A multi-factory industrial complex focused on lifestyle and functional sports garments.</p>
                    </div>
                </div>
                <div class="col-md-12">
                    <div class="factory-card text-center" style="background: var(--primary-dark); color: white;">
                        <span class="tag">Infrastructure</span>
                        <h3 class="text-white">4,000 SQM Industrial Complex</h3>
                        <p class="text-white-50">Introducing the <strong>Intelligent Hanger System</strong> to maximize production capacity and real-time QC monitoring.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="py-5 bg-white">
        <div class="container py-5">
            <div class="row">
                <div class="col-lg-4">
                    <h2 class="section-title">Global Inquiries</h2>
                    <p class="text-muted">Currently serving markets in the UK, Netherlands, Finland, Germany, Spain, and Australia.</p>
                    <div class="mt-5">
                        <p class="mb-1 fw-bold">Headquarters</p>
                        <p class="text-muted">Guangdong & Fujian Provinces, China</p>
                    </div>
                </div>
                <div class="col-lg-8">
                    <form class="row g-4">
                        <div class="col-md-6">
                            <label class="small fw-bold text-uppercase">Full Name</label>
                            <input type="text" class="form-control form-control-lg border-0 bg-light" placeholder="e.g. John Smith">
                        </div>
                        <div class="col-md-6">
                            <label class="small fw-bold text-uppercase">Company Email</label>
                            <input type="email" class="form-control form-control-lg border-0 bg-light" placeholder="email@company.com">
                        </div>
                        <div class="col-12">
                            <label class="small fw-bold text-uppercase">Project Details</label>
                            <textarea class="form-control form-control-lg border-0 bg-light" rows="4" placeholder="Describe your manufacturing needs..."></textarea>
                        </div>
                        <div class="col-12 text-end">
                            <button type="submit" class="btn btn-gold px-5">SEND PROPOSAL</button>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <footer class="py-4 bg-dark text-white-50 border-top border-secondary">
        <div class="container text-center">
            <p class="small mb-0">© 1991 - 2026 Well Yuen Garments Ltd. | BSCI Certified Manufacturer</p>
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
