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

        .navbar { background: rgba(15, 17, 21, 0.98); padding: 15px 0; border-bottom: 1px solid rgba(255,255,255,0.1); }
        .navbar-brand img { height: 40px; margin-right: 15px; width: auto; }
        .lang-switch .btn { color: #fff; border: 1px solid rgba(255,255,255,0.3); font-size: 0.75rem; padding: 4px 10px; margin-left: 5px; border-radius: 0; }
        .lang-switch .btn.active { background: var(--accent-gold); border-color: var(--accent-gold); }

        .hero-section { 
            height: 100vh; 
            background: linear-gradient(var(--overlay-dark), var(--overlay-dark)), 
                        url('https://i.postimg.cc/wT6Bwt7T/WY-pic.jpg');
            background-size: cover; 
            background-position: bottom center;
            background-attachment: fixed;
            display: flex; align-items: center; color: white;
            text-align: center;
        }

        .hero-content { width: 100%; max-width: 900px; margin: 0 auto; padding: 0 20px; }

        @media (max-width: 768px) {
            .hero-section h1 { font-size: 2.5rem !important; }
            .hero-section p { font-size: 1.1rem !important; }
        }

        .section-padding { padding: 90px 0; }
        .bg-light-gray { background: #f9f9f9; }
        .text-gold { color: var(--accent-gold); }

        .advantage-card { background: #fff; padding: 40px; height: 100%; border-top: 4px solid var(--accent-gold); box-shadow: 0 10px 30px rgba(0,0,0,0.05); }
        
        .step-num { width: 50px; height: 50px; background: var(--accent-gold); color: white; border-radius: 50%; display: flex; align-items: center; justify-content: center; margin: 0 auto 20px; font-weight: bold; font-size: 1.2rem; }

        .parallax-banner {
            padding: 100px 0;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), 
                        url('https://images.unsplash.com/photo-1581091226825-a6a2a5aee158?auto=format&fit=crop&q=80&w=2000');
            background-size: cover; background-attachment: fixed; color: white; text-align: center;
        }

        .btn-gold { background: var(--accent-gold); color: white; border-radius: 0; padding: 15px 40px; font-weight: 600; border: none; transition: 0.3s; text-decoration: none; display: inline-block; }
        .btn-gold:hover { background: #b08d4a; color: white; transform: translateY(-3px); }

        .footer-logo { height: 35px; width: auto; margin-bottom: 15px; }
        
        .contact-box { background: rgba(255,255,255,0.05); padding: 40px; border: 1px solid rgba(255,255,255,0.1); transition: 0.3s; height: 100%; }
        .contact-box:hover { border-color: var(--accent-gold); }
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

    <section class="section-padding">
        <div class="container text-center">
            <h2 class="fw-bold mb-5 lang-en">How We Work</h2>
            <h2 class="fw-bold mb-5 lang-zh">合作流程</h2>
            <div class="row g-4">
                <div class="col-md-3">
                    <div class="step-num">01</div>
                    <h5 class="lang-en">Inquiry</h5><h5 class="lang-zh">需求洽談</h5>
                    <p class="small text-muted lang-en">Send us your designs and requirements.</p>
                    <p class="small text-muted lang-zh">提供設計稿與生產需求。</p>
                </div>
                <div class="col-md-3">
                    <div class="step-num">02</div>
                    <h5 class="lang-en">Sampling</h5><h5 class="lang-zh">樣板開發</h5>
                    <p class="small text-muted lang-en">Prototype development with precision.</p>
                    <p class="small text-muted lang-zh">精準打樣，確保版型與細節。</p>
                </div>
                <div class="col-md-3">
                    <div class="step-num">03</div>
                    <h5 class="lang-en">Production</h5><h5 class="lang-zh">批量生產</h5>
                    <p class="small text-muted lang-en">Scale production in specialized units.</p>
                    <p class="small text-muted lang-zh">由專業工廠產線進行大規模生產。</p>
                </div>
                <div class="col-md-3">
                    <div class="step-num">04</div>
                    <h5 class="lang-en">Delivery</h5><h5 class="lang-zh">品檢與交貨</h5>
                    <p class="small text-muted lang-en">Global shipping with strict QC.</p>
                    <p class="small text-muted lang-zh">嚴格品控後，配送至全球指定地點。</p>
                </div>
            </div>
        </div>
    </section>

    <section class="section-padding bg-light-gray">
        <div class="container">
            <div class="row g-5 align-items-center">
                <div class="col-lg-6">
                    <div class="lang-en">
                        <h2 class="display-5 fw-bold mb-4">Our Advantage</h2>
                        <p class="text-muted">High quality garments at competitive prices. Our facilities cover most woven and knit items.</p>
                    </div>
                    <div class="lang-zh">
                        <h2 class="display-4 fw-bold mb-4">我們的優勢</h2>
                        <p class="text-muted">致力於以極具競爭力的價格提供高品質服飾。工廠產線全面，涵蓋大多數梭織與針織品類。</p>
                    </div>
                </div>
                <div class="col-lg-6">
                    <div class="row g-4">
                        <div class="col-md-6">
                            <div class="advantage-card">
                                <h5 class="fw-bold lang-en">Comprehensive</h5><h5 class="fw-bold lang-zh">品類全面</h5>
                                <p class="small text-muted lang-en">Jackets, Jeans, Sweaters & more</p>
                                <p class="small text-muted lang-zh">夾克、牛仔、毛衣等各類服裝</p>
                            </div>
                        </div>
                        <div class="col-md-6">
                            <div class="advantage-card">
                                <h5 class="fw-bold lang-en">Experienced</h5><h5 class="fw-bold lang-zh">專業團隊</h5>
                                <p class="small text-muted lang-en">Skilled merchandiser team</p>
                                <p class="small text-muted lang-zh">資深跟單團隊，精通國際市場需求</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="parallax-banner">
        <div class="container">
            <h2 class="display-4 fw-bold mb-4 lang-en">4,000 SQM Industrial Complex</h2>
            <h2 class="display-4 fw-bold mb-4 lang-zh">4,000 平方米現代化工業園區</h2>
            <div class="row mt-5">
                <div class="col-md-6 text-md-end border-md-end px-4">
                    <h4 class="text-gold lang-en">Guangdong Factory</h4><h4 class="text-gold lang-zh">廣東工廠</h4>
                    <p class="lang-en">Denims and Cardigans specialists</p>
                    <p class="lang-zh">牛仔及針織開衫專業生產基地</p>
                </div>
                <div class="col-md-6 text-md-start px-4">
                    <h4 class="text-gold lang-en">Fujian Factory</h4><h4 class="text-gold lang-zh">福建工廠</h4>
                    <p class="lang-en">Focused on specialized Woven and Knits</p>
                    <p class="lang-zh">分廠專注各類梭織與針織產品</p>
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
                        <p class="small text-white-50">1802 Million Fortune Industrial Centre,<br>34-36 Chai Wan Kok Street,<br>Tsuen Wan, New Territories, Hong Kong</p>
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
