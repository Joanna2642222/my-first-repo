<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sandomierska Winery | Premium Polish Wines</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#8B0000', // 深红色
                        secondary: '#D4AF37', // 金色
                        dark: '#1A1A1A', // 深黑色
                        light: '#F5F5DC', // 米白色
                        'wine-red': '#5D001E',
                        'wine-dark': '#2D0000',
                        'wine-light': '#E8C2CA',
                    },
                    fontFamily: {
                        serif: ['Playfair Display', 'serif'],
                        sans: ['Montserrat', 'sans-serif'],
                    },
                    backgroundImage: {
                        'hero-pattern': "url('https://i.pinimg.com/736x/36/d0/cf/36d0cfa9b6ddda2bff69315c9ee0977b.jpg')",
                    }
                },
            }
        }
    </script>
    <style type="text/tailwindcss">
        @layer utilities {
            .content-auto {
                content-visibility: auto;
            }
            .text-shadow {
                text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
            }
            .bg-blur {
                backdrop-filter: blur(8px);
            }
            .animate-fade-in {
                animation: fadeIn 0.8s ease-in-out;
            }
            .animate-slide-up {
                animation: slideUp 0.8s ease-out;
            }
            .animate-scale {
                transition: transform 0.3s ease;
            }
            .animate-scale:hover {
                transform: scale(1.05);
            }
            .wine-glass {
                position: relative;
                display: inline-block;
            }
            .wine-glass::after {
                content: '';
                position: absolute;
                bottom: -10px;
                left: 50%;
                transform: translateX(-50%);
                width: 60%;
                height: 2px;
                background: linear-gradient(90deg, transparent, #8B0000, transparent);
            }
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes slideUp {
            from { transform: translateY(30px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700&family=Montserrat:wght@300;400;500;600;700&display=swap" rel="stylesheet">
</head>
<body class="bg-dark text-light font-sans">
    <!-- 导航栏 -->
    <nav id="navbar" class="fixed w-full z-50 transition-all duration-500">
        <div class="container mx-auto px-4 py-4 flex justify-between items-center">
            <a href="#" class="text-secondary font-serif text-2xl md:text-3xl tracking-wider">Sandomierska<span class="text-light">Winery</span></a>
            
            <!-- 移动端菜单按钮 -->
            <button id="menu-toggle" class="md:hidden text-light text-2xl focus:outline-none">
                <i class="fa fa-bars"></i>
            </button>
            
            <!-- 桌面端导航 -->
            <ul class="hidden md:flex space-x-8 items-center">
                <li><a href="#home" class="text-light hover:text-secondary transition-colors duration-300">Home</a></li>
                <li><a href="#about" class="text-light hover:text-secondary transition-colors duration-300">About Us</a></li>
                <li><a href="#wines" class="text-light hover:text-secondary transition-colors duration-300">Our Wines</a></li>
                <li><a href="#production" class="text-light hover:text-secondary transition-colors duration-300">Production</a></li>
                <li><a href="#experiences" class="text-light hover:text-secondary transition-colors duration-300">Experiences</a></li>
                <li><a href="#contact" class="text-light hover:text-secondary transition-colors duration-300">Contact</a></li>
                <li>
                    <a href="#shop" class="bg-primary hover:bg-wine-red text-white px-6 py-2 rounded-full transition-all duration-300 transform hover:scale-105">
                        SHOP NOW
                    </a>
                </li>
            </ul>
        </div>
        
        <!-- 移动端菜单 -->
        <div id="mobile-menu" class="hidden md:hidden bg-dark/95 bg-blur">
            <ul class="container mx-auto px-4 py-4 flex flex-col space-y-4">
                <li><a href="#home" class="text-light hover:text-secondary transition-colors duration-300 py-2 block">Home</a></li>
                <li><a href="#about" class="text-light hover:text-secondary transition-colors duration-300 py-2 block">About Us</a></li>
                <li><a href="#wines" class="text-light hover:text-secondary transition-colors duration-300 py-2 block">Our Wines</a></li>
                <li><a href="#production" class="text-light hover:text-secondary transition-colors duration-300 py-2 block">Production</a></li>
                <li><a href="#experiences" class="text-light hover:text-secondary transition-colors duration-300 py-2 block">Experiences</a></li>
                <li><a href="#contact" class="text-light hover:text-secondary transition-colors duration-300 py-2 block">Contact</a></li>
                <li>
                    <a href="#shop" class="bg-primary hover:bg-wine-red text-white px-6 py-2 rounded-full transition-all duration-300 inline-block">
                        SHOP NOW
                    </a>
                </li>
            </ul>
        </div>
    </nav>

    <!-- 英雄区域 -->
    <section id="home" class="relative h-screen flex items-center justify-center overflow-hidden">
        <div class="absolute inset-0 z-0">
            <img src="https://i.pinimg.com/736x/36/d0/cf/36d0cfa9b6ddda2bff69315c9ee0977b.jpg" alt="Sandomierska Winery landscape" class="w-full h-full object-cover">
            <div class="absolute inset-0 bg-dark/50"></div>
        </div>
        
        <div class="container mx-auto px-4 z-10 text-center">
            <h1 class="font-serif text-[clamp(2.5rem,8vw,5rem)] font-bold text-white leading-tight text-shadow animate-fade-in">
                Sandomierska Winery
            </h1>
            <p class="text-[clamp(1rem,3vw,1.5rem)] text-light mt-6 max-w-3xl mx-auto text-shadow animate-slide-up">
                Crafting exceptional wines in the heart of Poland since 2003
            </p>
            <div class="mt-12 animate-slide-up" style="animation-delay: 0.3s;">
                <a href="#about" class="inline-block bg-secondary hover:bg-secondary/90 text-dark font-medium px-8 py-3 rounded-full transition-all duration-300 transform hover:scale-105 mr-4">
                    EXPLORE OUR WINES
                </a>
                <a href="#visit" class="inline-block bg-transparent border-2 border-light hover:border-secondary text-light hover:text-secondary px-8 py-3 rounded-full transition-all duration-300">
                    PLAN A VISIT
                </a>
            </div>
        </div>
        
        <div class="absolute bottom-10 left-0 right-0 text-center animate-bounce">
            <a href="#about" class="text-light text-3xl">
                <i class="fa fa-angle-down"></i>
            </a>
        </div>
    </section>

    <!-- 关于我们 -->
    <section id="about" class="py-24 bg-dark relative overflow-hidden">
        <div class="container mx-auto px-4">
            <div class="grid md:grid-cols-2 gap-16 items-center">
                <div class="order-2 md:order-1">
                    <h2 class="font-serif text-[clamp(1.8rem,4vw,3rem)] font-bold text-secondary mb-6 wine-glass">About Sandomierska Winery</h2>
                    <p class="text-light/90 mb-6 text-lg">
                        Nestled in the picturesque Sandomierska Uplands of Poland's Lesser Poland Voivodeship, Sandomierska Winery has been producing exceptional wines since 2003. Our 3-hectare vineyard benefits from unique soil and microclimate conditions, allowing us to cultivate grapes that yield wines of remarkable character.
                    </p>
                    <p class="text-light/90 mb-6 text-lg">
                        As a family-owned estate, we are dedicated to preserving traditional winemaking techniques while embracing modern innovations. Our commitment to quality has earned us recognition both locally and internationally.
                    </p>
                    
                    <div class="mt-10">
                        <h3 class="font-serif text-xl text-secondary mb-4">Our Philosophy</h3>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                            <div class="flex items-start">
                                <i class="fa fa-leaf text-secondary text-xl mt-1 mr-3"></i>
                                <div>
                                    <h4 class="font-medium text-light mb-1">Sustainability</h4>
                                    <p class="text-light/80 text-sm">We care for our environment through sustainable farming practices.</p>
                                </div>
                            </div>
                            <div class="flex items-start">
                                <i class="fa fa-history text-secondary text-xl mt-1 mr-3"></i>
                                <div>
                                    <h4 class="font-medium text-light mb-1">Heritage</h4>
                                    <p class="text-light/80 text-sm">Honoring generations of winemaking traditions.</p>
                                </div>
                            </div>
                            <div class="flex items-start">
                                <i class="fa fa-trophy text-secondary text-xl mt-1 mr-3"></i>
                                <div>
                                    <h4 class="font-medium text-light mb-1">Quality</h4>
                                    <p class="text-light/80 text-sm">Every bottle represents our pursuit of excellence.</p>
                                </div>
                            </div>
                            <div class="flex items-start">
                                <i class="fa fa-users text-secondary text-xl mt-1 mr-3"></i>
                                <div>
                                    <h4 class="font-medium text-light mb-1">Community</h4>
                                    <p class="text-light/80 text-sm">Sharing our passion for wine with visitors from around the world.</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="order-1 md:order-2 relative">
                    <img src="https://i.pinimg.com/736x/bd/3f/4b/bd3f4b5160b3f344959e64f6ea73cde0.jpg" alt="Sandomierska Winery" class="w-full h-auto rounded-lg shadow-2xl animate-scale">
                    <div class="absolute -bottom-6 -left-6 bg-wine-red p-4 rounded-lg shadow-lg hidden md:block">
                        <p class="text-secondary font-serif text-xl">Est. 2003</p>
                    </div>
                </div>
            </div>
            
            <!-- 关于庄主 -->
            <div class="mt-24 bg-wine-dark/50 rounded-xl p-8 md:p-12 relative">
                <div class="absolute -top-6 -right-6 md:-right-10 md:-top-10 text-6xl md:text-9xl text-secondary/20 rotate-12">
                    <i class="fa fa-quote-right"></i>
                </div>
                <div class="grid md:grid-cols-3 gap-8 items-center">
                    <div class="md:col-span-2 relative z-10">
                        <h3 class="font-serif text-2xl md:text-3xl text-secondary mb-4">From the Owner: Joanna Małkiewicz</h3>
                        <p class="text-light/90 mb-4 text-lg">
                            "At Sandomierska Winery, we believe that wine is not just a beverage—it's a reflection of our land, our heritage, and our dedication to craftsmanship. Every bottle tells a story of our family's passion for winemaking and our commitment to producing wines that capture the essence of our unique terroir."
                        </p>
                        <p class="text-light/90 mb-6 text-lg">
                            "We invite you to visit our estate, walk through our vineyards, and experience the magic of Polish wine. Whether you're a seasoned connoisseur or just beginning to explore the world of wine, there's something here for everyone."
                        </p>
                        <div class="flex items-center">
                            <img src="https://scontent-bkk1-1.xx.fbcdn.net/v/t39.30808-6/505663550_122104222550898441_4282831206242571131_n.jpg?_nc_cat=111&ccb=1-7&_nc_sid=669761&_nc_ohc=N_BSKF1QVGoQ7kNvwHjdnQj&_nc_oc=AdnAnXJn--c88jj46UlIWPV_NX4cTtXTICoXWffm4pQBJRKbJTdB4HN8YexfvCG2268&_nc_zt=23&_nc_ht=scontent-bkk1-1.xx&_nc_gid=NZqQdQ_TRP0-g15pgy4NFg&oh=00_AfMM0OC5dfMSclM0Rl0oQ-SGXvXdKQL55KDifEtlvO4VHw&oe=685753C6" alt="Joanna Małkiewicz" class="w-16 h-16 rounded-full object-cover mr-4 border-2 border-secondary">
                            <div>
                                <p class="font-medium text-secondary">Joanna Małkiewicz</p>
                                <p class="text-light/70 text-sm">Owner & Winemaker</p>
                            </div>
                        </div>
                    </div>
                    <div class="hidden md:block relative z-10">
                        <img src="https://scontent-bkk1-1.xx.fbcdn.net/v/t39.30808-6/505663550_122104222550898441_4282831206242571131_n.jpg?_nc_cat=111&ccb=1-7&_nc_sid=669761&_nc_ohc=N_BSKF1QVGoQ7kNvwHjdnQj&_nc_oc=AdnAnXJn--c88jj46UlIWPV_NX4cTtXTICoXWffm4pQBJRKbJTdB4HN8YexfvCG2268&_nc_zt=23&_nc_ht=scontent-bkk1-1.xx&_nc_gid=NZqQdQ_TRP0-g15pgy4NFg&oh=00_AfMM0OC5dfMSclM0Rl0oQ-SGXvXdKQL55KDifEtlvO4VHw&oe=685753C6" alt="Joanna Małkiewicz" class="w-full h-auto rounded-lg shadow-lg animate-scale">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 我们的葡萄酒 -->
    <section id="wines" class="py-24 bg-gradient-to-b from-wine-dark to-dark relative">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="font-serif text-[clamp(1.8rem,4vw,3rem)] font-bold text-secondary mb-4 wine-glass">Our Wines</h2>
                <p class="text-light/90 max-w-2xl mx-auto text-lg">
                    Discover our carefully crafted selection of wines, each expressing the unique character of our Sandomierska Uplands terroir.
                </p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- 红酒 -->
                <div class="bg-wine-dark/30 rounded-lg overflow-hidden shadow-lg transition-all duration-300 hover:shadow-xl group">
                    <div class="relative overflow-hidden h-64">
                        <img src="https://i.pinimg.com/736x/f0/0c/ad/f00cada57eb62c8fdc16227a9400974a.jpg" alt="Red Wine Collection" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                        <div class="absolute inset-0 bg-gradient-to-t from-wine-dark to-transparent"></div>
                        <div class="absolute bottom-4 left-4">
                            <span class="bg-primary text-white text-xs px-3 py-1 rounded-full">RED WINES</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="font-serif text-xl text-secondary mb-2">Red Collection</h3>
                        <p class="text-light/80 mb-4">
                            Bold, complex, and elegant, our red wines showcase the best of Polish terroir with rich fruit flavors and smooth tannins.
                        </p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="text-secondary font-medium">From €28</span>
                            </div>
                            <a href="#" class="text-secondary hover:text-light transition-colors duration-300">
                                <span>VIEW COLLECTION</span>
                                <i class="fa fa-arrow-right ml-2"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- 白葡萄酒 -->
                <div class="bg-wine-dark/30 rounded-lg overflow-hidden shadow-lg transition-all duration-300 hover:shadow-xl group">
                    <div class="relative overflow-hidden h-64">
                        <img src="https://i.pinimg.com/736x/c2/0b/92/c20b926f3aa46e427f35e98caa8a740e.jpg" alt="White Wine Collection" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                        <div class="absolute inset-0 bg-gradient-to-t from-wine-dark to-transparent"></div>
                        <div class="absolute bottom-4 left-4">
                            <span class="bg-secondary text-dark text-xs px-3 py-1 rounded-full">WHITE WINES</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="font-serif text-xl text-secondary mb-2">White Collection</h3>
                        <p class="text-light/80 mb-4">
                            Crisp, refreshing, and aromatic, our white wines offer a perfect balance of acidity and fruitiness.
                        </p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="text-secondary font-medium">From €24</span>
                            </div>
                            <a href="#" class="text-secondary hover:text-light transition-colors duration-300">
                                <span>VIEW COLLECTION</span>
                                <i class="fa fa-arrow-right ml-2"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- 桃红葡萄酒 -->
                <div class="bg-wine-dark/30 rounded-lg overflow-hidden shadow-lg transition-all duration-300 hover:shadow-xl group">
                    <div class="relative overflow-hidden h-64">
                        <img src="https://i.pinimg.com/736x/bd/3f/4b/bd3f4b5160b3f344959e64f6ea73cde0.jpg" alt="Rosé Wine Collection" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                        <div class="absolute inset-0 bg-gradient-to-t from-wine-dark to-transparent"></div>
                        <div class="absolute bottom-4 left-4">
                            <span class="bg-wine-light text-wine-dark text-xs px-3 py-1 rounded-full">ROSÉ WINES</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="font-serif text-xl text-secondary mb-2">Rosé Collection</h3>
                        <p class="text-light/80 mb-4">
                            Elegant and vibrant, our rosé wines offer delicate flavors and a beautiful pink hue, perfect for any occasion.
                        </p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="text-secondary font-medium">From €22</span>
                            </div>
                            <a href="#" class="text-secondary hover:text-light transition-colors duration-300">
                                <span>VIEW COLLECTION</span>
                                <i class="fa fa-arrow-right ml-2"></i>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- 精选葡萄酒 -->
            <div class="mt-16 bg-wine-dark/50 rounded-xl p-8 md:p-12">
                <h3 class="font-serif text-2xl md:text-3xl text-secondary mb-8 text-center">Featured Wines</h3>
                
                <div class="grid md:grid-cols-2 gap-8 items-center">
                    <div class="flex flex-col md:flex-row gap-6">
                        <img src="https://i.pinimg.com/736x/ad/05/c9/ad05c9f39966038d98d23cb29d65519a.jpg" alt="Red Navy Wine" class="w-48 h-auto rounded-lg shadow-lg animate-scale">
                        <div>
                            <h4 class="font-serif text-xl text-secondary mb-2">Red Navy</h4>
                            <p class="text-light/70 text-sm mb-2">Cabernet Sauvignon, Merlot, Pinot Noir Blend</p>
                            <div class="flex items-center mb-4">
                                <div class="text-secondary">
                                    <i class="fa fa-star"></i>
                                    <i class="fa fa-star"></i>
                                    <i class="fa fa-star"></i>
                                    <i class="fa fa-star"></i>
                                    <i class="fa fa-star-half-o"></i>
                                </div>
                                <span class="text-light/70 text-sm ml-2">4.5/5 (128 reviews)</span>
                            </div>
                            <p class="text-light/90 mb-4">
                                A bold and complex red wine with notes of dark fruit, spices, and a hint of oak. Perfect for pairing with grilled meats and hearty dishes.
                            </p>
                            <div class="flex items-center justify-between">
                                <span class="text-secondary font-serif text-xl">€38</span>
                                <a href="#" class="bg-primary hover:bg-wine-red text-white px-6 py-2 rounded-full transition-all duration-300 transform hover:scale-105">
                                    BUY NOW
                                </a>
                            </div>
                        </div>
                    </div>
                    
                    <div class="flex flex-col md:flex-row gap-6">
                        <img src="https://i.pinimg.com/736x/12/51/94/1251942405dea17464a5b981fd563b91.jpg" alt="Platinum Wine" class="w-48 h-auto rounded-lg shadow-lg animate-scale">
                        <div>
                            <h4 class="font-serif text-xl text-secondary mb-2">Platinum</h4>
                            <p class="text-light/70 text-sm mb-2">Chardonnay, Riesling Blend</p>
                            <div class="flex items-center mb-4">
                                <div class="text-secondary">
                                    <i class="fa fa-star"></i>
                                    <i class="fa fa-star"></i>
                                    <i class="fa fa-star"></i>
                                    <i class="fa fa-star"></i>
                                    <i class="fa fa-star"></i>
                                </div>
                                <span class="text-light/70 text-sm ml-2">5/5 (96 reviews)</span>
                            </div>
                            <p class="text-light/90 mb-4">
                                A crisp and elegant white wine with citrus and tropical fruit flavors, balanced by a subtle minerality. Ideal as an aperitif or with seafood.
                            </p>
                            <div class="flex items-center justify-between">
                                <span class="text-secondary font-serif text-xl">€34</span>
                                <a href="#" class="bg-primary hover:bg-wine-red text-white px-6 py-2 rounded-full transition-all duration-300 transform hover:scale-105">
                                    BUY NOW
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 生产流程 -->
    <section id="production" class="py-24 bg-dark relative">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="font-serif text-[clamp(1.8rem,4vw,3rem)] font-bold text-secondary mb-4 wine-glass">Our Production Process</h2>
                <p class="text-light/90 max-w-2xl mx-auto text-lg">
                    Discover the meticulous process behind every bottle of Sandomierska Winery wine, from vine to glass.
                </p>
            </div>
            
            <div class="relative">
                <!-- 流程时间线 -->
                <div class="hidden md:block absolute left-1/2 transform -translate-x-1/2 h-full w-1 bg-secondary/20 top-0"></div>
                
                <div class="space-y-16 relative">
                    <!-- 种植 -->
                    <div class="flex flex-col md:flex-row items-center">
                        <div class="md:w-1/2 md:pr-12 md:text-right order-2 md:order-1 mt-8 md:mt-0">
                            <h3 class="font-serif text-2xl text-secondary mb-4">Cultivation</h3>
                            <p class="text-light/90">
                                Our vineyards are carefully tended throughout the growing season, with sustainable practices that respect the environment and enhance the natural character of our grapes.
                            </p>
                            <div class="mt-4 hidden md:block">
                                <span class="inline-block bg-secondary text-dark px-4 py-1 rounded-full text-sm font-medium">1</span>
                            </div>
                        </div>
                        
                        <div class="md:w-1/2 order-1 md:order-2">
                            <img src="https://i.pinimg.com/736x/aa/11/72/aa1172b7dffbcf70f558b230f15044cb.jpg" alt="Vineyard Cultivation" class="w-full h-auto rounded-lg shadow-xl animate-scale">
                        </div>
                    </div>
                    
                    <!-- 采摘 -->
                    <div class="flex flex-col md:flex-row items-center">
                        <div class="md:w-1/2 md:pl-12 order-1">
                            <h3 class="font-serif text-2xl text-secondary mb-4">Harvest</h3>
                            <p class="text-light/90">
                                Grapes are handpicked at optimal ripeness to ensure the highest quality fruit. Each cluster is carefully selected and sorted before processing.
                            </p>
                            <div class="mt-4 hidden md:block">
                                <span class="inline-block bg-secondary text-dark px-4 py-1 rounded-full text-sm font-medium">2</span>
                            </div>
                        </div>
                        
                        <div class="md:w-1/2 md:pr-12 order-2">
                            <img src="https://i.pinimg.com/736x/4f/d0/d9/4fd0d92454051bd0db986bd7ba4bd3b4.jpg" alt="Grape Harvest" class="w-full h-auto rounded-lg shadow-xl animate-scale">
                        </div>
                    </div>
                    
                    <!-- 发酵 -->
                    <div class="flex flex-col md:flex-row items-center">
                        <div class="md:w-1/2 md:pr-12 md:text-right order-2 md:order-1 mt-8 md:mt-0">
                            <h3 class="font-serif text-2xl text-secondary mb-4">Fermentation</h3>
                            <p class="text-light/90">
                                Using traditional methods combined with modern techniques, our winemakers carefully monitor the fermentation process to develop the unique character of each wine.
                            </p>
                            <div class="mt-4 hidden md:block">
                                <span class="inline-block bg-secondary text-dark px-4 py-1 rounded-full text-sm font-medium">3</span>
                            </div>
                        </div>
                        
                        <div class="md:w-1/2 order-1 md:order-2">
                            <img src="https://i.pinimg.com/736x/4d/38/87/4d388760b96863000633f9293e379483.jpg" alt="Wine Fermentation" class="w-full h-auto rounded-lg shadow-xl animate-scale">
                        </div>
                    </div>
                    
                    <!-- 陈酿 -->
                    <div class="flex flex-col md:flex-row items-center">
                        <div class="md:w-1/2 md:pl-12 order-1">
                            <h3 class="font-serif text-2xl text-secondary mb-4">Aging</h3>
                            <p class="text-light/90">
                                Our wines are aged in oak barrels or stainless steel tanks, depending on the varietal and style, to develop complexity, depth, and balance.
                            </p>
                            <div class="mt-4 hidden md:block">
                                <span class="inline-block bg-secondary text-dark px-4 py-1 rounded-full text-sm font-medium">4</span>
                            </div>
                        </div>
                        
                        <div class="md:w-1/2 md:pr-12 order-2">
                            <img src="https://i.pinimg.com/736x/f9/9f/88/f99f881434554e4eee525cc530527f65.jpg" alt="Wine Aging" class="w-full h-auto rounded-lg shadow-xl animate-scale">
                        </div>
                    </div>
                    
                    <!-- 装瓶 -->
                    <div class="flex flex-col md:flex-row items-center">
                        <div class="md:w-1/2 md:pr-12 md:text-right order-2 md:order-1 mt-8 md:mt-0">
                            <h3 class="font-serif text-2xl text-secondary mb-4">Bottling</h3>
                            <p class="text-light/90">
                                After careful evaluation, our wines are bottled and labeled by hand, ensuring attention to detail and quality in every step of the process.
                            </p>
                            <div class="mt-4 hidden md:block">
                                <span class="inline-block bg-secondary text-dark px-4 py-1 rounded-full text-sm font-medium">5</span>
                            </div>
                        </div>
                        
                        <div class="md:w-1/2 order-1 md:order-2">
                            <img src="https://i.pinimg.com/736x/a7/af/98/a7af9859e7fb298877e2bc03de9a5d71.jpg" alt="Wine Bottling" class="w-full h-auto rounded-lg shadow-xl animate-scale">
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- 我们的团队 -->
            <div class="mt-24">
                <h3 class="font-serif text-2xl md:text-3xl text-secondary mb-8 text-center">Our Expert Team</h3>
                
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                    <div class="bg-wine-dark/30 rounded-lg overflow-hidden shadow-lg transition-all duration-300 hover:shadow-xl group">
                        <div class="relative overflow-hidden">
                            <img src="https://scontent-bkk1-1.xx.fbcdn.net/v/t39.30808-6/496920199_1241063188024993_3181908893052598450_n.jpg?stp=cp6_dst-jpg_tt6&_nc_cat=110&ccb=1-7&_nc_sid=833d8c&_nc_ohc=wfOuXC8_RrQQ7kNvwHR1ctL&_nc_oc=AdlDdK-aN4PuoJbsFiMlXwYtkUztlF2dg0jXXhvRIMZj8kRbmrMn2I7tgn2J0NsQ9Lo&_nc_zt=23&_nc_ht=scontent-bkk1-1.xx&_nc_gid=C7S-jFPu4RP-7sTSpp93lA&oh=00_AfOiix0IoFx2dIMMVB-TXybE4olfcYRzvkUJbA6WqxvoEA&oe=6857E288" alt="Head Winemaker" class="w-full h-80 object-cover transition-transform duration-700 group-hover:scale-110">
                            <div class="absolute inset-0 bg-gradient-to-t from-wine-dark via-wine-dark/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end">
                                <div class="p-6">
                                    <div class="flex space-x-3">
                                        <a href="#" class="bg-secondary/80 hover:bg-secondary text-dark w-8 h-8 rounded-full flex items-center justify-center transition-colors duration-300">
                                            <i class="fa fa-facebook"></i>
                                        </a>
                                        <a href="#" class="bg-secondary/80 hover:bg-secondary text-dark w-8 h-8 rounded-full flex items-center justify-center transition-colors duration-300">
                                            <i class="fa fa-instagram"></i>
                                        </a>
                                        <a href="#" class="bg-secondary/80 hover:bg-secondary text-dark w-8 h-8 rounded-full flex items-center justify-center transition-colors duration-300">
                                            <i class="fa fa-linkedin"></i>
                                        </a>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="p-6">
                            <h4 class="font-serif text-xl text-secondary mb-1">MARCELI Małkiewicz</h4>
                            <p class="text-light/70 text-sm mb-3">Head Winemaker</p>
                            <p class="text-light/80 text-sm">
                                With over 20 years of experience in premium winemaking, MARCELI oversees our entire production process with meticulous attention to detail.
                            </p>
                        </div>
                    </div>
                    
                    <div class="bg-wine-dark/30 rounded-lg overflow-hidden shadow-lg transition-all duration-300 hover:shadow-xl group">
                        <div class="relative overflow-hidden">
                            <img src="https://scontent-bkk1-1.xx.fbcdn.net/v/t39.30808-6/480828782_1168756628588983_7934557246441585883_n.jpg?_nc_cat=106&ccb=1-7&_nc_sid=127cfc&_nc_ohc=hXA0Mmtxj04Q7kNvwH6ZDad&_nc_oc=AdnMJwYz_GixlntNkmLO-GsU1IERQ26i30DPkjUaGLVqgUCOSHYgNbDd_Dc3MZ7yKGg&_nc_zt=23&_nc_ht=scontent-bkk1-1.xx&_nc_gid=vC4fstXktS60Wp2wKYhGbw&oh=00_AfOBrrMLO5KWY4EISqkbsdroLGd5kWNc32ZZydwkeQivDw&oe=6858CB93" alt="Vineyard Manager" class="w-full h-80 object-cover transition-transform duration-700 group-hover:scale-110">
                            <div class="absolute inset-0 bg-gradient-to-t from-wine-dark via-wine-dark/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end">
                                <div class="p-6">
                                    <div class="flex space-x-3">
                                        <a href="#" class="bg-secondary/80 hover:bg-secondary text-dark w-8 h-8 rounded-full flex items-center justify-center transition-colors duration-300">
                                            <i class="fa fa-facebook"></i>
                                        </a>
                                        <a href="#" class="bg-secondary/80 hover:bg-secondary text-dark w-8 h-8 rounded-full flex items-center justify-center transition-colors duration-300">
                                            <i class="fa fa-instagram"></i>
                                        </a>
                                        <a href="#" class="bg-secondary/80 hover:bg-secondary text-dark w-8 h-8 rounded-full flex items-center justify-center transition-colors duration-300">
                                            <i class="fa fa-linkedin"></i>
                                        </a>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="p-6">
                            <h4 class="font-serif text-xl text-secondary mb-1">Monika Małkiewicz</h4>
                            <p class="text-light/70 text-sm mb-3">Vineyard Manager</p>
                            <p class="text-light/80 text-sm">
                                Monika ensures our vines receive the perfect care, from pruning to harvest, creating optimal conditions for exceptional grapes.
                            </p>
                        </div>
                    </div>
                    
                    <div class="bg-wine-dark/30 rounded-lg overflow-hidden shadow-lg transition-all duration-300 hover:shadow-xl group">
                        <div class="relative overflow-hidden">
                            <img src="https://scontent-bkk1-2.cdninstagram.com/v/t39.30808-6/440156153_18433178212034056_8780449331130252319_n.jpg?stp=dst-jpg_e35_p480x480_tt6&efg=eyJ2ZW5jb2RlX3RhZyI6IkZFRUQuaW1hZ2VfdXJsZ2VuLjE0NDB4MTgwMC5zZHIuZjMwODA4LmRlZmF1bHRfaW1hZ2UifQ&_nc_ht=scontent-bkk1-2.cdninstagram.com&_nc_cat=104&_nc_oc=Q6cZ2QG2fHaXN5jdcyUn8JwNYS2ushBOi4FWuyrWUw2M9TLpS30A7ui5ivUIScfuyHw5VPE&_nc_ohc=C3gbM1z1S5YQ7kNvwGYJXXB&_nc_gid=a0wr4aE0b_yk5gY1gj5pYw&edm=AFlAz-oAAAAA&ccb=7-5&ig_cache_key=MzM2MDc4NDIyNDYwMjU5NzU4MA%3D%3D.3-ccb7-5&oh=00_AfOQYn7KOm8Y2ixcpfWu2a9JrIt-7CZMpF64VwgmVALliw&oe=6857AE1F&_nc_sid=76c0fc" alt="Cellar Master" class="w-full h-80 object-cover transition-transform duration-700 group-hover:scale-110">
                            <div class="absolute inset-0 bg-gradient-to-t from-wine-dark via-wine-dark/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end">
                                <div class="p-6">
                                    <div class="flex space-x-3">
                                        <a href="#" class="bg-secondary/80 hover:bg-secondary text-dark w-8 h-8 rounded-full flex items-center justify-center transition-colors duration-300">
                                            <i class="fa fa-facebook"></i>
                                        </a>
                                        <a href="#" class="bg-secondary/80 hover:bg-secondary text-dark w-8 h-8 rounded-full flex items-center justify-center transition-colors duration-300">
                                            <i class="fa fa-instagram"></i>
                                        </a>
                                        <a href="#" class="bg-secondary/80 hover:bg-secondary text-dark w-8 h-8 rounded-full flex items-center justify-center transition-colors duration-300">
                                            <i class="fa fa-linkedin"></i>
                                        </a>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="p-6">
                            <h4 class="font-serif text-xl text-secondary mb-1">Tomasz Wiśniewski</h4>
                            <p class="text-light/70 text-sm mb-3">Cellar Master</p>
                            <p class="text-light/80 text-sm">
                                Tomasz manages our aging process with precision, ensuring each wine develops its full potential before bottling.
                            </p>
                        </div>
                    </div>
                    
                    <div class="bg-wine-dark/30 rounded-lg overflow-hidden shadow-lg transition-all duration-300 hover:shadow-xl group">
                        <div class="relative overflow-hidden">
                            <img src="https://scontent-bkk1-1.xx.fbcdn.net/v/t39.30808-6/481156302_122100352760790641_7924110047008608052_n.jpg?_nc_cat=111&ccb=1-7&_nc_sid=6ee11a&_nc_ohc=g8-K_P1zkAUQ7kNvwFicA1p&_nc_oc=AdnEcR5fbdtKnyTIs8Gt21GHyiRLt6raYealyhAcP-Y-dP-Y6J-qf-TjfglMad5KjCE&_nc_zt=23&_nc_ht=scontent-bkk1-1.xx&_nc_gid=U5_kMfwIyedm5biT_srfFw&oh=00_AfMsU8NZf0wwouwmzLVozh0pMiDsVYImxsCuu8F-3zqHag&oe=6858CDDB" alt="Wine Educator" class="w-full h-80 object-cover transition-transform duration-700 group-hover:scale-110">
                            <div class="absolute inset-0 bg-gradient-to-t from-wine-dark via-wine-dark/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end">
                                <div class="p-6">
                                    <div class="flex space-x-3">
                                        <a href="#" class="bg-secondary/80 hover:bg-secondary text-dark w-8 h-8 rounded-full flex items-center justify-center transition-colors duration-300">
                                            <i class="fa fa-facebook"></i>
                                        </a>
                                        <a href="#" class="bg-secondary/80 hover:bg-secondary text-dark w-8 h-8 rounded-full flex items-center justify-center transition-colors duration-300">
                                            <i class="fa fa-instagram"></i>
                                        </a>
                                        <a href="#" class="bg-secondary/80 hover:bg-secondary text-dark w-8 h-8 rounded-full flex items-center justify-center transition-colors duration-300">
                                            <i class="fa fa-linkedin"></i>
                                        </a>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="p-6">
                            <h4 class="font-serif text-xl text-secondary mb-1">Anna Hare</h4>
                            <p class="text-light/70 text-sm mb-3">Wine Educator</p>
                            <p class="text-light/80 text-sm">
                                Anna leads our tasting experiences, sharing her extensive knowledge of wine with visitors from around the world.
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 体验活动 -->
    <section id="experiences" class="py-24 bg-gradient-to-b from-wine-dark to-dark relative">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="font-serif text-[clamp(1.8rem,4vw,3rem)] font-bold text-secondary mb-4 wine-glass">Wine Experiences</h2>
                <p class="text-light/90 max-w-2xl mx-auto text-lg">
                    Immerse yourself in the world of Sandomierska Winery with our curated experiences.
                </p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- 品鉴体验 -->
                <div class="bg-wine-dark/30 rounded-lg overflow-hidden shadow-lg transition-all duration-300 hover:shadow-xl group">
                    <div class="relative overflow-hidden h-64">
                        <img src="https://i.pinimg.com/736x/ef/79/27/ef792736e8e9c6320894f4431804494a.jpg" alt="Wine Tasting Experience" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                        <div class="absolute inset-0 bg-gradient-to-t from-wine-dark to-transparent"></div>
                        <div class="absolute bottom-4 left-4">
                            <span class="bg-secondary text-dark text-xs px-3 py-1 rounded-full">TASTING</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="font-serif text-xl text-secondary mb-2">Wine Tasting Experience</h3>
                        <p class="text-light/80 mb-4">
                            Discover the nuances of our wines with a guided tasting led by our expert sommelier. Includes 5 premium wines and artisanal cheese pairing.
                        </p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="text-secondary font-medium">€95 per person</span>
                            </div>
                            <a href="#" class="text-secondary hover:text-light transition-colors duration-300">
                                <span>BOOK NOW</span>
                                <i class="fa fa-arrow-right ml-2"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- 酒庄参观 -->
                <div class="bg-wine-dark/30 rounded-lg overflow-hidden shadow-lg transition-all duration-300 hover:shadow-xl group">
                    <div class="relative overflow-hidden h-64">
                        <img src="https://i.pinimg.com/736x/47/aa/a1/47aaa1a39346527303d9230dff8adf0b.jpg" alt="Winery Tour" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                        <div class="absolute inset-0 bg-gradient-to-t from-wine-dark to-transparent"></div>
                        <div class="absolute bottom-4 left-4">
                            <span class="bg-secondary text-dark text-xs px-3 py-1 rounded-full">TOUR</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="font-serif text-xl text-secondary mb-2">Vineyard & Winery Tour</h3>
                        <p class="text-light/80 mb-4">
                            Explore our vineyards and winemaking facilities with a knowledgeable guide. Includes a tasting of 4 wines and a visit to our historic cellars.
                        </p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="text-secondary font-medium">€105 per person</span>
                            </div>
                            <a href="#" class="text-secondary hover:text-light transition-colors duration-300">
                                <span>BOOK NOW</span>
                                <i class="fa fa-arrow-right ml-2"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- 美食与葡萄酒搭配 -->
                <div class="bg-wine-dark/30 rounded-lg overflow-hidden shadow-lg transition-all duration-300 hover:shadow-xl group">
                    <div class="relative overflow-hidden h-64">
                        <img src="https://scontent-bkk1-2.xx.fbcdn.net/v/t39.30808-6/494765220_1187631329830365_8513257298103366792_n.jpg?_nc_cat=107&ccb=1-7&_nc_sid=127cfc&_nc_ohc=yeJCy1hWBaAQ7kNvwHXd7kA&_nc_oc=Adl0fTUhMNUJUPwHjfQi0qC8NHbRiz9kJgJSJSxRtRRVfT4umc7C_VdfklmizrLnKeQ&_nc_zt=23&_nc_ht=scontent-bkk1-2.xx&_nc_gid=6m8yUlil0ECWN4wZhjanTw&oh=00_AfNNB9qz-D7m-rHrHCQTKnPYVc_U_c1f7LU5IxjiMvnw3g&oe=6858C314" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                        <div class="absolute inset-0 bg-gradient-to-t from-wine-dark to-transparent"></div>
                        <div class="absolute bottom-4 left-4">
                            <span class="bg-secondary text-dark text-xs px-3 py-1 rounded-full">DINING</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="font-serif text-xl text-secondary mb-2">Wine & Dine Experience</h3>
                        <p class="text-light/80 mb-4">
                            Enjoy a 5-course gourmet meal paired with our finest wines, prepared by our award-winning chef using local ingredients.
                        </p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="text-secondary font-medium">€85 per person</span>
                            </div>
                            <a href="#" class="text-secondary hover:text-light transition-colors duration-300">
                                <span>BOOK NOW</span>
                                <i class="fa fa-arrow-right ml-2"></i>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- 住宿体验 -->
            <div class="mt-16 bg-wine-dark/50 rounded-xl p-8 md:p-12">
                <div class="grid md:grid-cols-2 gap-8 items-center">
                    <div>
                        <h3 class="font-serif text-2xl md:text-3xl text-secondary mb-4">Stay with Us</h3>
                        <p class="text-light/90 mb-6 text-lg">
                            Extend your wine experience with a stay in our charming guesthouse. Our beautifully appointed rooms offer a peaceful retreat after a day of wine exploration. Each morning, enjoy a delicious breakfast featuring local specialties and our own wines.
                        </p>
                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 mb-6">
                            <div class="flex items-start">
                                <i class="fa fa-check-circle text-secondary text-xl mt-1 mr-3"></i>
                                <div>
                                    <h4 class="font-medium text-light mb-1">Luxurious Accommodations</h4>
                                    <p class="text-light/80 text-sm">Comfortable rooms with premium amenities</p>
                                </div>
                            </div>
                            <div class="flex items-start">
                                <i class="fa fa-check-circle text-secondary text-xl mt-1 mr-3"></i>
                                <div>
                                    <h4 class="font-medium text-light mb-1">Scenic Views</h4>
                                    <p class="text-light/80 text-sm">Overlooking the vineyards and countryside</p>
                                </div>
                            </div>
                            <div class="flex items-start">
                                <i class="fa fa-check-circle text-secondary text-xl mt-1 mr-3"></i>
                                <div>
                                    <h4 class="font-medium text-light mb-1">Gourmet Breakfast</h4>
                                    <p class="text-light/80 text-sm">Included with your stay</p>
                                </div>
                            </div>
                            <div class="flex items-start">
                                <i class="fa fa-check-circle text-secondary text-xl mt-1 mr-3"></i>
                                <div>
                                    <h4 class="font-medium text-light mb-1">Exclusive Access</h4>
                                    <p class="text-light/80 text-sm">To vineyard tours and private tastings</p>
                                </div>
                            </div>
                        </div>
                        <a href="#" class="inline-block bg-secondary hover:bg-secondary/90 text-dark font-medium px-8 py-3 rounded-full transition-all duration-300 transform hover:scale-105">
                            BOOK YOUR STAY
                        </a>
                    </div>
                    <div class="grid grid-cols-2 gap-4">
                        <img src="https://i.pinimg.com/736x/a0/6e/35/a06e35c889e77d7a09a8d125eb32f222.jpg" alt="Winery Guesthouse Room" class="w-full h-64 object-cover rounded-lg shadow-lg animate-scale">
                        <img src="https://i.pinimg.com/736x/b4/05/2c/b4052c4a2189576c131965c014b33c71.jpg" alt="Winery Guesthouse Exterior" class="w-full h-64 object-cover rounded-lg shadow-lg animate-scale mt-8">
                        <img src="https://i.pinimg.com/736x/9b/90/98/9b9098938262ea3f70c5616404c960d9.jpg" alt="Winery Guesthouse Dining" class="w-full h-64 object-cover rounded-lg shadow-lg animate-scale">
                        <img src="https://i.pinimg.com/736x/08/c6/4b/08c64bd2568297043146f08cd7d51a58.jpg" alt="Winery Guesthouse Garden" class="w-full h-64 object-cover rounded-lg shadow-lg animate-scale mt-8">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 客户评价 -->
    <section class="py-24 bg-dark relative">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="font-serif text-[clamp(1.8rem,4vw,3rem)] font-bold text-secondary mb-4 wine-glass">What Our Guests Say</h2>
                <p class="text-light/90 max-w-2xl mx-auto text-lg">
                    Discover why visitors from around the world rave about their experience at Sandomierska Winery.
                </p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- 评价 1 -->
                <div class="bg-wine-dark/30 rounded-lg p-8 shadow-lg relative">
                    <div class="absolute -top-6 -right-6 text-4xl text-secondary/20">
                        <i class="fa fa-quote-right"></i>
                    </div>
                    <div class="text-secondary mb-4">
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star"></i>
                    </div>
                    <p class="text-light/90 mb-6 relative z-10">
                        "An absolutely magical experience! The vineyard tour was informative and our guide was passionate about the wines. The tasting was exceptional, with each wine perfectly balanced and full of character. The cheese pairing was a delightful surprise. Can't wait to return!"
                    </p>
                    <div class="flex items-center">
                        <img src="https://picsum.photos/id/1027/100/100" alt="Guest" class="w-12 h-12 rounded-full object-cover mr-4">
                        <div>
                            <p class="font-medium text-light">Emily Johnson</p>
                            <p class="text-light/70 text-sm">Visited from United Kingdom</p>
                        </div>
                    </div>
                </div>
                
                <!-- 评价 2 -->
                <div class="bg-wine-dark/30 rounded-lg p-8 shadow-lg relative">
                    <div class="absolute -top-6 -right-6 text-4xl text-secondary/20">
                        <i class="fa fa-quote-right"></i>
                    </div>
                    <div class="text-secondary mb-4">
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star"></i>
                    </div>
                    <p class="text-light/90 mb-6 relative z-10">
                        "The Wine & Dine experience was extraordinary. The chef perfectly paired each course with a different wine from the estate, highlighting the versatility of their offerings. The accommodations were luxurious and the views of the vineyards at sunrise were breathtaking."
                    </p>
                    <div class="flex items-center">
                        <img src="https://picsum.photos/id/1012/100/100" alt="Guest" class="w-12 h-12 rounded-full object-cover mr-4">
                        <div>
                            <p class="font-medium text-light">Michael Thompson</p>
                            <p class="text-light/70 text-sm">Visited from United States</p>
                        </div>
                    </div>
                </div>
                
                <!-- 评价 3 -->
                <div class="bg-wine-dark/30 rounded-lg p-8 shadow-lg relative">
                    <div class="absolute -top-6 -right-6 text-4xl text-secondary/20">
                        <i class="fa fa-quote-right"></i>
                    </div>
                    <div class="text-secondary mb-4">
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star-half-o"></i>
                    </div>
                    <p class="text-light/90 mb-6 relative z-10">
                        "As a wine enthusiast, I've visited many wineries around the world, but Sandomierska Winery stands out. The attention to detail in their winemaking process is evident in every bottle. The Red Navy was particularly impressive - rich, complex, and perfectly balanced."
                    </p>
                    <div class="flex items-center">
                        <img src="https://picsum.photos/id/1000/100/100" alt="Guest" class="w-12 h-12 rounded-full object-cover mr-4">
                        <div>
                            <p class="font-medium text-light">Sophie Dubois</p>
                            <p class="text-light/70 text-sm">Visited from France</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 联系我们 -->
    <section id="contact" class="py-24 bg-gradient-to-b from-wine-dark to-dark relative">
        <div class="container mx-auto px-4">
            <div class="grid md:grid-cols-2 gap-16 items-center">
                <div>
                    <h2 class="font-serif text-[clamp(1.8rem,4vw,3rem)] font-bold text-secondary mb-6 wine-glass">Contact Us</h2>
                    <p class="text-light/90 mb-8 text-lg">
                        We'd love to hear from you! Whether you have questions about our wines, want to book a tour, or just want to say hello, we're here to assist you.
                    </p>
                    
                    <div class="space-y-6">
                        <div class="flex items-start">
                            <div class="bg-secondary/20 p-3 rounded-full mr-4">
                                <i class="fa fa-map-marker text-secondary text-xl"></i>
                            </div>
                            <div>
                                <h3 class="font-medium text-secondary mb-1">Location</h3>
                                <p class="text-light/90">
                                    Sandomierska Uplands, Lesser Poland Voivodeship<br>
                                    Approximately 8 km from the city center
                                </p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="bg-secondary/20 p-3 rounded-full mr-4">
                                <i class="fa fa-envelope text-secondary text-xl"></i>
                            </div>
                            <div>
                                <h3 class="font-medium text-secondary mb-1">Email</h3>
                                <p class="text-light/90">
                                    anjialaaoliao@gmail.com
                                </p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="bg-secondary/20 p-3 rounded-full mr-4">
                                <i class="fa fa-phone text-secondary text-xl"></i>
                            </div>
                            <div>
                                <h3 class="font-medium text-secondary mb-1">Phone</h3>
                                <p class="text-light/90">
                                    +15127367017 (IG & WhatsApp)
                                </p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="bg-secondary/20 p-3 rounded-full mr-4">
                                <i class="fa fa-clock-o text-secondary text-xl"></i>
                            </div>
                            <div>
                                <h3 class="font-medium text-secondary mb-1">Opening Hours</h3>
                                <p class="text-light/90">
                                    Monday - Friday: 10:00 AM - 7:00 PM<br>
                                    Saturday - Sunday: 10:00 AM - 8:00 PM
                                </p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="mt-10">
                        <h3 class="font-serif text-xl text-secondary mb-4">Follow Us</h3>
                        <div class="flex space-x-4">
                            <a href="https://www.facebook.com/profile.php?id=61576953242752" target="_blank" class="bg-wine-dark hover:bg-wine-red text-light w-10 h-10 rounded-full flex items-center justify-center transition-colors duration-300">
                                <i class="fa fa-facebook"></i>
                            </a>
                            <a href="#" target="_blank" class="bg-wine-dark hover:bg-wine-red text-light w-10 h-10 rounded-full flex items-center justify-center transition-colors duration-300">
                                <i class="fa fa-instagram"></i>
                            </a>
                            <a href="#" target="_blank" class="bg-wine-dark hover:bg-wine-red text-light w-10 h-10 rounded-full flex items-center justify-center transition-colors duration-300">
                                <i class="fa fa-twitter"></i>
                            </a>
                            <a href="#" target="_blank" class="bg-wine-dark hover:bg-wine-red text-light w-10 h-10 rounded-full flex items-center justify-center transition-colors duration-300">
                                <i class="fa fa-pinterest"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <div>
                    <div class="bg-wine-dark/50 rounded-xl p-8 shadow-xl">
                        <h3 class="font-serif text-2xl text-secondary mb-6">Send Us a Message</h3>
                        <form>
                            <div class="grid md:grid-cols-2 gap-6 mb-6">
                                <div>
                                    <label for="name" class="block text-light/80 mb-2 text-sm">Your Name</label>
                                    <input type="text" id="name" class="w-full bg-wine-dark border border-secondary/30 rounded-lg px-4 py-3 text-light focus:outline-none focus:border-secondary transition-colors duration-300" placeholder="Enter your name">
                                </div>
                                <div>
                                    <label for="email" class="block text-light/80 mb-2 text-sm">Email Address</label>
                                    <input type="email" id="email" class="w-full bg-wine-dark border border-secondary/30 rounded-lg px-4 py-3 text-light focus:outline-none focus:border-secondary transition-colors duration-300" placeholder="Enter your email">
                                </div>
                            </div>
                            
                            <div class="mb-6">
                                <label for="subject" class="block text-light/80 mb-2 text-sm">Subject</label>
                                <input type="text" id="subject" class="w-full bg-wine-dark border border-secondary/30 rounded-lg px-4 py-3 text-light focus:outline-none focus:border-secondary transition-colors duration-300" placeholder="Enter subject">
                            </div>
                            
                            <div class="mb-6">
                                <label for="message" class="block text-light/80 mb-2 text-sm">Your Message</label>
                                <textarea id="message" rows="5" class="w-full bg-wine-dark border border-secondary/30 rounded-lg px-4 py-3 text-light focus:outline-none focus:border-secondary transition-colors duration-300" placeholder="Enter your message"></textarea>
                            </div>
                            
                            <button type="submit" class="w-full bg-primary hover:bg-wine-red text-white font-medium py-3 rounded-lg transition-all duration-300 transform hover:scale-105">
                                SEND MESSAGE
                            </button>
                        </form>
