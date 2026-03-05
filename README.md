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
            --overlay-dark: rgba(0, 0, 0, 0.6); 
        }

        body { font-family: 'Plus Jakarta Sans', 'Noto Sans TC', sans-serif; color: #333; overflow-x: hidden; }
        html { scroll-behavior: smooth; }
        
        [lang="en"] .lang-zh { display: none !important; }
        [lang="zh"] .lang-en { display: none !important; }

        /* Navbar 優化：半透明黑 */
        .navbar { background: rgba(15, 17, 21, 0.95); padding: 12px 0; border-bottom: 1px solid rgba(255,255,255,0.1); }
        .navbar-brand img { height: 35px; margin-right: 12px; }
        .lang-switch .btn { color: #fff; border: 1px solid rgba(255,255,255,0.3); font-size: 0.7rem; padding: 2px 8px; border-radius: 0; }
        .lang-switch .btn.active { background: var(--accent-gold); border-color: var(--accent-gold); }

        /* Hero Section 優化：縮小高度，強化 Logo 展示 */
        .hero-section { 
            height: 75vh; /* 縮小高度，讓下方內容能露出一點，引導下滑 */
            min-height: 500px;
            background: linear-gradient(var(--overlay-dark), var(--overlay-dark)), 
                        url('https://i.postimg.cc/wT6Bwt7T/WY-pic.jpg');
            background-size: cover; 
            background-position: center 30%; /* 調整圖片中心點 */
            display: flex; align-items: center; color: white;
            text-align: center;
            padding-top: 80px; /* 為導航欄留空間 */
        }
        
        .hero-logo-big { 
            width: 120px; 
            margin-bottom: 25px; 
            filter: drop-shadow(0 0 10px rgba(0,0,0,0.5));
        }

        .hero-content { width: 100%; max-width: 900px; margin: 0 auto; padding: 0 20px; }
        .hero-content h1 { letter-spacing: 1px; }

        /* 通用樣式 */
        .section-padding { padding: 80px 0; }
        .bg-light-gray { background: #f8f9fa; }
        .text-gold { color: var(--accent-gold); }
        .btn-gold { background: var(--accent-gold); color: white; border-radius: 4px; padding: 12px 35px; font-weight: 600; text-decoration: none; display: inline-block; transition: 0.3s; border: none; }
        .btn-gold:hover { background: #b08d4a; color: white; transform: translateY(-2px); box-shadow: 0 5px 15px rgba(197, 160, 89, 0.3); }

        /* 關於我們區塊圖片裝飾 */
        .image-overlay-box { position: relative; padding: 10px; }
        .image-overlay-box::before {
            content: ""; position: absolute; left: -10px; bottom: -10px;
            width: 70%; height: 70%; border: 4px solid var(--accent-gold); z-index: 0;
        }
        .image-overlay-box img { position: relative; z-index: 1; width: 100%; box-shadow: 0 15px 35px rgba(0,0,0,0.15); }

        /* 產品卡片 */
        .product-card { 
            background: #fff; padding: 40px 25px; border-radius: 8px;
            border: 1px solid #eee; transition: 0.3s; height: 100%;
        }
        .product-card:hover { border-color: var(--accent-gold); transform: translateY(-5px); box-shadow: 0 10px 25px rgba(0,0,0,0.05); }

        /* 底部 */
        .contact-box { background: rgba(255,255,255,0.05); padding: 30px; border-radius: 8px; border: 1px solid rgba(255,255,255,0.1); }
    </style>
</head>
<body lang="en">

    <nav class="navbar navbar-expand-lg navbar-dark fixed-top">
        <div class="container">
            <a class="navbar-brand d-flex align-items-center" href="#">
                <img src="https://i.ibb.co/3W6qWbH/wy-logo-fixed.png" alt="Well Yuen Logo">
                <div class="lh-1">
                    <div class="lang-en fw-bold mb-0">WELL YUEN <span class="fw-light">Garments</span></div>
                    <div class="lang-zh fw-bold mb-0">華源製衣 <span class="fw-light">有限公司</span></div>
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
            <img src="https://i.ibb.co/3W6qWbH/wy-logo-fixed.png" alt="Well Yuen" class="hero-logo-big">
            
            <div class="lang-en">
                <h1 class="display-4 fw-bold mb-3">WELL YUEN Garments Ltd.</h1>
                <p class="fs-5 text-white-75 mb-4 mx-auto" style="max-width: 700px;">
                    Over 30 years of manufacturing excellence for global brands. <br>Reliability and Quality since 1991.
                </p>
                <a href="#contact" class="btn btn-gold">GET A QUOTE</a>
            </div>
            
            <div class="lang-zh">
                <h1 class="display-4 fw-bold mb-3">華源製衣有限公司</h1>
                <p class="fs-4 text-white-75 mb-4">
                    三十載匠心製造，全球品牌的信賴夥伴。<br>始於 1991，專注高品質服飾生產。
                </p>
                <a href="#contact" class="btn btn-gold">立即洽詢</a>
            </div>
        </div>
    </header>

    <section id="about" class="section-padding bg-white">
        <div class="container">
            <div class="row align-items-center g-5">
                <div class="col-lg-6">
                    <h6 class="text-gold fw-bold mb-3 lang-en">OUR HERITAGE</h6>
                    <h6 class="text-gold fw-bold mb-3 lang-zh">關於我們</h6>
                    <h2 class="fw-bold mb-4 lang-en">Excellence in Craftsmanship</h2>
                    <h2 class="fw-bold mb-4 lang-zh">傳承三十載的精湛工藝</h2>
                    <p class="text-muted lang-en">Well Yuen Garments has been a cornerstone of the industry since 1991. We combine traditional tailoring with modern automation to deliver garments that meet the highest international standards.</p>
                    <p class="text-muted lang-zh">華源製衣自 1991 年成立以來，一直是服裝製造行業的基石。我們將傳統裁剪工藝與現代化自動化生產相結合，確保每一件產品都符合國際最高標準。</p>
                    
                    <div class="row mt-4 g-4">
                        <div class="col-6">
                            <h3 class="fw-bold text-gold mb-0">30+</h3>
                            <small class="text-muted lang-en">Years of Experience</small>
                            <small class="text-muted lang-zh">產業經驗</small>
                        </div>
                        <div class="col-6 border-start ps-4">
                            <h3 class="fw-bold text-gold mb-0">BSCI</h3>
                            <small class="text-muted lang-en">SA8000 Certified</small>
                            <small class="text-muted lang-zh">合規生產認證</small>
                        </div>
                    </div>
                </div>
                <div class="col-lg-6">
                    <div class="image-overlay-box">
                        <img src="https://images.unsplash.com/photo-1558591710-4b4a1ae0f04d?auto=format&fit=crop&q=80&w=800" alt="Factory Interior">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="products" class="section-padding bg-light-gray">
        <div class="container">
            <div class="text-center mb-5">
                <h2 class="fw-bold lang-en">Product Categories</h2>
                <h2 class="fw-bold lang-zh">核心產品類別</h2>
            </div>
            <div class="row g-4 text-center">
                <div class="col-md-4">
                    <div class="product-card">
                        <i class="fa-solid fa-vest text-gold fa-3x mb-4"></i>
                        <h4 class="fw-bold lang-en">Denim & Woven</h4>
                        <h4 class="fw-bold lang-zh">牛仔與梭織</h4>
                        <p class="small text-muted">Jeans, Jackets, Workwear</p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="product-card">
                        <i class="fa-solid fa-shirt text-gold fa-3x mb-4"></i>
                        <h4 class="fw-bold lang-en">Knitwear</h4>
                        <h4 class="fw-bold lang-zh">針織毛衫</h4>
                        <p class="small text-muted">Cardigans, Sweaters, Knits</p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="product-card">
                        <i class="fa-solid fa-person-running text-gold fa-3x mb-4"></i>
                        <h4 class="fw-bold lang-en">Activewear</h4>
                        <h4 class="fw-bold lang-zh">運動與休閒</h4>
                        <p class="small text-muted">Hoodies, T-Shirts, Polo</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="section-padding bg-dark text-white">
        <div class="container">
            <div class="row g-4">
                <div class="col-md-4">
                    <div class="contact-box">
                        <i class="fa fa-envelope text-gold mb-3 fa-lg"></i>
                        <h5 class="fw-bold">Email</h5>
                        <p class="small mb-0"><a href="mailto:wicky@wellyuen.com.hk" class="text-white-50 text-decoration-none">wicky@wellyuen.com.hk</a></p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="contact-box">
                        <i class="fa fa-phone text-gold mb-3 fa-lg"></i>
                        <h5 class="fw-bold lang-en">Contact</h5><h5 class="fw-bold lang-zh">聯絡電話</h5>
                        <p class="small mb-0 text-white-50">(+852) 2611 3201</p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="contact-box">
                        <i class="fa fa-location-dot text-gold mb-3 fa-lg"></i>
                        <h5 class="fw-bold lang-en">Office</h5><h5 class="fw-bold lang-zh">辦事處</h5>
                        <p class="small mb-0 text-white-50">Tsuen Wan, Hong Kong</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <footer class="py-4 bg-black text-center text-white-50">
        <div class="container">
            <p class="small mb-0">© 1991-2026 Well Yuen Garments Ltd. All Rights Reserved.</p>
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
