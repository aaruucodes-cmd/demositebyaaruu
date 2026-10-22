<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MAISON L'AURA | Haute Joaillerie & High Fine Jewelry</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        gold: {
                            100: '#FDF8EC',
                            300: '#E5C887',
                            400: '#D4AF37',
                            500: '#AA771C',
                            600: '#855B10'
                        },
                        obsidian: '#0A0A0C'
                    },
                    fontFamily: {
                        serif: ['Cinzel', 'serif'],
                        sans: ['Montserrat', 'sans-serif']
                    }
                }
            }
        }
    </script>
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;500;600;700;800;900&family=Montserrat:wght@200;300;400;500;600&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Montserrat', sans-serif;
            background-color: #0A0A0C;
            color: #F3F3F3;
        }
        .font-cinzel { font-family: 'Cinzel', serif; }
        .gold-text {
            background: linear-gradient(135deg, #BF953F 0%, #FCF6BA 25%, #B38728 50%, #FBF5B7 75%, #AA771C 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .gold-border {
            border-image: linear-gradient(to right, #BF953F, #FCF6BA, #AA771C) 1;
        }
        /* Custom Glassmorphism */
        .glass-panel {
            background: rgba(18, 18, 22, 0.75);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(212, 175, 55, 0.15);
        }
        /* Hide scrollbars */
        .no-scrollbar::-webkit-scrollbar { display: none; }
        .no-scrollbar { -ms-overflow-style: none; scrollbar-width: none; }
        #webgl-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            z-index: 0;
            pointer-events: none;
        }
    </style>
</head>
<body class="bg-obsidian text-gray-200 antialiased selection:bg-gold-400 selection:text-black">

    <!-- 3D Canvas Background -->
    <div id="webgl-bg"></div>

    <!-- Announcement Bar -->
    <div class="relative z-50 bg-gradient-to-r from-gold-600 via-gold-400 to-gold-600 text-black text-[10px] sm:text-xs font-semibold uppercase tracking-[0.2em] py-2 text-center">
        Complimentary White-Glove Worldwide Delivery & Insured Shipping &bull; Private Concierge Available
    </div>

    <!-- Navigation Header -->
    <header class="sticky top-0 z-40 glass-panel border-b border-gold-400/20 px-6 lg:px-16 py-4 flex items-center justify-between">
        <a href="#" class="flex flex-col">
            <span class="text-2xl lg:text-3xl font-cinzel font-black tracking-[0.25em] gold-text">MAISON L'AURA</span>
            <span class="text-[8px] tracking-[0.4em] uppercase text-gray-400 text-center font-light">PARIS &bull; NEW YORK &bull; TOKYO</span>
        </a>

        <nav class="hidden md:flex items-center space-x-10 text-xs tracking-[0.2em] uppercase font-medium text-gray-300">
            <a href="#collections" class="hover:text-gold-400 transition">High Jewelry</a>
            <a href="#customizer" class="hover:text-gold-400 transition">Atelier Studio</a>
            <a href="#story" class="hover:text-gold-400 transition">Heritage</a>
            <a href="#boutique" class="hover:text-gold-400 transition">Flagships</a>
        </nav>

        <div class="flex items-center space-x-6">
            <button onclick="toggleCart()" class="relative p-2 text-gray-300 hover:text-gold-400 transition">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z"/>
                </svg>
                <span id="cart-count" class="absolute top-0 right-0 w-4 h-4 rounded-full bg-gold-400 text-black text-[10px] font-bold flex items-center justify-center">0</span>
            </button>
            <button class="hidden sm:block border border-gold-400/50 hover:bg-gold-400/10 text-gold-300 text-xs uppercase tracking-widest px-5 py-2.5 rounded-full transition">
                Book Consultation
            </button>
        </div>
    </header>

    <!-- Main Container -->
    <main class="relative z-10">

        <!-- HERO SECTION -->
        <section class="min-h-screen flex flex-col items-center justify-center text-center px-6 py-20 relative">
            <div class="max-w-4xl mx-auto space-y-6">
                <span class="inline-block border border-gold-400/40 bg-gold-400/5 text-gold-300 text-xs font-semibold uppercase tracking-[0.3em] px-4 py-1.5 rounded-full">
                    2026 High Jewelry Collection
                </span>
                <h1 class="text-5xl sm:text-7xl lg:text-8xl font-cinzel font-bold tracking-tight gold-text leading-tight">
                    THE ARCHITECTURE OF RADIANCE
                </h1>
                <p class="max-w-2xl mx-auto text-gray-300 text-sm sm:text-base font-light leading-relaxed">
                    Sculpted by hand in 18k Fairmined Gold and crowned with rare D-Flawless diamonds. Discover the pinnacle of modern fine jewelry design.
                </p>
                <div class="pt-6 flex flex-col sm:flex-row items-center justify-center gap-4">
                    <a href="#collections" class="w-full sm:w-auto bg-gradient-to-r from-gold-500 to-gold-400 hover:from-gold-400 hover:to-gold-300 text-black font-semibold text-xs tracking-[0.2em] uppercase px-8 py-4 rounded-full transition shadow-lg shadow-gold-500/20">
                        Explore Collection
                    </a>
                    <a href="#customizer" class="w-full sm:w-auto border border-white/20 hover:border-gold-400 text-white hover:text-gold-300 text-xs tracking-[0.2em] uppercase px-8 py-4 rounded-full transition glass-panel">
                        Design Bespoke Ring
                    </a>
                </div>
            </div>

            <!-- Scroll Indicator -->
            <div class="absolute bottom-8 left-1/2 -translate-x-1/2 flex flex-col items-center space-y-2 opacity-70">
                <span class="text-[10px] tracking-[0.3em] uppercase text-gray-400">Scroll to Experience</span>
                <div class="w-5 h-9 border-2 border-gold-400/40 rounded-full flex justify-center p-1">
                    <div class="w-1 h-2 bg-gold-400 rounded-full animate-bounce"></div>
                </div>
            </div>
        </section>

        <!-- CATEGORIES BAR -->
        <section class="border-y border-gold-400/10 bg-black/50 py-8 px-6 lg:px-16">
            <div class="max-w-7xl mx-auto grid grid-cols-2 md:grid-cols-4 gap-6 text-center">
                <div class="p-4 rounded-xl glass-panel hover:border-gold-400/50 transition cursor-pointer">
                    <h3 class="font-cinzel text-lg text-gold-300">Rings & Solitaires</h3>
                    <p class="text-xs text-gray-400 font-light mt-1">42 Designs &bull; From $4,800</p>
                </div>
                <div class="p-4 rounded-xl glass-panel hover:border-gold-400/50 transition cursor-pointer">
                    <h3 class="font-cinzel text-lg text-gold-300">Necklaces & Pendants</h3>
                    <p class="text-xs text-gray-400 font-light mt-1">28 Designs &bull; From $6,200</p>
                </div>
                <div class="p-4 rounded-xl glass-panel hover:border-gold-400/50 transition cursor-pointer">
                    <h3 class="font-cinzel text-lg text-gold-300">High Fine Earrings</h3>
                    <p class="text-xs text-gray-400 font-light mt-1">35 Designs &bull; From $3,500</p>
                </div>
                <div class="p-4 rounded-xl glass-panel hover:border-gold-400/50 transition cursor-pointer">
                    <h3 class="font-cinzel text-lg text-gold-300">Bespoke Bracelets</h3>
                    <p class="text-xs text-gray-400 font-light mt-1">19 Designs &bull; From $8,900</p>
                </div>
            </div>
        </section>

        <!-- FEATURED E-COMMERCE PRODUCTS CATALOG -->
        <section id="collections" class="max-w-7xl mx-auto px-6 lg:px-16 py-24">
            <div class="flex flex-col md:flex-row justify-between items-start md:items-end mb-16 gap-6">
                <div>
                    <span class="text-gold-400 text-xs font-semibold tracking-[0.3em] uppercase">Masterpiece Series</span>
                    <h2 class="text-3xl sm:text-5xl font-cinzel font-bold text-white mt-2">Curated High Fine Jewelry</h2>
                </div>
                <div class="flex space-x-3 text-xs uppercase tracking-widest">
                    <button class="px-4 py-2 border border-gold-400 bg-gold-400/20 text-gold-300 rounded-full font-medium">All Pieces</button>
                    <button class="px-4 py-2 border border-white/10 hover:border-gold-400/50 text-gray-400 hover:text-white rounded-full transition">Rings</button>
                    <button class="px-4 py-2 border border-white/10 hover:border-gold-400/50 text-gray-400 hover:text-white rounded-full transition">Necklaces</button>
                </div>
            </div>

            <!-- PRODUCT GRID -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8" id="product-grid">
                <!-- Products dynamically rendered by JS -->
            </div>
        </section>

        <!-- ATELIER BESPOKE RING CUSTOMIZER SECTION -->
        <section id="customizer" class="glass-panel border-y border-gold-400/20 my-12 py-20 px-6 lg:px-16 relative overflow-hidden">
            <div class="max-w-7xl mx-auto grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                
                <div class="space-y-6">
                    <span class="text-gold-400 text-xs font-semibold tracking-[0.3em] uppercase">Interactive Configurator</span>
                    <h2 class="text-4xl sm:text-5xl font-cinzel font-bold text-white leading-tight">
                        Craft Your Signature Solitaire
                    </h2>
                    <p class="text-gray-300 text-sm font-light leading-relaxed">
                        Customize stone cut, metal alloy, and carat weight in real time. Every bespoke piece is hand-finished by master craftspeople in Paris.
                    </p>

                    <!-- Customizer Options -->
                    <div class="space-y-6 border-t border-white/10 pt-6">
                        <!-- Metal Selection -->
                        <div>
                            <label class="block text-xs uppercase tracking-widest text-gray-400 mb-3">1. Select Precious Metal</label>
                            <div class="flex space-x-4">
                                <button onclick="setMetal('yellow')" id="btn-metal-yellow" class="flex-1 py-3 px-4 rounded-xl border border-gold-400 bg-gold-400/20 text-gold-300 text-xs uppercase tracking-wider font-semibold">
                                    18K Yellow Gold
                                </button>
                                <button onclick="setMetal('white')" id="btn-metal-white" class="flex-1 py-3 px-4 rounded-xl border border-white/20 bg-white/5 text-gray-300 text-xs uppercase tracking-wider hover:border-gold-400 transition">
                                    Platinum / White Gold
                                </button>
                                <button onclick="setMetal('rose')" id="btn-metal-rose" class="flex-1 py-3 px-4 rounded-xl border border-white/20 bg-white/5 text-gray-300 text-xs uppercase tracking-wider hover:border-gold-400 transition">
                                    18K Rose Gold
                                </button>
                            </div>
                        </div>

                        <!-- Carat Size -->
                        <div>
                            <div class="flex justify-between text-xs uppercase tracking-widest text-gray-400 mb-3">
                                <span>2. Diamond Carat Weight</span>
                                <span id="carat-val" class="text-gold-300 font-semibold">2.5 Carat</span>
                            </div>
                            <input type="range" min="1.0" max="5.0" step="0.1" value="2.5" id="carat-slider" oninput="updateCarat(this.value)" class="w-full accent-gold-400 bg-gray-800 rounded-lg cursor-pointer">
                        </div>

                        <!-- Price Calculation -->
                        <div class="p-6 rounded-2xl bg-black/60 border border-gold-400/30 flex justify-between items-center">
                            <div>
                                <span class="text-[10px] text-gray-400 uppercase tracking-widest block">Estimated Bespoke Price</span>
                                <span id="custom-price" class="text-2xl sm:text-3xl font-cinzel font-bold text-gold-300">$18,400</span>
                            </div>
                            <button onclick="addCustomToCart()" class="bg-gold-400 hover:bg-gold-300 text-black text-xs uppercase tracking-widest font-semibold px-6 py-3 rounded-full transition">
                                Reserve Custom Ring
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Customizer Visual Preview Box -->
                <div class="relative flex justify-center items-center h-[400px] lg:h-[500px] rounded-3xl border border-gold-400/20 bg-gradient-to-b from-obsidian via-black to-obsidian p-8 overflow-hidden">
                    <img id="custom-ring-img" src="https://images.unsplash.com/photo-1605100804763-247f67b3557e?auto=format&fit=crop&w=1000&q=80" alt="Bespoke Solitaire Ring" class="max-h-full max-w-full object-contain filter drop-shadow-[0_20px_50px_rgba(212,175,55,0.25)] transition-all duration-500">
                    <div class="absolute bottom-6 left-6 text-xs text-gray-400 bg-black/60 backdrop-blur-md px-4 py-2 rounded-full border border-white/10">
                        Live Render Preset: <span id="preset-label" class="text-gold-300 font-semibold">18K Yellow Gold - 2.5CT</span>
                    </div>
                </div>

            </div>
        </section>

        <!-- HERITAGE & CRAFTSMANSHIP STORY -->
        <section id="story" class="max-w-7xl mx-auto px-6 lg:px-16 py-24">
            <div class="grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
                <div class="relative group">
                    <div class="absolute -inset-2 bg-gradient-to-r from-gold-500 to-amber-600 rounded-3xl blur opacity-25 group-hover:opacity-40 transition duration-1000"></div>
                    <img src="https://images.unsplash.com/photo-1535632066927-ab7c9ab60908?auto=format&fit=crop&w=1200&q=80" alt="Craftsmanship" class="relative rounded-2xl border border-gold-400/30 object-cover shadow-2xl h-[500px] w-full">
                </div>
                <div class="space-y-6">
                    <span class="text-gold-400 text-xs font-semibold tracking-[0.3em] uppercase">Uncompromising Excellence</span>
                    <h2 class="text-4xl sm:text-5xl font-cinzel font-bold text-white leading-tight">
                        Over Three Decades of Artisanal Legacy
                    </h2>
                    <p class="text-gray-300 text-sm font-light leading-relaxed">
                        Each jewel created in our ateliers undergoes over 120 hours of intricate crafting. From selecting Conflict-Free Certified diamonds to hand-polishing solid 18k gold bands, we define fine jewelry for generations to come.
                    </p>
                    <div class="grid grid-cols-2 gap-6 pt-4 border-t border-white/10">
                        <div>
                            <span class="font-cinzel text-3xl text-gold-300 font-bold">100%</span>
                            <p class="text-xs text-gray-400 mt-1 uppercase tracking-wider">Ethically Sourced Gems</p>
                        </div>
                        <div>
                            <span class="font-cinzel text-3xl text-gold-300 font-bold">GIA</span>
                            <p class="text-xs text-gray-400 mt-1 uppercase tracking-wider">Certified Excellence</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- FLAGSHIP STORES -->
        <section id="boutique" class="border-t border-gold-400/20 bg-black/60 py-24 px-6 lg:px-16">
            <div class="max-w-7xl mx-auto text-center space-y-4 mb-16">
                <span class="text-gold-400 text-xs font-semibold tracking-[0.3em] uppercase">Global Destinations</span>
                <h2 class="text-4xl font-cinzel font-bold text-white">Visit Our Flagship Boutiques</h2>
            </div>
            <div class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="glass-panel p-8 rounded-2xl border border-gold-400/20 hover:border-gold-400/50 transition">
                    <h3 class="font-cinzel text-2xl text-gold-300 mb-2">Paris</h3>
                    <p class="text-xs text-gray-400 mb-4">Place Vendôme, 75001 Paris, France</p>
                    <p class="text-xs text-gray-300 font-light">+33 1 42 68 00 00</p>
                </div>
                <div class="glass-panel p-8 rounded-2xl border border-gold-400/20 hover:border-gold-400/50 transition">
                    <h3 class="font-cinzel text-2xl text-gold-300 mb-2">New York</h3>
                    <p class="text-xs text-gray-400 mb-4">742 Fifth Avenue, New York, NY 10019</p>
                    <p class="text-xs text-gray-300 font-light">+1 212 555 0192</p>
                </div>
                <div class="glass-panel p-8 rounded-2xl border border-gold-400/20 hover:border-gold-400/50 transition">
                    <h3 class="font-cinzel text-2xl text-gold-300 mb-2">Tokyo</h3>
                    <p class="text-xs text-gray-400 mb-4">Ginza 6-Chome, Chuo-ku, Tokyo 104-0061</p>
                    <p class="text-xs text-gray-300 font-light">+81 3 5555 0143</p>
                </div>
            </div>
        </section>

    </main>

    <!-- SHOPPING CART DRAWER OVERLAY -->
    <div id="cart-drawer" class="fixed inset-y-0 right-0 z-50 w-full max-w-md bg-obsidian border-l border-gold-400/30 p-8 transform translate-x-full transition-transform duration-300 shadow-2xl flex flex-col justify-between">
        <div>
            <div class="flex justify-between items-center border-b border-white/10 pb-6 mb-6">
                <h3 class="font-cinzel text-2xl text-gold-300 font-bold">Your Vault (<span id="drawer-count">0</span>)</h3>
                <button onclick="toggleCart()" class="text-gray-400 hover:text-white">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/></svg>
                </button>
            </div>
            <div id="cart-items" class="space-y-4 max-h-[50vh] overflow-y-auto pr-2 no-scrollbar">
                <p id="empty-cart-msg" class="text-gray-500 text-xs text-center py-12">Your shopping vault is currently empty.</p>
            </div>
        </div>

        <div class="border-t border-white/10 pt-6 space-y-4">
            <div class="flex justify-between text-sm">
                <span class="text-gray-400">Total Valuation:</span>
                <span id="cart-total" class="font-cinzel text-xl text-gold-300 font-bold">$0</span>
            </div>
            <button class="w-full bg-gradient-to-r from-gold-500 to-gold-400 hover:from-gold-400 hover:to-gold-300 text-black font-bold text-xs uppercase tracking-[0.2em] py-4 rounded-full transition shadow-lg shadow-gold-500/20">
                Proceed to Secure Checkout
            </button>
        </div>
    </div>

    <!-- FOOTER -->
    <footer class="relative z-10 bg-black border-t border-gold-400/20 text-gray-400 text-xs py-16 px-6 lg:px-16">
        <div class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-4 gap-12 mb-12">
            <div>
                <span class="text-2xl font-cinzel font-bold gold-text block mb-4">MAISON L'AURA</span>
                <p class="font-light leading-relaxed">Defining fine luxury, rarity, and high jewelry elegance worldwide.</p>
            </div>
            <div>
                <h4 class="font-cinzel text-white text-sm uppercase tracking-widest mb-4">Collections</h4>
                <ul class="space-y-2 font-light">
                    <li><a href="#" class="hover:text-gold-300 transition">Engagement Rings</a></li>
                    <li><a href="#" class="hover:text-gold-300 transition">Solitaire Necklaces</a></li>
                    <li><a href="#" class="hover:text-gold-300 transition">High Jewelry Sets</a></li>
                </ul>
            </div>
            <div>
                <h4 class="font-cinzel text-white text-sm uppercase tracking-widest mb-4">Client Care</h4>
                <ul class="space-y-2 font-light">
                    <li><a href="#" class="hover:text-gold-300 transition">Book Appointments</a></li>
                    <li><a href="#" class="hover:text-gold-300 transition">Jewelry Care & Cleaning</a></li>
                    <li><a href="#" class="hover:text-gold-300 transition">GIA Certification Verification</a></li>
                </ul>
            </div>
            <div>
                <h4 class="font-cinzel text-white text-sm uppercase tracking-widest mb-4">Maison Newsletter</h4>
                <p class="font-light mb-4">Subscribe to receive exclusive invitations to high jewelry unveilings.</p>
                <div class="flex">
                    <input type="email" placeholder="Enter your email" class="bg-gray-900 border border-white/20 px-4 py-2 text-xs text-white rounded-l-lg w-full focus:outline-none focus:border-gold-400">
                    <button class="bg-gold-400 text-black px-4 rounded-r-lg font-semibold uppercase hover:bg-gold-300 transition">Join</button>
                </div>
            </div>
        </div>
        <div class="max-w-7xl mx-auto border-t border-white/10 pt-8 flex flex-col sm:flex-row justify-between items-center text-gray-500">
            <p>&copy; 2026 MAISON L'AURA Haute Joaillerie. All Rights Reserved.</p>
            <div class="flex space-x-6 mt-4 sm:mt-0">
                <a href="#" class="hover:text-gray-300">Privacy Policy</a>
                <a href="#" class="hover:text-gray-300">Terms of Service</a>
                <a href="#" class="hover:text-gray-300">Ethics & Sustainability</a>
            </div>
        </div>
    </footer>

    <!-- Three.js Library for Background Canvas -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>

    <script>
        // --- 1. PRODUCT DATABASE ---
        const products = [
            {
                id: 1,
                title: "L'Aura Royal Solitaire Ring",
                price: 14500,
                category: "Rings",
                carat: "3.2 Carats",
                image: "https://images.unsplash.com/photo-1605100804763-247f67b3557e?auto=format&fit=crop&w=800&q=80",
                badge: "Signature"
            },
            {
                id: 2,
                title: "Imperial Emerald-Cut Diamond Pendant",
                price: 22800,
                category: "Necklaces",
                carat: "4.5 Carats",
                image: "https://images.unsplash.com/photo-1599643478518-a784e5dc4c8f?auto=format&fit=crop&w=800&q=80",
                badge: "High Fine"
            },
            {
                id: 3,
                title: "Sovereign Diamond Drop Earrings",
                price: 9600,
                category: "Earrings",
                carat: "2.1 Carats Each",
                image: "https://images.unsplash.com/photo-1630019852942-f89202989a59?auto=format&fit=crop&w=800&q=80",
                badge: "Popular"
            },
            {
                id: 4,
                title: "Celestial Pavilion Yellow Diamond Ring",
                price: 34000,
                category: "Rings",
                carat: "5.0 Carats Fancy Yellow",
                image: "https://images.unsplash.com/photo-1603561591411-07134e71a2a9?auto=format&fit=crop&w=800&q=80",
                badge: "Rare Find"
            },
            {
                id: 5,
                title: "Elysian Micro-Pave Gold Cuff",
                price: 18200,
                category: "Bracelets",
                carat: "3.8 Carats",
                image: "https://images.unsplash.com/photo-1611591475179-be252077e69c?auto=format&fit=crop&w=800&q=80",
                badge: "Bespoke"
            },
            {
                id: 6,
                title: "Eternal Radiance Oval Cut Band",
                price: 11400,
                category: "Rings",
                carat: "2.8 Carats",
                image: "https://images.unsplash.com/photo-1602751584552-8ba73aad10e1?auto=format&fit=crop&w=800&q=80",
                badge: "Classic"
            }
        ];

        let cart = [];

        // Render Products
        function renderProducts() {
            const grid = document.getElementById('product-grid');
            grid.innerHTML = products.map(p => `
                <div class="glass-panel rounded-2xl overflow-hidden border border-gold-400/20 group hover:border-gold-400/60 transition duration-500 flex flex-col justify-between">
                    <div class="relative overflow-hidden bg-black/40 h-[320px] flex items-center justify-center p-6">
                        <span class="absolute top-4 left-4 z-10 border border-gold-400/50 bg-black/60 backdrop-blur-md text-gold-300 text-[10px] uppercase tracking-widest px-3 py-1 rounded-full font-semibold">
                            ${p.badge}
                        </span>
                        <img src="${p.image}" alt="${p.title}" class="max-h-full object-cover group-hover:scale-105 transition duration-700 ease-out">
                    </div>
                    <div class="p-6 space-y-4 flex-1 flex flex-col justify-between border-t border-white/5">
                        <div>
                            <div class="text-[10px] text-gray-400 uppercase tracking-widest">${p.category} &bull; ${p.carat}</div>
                            <h3 class="font-cinzel text-xl text-white font-semibold mt-1 group-hover:text-gold-300 transition">${p.title}</h3>
                        </div>
                        <div class="flex items-center justify-between pt-2">
                            <span class="font-cinzel text-2xl font-bold text-gold-300">$${p.price.toLocaleString()}</span>
                            <button onclick="addToCart(${p.id})" class="border border-gold-400/50 hover:bg-gold-400 text-gold-300 hover:text-black font-semibold text-[11px] uppercase tracking-widest px-5 py-2.5 rounded-full transition">
                                Add To Vault
                            </button>
                        </div>
                    </div>
                </div>
            `).join('');
        }
        renderProducts();

        // --- 2. CART FUNCTIONS ---
        function toggleCart() {
            const drawer = document.getElementById('cart-drawer');
            drawer.classList.toggle('translate-x-full');
        }

        function addToCart(id) {
            const item = products.find(p => p.id === id);
            cart.push(item);
            updateCartUI();
            toggleCart();
        }

        function updateCartUI() {
            document.getElementById('cart-count').innerText = cart.length;
            document.getElementById('drawer-count').innerText = cart.length;

            const cartContainer = document.getElementById('cart-items');
            const emptyMsg = document.getElementById('empty-cart-msg');

            if(cart.length === 0) {
                cartContainer.innerHTML = `<p class="text-gray-500 text-xs text-center py-12">Your shopping vault is currently empty.</p>`;
            } else {
                cartContainer.innerHTML = cart.map((item, index) => `
                    <div class="flex items-center justify-between p-4 glass-panel rounded-xl border border-white/10">
                        <img src="${item.image}" class="w-14 h-14 object-cover rounded-lg">
                        <div class="flex-1 px-4">
                            <h4 class="font-cinzel text-xs text-white font-semibold">${item.title}</h4>
                            <span class="text-xs text-gold-300 font-bold">$${item.price.toLocaleString()}</span>
                        </div>
                        <button onclick="removeFromCart(${index})" class="text-gray-500 hover:text-red-400 text-xs">Remove</button>
                    </div>
                `).join('');
            }

            const total = cart.reduce((acc, curr) => acc + curr.price, 0);
            document.getElementById('cart-total').innerText = `$${total.toLocaleString()}`;
        }

        function removeFromCart(index) {
            cart.splice(index, 1);
            updateCartUI();
        }

        // --- 3. CUSTOMIZER LOGIC ---
        let selectedMetal = 'yellow';
        let selectedCarat = 2.5;

        function setMetal(type) {
            selectedMetal = type;
            document.getElementById('btn-metal-yellow').className = type === 'yellow' ? "flex-1 py-3 px-4 rounded-xl border border-gold-400 bg-gold-400/20 text-gold-300 text-xs uppercase tracking-wider font-semibold" : "flex-1 py-3 px-4 rounded-xl border border-white/20 bg-white/5 text-gray-300 text-xs uppercase tracking-wider hover:border-gold-400 transition";
            document.getElementById('btn-metal-white').className = type === 'white' ? "flex-1 py-3 px-4 rounded-xl border border-gold-400 bg-gold-400/20 text-gold-300 text-xs uppercase tracking-wider font-semibold" : "flex-1 py-3 px-4 rounded-xl border border-white/20 bg-white/5 text-gray-300 text-xs uppercase tracking-wider hover:border-gold-400 transition";
            document.getElementById('btn-metal-rose').className = type === 'rose' ? "flex-1 py-3 px-4 rounded-xl border border-gold-400 bg-gold-400/20 text-gold-300 text-xs uppercase tracking-wider font-semibold" : "flex-1 py-3 px-4 rounded-xl border border-white/20 bg-white/5 text-gray-300 text-xs uppercase tracking-wider hover:border-gold-400 transition";
            calculateCustomPrice();
        }

        function updateCarat(val) {
            selectedCarat = parseFloat(val);
            document.getElementById('carat-val').innerText = `${selectedCarat.toFixed(1)} Carat`;
            calculateCustomPrice();
        }

        function calculateCustomPrice() {
            const basePrice = 6000;
            const price = Math.round(basePrice + (selectedCarat * 4800) + (selectedMetal === 'white' ? 1200 : 0));
            document.getElementById('custom-price').innerText = `$${price.toLocaleString()}`;
            document.getElementById('preset-label').innerText = `${selectedMetal.toUpperCase()} Gold - ${selectedCarat.toFixed(1)}CT Solitaire`;
        }

        function addCustomToCart() {
            const customItem = {
                id: Date.now(),
                title: `Bespoke Solitaire (${selectedCarat}CT / ${selectedMetal.toUpperCase()})`,
                price: parseInt(document.getElementById('custom-price').innerText.replace('$', '').replace(',', '')),
                category: "Custom Ring",
                image: "https://images.unsplash.com/photo-1605100804763-247f67b3557e?auto=format&fit=crop&w=800&q=80"
            };
            cart.push(customItem);
            updateCartUI();
            toggleCart();
        }

        // --- 4. ELEGANT 3D SPARKLE CANVAS BACKGROUND (THREE.JS) ---
        const container = document.getElementById('webgl-bg');
        const scene = new THREE.Scene();
        const camera = new THREE.PerspectiveCamera(60, window.innerWidth / window.innerHeight, 0.1, 1000);
        camera.position.z = 5;

        const renderer = new THREE.WebGLRenderer({ alpha: true, antialias: true });
        renderer.setSize(window.innerWidth, window.innerHeight);
        renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2));
        container.appendChild(renderer.domElement);

        // Floating Diamond Gold Dust Particles
        const geometry = new THREE.BufferGeometry();
        const count = 500;
        const positions = new Float32Array(count * 3);

        for (let i = 0; i < count * 3; i++) {
            positions[i] = (Math.random() - 0.5) * 15;
        }
        geometry.setAttribute('position', new THREE.BufferAttribute(positions, 3));

        const material = new THREE.PointsMaterial({
            size: 0.04,
            color: 0xD4AF37,
            transparent: true,
            opacity: 0.5
        });

        const points = new THREE.Points(geometry, material);
        scene.add(points);

        function animate() {
            requestAnimationFrame(animate);
            points.rotation.y += 0.0005;
            points.rotation.x += 0.0002;
            renderer.render(scene, camera);
        }
        animate();

        window.addEventListener('resize', () => {
            camera.aspect = window.innerWidth / window.innerHeight;
            camera.updateProjectionMatrix();
            renderer.setSize(window.innerWidth, window.innerHeight);
        });
    </script>
</body>
</html>
