<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>AAYUR MILLAN</title>
    <!-- Font Awesome 6 -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: #fefaf2;
            color: #2e241f;
            scroll-behavior: smooth;
        }

        :root {
            --primary-gold: #c27e2e;
            --primary-dark: #9b5e1f;
            --accent-green: #4f6b2c;
            --sand-light: #fff4e6;
            --deep-brown: #3a2a22;
            --pure-white: #ffffff;
        }

        .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 24px;
        }

        .navbar {
            background: var(--pure-white);
            box-shadow: 0 4px 14px rgba(0, 0, 0, 0.03);
            position: sticky;
            top: 0;
            z-index: 100;
            border-bottom: 1px solid #f0e3d0;
        }

        .nav-flex {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 16px 0;
            flex-wrap: wrap;
            gap: 16px;
        }

        .logo h1 {
            font-size: 1.8rem;
            font-weight: 800;
            letter-spacing: -0.5px;
            background: linear-gradient(135deg, #b9671e, #8b4c1a);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
        }

        .logo p {
            font-size: 0.75rem;
            font-weight: 500;
            color: #7a5a44;
            letter-spacing: 0.5px;
        }

        .nav-links {
            display: flex;
            gap: 32px;
            align-items: center;
            flex-wrap: wrap;
        }

        .nav-links a {
            text-decoration: none;
            font-weight: 600;
            color: #3e2c23;
            transition: 0.2s;
        }

        .nav-links a:hover {
            color: var(--primary-gold);
        }

        .btn-order-nav {
            background: var(--primary-gold);
            color: white !important;
            padding: 8px 20px;
            border-radius: 40px;
            font-weight: 600;
        }

        .btn-order-nav:hover {
            background: #a85f1c;
        }

        .hero {
            background: linear-gradient(135deg, #fff3e6 0%, #feecd9 100%);
            border-radius: 48px;
            margin: 32px 0 48px;
            padding: 40px 32px;
            position: relative;
            overflow: hidden;
        }

        .hero-grid {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 32px;
            justify-content: space-between;
        }

        .hero-text {
            flex: 1.2;
        }

        .hero-badge {
            background: #e9dbc9;
            display: inline-block;
            padding: 6px 18px;
            border-radius: 40px;
            font-size: 0.8rem;
            font-weight: 700;
            color: #8b5616;
            margin-bottom: 20px;
        }

        .hero-text h2 {
            font-size: 2.5rem;
            font-weight: 800;
            line-height: 1.2;
            color: var(--deep-brown);
        }

        .hero-highlight {
            color: var(--primary-gold);
            font-size: 3rem;
            display: inline-block;
            margin-top: 8px;
        }

        .pure-premium {
            background: #f3e5d5;
            display: inline-block;
            padding: 5px 16px;
            border-radius: 50px;
            font-weight: 700;
            font-size: 0.9rem;
            margin: 16px 0 12px;
        }

        .hero-features {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin: 24px 0;
        }

        .hero-features span {
            font-size: 0.9rem;
            font-weight: 500;
            background: white;
            padding: 5px 14px;
            border-radius: 30px;
            box-shadow: 0 2px 6px rgba(0,0,0,0.05);
        }

        .hero-right {
            flex: 0.8;
            background: rgba(255,255,235,0.6);
            border-radius: 32px;
            padding: 24px;
            text-align: center;
            backdrop-filter: blur(2px);
            border: 1px solid #ffe1b3;
        }

        .product-image {
            width: 140px;
            height: 140px;
            margin: 0 auto 16px;
            background: linear-gradient(145deg, #ffefcf, #ffe3bc);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 12px 24px rgba(0,0,0,0.1);
        }

        .product-image i {
            font-size: 5rem;
            color: #c27e2e;
            filter: drop-shadow(2px 6px 12px rgba(0,0,0,0.2));
        }

        .product-badge {
            font-size: 0.8rem;
            background: var(--accent-green);
            color: white;
            padding: 4px 14px;
            border-radius: 50px;
            display: inline-block;
        }

        .product-name {
            font-size: 2.7rem;
            font-weight: 800;
            margin: 10px 0;
            letter-spacing: 2px;
        }

        .mrp-price {
            font-size: 2rem;
            font-weight: 800;
            color: #b4531b;
        }

        .net-weight {
            font-weight: 700;
            margin: 10px 0;
            font-size: 1.1rem;
            background: #f9e2c1;
            display: inline-block;
            padding: 4px 16px;
            border-radius: 40px;
        }

        .order-btn {
            background: #d9772b;
            border: none;
            padding: 14px 32px;
            font-size: 1.1rem;
            font-weight: 700;
            border-radius: 60px;
            color: white;
            cursor: pointer;
            margin-top: 16px;
            transition: 0.2s;
            box-shadow: 0 6px 14px rgba(193, 110, 29, 0.3);
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }

        .order-btn:hover {
            background: #b55f1f;
            transform: scale(1.02);
        }

        .features-highlight {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 24px;
            margin: 60px 0;
        }

        .feature-card {
            background: white;
            padding: 22px 16px;
            border-radius: 28px;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0,0,0,0.02);
            border: 1px solid #f3e2d0;
            transition: 0.2s;
        }

        .feature-card i {
            font-size: 2.2rem;
            color: var(--primary-gold);
            margin-bottom: 12px;
        }

        .feature-card h4 {
            font-size: 1.2rem;
            margin-bottom: 6px;
        }

        .purity-showcase {
            background: #fef6ea;
            border-radius: 48px;
            padding: 48px 32px;
            margin: 40px 0;
        }

        .purity-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 32px;
            justify-content: space-between;
        }

        .purity-left {
            flex: 1;
        }

        .purity-left h3 {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 18px;
        }

        .badge-list {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin: 20px 0;
        }

        .badge-list span {
            background: white;
            padding: 8px 18px;
            border-radius: 50px;
            font-weight: 600;
            font-size: 0.85rem;
            box-shadow: 0 1px 3px rgba(0,0,0,0.05);
        }

        .made-badge {
            background: #e6d5bd;
            display: inline-block;
            padding: 8px 20px;
            border-radius: 40px;
            font-weight: 700;
            margin-top: 10px;
        }

        .product-specs {
            margin-top: 30px;
        }

        .spec-row {
            display: flex;
            justify-content: space-between;
            border-bottom: 1px dashed #decbae;
            padding: 10px 0;
        }

        .launch-offer {
            background: #2c4c2c;
            background-image: radial-gradient(circle at 10% 30%, #416b2b, #1f3b1a);
            border-radius: 38px;
            padding: 32px 28px;
            color: white;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            margin: 48px 0;
        }

        .offer-text h3 {
            font-size: 1.8rem;
            font-weight: 800;
        }

        .offer-text p {
            font-size: 1.2rem;
            margin-top: 8px;
        }

        .free-delivery {
            background: #ffbc6e;
            padding: 10px 24px;
            border-radius: 60px;
            font-weight: bold;
            color: #2a2a1c;
        }

        .footer {
            background: #2b241f;
            color: #e6dacf;
            padding: 48px 0 24px;
            margin-top: 60px;
            border-radius: 40px 40px 0 0;
        }

        .footer-grid {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 32px;
        }

        .contact-social i {
            font-size: 1.6rem;
            margin-right: 16px;
            color: #dbaa6b;
        }

        .insta-handle {
            margin-top: 12px;
            background: #3f322a;
            display: inline-block;
            padding: 8px 20px;
            border-radius: 30px;
            transition: 0.2s;
        }

        .insta-handle a {
            color: #dbaa6b;
            text-decoration: none;
            font-weight: 500;
        }

        .insta-handle a:hover {
            color: #ffbc6e;
            text-decoration: underline;
        }

        .copyright {
            text-align: center;
            margin-top: 40px;
            font-size: 0.8rem;
            border-top: 1px solid #4d3c31;
            padding-top: 24px;
        }

        @media (max-width: 750px) {
            .hero-text h2 {
                font-size: 1.8rem;
            }
            .product-name {
                font-size: 2rem;
            }
            .nav-flex {
                flex-direction: column;
            }
            .hero-grid {
                flex-direction: column;
            }
            .product-image {
                width: 100px;
                height: 100px;
            }
            .product-image i {
                font-size: 3.5rem;
            }
        }

        button {
            background: none;
            border: none;
        }

        .weight-update-note {
            font-size: 0.7rem;
            background: #fff0d8;
            display: inline-block;
            padding: 2px 12px;
            border-radius: 30px;
            margin-left: 8px;
        }
    </style>
</head>
<body>

<header class="navbar">
    <div class="container nav-flex">
        <div class="logo">
            <h1>AAYUR MILLAN</h1>
            <p>100% PURE · FARM to KITCHEN</p>
        </div>
        <div class="nav-links">
            <a href="#">Home</a>
            <a href="#product">Product</a>
            <a href="#purity">Purity</a>
            <a href="#contact">Contact</a>
            <a href="#" class="btn-order-nav" id="navOrderBtn">Order Now</a>
        </div>
    </div>
</header>

<main>
    <div class="container">
        <!-- Hero section - NET WT 100g, MRP ₹75 + IMAGE -->
        <div class="hero">
            <div class="hero-grid">
                <div class="hero-text">
                    <div class="hero-badge">✨ Finally Our ✨</div>
                    <h2>PURE & PREMIUM <br> <span class="hero-highlight">100% HALDI</span></h2>
                    <div class="pure-premium">
                        <i class="fas fa-leaf"></i> NATURAL · PURE & PREMIUM
                    </div>
                    <p style="font-weight: 500; margin: 12px 0 8px;">🌿 From Our FARMS to Your KITCHEN</p>
                    <div class="hero-features">
                        <span><i class="fas fa-ban"></i> NO ADDED COLOR</span>
                        <span><i class="fas fa-flask"></i> CHEMICAL FREE</span>
                        <span><i class="fas fa-prescription-bottle"></i> NO PRESERVATIVES</span>
                        <span><i class="fas fa-spa"></i> AYURVEDIC PRODUCT</span>
                    </div>
                </div>
                <div class="hero-right" id="product">
                    <div class="product-image">
                        <i class="fas fa-mortar-pestle"></i>
                    </div>
                    <span class="product-badge"><i class="fas fa-certificate"></i> 100% PURE</span>
                    <div class="product-name">HALDI<br>(Turmeric)</div>
                    <div class="mrp-price">MRP: ₹75</div>
                    <div class="net-weight">
                        <i class="fas fa-weight-hanging"></i> NET WT. 100g
                        <span class="weight-update-note">✨ Premium 100g pack</span>
                    </div>
                    <div class="hero-features" style="justify-content: center; margin: 12px 0 0;">
                        <span>RICH IN CURCUMIN</span>
                        <span>BOOSTS IMMUNITY</span>
                    </div>
                    <button class="order-btn" id="heroOrderBtn">
                        <i class="fab fa-whatsapp"></i> ORDER NOW
                    </button>
                    <div style="margin-top: 14px; font-size: 0.75rem; font-weight: 500;">FREE DELIVERY on orders above 1KG</div>
                </div>
            </div>
        </div>

        <!-- Trust badges -->
        <div class="features-highlight">
            <div class="feature-card">
                <i class="fas fa-tractor"></i>
                <h4>FRESH FROM FARMS</h4>
                <p>Harvested directly, no middlemen</p>
            </div>
            <div class="feature-card">
                <i class="fas fa-check-circle"></i>
                <h4>PREMIUM QUALITY</h4>
                <p>Lab tested & premium grade</p>
            </div>
            <div class="feature-card">
                <i class="fas fa-box-open"></i>
                <h4>FRESHLY PACKED</h4>
                <p>Hygienic packing, farm-fresh seal</p>
            </div>
            <div class="feature-card">
                <i class="fas fa-users"></i>
                <h4>TRUSTED BY MANY</h4>
                <p>Thousands of happy families</p>
            </div>
        </div>

        <!-- Purity section -->
        <div id="purity" class="purity-showcase">
            <div class="purity-grid">
                <div class="purity-left">
                    <h3>Shuddh Haldi, Swasth Zindagi</h3>
                    <p><strong>100% Pure & Natural Curcumin</strong> — No adulteration, just the golden goodness of nature. Our turmeric is grown in rich Indian soil and processed without any chemicals.</p>
                    <div class="badge-list">
                        <span><i class="fas fa-vial"></i> CHEMICAL FREE</span>
                        <span><i class="fas fa-heartbeat"></i> BOOSTS IMMUNITY</span>
                        <span><i class="fas fa-sun"></i> GOOD FOR SKIN & HEALTH</span>
                        <span><i class="fas fa-mortar-pestle"></i> AYURVEDIC PRODUCT</span>
                    </div>
                    <div class="made-badge">
                        🇮🇳 MADE IN INDIA | RICH IN CURCUMIN
                    </div>
                    <div class="product-specs">
                        <div class="spec-row"><span>✅ No added colour / preservatives</span><span>✨ 100% Natural</span></div>
                        <div class="spec-row"><span>✅ Premium high curcumin content</span><span>🌱 Supports digestion & glow</span></div>
                        <div class="spec-row"><span>✅ Farm to kitchen traceability</span><span>🚫 GMO FREE</span></div>
                        <div class="spec-row"><span>📦 NET WT. 100g PACK</span><span>💰 MRP ₹75 only</span></div>
                    </div>
                </div>
                <div style="flex: 0.8; background: #fff3e2; border-radius: 32px; padding: 22px; text-align: center;">
                    <i class="fas fa-seedling" style="font-size: 3rem; color:#c27e2e;"></i>
                    <h3 style="margin: 12px 0;">100% <br>PURE & PREMIUM</h3>
                    <p style="font-weight: 500;">"From our farms to your kitchen — purity delivered."</p>
                    <div style="margin-top: 20px;"><span class="product-badge" style="background:#d88c3a;">⭐ 100% PURE HALDI ⭐</span></div>
                </div>
            </div>
        </div>

        <!-- Launch Offer -->
        <div class="launch-offer">
            <div class="offer-text">
                <h3>🎉 LAUNCH OFFER 🎉</h3>
                <p>Get AAYUR MILLAN Pure Haldi at special price <strong>₹75 (100g pack)</strong></p>
                <p><i class="fas fa-truck"></i> FREE DELIVERY on orders above 1KG</p>
                <p style="font-size: 0.9rem;">✨ No hidden charges · Limited period offer</p>
            </div>
            <div class="free-delivery">
                <i class="fas fa-shipping-fast"></i> FREE SHIPPING > 1KG
            </div>
        </div>

        <!-- Contact Section - Email ID REMOVED -->
        <div id="contact" style="background: #FAF1E4; border-radius: 40px; padding: 32px 28px; margin: 32px 0;">
            <div style="display: flex; flex-wrap: wrap; justify-content: space-between; align-items: center; gap: 24px;">
                <div>
                    <h3 style="font-size: 1.6rem;">Order Now — ₹75 (100g)</h3>
                    <p style="margin: 8px 0;">📞 Call / WhatsApp: <strong>9253302669</strong></p>
                    <div class="insta-handle" style="background:#dac09f; color:#281f1a;">
                        <i class="fab fa-instagram"></i> 
                        <a href="https://www.instagram.com/aayurmilanindia?igsh=MW5uZTB3cDJweGduYQ==" target="_blank" style="color:#281f1a; font-weight:600;">
                            DM us on Instagram: @aayurmilanindia
                        </a>
                    </div>
                    <p style="margin-top: 16px;"><i class="fas fa-map-marker-alt"></i> Direct from ethical farms to your doorstep</p>
                </div>
                <div>
                    <button class="order-btn" id="whatsappOrderBtn" style="background: #25D366; box-shadow: none;">
                        <i class="fab fa-whatsapp"></i> Order via WhatsApp
                    </button>
                    <p style="font-size: 12px; margin-top: 8px;">Click to place your order for 100g pack</p>
                </div>
            </div>
        </div>
    </div>
</main>

<footer class="footer">
    <div class="container footer-grid">
        <div>
            <h3>AAYUR MILLAN</h3>
            <p>100% Pure Products · Farm to Kitchen</p>
            <p style="margin-top: 10px;">🌱 Chemical Free | No Preservatives | Ayurvedic</p>
        </div>
        <div class="contact-social">
            <p><i class="fab fa-whatsapp"></i> +91 9253302669</p>
            <p><i class="fab fa-instagram"></i> 
                <a href="https://www.instagram.com/aayurmilanindia?igsh=MW5uZTB3cDJweGduYQ==" target="_blank" style="color:#dbaa6b; text-decoration:none;">
                    @aayurmilanindia
                </a>
            </p>
            <div class="insta-handle" style="background: none; padding-left: 0;">
                📢 <a href="https://www.instagram.com/aayurmilanindia?igsh=MW5uZTB3cDJweGduYQ==" target="_blank" style="color:#dbaa6b;">DM on Instagram</a> for bulk orders
            </div>
        </div>
        <div>
            <p>✨ Pure & Premium Haldi (100g)<br>Rich in Curcumin | Immunity Booster</p>
            <p>🇮🇳 Made in India | MRP ₹75</p>
        </div>
    </div>
    <div class="container copyright">
        <p>© 2026 AAYUR MILLAN — 100% Natural Farm to Kitchen | Shuddh Haldi, Swasth Zindagi | 100g Pack at ₹75</p>
    </div>
</footer>

<script>
    // WhatsApp ordering with phone number 9253302669, product 100g
    function sendWhatsAppOrder() {
        const phone = "9253302669";
        const productName = "AAYUR MILLAN 100% Pure Haldi (Turmeric)";
        const weight = "100g";
        const mrp = "₹75";
        const message = `Hello AAYUR MILLAN, I want to order ${productName} - ${weight} pack. MRP ${mrp}. Please share payment and delivery details.`;
        const encodedMsg = encodeURIComponent(message);
        const whatsappUrl = `https://wa.me/${phone}?text=${encodedMsg}`;
        window.open(whatsappUrl, '_blank');
    }

    const heroBtn = document.getElementById('heroOrderBtn');
    const navBtn = document.getElementById('navOrderBtn');
    const whatsappSpecific = document.getElementById('whatsappOrderBtn');

    if (heroBtn) heroBtn.addEventListener('click', sendWhatsAppOrder);
    if (navBtn) navBtn.addEventListener('click', sendWhatsAppOrder);
    if (whatsappSpecific) whatsappSpecific.addEventListener('click', sendWhatsAppOrder);

    // Smooth scrolling for anchor links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function(e) {
            const href = this.getAttribute('href');
            if (href === "#" || href === "") return;
            const targetId = href.substring(1);
            const targetElement = document.getElementById(targetId);
            if (targetElement) {
                e.preventDefault();
                targetElement.scrollIntoView({ behavior: 'smooth' });
            }
        });
    });
</script>
</body>
</html>
