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
            flex: 0 0 320px;
        }

        .header-branding .logo-area {
            display: flex;
            align-items: baseline;
            justify-content: center;
            gap: 10px;
            margin-bottom: 10px;
        }
        .header-branding .logo-mark {
            font-size: 24px;
            font-weight: bold;
            color: #fff;
        }
        .header-branding .logo-text {
            font-size: 20px;
            font-weight: bold;
        }
        .header-branding .site-title-header {
            font-weight: bold;
            text-align: center;
            margin: 10px 0;
            line-height: 1.1;
            color: #fff;
        }
        .site-title-header .title-large {
            font-size: 52px;
            letter-spacing: -2px;
        }
        .site-title-header .title-small {
            font-size: 36px;
            letter-spacing: -1px;
        }
        .header-branding .site-subtitle-header {
            font-size: 30px;
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
        .line-add-friend-btn {
            width: 220px;
            display: flex;
            justify-content: center;
        }

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
        .footer-nav { display: flex; justify-content: space-around; margin-bottom: 30px; flex-wrap: wrap; }
        .footer-nav-column { width: 30%; min-width: 200px; margin-bottom: 20px; }
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

        /* 規約ページ用スタイル */
        .kiyaku-container {
            max-width: 800px;
            margin: 20px auto;
            background-color: #fff;
            padding: 2em 3em;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
        }
        .kiyaku-container h1 { font-size: 2em; text-align: center; margin-bottom: 0.5em; border-bottom: 3px solid #4a5568; padding-bottom: 0.5em; }
        .kiyaku-container h2 { font-size: 1.6em; margin-top: 2.5em; border-bottom: 1px solid #ccc; padding-bottom: 0.4em; }
        .kiyaku-container h3 { font-size: 1.3em; margin-top: 2em; border-left: 6px solid #4a5568; padding-left: 0.8em; background-color: #f7fafc; padding-top: 0.3em; padding-bottom: 0.3em; }
        .kiyaku-container h4 { font-size: 1.1em; margin-top: 1.8em; color: #2d3748; }
        .kiyaku-container p { margin: 0.8em 0; }
        .kiyaku-container .article-title { font-weight: bold; }
        .kiyaku-container .revision-date { text-align: right; font-weight: bold; margin-bottom: 2em; color: #555; }
        .kiyaku-container .indent-1 { margin-left: 1.5em; text-indent: -1.5em; padding-left: 1.5em; }
        .kiyaku-container .indent-2 { margin-left: 3em; text-indent: -1.5em; padding-left: 1.5em; }
        .kiyaku-container table { width: 100%; border-collapse: collapse; margin: 1.5em 0; font-size: 0.95em; }
        .kiyaku-container th, .kiyaku-container td { border: 1px solid #ddd; padding: 10px; text-align: center; }
        .kiyaku-container th { background-color: #f2f2f2; font-weight: bold; }
        .back-button {
            display: inline-block;
            padding: 10px 20px;
            margin-bottom: 20px;
            background-color: #007bff;
            color: white;
            border-radius: 5px;
            font-weight: bold;
            cursor: pointer;
        }
        .back-button:hover {
            background-color: #0056b3;
        }

        @media (max-width: 768px) {
            .kiyaku-container { padding: 1.5em; }
            .kiyaku-container h1 { font-size: 1.8em; }
            .kiyaku-container h2 { font-size: 1.4em; }
            .kiyaku-container h3 { font-size: 1.2em; }
        }

    </style>
</head>
<body>

    <div id="main-page">
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
                     <div class="line-add-friend-btn">
                        <a href="https://lin.ee/kjiVD70"><img src="https://scdn.line-apps.com/n/line_add_friends/btn/ja.png" alt="友だち追加" height="36" border="0"></a>
                     </div>
                </div>

                <div class="header-nav-area">
                    <nav class="global-nav">
                        <div class="global-nav-grid">
                            <a href="https://note.com/good_mimosa3389/n/n0202f1da46b0" class="nav-item" target="_blank" rel="noopener noreferrer"><div class="nav-item-icon"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M16 11c1.66 0 2.99-1.34 2.99-3S17.66 5 16 5c-1.66 0-3 1.34-3 3s1.34 3 3 3zm-8 0c1.66 0 2.99-1.34 2.99-3S9.66 5 8 5C6.34 5 5 6.34 5 8s1.34 3 3 3zm0 2c-2.33 0-7 1.17-7 3.5V19h14v-2.5c0-2.33-4.67-3.5-7-3.5zm8 0c-.29 0-.62.02-.97.05 1.16.84 1.97 1.97 1.97 3.45V19h6v-2.5c0-2.33-4.67-3.5-7-3.5z"/></svg></div><span class="nav-item-title">全国税とは</span><span class="nav-item-subtitle">about</span></a>
                            <a href="https://note.com/good_mimosa3389/n/nd418ce78cb2e" class="nav-item" target="_blank" rel="noopener noreferrer"><div class="nav-item-icon"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M4.47 15.06L2 12.59l2.47-2.47.71.71L3.41 12.59l1.77 1.76-.71.71zM12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm0 18c-4.42 0-8-3.58-8-8s3.58-8 8-8 8 3.58 8 8-3.58 8-8 8zm-3.24-2.75l-.71-.71 1.76-1.76-1.76-1.76.71-.71 2.47 2.47-2.47 2.47zm6.48 0l-2.47-2.47 2.47-2.47.71.71-1.76 1.76 1.76 1.76-.71.71z"/></svg></div><span class="nav-item-title">ニュース</span><span class="nav-item-subtitle">What's new</span></a>
                            <a href="https://note.com/good_mimosa3389/n/n6e3c277be43d" class="nav-item" target="_blank" rel="noopener noreferrer"><div class="nav-item-icon"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M20 2H4c-1.1 0-2 .9-2 2v18l4-4h14c1.1 0 2-.9 2-2V4c0-1.1-.9-2-2-2zm-2 12H6v-2h12v2zm0-3H6V9h12v2zm0-3H6V6h12v2z"/></svg></div><span class="nav-item-title">オピニオン</span><span class="nav-item-subtitle">opinions</span></a>
                            <a href="https://note.com/good_mimosa3389" class="nav-item" target="_blank" rel="noopener noreferrer"><div class="nav-item-icon"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M14 2H6c-1.1 0-1.99.9-1.99 2L4 20c0 1.1.89 2 1.99 2H18c1.1 0 2-.9 2-2V8l-6-6zm2 16H8v-2h8v2zm0-4H8v-2h8v2zm-3-5V3.5L18.5 9H13z"/></svg></div><span class="nav-item-title">発行物</span><span class="nav-item-subtitle">publications</span></a>
                        </div>
                    </nav>
                </div>
            </div>
        </header>

        <!-- フッター -->
        <footer class="footer">
            <div class="container">
                <div class="footer-nav">
                    <div class="footer-nav-column"><h4>全国税について</h4><ul><li><a href="#" onclick="showPage('kiyaku-page'); return false;">規約</a></li><li><a href="https://zenkokuzeijimukyok.wixstudio.com/zenkokuzei" target="_blank" rel="noopener noreferrer">組合費</a></li><li><a href="https://note.com/good_mimosa3389/n/nc593aa9817e1" target="_blank" rel="noopener noreferrer">税研運動とは</a></li></ul></div>
                    <div class="footer-nav-column"><h4>運動方針</h4><ul><li><a href="https://note.com/good_mimosa3389/n/nbb28e63463ff" target="_blank" rel="noopener noreferrer">国民的課題</a></li><li><a href="https://note.com/good_mimosa3389/n/n6f35dab2c8fa" target="_blank" rel="noopener noreferrer">公務労働者の課題</a></li><li><a href="https://note.com/good_mimosa3389/n/ndbfaf05ef9cc" target="_blank" rel="noopener noreferrer">国税労働者の課題</a></li><li><a href="https://note.com/good_mimosa3389/n/n5f5eec5720fe" target="_blank" rel="noopener noreferrer">組織の拡大・強化</a></li><li><a href="https://note.com/good_mimosa3389/n/n62ba040d2cf3" target="_blank" rel="noopener noreferrer">税研運動方針</a></li></ul></div>
                     <div class="footer-nav-column">
                        <h4>お問い合わせ</h4>
                        <p>〒100-0013<br>東京都千代田区霞ヶ関３－１－１<br>財務ビル内　全国税労働組合</p>
                        <p>メールアドレス<br><a href="mailto:zenkokuzei@gmail.com" style="word-break: break-all;">zenkokuzei@gmail.com</a></p>
                    </div>
                </div>
                <div class="copyright"><p>&copy; 2025 全国税労働組合 All Rights Reserved.</p></div>
            </div>
        </footer>
    </div>

    <div id="kiyaku-page" style="display:none;">
        <div class="kiyaku-container">
            <a href="#" class="back-button" onclick="showPage('main-page'); return false;">メインページに戻る</a>
            <h1>全国税労働組合規約</h1>
            <p class="revision-date">2024年8月24日規約改正後</p>

            <h2>第1章 総則</h2>
            
            <h4>名称及び所在地</h4>
            <p><span class="article-title">第1条</span>　この組合は、全国税労働組合（略称：全国税）といい、本部を東京都千代田区霞ヶ関3-1-1におく。</p>
            <p class="indent-1">② この組合は、法人とする。</p>
            
            <h4>目的及び事業</h4>
            <p><span class="article-title">第2条</span> この組合は、綱領に従い、組合員の団結によって国税労働者の勤務条件の維持・改善を主たる目的とし、併せて職場であらゆる民主的諸権利の確保・拡大をたたかい、豊かな生活と明るい職場を確立し、世界の平和と労働者解放のために寄与することを目的とする。</p>
            <p><span class="article-title">第3条</span>　この組合は、前条の目的を達成するために、次の事業を行う。</p>
            <p class="indent-1">1. 組合員の労働条件、生活条件及び諸権利の確保・拡大に関すること。</p>
            <p class="indent-1">2. 税務行政の民主化に必要な調査、研究及び対策に関すること。</p>
            <p class="indent-1">3. 教育、文化に関すること。</p>
            <p class="indent-1">4. 機関誌発行に関すること。</p>
            <p class="indent-1">5. 同一目的を有する他団体との協力、提携に関すること。</p>
            <p class="indent-1">6. その他、組合の目的達成に必要なこと。</p>
            
            <h4>組合員</h4>
            <p><span class="article-title">第4条</span> この組合は、全国の国税労働者をもって組織する。ただし、国家公務員法第108条の2に規定する管理職員を除外する。</p>
            <p class="indent-1">② 組合員としての資格は、前項に規程するものが組合加入の意思を表明することによって取得する。</p>
            <p class="indent-1">③ 組合員としての資格は、次に掲げる場合に喪失する。</p>
            <p class="indent-2">1. 第1項ただし書きによる除外者となったとき。</p>
            <p class="indent-2">2. 第50条により組合を脱退したとき。</p>
            <p class="indent-2">3. 第61条により除名されたとき。</p>

            <h2>第2章　組合員の権利及び義務</h2>
            <h4>組合員の権利</h4>
            <p><span class="article-title">第5条</span>　組合員は、平等に次の権利を有する。</p>
            <p class="indent-1">1. 組合のすべての業務に参加し、自由に発言し、また議決すること。</p>
            <p class="indent-1">2. 組合業務による利益をうけること。</p>
            <p class="indent-1">3. 役員その他の委員を選考し、また選挙され就任すること。</p>
            
            <h4>組合員の義務</h4>
            <p><span class="article-title">第6条</span>　組合員は、次の義務を負う。</p>
            <p class="indent-1">1. 規約及び議決を遵守して、組合の発展に協力すること。</p>
            <p class="indent-1">2. 役員に選ばれた場合、正当な理由なくして就任を拒むことができず、かつ忠実にその業務に従事すること。</p>
            <p class="indent-1">3. 組合費を納入すること。</p>

            <h2>第3章　組織</h2>
            <h3>第1節　総則</h3>
            <h4>組合の組織</h4>
            <p><span class="article-title">第7条</span>　この組合は、次の組織をもつ。</p>
            <p class="indent-1">1. 本部</p>
            <p class="indent-1">2. 支部</p>
            <p class="indent-1">3. 分会</p>

            <h3>第2節　本部</h3>
            <h4>本部の構成</h4>
            <p><span class="article-title">第8条</span>　本部は、中央執行委員会と事務機関としての書記局で構成する。</p>
            <h4>諮問機関</h4>
            <p><span class="article-title">第8条の2</span>　中央執行委員会に諮問機関をおくことができる。諮問機関の名称、任務、構成については中央執行委員会で決定し、大会または中央委員会に報告、承認を受けるものとする。</p>
            <h4>特別委員会</h4>
            <p><span class="article-title">第8条の3</span>　組合活動を推進し、または業務遂行のため必要と認められるときは、中央執行委員会の決議により特別に委員会を設けることができる。その名称・性格・構成、処理すべき事項及び権限については、中央執行委員会が決定する。</p>
            <h4>特別中央執行委員及び顧問</h4>
            <p><span class="article-title">第8条の4</span>　本部に特別中央執行委員及び顧問をおくことができる。</p>
            <p class="indent-1">② 特別中央執行委員は、組合員のなかから、中央執行委員会の推薦に基づいて大会で決定する。顧問は、組合員であった者、または学識経験者のなかから、中央執行委員会の推薦に基づいて大会で決定する。</p>
            <p class="indent-1">③ 特別中央執行委員は、本部の各機関の会議に出席することができる。ただし、表決権をもたない。</p>
            <p class="indent-1">④ 第43条（役員の任期）の規程は、特別中央執行委員及び顧問について準用する。</p>
            <h4>書記局の構成</h4>
            <p><span class="article-title">第9条</span>　書記局は、中央執行委員会が指名した書記局員で構成し、次の各専門部をおく。</p>
            <p class="indent-1">1. 総務財政部</p>
            <p class="indent-1">2. 調査部</p>
            <p class="indent-1">3. 組織部</p>
            <p class="indent-1">4. 教育宣伝部</p>
            <p class="indent-1">5. 婦人部</p>
            <p class="indent-1">6. 青年対策部</p>
            <h4>書記局の統括</h4>
            <p><span class="article-title">第10条</span>　書記局は、書記長が統括する。</p>
            <h4>部長及び部員</h4>
            <p><span class="article-title">第11条</span>　書記局各専門部に、部長及び部員をおく。部長及び部員は、中央執行委員会で決定する。</p>
            <h4>書記局規程</h4>
            <p><span class="article-title">第12条</span>　書記局各専門部の事務分掌その他については、中央執行委員会で定める。</p>
            <h4>書記</h4>
            <p><span class="article-title">第13条</span>　書記局の業務遂行のため、書記をおくことができる。書記の任用は、中央執行委員会の承認を得て、中央執行委員長が行う。</p>
            
            <h3>第3節　削除</h3>
            <p><span class="article-title">第14条</span>　削除</p>

            <h3>第4節　支部</h3>
            <h4>支部</h4>
            <p><span class="article-title">第15条</span>　支部は、この組合の組織単位であって、その設置は、本規約別表に定めるところによる。</p>
            <p class="indent-1">② 支部は、役員及び代議員で構成する支部大会と、大会で選挙した役員によって構成される支部執行委員会で運営する。支部は支部規約、支部役員及び組合員名簿を本部に提出しなければならない。支部規約は、支部大会で別にこれを定める。</p>

            <h3>第5節　分会</h3>
            <h4>分会</h4>
            <p><span class="article-title">第16条</span>　分会は、各税務署（国税不服審判所を含む）、国税局（国税不服審判所、税務大学校地方研修所、国税庁派遣監督官室、同監察官室を含む。ただし、東京・関東信越・大阪国税局を除く）ごとに構成し、当該職場に所属する組合員で組織する。</p>
            <h4>運営</h4>
            <p><span class="article-title">第17条</span>　分会は、役員及び全組合員で構成する分会大会と、分会員が直接選挙した役員によって構成される分会執行委員会によって運営する。分会規約は、分会大会で別に定める。</p>

            <h3>第6節　青年部</h3>
            <h4>青年部</h4>
            <p><span class="article-title">第17条の2</span>　本組合に青年部をおく。青年部は、青年の要求実現のための独自の活動と、本組合の運動を積極的に推進することを目的とする。</p>
            <p class="indent-1">② 青年部の規約は別に定める。</p>
            <p class="indent-1">③ 支部、分会に青年部をおくことができる。</p>

            <h2>第四章　機関</h2>
            <h3>第1節　総則</h3>
            <h4>機関</h4>
            <p><span class="article-title">第18条</span>　この組合に次の機関をおく。</p>
            <p class="indent-1">1. 大会</p>
            <p class="indent-1">2. 中央委員会</p>
            <p class="indent-1">3. 中央執行委員会</p>
            <h4>会議の成立と議決</h4>
            <p><span class="article-title">第19条</span>　前条の機関の会議は、構成員の3分の2以上の出席をえて成立する。</p>
            <p class="indent-1">② 議決は、表決権をもつ出席構成員の過半数で決し、可否同数の場合は議長がこれを決する。</p>
            <h4>表決権</h4>
            <p><span class="article-title">第20条</span>　表決権は1人1票とする。ただし、大会及び中央委員会においては、役員は表決権をもたない。</p>
            <h4>傍聴</h4>
            <p><span class="article-title">第21条</span>　組合員は、自由に各機関の傍聴ができる。ただし、傍聴の目的に利敵行為のおそれのある場合は、各機関の決議により傍聴を禁止することができる。</p>
            
            <h3>第2節　大会</h3>
            <h4>大会</h4>
            <p><span class="article-title">第22条</span>　大会は、この組合の最高議決機関であり、次の者で構成する。</p>
            <p class="indent-1">1. 代議員</p>
            <p class="indent-1">2. 中央執行委員会を構成する役員</p>
            <p class="indent-1">3. 会計監査委員</p>
            <p class="indent-1">4. 統制委員会議長</p>
            <p class="indent-1">② 大会には、特別代議員を参加させる。特別代議員は表決権をもたない。</p>
            <h4>召集</h4>
            <p><span class="article-title">第23条</span>　定期大会は、毎年8月または9月に、中央執行委員長が招集する。</p>
            <p class="indent-1">② 中央執行委員長は、大会の日とき、場所及び議題を、特別事情のない限り2週間前に組合員に告示しなければならない。</p>
            <p class="indent-1">③ 前項の告示は、機関紙で行う。</p>
            <h4>臨時大会</h4>
            <p><span class="article-title">第24条</span>　中央執行委員長は、次の場合には臨時大会を招集しなければならない。</p>
            <p class="indent-1">1. 中央執行委員会で招集を決議したとき。</p>
            <p class="indent-1">2. 中央委員会で招集を決議したとき。</p>
            <p class="indent-1">3. 代議員の3分の1以上の要求があったとき。</p>
            <p class="indent-1">② 前項による大会を開かねばならなくなったときは、中央執行委員長は、その理由及び目的を明示し、30日以内に開催するよう招集しなければならない。</p>
            <h4>付議事項</h4>
            <p><span class="article-title">第25条</span>　次の事項は、大会の決定によらなければならない。</p>
            <p class="indent-1">1. 運動方針その他重要な議案</p>
            <p class="indent-1">2. 予算及び決算</p>
            <p class="indent-1">3. 役員の選出、信任または不信任</p>
            <p class="indent-1">4. 選挙管理委員の選出</p>
            <p class="indent-1">5. 綱領・規約の制定、変更もしくは廃止</p>
            <p class="indent-1">6. 他団体への加盟もしくは脱退</p>
            <p class="indent-1">7. 組合財産の処分</p>
            <p class="indent-1">8. 懲罰</p>
            <p class="indent-1">9. 改組、合併、解散</p>
            <p class="indent-1">ただし、第3号及び第5号、第6号、第9号については、代議員の平等にして無記名・直接・秘密の投票により決定しなければならない。</p>
            <p class="indent-1">② 前項第3号は、採決権をもつ出席構成員の過半数、第6号は、採決権をもつ構成員の過半数、第5・8号は、同3分の2以上、第9号は、同4分の3以上により決定しなければならない。</p>
            <h4>代議員の選出</h4>
            <p><span class="article-title">第26条</span>　代議員は、7月1日現在の組合員数に基づき、各支部ごとに組合員20名及びその端数につき1名の割合で支部組合員の平等にして直接・無記名・秘密の投票により、過半数をもって選出する。組合員数は、同月の組合費を大会前日までに納入した人員とする。</p>
            <p class="indent-1">② 代議員の任期は、定期大会から次期定期大会までの期間とする。</p>
            <p class="indent-1">③ 代議員の名簿は、支部ごとに支部長から大会前日までに中央執行委員長に提出する。</p>
            <p class="indent-1">④ 選出の細部については、別に定める選挙規則によらなければならない。</p>
            <h4>議長</h4>
            <p><span class="article-title">第27条</span>　大会の決議により議長を罷免することができる。</p>
            <p class="indent-1">② 議長は、大会を統制し、大会の運営について一切の責任を負う。</p>
            <h4>議事運営規程</h4>
            <p><span class="article-title">第28条</span>　議事運営規程については、大会または中央委員会において別に定める。</p>

            <h3>第3節　中央委員会</h3>
            <h4>中央委員会</h4>
            <p><span class="article-title">第29条</span>　中央委員会は、大会に次ぐ議決機関であり、次の者で構成する。</p>
            <p class="indent-1">1. 中央委員</p>
            <p class="indent-1">2. 中央執行委員会を構成する役員</p>
            <p class="indent-1">② 中央委員会には特別中央委員を参加させる。特別中央委員は、表決権をもたない。</p>
            <h4>招集</h4>
            <p><span class="article-title">第30条</span>　中央委員会は、次の場合中央執行委員長が招集する。</p>
            <p class="indent-1">1. 中央執行委員会で招集を決議したとき。</p>
            <p class="indent-1">2. 中央委員の3分の1以上の要求があったとき。</p>
            <h4>中央委員</h4>
            <p><span class="article-title">第31条</span>　中央委員は、大会において組合費を納入した人員に基づき、各支部ごとに組合員1,000名及びその端数につき1名の割合で、支部組合員の平等にして直接・無記名・秘密の投票により選出された中央委員候補を確認する。</p>
            <p class="indent-1">② 中央委員の定数は大会において決定する。</p>
            <p class="indent-1">③ 中央委員の任期は、定期大会から次期定期大会までの期間とする。</p>
            <p class="indent-1">④ 中央委員に欠員を生じた場合は、次点者を繰り上げ、その任期は前任者の残任期間とする。</p>
            <p class="indent-1">⑤ 選出の細部については、別に定める選挙規則によらなければならない。</p>
            <h4>付議事項</h4>
            <p><span class="article-title">第32条</span>　中央委員会は、次の事項を決する。</p>
            <p class="indent-1">1. 大会から委任された事項</p>
            <p class="indent-1">2. 規約及び規程の解釈に関する事項</p>
            <p class="indent-1">3. 規程の制定または改廃</p>
            <p class="indent-1">4. 予算の補正及び予算不成立の場合の暫定予算</p>
            <p class="indent-1">5. その他緊急事項</p>
            <h4>規程の準用</h4>
            <p><span class="article-title">第33条</span>　中央委員会の運営については、前各条によるもののほか、大会に関する規程を準用する。</p>

            <h3>第4節　中央執行委員会</h3>
            <h4>中央執行委員会</h4>
            <p><span class="article-title">第34条</span>　組合業務の執行権は中央執行委員会に属する。</p>
            <p class="indent-1">② 中央執行委員会は、執行権の行使に関し、大会並びに中央委員会に対して責任を負う。</p>
            <h4>構成</h4>
            <p><span class="article-title">第35条</span>　中央執行委員会は、役員（会計監査委員、統制委員会議長、統制委員を除く）で構成し、中央執行委員長は議長となる。</p>
            <h4>召集</h4>
            <p><span class="article-title">第36条</span>　中央執行委員会は、次の場合に中央執行委員長が招集する。</p>
            <p class="indent-1">1. 中央執行委員長が必要と認めたとき。</p>
            <p class="indent-1">2. 構成員の3分の1以上の要求があったとき。</p>
            <h4>権限と責任</h4>
            <p><span class="article-title">第37条</span>　中央執行委員会は、次の権限と責任を有する。</p>
            <p class="indent-1">1. 綱領、規約、規程及び機関の決議に従って組合業務を執行すること。</p>
            <p class="indent-1">2. 緊急事項を処理すること。</p>
            <p class="indent-1">3. 大会及び中央委員会の招集を決定すること。</p>
            <p class="indent-1">4. 大会及び中央委員会に議案を提出すること。</p>
            <p class="indent-1">5. 組合業務の執行を大会に報告し、その承認を求めること。</p>
            <p class="indent-1">6. 組合の経理につき、一切の責任を負うこと。</p>
            <h4>辞職</h4>
            <p><span class="article-title">第38条</span>　役員は、大会において不信任の決議をされ、または新任の決議案を否決されたときは、ただちに辞職しなければならない。</p>
            <p><span class="article-title">第39条</span>　削除</p>
            
            <h2>第5章　役員</h2>
            <h4>役員</h4>
            <p><span class="article-title">第40条</span>　組合に次の役員をおく。</p>
            <p class="indent-1">1. 中央執行委員長　1名</p>
            <p class="indent-1">2. 副中央執行委員長　5名</p>
            <p class="indent-1">3. 書記長　1名</p>
            <p class="indent-1">4. 書記次長　1名</p>
            <p class="indent-1">5. 中央執行委員　若干名</p>
            <p class="indent-1">6. 会計監査委員　若干名</p>
            <p class="indent-1">7. 統制委員会議長　1名</p>
            <p class="indent-1">8. 統制委員　若干名</p>
            <h4>任期</h4>
            <p><span class="article-title">第41条</span>　役員は、次の任期を有する。</p>
            <p class="indent-1">1. 中央執行委員長は、組合を代表し、組合業務を統括する。</p>
            <p class="indent-1">2. 副中央執行委員長は、中央執行委員長を補佐し、中央執行委員長に事故あるときはその職務を代行する。</p>
            <p class="indent-1">3. 書記長は、書記局を統括し業務を処理する。</p>
            <p class="indent-1">4. 書記次長は、書記長を補佐し、書記長に事故あるときはその職務を代行する。</p>
            <p class="indent-1">5. 中央執行委員は、組合の業務を分担処理する。</p>
            <p class="indent-1">6. 会計監査委員は、組合の財産・会計を監査し、監査結果に意見を付し中央委員会、大会に報告する。</p>
            <p class="indent-1">7. 統制委員会議長は、統制委員会を代表し、統制委員会業務を統括する。</p>
            <p class="indent-1">8. 統制委員は、統制委員会の業務を分担処理する。</p>
            <h4>役員の選出</h4>
            <p><span class="article-title">第42条</span>　役員は、第25条第1項ただし書きに基づき選出する。ただし、役員に欠員を生じた場合は、大会で選出した役員の次点者を繰り上げることができる。</p>
            <p class="indent-1">② 大会において不信任が決議された場合は、ただちに新役員を選出しなければならない。</p>
            <p class="indent-1">③ 選出方法は、別に定める選挙規則による。</p>
            <h4>任期</h4>
            <p><span class="article-title">第43条</span>　役員の任期は、定期大会より次期定期大会までの期間とする。ただし、任期満了後であっても後任者が就任するまでは、その職務を遂行しなければならない。</p>
            <p class="indent-1">② 前項にかかわらず、前条第1項及び第2項の場合の任期は、前任者の残任期間とする。</p>

            <h2>第6章　選挙</h2>
            <h4>選挙</h4>
            <p><span class="article-title">第44条</span>　選挙権は、代議員のみ行使する。</p>
            <p class="indent-1">② 代議員は、発表された候補者以外の組合員に投票することを妨げない。</p>
            <p class="indent-1">③ 役員選挙の投票は、次の順序により次の方法によって行う。</p>
            <p class="indent-2">1. 中央執行委員長　単記</p>
            <p class="indent-2">2. 副中央執行委員長　5名連記</p>
            <p class="indent-2">3. 書記長　単記</p>
            <p class="indent-2">4. 書記次長　単記</p>
            <p class="indent-2">5. 中央執行委員　若干名連記</p>
            <p class="indent-2">6. 会計監査委員　若干名連記</p>
            <p class="indent-2">7. 統制委員会議長　単記</p>
            <p class="indent-2">8. 統制委員　若干名連記</p>
            <p class="indent-1">④ 候補者が定数の範囲内の場合の選挙方法は、一括信任投票によることを妨げない。</p>
            <h4>当選の決定</h4>
            <p><span class="article-title">第45条</span>　役員の当選は、有効投票の多数を得たものから順次定数の範囲内で決定する。当選を決めるにあたって得票が同数のものについては決選投票を行う。ただし、定数の範囲内における得票の場合については、この限りでない。</p>
            <p class="indent-1">② 信任投票による場合は、投票者の過半数の信任票を得た者を当選者とする。</p>
            <h4>選挙管理委員会</h4>
            <p><span class="article-title">第46条</span>　役員の選挙の実施は、選挙管理委員会が行う。</p>
            <h4>構成</h4>
            <p><span class="article-title">第47条</span>　選挙管理委員会は、大会で選出された若干名の委員で構成し、委員の互選により委員長を決定する。</p>
            <h4>業務</h4>
            <p><span class="article-title">第48条</span>　選挙管理委員会は、次の業務を行う。</p>
            <p class="indent-1">1. 立候補者及び推薦候補者の氏名の発表</p>
            <p class="indent-1">2. 投票と開票の管理</p>
            <p class="indent-1">3. 投票の有効、無効の判定</p>
            <p class="indent-1">4. 当選者の氏名報告</p>
            <p class="indent-1">5. 規約第25条の重要事項についての投票及び開票の管理</p>
            <p class="indent-1">6. その他選挙及び投票に関する必要な事項</p>

            <h2>第7章　加入及び脱退</h2>
            <h4>加入</h4>
            <p><span class="article-title">第49条</span>　この組合に加入しようとするものは、中央執行委員長に対し文書をもって、その旨意思の表明をしなければならない。</p>
            <h4>脱退</h4>
            <p><span class="article-title">第50条</span>　この組合を脱退しようとするものは、脱退届に理由を明記し、中央執行委員長に提出しなければならない。</p>

            <h2>第8章　会計</h2>
            <h3>第1節　総則</h3>
            <h4>原則</h4>
            <p><span class="article-title">第51条</span>　この組合の収入及び支出は、規約・規程及び予算に基づいて行う。</p>
            <p class="indent-1">② この組合の経費は、組合費及びその他の収入をもって充てる。</p>
            <h4>組合費</h4>
            <p><span class="article-title">第52条</span>　組合員は、次により組合費を納入しなければならない。</p>
            <p class="indent-1">1. 行政職（二）俸給表の適用を受けている組合員は1人月額1,620円。ただし、同俸給表の適用を受けている場合の定年延長組合費は1,130円。</p>
            <p class="indent-1">2. 非常勤職員の組合員は、一人月額450円。</p>
            <p class="indent-1">3. 前2号以外の組合員は、一人月額表１に掲げる額。</p>
            <table>
                <caption>表1</caption>
                <thead>
                    <tr>
                        <th>級</th>
                        <th>組合費</th>
                        <th>定年延長組合員</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>6</td>
                        <td>5,760円</td>
                        <td>4,030円</td>
                    </tr>
                    <tr>
                        <td>5</td>
                        <td>5,310円</td>
                        <td>3,710円</td>
                    </tr>
                    <tr>
                        <td>4</td>
                        <td>4,860円</td>
                        <td>3,400円</td>
                    </tr>
                    <tr>
                        <td>3</td>
                        <td>3,870円</td>
                        <td>2,700円</td>
                    </tr>
                    <tr>
                        <td>2</td>
                        <td>2,160円</td>
                        <td>1,500円</td>
                    </tr>
                    <tr>
                        <td>1</td>
                        <td>1,260円</td>
                        <td>880円</td>
                    </tr>
                </tbody>
            </table>
            <p class="indent-1">4. 前号の組合員は、12月及び6月は前号にかかわらず、前号に掲げる金額と表２に掲げる金額（以下「特別組合費」という）を加算した額。</p>
            <table>
                <caption>表2</caption>
                <thead>
                    <tr>
                        <th>級</th>
                        <th>組合費</th>
                        <th>定年延長組合員</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>6</td>
                        <td>18,000円</td>
                        <td>12,600円</td>
                    </tr>
                    <tr>
                        <td>5</td>
                        <td>10,800円</td>
                        <td>7,560円</td>
                    </tr>
                    <tr>
                        <td>4</td>
                        <td>9,000円</td>
                        <td>6,300円</td>
                    </tr>
                    <tr>
                        <td>3</td>
                        <td>5,850円</td>
                        <td>4,090円</td>
                    </tr>
                    <tr>
                        <td>2</td>
                        <td>2,700円</td>
                        <td>1,890円</td>
                    </tr>
                    <tr>
                        <td>1</td>
                        <td>900円</td>
                        <td>630円</td>
                    </tr>
                </tbody>
            </table>
            <p class="indent-1">5. 第1項ただし書き、第3号表1及び第4号表2に掲げる「定年延長組合費」とは、一般職の職員の給与に関する法律（昭和25年法律第95号）附則第８項の規定の適用を受ける組合員の納入すべき組合費とし、「組合員」とは同項の適用を受けない組合員が納入すべき組合費とする。</p>
            <p class="indent-1">6. 再任用職員である組合員の組合費は適用される俸給表に応じ第1号又は第3号の規程を適用し、第4号に掲げる特別組合費は適用しない。ただし、その組合員が短時間勤務職員である場合は、税務職俸給表適用組合員は1級の組合費とし、行政職（二）俸給表適用組合員は一人月額630円とする。</p>
            <p class="indent-1">② 各分会は毎月1日現在の組合員数をもって、その月の25日までに納入しなければならない。</p>
            <p class="indent-1">③ 既納の組合費は返却しない。</p>
            <p class="indent-1">④ 中央執行委員会は、相当の理由があると認めるときは、組合費を減免することができる。</p>
            <p class="indent-1">⑤ 組合員の機関紙「全国税」購読料金は組合費に含む。</p>
            <h4>臨時徴収</h4>
            <p><span class="article-title">第53条</span>　経費が不足した場合、並びに不足を生ずると認められる場合は、大会または中央委員会の決定によって、組合費を臨時に徴収することができる。</p>
            <h4>会計年度</h4>
            <p><span class="article-title">第54条</span>　この組合の会計年度は、毎年7月1日より翌年6月30日までとする。</p>
            <h4>特別会計</h4>
            <p><span class="article-title">第55条</span>　この組合の会計は、一般会計と特別会計とする。</p>
            <p class="indent-1">② 特別会計は、組合が特定の資金を運用する必要がある場合に、大会の決議を経て設置する。</p>
            <h4>帳簿の閲覧</h4>
            <p><span class="article-title">第56条</span>　組合員は、所属支部長の資格証明により、中央執行委員長の承認を経て、次の場合を除きいつでも会計帳簿を閲覧することができる。</p>
            <p class="indent-1">1. 執務時間外の場合</p>
            <p class="indent-1">2. 組合業務に重大な支障ある場合</p>

            <h3>第2節　予算及び決算</h3>
            <h4>予算</h4>
            <p><span class="article-title">第57条</span>　中央執行委員会は、毎会計年度ごとに予算案を作成し、大会の決定を経なければならない。</p>
            <p class="indent-1">② 中央執行委員会は、予算を補正する必要が生じたときは補正予算案を作成し、大会または中央執行委員会の決定を経なければならない。</p>
            <p class="indent-1">③ 毎年7月1日より予算確定の定期大会までの暫定予算は、前年度予算月割額の範囲内で中央執行委員会が決定し執行する。</p>
            <h4>会計の一元化</h4>
            <p><span class="article-title">第58条</span>　収入と支出は、すべて予算に編入しなければならない。</p>
            <h4>決算</h4>
            <p><span class="article-title">第59条</span>　中央執行委員会は、会計年度終了後すみやかに決算を行い、会計監査委員の監査報告書を添えて大会に報告し、承認をえなければならない。</p>
            <p class="indent-1">② 決算書類は、次のとおりとする。</p>
            <p class="indent-2">1. 貸借対照表及び財産目録</p>
            <p class="indent-2">2. 予算対比収支計算書</p>
            <p class="indent-2">3. 前2号の付表</p>
            <h4>会計規程</h4>
            <p><span class="article-title">第60条</span>　会計について必要な事項は、規程をもって別に定める。</p>

            <h2>第9章　統制</h2>
            <h4>懲罰</h4>
            <p><span class="article-title">第61条</span>　次の各号のいずれかに該当するものは、3ヶ月以内の権利停止、もしくは除名に付する。</p>
            <p class="indent-1">1. 綱領、規約または決議に違反したもの。</p>
            <p class="indent-1">2. 組合の名誉を毀損したもの。</p>
            <p class="indent-1">② 懲罰の決定は、別に定める統制委員会規程に基づく統制委員会の決定で発効する。</p>
            <p class="indent-1">③ 前項の決定は、大会出席代議員の3分の2以上の承認を得なければならない。</p>

            <h2>第10章　救援</h2>
            <h4>救援</h4>
            <p><span class="article-title">第62条</span>　組合員が、組合機関の決定に基づき業務を遂行中、または遂行したことによって損害または不利益を受けた場合は、本人またはその家族に対して救援を行う。</p>
            <p class="indent-1">② 組合員が組合機関の役員として専従した場合（共闘関係にある団体の役員として派遣された場合を含む）は、そのことによって受ける損失または不利益を補償する。</p>
            <p class="indent-1">③ 前2項の救援及び補償の基準は別に規程をもって定める。</p>
            <p class="indent-1">④ 第1項の救援に充てる資金を運用するため、弾圧犠牲者救援特別会計を設ける。この資金は、組合員から徴収する資金、一般会計からの繰入金、寄付金及びその他の収入をもつて充てる。</p>
            <p class="indent-1">⑤ 日本国家公務員労働組合連合会の統一救援拠出金並びに同救援基金については、前項の弾圧犠牲者救援特別会計から支出することを妨げない。</p>
            <p class="indent-1">⑥ 第2項の補償に充てる資金を運用するため、専従者補償特別会計を設ける。この資金として組合員1人1ヶ月400円を徴収する。</p>

            <h2>第11章　解散</h2>
            <h4>解散</h4>
            <p><span class="article-title">第63条</span>　この組合の改組、合併、解散については、大会において構成代議員の4分の３以上の同意を得なければならない。</p>

            <h2>第12章　附則</h2>
            <p><span class="article-title">第64条</span>　この規約は、第52条を除き1958年12月25日から施行する。</p>
            <p class="indent-1">② この規約の第52条は、1959年2月1日から施行する。</p>
            <p><span class="article-title">第65条</span>　規約第15条により定める支部の設置は次による。（省略）</p>
            <p><span class="article-title">第101条</span>　この規約改正は、2024年4月1日に遡り施行する。</p>
            
        </div>
    </div>

    <a href="#" id="to-top" class="to-top-btn">↑</a>

    <script>
        function showPage(pageId) {
            document.getElementById('main-page').style.display = 'none';
            document.getElementById('kiyaku-page').style.display = 'none';
            
            document.getElementById(pageId).style.display = 'block';
            window.scrollTo(0, 0);
        }

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
