<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>全国税労働組合</title>
    <style>
        /* 基本設定 */
        body {
            font-family: 'Helvetica Neue', 'Arial', 'Hiragino Sans', 'Meiryo', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f8ff;
            color: #333;
            font-size: 16px;
            line-height: 1.6;
            display: flex;
            flex-direction: column;
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        a {
            color: #0056b3;
            text-decoration: none;
            transition: color 0.3s, opacity 0.3s, background-color 0.3s;
        }

        a:hover {
            color: #007bff;
            text-decoration: none;
        }

        img {
            max-width: 100%;
            height: auto;
            vertical-align: middle;
        }

        h1, h2, h3, h4 {
            margin-top: 0;
        }

        /* 新ヘッダー */
        .site-header {
            background-color: #00a0e9;
            color: #fff;
            padding: 20px 0;
        }

        .header-container {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 15px;
        }

        .header-branding {
            flex: 0 0 300px;
        }

        .header-branding .logo-area {
            display: flex;
            align-items: baseline;
            justify-content: center;
            gap: 10px;
            margin-bottom: 10px;
        }
        .header-branding .logo-mark {
            font-size: 22px;
            font-weight: bold;
            color: #fff;
        }
        .header-branding .logo-text {
            font-size: 18px;
            font-weight: bold;
        }
        .header-branding .site-title-header {
            font-weight: bold;
            text-align: center;
            margin: 0;
            line-height: 1.1;
            color: #fff;
        }
        .site-title-header .title-large {
            font-size: 48px;
            letter-spacing: -2px;
        }
        .site-title-header .title-small {
            font-size: 32px;
            letter-spacing: -1px;
        }
        .header-branding .site-subtitle-header {
            font-size: 28px;
            font-weight: bold;
            text-align: center;
            margin-bottom: 15px;
            border-bottom: 1px solid #fff;
            padding-bottom: 15px;
        }
        .header-branding .email-address {
            font-size: 16px;
            font-weight: bold;
            text-align: center;
            margin: 15px 0;
        }
        .header-branding .email-address a {
            color: #fff;
            display: flex;
            align-items: center;
            justify-content: center;
            word-break: break-all;
        }
        .header-branding .email-address a:hover {
            text-decoration: underline;
        }
        .header-branding .email-address svg {
            width: 24px;
            height: 24px;
            margin-right: 8px;
            fill: #fff;
            flex-shrink: 0;
        }

        /* 中央のSNSボタンエリア */
        .header-social-buttons {
            display: flex;
            flex-direction: column;
            gap: 10px;
            align-items: center;
            justify-content: center;
            flex-grow: 1;
        }
        .social-btn {
            display: flex;
            align-items: center;
            padding: 8px 12px;
            border-radius: 5px;
            background-color: #fff;
            color: #333;
            border: 1px solid #ddd;
            font-weight: bold;
            width: 220px;
        }
        .social-btn:hover {
            background-color: #f0f0f0;
            border-color: #ccc;
            color: #333;
        }
        .social-btn svg {
            margin-right: 8px;
            width: 24px;
            height: 24px;
        }
        .social-btn.youtube-btn svg { fill: #FF0000; }
        .social-btn.x-btn svg { fill: #000000; }
        .social-btn.facebook-btn svg { fill: #1877F2; }
        .social-btn.line-btn svg {
            width: 24px;
            height: 24px;
        }
        .social-btn .btn-text {
            display: flex;
            flex-direction: column;
            line-height: 1.2;
            text-align: left;
        }
        .social-btn .btn-text strong { font-size: 14px; }
        .social-btn .btn-text span { font-size: 11px; font-weight: normal; }

        /* 右側のナビゲーションエリア */
        .header-nav-area {
            flex: 0 0 250px;
        }
        .global-nav-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1px;
            background-color: #fff;
            border: 1px solid #fff;
            width: 100%;
        }
        .nav-item {
            background-color: #00a0e9;
            color: #fff;
            text-align: center;
            padding: 15px 5px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            min-height: 110px;
        }
        .nav-item:hover {
            background-color: #007bff;
            color: #fff;
        }
        .nav-item-icon svg { width: 32px; height: 32px; fill: #fff; margin-bottom: 8px; }
        .nav-item-title { font-size: 16px; font-weight: bold; line-height: 1.2; }
        .nav-item-subtitle { font-size: 12px; color: #f0c20c; font-weight: bold; margin-top: 4px; }
        
        /* フッター */
        .footer { 
            background-color: #003366; 
            color: #fff; 
            padding: 40px 0 20px; 
            margin-top: auto; /* Push footer to the bottom */
        }
        .footer a { color: #fff; }
        .footer a:hover { text-decoration: underline; }
        .footer-nav { display: flex; justify-content: space-between; margin-bottom: 30px; flex-wrap: wrap; }
        .footer-nav-column { width: 23%; min-width: 200px; margin-bottom: 20px; }
        .footer-nav-column h4 { font-size: 18px; border-bottom: 1px solid #fff; padding-bottom: 10px; margin-bottom: 15px; }
        .footer-nav-column ul { list-style: none; padding: 0; margin: 0; }
        .footer-nav-column li { margin-bottom: 10px; }
        .copyright { text-align: center; border-top: 1px solid #336699; padding-top: 20px; font-size: 14px; }

        /* トップへ戻るボタン */
        .to-top-btn { position: fixed; bottom: 20px; right: 20px; width: 50px; height: 50px; background-color: #007bff; color: #fff; border-radius: 50%; text-align: center; line-height: 50px; font-size: 24px; display: none; z-index: 1000; }
        .to-top-btn:hover { background-color: #0056b3; color: #fff; }

        /* Responsive Design */
        /* Tablet & Landscape Phone */
        @media (max-width: 1100px) {
            .header-container {
                flex-direction: column;
                gap: 25px;
            }
        }

        /* Mobile Phone */
        @media (max-width: 768px) {
            .footer-nav-column { 
                width: 48%; 
                min-width: 0;
            }
        }

        @media (max-width: 520px) {
            .header-social-buttons {
                flex-direction: column;
                align-items: center;
            }
            .footer-nav-column { 
                width: 100%; 
            }
        }
    </style>
</head>
<body>

    <!-- ヘッダー -->
    <header class="site-header">
        <div class="container header-container">
            <div class="header-branding">
                <div class="logo-area">
                    <span class="logo-mark">全国税</span>
                    <span class="logo-text">憲法をいかす</span>
                </div>
                <h1 class="site-title-header">
                    <span class="title-large">ZEN</span><span class="title-small">kokuzei</span>
                </h1>
                <p class="site-subtitle-header">全国税労働組合</p>
                <p class="email-address">
                    <a href="mailto:zenkokuzei@gmail.com">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor"><path d="M22 6c0-1.1-.9-2-2-2H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6zm-2 0l-8 5-8-5h16zm0 12H4V8l8 5 8-5v10z"/></svg>
                        zenkokuzei@gmail.com
                    </a>
                </p>
            </div>

            <div class="header-social-buttons">
                <a href="https://www.youtube.com/@%E5%85%A8%E5%9B%BD%E7%A8%8E%E5%8A%B4%E5%83%8D%E7%B5%84%E5%90%88%E4%BA%8B%E5%8B%99%E5%B1%80" class="social-btn youtube-btn" target="_blank" rel="noopener noreferrer">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M21.582,6.186c-0.23-0.86-0.908-1.538-1.768-1.768C18.25,4,12,4,12,4S5.75,4,4.186,4.418 c-0.86,0.23-1.538,0.908-1.768,1.768C2,7.75,2,12,2,12s0,4.25,0.418,5.814c0.23,0.86,0.908,1.538,1.768,1.768 C5.75,20,12,20,12,20s6.25,0,7.814-0.418c0.861-0.23,1.538-0.908,1.768-1.768C22,16.25,22,12,22,12S22,7.75,21.582,6.186z M10,15.464V8.536L16,12L10,15.464z"/></svg>
                    <div class="btn-text">
                        <strong>YouTube</strong>
                        <span>全国税チャンネル #動画</span>
                    </div>
                </a>
                 <a href="https://x.com/guo_quan89661" class="social-btn x-btn" target="_blank" rel="noopener noreferrer">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/></svg>
                    <span>X (Twitter)</span>
                </a>
                <a href="https://www.facebook.com/profile.php?id=61578354306982" class="social-btn facebook-btn" target="_blank" rel="noopener noreferrer">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M22,12c0-5.523-4.477-10-10-10S2,6.477,2,12c0,4.99,3.657,9.128,8.438,9.878V14.89H8.078v-2.89h2.359v-2.18c0-2.325,1.383-3.621,3.52-3.621c1.003,0,1.865,0.074,2.115,0.108v2.58h-1.52c-1.13,0-1.35,0.536-1.35,1.322v1.73h2.867l-0.375,2.89h-2.492v7.008C18.343,21.128,22,16.99,22,12z"/></svg>
                    <span>Facebook</span>
                </a>
                <a href="https://www.tiktok.com/@zenkokuzei" class="social-btn tiktok-btn" target="_blank" rel="noopener noreferrer">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor"><path d="M12.525.02c1.31-.02 2.61-.01 3.91-.02.08 1.53.63 3.09 1.75 4.17 1.12 1.11 2.7 1.62 4.24 1.79v4.03c-1.44-.05-2.89-.35-4.2-.97-.57-.26-1.1-.59-1.62-.93-.01 2.92.01 5.84-.02 8.75-.08 1.4-.54 2.79-1.35 3.94-1.31 1.92-3.58 3.17-5.91 3.21-2.43.05-4.86-.95-6.43-2.8-1.58-1.85-2.03-4.35-1.7-6.73.33-2.37 1.8-4.28 3.57-5.52 1.85-1.29 3.9-1.96 5.96-1.98.02 1.56.02 3.13.01 4.69-.68.01-1.36.09-2.03.36-1.03.41-1.92 1.11-2.49 2.06-.63 1.05-.8 2.33-.65 3.58.17 1.43 1.02 2.7 2.25 3.45.95.58 2.09.78 3.19.57.85-.16 1.68-.52 2.31-1.09.63-.58 1.1-1.33 1.32-2.14.24-.9.28-1.87.23-2.82.01-1.35.01-2.7.01-4.05Z"/></svg>
                    <span>TikTok</span>
                </a>
                <a href="https://www.instagram.com/zenkokuzei/" class="social-btn instagram-btn" target="_blank" rel="noopener noreferrer">
                     <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.85s-.011 3.585-.069 4.85c-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.85-.07-3.252-.148-4.771-1.691-4.919-4.919-.058-1.265-.069-1.645-.069-4.85s.011-3.585.069-4.85c.149-3.225 1.664-4.771 4.919-4.919 1.266-.058 1.644-.07 4.85-.07zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.162 6.162 6.162 6.162-2.759 6.162-6.162-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4s1.791-4 4-4 4 1.79 4 4-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/></svg>
                    <span>インスタグラム</span>
                </a>
                 <a href="#" class="social-btn line-btn">
                     <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                        <path fill="#06C755" d="M20.5,0H3.5A3.5,3.5,0,0,0,0,3.5V20.5A3.5,3.5,0,0,0,3.5,24h17A3.5,3.5,0,0,0,24,20.5V3.5A3.5,3.5,0,0,0,20.5,0Z"/>
                        <path fill="white" d="M12 5.5C8.13 5.5 5 8.36 5 11.91c0 2.29 1.44 4.3 3.61 5.43a1 1 0 0 0 .47.12c.11 0 .22-.03.32-.08 1.19-.6 2.62-1.22 2.62-1.22s.37.1.78.16c.4.06.81.09 1.2.09 3.87 0 7-2.86 7-6.41S15.87 5.5 12 5.5zm-3.9 7.2H7v-3h1.1v3zm2.6 0h-1.1v-3h1.1v3zm2.6 0h-1.1v-3h1.1v3zm3.7-1.4c0 .41-.34.75-.75.75h-2.2c-.41 0-.75-.34-.75-.75V10c0-.41.34-.75.75-.75h2.2c.41 0 .75.34.75.75v1.4z"/>
                    </svg>
                    <span>LINE</span>
                </a>
            </div>

            <div class="header-nav-area">
                <nav class="global-nav">
                    <div class="global-nav-grid">
                        <a href="#" class="nav-item"><div class="nav-item-icon"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M16 11c1.66 0 2.99-1.34 2.99-3S17.66 5 16 5c-1.66 0-3 1.34-3 3s1.34 3 3 3zm-8 0c1.66 0 2.99-1.34 2.99-3S9.66 5 8 5C6.34 5 5 6.34 5 8s1.34 3 3 3zm0 2c-2.33 0-7 1.17-7 3.5V19h14v-2.5c0-2.33-4.67-3.5-7-3.5zm8 0c-.29 0-.62.02-.97.05 1.16.84 1.97 1.97 1.97 3.45V19h6v-2.5c0-2.33-4.67-3.5-7-3.5z"/></svg></div><span class="nav-item-title">全国税とは</span><span class="nav-item-subtitle">about</span></a>
                        <a href="#" class="nav-item"><div class="nav-item-icon"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M4.47 15.06L2 12.59l2.47-2.47.71.71L3.41 12.59l1.77 1.76-.71.71zM12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm0 18c-4.42 0-8-3.58-8-8s3.58-8 8-8 8 3.58 8 8-3.58 8-8 8zm-3.24-2.75l-.71-.71 1.76-1.76-1.76-1.76.71-.71 2.47 2.47-2.47 2.47zm6.48 0l-2.47-2.47 2.47-2.47.71.71-1.76 1.76 1.76 1.76-.71.71z"/></svg></div><span class="nav-item-title">ニュース</span><span class="nav-item-subtitle">What's new</span></a>
                        <a href="#" class="nav-item"><div class="nav-item-icon"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M20 2H4c-1.1 0-2 .9-2 2v18l4-4h14c1.1 0 2-.9 2-2V4c0-1.1-.9-2-2-2zm-2 12H6v-2h12v2zm0-3H6V9h12v2zm0-3H6V6h12v2z"/></svg></div><span class="nav-item-title">オピニオン</span><span class="nav-item-subtitle">opinions</span></a>
                        <a href="#" class="nav-item"><div class="nav-item-icon"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M14 2H6c-1.1 0-1.99.9-1.99 2L4 20c0 1.1.89 2 1.99 2H18c1.1 0 2-.9 2-2V8l-6-6zm2 16H8v-2h8v2zm0-4H8v-2h8v2zm-3-5V3.5L18.5 9H13z"/></svg></div><span class="nav-item-title">発行物</span><span class="nav-item-subtitle">publications</span></a>
                    </div>
                </nav>
            </div>
        </div>
    </header>

    <!-- フッター -->
    <footer class="footer">
        <div class="container">
            <div class="footer-nav">
                <div class="footer-nav-column"><h4>全国税について</h4><ul><li><a href="#">綱領</a></li><li><a href="#">規約</a></li><li><a href="#">運動の基本方向</a></li></ul></div>
                <div class="footer-nav-column"><h4>政策・制度</h4><ul><li><a href="#">税制・税務行政</a></li><li><a href="#">勤務条件の改善</a></li><li><a href="#">定員・機構問題</a></li></ul></div>
                <div class="footer-nav-column"><h4>各種資料</h4><ul><li><a href="#">News</a></li><li><a href="#">声明・談話</a></li><li><a href="#">調査・研究</a></li></ul></div>
                 <div class="footer-nav-column">
                    <h4>お問い合わせ</h4>
                    <p>〒100-0013<br>東京都千代田区霞ヶ関３－１－１<br>財務ビル内　全国税労働組合</p>
                    <p>メールアドレス<br><a href="mailto:zenkokuzei@gmail.com" style="word-break: break-all;">zenkokuzei@gmail.com</a></p>
                </div>
            </div>
            <div class="copyright"><p>&copy; 2025 全国税労働組合 All Rights Reserved.</p></div>
        </div>
    </footer>

    <a href="#" id="to-top" class="to-top-btn">↑</a>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // トップへ戻るボタン
            const toTopBtn = document.getElementById('to-top');
            if (toTopBtn) {
                window.addEventListener('scroll', () => {
                    if (window.pageYOffset > 200) {
                        toTopBtn.style.display = 'block';
                    } else {
                        toTopBtn.style.display = 'none';
                    }
                });
                toTopBtn.addEventListener('click', (e) => {
                    e.preventDefault();
                    window.scrollTo({ top: 0, behavior: 'smooth' });
                });
            }

        });
    </script>
</body>
</html>
