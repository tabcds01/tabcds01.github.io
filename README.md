<!DOCTYPE html>
<html lang="zh-Hant">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Well Yuen Garments Ltd | 華源制衣有限公司</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@300;400;700&family=Plus+Jakarta+Sans:wght@400;600;700&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --primary-dark: #12141a;
            --accent-gold: #b08d57;
            --overlay-dark: rgba(0, 0, 0, 0.7);
        }

        body { font-family: 'Plus Jakarta Sans', 'Noto Sans TC', sans-serif; transition: 0.3s; }
        
        /* 語言切換核心樣式 */
        [lang="en"] .lang-zh { display: none !important; }
        [lang="zh"] .lang-en { display: none !important; }

        /* 導航欄樣式 */
        .navbar { background: rgba(18, 20, 26, 0.98); padding: 15px 0; }
        .lang-switch .btn { color: #fff; border: 1px solid rgba(255,255,255,0.3); font-size: 0.8rem; padding: 4px 12px; margin-left: 5px; }
        .lang-switch .btn.active { background: var(--accent-gold); border-color: var(--accent-gold); }

        /* 內容樣式 */
        .hero-section { 
            height: 100vh; 
            background: linear-gradient(var(--overlay-dark), var(--overlay-dark)), 
                        url('https://images.unsplash.com/photo-1558444479-c84824d2936e?auto=format&fit=crop&q=80&w=2000');
            background-size: cover; background-position: center; display: flex; align-items: center; color: white;
        }

        .section-padding { padding: 100px 0; }
        .feature-card { background: #f8f9fa; border: none; padding: 40px; height: 100%; transition: 0.3s; }
        .feature-card:hover { background: #fff; box-shadow: 0 15px 40px rgba(0,0,0,0.1); transform: translateY(-10px); }
        .btn-gold { background: var(--accent-gold); color: white; border-radius: 0; padding: 15px 40px; text-transform: uppercase; font-weight: 600; border: none; }
        
        .parallax-banner {
            padding: 120px 0;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), 
                        url('https://images.unsplash.com/photo-1581091226825-a6a2a5aee158?auto=format&fit=crop&q=80&w=2000');
            background-size: cover; background-attachment: fixed; color: white; text-align: center;
        }
    </style>
</head>
<body lang="en"> <nav class="navbar navbar-expand-lg navbar-dark fixed-top">
        <div class="container">
            <a class="navbar-brand fw-bold" href="#">
                <span class="lang-en">WELL YUEN</span>
                <span class="lang-zh">華源制衣</span>
            </a>
            <div class="ms-auto d-flex align-items: center;">
                <div class="lang-switch">
                    <button class="btn btn-sm active" onclick="setLanguage('en')">EN</button>
                    <button class="btn btn-sm" onclick="setLanguage('zh')">中文</button>
                </div>
            </div>
        </div>
    </nav>

    <header class="hero-section">
        <div class="container text-center">
            <div class="lang-en">
                <p class="text-uppercase tracking-widest mb-3" style="color: var(--accent-gold); letter-spacing: 4px;">Since 1991</p>
                <h1 class="display-1 fw-bold mb-4">Well Yuen Garments Ltd.</h1>
                <p class="fs-4 text-white-50 mb-5">Premier Garment Manufacturing & Export Excellence</p>
            </div>
            <div class="lang-zh">
                <p class="text-uppercase tracking-widest mb-3" style="color: var(--accent-gold); letter-spacing: 4px;">始於 1991 年</p>
                <h1 class="display-2 fw-bold mb-4">華源制衣有限公司</h1>
                <p class="fs-3 text-white-50 mb-5">專業服裝製造與出口專家 · 橫跨三十載的品質傳承</p>
            </div>
            <a href="#about" class="btn btn-gold">
                <span class="lang-en">Explore More</span>
                <span class="lang-zh">探索更多</span>
            </a>
        </div>
    </header>

    <section id="about" class="section-padding">
        <div class="container">
            <div class="row g-5 align-items-center">
                <div class="col-lg-6">
                    <img src="https://images.unsplash.com/photo-1524292332709-b33366a7f139?auto=format&fit=crop&q=80&w=1000" class="img-fluid shadow-lg" alt="Factory">
                </div>
                <div class="col-lg-6">
                    <div class="lang-en">
                        <h2 class="display-5 fw-bold mb-4">Corporate Heritage</h2>
                        <p class="lead">Established in 1991, Well Yuen Garments Ltd. is a clothing manufacturer with over 30 years of experience.</p>
                        <p class="text-muted">We provide high-quality garments to various sectors at highly competitive prices. Specializing in jackets, coats, jeans, sweaters, and all kinds of knitted & woven garments.</p>
                    </div>
                    <div class="lang-zh">
                        <h2 class="display-5 fw-bold mb-4">公司傳承</h2>
                        <p class="lead">華源制衣有限公司成立於 1991 年，擁有超過 30 年的服裝製造資深經驗。</p>
                        <p class="text-muted">我們致力於以極具競爭力的價格為各行業提供高品質服飾。專業生產夾克、大衣、牛仔褲、毛衣及各類針織與梭織服裝。</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="section-padding bg-light">
        <div class="container text-center">
            <h2 class="mb-5 fw-bold">
                <span class="lang-en">Production Hubs</span>
                <span class="lang-zh">生產基地</span>
            </h2>
            <div class="row g-4 text-start">
                <div class="col-md-6">
                    <div class="feature-card">
                        <h4 class="fw-bold mb-3">
                            <span class="lang-en">Guangdong Facility</span>
                            <span class="lang-zh">廣東生產中心</span>
                        </h4>
                        <p class="text-muted">
                            <span class="lang-en">Specialized in heavy denim production and premium cardigan knitwear.</span>
                            <span class="lang-zh">專注於高品質牛仔服裝生產以及精細的針織開衫系列。</span>
                        </p>
                    </div>
                </div>
                <div class="col-md-6">
                    <div class="feature-card">
                        <h4 class="fw-bold mb-3">
                            <span class="lang-en">Fujian Hub</span>
                            <span class="lang-zh">福建生產中心</span>
                        </h4>
                        <p class="text-muted">
                            <span class="lang-en">Focused on woven and knit garments for global lifestyle and sport brands.</span>
                            <span class="lang-zh">專為全球休閒與運動品牌提供各類梭織及針織服飾。</span>
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="parallax-banner">
        <div class="container">
            <h2 class="display-4 fw-bold">
                <span class="lang-en">4,000 SQM Industrial Complex</span>
                <span class="lang-zh">4,000 平方米現代化工廠</span>
            </h2>
            <p class="fs-5 mt-4 opacity-75">
                <span class="lang-en">Equipped with Intelligent Hanger Systems for maximum efficiency.</span>
                <span class="lang-zh">引入智能吊掛系統，實現產能與生產效率的極大化。</span>
            </p>
        </div>
    </section>

    <section id="contact" class="section-padding">
        <div class="container">
            <div class="row g-5">
                <div class="col-lg-5">
                    <h2 class="fw-bold">
                        <span class="lang-en">Inquiry</span>
                        <span class="lang-zh">業務諮詢</span>
                    </h2>
                    <p class="text-muted mt-3">
                        <span class="lang-en">Servicing over 20 countries including UK, Netherlands, Germany, and Australia.</span>
                        <span class="lang-zh">產品遠銷荷蘭、英國、芬蘭、德國、西班牙和澳洲等 20 多個國家。</span>
                    </p>
                </div>
                <div class="col-lg-7">
                    <form class="row g-3">
                        <div class="col-md-6"><input type="text" class="form-control" placeholder="Name 姓名"></div>
                        <div class="col-md-6"><input type="email" class="form-control" placeholder="Email 電郵"></div>
                        <div class="col-12"><textarea class="form-control" rows="4" placeholder="Message 需求"></textarea></div>
                        <div class="col-12"><button type="submit" class="btn btn-gold w-100">
                            <span class="lang-en">Send Message</span>
                            <span class="lang-zh">提交諮詢</span>
                        </button></div>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <footer class="py-4 bg-dark text-white-50 text-center">
        <p class="mb-0">© 1991 - 2026 Well Yuen Garments Ltd. 華源制衣有限公司</p>
    </footer>

    <script>
        function setLanguage(lang) {
            // 改變 body 的 lang 屬性
            document.body.setAttribute('lang', lang);
            
            // 更新按鈕狀態
            const buttons = document.querySelectorAll('.lang-switch .btn');
            buttons.forEach(btn => {
                if (btn.innerText.toLowerCase() === lang || (btn.innerText === '中文' && lang === 'zh')) {
                    btn.classList.add('active');
                } else {
                    btn.classList.remove('active');
                }
            });
            
            // 可選：將偏好儲存到 local storage
            localStorage.setItem('preferred_lang', lang);
        }

        // 初始化檢查用戶之前的選擇
        window.onload = () => {
            const savedLang = localStorage.getItem('preferred_lang');
            if (savedLang) setLanguage(savedLang);
        };
    </script>

</body>
</html>
