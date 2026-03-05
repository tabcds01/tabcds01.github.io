<html lang="zh-Hant">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Well Yuen Garments Ltd | 華源制衣有限公司</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@300;400;700&family=Plus+Jakarta+Sans:wght@400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary-dark: #0f1115;
            --accent-gold: #c5a059;
            --overlay-dark: rgba(15, 17, 21, 0.8);
        }

        body { font-family: 'Plus Jakarta Sans', 'Noto Sans TC', sans-serif; transition: 0.3s; color: #333; overflow-x: hidden; }
        html { scroll-behavior: smooth; }
        
        /* 語言切換邏輯 */
        [lang="en"] .lang-zh { display: none !important; }
        [lang="zh"] .lang-en { display: none !important; }

        /* 導航欄 */
        .navbar { background: rgba(15, 17, 21, 0.98); padding: 15px 0; border-bottom: 1px solid rgba(255,255,255,0.1); }
        .navbar-brand img { height: 40px; margin-right: 15px; width: auto; }
        .lang-switch .btn { color: #fff; border: 1px solid rgba(255,255,255,0.3); font-size: 0.75rem; padding: 4px 10px; margin-left: 5px; border-radius: 0; }
        .lang-switch .btn.active { background: var(--accent-gold); border-color: var(--accent-gold); }

        /* 首屏：專業質感 */
        .hero-section { 
            height: 100vh; 
            background: linear-gradient(var(--overlay-dark), var(--overlay-dark)), 
                        url('https://images.unsplash.com/photo-1558600090-f73f709300c8?auto=format&fit=crop&q=80&w=2000');
            background-size: cover; background-position: center; background-attachment: fixed;
            display: flex; align-items: center; color: white;
        }

        .section-padding { padding: 100px 0; }
        .bg-light-gray { background: #f9f9f9; }

        /* 核心優勢卡片 */
        .advantage-card { background: #fff; padding: 40px; height: 100%; border-top: 4px solid var(--accent-gold); box-shadow: 0 10px 30px rgba(0,0,0,0.05); }
        
        /* 服務流程步驟 */
        .process-step { position: relative; padding: 20px; text-align: center; }
        .step-num { width: 40px; height: 40px; background: var(--accent-gold); color: white; border-radius: 50%; display: flex; align-items: center; justify-content: center; margin: 0 auto 15px; font-weight: bold; }

        /* 視差橫幅 */
        .parallax-banner {
            padding: 120px 0;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), 
                        url('https://images.unsplash.com/photo-1581091226825-a6a2a5aee158?auto=format&fit=crop&q=80&w=2000');
            background-size: cover; background-attachment: fixed; color: white; text-align: center;
        }

        /* 聯繫區域與表格樣式修復 */
        .text-gold { color: var(--accent-gold); }
        .btn-gold { background: var(--accent-gold); color: white; border-radius: 0; padding: 15px 40px; font-weight: 600; border: none; transition: 0.3s; }
        .btn-gold:hover { background: #b08d4a; color: white; transform: translateY(-3px); }
        .form-control::placeholder { color: rgba(255,255,255,0.5); }
        .form-control:focus { 
            background-color: #444 !important; 
            border-color: var(--accent-gold) !important; 
            box-shadow: none; 
            color: white; 
        }

        /* 頁尾 */
        .footer-logo { height: 30px; width: auto; margin-bottom: 10px; }
    </style>
</head>
<body lang="en">

    <nav class="navbar navbar-expand-lg navbar-dark fixed-top">
        <div class="container">
            <a class="navbar-brand d-flex align-items-center" href="#" onclick="scrollToTop()">
                <img src="https://i.ibb.co/3W6qWbH/wy-logo-fixed.png" alt="Well Yuen Garments Ltd. Logo" class="footer-logo">
                <div>
                    <span class="lang-en">WELL YUEN <small style="font-weight:300;">Garments</small></span>
                    <span class="lang-zh">華源制衣 <small style="font-weight:300;">有限公司</small></span>
                </div>
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
            <div class="lang-en">
                <h1 class="display-1 fw-bold mb-4">Looking for the right factory?</h1>
                <p class="fs-4 text-white-50 mb-5">Established in 1991. Over 30 years of manufacturing excellence for global brands.</p>
            </div>
            <div class="lang-zh">
                <h1 class="display-2 fw-bold mb-4">正在尋找理想的工廠？</h1>
                <p class="fs-3 text-white-50 mb-5">華源制衣成立於 1991 年。三十載深耕，為全球品牌提供卓越製造服務。</p>
            </div>
            <a href="#contact" class="btn btn-gold">
                <span class="lang-en">CONTACT US NOW</span>
                <span class="lang-zh">立即聯絡我們</span>
            </a>
        </div>
    </header>

    <section id="about" class="section-padding">
        <div class="container">
            <div class="row g-5 align-items-center mb-5">
                <div class="col-lg-6">
                    <div class="lang-en">
                        <h2 class="display-5 fw-bold mb-4">Our Advantage</h2>
                        <p class="text-muted">We specialize in providing high quality garments to various sectors at highly competitive prices. Our three factories cover most types of woven and knit items.</p>
                    </div>
                    <div class="lang-zh">
                        <h2 class="display-4 fw-bold mb-4">我們的優勢</h2>
                        <p class="text-muted">我們致力於以極具競爭力的價格為各行業提供高品質服飾。旗下三家工廠產線全面，涵蓋絕大多數梭織與針織品類。</p>
                    </div>
                </div>
                <div class="col-lg-6">
                    <div class="row g-4">
                        <div class="col-md-6">
                            <div class="advantage-card">
                                <h5 class="fw-bold"><span class="lang-en">Comprehensive</span><span class="lang-zh">品類全面</span></h5>
                                <p class="small text-muted">Most woven and knit items / 覆蓋各類梭織及針織品項</p>
                            </div>
                        </div>
                        <div class="col-md-6">
                            <div class="advantage-card">
                                <h5 class="fw-bold"><span class="lang-en">Experienced</span><span class="lang-zh">專業團隊</span></h5>
                                <p class="small text-muted">Skilled merchandiser team / 資深跟單團隊精通市場需求</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="section-padding bg-light-gray">
        <div class="container text-center">
            <h2 class="fw-bold mb-5"><span class="lang-en">Main Products</span><span class="lang-zh">核心產品</span></h2>
            <div class="row g-4">
                <div class="col-md-3">
                    <div class="p-4 bg-white shadow-sm">
                        <i class="fa fa-user-ninja fa-2x mb-3 text-gold"></i>
                        <h6><span class="lang-en">Jackets & Coats</span><span class="lang-zh">夾克與大衣</span></h6>
                    </div>
                </div>
                <div class="col-md-3">
                    <div class="p-4 bg-white shadow-sm">
                        <i class="fa fa-vest fa-2x mb-3 text-gold"></i>
                        <h6><span class="lang-en">Jeans / Denims</span><span class="lang-zh">牛仔系列</span></h6>
                    </div>
                </div>
                <div class="col-md-3">
                    <div class="p-4 bg-white shadow-sm">
                        <i class="fa fa-mitten fa-2x mb-3 text-gold"></i>
                        <h6><span class="lang-en">Sweaters</span><span class="lang-zh">針織毛衣</span></h6>
                    </div>
                </div>
                <div class="col-md-3">
                    <div class="p-4 bg-white shadow-sm">
                        <i class="fa fa-tshirt fa-2x mb-3 text-gold"></i>
                        <h6><span class="lang-en">Knitted & Woven</span><span class="lang-zh">各類針梭織服裝</span></h6>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="section-padding">
        <div class="container">
            <h2 class="text-center fw-bold mb-5"><span class="lang-en">How We Work?</span><span class="lang-zh">服務流程</span></h2>
            <div class="row g-4">
                <div class="col-6 col-md-2 process-step">
                    <div class="step-num">1</div>
                    <p class="small fw-bold"><span class="lang-en">Samples/Designs</span><span class="lang-zh">獲取樣板/設計</span></p>
                </div>
                <div class="col-6 col-md-2 process-step">
                    <div class="step-num">2</div>
                    <p class="small fw-bold"><span class="lang-en">Finalize Details</span><span class="lang-zh">落實細節</span></p>
                </div>
                <div class="col-6 col-md-2 process-step">
                    <div class="step-num">3</div>
                    <p class="small fw-bold"><span class="lang-en">Quotation</span><span class="lang-zh">報價與打樣</span></p>
                </div>
                <div class="col-6 col-md-2 process-step">
                    <div class="step-num">4</div>
                    <p class="small fw-bold"><span class="lang-en">Confirm Order</span><span class="lang-zh">確認訂單並付定</span></p>
                </div>
                <div class="col-6 col-md-2 process-step">
                    <div class="step-num">5</div>
                    <p class="small fw-bold"><span class="lang-en">Mass Production</span><span class="lang-zh">大貨生產與質檢</span></p>
                </div>
                <div class="col-6 col-md-2 process-step">
                    <div class="step-num">6</div>
                    <p class="small fw-bold"><span class="lang-en">Deliver Goods</span><span class="lang-zh">成品交付</span></p>
                </div>
            </div>
        </div>
    </section>

    <section class="parallax-banner">
        <div class="container">
            <h2 class="display-4 fw-bold mb-4">
                <span class="lang-en">4,000 SQM Industrial Complex</span>
                <span class="lang-zh">4,000 平方米現代化工業園區</span>
            </h2>
            <p class="fs-5 opacity-75">
                <span class="lang-en">BSCI / SA8000 Certified Facilities with Intelligent Hanger System.</span>
                <span class="lang-zh">獲得 BSCI 及 SA8000 國際認證，引入智能吊掛系統優化產能。</span>
            </p>
            <div class="row mt-5">
                <div class="col-md-6 text-md-end border-md-end px-4">
                    <h4 class="text-gold">Guangdong Center</h4>
                    <p>Mainly producing Denims and Cardigans / 主要生產牛仔及針織開衫</p>
                </div>
                <div class="col-md-6 text-md-start px-4">
                    <h4 class="text-gold">Fujian Center</h4>
                    <p>Focused on Woven and Knits across different factories / 不同分廠專注梭織與針織</p>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="section-padding bg-dark text-white">
        <div class="container">
            <div class="row g-5 justify-content-center">
                <div class="col-lg-8 text-center">
                    <h2 class="fw-bold mb-4">
                        <span class="lang-en">Contact Our Team</span>
                        <span class="lang-zh">聯繫華源</span>
                    </h2>
                    <p class="text-white-50 fs-5 mb-5">
                        <span class="lang-en">Experienced in working with quality brands in leisure, lifestyle and functional sports sectors. Contact us directly for inquiries.</span>
                        <span class="lang-zh">我們擁有與休閒、生活方式及功能性運動品牌合作的豐富經驗。歡迎直接聯繫我們洽談業務。</span>
                    </p>
                    
                    <div class="row g-4 justify-content-center">
                        <div class="col-md-5">
                            <div class="p-4 border border-secondary">
                                <i class="fa fa-envelope text-gold fa-2x mb-3"></i>
                                <h5 class="text-white">Email</h5>
                                <a href="mailto:wicky@wellyuen.com.hk" class="text-decoration-none text-white-50">wicky@wellyuen.com.hk</a>
                            </div>
                        </div>
                        <div class="col-md-5">
                            <div class="p-4 border border-secondary">
                                <i class="fa fa-phone text-gold fa-2x mb-3"></i>
                                <h5 class="text-white">Phone / WhatsApp</h5>
                                <a href="tel:+85226113201" class="text-decoration-none text-white-50">(+852) 2611 3201</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <footer class="py-4 bg-black text-white-50 text-center">
        <div class="container">
            <img src="https://i.
