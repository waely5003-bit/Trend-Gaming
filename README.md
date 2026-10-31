<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Trend Gaming Center - المرج</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;900&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Cairo', sans-serif;
        }

        body {
            /* خلفية ملونة وساحرة تدمج بين تدرجات النيون والجيمنج */
            background: linear-gradient(135deg, #0d0221 0%, #190933 35%, #2c0c4d 70%, #4a0e4e 100%);
            background-attachment: fixed;
            color: #ffffff;
            min-height: 100vh;
            overflow-x: hidden;
        }

        /* تأثير إضاءات خلفية ملونة متحركة */
        body::before {
            content: '';
            position: fixed;
            top: -20%;
            left: -20%;
            width: 60vw;
            height: 60vw;
            background: radial-gradient(circle, rgba(0, 243, 255, 0.15) 0%, rgba(131, 56, 236, 0.05) 50%, transparent 70%);
            z-index: -1;
            filter: blur(80px);
        }

        body::after {
            content: '';
            position: fixed;
            bottom: -20%;
            right: -20%;
            width: 60vw;
            height: 60vw;
            background: radial-gradient(circle, rgba(255, 0, 128, 0.15) 0%, rgba(131, 56, 236, 0.05) 50%, transparent 70%);
            z-index: -1;
            filter: blur(80px);
        }

        /* الهيدر وشريط التنقل */
        header {
            background: rgba(13, 2, 33, 0.85);
            backdrop-filter: blur(12px);
            border-bottom: 1px solid rgba(0, 243, 255, 0.2);
            position: sticky;
            top: 0;
            z-index: 1000;
            padding: 15px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo-area {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo-area h1 {
            font-size: 1.5rem;
            font-weight: 900;
            background: linear-gradient(45deg, #00f3ff, #ff007f);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 20px rgba(0, 243, 255, 0.4);
        }

        nav {
            display: flex;
            gap: 20px;
            align-items: center;
        }

        nav a {
            color: #b8c1ec;
            text-decoration: none;
            font-weight: 600;
            font-size: 0.95rem;
            transition: 0.3s;
        }

        nav a:hover {
            color: #00f3ff;
            text-shadow: 0 0 10px rgba(0, 243, 255, 0.8);
        }

        .cta-nav {
            background: linear-gradient(45deg, #00f3ff, #7000ff);
            color: #fff !important;
            padding: 8px 20px;
            border-radius: 30px;
            box-shadow: 0 0 15px rgba(0, 243, 255, 0.4);
        }

        /* المحتوى الرئيسي */
        .container {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 30px;
        }

        @media(max-width: 900px) {
            .container {
                grid-template-columns: 1fr;
            }
        }

        .hero-card {
            background: rgba(25, 12, 51, 0.7);
            backdrop-filter: blur(15px);
            border: 1px solid rgba(131, 56, 236, 0.4);
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5), inset 0 0 20px rgba(0, 243, 255, 0.1);
            position: relative;
            overflow: hidden;
        }

        .hero-card::before {
            content: '';
            position: absolute;
            top: 0; right: 0; width: 100%; height: 4px;
            background: linear-gradient(90deg, #00f3ff, #ff007f, #7000ff);
        }

        .badge {
            display: inline-block;
            background: rgba(0, 243, 255, 0.1);
            color: #00f3ff;
            border: 1px solid rgba(0, 243, 255, 0.3);
            padding: 6px 15px;
            border-radius: 20px;
            font-size: 0.85rem;
            margin-bottom: 20px;
            box-shadow: 0 0 10px rgba(0, 243, 255, 0.2);
        }

        h2 {
            font-size: 2.5rem;
            font-weight: 900;
            margin-bottom: 15px;
            background: linear-gradient(45deg, #ffffff, #00f3ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        p {
            color: #b8c1ec;
            font-size: 1.05rem;
            line-height: 1.6;
            margin-bottom: 30px;
        }

        /* كروت المميزات والأسعار */
        .features-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
            margin-bottom: 30px;
        }

        .feature-box {
            background: rgba(13, 2, 33, 0.6);
            border: 1px solid rgba(255, 255, 255, 0.1);
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            transition: 0.3s;
        }

        .feature-box:hover {
            border-color: #00f3ff;
            box-shadow: 0 0 20px rgba(0, 243, 255, 0.3);
            transform: translateY(-5px);
        }

        .feature-box h4 {
            color: #00f3ff;
            font-size: 1.2rem;
            margin-bottom: 5px;
        }

        .feature-box span {
            color: #ff007f;
            font-weight: 700;
            font-size: 0.9rem;
        }

        /* الأزرار */
        .btn-group {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }

        .btn {
            padding: 12px 25px;
            border-radius: 12px;
            font-weight: 700;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            transition: 0.3s;
            cursor: pointer;
        }

        .btn-primary {
            background: linear-gradient(45deg, #00f3ff, #0077ff);
            color: #fff;
            box-shadow: 0 0 20px rgba(0, 243, 255, 0.4);
        }

        .btn-primary:hover {
            box-shadow: 0 0 30px rgba(0, 243, 255, 0.8);
            transform: scale(1.05);
        }

        .btn-secondary {
            background: linear-gradient(45deg, #ff007f, #8338ec);
            color: #fff;
            box-shadow: 0 0 20px rgba(255, 0, 127, 0.4);
        }

        .btn-secondary:hover {
            box-shadow: 0 0 30px rgba(255, 0, 127, 0.8);
            transform: scale(1.05);
        }

        /* الجانب الأيمن / البطولات */
        .side-card {
            background: linear-gradient(135deg, rgba(131, 56, 236, 0.2), rgba(255, 0, 127, 0.1));
            backdrop-filter: blur(15px);
            border: 2px solid rgba(255, 0, 127, 0.4);
            border-radius: 20px;
            padding: 30px;
            box-shadow: 0 0 30px rgba(255, 0, 127, 0.2);
        }

        .side-card h3 {
            color: #ff007f;
            font-size: 1.5rem;
            margin-bottom: 15px;
            text-shadow: 0 0 10px rgba(255, 0, 127, 0.5);
        }

        .price-list {
            list-style: none;
            margin: 20px 0;
        }

        .price-list li {
            display: flex;
            justify-content: space-between;
            padding: 10px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            font-weight: 600;
        }

        .price-list li span:last-child {
            color: #00f3ff;
        }
    </style>
</head>
<body>

    <header>
        <div class="logo-area">
            <h1>TREND GAMING</h1>
        </div>
        <nav>
            <a href="#">الرئيسية</a>
            <a href="#">أسعار الأجهزة</a>
            <a href="#">متجر الشحن</a>
            <a href="#">الكافيه</a>
            <a href="#" class="cta-nav">تواصل معنا</a>
        </nav>
    </header>

    <div class="container">
        <!-- القسم الرئيسي -->
        <div class="hero-card">
            <div class="badge">🔥 أقوى تجربة جيمنج في المرج</div>
            <h2>مرحباً بك في <br><span style="color: #00f3ff;">TREND GAMING</span></h2>
            <p>أعلى مواصفات للكمبيوتر والجيمنج الاحترافي بشاشات تصل لـ 240Hz، إنترنت ألياف ضوئية فائق السرعة وبينغ منخفض جداً.</p>

            <!-- أسعار الساعات -->
            <div class="features-grid">
                <div class="feature-box">
                    <h4>10 ج.م</h4>
                    <span>الساعة العادية</span>
                </div>
                <div class="feature-box">
                    <h4>12 ج.م</h4>
                    <span>فئة Pro</span>
                </div>
                <div class="feature-box">
                    <h4>15 ج.م</h4>
                    <span>فئة Ultra 240Hz</span>
                </div>
            </div>

            <div class="btn-group">
                <a href="#" class="btn btn-primary">استعرض الأسعار</a>
                <a href="#" class="btn btn-secondary">شحن الألعاب</a>
            </div>
        </div>

        <!-- القسم الجانبي -->
        <div class="side-card">
            <h3>🎮 بطولات وشحن ألعاب</h3>
            <p>تابع مسابقات تريند الجيمينج وشحن ألعابك بأرخص سعر في مصر وبأسرع وقت عبر فودافون كاش.</p>
            
            <ul class="price-list">
                <li><span>ساعة العادي:</span> <span>10 جنيه</span></li>
                <li><span>ساعة Pro:</span> <span>12 جنيه</span></li>
                <li><span>ساعة Ultra:</span> <span>15 جنيه</span></li>
                <li><span>حالة السيرفرات:</span> <span style="color: #00ff66;">متوفر حالياً 🟢</span></li>
            </ul>

            <a href="#" class="btn btn-secondary" style="width: 100%; justify-content: center; margin-top: 15px;">تواصل معنا للاستفسار ←</a>
        </div>
    </div>

</body>
</html>
