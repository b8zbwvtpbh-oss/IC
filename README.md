<!DOCTYPE html>
<html lang="ar" dir="rtl" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>موقف الشريعة الإسلامية من الانحراف الفكري</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts: Cairo & Amiri -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Amiri:ital,wght@0,400;0,700;1,400&family=Cairo:wght@300;400;600;700;800;900&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        navy: {
                            50: '#f0f3f9',
                            100: '#e1e7f2',
                            200: '#c7d3e6',
                            700: '#2c3e5a',
                            800: '#1e293b',
                            900: '#0f172a',
                            950: '#0a0f1d',
                        },
                        gold: {
                            400: '#facc15',
                            500: '#eab308',
                            600: '#ca8a04',
                        }
                    },
                    fontFamily: {
                        cairo: ['Cairo', 'sans-serif'],
                        amiri: ['Amiri', 'serif'],
                    }
                }
            }
        }
    </script>
    <style>
        body {
            font-family: 'Cairo', sans-serif;
        }
        .font-quran {
            font-family: 'Amiri', serif;
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 dark:bg-navy-950 dark:text-slate-100 transition-colors duration-300 min-h-screen flex flex-col">

    <!-- Welcome Modal (النافذة المنبثقة الترحيبية) -->
    <div id="welcomeModal" class="fixed inset-0 z-[100] flex items-center justify-center p-4 bg-slate-900/60 backdrop-blur-md transition-opacity duration-300">
        <div class="relative w-full max-w-lg bg-white dark:bg-navy-900 border-2 border-navy-800/30 dark:border-gold-500/30 rounded-3xl p-6 sm:p-8 shadow-2xl text-center space-y-6 transform transition-all scale-100 overflow-hidden">
            
            <!-- Close Button (X) -->
            <button onclick="closeWelcomeModal()" class="absolute top-4 left-4 w-9 h-9 rounded-full bg-slate-100 dark:bg-navy-800 text-slate-500 dark:text-slate-300 hover:text-red-500 flex items-center justify-center transition-colors">
                <i class="fa-solid fa-xmark text-lg"></i>
            </button>

            <!-- Modal Title -->
            <h2 class="text-xl sm:text-2xl font-extrabold text-navy-900 dark:text-gold-400 leading-snug pt-2">
                موقف الشريعة الإسلامية من الانحراف الفكري
            </h2>

            <!-- Quran Verse Box -->
            <div class="p-6 rounded-2xl bg-navy-50 dark:bg-navy-950 border border-navy-200 dark:border-navy-800 space-y-2">
                <p class="font-quran text-2xl sm:text-3xl text-navy-900 dark:text-gold-400 leading-loose">
                    ﴿اهْدِنَا الصِّرَاطَ الْمُسْتَقِيمَ﴾
                </p>
                <p class="text-xs sm:text-sm font-semibold text-navy-700 dark:text-slate-400 pt-1">
                    [سورة الفاتحة - آية 6]
                </p>
            </div>

            <!-- Enter Button -->
            <div>
                <button onclick="closeWelcomeModal()" class="w-full py-3.5 px-6 rounded-xl bg-navy-800 hover:bg-navy-900 dark:bg-gold-500 dark:hover:bg-gold-600 dark:text-navy-950 text-white font-extrabold text-base shadow-lg transition-all flex items-center justify-center space-x-2 space-x-reverse">
                    <span>الدخول إلى الموقع</span>
                    <i class="fa-solid fa-arrow-left"></i>
                </button>
            </div>
        </div>
    </div>

    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-white/95 dark:bg-navy-900/95 backdrop-blur-md border-b border-navy-100 dark:border-navy-800 shadow-sm transition-colors duration-300">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-20">
                <!-- Logo / Title -->
                <div class="flex items-center space-x-3 space-x-reverse">
                    <div>
                        <span class="text-xl font-bold text-navy-900 dark:text-white block leading-tight">الشريعة والأمان الفكري</span>
                        <span class="text-xs text-navy-700 dark:text-gold-400 font-medium">حماية الفكر وفق المقاصد الشرعية</span>
                    </div>
                </div>

                <!-- Desktop Navigation Links -->
                <nav class="hidden md:flex space-x-6 space-x-reverse text-sm font-semibold text-slate-700 dark:text-slate-200">
                    <a href="#about" class="hover:text-navy-900 dark:hover:text-gold-400 transition-colors py-2">مفهوم الانحراف</a>
                    <a href="#rulings" class="hover:text-navy-900 dark:hover:text-gold-400 transition-colors py-2">الموقف والأحكام</a>
                    <a href="#prevention" class="hover:text-navy-900 dark:hover:text-gold-400 transition-colors py-2">سبل الوقاية</a>
                    <a href="#media" class="hover:text-navy-900 dark:hover:text-gold-400 transition-colors py-2">المرئيات والشروحات</a>
                    <a href="#quiz" class="hover:text-navy-900 dark:hover:text-gold-400 transition-colors py-2">اختبار الوعي الفكري</a>
                </nav>

                <!-- Actions: Dark Mode Switcher & Mobile Menu Button -->
                <div class="flex items-center space-x-3 space-x-reverse">
                    <!-- Dark/Light Mode Button -->
                    <button id="themeToggleBtn" onclick="toggleTheme()" class="p-2.5 rounded-xl bg-slate-100 dark:bg-navy-800 text-slate-700 dark:text-gold-400 hover:bg-slate-200 dark:hover:bg-navy-700 transition-colors flex items-center gap-2 text-xs font-bold">
                        <i id="themeIcon" class="fa-solid fa-moon text-base"></i>
                        <span id="themeText" class="hidden sm:inline">الوضع الداكن</span>
                    </button>

                    <!-- Mobile Menu Button -->
                    <button id="mobileMenuBtn" class="md:hidden p-2 rounded-lg text-slate-700 dark:text-slate-200 hover:bg-slate-100 dark:hover:bg-navy-800">
                        <i class="fa-solid fa-bars text-xl"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Menu -->
        <div id="mobileMenu" class="hidden md:hidden bg-white dark:bg-navy-900 border-b border-slate-200 dark:border-navy-800 px-4 pt-2 pb-4 space-y-2 text-sm font-semibold text-slate-700 dark:text-slate-200">
            <a href="#about" class="block py-2 px-3 rounded-md hover:bg-navy-50 dark:hover:bg-navy-800">مفهوم الانحراف</a>
            <a href="#rulings" class="block py-2 px-3 rounded-md hover:bg-navy-50 dark:hover:bg-navy-800">الموقف والأحكام</a>
            <a href="#prevention" class="block py-2 px-3 rounded-md hover:bg-navy-50 dark:hover:bg-navy-800">سبل الوقاية</a>
            <a href="#media" class="block py-2 px-3 rounded-md hover:bg-navy-50 dark:hover:bg-navy-800">المرئيات والشروحات</a>
            <a href="#quiz" class="block py-2 px-3 rounded-md hover:bg-navy-50 dark:hover:bg-navy-800">اختبار الوعي الفكري</a>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="relative bg-navy-900 dark:bg-navy-950 text-white py-20 lg:py-28 overflow-hidden shadow-md border-b border-navy-800">
        <div class="relative max-w-5xl mx-auto px-4 sm:px-6 lg:px-8 text-center space-y-6">
            <div class="inline-flex items-center space-x-2 space-x-reverse px-4 py-1.5 rounded-full bg-navy-800 border border-navy-700 text-gold-400 text-sm font-medium mb-2">
                <span>الأمان الفكري والتأصيل الشرعي</span>
            </div>
            
            <h1 class="text-3xl sm:text-5xl lg:text-6xl font-extrabold tracking-tight text-white leading-tight">
                موقف الشريعة الإسلامية من <span class="text-gold-400 underline decoration-gold-500/50 underline-offset-8">الانحراف الفكري</span>
            </h1>
            
            <p class="max-w-3xl mx-auto text-lg sm:text-xl text-slate-300 font-light leading-relaxed">
                رؤية إسلامية شاملة توضح حقيقة الحماية الفكرية، ومقاصد الشريعة السمحة في صيانة العقل والمجتمع من أفكار الغلو والإنحلال والجفاء.
            </p>

            <div class="pt-6 flex flex-wrap justify-center gap-4">
                <a href="#rulings" class="px-7 py-3.5 rounded-xl bg-gold-500 hover:bg-gold-600 text-navy-950 font-bold shadow-lg shadow-gold-500/20 transition-all flex items-center space-x-2 space-x-reverse">
                    <span>استكشف موقف الشريعة</span>
                    <i class="fa-solid fa-arrow-left"></i>
                </a>
                <a href="#media" class="px-7 py-3.5 rounded-xl bg-navy-800 hover:bg-navy-700 text-white font-semibold border border-navy-700 transition-all flex items-center space-x-2 space-x-reverse">
                    <span>مشاهدة المحاضرة</span>
                </a>
            </div>
        </div>
    </section>

    <!-- Section 1: Concept & Manifestations -->
    <section id="about" class="py-16 lg:py-24 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center max-w-3xl mx-auto mb-16 space-y-3">
            <h2 class="text-sm font-bold text-navy-700 dark:text-gold-400 uppercase tracking-wider">التأطير والمفهوم</h2>
            <h3 class="text-3xl font-extrabold text-navy-900 dark:text-white">ما هو الانحراف الفكري ومظاهره؟</h3>
            <div class="w-20 h-1 bg-navy-800 dark:bg-gold-500 mx-auto rounded-full"></div>
            <p class="text-slate-600 dark:text-slate-300 text-base sm:text-lg">
                الانحراف الفكري هو الميل والعدول عن الفطرة السليمة والمنهج الوسطي المستقيم إلى أفكار وآراء شاذة تخالف المبادئ الشرعية.
            </p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <div class="bg-white dark:bg-navy-900 rounded-2xl p-8 border border-slate-200 dark:border-navy-800 shadow-md hover:shadow-xl hover:-translate-y-1 transition-all duration-300 relative overflow-hidden">
                <h4 class="text-xl font-bold mb-3 text-navy-900 dark:text-gold-400">1. الغلو والتطرف (الإفراط)</h4>
                <p class="text-slate-600 dark:text-slate-300 text-sm leading-relaxed mb-4">
                    مجاوزة الحد الشرعي بالتكفير بغير حق، والتشدد المعطل للمقاصد، وتبني منهج العنف والخروج عن الجماعة.
                </p>
                <ul class="text-xs space-y-2 text-slate-500 dark:text-slate-400 border-t border-slate-200 dark:border-navy-800 pt-4">
                    <li>• استباحة الدماء والأموال المعصومة</li>
                    <li>• إساءة الظن بعلماء الأمة</li>
                </ul>
            </div>

            <div class="bg-white dark:bg-navy-900 rounded-2xl p-8 border border-slate-200 dark:border-navy-800 shadow-md hover:shadow-xl hover:-translate-y-1 transition-all duration-300 relative overflow-hidden">
                <h4 class="text-xl font-bold mb-3 text-navy-900 dark:text-gold-400">2. الإلحاد والتشكيك (التفريط)</h4>
                <p class="text-slate-600 dark:text-slate-300 text-sm leading-relaxed mb-4">
                    الانسلاخ من الثوابت الدينية، والتشكيك في مصادر التشريع الإسلامي، والترويج للشبهات الهدامة والعدمية.
                </p>
                <ul class="text-xs space-y-2 text-slate-500 dark:text-slate-400 border-t border-slate-200 dark:border-navy-800 pt-4">
                    <li>• الطعن في السنة النبوية والتفسير</li>
                    <li>• إنكار الغيبيات والمسلمات العقلية</li>
                </ul>
            </div>

            <div class="bg-white dark:bg-navy-900 rounded-2xl p-8 border border-slate-200 dark:border-navy-800 shadow-md hover:shadow-xl hover:-translate-y-1 transition-all duration-300 relative overflow-hidden">
                <h4 class="text-xl font-bold mb-3 text-navy-900 dark:text-gold-400">3. الغزو الفكري والإنحلال</h4>
                <p class="text-slate-600 dark:text-slate-300 text-sm leading-relaxed mb-4">
                    استيراد المفاهيم الهدامة وتفريغ المجتمع من هويته الإسلامية والقيم الأخلاقية تحت مسميات معاصرة براقة.
                </p>
                <ul class="text-xs space-y-2 text-slate-500 dark:text-slate-400 border-t border-slate-200 dark:border-navy-800 pt-4">
                    <li>• ذوبان الهوية الإسلامية المستقلة</li>
                    <li>• التبعية الفكرية والأخلاقية</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Section 2: Islamic Rulings & Maqasid -->
    <section id="rulings" class="py-16 lg:py-24 bg-navy-50 dark:bg-navy-900 border-y border-navy-100 dark:border-navy-800 transition-colors duration-300">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16 space-y-3">
                <h2 class="text-sm font-bold text-navy-700 dark:text-gold-400 uppercase tracking-wider">الأصول والأحكام</h2>
                <h3 class="text-3xl font-extrabold text-navy-900 dark:text-white">موقف الشريعة الإسلامية ومقاصدها</h3>
                <div class="w-20 h-1 bg-navy-800 dark:bg-gold-500 mx-auto rounded-full"></div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mb-12">
                <div class="bg-white dark:bg-navy-950 p-8 rounded-2xl border-r-4 border-navy-800 dark:border-gold-500 shadow-md flex space-x-6 space-x-reverse">
                    <div>
                        <h4 class="text-xl font-bold mb-2 text-navy-900 dark:text-gold-400">حفظ العقل والدين (من المقاصد الخمسة)</h4>
                        <p class="text-slate-600 dark:text-slate-300 text-sm leading-relaxed">
                            جاءت الشريعة لحماية عقل الإنسان من الشبهات والخرافات، وحفظ الدين من التحريف والزيادة أو النقصان. والانحراف الفكري يعد اعتداءً مباشراً على هذين المقصدين الجليلين.
                        </p>
                    </div>
                </div>

                <div class="bg-white dark:bg-navy-950 p-8 rounded-2xl border-r-4 border-gold-500 dark:border-gold-400 shadow-md flex space-x-6 space-x-reverse">
                    <div>
                        <h4 class="text-xl font-bold mb-2 text-navy-900 dark:text-gold-400">وجوب لزوم الوسطية والاعتدال</h4>
                        <p class="text-slate-600 dark:text-slate-300 text-sm leading-relaxed">
                            المنهج الإسلامي قائم على الوسطية بين الإفراط والتفريط. قال الله تعالى: ﴿وَكَذَٰلِكَ جَعَلْنَاكُمْ أُمَّةً وَسَطًا﴾، فالإسلام يحرم الغلو الشديد كما يحرم التفريط والتساهل.
                        </p>
                    </div>
                </div>
            </div>

            <div class="bg-navy-900 text-white rounded-3xl p-8 sm:p-12 shadow-xl relative overflow-hidden border border-navy-800">
                <h4 class="text-2xl font-bold text-gold-400 mb-8 flex items-center gap-3">
                    <span>من الأدلة الشرعية المحكمة</span>
                </h4>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                    <div class="bg-navy-950/80 p-6 rounded-2xl border border-navy-700 space-y-3">
                        <span class="text-xs font-semibold px-3 py-1 rounded-full bg-navy-800 text-gold-400 border border-navy-700">القرآن الكريم</span>
                        <p class="font-quran text-xl text-gold-300 leading-loose">
                            ﴿ يَا أَهْلَ الْكِتَابِ لَا تَغْلُوا فِي دِينِكُمْ وَلَا تَقُولُوا عَلَى اللَّهِ إِلَّا الْحَقَّ ﴾
                        </p>
                        <p class="text-xs text-slate-300 border-t border-white/10 pt-3">
                            [سورة النساء: 171] - نهي صريح ومباشر عن الغلو وتجاوز الحدود الشرعية.
                        </p>
                    </div>

                    <div class="bg-navy-950/80 p-6 rounded-2xl border border-navy-700 space-y-3">
                        <span class="text-xs font-semibold px-3 py-1 rounded-full bg-navy-800 text-gold-400 border border-navy-700">السنة النبوية</span>
                        <p class="font-quran text-xl text-gold-300 leading-loose">
                            «إِيَّاكُمْ وَالْغُلُوَّ فِي الدِّينِ، فَإِنَّمَا أَهْلَكَ مَنْ كَانَ قَبْلَكُمُ الْغُلُوُّ فِي الدِّينِ»
                        </p>
                        <p class="text-xs text-slate-300 border-t border-white/10 pt-3">
                            [رواه النسائي وابن ماجه وصححه الألباني] - تحذير نبوي جامع من خطر الانحراف الفكري والتشدد.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Section 3: Prevention & Treatment Tabs -->
    <section id="prevention" class="py-16 lg:py-24 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center max-w-3xl mx-auto mb-16 space-y-3">
            <h2 class="text-sm font-bold text-navy-700 dark:text-gold-400 uppercase tracking-wider">الحصانة الفكرية</h2>
            <h3 class="text-3xl font-extrabold text-navy-900 dark:text-white">سبل الوقاية والعلاج من الانحراف الفكري</h3>
            <div class="w-20 h-1 bg-navy-800 dark:bg-gold-500 mx-auto rounded-full"></div>
        </div>

        <div class="flex flex-wrap justify-center gap-2 mb-8" id="preventionTabs">
            <button onclick="switchTab('tab1')" id="btn-tab1" class="tab-btn active px-6 py-3 rounded-xl font-bold text-sm transition-all bg-navy-800 dark:bg-gold-500 text-white dark:text-navy-950 shadow-md">
                العلم الشرعي الراسخ
            </button>
            <button onclick="switchTab('tab2')" id="btn-tab2" class="tab-btn px-6 py-3 rounded-xl font-bold text-sm transition-all bg-slate-200 dark:bg-navy-900 text-slate-700 dark:text-slate-300 hover:bg-navy-100 dark:hover:bg-navy-800">
                الرجوع للعلماء الموثوقين
            </button>
            <button onclick="switchTab('tab3')" id="btn-tab3" class="tab-btn px-6 py-3 rounded-xl font-bold text-sm transition-all bg-slate-200 dark:bg-navy-900 text-slate-700 dark:text-slate-300 hover:bg-navy-100 dark:hover:bg-navy-800">
                التفكير الناقد والحذر
            </button>
        </div>

        <div class="bg-white dark:bg-navy-900 rounded-3xl p-8 border border-slate-200 dark:border-navy-800 shadow-lg">
            <div id="tab1" class="tab-content block space-y-4">
                <h4 class="text-2xl font-bold text-navy-900 dark:text-gold-400">1. نشر العلم النافع والفهم الصحيح</h4>
                <p class="text-slate-600 dark:text-slate-300 leading-relaxed">
                    العلم هو النور الذي يبدد ظلمات الجهل والشبهات. إن دراسة مقاصد الشريعة وقواعدها الكلية تمنح الفرد حصانة تمنعه من الوقوع في فخ الأفكار المنحرفة السطحية.
                </p>
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 pt-4">
                    <div class="p-4 rounded-xl bg-slate-50 dark:bg-navy-950 border border-slate-200 dark:border-navy-800 flex items-start space-x-3 space-x-reverse">
                        <span class="text-sm font-semibold text-navy-900 dark:text-slate-200">• تعلم أحكام الدين من مصادرها الأصيلة</span>
                    </div>
                    <div class="p-4 rounded-xl bg-slate-50 dark:bg-navy-950 border border-slate-200 dark:border-navy-800 flex items-start space-x-3 space-x-reverse">
                        <span class="text-sm font-semibold text-navy-900 dark:text-slate-200">• فهم النصوص الشرعية وفق فهم السلف الصالح</span>
                    </div>
                </div>
            </div>

            <div id="tab2" class="tab-content hidden space-y-4">
                <h4 class="text-2xl font-bold text-navy-900 dark:text-gold-400">2. الأخذ عن العلماء الموثوقين وهيئة كبار العلماء</h4>
                <p class="text-slate-600 dark:text-slate-300 leading-relaxed">
                    العلماء الراسخون هم الأمان بعد الله من الفتن. الانعزال عن العلماء وتلقي الفتاوى والأفكار من دعاة غير معروفين أو مجهولين عبر شبكات التواصل هو أول طرق الانحراف.
                </p>
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 pt-4">
                    <div class="p-4 rounded-xl bg-slate-50 dark:bg-navy-950 border border-slate-200 dark:border-navy-800 flex items-start space-x-3 space-x-reverse">
                        <span class="text-sm font-semibold text-navy-900 dark:text-slate-200">• صد الشبهات برأي العلماء المحققين</span>
                    </div>
                    <div class="p-4 rounded-xl bg-slate-50 dark:bg-navy-950 border border-slate-200 dark:border-navy-800 flex items-start space-x-3 space-x-reverse">
                        <span class="text-sm font-semibold text-navy-900 dark:text-slate-200">• التثبت والتحري من مصدر الفتاوى والمعلومات</span>
                    </div>
                </div>
            </div>

            <div id="tab3" class="tab-content hidden space-y-4">
                <h4 class="text-2xl font-bold text-navy-900 dark:text-gold-400">3. تعزيز التفكير الناقد والتوعية الإعلامية</h4>
                <p class="text-slate-600 dark:text-slate-300 leading-relaxed">
                    من يمتلك تفكيراً نقيداً لا ينساق خلف الشعارات البراقة والدعايات المضللة. التوعية بالأساليب التي تستخدمها الجماعات المنحرفة في استقطاب الشباب تسهم في إبطال مخططاتهم.
                </p>
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 pt-4">
                    <div class="p-4 rounded-xl bg-slate-50 dark:bg-navy-950 border border-slate-200 dark:border-navy-800 flex items-start space-x-3 space-x-reverse">
                        <span class="text-sm font-semibold text-navy-900 dark:text-slate-200">• عدم تداول الشائعات والحسابات المشبوهة</span>
                    </div>
                    <div class="p-4 rounded-xl bg-slate-50 dark:bg-navy-950 border border-slate-200 dark:border-navy-800 flex items-start space-x-3 space-x-reverse">
                        <span class="text-sm font-semibold text-navy-900 dark:text-slate-200">• تحكيم العقل والشرع قبل تصديق الشبهات</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Section 4: Media & Video Lecture (محاضرة الغزو الفكري - ابن باز) -->
    <section id="media" class="py-16 lg:py-24 bg-slate-100 dark:bg-navy-900 border-t border-slate-200 dark:border-navy-800 transition-colors duration-300">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-12 space-y-3">
                <h2 class="text-sm font-bold text-navy-700 dark:text-gold-400 uppercase tracking-wider">المرئيات والدروس</h2>
                <h3 class="text-3xl font-extrabold text-navy-900 dark:text-white">محاضرة قيمة: الغزو الفكري</h3>
                <p class="text-slate-600 dark:text-slate-300 text-sm sm:text-base">
                    للشيخ العلامة عبد العزيز بن عبد الله بن باز (رحمه الله تعالى)
                </p>
                <div class="w-20 h-1 bg-navy-800 dark:bg-gold-500 mx-auto rounded-full"></div>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 items-center">
                <!-- Interactive Direct Card Player for Guaranteed Access -->
                <div class="lg:col-span-7">
                    <div class="bg-white dark:bg-navy-950 rounded-2xl p-8 border border-slate-200 dark:border-navy-800 shadow-xl text-center space-y-6">
                        <div class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-red-100 dark:bg-red-950/60 text-red-600 dark:text-red-400 text-xs font-bold">
                            <i class="fa-brands fa-youtube text-sm"></i>
                            <span>إذاعة طريق السلف - المحاضرة الكاملة</span>
                        </div>
                        
                        <h4 class="text-xl sm:text-2xl font-bold text-navy-900 dark:text-white leading-relaxed">
                            محاضرة الغزو الفكري ووسائل مواجهته
                        </h4>
                        
                        <p class="text-xs sm:text-sm text-slate-500 dark:text-slate-400 max-w-md mx-auto">
                            يمكنك الانتقال المباشر للاستماع للمحاضرة بجودة عالية عبر منصة يوتيوب دون أي مشكلات في التشغيل:
                        </p>

                        <div>
                            <a href="https://youtu.be/xFDfdVrQnWM" target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-3 px-8 py-4 rounded-xl bg-red-600 hover:bg-red-700 text-white font-extrabold text-base shadow-lg shadow-red-600/30 transition-all">
                                <i class="fa-brands fa-youtube text-xl"></i>
                                <span>مشاهدة المحاضرة على يوتيوب</span>
                            </a>
                        </div>
                    </div>
                </div>

                <!-- Lecture Summary -->
                <div class="lg:col-span-5 space-y-6">
                    <div class="bg-white dark:bg-navy-950 p-6 sm:p-8 rounded-2xl shadow-md border border-slate-200 dark:border-navy-800">
                        <h4 class="text-xl font-bold text-navy-900 dark:text-gold-400 mb-4 flex items-center gap-2">
                            <span>أبرز محاور المحاضرة</span>
                        </h4>

                        <ul class="space-y-4 text-sm text-slate-700 dark:text-slate-300">
                            <li class="flex items-start gap-3">
                                <span class="w-6 h-6 rounded-full bg-navy-100 dark:bg-navy-800 text-navy-800 dark:text-gold-400 flex items-center justify-center shrink-0 text-xs font-bold mt-0.5">1</span>
                                <span>خطورة الغزو الفكري وأساليبه الحديثة في استهداف عقيدة الأمة وقيمها.</span>
                            </li>
                            <li class="flex items-start gap-3">
                                <span class="w-6 h-6 rounded-full bg-navy-100 dark:bg-navy-800 text-navy-800 dark:text-gold-400 flex items-center justify-center shrink-0 text-xs font-bold mt-0.5">2</span>
                                <span>ضرورة الاعتصام بالكتاب والسنة والالتفاف حول علماء الأمة الموثوقين.</span>
                            </li>
                            <li class="flex items-start gap-3">
                                <span class="w-6 h-6 rounded-full bg-navy-100 dark:bg-navy-800 text-navy-800 dark:text-gold-400 flex items-center justify-center shrink-0 text-xs font-bold mt-0.5">3</span>
                                <span>واجب الأسرة والمؤسسات التعليمية في تحصين الناشئة من الأفكار المنحرفة.</span>
                            </li>
                        </ul>

                        <div class="mt-6 pt-4 border-t border-slate-200 dark:border-navy-800 flex items-center justify-between text-xs text-slate-500 dark:text-slate-400">
                            <span>مادة صوتية موثوقة</span>
                            <span>التأصيل الشرعي</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Section 5: Interactive Quiz -->
    <section id="quiz" class="py-16 lg:py-24 max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="bg-white dark:bg-navy-900 rounded-3xl p-6 sm:p-10 border border-slate-200 dark:border-navy-800 shadow-xl relative overflow-hidden">
            <div class="text-center max-w-2xl mx-auto mb-8 space-y-2">
                <span class="px-3 py-1 rounded-full bg-navy-100 dark:bg-navy-800 text-navy-800 dark:text-gold-400 text-xs font-bold">اختبر معلوماتك</span>
                <h3 class="text-2xl sm:text-3xl font-extrabold text-navy-900 dark:text-white">اختبار الوعي الفكري التفاعلي</h3>
                <p class="text-slate-600 dark:text-slate-300 text-xs sm:text-sm">
                    هل تستطيع التمييز بين المنهج الوسطي والتفكير المنحرف؟ أجب عن الأسئلة التالية لمعرفة النتيجة:
                </p>
            </div>

            <div id="quizContainer">
                <div id="questionCard" class="space-y-6">
                    <div class="w-full bg-slate-100 dark:bg-navy-950 h-2 rounded-full overflow-hidden">
                        <div id="progressBar" class="bg-navy-800 dark:bg-gold-500 h-full w-1/3 transition-all duration-300"></div>
                    </div>

                    <div class="flex justify-between items-center text-xs text-slate-500 dark:text-slate-400">
                        <span id="questionNum">السؤال 1 من 3</span>
                        <span id="scoreTracker" class="font-semibold text-navy-800 dark:text-gold-400">النقاط: 0</span>
                    </div>

                    <h4 id="questionText" class="text-lg sm:text-xl font-bold text-navy-900 dark:text-white min-h-[60px]">
                        جاري تحميل السؤال...
                    </h4>

                    <div id="optionsContainer" class="space-y-3"></div>

                    <div id="feedbackText" class="hidden p-4 rounded-xl text-sm font-semibold"></div>

                    <div class="flex justify-end pt-4">
                        <button id="nextBtn" onclick="nextQuestion()" disabled class="px-6 py-2.5 rounded-xl bg-navy-800 dark:bg-gold-500 opacity-50 cursor-not-allowed text-white dark:text-navy-950 font-bold transition-all">
                            السؤال التالي
                        </button>
                    </div>
                </div>

                <div id="resultCard" class="hidden text-center py-8 space-y-6">
                    <h4 class="text-2xl font-bold text-navy-900 dark:text-white">اكتمل الاختبار بنجاح!</h4>
                    <p id="finalScoreText" class="text-lg text-slate-600 dark:text-slate-300"></p>
                    <button onclick="restartQuiz()" class="px-8 py-3 rounded-xl bg-navy-800 dark:bg-gold-500 text-white dark:text-navy-950 font-bold hover:bg-navy-900 dark:hover:bg-gold-600 transition-all shadow-md">
                        إعادة الاختبار
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="mt-auto bg-navy-950 text-slate-300 border-t border-navy-900 py-12 relative overflow-hidden">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center space-y-6">
            <div class="flex justify-center items-center space-x-3 space-x-reverse">
                <span class="text-lg font-bold text-white">الأمان الفكري في الشريعة الإسلامية</span>
            </div>

            <p class="text-xs text-slate-400 max-w-md mx-auto leading-relaxed">
                موقع توعوي يهدف لنشر الوسطية وتوضيح موقف الشريعة السمحاء من الغلو والانحراف الفكري بمختلف أشكاله.
            </p>

            <div class="w-24 h-0.5 bg-navy-800 mx-auto"></div>

            <div class="pt-2">
                <p class="text-base sm:text-lg font-semibold text-gold-400 tracking-wide">
                    طور بواسطة <span class="text-gold-300 font-bold border-b border-gold-400 pb-0.5">لمار السعود</span>
                </p>
                <p class="text-xs text-slate-500 mt-2">جميع الحقوق محفوظة © 2026</p>
            </div>
        </div>
    </footer>

    <!-- JavaScript Logic -->
    <script>
        // Theme Toggle Logic (Light / Dark Mode)
        function toggleTheme() {
            const html = document.documentElement;
            const themeIcon = document.getElementById('themeIcon');
            const themeText = document.getElementById('themeText');

            if (html.classList.contains('dark')) {
                html.classList.remove('dark');
                themeIcon.className = 'fa-solid fa-moon text-base';
                themeText.textContent = 'الوضع الداكن';
                localStorage.setItem('theme', 'light');
            } else {
                html.classList.add('dark');
                themeIcon.className = 'fa-solid fa-sun text-base';
                themeText.textContent = 'الوضع الفاتح';
                localStorage.setItem('theme', 'dark');
            }
        }

        // Mobile Menu Toggle
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const mobileMenu = document.getElementById('mobileMenu');

        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // Prevention Tabs Function
        function switchTab(tabId) {
            document.querySelectorAll('.tab-content').forEach(content => {
                content.classList.add('hidden');
            });
            document.querySelectorAll('.tab-btn').forEach(btn => {
                btn.classList.remove('bg-navy-800', 'dark:bg-gold-500', 'text-white', 'dark:text-navy-950', 'shadow-md');
                btn.classList.add('bg-slate-200', 'dark:bg-navy-900', 'text-slate-700', 'dark:text-slate-300');
            });

            document.getElementById(tabId).classList.remove('hidden');
            const activeBtn = document.getElementById('btn-' + tabId);
            activeBtn.classList.remove('bg-slate-200', 'dark:bg-navy-900', 'text-slate-700', 'dark:text-slate-300');
            activeBtn.classList.add('bg-navy-800', 'dark:bg-gold-500', 'text-white', 'dark:text-navy-950', 'shadow-md');
        }

        // Quiz Logic
        const quizData = [
            {
                question: "ما هو المنهج الشرعي الذي حث عليه القرآن الكريم والسنة النبوية؟",
                options: [
                    "الإنحلال والانسلاخ من الثوابت",
                    "الوسطية والاعتدال بلا غلو ولا جفاء",
                    "التشدد وتكفير الآخرين بدون حق",
                    "الانعزال التام عن الحياة والمجتمع"
                ],
                correct: 1,
                explanation: "الوسطية والاعتدال هي جوهر الإسلام كما قال تعالى: ﴿وَكَذَٰلِكَ جَعَلْنَاكُمْ أُمَّةً وَسَطًا﴾."
            },
            {
                question: "ما الواجب عند سماع شبهات أو فتاوى مجهولة المصدر عبر منصات التواصل؟",
                options: [
                    "تداولها ونشرها مباشرة للناس",
                    "تصديقها والعمل بها فوراً",
                    "ردها والتثبت بعرضها على العلماء الراسخين والمصادر الموثوقة",
                    "تجاهل العلم الشرعي بالكلية"
                ],
                correct: 2,
                explanation: "الرد للعلماء الموثوقين يحمي العقل من الانسياق خلف الشبهات والأفكار المنحرفة."
            },
            {
                question: "أي من المقاصد الشرعية الخمسة يرتبط بشكل مباشر بحمايتنا من الانحراف الفكري؟",
                options: [
                    "حفظ المال فقط",
                    "حفظ الدين والعقل",
                    "حفظ النسل فقط",
                    "لا يتصل بمقاصد الشريعة"
                ],
                correct: 1,
                explanation: "حفظ الدين والعقل من أهم المقاصد الضرورية الخمسة التي جاءت الشريعة لرعايتها وصيانتها."
            }
        ];

        let currentQuestion = 0;
        let score = 0;

        function loadQuestion() {
            const q = quizData[currentQuestion];
            document.getElementById('questionText').innerText = q.question;
            document.getElementById('questionNum').innerText = `السؤال ${currentQuestion + 1} من ${quizData.length}`;
            document.getElementById('scoreTracker').innerText = `النقاط: ${score}`;
            document.getElementById('progressBar').style.width = `${((currentQuestion + 1) / quizData.length) * 100}%`;
            
            const optionsContainer = document.getElementById('optionsContainer');
            optionsContainer.innerHTML = '';

            const feedback = document.getElementById('feedbackText');
            feedback.classList.add('hidden');

            const nextBtn = document.getElementById('nextBtn');
            nextBtn.disabled = true;
            nextBtn.classList.add('opacity-50', 'cursor-not-allowed');

            q.options.forEach((opt, index) => {
                const btn = document.createElement('button');
                btn.className = 'w-full text-right p-4 rounded-xl border border-slate-200 dark:border-navy-800 bg-slate-50 dark:bg-navy-950 hover:bg-navy-50 dark:hover:bg-navy-800 transition-all font-medium text-sm flex items-center justify-between text-navy-900 dark:text-slate-200';
                btn.innerHTML = `<span>${opt}</span>`;
                btn.onclick = () => selectOption(index, btn);
                optionsContainer.appendChild(btn);
            });
        }

        function selectOption(index, btnElement) {
            const q = quizData[currentQuestion];
            const optionsBtns = document.getElementById('optionsContainer').children;

            for (let b of optionsBtns) {
                b.disabled = true;
                b.classList.add('cursor-default');
            }

            const feedback = document.getElementById('feedbackText');
            feedback.classList.remove('hidden');

            if (index === q.correct) {
                score += 10;
                btnElement.classList.remove('bg-slate-50', 'dark:bg-navy-950');
                btnElement.classList.add('bg-emerald-100', 'dark:bg-emerald-950/80', 'border-emerald-500', 'text-emerald-950', 'dark:text-emerald-200');
                
                feedback.className = 'p-4 rounded-xl text-sm font-semibold bg-emerald-100 dark:bg-emerald-950/80 text-emerald-950 dark:text-emerald-200 border border-emerald-500';
                feedback.innerHTML = `إجابة صحيحة! ${q.explanation}`;
            } else {
                btnElement.classList.remove('bg-slate-50', 'dark:bg-navy-950');
                btnElement.classList.add('bg-red-100', 'dark:bg-red-950/80', 'border-red-500', 'text-red-950', 'dark:text-red-200');

                optionsBtns[q.correct].classList.add('bg-emerald-100', 'dark:bg-emerald-950/80', 'border-emerald-500');

                feedback.className = 'p-4 rounded-xl text-sm font-semibold bg-red-100 dark:bg-red-950/80 text-red-950 dark:text-red-200 border border-red-500';
                feedback.innerHTML = `إجابة خاطئة. الإجابة الصحيحة هي: (${q.options[q.correct]}).`;
            }

            document.getElementById('scoreTracker').innerText = `النقاط: ${score}`;

            const nextBtn = document.getElementById('nextBtn');
            nextBtn.disabled = false;
            nextBtn.classList.remove('opacity-50', 'cursor-not-allowed');
        }

        function nextQuestion() {
            currentQuestion++;
            if (currentQuestion < quizData.length) {
                loadQuestion();
            } else {
                showResults();
            }
        }

        function showResults() {
            document.getElementById('questionCard').classList.add('hidden');
            const resultCard = document.getElementById('resultCard');
            resultCard.classList.remove('hidden');

            const total = quizData.length * 10;
            document.getElementById('finalScoreText').innerText = `حصلت على ${score} من أصل ${total} درجة. ممتاز! وعيك الفكري والشرعي عالي.`;
        }

        function restartQuiz() {
            currentQuestion = 0;
            score = 0;
            document.getElementById('resultCard').classList.add('hidden');
            document.getElementById('questionCard').classList.remove('hidden');
            loadQuestion();
        }

        window.onload = function() {
            loadQuestion();
        };

        function closeWelcomeModal() {
            const modal = document.getElementById('welcomeModal');
            modal.classList.add('opacity-0', 'pointer-events-none');
            setTimeout(() => {
                modal.style.display = 'none';
            }, 300);
        }
    </script>
</body>
</html>
