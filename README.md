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
            --primary-dark: #121418;
            --accent-gold: #c5a059;
            --text-gray: #888;
            --white: #ffffff;
        }

        body { 
            font-family: 'Plus Jakarta Sans', 'Noto Sans TC', sans-serif; 
            background-color: #fff; 
            color: #333;
            margin: 0;
        }

        /* 語系切換顯示邏輯 */
        [lang="en"] .lang-zh { display: none !important; }
        [lang="zh"] .lang-en { display: none !important; }

        /* --- 1. 頂部導航欄 (精簡化排版) --- */
        .navbar { 
            background: rgba(18, 20, 24, 0.98); 
            padding: 15px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
        }
        .navbar-brand { display: flex; align-items: center; }
        .brand-logo-icon { color: var(--accent-gold); font-size: 1.8rem; margin-right: 15px; }
        .brand-divider { height: 30px; width: 1px; background: #444; margin-right: 15px; }
        .brand-name-text { color: var(--white); line-height: 1.1; }
        .brand-name-text .main { font-weight: 700; font-size: 1.1rem; letter-spacing: 1px; }
        .brand-name-text .sub { font-size: 0.75rem; color: var(--text-gray); font-weight: 300; }

        .lang-link { color: rgba(255,255,255,0.6); text-decoration: none; font-size: 0.8rem; transition: 0.3s; padding: 0 10px; }
        .lang-link:hover, .lang-link.active { color: var(--accent-gold); }

        /* --- 2. Hero Section (高度縮小 + 置中 Logo + 右下浮動圖) --- */
        .hero-section { 
            height: 75vh; /* 縮小高度，確保一打開網址即見全貌 */
            min-height: 550px;
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), 
                        url('https://images.unsplash.com/photo-1558591710-4b4a1ae0f04d?q=80&w=2000&auto=format&fit=crop') center/cover;
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            overflow: hidden;
        }

        .hero-center-content { text-align: center; z-index: 10; max-width: 800px; }
        .hero-main-logo { font-size: 4.5rem; color: var(--accent-gold); margin-bottom: 20px; filter: drop-shadow(0 0 20px rgba(0,0,0,0.5)); }
        .hero-title { font-size: 3.5rem; font-weight: 700; margin-bottom: 0px; letter-spacing: 2px; }
        .hero-subtitle { font-size: 1.5rem; color: var(--accent-gold); font-weight: 300; margin-bottom: 40px; }
        .btn-cta { 
            background: transparent; border: 1px solid var(--accent-gold); color: var(--accent-gold);
            padding: 12px 40px; border-radius: 0; font-weight: 600; transition: 0.4s; text-decoration: none;
        }
        .btn-cta:hover { background: var(--accent-gold); color: var(--white); }

        /* 右下角浮動圖片窗格 (還原您滿意的排版) */
        .floating-window {
            position: absolute;
            bottom: 40px;
            right: 5%;
            width: 380px;
            background: var(--white);
            padding: 10px;
            box-shadow: 0 20px 50px rgba(0,0,0,0.3);
            z-index: 20;
            display: none; /* 平板以下隱藏以維持純淨 */
        }
        @media (min-width: 1200px) { .floating-window { display: block; } }
        .floating-window img { width: 100%; height: auto; display: block; }

        /* --- 3. 內容與地址區塊 --- */
        .section-padding { padding: 90px 0; }
        .address-box { 
            background: #fcfcfc; border: 1px solid #eee; padding: 50px; 
            border-left: 5px solid var(--accent-gold);
        }
        .address-box h3 { font-weight: 700; margin-bottom: 30px; color: var(--primary-dark); }
        .address-box p { font-size: 1.05rem; line-height: 2; color: #555; }
        .icon-circle { 
            width: 40px; height: 40px; background: rgba(197, 160, 89, 0.1); 
            display: inline-flex; align-items: center; justify-content: center; 
            border-radius: 50%; color: var(--accent-gold); margin-right: 15px;
        }

        footer { background: #000; color: #555; padding: 30px 0; text-align: center; font-size: 0.85rem; }
    </style>
</head>
<body lang="zh">

    <nav class="navbar navbar-expand-lg fixed-top">
        <div class="container">
            <a class="navbar-brand" href="#">
                <i class="fa-solid fa-needle brand-logo-icon"></i>
                <div class="brand-divider"></div>
                <div class="brand-name-text">
                    <div class="main">WELL YUEN</div>
                    <div class="sub">Garments Ltd. | 華源製衣</div>
                </div>
            </a>
            <div class="ms-auto">
                <a href="javascript:void(0)" class="lang-link active" onclick="setLanguage('zh')">中文</a>
                <span style="color:#444">/</span>
                <a href="javascript:void(0)" class="lang-link" onclick="setLanguage('en')">EN</a>
            </div>
        </div>
    </nav>

    <header class="hero-section">
        <div class="hero-center-content">
            <i class="fa-solid fa-vest-patches hero-main-logo"></i>
            
            <div class="lang-zh">
                <h1 class="hero-title">華源製衣有限公司</h1>
                <p class="hero-subtitle">WELL YUEN GARMENTS LTD.</p>
                <a href="#contact" class="btn-cta">立即洽詢</a>
            </div>

            <div class="lang-en">
                <h1 class="hero-title">WELL YUEN Garments</h1>
                <p class="hero-subtitle">Excellence Since 1991</p>
                <a href="#contact" class="btn-cta">CONTACT US</a>
            </div>
        </div>

        <div class="floating-window">
            <img src="https://images.unsplash.com/photo-1556761175-b413da4baf72?q=80&w=800&auto=format&fit=crop" alt="Factory Overview">
            <div class="p-2 text-center">
                <small class="text-muted fw-bold">OUR PRODUCTION LINE</small>
            </div>
        </div>
    </header>

    <section id="contact" class="section-padding">
        <div class="container">
            <div class="row g-5 align-items-center">
                <div class="col-lg-6">
                    <div class="address-box">
                        <h3 class="lang-zh">聯繫我們</h3>
                        <h3 class="lang-en">Office Location</h3>
                        
                        <p>
                            <span class="icon-circle"><i class="fa-solid fa-location-dot"></i></span>
                            <strong>Address:</strong><br>
                            <span class="ps-5 d-block">
                                1802 Million Fortune Industrial Centre,<br>
                                34-36 Chai Wan Kok Street,<br>
                                Tsuen Wan, New Territories, Hong Kong
                            </span>
                        </p>
                        
                        <p class="mt-4">
                            <span class="icon-circle"><i class="fa-solid fa-envelope"></i></span>
                            <strong>Email:</strong> wicky@wellyuen.com.hk
                        </p>
                        
                        <p>
                            <span class="icon-circle"><i class="fa-solid fa-phone"></i></span>
                            <strong>Phone:</strong> (+852) 2611 3201
                        </p>
                    </div>
                </div>
                
                <div class="col-lg-6 ps-lg-5">
                    <div class="lang-zh">
                        <h2 class="fw-bold mb-4">追求卓越的製造品質</h2>
                        <p class="text-muted mb-4">我們擁有超過三十年的服裝製造經驗，透過嚴謹的 BSCI 與 SA8000 認證管理，確保您的每一張訂單都能在最合規且高效的環境下完成。</p>
                        <ul class="list-unstyled">
                            <li class="mb-2"><i class="fa-solid fa-check text-gold me-2"></i> 靈活的起訂量 (MOQ)</li>
                            <li class="mb-2"><i class="fa-solid fa-check text-gold me-2"></i> 全自動化針織技術</li>
                            <li class="mb-2"><i class="fa-solid fa-check text-gold me-2"></i> 國際出口合規標準</li>
                        </ul>
                    </div>
                    <div class="lang-en">
                        <h2 class="fw-bold mb-4">Superior Manufacturing Quality</h2>
                        <p class="text-muted mb-4">With over 30 years of experience, our facilities are BSCI & SA8000 certified, ensuring every order is produced ethically and efficiently.</p>
                        <ul class="list-unstyled">
                            <li class="mb-2"><i class="fa-solid fa-check text-gold me-2"></i> Flexible MOQ</li>
                            <li class="mb-2"><i class="fa-solid fa-check text-gold me-2"></i> Automated Knitting Technology</li>
                            <li class="mb-2"><i class="fa-solid fa-check text-gold me-2"></i> Global Compliance Standards</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>© 1991-2026 Well Yuen Garments Ltd. All Rights Reserved.</p>
        </div>
    </footer>

    <script>
        function setLanguage(lang) {
            document.documentElement.setAttribute('lang', lang);
            document.body.setAttribute('lang', lang);
            
            // 切換連結樣式
            const links = document.querySelectorAll('.lang-link');
            links.forEach(link => {
                link.classList.remove('active');
                if(link.textContent.trim().toLowerCase().includes(lang === 'en' ? 'en' : '中')) {
                    link.classList.add('active');
                }
            });
        }
    </script>
</body>
</html>
