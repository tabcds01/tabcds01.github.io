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
            --primary-dark: #1a1c20;
            --accent-gold: #c5a059;
            --overlay: rgba(0, 0, 0, 0.55); 
        }

        body { font-family: 'Plus Jakarta Sans', 'Noto Sans TC', sans-serif; background-color: #fdfdfd; }
        
        [lang="en"] .lang-zh { display: none !important; }
        [lang="zh"] .lang-en { display: none !important; }

        /* 頂部導航欄 - 還原圖示設計 */
        .navbar { 
            background: rgba(26, 28, 32, 0.95); 
            border-bottom: 1px solid rgba(197, 160, 89, 0.3);
            padding: 15px 0;
        }
        .navbar-brand img { height: 40px; margin-right: 15px; }
        .brand-text-box { border-left: 1px solid #666; padding-left: 15px; color: white; line-height: 1.2; }
        .lang-switch .btn { color: #fff; font-size: 0.8rem; opacity: 0.7; }
        .lang-switch .btn.active { opacity: 1; color: var(--accent-gold); font-weight: bold; }

        /* Hero 主視覺 - 完全還原圖示版面 */
        .hero-section { 
            height: 75vh; /* 縮小高度，確保一打開就看到完整 Logo */
            position: relative;
            background: linear-gradient(var(--overlay), var(--overlay)), 
                        url('https://i.postimg.cc/wT6Bwt7T/WY-pic.jpg');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            color: white;
            overflow: hidden;
        }

        .hero-main-content { position: relative; z-index: 2; text-align: center; width: 100%; }
        .hero-logo-center { width: 120px; margin-bottom: 20px; }
        .hero-title { font-size: 3.5rem; font-weight: 700; letter-spacing: 2px; margin-bottom: 10px; }
        .hero-subtitle { font-size: 1.2rem; opacity: 0.9; margin-bottom: 30px; }

        /* 右下角浮動圖片 - 還原圖示特色 */
        .hero-floating-card {
            position: absolute;
            right: 5%;
            bottom: -50px; /* 跨越到下一個區塊的視覺感 */
            width: 380px;
            background: white;
            padding: 10px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
            z-index: 3;
            border-radius: 2px;
        }
        .hero-floating-card img { width: 100%; display: block; }

        /* 內容區塊 */
        .section-padding { padding: 100px 0; }
        .content-heading { border-bottom: 2px solid var(--accent-gold); display: inline-block; margin-bottom: 30px; padding-bottom: 10px; }
        
        /* 聯絡資訊 - 補完完整地址 */
        .contact-section { background: #1a1c20; color: white; }
        .address-box { line-height: 1.8; color: #aaa; font-size: 0.95rem; }
        .btn-gold-action { 
            background: var(--accent-gold); 
            color: white; 
            padding: 12px 35px; 
            text-decoration: none; 
            font-weight: bold;
            display: inline-block;
            transition: 0.3s;
        }
        .btn-gold-action:hover { background: #a8884a; transform: translateY(-3px); color: white; }

        @media (max-width: 992px) {
            .hero-floating-card { display: none; } /* 手機端隱藏浮動圖避免遮擋 */
            .hero-title { font-size: 2.2rem; }
        }
    </style>
</head>
<body lang="en">

    <nav class="navbar navbar-expand-lg navbar-dark fixed-top">
        <div class="container">
            <a class="navbar-brand d-flex align-items-center" href="#">
                <img src="https://i.ibb.co/3W6qWbH/wy-logo-fixed.png" alt="Logo">
                <div class="brand-text-box">
                    <div class="fw-bold">WELL YUEN</div>
                    <div class="small fw-light">Garments Ltd.</div>
                </div>
            </a>
            <div class="ms-auto lang-switch">
                <button id="btn-en" class="btn active" onclick="setLanguage('en')">EN</button>
                <span class="text-white-50">|</span>
                <button id="btn-zh" class="btn" onclick="setLanguage('zh')">中文</button>
            </div>
        </div>
    </nav>

    <header class="hero-section">
        <div class="container hero-main-content">
            <img src="https://i.ibb.co/3W6qWbH/wy-logo-fixed.png" alt="Well Yuen" class="hero-logo-center">
            
            <div class="lang-en">
                <h1 class="hero-title">WELL YUEN Garments</h1>
                <h2 class="hero-subtitle">華源製衣有限公司</h2>
                <p class="mb-4 text-white-50">Established in 1991. Excellence in Global Apparel Manufacturing.</p>
                <a href="#contact" class="btn-gold-action">CONTACT US NOW</a>
            </div>
            
            <div class="lang-zh">
                <h1 class="hero-title">華源製衣有限公司</h1>
                <h2 class="hero-subtitle">WELL YUEN Garments Ltd.</h2>
                <p class="mb-4 text-white-50">始於 1991 年。為全球品牌提供卓越的成衣製造服務。</p>
                <a href="#contact" class="btn-gold-action">立即洽詢</a>
            </div>
        </div>

        <div class="hero-floating-card d-none d-lg-block">
            <img src="https://images.unsplash.com/photo-1558591710-4b4a1ae0f04d?auto=format&fit=crop&q=80&w=600" alt="Factory Interior">
        </div>
    </header>

    <section class="section-padding">
        <div class="container">
            <div class="row">
                <div class="col-lg-7">
                    <h3 class="content-heading lang-en">Heritage in Craftsmanship</h3>
                    <h3 class="content-heading lang-zh">三十載匠心工藝</h3>
                    <div class="lang-en">
                        <p class="lead">Over 30 years of manufacturing excellence for global brands.</p>
                        <p>Well Yuen Garments has been a cornerstone of the industry since 1991. We combine traditional tailoring with modern automation to deliver garments that meet the highest international standards.</p>
                    </div>
                    <div class="lang-zh">
                        <p class="lead">我們為全球品牌提供超過 30 年的卓越製造服務。</p>
                        <p>華源製衣自 1991 年成立以來，一直是服裝行業的領先者。我們將傳統裁剪工藝與現代自動化生產相結合，確保每一件產品都符合國際最高品質標準。</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="section-padding contact-section">
        <div class="container">
            <div class="row g-5">
                <div class="col-md-6">
                    <h4 class="text-gold mb-4 lang-en">Contact Information</h4>
                    <h4 class="text-gold mb-4 lang-zh">聯絡資訊</h4>
                    <div class="address-box">
                        <p><i class="fa fa-map-marker-alt text-gold me-3"></i> 
                            <strong>Address:</strong><br>
                            1802 Million Fortune Industrial Centre,<br>
                            34-36 Chai Wan Kok Street,<br>
                            Tsuen Wan, New Territories, Hong Kong
                        </p>
                        <p><i class="fa fa-envelope text-gold me-3"></i> wicky@wellyuen.com.hk</p>
                        <p><i class="fa fa-phone text-gold me-3"></i> (+852) 2611 3201</p>
                    </div>
                </div>
                <div class="col-md-6 text-center text-md-end d-flex align-items-center justify-content-center">
                    <div class="border border-secondary p-5 w-100">
                        <h5 class="lang-en">Social Compliance</h5>
                        <h5 class="lang-zh">國際生產合規</h5>
                        <p class="text-gold fw-bold fs-3">BSCI & SA8000</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <footer class="py-3 bg-black text-center text-white-50 small">
        © 1991-2026 Well Yuen Garments Ltd. All Rights Reserved.
    </footer>

    <script>
        function setLanguage(lang) {
            document.documentElement.setAttribute('lang', lang);
            document.body.setAttribute('lang', lang);
            document.getElementById('btn-en').classList.toggle('active', lang === 'en');
            document.getElementById('btn-zh').classList.toggle('active', lang === 'zh');
        }
    </script>
</body>
</html>
