<!DOCTYPE html>
<html lang="zh-Hant">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Well Yuen Garments Ltd | 華源製衣有限公司</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@300;400;700&family=Plus+Jakarta+Sans:wght@400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary-dark: #0f1115;
            --accent-gold: #c5a059;
            --overlay-dark: rgba(0, 0, 0, 0.65); 
        }

        body { font-family: 'Plus Jakarta Sans', 'Noto Sans TC', sans-serif; transition: 0.3s; color: #333; overflow-x: hidden; }
        html { scroll-behavior: smooth; }
        
        [lang="en"] .lang-zh { display: none !important; }
        [lang="zh"] .lang-en { display: none !important; }

        /* Navbar */
        .navbar { background: rgba(15, 17, 21, 0.98); padding: 12px 0; border-bottom: 1px solid rgba(255,255,255,0.1); }
        .navbar-brand img { height: 38px; margin-right: 12px; width: auto; }
        .lang-switch .btn { color: #fff; border: 1px solid rgba(255,255,255,0.3); font-size: 0.75rem; padding: 4px 10px; margin-left: 5px; border-radius: 0; }
        .lang-switch .btn.active { background: var(--accent-gold); border-color: var(--accent-gold); }

        /* Hero Section - 縮小高度並強化視覺中心 */
        .hero-section { 
            height: 75vh; 
            min-height: 550px;
            background: linear-gradient(var(--overlay-dark), var(--overlay-dark)), 
                        url('https://i.postimg.cc/wT6Bwt7T/WY-pic.jpg');
            background-size: cover; 
            background-position: center 30%;
            display: flex; align-items: center; color: white;
            text-align: center;
            padding-top: 70px;
        }
        .hero-logo-big { width: 110px; margin-bottom: 25px; filter: drop-shadow(0 0 20px rgba(0,0,0,0.4)); }
        .hero-content { width: 100%; max-width: 900px; margin: 0 auto; padding: 0 20px; }

        /* Section Commons */
        .section-padding { padding: 90px 0; }
        .bg-light-gray { background: #f9f9f9; }
        .text-gold { color: var(--accent-gold); }
        
        /* About Stats */
        .stat-item h3 { font-size: 2.8rem; color: var(--primary-dark); line-height: 1; margin-bottom: 5px; }
        .image-overlay-box { position: relative; padding: 10px; }
        .image-overlay-box::before {
            content: ""; position: absolute; left: -10px; bottom: -10px;
            width: 70%; height: 70%; border: 4px solid var(--accent-gold); z-index: 0;
        }
        .image-overlay-box img { position: relative; z-index: 1; width: 100%; box-shadow: 0 15px 35px rgba(0,0,0,0.15); }

        /* Product Cards */
        .product-card { 
            background: #fff; padding: 45px 30px; height: 100%; 
            border-top: 4px solid var(--accent-gold); 
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
            transition: all 0.4s ease;
        }
        .product-card:hover { transform: translateY(-10px); }

        /* Feature Icons */
        .feature-icon-small { font-size: 1.5rem; color: var(--accent-gold); margin-right: 15px; }

        /* Contact & Footer */
        .contact-box { background: rgba(255,255,255,0.05); padding: 35px; border: 1px solid rgba(255,255,255,0.1); border-radius: 5px; height: 100%; transition: 0.3s; }
        .contact-box:hover { border-color: var(--accent-gold); }
        .address-text { font-size: 0.95rem; line-height: 1.8; color: rgba(255,255,255,0.7); }
        
        .btn-gold { background: var(--accent-gold); color: white; border-radius: 0; padding: 14px 40px; font-weight: 600; border: none; transition: 0.3s; text-decoration: none; display: inline-block; }
        .btn-gold:hover { background: #b08d4a; color: white; transform: translateY(-3px); }

        @media (max-width: 768px) {
            .hero-section { height: 85vh; }
            .hero-content h1 { font-size: 1.8rem !important; }
        }
    </style>
</head>
<body lang="en">

    <nav class="navbar navbar-expand-lg navbar-dark fixed-top">
        <div class="container">
            <a class="navbar-brand d-flex align-items-center" href="#">
                <img src="https://i.ibb.co/3W6qWbH/wy-logo-fixed.png" alt="Well Yuen Logo">
                <div class="lh-1">
                    <span class="lang-en fw-bold d-block">WELL YUEN <small class="fw-light">Garments</small></span>
                    <span class="lang-zh fw-bold d-block">華源製衣 <small class="fw-light">有限公司</small></span>
                </div>
            </a>
            <div class="ms-auto lang-switch">
                <button id="btn-en" class="btn" onclick="setLanguage('en')">EN</button>
                <button id="btn-zh" class="btn" onclick="setLanguage('zh')">中文</button>
            </div>
        </div>
    </nav>

    <header class="hero-section">
        <div class="hero-content">
            <img src="https://i.ibb.co/3W6qWbH/wy-logo-fixed.png" alt="Well Yuen Logo" class="hero-logo-big">
            <div class="lang-en">
                <h1 class="display-3 fw-bold mb-3">WELL YUEN Garments Ltd.</h1>
                <p class="fs-5 text-white-75 mb-5">Professional Apparel Manufacturing Partner Since 1991.</p>
                <a href="#contact" class="btn btn-gold">CONTACT US</a>
            </div>
            <div class="lang-zh">
                <h1 class="display-3 fw-bold mb-3">華源製衣有限公司</h1>
                <p class="fs-4 text-white-75 mb-5">始於 1991 年。您最值得信賴的專業服飾製造夥伴。</p>
                <a href="#contact" class="btn btn-gold">立即洽詢</a>
            </div>
        </div>
    </header>

    <section id="about" class="section-padding bg-white">
        <div class="container">
            <div class="row align-items-center g-5">
                <div class="col-lg-6">
                    <h6 class="text-gold fw-bold mb-3 lang-en">OUR HERITAGE</h6>
                    <h6 class="text-gold fw-bold mb-3 lang-zh">公司傳承</h6>
                    <h2 class="display-5 fw-bold mb-4 lang-en">30+ Years of Excellence</h2>
                    <h2 class="display-5 fw-bold mb-4 lang-zh">三十載深耕，成就卓越</h2>
                    <p class="text-muted lang-en">Established in 1991, Well Yuen Garments has grown into a leader in garment production, serving prestigious global brands with unwavering quality and social compliance.</p>
                    <p class="text-muted lang-zh">華源製衣成立於 1991 年。我們以香港為管理核心，憑藉卓越的品質控管與國際合規認證，成為全球眾多知名品牌的長期戰略合作工廠。</p>
                    <div class="d-flex gap-5 mt-5">
                        <div class="stat-item">
                            <h3 class="fw-bold">35+</h3>
                            <small class="text-muted lang-en">Years of Mastery</small>
                            <small class="text-muted lang-zh">產業資歷</small>
                        </div>
                        <div class="stat-item border-start ps-4">
                            <h3 class="fw-bold text-gold">BSCI</h3>
                            <small class="text-muted lang-en">SA8000 Certified</small>
                            <small class="text-muted lang-zh">國際生產認證</small>
                        </div>
                    </div>
                </div>
                <div class="col-lg-6">
                    <div class="image-overlay-box">
                        <img src="https://images.unsplash.com/photo-1558591710-4b4a1ae0f04d?auto=format&fit=crop&q=80&w=800" class="img-fluid rounded" alt="Factory">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="section-padding bg-light-gray">
        <div class="container">
            <div class="row g-5">
                <div class="col-lg-4">
                    <h2 class="fw-bold lang-en">Why Partner With Us?</h2>
                    <h2 class="fw-bold lang-zh">為何選擇華源？</h2>
                    <div class="bg-gold mt-3" style="width: 50px; height: 3px;"></div>
                </div>
                <div class="col-lg-8">
                    <div class="row g-4">
                        <div class="col-md-6">
                            <div class="d-flex align-items-start">
                                <i class="fa-solid fa-leaf feature-icon-small"></i>
                                <div>
                                    <h6 class="fw-bold lang-en">Sustainability</h6><h6 class="fw-bold lang-zh">永續面料</h6>
                                    <p class="small text-muted lang-zh">提供有機棉與再生纖維等環保方案。</p>
                                </div>
                            </div>
                        </div>
                        <div class="col-md-6">
                            <div class="d-flex align-items-start">
                                <i class="fa-solid fa-check-double feature-icon-small"></i>
                                <div>
                                    <h6 class="fw-bold lang-en">Quality First</h6><h6 class="fw-bold lang-zh">品質至上</h6>
                                    <p class="small text-muted lang-zh">嚴格的三道品檢工序，確保零瑕疵交貨。</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="section-padding bg-dark text-white text-center">
        <div class="container">
            <h2 class="fw-bold mb-5 lang-en">Get In Touch</h2>
            <h2 class="fw-bold mb-5 lang-zh">與我們聯絡</h2>
            <div class="row g-4">
                <div class="col-md-4">
                    <div class="contact-box">
                        <i class="fa fa-map-marker-alt text-gold mb-4 fa-2x"></i>
                        <h5 class="fw-bold mb-3 lang-en">Office Address</h5><h5 class="fw-bold mb-3 lang-zh">辦事處地址</h5>
                        <p class="address-text">
                            1802 Million Fortune Industrial Centre,<br>
                            34-36 Chai Wan Kok Street,<br>
                            Tsuen Wan, New Territories, Hong Kong
                        </p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="contact-box">
                        <i class="fa fa-envelope text-gold mb-4 fa-2x"></i>
                        <h5 class="fw-bold mb-3">Email</h5>
                        <p class="fs-5"><a href="mailto:wicky@wellyuen.com.hk" class="text-white-50 text-decoration-none">wicky@wellyuen.com.hk</a></p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="contact-box">
                        <i class="fa fa-phone text-gold mb-4 fa-2x"></i>
                        <h5 class="fw-bold mb-3 lang-en">Call Us</h5><h5 class="fw-bold mb-3 lang-zh">致電我們</h5>
                        <p class="fs-5 text-white-50">(+852) 2611 3201</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <footer class="py-4 bg-black text-center text-white-50 border-top border-secondary">
        <div class="container">
            <p class="small mb-0">© 1991-2026 Well Yuen Garments Ltd. | BSCI & SA8000 Certified Manufacturer</p>
        </div>
    </footer>

    <script>
        function setLanguage(lang) {
            document.documentElement.setAttribute('lang', lang);
            document.body.setAttribute('lang', lang);
            document.getElementById('btn-en').classList.toggle('active', lang === 'en');
            document.getElementById('btn-zh').classList.toggle('active', lang === 'zh');
            localStorage.setItem('preferred_lang', lang);
        }
        window.onload = () => {
            const savedLang = localStorage.getItem('preferred_lang') || 'en';
            setLanguage(savedLang);
        };
    </script>
</body>
</html>
