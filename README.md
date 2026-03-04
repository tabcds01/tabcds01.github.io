<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Well Yuen Garments Ltd. | Premium Clothing Manufacturer Since 1991</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/bootstrap.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    
    <style>
        body { font-family: 'Inter', sans-serif; color: #333; }
        .hero { 
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1558600090-f73f709300c8?auto=format&fit=crop&q=80&w=1600'); 
            background-size: cover; background-position: center; height: 80vh; color: white;
            display: flex; align-items: center; text-align: center;
        }
        .section-padding { padding: 80px 0; }
        .navbar-brand { font-weight: 700; letter-spacing: 1px; }
        .bg-dark-blue { background-color: #1a2a3a; color: white; }
        .card { border: none; transition: transform 0.3s; box-shadow: 0 4px 15px rgba(0,0,0,0.05); }
        .card:hover { transform: translateY(-5px); }
        .feature-icon { font-size: 2.5rem; color: #0d6efd; margin-bottom: 1.5rem; }
        .stats-box { background: #f8f9fa; border-radius: 10px; padding: 30px; text-align: center; }
        .footer { background: #111; color: #ccc; padding: 40px 0; }
    </style>
</head>
<body>

    <nav class="navbar navbar-expand-lg navbar-dark bg-dark sticky-top">
        <div class="container">
            <a class="navbar-brand" href="#">WELL YUEN <span class="text-primary">GARMENTS</span></a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link" href="#about">About Us</a></li>
                    <li class="nav-item"><a class="nav-link" href="#production">Production</a></li>
                    <li class="nav-item"><a class="nav-link" href="#capabilities">Capabilities</a></li>
                    <li class="nav-item"><a class="nav-link" href="#contact">Contact</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <header class="hero">
        <div class="container">
            <h1 class="display-3 fw-bold mb-3">Professional Garment Manufacturing & Export</h1>
            <p class="lead mb-5">Providing high-quality clothing solutions to over 20 countries since 1991.</p>
            <a href="#contact" class="btn btn-primary btn-lg px-5">Inquire Now</a>
        </div>
    </header>

    <section class="container shadow-sm p-4 bg-white rounded" style="margin-top: -50px; position: relative; z-index: 10;">
        <div class="row text-center">
            <div class="col-md-3 border-end"><h3>30+</h3><p class="text-muted mb-0">Years Experience</p></div>
            <div class="col-md-3 border-end"><h3>BSCI</h3><p class="text-muted mb-0">Certified Facility</p></div>
            <div class="col-md-3 border-end"><h3>4000m²</h3><p class="text-muted mb-0">Industrial Complex</p></div>
            <div class="col-md-3"><h3>20+</h3><p class="text-muted mb-0">Global Markets</p></div>
        </div>
    </section>

    <section id="about" class="section-padding">
        <div class="container">
            <div class="row align-items: center;">
                <div class="col-lg-6">
                    <h2 class="fw-bold mb-4">Our Heritage</h2>
                    <p class="text-muted">Established in 1991, Well Yuen Garments Ltd. is a premier clothing manufacturer and exporter in China. With over 30 years of industry leadership, we specialize in jackets, coats, jeans, sweaters, and a full range of knitted and woven garments.</p>
                    <p class="text-muted">We partner with global brands in the leisure, lifestyle, and functional sports sectors, maintaining a reputation for innovation, competitive pricing, and strict quality control.</p>
                </div>
                <div class="col-lg-6">
                    <div class="row g-3">
                        <div class="col-6"><div class="stats-box"><i class="fa fa-microchip feature-icon"></i><h6>Smart Tech</h6><p class="small">Intelligent Hanger System</p></div></div>
                        <div class="col-6"><div class="stats-box"><i class="fa fa-check-circle feature-icon"></i><h6>Quality</h6><p class="small">Strict QC Protocol</p></div></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="production" class="section-padding bg-light">
        <div class="container text-center">
            <h2 class="fw-bold mb-5">Our Production Hubs</h2>
            <div class="row g-4">
                <div class="col-md-6">
                    <div class="card h-100 p-4">
                        <div class="card-body">
                            <h4 class="card-title">Guangdong Center</h4>
                            <p class="text-primary fw-bold">Denims & Cardigans</p>
                            <p class="text-muted">Specialized production lines for high-end denim wear and precision knit cardigans.</p>
                        </div>
                    </div>
                </div>
                <div class="col-md-6">
                    <div class="card h-100 p-4">
                        <div class="card-body">
                            <h4 class="card-title">Fujian Hub</h4>
                            <p class="text-primary fw-bold">Woven & Knits</p>
                            <p class="text-muted">Multi-factory network focusing on durable woven products and versatile knitwear.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="section-padding">
        <div class="container">
            <div class="row">
                <div class="col-lg-5">
                    <h2 class="fw-bold">Get In Touch</h2>
                    <p class="text-muted mb-4">Contact our experienced merchandiser team for inquiries regarding quality, innovation, and international distribution.</p>
                    <ul class="list-unstyled">
                        <li class="mb-3"><i class="fa fa-map-marker-alt text-primary me-3"></i> Guangdong & Fujian, China</li>
                        <li class="mb-3"><i class="fa fa-globe text-primary me-3"></i> Serving 20+ Countries (UK, NL, FI, DE, ES, AU)</li>
                        <li class="mb-3"><i class="fa fa-certificate text-primary me-3"></i> BSCI Certified</li>
                    </ul>
                </div>
                <div class="col-lg-7">
                    <form class="row g-3">
                        <div class="col-md-6"><input type="text" class="form-control" placeholder="Your Name"></div>
                        <div class="col-md-6"><input type="email" class="form-control" placeholder="Business Email"></div>
                        <div class="col-12"><input type="text" class="form-control" placeholder="Subject (e.g., Denim Inquiry)"></div>
                        <div class="col-12"><textarea class="form-control" rows="5" placeholder="Message"></textarea></div>
                        <div class="col-12"><button type="submit" class="btn btn-primary px-5">Send Inquiry</button></div>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <footer class="footer text-center">
        <div class="container">
            <p class="mb-0">&copy; 1991 - 2026 Well Yuen Garments Ltd. All Rights Reserved.</p>
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
