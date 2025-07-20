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
            transition: font-size 0.3s;
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
            font-size: 12px;
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
        .header-branding .font-sizer {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 5px;
            margin-bottom: 15px;
        }
        .header-branding .font-sizer span {
            font-size: 14px;
        }
        .header-branding .font-sizer button {
            background: #fff;
            border: 1px solid #ccc;
            padding: 2px 8px;
            cursor: pointer;
            font-size: 14px;
        }
        .header-branding .font-sizer button.active {
            background: #003366;
            color: #fff;
            border-color: #003366;
        }
        .header-branding .search-form {
            display: flex;
        }
        .header-branding .search-form input {
            width: 100%;
            border: none;
            padding: 8px;
            border-radius: 3px 0 0 3px;
            font-size: 14px;
        }
        .header-branding .search-form button {
            background: #fff;
            border: none;
            padding: 0 10px;
            cursor: pointer;
            border-radius: 0 3px 3px 0;
        }
        .header-branding .search-form svg {
            width: 18px;
            height: 18px;
            fill: #333;
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
        
        /* メインコンテンツエリア */
        .main-wrapper { padding: 20px 0; }
        .main-content-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; }
        section { background-color: #fff; padding: 20px; border-radius: 8px; box-shadow: 0 2px 5px rgba(0,0,0,0.05); margin-bottom: 20px; }
        h2.section-title { font-size: 24px; color: #0056b3; border-bottom: 2px solid #007bff; padding-bottom: 10px; margin-bottom: 20px; }

        /* コンテンツ詳細 */
        .news-item { display: flex; align-items: center; gap: 15px; margin-bottom: 15px; }
        .news-item:last-child { margin-bottom: 0; }
        .news-item img { width: 120px; height: 80px; object-fit: cover; border-radius: 5px; flex-shrink: 0; }
        .news-text time { font-size: 14px; color: #666; }
        .news-text h3 { font-size: 16px; margin: 5px 0 0 0; }
        .card { display: flex; align-items: center; background-color: #eaf4ff; border: 1px solid #bde0ff; border-radius: 8px; padding: 20px; }
        .card-icon { margin-right: 15px; }
        .card-content h3 { margin: 0 0 10px 0; color: #0056b3; }
        .card-content p { margin: 0; font-size: 14px; }
        .text-center { text-align: center; margin-top: 20px; }
        .btn { display: inline-block; background-color: #007bff; color: #fff; padding: 10px 30px; border-radius: 20px; font-weight: bold; }
        .btn:hover { background-color: #0056b3; color: #fff; }
        .feed-placeholder { border: 1px dashed #ccc; height: 200px; display: flex; justify-content: center; align-items: center; color: #999; border-radius: 5px; background-color: #f9f9f9; }

        /* フッター */
        .footer { background-color: #003366; color: #fff; padding: 40px 0 20px; margin-top: 20px; }
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
        @media (max-width: 1100px) {
            .header-container {
                flex-wrap: wrap;
                justify-content: center;
            }
            .header-branding {
                flex-basis: 100%;
                max-width: 400px;
                margin: 0 auto 20px auto;
            }
            .header-social-buttons {
                order: 3;
                margin-top: 10px;
                flex-direction: row;
                flex-wrap: wrap;
                justify-content: center;
            }
            .header-nav-area {
                margin-bottom: 20px;
            }
        }
        @media (max-width: 768px) {
            .footer-nav-column { width: 48%; }
        }
        @media (max-width: 520px) {
            .header-social-buttons {
                flex-direction: column;
                align-items: center;
            }
            .footer-nav-column { width: 100%; }
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
                <div class="font-sizer">
                    <span>文字サイズ</span>
                    <button id="font-small">小</button>
                    <button id="font-medium" class="active">中</button>
                    <button id="font-large">大</button>
                </div>
                <form class="search-form">
                    <input type="search" placeholder="サイト内検索">
                    <button type="submit">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M15.5 14h-.79l-.28-.27A6.471 6.471 0 0 0 16 9.5 6.5 6.5 0 1 0 9.5 16c1.61 0 3.09-.59 4.23-1.57l.27.28v.79l5 4.99L20.49 19l-4.99-5zm-6 0C7.01 14 5 11.99 5 9.5S7.01 5 9.5 5 14 7.01 14 9.5 11.99 14 9.5 14z"/></svg>
                    </button>
                </form>
            </div>

            <div class="header-social-buttons">
                <a href="https://www.youtube.com/@%E5%85%A8%E5%9B%BD%E7%A8%8E%E5%8A%B4%E5%83%8D%E7%B5%84%E5%90%88%E4%BA%8B%E5%8B%99%E5%B1%80" class="social-btn youtube-btn" target="_blank" rel="noopener noreferrer">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M21.582,6.186c-0.23-0.86-0.908-1.538-1.768-1.768C18.25,4,12,4,12,4S5.75,4,4.186,4.418 c-0.86,0.23-1.538,0.908-1.768,1.768C2,7.75,2,12,2,12s0,4.25,0.418,5.814c0.23,0.86,0.908,1.538,1.768,1.768 C5.75,20,12,20,12,20s6.25,0,7.814-0.418c0.861-0.23,1.538-0.908,1.768-1.768C22,16.25,22,12,22,12S22,7.75,21.582,6.186z M10,15.464V8.536L16,12L10,15.464z"/></svg>
                    <div class="btn-text">
                        <strong>YouTube</strong>
                        <span>全国税チャンネル #動画</span>
                    </div>
                </a>
                 <a href="#" class="social-btn x-btn">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/></svg>
                    <span>X (Twitter)</span>
                </a>
                <a href="#" class="social-btn facebook-btn">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M22,12c0-5.523-4.477-10-10-10S2,6.477,2,12c0,4.99,3.657,9.128,8.438,9.878V14.89H8.078v-2.89h2.359v-2.18c0-2.325,1.383-3.621,3.52-3.621c1.003,0,1.865,0.074,2.115,0.108v2.58h-1.52c-1.13,0-1.35,0.536-1.35,1.322v1.73h2.867l-0.375,2.89h-2.492v7.008C18.343,21.128,22,16.99,22,12z"/></svg>
                    <span>Facebook</span>
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

    <!-- メインコンテンツ -->
    <div class="main-wrapper">
        <div class="container">
            <div class="main-content-grid">
                <section id="news">
                    <h2 class="section-title">ニュース＆トピックス</h2>
                    <div class="news-list">
                        <article class="news-item"><img src="https://placehold.co/120x80/CCCCCC/FFFFFF?text=ニュース1" alt="ニュース画像1"><div class="news-text"><time datetime="2025-07-20">2025.07.20</time><h3><a href="#">2025国民春闘 News No.1を発行しました</a></h3></div></article>
                        <article class="news-item"><img src="https://placehold.co/120x80/CCCCCC/FFFFFF?text=ニュース2" alt="ニュース画像2"><div class="news-text"><time datetime="2025-07-19">2025.07.19</time><h3><a href="#">全国税第46回定期大会第1号議案のポイント</a></h3></div></article>
                    </div>
                </section>
                <section id="whats-new">
                    <h2 class="section-title">What's New 新着情報</h2>
                    <div class="card"><div class="card-icon"><img src="https://placehold.co/60x60/3498DB/FFFFFF?text=ICON" alt="アイコン"></div><div class="card-content"><h3>政策・提言</h3><p>全国税の政策や提言をまとめています。</p></div></div>
                    <div class="text-center"><a href="#" class="btn">一覧を見る</a></div>
                </section>
                <section id="social">
                    <h2 class="section-title">ソーシャルメディア</h2>
                    <div class="social-container"><h3>Twitter</h3><div class="feed-placeholder"><p>Twitterのタイムライン</p></div></div>
                </section>
            </div>
        </div>
    </div>

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

            // 文字サイズ変更
            const fontSizer = document.querySelector('.font-sizer');
            if (fontSizer) {
                const body = document.body;
                const buttons = fontSizer.querySelectorAll('button');
                buttons.forEach(button => {
                    button.addEventListener('click', (e) => {
                        e.preventDefault();
                        buttons.forEach(btn => btn.classList.remove('active'));
                        button.classList.add('active');
                        if (button.id === 'font-small') {
                            body.style.fontSize = '14px';
                        } else if (button.id === 'font-medium') {
                            body.style.fontSize = '16px';
                        } else if (button.id === 'font-large') {
                            body.style.fontSize = '18px';
                        }
                    });
                });
            }
        });
    </script>
</body>
</html>
