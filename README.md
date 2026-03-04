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
            --primary-dark: #0f1115;
            --accent-gold: #c5a059;
            --overlay-dark: rgba(15, 17, 21, 0.75);
            --overlay-gold: rgba(197, 160, 89, 0.15);
        }

        body { font-family: 'Plus Jakarta Sans', 'Noto Sans TC', sans-serif; transition: 0.3s; color: #333; }
        
        /* 語言切換核心邏輯 */
        [lang="en"] .lang-zh { display: none !important; }
        [lang="zh"] .lang-en { display: none !important; }

        /* 導航欄 */
        .navbar { background: rgba(15, 17, 21, 0.95); backdrop-filter: blur(10px); padding: 15px 0; border-bottom: 1px solid rgba(255,255,255,0.1); }
        .lang-switch .btn { color: #fff; border: 1px solid rgba(255,255,255,0.3); font-size: 0.75rem; padding: 4px 10px; margin-left: 5px; border-radius: 0; }
        .lang-switch .btn.active { background: var(--accent-gold); border-color: var(--accent-gold); }

        /* 首屏：專業布料質感背景 */
        .hero-section { 
            height: 100vh; 
            background: linear-gradient(var(--overlay-dark), var(--overlay-dark)), 
                        url('https://images.unsplash.com/photo-1558600090-f73f709300c8?auto=format&fit=crop&q=80&w=2000');
            background-size: cover; background-position: center; background-attachment: fixed;
            display: flex; align-items: center; color: white;
        }

        /* 內容區塊樣式 */
        .section-padding { padding: 120px 0; }
        .feature-card { background: #fff; border: 1px solid #f0f0f0; padding: 50px; height: 100%; transition: 0.4s; position: relative; overflow: hidden; }
        .feature-card:hover { transform: translateY(-10px); box-shadow: 0 20px 40px rgba(0,0,0,0.08); border-color: var(--accent-gold); }
        
        /* 橫幅：現代工業技術背景 (視差) */
        .innovation-banner {
            padding: 150px 0;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), 
                        url('https://images.unsplash.com/photo-1581091226825-a6a2a5aee158?auto=format&fit=crop&q=80&w=2000');
            background-size: cover; background-position: center; background-attachment: fixed;
            color: white; text-align: center;
        }

        /* 產品分類：展示區背景 */
        .product-section { background: #fcfcfc; position: relative; }
        .product-section::before {
            content: ""; position: absolute; top: 0; right: 0; width: 300px; height: 100%;
            background: url('https://images.unsplash.com/photo-1524292332709-b33366a7f139?auto=format&fit=crop&q=80&w=600');
            opacity: 0.03; pointer-events: none;
        }

        .btn-gold { background: var(--accent-gold); color: white; border-radius: 0; padding: 18px 45px; letter-spacing: 2px; font-weight: 600; border: none; transition: 0.3s; }
        .btn-gold:hover { background: #b08d4a; color: white; box-shadow: 0 10px 20px rgba(197,160,89,0.3); }
        
        .stat-item h3 { color: var(--accent-gold); font-size: 3.5rem; font-weight: 700; margin-bottom: 5px; }
    </style>
</head>
<body lang="en">

    <nav class="navbar navbar-expand-lg navbar-dark fixed-top">
        <div class="container">
            <a class="navbar-brand fw-bold" href="#">
                <span class="lang-en">WELL YUEN <small style="font-weight:300; font-size: 0.7em;">Garments</small></span>
                <span class="lang-zh">華源制衣 <small style="font-weight:300; font-size: 0.7em;">有限公司</small></span>
            </a>
            <div class="ms-auto d-flex align-items-center">
                <div class="lang-switch">
                    <button class="btn active" onclick="setLanguage('en')">EN</button>
                    <button class="btn" onclick="setLanguage('zh')">中文</button>
                </div>
            </div>
        </div>
    </nav>

    <header class="hero-section">
        <div class="container">
            <div class="row">
                <div class="col-lg-8">
                    <div class="lang-en">
                        <p class="text-uppercase tracking-widest mb-3" style="color: var(--accent-gold); letter-spacing: 5px;">Excellence in Textiles</p>
                        <h1 class="display-1 fw-bold mb-4">Crafting the Future<br>of Apparel</h1>
                        <p class="fs-5 text-white-50 mb-5 mb-lg-5" style="max-width: 600px;">Since 1991, providing high-quality garment manufacturing solutions to over 20 countries worldwide.</p>
                    </div>
                    <div class="lang-zh">
                        <p class="text-uppercase tracking-widest mb-3" style="color: var(--accent-gold); letter-spacing: 5px;">卓越紡織工藝</p>
                        <h1 class="display-2 fw-bold mb-4">華源制衣：<br>定義服裝製造新標準</h1>
                        <p class="fs-4 text-white-50 mb-5" style="max-width: 600px;">始於 1991 年，深耕服裝製造三十載。以高品質產品與專業技術，服務全球二十餘國客戶。</p>
                    </div>
                    <a href="#contact" class="btn btn-gold">
                        <span class="lang-en">Partner With Us</span>
                        <span class="lang-zh">洽談合作</span>
                    </a>
                </div>
            </div>
        </div>
    </header>

    <section id="about" class="section-padding">
        <div class="container">
            <div class="row mb-5 align-items-center">
                <div class="col-lg-6 mb-4 mb-lg-0">
                    <img src="https://images.unsplash.com/photo-1551135049-8a33b5883817?auto=format&fit=crop&q=80&w=1200" class="img-fluid shadow-lg" alt="Industrial Excellence">
                </div>
                <div class="col-lg-6 ps-lg-5">
                    <div class="lang-en">
                        <h2 class="display-5 fw-bold mb-4">Our Heritage</h2>
                        <p class="lead text-dark">Well Yuen Garments Ltd. represents over 30 years of industrial mastery.</p>
                        <p class="text-muted">Specializing in jackets, coats, jeans, and premium knitwear, we balance high-volume capacity with meticulous quality control for the world's leading brands.</p>
                    </div>
                    <div class="lang-zh">
                        <h2 class="display-4 fw-bold mb-4">關於華源</h2>
                        <p class="lead text-dark">華源制衣有限公司代表了超過三十年的工業積澱。</p>
                        <p class="text-muted">我們專業生產夾克、大衣、牛仔褲及各類高品質針織服飾。在追求大規模產能的同時，華源始於終堅持嚴苛的質量管控，成為全球知名品牌的信賴夥伴。</p>
                    </div>
                </div>
            </div>
            
            <div class="row g-4 mt-5">
                <div class="col-6 col-md-3 stat-item text-center">
                    <h3>30+</h3>
                    <p class="lang-en">Years Experience</p><p class="lang-zh">年製造經驗</p>
                </div>
                <div class="col-6 col-md-3 stat-item text-center">
                    <h3>20+</h3>
                    <p class="lang-en">Global Markets</p><p class="lang-zh">全球市場</p>
                </div>
                <div class="col-6 col-md-3 stat-item text-center">
                    <h3>4k</h3>
                    <p class="lang-en">SQM Facility</p><p class="lang-zh">平方米園區</p>
                </div>
                <div class="col-6 col-md-3 stat-item text-center">
                    <h3>BSCI</h3>
                    <p class="lang-en">Certified</p><p class="lang-zh">國際合規認證</p>
                </div>
            </div>
        </div>
    </section>

    <section class="innovation-banner">
        <div class="container">
            <h2 class="display-4 fw-bold mb-4">
                <span class="lang-en">Advanced Smart Production</span>
                <span class="lang-zh">智慧生產 · 科技賦能</span>
            </h2>
            <p class="fs-5 opacity-75 mx-auto" style="max-width: 800px;">
                <span class="lang-en">We integrate the Intelligent Hanger System to maximize production efficiency, ensuring consistent quality and on-time global delivery.</span>
                <span class="lang-zh">我們引入了「智能吊掛系統」以實現生產效率的極大化，確保每一件產品的質量穩定，並精準達成全球交付目標。</span>
            </p>
        </div>
    </section>

    <section id="facilities" class="section-padding product-section">
        <div class="container text-center">
            <h2 class="mb-5 fw-bold display-6">
                <span class="lang-en">Manufacturing Hubs</span>
                <span class="lang-zh">兩大生產中心</span>
            </h2>
            <div class="row g-5 text-start">
                <div class="col-md-6">
                    <div class="feature-card">
                        <div style="width: 40px; height: 3px; background: var(--accent-gold); margin-bottom: 20px;"></div>
                        <h4 class="fw-bold">
                            <span class="lang-en">Guangdong Facility</span>
                            <span class="lang-zh">廣東生產基地</span>
                        </h4>
                        <p class="text-muted mt-3">
                            <span class="lang-en">Specialized focus on high-durability Denim and precision Cardigans.</span>
                            <span class="lang-zh">核心業務：高品質牛仔服飾系列及精細針織開衫。</span>
                        </p>
                    </div>
                </div>
                <div class="col-md-6">
                    <div class="feature-card">
                        <div style="width: 40px; height: 3px; background: var(--accent-gold); margin-bottom: 20px;"></div>
                        <h4 class="fw-bold">
                            <span class="lang-en">Fujian Production Center</span>
                            <span class="lang-zh">福建生產基地</span>
                        </h4>
                        <p class="text-muted mt-3">
                            <span class="lang-en">The hub for complex Woven garments and various functional Knits.</span>
                            <span class="lang-zh">核心業務：各類梭織服飾及功能性運動針織系列。</span>
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="section-padding bg-dark text-white">
        <div class="container">
            <div class="row g-5">
                <div class="col-lg-5">
                    <h2 class="display-6 fw-bold mb-4">
                        <span class="lang-en">Global Partnership</span>
                        <span class="lang-zh">全球夥伴合作</span>
                    </h2>
                    <p class="text-white-50">
                        <span class="lang-en">Expanding reach from the UK to Australia. Our merchandiser team is ready to assist your brand with fabric innovation and strategic pricing.</span>
                        <span class="lang-zh">業務版圖從歐洲延伸至澳洲。我們的專業跟單團隊已準備就緒，為您的品牌提供面料創新、具競爭力的價格及優質的供應鏈支持。</span>
                    </p>
                </div>
                <div class="col-lg-7">
                    <form class="row g-3">
                        <div class="col-md-6"><input type="text" class="form-control bg-secondary text-white border-0" placeholder="Name 姓名" style="padding: 15px;"></div>
                        <div class="col-md-6"><input type="email" class="form-control bg-secondary text-white border-0" placeholder="Email 電郵" style="padding: 15px;"></div>
                        <div class="col-12"><textarea class="form-control bg-secondary text-white border-0" rows="4" placeholder="Message 需求描述" style="padding: 15px;"></textarea></div>
                        <div class="col-12"><button type="submit" class="btn btn-gold w-100">
                            <span class="lang-en">Submit Inquiry</span>
                            <span class="lang-zh">提交諮詢</span>
                        </button></div>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <footer class="py-4 bg-black text-white-50 text-center" style="font-size: 0.85rem;">
        <div class="container">
            <p class="mb-0">© 1991 - 2026 Well Yuen Garments Ltd. 華源制衣有限公司 | All Rights Reserved.</p>
        </div>
    </footer>

    <script>
        function setLanguage(lang) {
            document.body.setAttribute('lang', lang);
            const buttons = document.querySelectorAll('.lang-switch .btn');
            buttons.forEach(btn => {
                btn.classList.toggle('active', btn.innerText.toLowerCase() === lang || (btn.innerText === '中文' && lang === 'zh'));
            });
            localStorage.setItem('preferred_lang', lang);
        }

        window.onload = () => {
            const savedLang = localStorage.getItem('preferred_lang') || 'en';
            setLanguage(savedLang);
        };
    </script>

</body>
</html>
