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
        .navbar { background: rgba(15, 17, 21, 0.98); padding: 15px 0; border-bottom: 1px solid rgba(255,255,255,0.1); }
        .navbar-brand img { height: 40px; margin-right: 15px; width: auto; }
        .lang-switch .btn { color: #fff; border: 1px solid rgba(255,255,255,0.3); font-size: 0.75rem; padding: 4px 10px; margin-left: 5px; border-radius: 0; }
        .lang-switch .btn.active { background: var(--accent-gold); border-color: var(--accent-gold); }

        /* Hero */
        .hero-section { 
            height: 100vh; 
            background: linear-gradient(var(--overlay-dark), var(--overlay-dark)), 
                        url('https://i.postimg.cc/wT6Bwt7T/WY-pic.jpg');
            background-size: cover; 
            background-position: center;
            background-attachment: fixed;
            display: flex; align-items: center; color: white;
            text-align: center;
        }
        .hero-content { width: 100%; max-width: 900px; margin: 0 auto; padding: 0 20px; }

        /* Section Commons */
        .section-padding { padding: 100px 0; }
        .bg-light-gray { background: #f9f9f9; }
        .text-gold { color: var(--accent-gold); }
        .bg-gold { background-color: var(--accent-gold); }

        /* About & Stats */
        .stat-item h3 { font-size: 2.8rem; color: var(--primary-dark); line-height: 1; margin-bottom: 5px; }
        .image-overlay-box { position: relative; padding-left: 20px; padding-bottom: 20px; }
        .image-overlay-box::before {
            content: ""; position: absolute; left: 0; bottom: 0;
            width: 80%; height: 80%; border: 5px solid var(--accent-gold); z-index: 0;
        }
        .image-overlay-box img { position: relative; z-index: 1; width: 100%; }

        /* Cards */
        .advantage-card { 
            background: #fff; padding: 45px 30px; height: 100%; 
            border-top: 4px solid var(--accent-gold); 
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
            transition: all 0.4s ease;
        }
        .product-card:hover { transform: translateY(-10px); border-color: var(--accent-gold); }
        
        /* Steps */
        .step-num { 
            width: 60px; height: 60px; background: var(--accent-gold); color: white; 
            border-radius: 50%; display: flex; align-items: center; justify-content: center; 
            margin: 0 auto 25px; font-weight: bold; font-size: 1.3rem; transition: 0.3s;
        }
        .step-item:hover .step-num { transform: scale(1.1); background: var(--primary-dark); }

        /* Banner */
        .parallax-banner {
            padding: 120px 0;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), 
                        url('https://images.unsplash.com/photo-1581091226825-a6a2a5aee158?auto=format&fit=crop&q=80&w=2000');
            background-size: cover; background-attachment: fixed; color: white; text-align: center;
        }

        .btn-gold { background: var(--accent-gold); color: white; border-radius: 0; padding: 15px 40px; font-weight: 600; border: none; transition: 0.3s; text-decoration: none; display: inline-block; }
        .btn-gold:hover { background: #b08d4a; color: white; transform: translateY(-3px); }

        /* Contact & Footer */
        .contact-box { background: rgba(255,255,255,0.05); padding: 40px; border: 1px solid rgba(255,255,255,0.1); transition: 0.3s; height: 100%; }
        .contact-box:hover { border-color: var(--accent-gold); background: rgba(255,255,255,0.08); }
        .footer-logo { height: 40px; width: auto; margin-bottom: 20px; }

        @media (max-width: 768px) {
            .hero-section h1 { font-size: 2.5rem !important; }
            .section-padding { padding: 60px 0; }
        }
    </style>
</head>
<body lang="en">

    <nav class="navbar navbar-expand-lg navbar-dark fixed-top">
        <div class="container">
            <a class="navbar-brand d-flex align-items-center" href="#">
                <img src="https://i.ibb.co/3W6qWbH/wy-logo-fixed.png" alt="Well Yuen Logo">
                <span class="lang-en fw-bold">WELL YUEN <small style="font-weight:300;">Garments</small></span>
                <span class="lang-zh fw-bold">華源製衣 <small style="font-weight:300;">有限公司</small></span>
            </a>
            <div class="ms-auto">
                <div class="lang-switch">
                    <button id="btn-en" class="btn" onclick="setLanguage('en')">EN</button>
                    <button id="btn-zh" class="btn" onclick="setLanguage('zh')">中文</button>
                </div>
            </div>
        </div>
    </nav>

    <header class="hero-section">
        <div class="hero-content">
            <div class="lang-en">
                <h1 class="display-2 fw-bold mb-4">Looking for the right factory?</h1>
                <p class="fs-4 text-white-75 mb-5">Established in 1991. Over 30 years of manufacturing excellence for global brands.</p>
                <a href="#contact" class="btn btn-gold">CONTACT US NOW</a>
            </div>
            <div class="lang-zh">
                <h1 class="display-3 fw-bold mb-4">正在尋找理想的工廠？</h1>
                <p class="fs-3 text-white-75 mb-5">華源製衣成立於 1991 年。三十載深耕，為全球品牌提供卓越製造服務。</p>
                <a href="#contact" class="btn btn-gold">立即聯絡我們</a>
            </div>
        </div>
    </header>

    <section id="about" class="section-padding bg-white">
        <div class="container">
            <div class="row align-items-center g-5">
                <div class="col-lg-6">
                    <div class="pe-lg-5">
                        <h6 class="text-gold fw-bold mb-3 lang-en">ESTABLISHED 1991</h6>
                        <h6 class="text-gold fw-bold mb-3 lang-zh">始於 1991 年</h6>
                        <h2 class="display-5 fw-bold mb-4 lang-en">30+ Years of Manufacturing Mastery</h2>
                        <h2 class="display-5 fw-bold mb-4 lang-zh">三十載匠心，定義卓越製造</h2>
                        <p class="text-muted mb-4 lang-en">
                            Well Yuen Garments has been a trusted partner for global brands for over three decades. From our headquarters in Hong Kong to our specialized production bases, we combine traditional craftsmanship with modern technology to deliver garments that meet the highest international standards.
                        </p>
                        <p class="text-muted mb-4 lang-zh">
                            華源製衣深耕服飾製造領域逾三十載。我們將傳統匠心工藝與現代化生產技術相結合，不僅是製造商，更是全球品牌最可靠的戰略合作夥伴，確保每一件產品都符合國際最高標準。
                        </p>
                        <div class="d-flex gap-5 mb-2 mt-5">
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
                </div>
                <div class="col-lg-6">
                    <div class="image-overlay-box">
                        <img src="https://images.unsplash.com/photo-1558591710-4b4a1ae0f04d?auto=format&fit=crop&q=80&w=800" class="img-fluid shadow-lg" alt="Factory">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="products" class="section-padding bg-light-gray">
        <div class="container">
            <div class="text-center mb-5">
                <h2 class="fw-bold display-6 lang-en">Product Expertise</h2>
                <h2 class="fw-bold display-6 lang-zh">核心產品範圍</h2>
                <div class="mx-auto bg-gold mt-3" style="width: 60px; height: 3px;"></div>
            </div>
            <div class="row g-4">
                <div class="col-md-4">
                    <div class="advantage-card product-card text-center">
                        <i class="fa-solid fa-vest-patches text-gold fa-3x mb-4"></i>
                        <h4 class="fw-bold lang-en">Denim & Woven</h4>
                        <h4 class="fw-bold lang-zh">牛仔與梭織</h4>
                        <p class="small text-muted lang-en">Specializing in premium jeans, jackets, and workwear with advanced washing & distressing effects.</p>
                        <p class="small text-muted lang-zh">專精於高品質牛仔褲、夾克及梭織工裝，具備先進的水洗、噴砂與特殊染色工藝。</p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="advantage-card product-card text-center">
                        <i class="fa-solid fa-shirt text-gold fa-3x mb-4"></i>
                        <h4 class="fw-bold lang-en">Knitwear & Sweaters</h4>
                        <h4 class="fw-bold lang-zh">針織與毛衫</h4>
                        <p class="small text-muted lang-en">Expertise in multi-gauge knitting, from fine cardigans to chunky sweaters, using automated machinery.</p>
                        <p class="small text-muted lang-zh">精通各種針寸的毛衫製造，從輕盈開衫到粗針毛衣，均採用自動化電腦橫機生產。</p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="advantage-card product-card text-center">
                        <i class="fa-solid fa-person-running text-gold fa-3x mb-4"></i>
                        <h4 class="fw-bold lang-en">Active & Casual</h4>
                        <h4 class="fw-bold lang-zh">運動與休閒</h4>
                        <p class="small text-muted lang-en">Functional hoodies, polo shirts, and technical jerseys focused on durability and modern fit.</p>
                        <p class="small text-muted lang-zh">涵蓋連帽衫、POLO 衫及機能性面料產品，注重耐穿性、舒適感與時尚剪裁。</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="section-padding bg-white">
        <div class="container text-center">
            <h2 class="fw-bold mb-5 lang-en">How We Work</h2>
            <h2 class="fw-bold mb-5 lang-zh">合作流程</h2>
            <div class="row g-4">
                <div class="col-md-3 step-item">
                    <div class="step-num">01</div>
                    <h5 class="fw-bold lang-en">Inquiry</h5><h5 class="fw-bold lang-zh">需求洽談</h5>
                    <p class="small text-muted lang-en">Send us your designs and technical requirements.</p>
                    <p class="small text-muted lang-zh">提供設計稿與生產技術要求。</p>
                </div>
                <div class="col-md-3 step-item">
                    <div class="step-num">02</div>
                    <h5 class="fw-bold lang-en">Sampling</h5><h5 class="fw-bold lang-zh">樣板開發</h5>
                    <p class="small text-muted lang-en">Precise prototype development for your approval.</p>
                    <p class="small text-muted lang-zh">精準打樣，確保版型細節符合標準。</p>
                </div>
                <div class="col-md-3 step-item">
                    <div class="step-num">03</div>
                    <h5 class="fw-bold lang-en">Production</h5><h5 class="fw-bold lang-zh">批量生產</h5>
                    <p class="small text-muted lang-en">Scale manufacturing in our specialized units.</p>
                    <p class="small text-muted lang-zh">由專業生產線進行大規模高效生產。</p>
                </div>
                <div class="col-md-3 step-item">
                    <div class="step-num">04</div>
                    <h5 class="fw-bold lang-en">Delivery</h5><h5 class="fw-bold lang-zh">品檢與交貨</h5>
                    <p class="small text-muted lang-en">Strict quality control and global shipping.</p>
                    <p class="small text-muted lang-zh">經嚴格品控後，配送至全球指定地點。</p>
                </div>
            </div>
        </div>
    </section>

    <section class="parallax-banner">
        <div class="container">
            <h2 class="display-4 fw-bold mb-4 lang-en">4,000 SQM Industrial Complex</h2>
            <h2 class="display-4 fw-bold mb-4 lang-zh">4,000 平方米現代化工業基地</h2>
            <div class="row mt-5">
                <div class="col-md-6 text-md-end border-md-end px-4 mb-4 mb-md-0">
                    <h4 class="text-gold lang-en">Guangdong Factory</h4><h4 class="text-gold lang-zh">廣東工廠</h4>
                    <p class="lang-en text-white-75">Denims and Cardigans specialists</p>
                    <p class="lang-zh text-white-75">牛仔及針織開衫專業生產中心</p>
                </div>
                <div class="col-md-6 text-md-start px-4">
                    <h4 class="text-gold lang-en">Fujian Factory</h4><h4 class="text-gold lang-zh">福建分廠</h4>
                    <p class="lang-en text-white-75">Focused on specialized Woven and Knits</p>
                    <p class="lang-zh text-white-75">專注於各類技術性梭織與針織產品</p>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="section-padding bg-dark text-white text-center">
        <div class="container">
            <h2 class="fw-bold mb-5 lang-en">Contact Our Team</h2>
            <h2 class="fw-bold mb-5 lang-zh">聯絡我們</h2>
            <div class="row g-4 justify-content-center">
                <div class="col-md-4">
                    <div class="contact-box">
                        <i class="fa fa-map-marker-alt text-gold fa-2x mb-3"></i>
                        <h5 class="lang-en">Hong Kong Office</h5><h5 class="lang-zh">香港辦事處</h5>
                        <p class="small text-white-50">1802 Million Fortune Industrial Centre,<br>34-36 Chai Wan Kok Street,<br>Tsuen Wan, Hong Kong</p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="contact-box">
                        <i class="fa fa-envelope text-gold fa-2x mb-3"></i>
                        <h5>Email</h5>
                        <a href="mailto:wicky@wellyuen.com.hk" class="text-decoration-none text-white-50">wicky@wellyuen.com.hk</a>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="contact-box">
                        <i class="fa fa-phone text-gold fa-2x mb-3"></i>
                        <h5 class="lang-en">Phone</h5><h5 class="lang-zh">電話</h5>
                        <a href="tel:+85226113201" class="text-decoration-none text-white-50">(+852) 2611 3201</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <footer class="py-5 bg-black text-white-50 text-center">
        <div class="container">
            <img src="https://i.ibb.co/3W6qWbH/wy-logo-fixed.png" alt="Well Yuen Logo" class="footer-logo">
            <p class="small mb-1">Well Yuen Garments Ltd. | 華源製衣有限公司</p>
            <p class="small mb-0">© 1991 - 2026 | BSCI & SA8000 Certified Manufacturer</p>
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
