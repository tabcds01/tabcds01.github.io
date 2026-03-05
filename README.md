<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>華源製衣有限公司 - 專業服裝生產廠家</title>
    <meta name="description" content="華源製衣有限公司，30多年服裝生產經驗，專注梭織、針織、牛仔服裝生產">
    <!-- 稳定CDN加载Font Awesome -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css">
    <style>
        /* 基础样式 */
        :root {
            --primary: #2D3748;
            --accent1: #E53E3E;
            --accent2: #48BB78;
            --neutral1: #F7FAFC;
            --neutral2: #718096;
            --neutral3: #1A202C;
            --white: #FFFFFF;
        }
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', '微軟雅黑', 'Microsoft YaHei', sans-serif;
        }
        body {
            background-color: var(--neutral1);
            color: var(--neutral3);
            line-height: 1.8;
            overflow-x: hidden;
        }

        /* 导航栏（核心：包含语言按钮） */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background-color: var(--white);
            box-shadow: 0 2px 4px rgba(0,0,0,0.05);
            z-index: 1000;
            padding: 1rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 2rem;
        }
        .logo {
            font-size: 1.25rem;
            font-weight: bold;
            color: var(--primary);
            white-space: nowrap;
        }
        .nav-links {
            display: flex;
            gap: 2rem;
            flex: 1;
            justify-content: center;
        }
        .nav-links a {
            text-decoration: none;
            color: var(--neutral3);
            font-size: 0.875rem;
            transition: color 0.3s;
        }
        .nav-links a:hover {
            color: var(--primary);
        }

        /* 中英切换按钮（核心样式） */
        .lang-switch {
            display: flex;
            gap: 1.2rem;
            margin-left: auto;
            white-space: nowrap;
        }
        .lang-switch button {
            border: none;
            background: none;
            color: var(--neutral3);
            cursor: pointer;
            font-size: 1rem;
            font-weight: 500;
            padding: 0.3rem 0.6rem;
            border-radius: 4px;
            transition: all 0.3s;
        }
        .lang-switch button.active {
            color: var(--white);
            background-color: var(--primary);
            font-weight: bold;
        }
        .lang-switch button:hover:not(.active) {
            color: var(--primary);
        }

        /* 移动端菜单按钮 */
        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
            margin-left: 1rem;
        }

        /* 通用区块样式 */
        section {
            padding: 5rem 5%;
            scroll-margin-top: 80px;
        }
        .section-title {
            text-align: center;
            font-size: 1.5rem;
            color: var(--primary);
            font-weight: bold;
            margin-bottom: 2rem;
            position: relative;
        }
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -0.5rem;
            left: 50%;
            transform: translateX(-50%);
            width: 3rem;
            height: 2px;
            background-color: var(--accent1);
        }

        /* 首页banner */
        #home {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding: 80px 5% 2rem;
        }
        .banner {
            display: flex;
            width: 100%;
            gap: 2rem;
            flex-wrap: wrap;
        }
        .banner-text {
            flex: 1;
            min-width: 300px;
        }
        .banner-text h1 {
            font-size: 2.25rem;
            margin-bottom: 1rem;
        }
        .banner-text h2 {
            font-size: 1.5rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }
        .banner-text p {
            font-size: 1rem;
            color: var(--neutral2);
            margin-bottom: 2rem;
        }
        .btn {
            display: inline-block;
            padding: 0.75rem 1.5rem;
            background-color: var(--primary);
            color: var(--white);
            text-decoration: none;
            border-radius: 4px;
            font-size: 0.875rem;
            transition: background-color 0.3s;
        }
        .btn:hover {
            background-color: var(--accent1);
        }
        .banner-img {
            flex: 1;
            min-width: 300px;
        }
        .banner-img img {
            width: 100%;
            height: auto;
            border-radius: 8px;
            object-fit: cover;
        }

        /* 关于我们 */
        #about {
            background-color: var(--white);
        }
        .about-content {
            max-width: 100%;
            margin: 0 auto;
            text-align: center;
            padding: 0 1rem;
        }

        /* 产品中心 */
        #products {
            background-color: var(--neutral1);
        }
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }
        .product-card {
            background-color: var(--white);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 2px 8px rgba(0,0,0,0.05);
        }
        .product-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        .product-card p {
            padding: 1rem;
            text-align: center;
            font-size: 0.875rem;
        }
        .products-note {
            text-align: center;
            margin-top: 2rem;
            font-size: 0.75rem;
            color: var(--neutral2);
        }

        /* 合作流程 */
        #process {
            background-color: var(--white);
        }
        .process-list {
            max-width: 100%;
            margin: 0 auto;
            padding: 0 1rem;
        }
        .process-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 1.5rem;
            padding-bottom: 1.5rem;
            border-bottom: 1px solid var(--neutral2);
        }
        .process-number {
            width: 2rem;
            height: 2rem;
            border-radius: 50%;
            background-color: var(--accent2);
            color: var(--white);
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            margin-right: 1rem;
            flex-shrink: 0;
        }
        .process-text {
            font-size: 0.875rem;
        }

        /* 工厂实力 */
        #factory {
            background-color: var(--neutral1);
        }
        .factory-content {
            display: flex;
            gap: 2rem;
            flex-wrap: wrap;
            padding: 0 1rem;
        }
        .factory-text {
            flex: 1;
            min-width: 300px;
        }
        .factory-text h3 {
            font-size: 1.25rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }
        .factory-list {
            list-style: none;
        }
        .factory-list li {
            font-size: 0.875rem;
            margin-bottom: 0.75rem;
            display: flex;
            align-items: center;
        }
        .factory-list li::before {
            content: '✔';
            color: var(--accent2);
            margin-right: 0.5rem;
        }
        .factory-img {
            flex: 1;
            min-width: 300px;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 1rem;
        }
        .factory-img img {
            width: 100%;
            height: 150px;
            object-fit: cover;
            border-radius: 8px;
        }

        /* 核心优势 */
        #advantage {
            background-color: var(--white);
        }
        .advantage-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            max-width: 100%;
            margin: 0 auto;
            padding: 0 1rem;
        }
        .advantage-card {
            background-color: var(--neutral1);
            border-radius: 8px;
            padding: 2rem;
            box-shadow: 0 2px 8px rgba(0,0,0,0.05);
            transition: transform 0.3s;
        }
        .advantage-card:hover {
            transform: translateY(-5px);
        }
        .advantage-card i {
            font-size: 1.5rem;
            color: var(--accent2);
            margin-bottom: 1rem;
        }
        .advantage-card h3 {
            font-size: 1rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }
        .advantage-card p {
            font-size: 0.875rem;
            color: var(--neutral2);
        }

        /* 联系我们 */
        #contact {
            background-color: var(--white);
        }
        .contact-content {
            max-width: 100%;
            margin: 0 auto;
            padding: 0 1rem;
        }
        .contact-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 2rem;
        }
        .contact-item i {
            color: var(--primary);
            margin-right: 1rem;
            margin-top: 0.25rem;
            flex-shrink: 0;
            font-size: 1.2rem;
        }
        .contact-item p {
            font-size: 1rem;
        }
        .contact-item a {
            color: #0066cc;
            text-decoration: none;
            word-break: break-all;
        }

        /* 页脚 */
        footer {
            background-color: var(--primary);
            color: var(--white);
            padding: 3rem 5%;
            text-align: center;
            width: 100%;
        }
        .footer-logo {
            font-size: 1.25rem;
            font-weight: bold;
            margin-bottom: 1rem;
        }
        .footer-slogan {
            font-size: 0.875rem;
            opacity: 0.8;
            margin-bottom: 2rem;
        }
        .copyright {
            font-size: 0.75rem;
            opacity: 0.6;
        }

        /* 响应式适配 */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
                position: absolute;
                top: 80px;
                left: 0;
                right: 0;
                background: var(--white);
                flex-direction: column;
                padding: 2rem 5%;
                box-shadow: 0 4px 8px rgba(0,0,0,0.1);
                gap: 1rem;
                z-index: 999;
            }
            .nav-links.show {
                display: flex;
            }
            .menu-toggle {
                display: block;
            }
            .banner-text h1 {
                font-size: 1.75rem;
            }
            .banner-text h2 {
                font-size: 1.25rem;
            }
        }
        @media (max-width: 480px) {
            .lang-switch button {
                font-size: 0.9rem;
            }
            .logo {
                font-size: 1rem;
            }
            section {
                padding: 3rem 5%;
            }
        }
    </style>
</head>
<body>
    <!-- 导航栏（包含中英切换按钮） -->
    <nav>
        <div class="logo" data-lang="zh">華源製衣有限公司</div>
        <div class="logo" data-lang="en" style="display: none;">Well Yuen Garments Ltd.</div>
        
        <div class="nav-links">
            <a href="#home" data-lang="zh">首頁</a>
            <a href="#home" data-lang="en" style="display: none;">Home</a>
            <a href="#about" data-lang="zh">關於我們</a>
            <a href="#about" data-lang="en" style="display: none;">About Us</a>
            <a href="#products" data-lang="zh">產品中心</a>
            <a href="#products" data-lang="en" style="display: none;">Products</a>
            <a href="#process" data-lang="zh">合作流程</a>
            <a href="#process" data-lang="en" style="display: none;">How We Work</a>
            <a href="#factory" data-lang="zh">工廠實力</a>
            <a href="#factory" data-lang="en" style="display: none;">Factories</a>
            <a href="#advantage" data-lang="zh">核心優勢</a>
            <a href="#advantage" data-lang="en" style="display: none;">Advantage</a>
            <a href="#contact" data-lang="zh">聯繫我們</a>
            <a href="#contact" data-lang="en" style="display: none;">Contact Us</a>
        </div>

        <!-- 中英切换按钮（核心DOM） -->
        <div class="lang-switch">
            <button id="btn-zh" class="active">中</button>
            <button id="btn-en">EN</button>
        </div>
        <div class="menu-toggle">
            <i class="fa fa-bars"></i>
        </div>
    </nav>

    <!-- 首页 -->
    <section id="home">
        <div class="banner">
            <div class="banner-text">
                <h1 data-lang="zh">尋找合適的服裝生產工廠？</h1>
                <h1 data-lang="en" style="display: none;">Looking for the right factory?</h1>
                <h2 data-lang="zh">我們可以幫到您！</h2>
                <h2 data-lang="en" style="display: none;">We can help!</h2>
                <p data-lang="zh">華源製衣有限公司成立於1991年，擁有30多年服裝生產經驗，為您提供高品質、高性價比的服裝產品。</p>
                <p data-lang="en" style="display: none;">Well Yuen Garments Ltd. was established in 1991. A clothing manufacturer with over 30 years of experience, providing high quality garments at highly competitive prices.</p>
                <a href="#contact" class="btn" data-lang="zh">立即聯繫我們</a>
                <a href="#contact" class="btn" data-lang="en" style="display: none;">Contact Us Now</a>
            </div>
            <div class="banner-img">
                <img src="https://picsum.photos/800/600?random=100" alt="服裝產品展示" loading="lazy">
            </div>
        </div>
    </section>

    <!-- 关于我们 -->
    <section id="about">
        <h2 class="section-title" data-lang="zh">關於我們</h2>
        <h2 class="section-title" data-lang="en" style="display: none;">About Us</h2>
        <div class="about-content">
            <p data-lang="zh">我們是擁有30多年經驗的專業服裝生產廠家，專注於為各領域客戶提供高品質服裝產品，在休閒、生活方式和功能性運動領域的優質品牌合作方面擁有豐富經驗。我們擁有設備完善的生產線和嚴格的產品質量控制體系，確保產品質量和準時交付。</p>
            <p data-lang="en" style="display: none;">We are a professional clothing manufacturer with over 30 years of experience. We focus on providing high quality garments to various sectors, and have rich experience in cooperating with quality brands in the leisure, lifestyle and functional sports sector. We have a well-equipped production line with strict product quality control to ensure product quality and on-time delivery.</p>
        </div>
    </section>

    <!-- 产品中心 -->
    <section id="products">
        <h2 class="section-title" data-lang="zh">產品中心</h2>
        <h2 class="section-title" data-lang="en" style="display: none;">Products</h2>
        <div class="products-grid">
            <div class="product-card">
                <img src="https://picsum.photos/400/300?random=101" alt="夾克" loading="lazy">
                <p data-lang="zh">夾克</p>
                <p data-lang="en" style="display: none;">Jacket</p>
            </div>
            <div class="product-card">
                <img src="https://picsum.photos/400/300?random=102" alt="大衣" loading="lazy">
                <p data-lang="zh">大衣</p>
                <p data-lang="en" style="display: none;">Coats</p>
            </div>
            <div class="product-card">
                <img src="https://picsum.photos/400/300?random=103" alt="牛仔" loading="lazy">
                <p data-lang="zh">牛仔</p>
                <p data-lang="en" style="display: none;">Jeans</p>
            </div>
            <div class="product-card">
                <img src="https://picsum.photos/400/300?random=104" alt="毛衣" loading="lazy">
                <p data-lang="zh">毛衣</p>
                <p data-lang="en" style="display: none;">Sweaters</p>
            </div>
            <div class="product-card">
                <img src="https://picsum.photos/400/300?random=105" alt="針織服裝" loading="lazy">
                <p data-lang="zh">針織服裝</p>
                <p data-lang="en" style="display: none;">Knitted Garments</p>
            </div>
            <div class="product-card">
                <img src="https://picsum.photos/400/300?random=106" alt="梭織服裝" loading="lazy">
                <p data-lang="zh">梭織服裝</p>
                <p data-lang="en" style="display: none;">Woven Garments</p>
            </div>
        </div>
        <p class="products-note" data-lang="zh">以及各類針織和梭織服裝產品</p>
        <p class="products-note" data-lang="en" style="display: none;">and all kinds of knitted & woven garments.</p>
    </section>

    <!-- 合作流程 -->
    <section id="process">
        <h2 class="section-title" data-lang="zh">合作流程</h2>
        <h2 class="section-title" data-lang="en" style="display: none;">How We Work</h2>
        <div class="process-list">
            <div class="process-item">
                <div class="process-number">1</div>
                <div class="process-text" data-lang="zh">提供您的樣品或原創設計</div>
                <div class="process-text" data-lang="en" style="display: none;">Get your samples or original designs</div>
            </div>
            <div class="process-item">
                <div class="process-number">2</div>
                <div class="process-text" data-lang="zh">與我們的團隊確定所有產品細節</div>
                <div class="process-text" data-lang="en" style="display: none;">Finalize all product details with our team</div>
            </div>
            <div class="process-item">
                <div class="process-number">3</div>
                <div class="process-text" data-lang="zh">專業報價與樣品製作</div>
                <div class="process-text" data-lang="en" style="display: none;">Professional quotation & sample making</div>
            </div>
            <div class="process-item">
                <div class="process-number">4</div>
                <div class="process-text" data-lang="zh">確認訂單並支付定金</div>
                <div class="process-text" data-lang="en" style="display: none;">Confirm the order and remit the deposit</div>
            </div>
            <div class="process-item">
                <div class="process-number">5</div>
                <div class="process-text" data-lang="zh">批量生產與嚴格質量檢驗</div>
                <div class="process-text" data-lang="en" style="display: none;">Mass production & strict quality inspection</div>
            </div>
            <div class="process-item">
                <div class="process-number">6</div>
                <div class="process-text" data-lang="zh">安排成品發貨</div>
                <div class="process-text" data-lang="en" style="display: none;">Arrange delivery of the finished goods</div>
            </div>
        </div>
    </section>

    <!-- 工厂实力 -->
    <section id="factory">
        <h2 class="section-title" data-lang="zh">工廠實力</h2>
        <h2 class="section-title" data-lang="en" style="display: none;">Factories</h2>
        <div class="factory-content">
            <div class="factory-text">
                <h3 data-lang="zh">我們的工廠與實力</h3>
                <h3 data-lang="en" style="display: none;">Our Factories & Strength</h3>
                <ul class="factory-list">
                    <li data-lang="zh">位於中國廣東和福建地區</li>
                    <li data-lang="en" style="display: none;">Located in Guangdong and Fujian area, China</li>
                    <li data-lang="zh">牛仔產品主要在廣東工廠生產</li>
                    <li data-lang="en" style="display: none;">Denims are mainly produced in Guangdong factory</li>
                    <li data-lang="zh">梭織和針織產品在福建工廠生產</li>
                    <li data-lang="en" style="display: none;">Woven and knits are produced in Fujian factories</li>
                    <li data-lang="zh">超過4000平方米的工業廠房</li>
                    <li data-lang="en" style="display: none;">Over 4000 square meters of industrial complex</li>
                    <li data-lang="zh">獲得BSCI / SA8000國際認證</li>
                    <li data-lang="en" style="display: none;">BSCI / SA8000 international certification obtained</li>
                    <li data-lang="zh">引入智能懸掛系統進行生產</li>
                    <li data-lang="en" style="display: none;">Introduced intelligent hanger system for production</li>
                </ul>
            </div>
            <div class="factory-img">
                <img src="https://picsum.photos/400/300?random=201" alt="工廠外觀" loading="lazy">
                <img src="https://picsum.photos/400/300?random=202" alt="智能懸掛系統" loading="lazy">
                <img src="https://picsum.photos/400/300?random=203" alt="BSCI認證證書" loading="lazy">
            </div>
        </div>
    </section>

    <!-- 核心优势 -->
    <section id="advantage">
        <h2 class="section-title" data-lang="zh">核心優勢</h2>
        <h2 class="section-title" data-lang="en" style="display: none;">Advantage</h2>
        <div class="advantage-grid">
            <div class="advantage-card">
                <i class="fa fa-cogs"></i>
                <h3 data-lang="zh">綜合生產能力</h3>
                <h3 data-lang="en" style="display: none;">Comprehensive Production Capacity</h3>
                <p data-lang="zh">三家工廠可覆蓋大部分梭織和針織產品類型，滿足多樣化的產品定製需求。</p>
                <p data-lang="en" style="display: none;">Three factories can cover most type of woven and knit items, meeting diverse product customization needs.</p>
            </div>
            <div class="advantage-card">
                <i class="fa fa-users"></i>
                <h3 data-lang="zh">資深業務團隊</h3>
                <h3 data-lang="en" style="display: none;">Experienced Merchandiser Team</h3>
                <p data-lang="zh">熟悉全球市場對質量、面料、創新、價格、準時交付的要求。</p>
                <p data-lang="en" style="display: none;">Familiar with the requirements of the global market in respect to quality, fabric, innovation, price, on-time delivery.</p>
            </div>
        </div>
    </section>

    <!-- 联系我们 -->
    <section id="contact">
        <h2 class="section-title" data-lang="zh">聯繫我們</h2>
        <h2 class="section-title" data-lang="en" style="display: none;">Contact Us</h2>
        <div class="contact-content">
            <div class="contact-info">
                <div class="contact-item">
                    <i class="fa fa-map-marker"></i>
                    <p data-lang="zh">地址：香港新界荃灣柴灣角街34-36號萬達來工業中心1802室</p>
                    <p data-lang="en" style="display: none;">Address: 1802 Million Fortune Industrial Centre, 34-36 Chai Wan Kok Street, Tsuen Wan, New Territories, Hong Kong</p>
                </div>
                <div class="contact-item">
                    <i class="fa fa-phone"></i>
                    <p data-lang="zh">電話：(+852) 26113201</p>
                    <p data-lang="en" style="display: none;">TEL: (+852) 26113201</p>
                </div>
                <div class="contact-item">
                    <i class="fa fa-envelope"></i>
                    <p data-lang="zh">郵箱：<a href="mailto:Wicky@wellyuen.com.hk">Wicky@wellyuen.com.hk</a></p>
                    <p data-lang="en" style="display: none;">EMAIL: <a href="mailto:Wicky@wellyuen.com.hk">Wicky@wellyuen.com.hk</a></p>
                </div>
            </div>
        </div>
    </section>

    <!-- 页脚 -->
    <footer>
        <div class="footer-logo" data-lang="zh">華源製衣有限公司</div>
        <div class="footer-logo" data-lang="en" style="display: none;">Well Yuen Garments Ltd.</div>
        <div class="footer-slogan" data-lang="zh">30年專業服裝生產廠家</div>
        <div class="footer-slogan" data-lang="en" style="display: none;">30 Years of Professional Clothing Manufacturer</div>
        <div class="copyright">© 2025 Well Yuen Garments Ltd. All Rights Reserved.</div>
    </footer>

    <!-- 核心交互脚本（包含中英切换） -->
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // 核心元素获取
            const btnZh = document.getElementById('btn-zh');
            const btnEn = document.getElementById('btn-en');
            const langElements = document.querySelectorAll('[data-lang]');
            const menuToggle = document.querySelector('.menu-toggle');
            const navLinks = document.querySelector('.nav-links');

            // 中英切换核心逻辑
            const switchLang = (targetLang) => {
                if (targetLang === 'zh') {
                    btnZh.classList.add('active');
                    btnEn.classList.remove('active');
                } else {
                    btnEn.classList.add('active');
                    btnZh.classList.remove('active');
                }
                langElements.forEach(el => {
                    el.style.display = el.getAttribute('data-lang') === targetLang ? 'block' : 'none';
                });
                localStorage.setItem('preferredLang', targetLang);
            };

            // 按钮点击事件
            btnZh.addEventListener('click', () => switchLang('zh'));
            btnEn.addEventListener('click', () => switchLang('en'));

            // 初始化语言（优先本地存储，默认中文）
            const preferredLang = localStorage.getItem('preferredLang') || 'zh';
            switchLang(preferredLang);

            // 移动端菜单切换
            menuToggle.addEventListener('click', () => {
                navLinks.classList.toggle('show');
            });

            // 平滑滚动
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href');
                    const targetElement = document.querySelector(targetId);
                    if (targetElement) {
                        targetElement.scrollIntoView({ behavior: 'smooth' });
                        // 移动端点击后关闭菜单
                        if (window.innerWidth <= 768) {
                            navLinks.classList.remove('show');
                        }
                    }
                });
            });

            // 窗口缩放重置菜单
            window.addEventListener('resize', () => {
                if (window.innerWidth > 768) {
                    navLinks.classList.remove('show');
                }
            });
        });
    </script>
</body>
</html>
