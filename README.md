<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>موقف الشريعة الإسلامية من الانحراف الفكري</title>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;500;700;800&family=Amiri:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-color: #f8fafc;
            --card-bg: #ffffff;
            --text-main: #0f172a;
            --text-muted: #475569;
            --primary: #065f46;
            --primary-light: #047857;
            --accent: #d97706;
            --border: #e2e8f0;
            --shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05), 0 2px 4px -1px rgba(0, 0, 0, 0.03);
            --shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.08);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Tajawal', sans-serif;
            transition: all 0.25s ease;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-main);
            line-height: 1.8;
            overflow-x: hidden;
        }

        /* Modal / Pop-up */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(15, 23, 42, 0.6);
            backdrop-filter: blur(4px);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 9999;
            padding: 20px;
            opacity: 1;
            visibility: visible;
            transition: opacity 0.3s ease, visibility 0.3s ease;
        }

        .modal-overlay.hidden {
            opacity: 0;
            visibility: hidden;
            pointer-events: none;
        }

        .modal-card {
            background: #ffffff;
            border-radius: 16px;
            max-width: 520px;
            width: 100%;
            padding: 36px 28px;
            text-align: center;
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1);
            border: 1px solid var(--border);
            position: relative;
        }

        .modal-close-btn {
            position: absolute;
            top: 16px;
            left: 16px;
            background: #f1f5f9;
            border: none;
            width: 32px;
            height: 32px;
            border-radius: 50%;
            font-size: 16px;
            cursor: pointer;
            color: var(--text-muted);
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .modal-close-btn:hover {
            background: #e2e8f0;
            color: var(--text-main);
        }

        .modal-title {
            font-size: 1.35rem;
            font-weight: 800;
            color: var(--primary);
            margin-bottom: 20px;
            line-height: 1.5;
        }

        .modal-quran {
            font-family: 'Amiri', serif;
            font-size: 1.8rem;
            color: var(--accent);
            margin: 16px 0 8px;
            font-weight: 700;
        }

        .modal-surah {
            font-size: 0.95rem;
            color: var(--text-muted);
            margin-bottom: 28px;
            font-weight: 500;
        }

        .btn-modal {
            background: var(--primary);
            color: #ffffff;
            border: none;
            padding: 12px 32px;
            font-size: 1rem;
            font-weight: 700;
            border-radius: 10px;
            cursor: pointer;
            width: 100%;
        }

        .btn-modal:hover {
            background: var(--primary-light);
        }

        /* Container */
        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            background: #ffffff;
            border-bottom: 1px solid var(--border);
            padding: 20px 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .nav-wrapper {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.2rem;
            font-weight: 800;
            color: var(--primary);
        }

        /* Hero */
        .hero {
            padding: 60px 0 40px;
            text-align: center;
        }

        .hero h1 {
            font-size: 2.2rem;
            font-weight: 800;
            color: var(--primary);
            margin-bottom: 16px;
        }

        .hero p {
            font-size: 1.15rem;
            color: var(--text-muted);
            max-width: 750px;
            margin: 0 auto 30px;
        }

        /* Section Cards */
        .section-title {
            font-size: 1.6rem;
            font-weight: 800;
            color: var(--primary);
            margin-bottom: 24px;
            position: relative;
            padding-bottom: 8px;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            right: 0;
            width: 60px;
            height: 4px;
            background: var(--accent);
            border-radius: 2px;
        }

        .grid-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 24px;
            margin-bottom: 50px;
        }

        .card {
            background: var(--card-bg);
            padding: 28px;
            border-radius: 14px;
            border: 1px solid var(--border);
            box-shadow: var(--shadow);
        }

        .card:hover {
            transform: translateY(-3px);
            box-shadow: var(--shadow-lg);
        }

        .card h3 {
            font-size: 1.25rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 12px;
        }

        .card p {
            color: var(--text-muted);
            font-size: 0.98rem;
        }

        /* Video Box */
        .video-box {
            background: var(--card-bg);
            border: 1px solid var(--border);
            border-radius: 16px;
            padding: 32px;
            box-shadow: var(--shadow);
            margin-bottom: 50px;
        }

        .video-player-container {
            position: relative;
            padding-bottom: 56.25%;
            height: 0;
            overflow: hidden;
            border-radius: 12px;
            margin-bottom: 24px;
            background: #000;
        }

        .video-player-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: 0;
        }

        .video-link-fallback {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            background: #cc0000;
            color: #ffffff;
            text-decoration: none;
            padding: 12px 24px;
            border-radius: 8px;
            font-weight: 700;
            font-size: 0.95rem;
            margin-top: 10px;
        }

        .video-link-fallback:hover {
            background: #a30000;
        }

        /* Tabs Section */
        .tabs-container {
            background: var(--card-bg);
            border: 1px solid var(--border);
            border-radius: 16px;
            padding: 30px;
            margin-bottom: 50px;
            box-shadow: var(--shadow);
        }

        .tab-buttons {
            display: flex;
            gap: 12px;
            border-bottom: 2px solid var(--border);
            padding-bottom: 12px;
            margin-bottom: 24px;
            flex-wrap: wrap;
        }

        .tab-btn {
            background: transparent;
            border: none;
            padding: 10px 20px;
            font-size: 1rem;
            font-weight: 700;
            color: var(--text-muted);
            cursor: pointer;
            border-radius: 8px;
        }

        .tab-btn.active {
            background: var(--primary);
            color: #ffffff;
        }

        .tab-content {
            display: none;
        }

        .tab-content.active {
            display: block;
        }

        /* Quiz */
        .quiz-container {
            background: var(--card-bg);
            border: 1px solid var(--border);
            border-radius: 16px;
            padding: 32px;
            margin-bottom: 60px;
            box-shadow: var(--shadow);
        }

        .quiz-option {
            background: #f8fafc;
            border: 1px solid var(--border);
            padding: 14px 20px;
            border-radius: 10px;
            margin-bottom: 12px;
            cursor: pointer;
            font-weight: 500;
        }

        .quiz-option:hover {
            background: #f1f5f9;
            border-color: var(--primary);
        }

        .quiz-option.correct {
            background: #dcfce7;
            border-color: #16a34a;
            color: #15803d;
            font-weight: 700;
        }

        .quiz-option.wrong {
            background: #fee2e2;
            border-color: #dc2626;
            color: #b91c1c;
            font-weight: 700;
        }

        /* Footer */
        footer {
            background: #ffffff;
            border-top: 1px solid var(--border);
            padding: 30px 0;
            text-align: center;
            font-weight: 700;
            color: var(--primary);
            font-size: 1.05rem;
        }
    </style>
</head>
<body>

    <!-- Pop-up Modal -->
    <div class="modal-overlay" id="welcomeModal">
        <div class="modal-card">
            <button class="modal-close-btn" onclick="closeModal()">✕</button>
            <div class="modal-title">موقف الشريعة الإسلامية من الانحراف الفكري</div>
            <div class="modal-quran">﴿ اهْدِنَا الصِّرَاطَ الْمُسْتَقِيمَ ﴾</div>
            <div class="modal-surah">سورة الفاتحة - آية 6</div>
            <button class="btn-modal" onclick="closeModal()">الدخول إلى الموقع</button>
        </div>
    </div>

    <!-- Header -->
    <header>
        <div class="container nav-wrapper">
            <div class="logo">موقف الشريعة من الانحراف الفكري</div>
        </div>
    </header>

    <!-- Main Content -->
    <div class="container">
        
        <!-- Hero -->
        <section class="hero">
            <h1>موقف الشريعة الإسلامية من الانحراف الفكري</h1>
            <p>تأصيل شرعي وبيان علمي لكيفية مواجهة الفكر الضال والغزو الفكري وحماية المجتمع وحفظ مقاصد الشريعة الإسلامية.</p>
        </section>

        <!-- Section 1: Concept -->
        <section>
            <h2 class="section-title">مفهوم الانحراف الفكري ومظاهره</h2>
            <div class="grid-cards">
                <div class="card">
                    <h3>التطرف والغلو</h3>
                    <p>مجاوزة حد الاعتدال في الفهم والتطبيق، والخروج عن نهج الوسطية الذي جاء به الإسلام ليتحول إلى صدام وتكفير.</p>
                </div>
                <div class="card">
                    <h3>الإلحاد والتشكيك</h3>
                    <p>الطعن في الثوابت الشرعية والعقائدية ونشر الشبهات الهادفة لزعزعة إيمان الشباب وتفريغ الدين من محتواه.</p>
                </div>
                <div class="card">
                    <h3>الغزو الفكري</h3>
                    <p>المحاولات المستمرة لتغيير المفاهيم والقيم الإسلامية عبر وسائل الإعلام المختلفة وتسهيل قبول الشبهات.</p>
                </div>
            </div>
        </section>

        <!-- Section 2: Video -->
        <section class="video-box">
            <h2 class="section-title">محاضرة مرئية: الغزو الفكري</h2>
            <p style="color: var(--text-muted); margin-bottom: 20px;">سماحة الشيخ العلامة عبد العزيز بن عبد الله بن باز - رحمه الله تعالى -</p>
            
            <div class="video-player-container">
                <iframe src="https://www.youtube.com/embed/xFDfdVrQnWM" title="محاضرة الغزو الفكري - الشيخ ابن باز" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </div>

            <div style="text-align: center;">
                <p style="font-size: 0.9rem; color: var(--text-muted); margin-bottom: 10px;">إذا لم يظهر المشغل أعلاه بشكل صحيح، يمكنك الانتقال مباشرة لرابط المقطع:</p>
                <a href="https://youtu.be/xFDfdVrQnWM" target="_blank" class="video-link-fallback">
                    فتح المحاضرة في يوتيوب
                </a>
            </div>
        </section>

        <!-- Section 3: Tabs -->
        <section class="tabs-container">
            <h2 class="section-title">سبل الشريعة في الوقاية والعلاج</h2>
            
            <div class="tab-buttons">
                <button class="tab-btn active" onclick="openTab(event, 'tab1')">1. العناية بالقرآن والسنة</button>
                <button class="tab-btn" onclick="openTab(event, 'tab2')">2. لزوم العلماء</button>
                <button class="tab-btn" onclick="openTab(event, 'tab3')">3. نشر الفكر الوسطي</button>
            </div>

            <div id="tab1" class="tab-content active">
                <h3 style="color: var(--primary); margin-bottom: 10px;">الاعتصام بالوحيين</h3>
                <p style="color: var(--text-muted);">الرجوع إلى القرآن الكريم والسنة النبوية الصحيحة على فهم السلف الصالح هو الحصن المنيع من ورود الشبهات واستقرار الضلالات في القلوب.</p>
            </div>

            <div id="tab2" class="tab-content">
                <h3 style="color: var(--primary); margin-bottom: 10px;">أخذ العلم عن أهله</h3>
                <p style="color: var(--text-muted);">تلقي العلم عن العلماء الرسوخ المعروفين بالنصح والاعتدال يمنع الفهم المبتور ويحمي من الانجرار خلف أصحاب الأهواء والدعوات المجهولة.</p>
            </div>

            <div id="tab3" class="tab-content">
                <h3 style="color: var(--primary); margin-bottom: 10px;">تعزيز الوسطية والاعتدال</h3>
                <p style="color: var(--text-muted);">إبراز محاسن الشريعة الإسلامية وسماحتها ومقاصدها العالية في حفظ الضروريات الخمس (الدين، النفس، العقل، العرض، المال).</p>
            </div>
        </section>

        <!-- Section 4: Interactive Quiz -->
        <section class="quiz-container">
            <h2 class="section-title">اختبار الوعي الفكري</h2>
            <p style="margin-bottom: 20px; color: var(--text-muted);">ما هي الوسيلة الأساسية التي حثت الشريعة عليها للحماية من الانحراف الفكري؟</p>

            <div class="quiz-option" onclick="checkAnswer(this, false)">الانعزال التام عن المجتمع وعدم التعلم.</div>
            <div class="quiz-option" onclick="checkAnswer(this, true)">التمسك بالكتاب والسنة وأخذ العلم عن العلماء الراسخين.</div>
            <div class="quiz-option" onclick="checkAnswer(this, false)">اتباع كل ما يُنشر في وسائل التواصل دون تثبت.</div>

            <div id="quizResult" style="margin-top: 15px; font-weight: 700; display: none;"></div>
        </section>

    </div>

    <!-- Footer -->
    <footer>
        <div class="container">
            طور بواسطة لمار السعود
        </div>
    </footer>

    <script>
        function closeModal() {
            document.getElementById('welcomeModal').classList.add('hidden');
        }

        function openTab(evt, tabId) {
            const contents = document.querySelectorAll('.tab-content');
            contents.forEach(content => content.classList.remove('active'));

            const buttons = document.querySelectorAll('.tab-btn');
            buttons.forEach(btn => btn.classList.remove('active'));

            document.getElementById(tabId).classList.add('active');
            evt.currentTarget.classList.add('active');
        }

        function checkAnswer(element, isCorrect) {
            const options = document.querySelectorAll('.quiz-option');
            options.forEach(opt => {
                opt.style.pointerEvents = 'none';
            });

            const resultDiv = document.getElementById('quizResult');
            resultDiv.style.display = 'block';

            if (isCorrect) {
                element.classList.add('correct');
                resultDiv.style.color = '#15803d';
                resultDiv.textContent = 'إجابة صحيحة! التمسك بالوحيين وأخذ العلم عن العلماء هو الأمان والوقاية.';
            } else {
                element.classList.add('wrong');
                resultDiv.style.color = '#b91c1c';
                resultDiv.textContent = 'إجابة خاطئة. الإجابة الصحيحة هي: التمسك بالكتاب والسنة وأخذ العلم عن العلماء الراسخين.';
            }
        }
    </script>
</body>
</html>
