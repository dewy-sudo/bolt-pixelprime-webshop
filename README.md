<!DOCTYPE html>
<html lang="hu">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PixelPrime Webshop - Rangok és Kiegészítők a Szerveredhez!</title>
    <meta name="description" content="Üdvözlünk a PixelPrime Minecraft szerver hivatalos webshopjában! Vásárolj exkluzív rangokat, kulcsokat és egyedi kiegészítőket, hogy maximalizáld a játékélményedet.">
    <link rel="icon" href="https://via.placeholder.com/32x32?text=PP" type="image/x-icon">
    
    <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    
    <style>
        /* Alapvető reset és globális stílusok */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Roboto', sans-serif; /* Modern, olvasható betűtípus */
            background-color: #1a1a2e; /* Mély sötétkék háttér */
            color: #e0e0e0; /* Világos szöveg */
            line-height: 1.6;
            display: flex;
            flex-direction: column;
            min-height: 100vh;
        }

        /* Konténer a tartalomnak */
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px 0;
        }

        /* Címsor és Navigáció */
        header {
            background: linear-gradient(to right, #0f3460, #16213e); /* Kék-lila átmenet */
            padding: 20px 0;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.4);
            border-bottom: 3px solid #e94560; /* Élénk piros alul */
            text-align: center;
        }

        header h1 {
            font-family: 'Press Start 2P', cursive; /* Pixel betűtípus */
            font-size: 3em;
            color: #00ff00; /* Neon zöld */
            text-shadow: 0 0 10px #00ff00, 0 0 20px #00ff00;
            margin-bottom: 10px;
        }

        header p {
            font-size: 1.2em;
            color: #c0c0c0;
        }

        nav {
            background-color: #0f3460; /* Sötétkék navigáció */
            padding: 10px 0;
            text-align: center;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        nav a {
            color: #e94560; /* Élénk piros linkek */
            text-decoration: none;
            padding: 10px 20px;
            margin: 0 5px;
            font-weight: bold;
            transition: all 0.3s ease;
            border-radius: 5px;
        }

        nav a:hover {
            background-color: #e94560; /* Piros háttér hoverre */
            color: #fff; /* Fehér szöveg hoverre */
            text-shadow: 0 0 5px #fff;
        }

        /* Fő tartalom */
        main {
            flex-grow: 1; /* A tartalom kitölti a rendelkezésre álló helyet */
            padding: 40px 0;
        }

        section {
            background-color: #16213e; /* Sötétebb kék szekció háttér */
            padding: 30px;
            margin-bottom: 30px;
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        section h2 {
            font-family: 'Press Start 2P', cursive;
            font-size: 2em;
            color: #00ff00;
            text-align: center;
            margin-bottom: 25px;
            text-shadow: 0 0 8px #00ff00;
        }

        section p {
            font-size: 1.1em;
            color: #c0c0c0;
            text-align: center;
            margin-bottom: 15px;
        }

        hr {
            border: none;
            border-top: 1px dashed rgba(255, 255, 255, 0.2);
            margin: 40px 0;
        }

        /* Termék rács */
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }

        .product-card {
            background-color: #0f3460; /* Termékkártya háttér */
            border: 2px solid #e94560; /* Élénk piros keret */
            padding: 20px;
            text-align: center;
            border-radius: 10px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.6);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .product-card:hover {
            transform: translateY(-8px) scale(1.02); /* Kicsit feljebb ugrik és nő */
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.8), 0 0 20px #e94560; /* Erősebb árnyék és piros fény */
        }

        .product-card img {
            max-width: 100%;
            height: 150px; /* Fix magasság a képeknek */
            object-fit: cover; /* Kitölti a területet, de nem torzít */
            border-radius: 8px;
            margin-bottom: 15px;
            border: 2px solid #00ff00; /* Zöld keret a képeken */
            box-shadow: 0 0 10px rgba(0, 255, 0, 0.5);
        }

        .product-card h3 {
            font-family: 'Press Start 2P', cursive;
            font-size: 1.6em;
            color: #00ff00;
            margin-top: 10px;
            margin-bottom: 10px;
            text-shadow: 0 0 5px #00ff00;
        }

        .product-card .description {
            font-size: 0.95em;
            color: #c0c0c0;
            flex-grow: 1;
            margin-bottom: 20px;
        }

        .product-card .price {
            font-family: 'Press Start 2P', cursive;
            font-size: 1.5em;
            color: #ffd700; /* Arany szín az árnak */
            font-weight: bold;
            margin-bottom: 20px;
            text-shadow: 0 0 5px #ffd700;
        }

        .buy-button {
            background-color: #e94560; /* Élénk piros gomb */
            color: white;
            padding: 12px 25px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-size: 1.1em;
            font-weight: bold;
            transition: background-color 0.3s ease, transform 0.2s ease;
            text-decoration: none;
            display: inline-block;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.4);
            font-family: 'Roboto', sans-serif;
        }

        .buy-button:hover {
            background-color: #ff6b8a; /* Világosabb piros hoverre */
            transform: translateY(-2px);
        }

        /* GYIK és Kapcsolat szekciók */
        .faq-item h3 {
            font-family: 'Roboto', sans-serif;
            color: #e94560;
            font-size: 1.4em;
            margin-top: 20px;
            margin-bottom: 10px;
        }

        .faq-item p {
            text-align: left;
            margin-bottom: 15px;
        }

        .contact-info p {
            text-align: center;
        }

        .contact-info a {
            color: #00ff00;
            text-decoration: none;
            font-weight: bold;
        }

        .contact-info a:hover {
            text-decoration: underline;
        }

        /* Lábjegyzet */
        footer {
            text-align: center;
            padding: 20px 0;
            background-color: #0f3460;
            color: #c0c0c0;
            margin-top: auto; /* A lábjegyzet alulra ragad */
            border-top: 3px solid #e94560;
            font-size: 0.9em;
        }

        /* Reszponzív design */
        @media (max-width: 768px) {
            header h1 {
                font-size: 2em;
            }
            nav a {
                display: block;
                margin: 5px 0;
            }
            .product-grid {
                grid-template-columns: 1fr; /* Egy oszlop mobil nézetben */
            }
        }
    </style>
</head>
<body>

    <header>
        <h1>PixelPrime Webshop</h1>
        <p>Ahol a Minecraft élményed még jobb lesz!</p>
    </header>

    <nav>
        <div class="container">
            <a href="#welcome">Kezdőlap</a>
            <a href="#products">Termékeink</a>
            <a href="#gyik">GYIK</a>
            <a href="#contact">Kapcsolat</a>
        </div>
    </nav>

    <main class="container">
        <section id="welcome">
            <h2>Üdvözlünk a PixelPrime Webshopban!</h2>
            <p>Itt találsz mindent, amire szükséged lehet a **PixelPrime** szerveren, hogy a játékélményed a maximumra pörgesd. Válogass a különleges **rangok**, értékes **kulcsok** és egyedi **kiegészítők** közül!</p>
            <p>Minden vásárlással a szerver fejlődését és fenntartását támogatod. Köszönjük a támogatásod!</p>
        </section>

        <hr>

        <section id="products">
            <h2>Válogass Termékeink Közül!</h2>
            <p>Fedezd fel a legnépszerűbb ajánlatainkat. Kattints a "Megveszem" gombra a részletekért!</p>
            <div class="product-grid">

                <div class="product-card">
                    <img src="https://via.placeholder.com/250x150/00ff00/000000?text=VIP+Rang" alt="PixelPrime VIP Rang">
                    <h3>VIP Rang</h3>
                    <p class="description">Hozzáfért exkluzív parancsokhoz, különleges prefix, több otthon, és extra képességek a szerveren. Légy te a legmenőbb!</p>
                    <p class="price">4990 Ft</p>
                    <a href="URL_A_VÁSÁRLÁSHOZ_VIP" class="buy-button">Megveszem</a>
                </div>

                <div class="product-card">
                    <img src="https://via.placeholder.com/250x150/ffd700/000000?text=MVP+Rang" alt="PixelPrime MVP Rang">
                    <h3>MVP Rang</h3>
                    <p class="description">A VIP rang minden előnye plusz prémium ládák, dedikált chat szín, és még több teleport lehetőség. A szerver igazi uralkodója!</p>
                    <p class="price">7990 Ft</p>
                    <a href="URL_A_VÁSÁRLÁSHOZ_MVP" class="buy-button">Megveszem</a>
                </div>

                <div class="product-card">
                    <img src="https://via.placeholder.com/250x150/e94560/FFFFFF?text=Legendás+Kulcs" alt="PixelPrime Legendás Kulcs">
                    <h3>Legendás Kulcs</h3>
                    <p class="description">Nyiss ki egy epikus kincsesládát, és nyerj garantáltan ritka tárgyakat, értékes nyersanyagokat vagy akár rangokat!</p>
                    <p class="price">990 Ft</p>
                    <a href="URL_A_VÁSÁRLÁSHOZ_KULCS" class="buy-button">Megveszem</a>
                </div>

                <div class="product-card">
                    <img src="https://via.placeholder.com/250x150/007bff/FFFFFF?text=Egyedi+Pet" alt="PixelPrime Egyedi Pet">
                    <h3>Egyedi Pet Csomag</h3>
                    <p class="description">Válassz egy hűséges, egyedi megjelenésű társat, aki elkísér a kalandjaid során. Légy kitűnő a tömegből!</p>
                    <p class="price">2990 Ft</p>
                    <a href="URL_A_VÁSÁRLÁSHOZ_PET" class="buy-button">Megveszem</a>
                </div>

                <div class="product-card">
                    <img src="https://via.placeholder.com/250x150/6a0dad/FFFFFF?text=Pénz+Csomag" alt="PixelPrime Pénz Csomag">
                    <h3>Pénz Csomag (50.000$)</h3>
                    <p class="description">Szerezz be extra játékpénzt, hogy fejleszthesd a bázisod, vegyél eszközöket, vagy kereskedj más játékosokkal!</p>
                    <p class="price">1490 Ft</p>
                    <a href="URL_A_VÁSÁRLÁSHOZ_PÉNZ" class="buy-button">Megveszem</a>
                </div>

            </div>
        </section>

        <hr>

        <section id="gyik">
            <h2>Gyakran Ismételt Kérdések (GYIK)</h2>
            <div class="faq-item">
                <h3>Hogyan történik a vásárlás és a termék aktiválása?</h3>
                <p>A "Megveszem" gombra kattintva átirányítunk a biztonságos fizetési oldalunkra. A fizetés feldolgozása után a termék automatikusan hozzárendelődik a Minecraft nevedhez (kérjük, ügyelj a helyes felhasználónév megadására!). A legtöbb termék azonnal aktiválódik a szerverre való belépéskor, vagy a következő újraindításkor.</p>
            </div>
            <div class="faq-item">
                <h3>Milyen fizetési módokat fogadtok el?</h3>
                <p>Jelenleg a következő fizetési módokat támogatjuk: PayPal, bankkártyás fizetés (Stripe / Barion), és ... (itt sorold fel a többit, pl. telefonos fizetés, banki átutalás, stb.).</p>
            </div>
            <div class="faq-item">
                <h3>Mi történik, ha nem kapom meg a vásárolt terméket?</h3>
                <p>Először is, ellenőrizd, hogy helyes Minecraft felhasználónevet adtál-e meg. Ha minden rendben van, és a termék 15 percen belül sem jelenik meg, kérjük, vedd fel velünk a kapcsolatot a Kapcsolat szekcióban megadott elérhetőségeinken, és a tranzakciós azonosítóval együtt küldj egy üzenetet. Segítünk megoldani a problémát!</p>
            </div>
            <div class="faq-item">
                <h3>Támogatom a szervert a vásárlásommal?</h3>
                <p>Igen! Minden egyes vásárlás közvetlenül a PixelPrime szerver fejlesztését, karbantartását és a közösségi események szervezését segíti. Hatalmas köszönet érte!</p>
            </div>
        </section>

        <hr>

        <section id="contact">
            <h2>Kapcsolat</h2>
            <div class="contact-info">
                <p>Ha kérdésed van, vagy segítségre van szükséged, ne habozz felvenni velünk a kapcsolatot!</p>
                <p>Discord: <a href="https://discord.gg/yourdiscordlink" target="_blank">discord.gg/PixelPrimeDiscord</a> (a leggyorsabb válaszért)</p>
                <p>Email: <a href="mailto:support@pixelprime.com">support@pixelprime.com</a></p>
                <p>Facebook: <a href="https://facebook.com/yourfacebookpage" target="_blank">facebook.com/PixelPrimeMC</a></p>
            </div>
        </section>

    </main>

    <footer>
        <div class="container">
            <p>&copy; 2025 PixelPrime Minecraft Szerver. Minden jog fenntartva. | <a href="URL_ADATVEDELMI_NYILATKOZAT" style="color: #e94560;">Adatvédelmi Nyilatkozat</a> | <a href="URL_ÁSZF" style="color: #e94560;">Általános Szerződési Feltételek</a></p>
            <p>Domain: bolt-pixelprime.webhop.me</p>
        </div>
    </footer>

</body>
</html>
