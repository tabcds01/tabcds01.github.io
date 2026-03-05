<!DOCTYPE html>
<html lang="zh-Hant">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Well Yuen Garments Ltd | 華源製衣有限公司</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@300;400;700&family=Plus+Jakarta+Sans:wght@300;400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --bg-dark: #1e2229;
            --accent-gold: #c5a059;
            --white: #ffffff;
            --text-gray: #777;
        }

        body { 
            font-family: 'Plus Jakarta Sans', 'Noto Sans TC', sans-serif; 
            background-color: #ffffff;
            margin: 0;
        }

        /* --- 頂部導航欄 (NavBar) --- */
        .navbar {
            background-color: var(--bg-dark);
            padding: 15px 0;
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }
        .navbar-brand { display: flex; align-items: center; }
        .navbar-brand img { height: 45px; margin-right: 15px; }
        .brand-text { color: white; line-height: 1.2; border-left: 1px solid #555; padding-left: 15px; }
        .brand-text .en { font-weight: 700; font-size: 1.1rem; }
        .brand-text .zh { font-size: 0.9rem; font-weight: 400; }
        
        .lang-switch { color: rgba(255,255,255,0.7); font-size: 0.85rem; }
        .lang-switch span { margin: 0 10px; cursor: pointer; transition: 0.3s; }
        .lang-switch span:hover { color: var(--accent-gold); }

        /* --- Hero Section (大圖背景 + 置中內容) --- */
        .hero-section {
            height: 70vh; /* 縮小高度，確保一開網頁即見全貌 */
            min-height: 550px;
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), 
                        url('https://images.unsplash.com/photo-1558591710-4b4a1ae0f04d?q=80&w=2000&auto=format&fit=crop') center/cover;
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
        }

        .hero-content { z-index: 5; }
        .hero-logo-large { width: 100px; margin-bottom: 20px; filter: drop-shadow(0 0 10px rgba(0,0,0,0.5)); }
        .hero-title-en { font-size: 3.2rem; font-weight: 700; margin-bottom: 5px; letter-spacing: 1px; }
        .hero-title-zh { font-size: 2.8rem; font-weight: 700; margin-bottom: 25px; }
        .hero-description { font-size: 1rem; opacity: 0.9; line-height: 1.6; max-width: 800px; margin: 0 auto 30px; }
        
        .btn-contact {
            background-color: var(--accent-gold);
            color: white;
            border: none;
            padding: 12px 35px;
            font-weight: 700;
            border-radius: 50px;
            text-decoration: none;
            transition: 0.3s;
        }
        .btn-contact:hover { background-color: #a8884a; color: white; transform: translateY(-3px); }

        /* --- 右下角浮動圖片 --- */
        .floating-window {
            position: absolute;
            bottom: -50px;
            right: 5%;
            width: 380px;
            background: white;
            padding: 8px;
            box-shadow: 0 15px 40px rgba(0,0,0,0.2);
            z-index: 10;
        }
        .floating-window img { width: 100%; display: block; }

        /* --- 下方詳情區塊 (About & Product) --- */
        .info-section { padding: 100px 0 60px; }
        .section-title { font-size: 1.8rem; font-weight: 700; color: #111; margin-bottom: 10px; }
        .section-subtitle { font-size: 1.2rem; color: #444; margin-bottom: 25px; }
        .gold-line { width: 40px; height: 2px; background: var(--accent-gold); margin-bottom: 25px; }
        .info-text { color: var(--text-gray); font-size: 0.95rem; line-height: 1.8; }
        
        .expertise-list { list-style: none; padding: 0; display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
        .expertise-list li { color: #333; font-size: 0.95rem; display: flex; align-items: center; }
        .expertise-list li::before { content: "•"; color: var(--accent-gold); font-weight: bold; margin-right: 10px; }

        /* --- 聯絡資訊區塊 (包含完整地址) --- */
        .footer-info { background: #f9f9f9; padding: 60px 0; border-top: 1px solid #eee; }
        .address-text { font-size: 0.95rem; color: #555; line-height: 1.8; }
        .icon-gold { color: var(--accent-gold); margin-right: 10px; width: 20px; text-align: center; }

        footer { background: #000; color: #444; padding: 25px 0; text-align: center; font-size: 0.8rem; }

        @media (max-width: 991px) {
            .floating-window { display: none; }
            .hero-title-en { font-size: 2.2rem; }
            .hero-title-zh { font-size: 1.8rem; }
            .expertise-list { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>

    <nav class="navbar fixed-top">
        <div class="container">
            <a class="navbar-brand" href="#">
                <img src="https://i.ibb.co/3W6qWbH/wy-logo-fixed.png" alt="Well Yuen Logo">
                <div class="brand-text">
                    <div class="en">WELL YUEN Garments</div>
                    <div class="zh">華源製衣有限公司</div>
                </div>
            </a>
            <div class="ms-auto lang-switch">
                <span>EN</span> | <span>中文</span>
            </div>
        </div>
    </nav>

    <header class="hero-section">
        <div class="hero-content container">
            <img src="https://i.ibb.co/3W6qWbH/wy-logo-fixed.png" alt="Well Yuen Logo" class="hero-logo-large">
            <h1 class="hero-title-en">WELL YUEN Garments</h1>
            <h2 class="hero-title-zh">華源製衣有限公司</h2>
            
            <div class="hero-description">
                Looking for the right factory? Established in 1991. <br>
                Over 30 years of manufacturing excellence for global brands. <br>
                華源製衣有限公司成立於 1991 年。 <br>
                嚴至30年度大年的成衣庫經驗性實為有的品牌。
            </div>
            
            <a href="#contact" class="btn-contact">CONTACT US NOW</a>
        </div>

        <div class="floating-window">
            <img src="https://images.unsplash.com/photo-1556761175-b413da4baf72?q=80&w=800&auto=format&fit=crop" alt="Production Line">
        </div>
    </header>

    <section class="info-section container">
        <div class="row g-5">
            <div class="col-lg-6">
                <h3 class="section-title">Heritage in Craftsmanship</h3>
                <h4 class="section-subtitle">About Us</h4>
                <div class="gold-line"></div>
                <p class="info-text">
                    WELL YUEN Garments Established in 1991. Over 30 years of manufacturing excellence for global brands. 
                    Inowing for the quality of our craftsmanship and dedication to social compliance. 
                    We serve as a reliable partner in the global supply chain.
                </p>
            </div>

            <div class="col-lg-6">
                <h3 class="section-title">Product Expertise</h3>
                <div class="gold-line"></div>
                <ul class="expertise-list">
                    <li>Belliffing Brand</li>
                    <li>Farane Expertise</li>
                    <li>High Quality Sarnes</li>
                    <li>Product Expertise</li>
                    <li>Knitting Mastery</li>
                    <li>Global Compliance</li>
                </ul>
            </div>
        </div>
    </section>

    <section id="contact" class="footer-info">
        <div class="container">
            <div class="row">
                <div class="col-md-6">
                    <h5 class="fw-bold mb-4">Contact Information</h5>
                    <div class="address-text">
                        <p><i class="fa-solid fa-location-dot icon-gold"></i> 
                            1802 Million Fortune Industrial Centre, <br>
                            34-36 Chai Wan Kok Street, Tsuen Wan, <br>
                            New Territories, Hong Kong
                        </p>
                        <p><i class="fa-solid fa-phone icon-gold"></i> (+852) 2611 3201</p>
                        <p><i class="fa-solid fa-envelope icon-gold"></i> wicky@wellyuen.com.hk</p>
                    </div>
                </div>
                <div class="col-md-6 text-md
