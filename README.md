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

        /* Hero Section - 縮小高度並強化 Logo */
        .hero-section { 
            height: 75vh; /* 縮小高度，讓首屏能看到下方內容標題 */
            min-height: 550px;
            background: linear-gradient(var(--overlay-dark), var(--overlay-dark)), 
                        url('https://i.postimg.cc/wT6Bwt7T/WY-pic.jpg');
            background-size: cover; 
            background-position: center 30%;
            display: flex; align-items: center; color: white;
            text-align: center;
            padding-top: 70px;
        }
        .hero-logo-big { width: 100px; margin-bottom: 20px; filter: drop-shadow(0 0 15px rgba(0,0,0,0.3)); }
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

        /* Feature List */
        .feature-icon-small { font-size: 1.5rem; color: var(--accent-gold); margin-right: 15px; }

        /* Steps */
        .step-num { 
            width: 50px; height: 50px; background: var(--accent-gold); color: white; 
            border-radius: 50%; display: flex; align-items: center; justify-content: center; 
            margin: 0 auto 20px; font-weight: bold;
        }

        /* Footer & Contact */
        .contact-box { background: rgba(255,255,255,0.05); padding: 35px; border: 1px solid rgba(255,255,255,0.1); border-radius: 5px; height: 100%; }
        .btn-gold { background: var(--accent-gold); color: white; border-radius: 0; padding: 14px 40px; font-weight: 600; border: none; transition: 0.3s; text-decoration: none; display: inline-block; }
        .btn-gold:hover { background: #b08d4a; color: white; transform: translateY(-3px); }

        @media (max-width: 768px) {
            .hero-section { height: 85vh; }
            .hero-content h1 { font-size: 2rem !important; }
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
                <p class="fs-5 text-white-75 mb-5">Since 1991. Professional Manufacturing Partner for Global Apparel Brands.</p>
                <a href="#contact" class="btn btn-gold">CONTACT US NOW</a>
            </div>
            <div class="lang-zh">
                <h1 class="display-3 fw-bold mb-3">華源製衣有限公司</h1>
                <p class="fs-4 text-white-75 mb-5">始於 1991 年。全球服飾品牌的專業製造合作夥伴。</p>
                <a href="#contact" class="btn btn-gold">立即聯絡我們</a>
            </div>
        </div>
    </header>

    <section id="about" class="section-padding bg-white">
        <div class="container">
            <div class="row align-items-center g-5">
                <div class="col-lg-6">
                    <h6 class="text-gold fw-bold mb-3 lang-en">ESTABLISHED 1991</h6>
                    <h6 class="text-gold fw-bold mb-3 lang-zh">始於 1991 年</h6>
                    <h2 class="display-5 fw-bold mb-4 lang-en">Mastery in Every Stitch</h2>
                    <h2 class="display-5 fw-bold mb-4 lang-zh">傳承三十載，定義卓越製造</h2>
                    <p class="text-muted mb-4 lang-en">Well Yuen Garments has been a trusted manufacturer for over 30 years. From our Hong Kong headquarters to our advanced production bases, we combine craftsmanship with modern technology.</p>
                    <p class="text-muted mb-4 lang-zh">華源製衣深耕行業逾三十載。從香港總部到現代化生產基地，我們將匠心工藝與尖端技術相結合，為全球客戶提供高品質的服裝解決方案。</p>
                    <div class="d-flex gap-5 mt-5">
                        <div class="stat-item">
                            <h3 class="fw-bold">35+</h3>
                            <small class="text-muted lang-en">Years Experience</small>
                            <small class="text-muted lang-zh">產業經驗</small>
                        </div>
                        <div class="stat-item border-start ps-4">
                            <h3 class="fw-bold text-gold">BSCI</h3>
                            <small class="text-muted lang-en">SA8000 Certified</small>
                            <small class="text-muted lang-zh">合規生產認證</small>
                        </div>
                    </div>
                </div>
                <div class="col-lg-6 text-center">
                    <div class="image-overlay-box">
                        <img src="https://images.unsplash.com/photo-1558591710-4b4a1ae0f04d?auto=format&fit=crop&q=80&w=800" class="img-fluid rounded" alt="Factory">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="products" class="section-padding bg-light-gray">
        <div class="container text-center">
            <h2 class="fw-bold mb-5 lang-en">Product Expertise</h2>
            <h2 class="fw-bold mb-5 lang-zh">核心產品範圍</h2>
            <div class="row g-4">
                <div class="col-md-4">
                    <div class="product-card">
                        <i class="fa-solid fa-vest-patches text-gold fa-3x mb-4"></i>
                        <h4 class="fw-bold lang-en">Denim & Woven</h4>
                        <h4 class="fw-bold lang-zh">丹寧與梭織</h4>
                        <p class="small text-muted">Jeans, Jackets, & Workwear with specialized washing effects.</p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="product-card">
                        <i class="fa-solid fa-shirt text-gold fa-3x mb-4"></i>
                        <h4 class="fw-bold lang-en">Knitwear</h4>
                        <h4 class="fw-bold lang-zh">針織毛衫</h4>
                        <p class="small text-muted">Multi-gauge sweaters and cardigans using automated machinery.</p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="product-card">
                        <i class="fa-solid fa-person-running text-gold fa-3x mb-4"></i>
                        <h4 class="fw-bold lang-en">Active & Casual</h4>
                        <h4 class="fw-bold lang-zh">運動與休閒</h4>
                        <p class="small text-muted">Performance hoodies, Polo shirts, and comfortable jerseys.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="section-padding bg-white">
        <div class="container">
            <div class="row g-5">
                <div class="col-lg-5">
                    <h2 class="fw-bold lang-en">Why Choose Us?</h2>
                    <h2 class="fw-bold lang-zh">為何選擇我們？</h2>
                    <p class="text-muted lang-en">We understand the requirements of modern global brands.</p>
                    <p class="text-muted lang-zh">我們深諳全球化品牌對品質與效率的要求。</p>
                </div>
                <div class="col-lg-7">
                    <div class="row g-4">
                        <div class="col-md-6">
                            <div class="d-flex align-items-start">
                                <i class="fa-solid fa-leaf feature-icon-small"></i>
                                <div><h6 class="fw-bold lang-en">Eco-Friendly</h6><h6 class="fw-bold lang-zh">永續發展</h6><p class="small text-muted lang-zh">提供環保面料選擇。</p></div>
                            </div>
                        </div>
                        <div class="col-md-6">
                            <div class="d-flex align-items-start">
                                <i class="fa-solid fa-boxes-stacked feature-icon-small"></i>
                                <div><h6 class="fw-bold lang-en">Flexible MOQ</h6><h6 class="fw-bold lang-zh">靈活訂量</h6><p class="small text-muted lang-zh">支持不同規模生產。</p></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="section-padding bg-light-gray text-center">
        <div class="container">
            <h2 class="fw-bold mb-5 lang-en">How We Work</h2>
            <h2 class="fw-bold mb-5 lang-zh">合作流程</h2>
            <div class="row g-4">
                <div class="col-md-3">
                    <div class="step-num">01</div>
                    <h6 class="fw-bold lang-en">Inquiry</h6><h6 class="fw-bold lang-zh">需求洽談</h6>
                </div>
                <div class="col-md-3">
                    <div class="step-num">02</div>
                    <h6 class="fw-bold lang-en">Sampling</h6><h6 class="fw-bold lang-zh">開發打樣</h6>
                </div>
                <div class="col-md-3">
                    <div class="step-num">03</div>
                    <h6 class="fw-bold lang-en">Production</h6><h6 class="fw-bold lang-zh">批量生產</h6>
                </div>
                <div class="col-md-3">
                    <div class="step-num">04</div>
                    <h6 class="fw-bold lang-en">Delivery</h6><h6 class="fw-bold lang-zh">品檢交貨</h6>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="section-padding bg-dark text-white text-center">
        <div class="container">
            <h2 class="fw-bold mb-5 lang-en">Contact Us</h2>
            <h2 class="fw-bold mb-5 lang-zh">聯絡我們</h2>
            <div class="row g-4">
                <div class="col-md-4">
                    <div class="contact-box">
                        <i class="fa fa-envelope text-gold mb-3"></i>
                        <p class="small mb-0">wicky@wellyuen.com.hk</p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="contact-box">
                        <i class="fa fa-phone text-gold mb-3"></i>
                        <p class="small mb-0">(+852) 2611 3201</p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="contact-box">
                        <i class="fa fa-location-dot text-gold mb-3"></i>
                        <p class="address-text text-white-50">
                            1802 Million Fortune Industrial Centre,<br>
                            34-36 Chai Wan Kok Street,<br>
                            Tsuen Wan, New Territories, Hong Kong
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <footer class="py-4 bg-black text-center text-white-50">
        <div class="container">
            <p class="small mb-0">© 1991-2026 Well Yuen Garments Ltd. | BSCI & SA8000 Certified</p>
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
