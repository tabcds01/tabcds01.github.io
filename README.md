<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>華源製衣有限公司 - 专业服装生产厂家</title>
    <!-- 引入字体和图标 -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* 全局样式 - 核心配色 */
        :root {
            --primary: #2D3748; /* 深灰蓝-主色 */
            --accent1: #E53E3E; /* 砖红-辅助色1 */
            --accent2: #48BB78; /* 浅绿-辅助色2 */
            --neutral1: #F7FAFC; /* 浅灰白-背景 */
            --neutral2: #718096; /* 中灰-副文本 */
            --neutral3: #1A202C; /* 纯深灰-大标题 */
            --white: #FFFFFF;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', '微软雅黑', '思源黑体', sans-serif;
        }

        body {
            background-color: var(--neutral1);
            color: var(--neutral3);
            line-height: 1.8;
        }

        /* 导航栏样式 */
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
        }

        .logo {
            font-size: 1.25rem;
            font-weight: bold;
            color: var(--primary);
        }

        .nav-links {
            display: flex;
            gap: 2rem;
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

        .lang-switch {
            display: flex;
            gap: 1rem;
        }

        .lang-switch button {
            border: none;
            background: none;
            color: var(--neutral3);
            cursor: pointer;
            font-size: 0.875rem;
        }

        .lang-switch button.active {
            color: var(--primary);
            font-weight: bold;
        }

        /* 移动端菜单 */
        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* 通用板块样式 */
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

        /* 首屏Banner */
        #home {
            height: 100vh;
            display: flex;
            align-items: center;
            padding-top: 0;
            padding-bottom: 0;
        }

        .banner {
            display: flex;
            width: 100%;
            gap: 2rem;
        }

        .banner-text {
            flex: 6;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .banner-text h1 {
            font-size: 2.25rem;
            color: var(--neutral3);
            margin-bottom: 1rem;
        }

        .banner-text h2 {
            font-size: 1.5rem;
            color: var(--primary);
            font-weight: bold;
            margin-bottom: 1.5rem;
        }

        .banner-text p {
            font-size: 1rem;
            color: var(--neutral2);
            margin-bottom: 2rem;
            max-width: 80%;
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
            flex: 4;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .banner-img img {
            width: 100%;
            height: auto;
            border-radius: 8px;
        }

        /* 公司介绍 */
        #about {
            background-color: var(--white);
        }

        .about-content {
            max-width: 80%;
            margin: 0 auto;
            text-align: center;
            font-size: 1rem;
            color: var(--neutral3);
        }

        /* 产品中心 */
        #products {
            background-color: var(--neutral1);
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .product-card {
            background-color: var(--white);
            border-radius: 8px;
            overflow: hidden;
            transition: border 0.3s;
        }

        .product-card:hover {
            border: 2px solid var(--primary);
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
            color: var(--neutral3);
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
            max-width: 80%;
            margin: 0 auto;
        }

        .process-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 1.5rem;
            padding-bottom: 1.5rem;
            border-bottom: 1px solid var(--neutral2);
        }

        .process-item:last-child {
            border-bottom: none;
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
            color: var(--neutral3);
        }

        /* 工厂实力 */
        #factory {
            background-color: var(--neutral1);
        }

        .factory-content {
            display: flex;
            gap: 2rem;
            align-items: center;
        }

        .factory-text {
            flex: 1;
        }

        .factory-text h3 {
            font-size: 1.25rem;
            color: var(--primary);
            font-weight: bold;
            margin-bottom: 1.5rem;
        }

        .factory-list {
            list-style: none;
        }

        .factory-list li {
            font-size: 0.875rem;
            color: var(--neutral3);
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
            display: grid;
            grid-template-columns: repeat(3, 1fr);
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
            grid-template-columns: repeat(2, 1fr);
            gap: 2rem;
            max-width: 80%;
            margin: 0 auto;
        }

        .advantage-card {
            background-color: var(--neutral1);
            border-radius: 8px;
            padding: 2rem;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .advantage-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 4px 8px rgba(45,55,72,0.1);
        }

        .advantage-card i {
            font-size: 1.5rem;
            color: var(--accent2);
            margin-bottom: 1rem;
        }

        .advantage-card h3 {
            font-size: 1rem;
            color: var(--primary);
            font-weight: bold;
            margin-bottom: 1rem;
        }

        .advantage-card p {
            font-size: 0.875rem;
            color: var(--neutral2);
        }

        /* 客户案例 */
        #clients {
            background-color: var(--neutral1);
        }

        .clients-grid {
            display: grid;
            grid-template-columns: repeat(5, 1fr);
            gap: 1.5rem;
            max-width: 90%;
            margin: 0 auto;
        }

        .client-logo {
            background-color: var(--white);
            padding: 1rem;
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            filter: grayscale(100%);
            transition: filter 0.3s;
        }

        .client-logo:hover {
            filter: grayscale(0);
        }

        .client-logo img {
            max-width: 100px;
            max-height: 50px;
            object-fit: contain;
        }

        /* 联系我们 */
        #contact {
            background-color: var(--white);
        }

        .contact-content {
            display: flex;
            gap: 2rem;
            max-width: 90%;
            margin: 0 auto;
        }

        .contact-info {
            flex: 1;
        }

        .contact-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 1.5rem;
        }

        .contact-item i {
            color: var(--primary);
            margin-right: 1rem;
            margin-top: 0.25rem;
            flex-shrink: 0;
        }

        .contact-item p {
            font-size: 0.875rem;
            color: var(--neutral3);
        }

        .contact-item a {
            color: #0066cc;
            text-decoration: none;
        }

        .contact-form {
            flex: 1;
            background-color: var(--neutral1);
            padding: 2rem;
            border-radius: 8px;
        }

        .contact-form h3 {
            font-size: 1rem;
            color: var(--primary);
            font-weight: bold;
            margin-bottom: 1.5rem;
        }

        .form-group {
            margin-bottom: 1rem;
        }

        .form-group label {
            display: block;
            font-size: 0.75rem;
            color: var(--neutral3);
            margin-bottom: 0.5rem;
        }

        .form-group input, .form-group textarea {
            width: 100%;
            padding: 0.75rem;
            border: 1px solid var(--neutral2);
            border-radius: 4px;
            font-size: 0.875rem;
            color: var(--neutral3);
        }

        .form-group textarea {
            height: 150px;
            resize: none;
        }

        /* 页脚 */
        footer {
            background-color: var(--primary);
            color: var(--white);
            padding: 3rem 5%;
            text-align: center;
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
        @media (max-width: 1024px) {
            .products-grid {
                grid-template-columns: repeat(3, 1fr);
            }
            .clients-grid {
                grid-template-columns: repeat(4, 1fr);
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            .menu-toggle {
                display: block;
            }
            .banner {
                flex-direction: column;
            }
            .banner-text h1 {
                font-size: 1.75rem;
            }
            .banner-text h2 {
                font-size: 1.25rem;
            }
            .banner-text p {
                max-width: 100%;
            }
            .products-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            .factory-content {
                flex-direction: column;
            }
            .advantage-grid {
                grid-template-columns: 1fr;
                max-width: 100%;
            }
            .clients-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            .contact-content {
                flex-direction: column;
            }
        }

        @media (max-width: 480px) {
            .products-grid {
                grid-template-columns: 1fr;
            }
            .clients-grid {
                grid-template-columns: 1fr;
            }
            .factory-img {
                grid-template-columns: 1fr;
            }
            section {
                padding: 3rem 5%;
            }
        }
    </style>
</head>
<body>
    <!-- 导航栏 -->
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
            
            <a href="#clients" data-lang="zh">客戶案例</a>
            <a href="#clients" data-lang="en" style="display: none;">Clients</a>
            
            <a href="#contact" data-lang="zh">聯繫我們</a>
            <a href="#contact" data-lang="en" style="display: none;">Contact Us</a>
        </div>
        
        <div class="lang-switch">
            <button id="btn-zh" class="active">中</button>
            <button id="btn-en">EN</button>
        </div>
        
        <div class="menu-toggle">
            <i class="fas fa-bars"></i>
        </div>
    </nav>

    <!-- 首屏Banner -->
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
                <!-- 替换为你的产品主图 -->
                <img src="https://picsum.photos/800/600?random=1" alt="服裝產品展示">
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
                <img src="https://picsum.photos/400/300?random=2" alt="夾克">
                <p data-lang="zh">夾克</p>
                <p data-lang="en" style="display: none;">Jacket</p>
            </div>
            <div class="product-card">
                <img src="https://picsum.photos/400/300?random=3" alt="大衣">
                <p data-lang="zh">大衣</p>
                <p data-lang="en" style="display: none;">Coats</p>
            </div>
            <div class="product-card">
                <img src="https://picsum.photos/400/300?random=4" alt="牛仔">
                <p data-lang="zh">牛仔</p>
                <p data-lang="en" style="display: none;">Jeans</p>
            </div>
            <div class="product-card">
                <img src="https://picsum.photos/400/300?random=5" alt="毛衣">
                <p data-lang="zh">毛衣</p>
                <p data-lang="en" style="display: none;">Sweaters</p>
            </div>
            <div class="product-card">
                <img src="https://picsum.photos/400/300?random=6" alt="針織服裝">
                <p data-lang="zh">針織服裝</p>
                <p data-lang="en" style="display: none;">Knitted Garments</p>
            </div>
            <div class="product-card">
                <img src="https://picsum.photos/400/300?random=7" alt="梭織服裝">
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
                <!-- 替换为你的工厂图片 -->
                <img src="https://picsum.photos/400/300?random=8" alt="工廠外觀">
                <img src="https://picsum.photos/400/300?random=9" alt="智能懸掛系統">
                <img src="https://picsum.photos/400/300?random=10" alt="認證證書">
            </div>
        </div>
    </section>

    <!-- 核心优势 -->
    <section id="advantage">
        <h2 class="section-title" data-lang="zh">核心優勢</h2>
        <h2 class="section-title" data-lang="en" style="display: none;">Advantage</h2>
        
        <div class="advantage-grid">
            <div class="advantage-card">
                <i class="fas fa-cogs"></i>
                <h3 data-lang="zh">綜合生產能力</h3>
                <h3 data-lang="en" style="display: none;">Comprehensive Production Capacity</h3>
                
                <p data-lang="zh">三家工廠可覆蓋大部分梭織和針織產品類型，滿足多樣化的產品定製需求。</p>
                <p data-lang="en" style="display: none;">Three factories can cover most type of woven and knit items, meeting diverse product customization needs.</p>
            </div>
            <div class="advantage-card">
                <i class="fas fa-users"></i>
                <h3 data-lang="zh">資深業務團隊</h3>
                <h3 data-lang="en" style="display: none;">Experienced Merchandiser Team</h3>
                
                <p data-lang="zh">熟悉全球市場對質量、面料、創新、價格、準時交付的要求。</p>
                <p data-lang="en" style="display: none;">Familiar with the requirements of the global market in respect to quality, fabric, innovation, price, on-time delivery.</p>
            </div>
        </div>
    </section>

    <!-- 客户案例 -->
    <section id="clients">
        <h2 class="section-title" data-lang="zh">客戶案例</h2>
        <h2 class="section-title" data-lang="en" style="display: none;">Clients</h2>
        
        <div class="clients-grid">
            <!-- 替换为你的客户logo -->
            <div class="client-logo"><img src="https://picsum.photos/200/100?random=11" alt="BALR."></div>
            <div class="client-logo"><img src="https://picsum.photos/200/100?random=12" alt="SEBAGO"></div>
            <div class="client-logo"><img src="https://picsum.photos/200/100?random=13" alt="BACKTEE"></div>
            <div class="client-logo"><img src="https://picsum.photos/200/100?random=14" alt="graniph&MOOMIN"></div>
            <div class="client-logo"><img src="https://picsum.photos/200/100?random=15" alt="OA Dee"></div>
            <div class="client-logo"><img src="https://picsum.photos/200/100?random=16" alt="mitch&son"></div>
            <div class="client-logo"><img src="https://picsum.photos/200/100?random=17" alt="C/MEO"></div>
            <div class="client-logo"><img src="https://picsum.photos/200/100?random=18" alt="PROTEST"></div>
            <div class="client-logo"><img src="https://picsum.photos/200/100?random=19" alt="claudia strater"></div>
            <div class="client-logo"><img src="https://picsum.photos/200/100?random=20" alt="So Soire"></div>
        </div>
    </section>

    <!-- 联系我们 -->
    <section id="contact">
        <h2 class="section-title" data-lang="zh">聯繫我們</h2>
        <h2 class="section-title" data-lang="en" style="display: none;">Contact Us</h2>
        
        <div class="contact-content">
            <div class="contact-info">
                <div class="contact-item">
                    <i class="fas fa-map-marker-alt"></i>
                    <p data-lang="zh">地址：香港新界荃灣柴灣角街34-36號萬豐工業中心1802室</p>
                    <p data-lang="en" style="display: none;">Address: 1802 Million Fortune Industrial Centre, 34-36 Chai Wan Kok Street,Tsuen Wan, New Territories, Hong Kong</p>
                </div>
                <div class="contact-item">
                    <i class="fas fa-phone"></i>
                    <p data-lang="zh">電話：(+852) 26113201</p>
                    <p data-lang="en" style="display: none;">Phone: (+852) 26113201</p>
                </div>
                <div class="contact-item">
                    <i class="fas fa-envelope"></i>
                    <p data-lang="zh">郵箱：<a href="mailto:Wicky@wellyuen.com.hk">Wicky@wellyuen.com.hk</a></p>
                    <p data-lang="en" style="display: none;">Email: <a href="mailto:Wicky@wellyuen.com.hk">Wicky@wellyuen.com.hk</a></p>
                </div>
            </div>
            <div class="contact-form">
                <h3 data-lang="zh">發送咨詢</h3>
                <h3 data-lang="en" style="display: none;">Send Inquiry</h3>
                
                <form>
                    <div class="form-group">
                        <label data-lang="zh">姓名</label>
                        <label data-lang="en" style="display: none;">Name</label>
                        <input type="text" placeholder="請輸入您的姓名">
                    </div>
                    <div class="form-group">
                        <label data-lang="zh">郵箱</label>
                        <label data-lang="en" style="display: none;">Email</label>
                        <input type="email" placeholder="請輸入您的郵箱">
                    </div>
                    <div class="form-group">
                        <label data-lang="zh">需求描述</label>
                        <label data-lang="en" style="display: none;">Message</label>
                        <textarea placeholder="請詳細描述您的需求"></textarea>
                    </div>
                    <button type="submit" class="btn" data-lang="zh">提交</button>
                    <button type="submit" class="btn" data-lang="en" style="display: none;">Submit</button>
                </form>
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

    <!-- 脚本 - 双语切换 + 平滑滚动 -->
    <script>
        // 双语切换功能
        const btnZh = document.getElementById('btn-zh');
        const btnEn = document.getElementById('btn-en');
        const langElements = document.querySelectorAll('[data-lang]');

        // 切换到中文
        btnZh.addEventListener('click', () => {
            btnZh.classList.add('active');
            btnEn.classList.remove('active');
            
            langElements.forEach(el => {
                if (el.getAttribute('data-lang') === 'zh') {
                    el.style.display = 'block';
                } else {
                    el.style.display = 'none';
                }
            });
        });

        // 切换到英文
        btnEn.addEventListener('click', () => {
            btnEn.classList.add('active');
            btnZh.classList.remove('active');
            
            langElements.forEach(el => {
                if (el.getAttribute('data-lang') === 'en') {
                    el.style.display = 'block';
                } else {
                    el.style.display = 'none';
                }
            });
        });

        // 平滑滚动
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // 移动端菜单（简化版，如需完整功能可扩展）
        const menuToggle = document.querySelector('.menu-toggle');
        const navLinks = document.querySelector('.nav-links');
        
        menuToggle.addEventListener('click', () => {
            navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
            navLinks.style.flexDirection = 'column';
            navLinks.style.position = 'absolute';
            navLinks.style.top = '80px';
            navLinks.style.right = '5%';
            navLinks.style.background = 'white';
            navLinks.style.padding = '2rem';
            navLinks.style.boxShadow = '0 2px 8px rgba(0,0,0,0.1)';
            navLinks.style.borderRadius = '4px';
        });
    </script>
</body>
</html>
