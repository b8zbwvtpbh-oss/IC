<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>الانحراف الفكري بالشريعة الإسلامية</title>
    <link href="https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&family=Tajawal:wght@400;500;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-main: #121212;
            --bg-card: #1e1e1e;
            --bg-hover: #2a2a2a;
            --primary-orange: #f57c00;
            --dark-orange: #e65100;
            --accent-yellow: #ffb300;
            --text-white: #fffdf9;
            --text-muted: #b0bec5;
            --border-color: #333333;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Tajawal', sans-serif;
        }

        body {
            background-color: var(--bg-main);
            /* تدرج لوني دافئ ومضيء من الأعلى */
            background-image: radial-gradient(circle at 50% 0%, rgba(245, 124, 0, 0.28) 0%, rgba(230, 81, 0, 0.14) 35%, rgba(18, 18, 18, 0) 70%);
            background-repeat: no-repeat;
            color: var(--text-white);
            line-height: 1.8;
            padding-bottom: 50px;
            position: relative;
            overflow-x: hidden;
        }

        /* Fixed Background Icons Layer */
        .bg-icons-layer {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
            overflow: hidden;
        }

        .floating-icon {
            position: absolute;
            color: var(--accent-yellow);
            opacity: 0.12;
            animation: floatAnim 10s infinite ease-in-out alternate;
            font-size: 2rem;
            user-select: none;
        }

        @keyframes floatAnim {
            0% { transform: translateY(0px) rotate(0deg); }
            100% { transform: translateY(-30px) rotate(15deg); }
        }

        /* Modal Overlay */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.88);
            backdrop-filter: blur(8px);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 9999;
            padding: 20px;
        }

        .modal-card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 16px;
            width: 100%;
            max-width: 440px;
            padding: 24px;
            position: relative;
            box-shadow: 0 10px 30px rgba(0,0,0,0.6);
            text-align: center;
        }

        .close-btn {
            position: absolute;
            top: 16px;
            left: 16px;
            width: 36px;
            height: 36px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            border: none;
            color: var(--text-white);
            font-size: 18px;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: 0.2s;
        }

        .close-btn:hover {
            background: rgba(255, 255, 255, 0.2);
        }

        .modal-title {
            font-size: 1.3rem;
            font-weight: 700;
            color: var(--accent-yellow);
            margin-top: 10px;
            margin-bottom: 20px;
        }

        .verse-box {
            background: rgba(245, 124, 0, 0.1);
            border: 1px solid var(--primary-orange);
            border-radius: 12px;
            padding: 20px;
            margin-bottom: 20px;
        }

        .verse-text {
            font-family: 'Amiri', serif;
            font-size: 1.6rem;
            color: var(--accent-yellow);
            margin-bottom: 5px;
        }

        .verse-label {
            font-size: 0.85rem;
            color: var(--text-muted);
        }

        .developer-tag {
            font-size: 0.95rem;
            color: var(--text-muted);
            border-top: 1px solid var(--border-color);
            padding-top: 15px;
        }

        /* Container & Content */
        .container {
            position: relative;
            z-index: 1;
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            text-align: center;
            padding: 30px 0 10px;
        }

        header h1 {
            color: var(--accent-yellow);
            font-size: 2rem;
            margin-bottom: 8px;
            text-shadow: 0 0 20px rgba(255, 179, 0, 0.3);
        }

        header p {
            color: var(--text-muted);
            font-size: 0.95rem;
        }

        /* Top Navigation Tabs */
        .nav-tabs {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin: 25px 0;
            border-bottom: 1px solid var(--border-color);
            padding-bottom: 15px;
            flex-wrap: wrap;
        }

        .nav-btn {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            color: var(--text-white);
            padding: 10px 20px;
            border-radius: 20px;
            cursor: pointer;
            font-weight: 600;
            transition: 0.3s;
        }

        .nav-btn.active, .nav-btn:hover {
            background: var(--primary-orange);
            border-color: var(--accent-yellow);
            color: #fff;
            box-shadow: 0 4px 15px rgba(245, 124, 0, 0.3);
        }

        /* Pages & Accordions */
        .page-content {
            display: none;
        }

        .page-content.active {
            display: block;
        }

        .accordion-item {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            margin-bottom: 15px;
            overflow: hidden;
        }

        .accordion-header {
            width: 100%;
            background: var(--bg-card);
            border: none;
            color: var(--accent-yellow);
            padding: 18px 20px;
            font-size: 1.1rem;
            font-weight: 700;
            text-align: right;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: 0.2s;
        }

        .accordion-header:hover {
            background: var(--bg-hover);
        }

        .accordion-icon {
            font-size: 1.1rem;
            color: var(--primary-orange);
            transition: transform 0.3s ease, color 0.3s ease;
        }

        .accordion-body {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease-out;
            padding: 0 20px;
            background: #181818;
            color: var(--text-white);
            border-top: 1px solid transparent;
        }

        .accordion-body.open {
            padding: 20px;
            max-height: 1000px;
            border-top-color: var(--border-color);
        }

        ul {
            list-style: none;
            padding-right: 0;
        }

        li {
            position: relative;
            padding-right: 22px;
            margin-bottom: 12px;
        }

        li::before {
            content: "✨";
            font-size: 0.9rem;
            position: absolute;
            right: 0;
            top: 2px;
        }

        /* Quiz Styling */
        .quiz-card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            padding: 20px;
            margin-bottom: 15px;
        }

        .quiz-card p {
            font-weight: 700;
            color: var(--accent-yellow);
            margin-bottom: 12px;
        }

        .options-grid {
            display: grid;
            gap: 10px;
        }

        .option-btn {
            background: var(--bg-hover);
            border: 1px solid var(--border-color);
            color: var(--text-white);
            padding: 12px 15px;
            border-radius: 8px;
            text-align: right;
            cursor: pointer;
            transition: 0.2s;
        }

        .option-btn:hover {
            border-color: var(--primary-orange);
        }

        .option-btn.correct {
            background: #2e7d32 !important;
            border-color: #4caf50 !important;
        }

        .option-btn.wrong {
            background: #c62828 !important;
            border-color: #ef5350 !important;
        }

        .footer-tag {
            text-align: center;
            margin-top: 40px;
            font-size: 0.95rem;
            color: var(--text-muted);
            border-top: 1px solid var(--border-color);
            padding-top: 20px;
        }

        @media (max-width: 600px) {
            header h1 { font-size: 1.6rem; }
            .container { padding: 12px; }
        }
    </style>
</head>
<body>

    <!-- Transparent Floating Yellow/Orange Icons in Background -->
    <div class="bg-icons-layer">
        <div class="floating-icon" style="top: 8%; left: 10%; animation-duration: 8s;">💡</div>
        <div class="floating-icon" style="top: 18%; right: 15%; animation-duration: 11s;">🧠</div>
        <div class="floating-icon" style="top: 42%; left: 8%; animation-duration: 9s;">✨</div>
        <div class="floating-icon" style="top: 58%; right: 12%; animation-duration: 12s;">💡</div>
        <div class="floating-icon" style="top: 78%; left: 15%; animation-duration: 10s;">✨</div>
        <div class="floating-icon" style="top: 85%; right: 20%; animation-duration: 7s;">🧠</div>
    </div>

    <!-- Popup Modal -->
    <div class="modal-overlay" id="welcomeModal">
        <div class="modal-card">
            <button class="close-btn" onclick="closeModal()">✕</button>
            <div class="modal-title">الانحراف الفكري بالشريعة الإسلامية</div>
            <div class="verse-box">
                <div class="verse-text">« اهْدِنَا الصِّرَاطَ الْمُسْتَقِيمَ »</div>
                <div class="verse-label">سورة الفاتحة: آية 6</div>
            </div>
            <div class="developer-tag">
                طور بواسطة لمار السعود
            </div>
        </div>
    </div>

    <!-- Main Container -->
    <div class="container">
        <header>
            <h1>الانحراف الفكري بالشريعة الإسلامية</h1>
            <p>دراسة شرعية متكاملة ومستنبطة للمبادئ والأحكام</p>
        </header>

        <!-- Top Navigation -->
        <div class="nav-tabs">
            <button class="nav-btn active" onclick="switchTab('tab1', this)">✨ المحاور الشاملة</button>
            <button class="nav-btn" onclick="switchTab('tab2', this)">📖 الأدلة والمصادر</button>
            <button class="nav-btn" onclick="switchTab('tab3', this)">📝 الاختبار التفاعلي</button>
        </div>

        <!-- PAGE 1: Main Topics -->
        <div id="tab1" class="page-content active">
            
            <div class="accordion-item">
                <button class="accordion-header" onclick="toggleAccordion(this)">
                    <span>1. مفهوم الانحراف الفكري ومظاهره</span>
                    <span class="accordion-icon">✨</span>
                </button>
                <div class="accordion-body">
                    <p style="margin-bottom: 12px;"><strong>تعريف الانحراف الفكري:</strong> وهو الميل عن منهج الحق والعدول عن الصراط المستقيم، واعتناق أفكار غير سوية تؤدي إلى هدم معالم الدين والخلل بالأمن الفكري من خلال:</p>
                    <ul>
                        <li>اعتناق المذاهب والأفكار المنافية لثوابت الشريعة الإسلامية كالعلمانية والقومية.</li>
                        <li>انتقاص أحكام الإسلام والتكذيب أو الاعتقاد بعدم وجوب الحكم بما أنزل الله.</li>
                        <li>الطعن في صحابة رسول الله ﷺ وانتقاص منهج السلف الصالح.</li>
                        <li>التشكيك في مقومات الحضارة الإسلامية المترسخة والتهوين منها.</li>
                        <li>الفهم الخاطئ لبعض أركان ومفاهيم العقيدة كالقضاء والقدر والجماعة والولاء والبراء.</li>
                        <li>التشدد والغلو في الدين أو التفريط والجفاء عن سنن الوسطية.</li>
                    </ul>
                </div>
            </div>

            <div class="accordion-item">
                <button class="accordion-header" onclick="toggleAccordion(this)">
                    <span>2. أسباب ومسببات الانحراف الفكري</span>
                    <span class="accordion-icon">✨</span>
                </button>
                <div class="accordion-body">
                    <ul>
                        <li><strong>الجهل بمقاصد الشريعة:</strong> الفهم السطحي والأخذ بالمتشابهات وترك المحكمات بعيداً عن العلماء الراسخين.</li>
                        <li><strong>الانعزال الفكري والتحزب:</strong> التعصب لجماعة أو أفكار معينة دون الرجوع لمنهج الكتاب والسنة.</li>
                        <li><strong>الغزو الثقافي والشبهات:</strong> الانفتاح غير المضبط والتأثر بصفحات ومصادر مشبوهة.</li>
                        <li><strong>الفراغ الروحي والتربوي:</strong> ضعف الحصانة الذاتية وغياب التفكير الناقد الواعي.</li>
                    </ul>
                </div>
            </div>

            <div class="accordion-item">
                <button class="accordion-header" onclick="toggleAccordion(this)">
                    <span>3. الحصانة الفكرية والأمن الثقافي</span>
                    <span class="accordion-icon">✨</span>
                </button>
                <div class="accordion-body">
                    <ul>
                        <li><strong>نهي النبي ﷺ عن الغلو:</strong> موقف النبي ﷺ مع النفر الثلاثة الذين حاولوا التشدد بالصيام الدائم وقيام الليل واعتزال النساء، مؤكداً الاعتدال: «فمن رغب عن سنتي فليس مني».</li>
                        <li><strong>بناء الحصانة المبكرة:</strong> إحاطة الشباب بالمعالم العامة للدين وتعميق عقيدتهم للوقاية من الشبهات قبل الانفتاح على الأفكار الأخرى.</li>
                    </ul>
                </div>
            </div>

            <div class="accordion-item">
                <button class="accordion-header" onclick="toggleAccordion(this)">
                    <span>4. موقف الشريعة الإسلامية من الانحراف الفكري</span>
                    <span class="accordion-icon">✨</span>
                </button>
                <div class="accordion-body">
                    <ul>
                        <li><strong>موقف الشريعة الإسلامية من صحيفة التوراة:</strong> تذكير عمر بن الخطاب رضي الله عنه بطلب الهداية التامة من كتاب الله وسنة نبيه المصطفى ﷺ.</li>
                        <li><strong>تشجيع العلم والابتكار:</strong> الإسلام يحث على طلب العلوم النافعة والاستفادة من تجارب الأمم بما ينفع المجتمع.</li>
                        <li><strong>الأدلة الشرعية:</strong> قوله تعالى: ﴿وَقُل رَّبِّ زِدْنِي عِلْمًا﴾ [طه: 114]، وقوله ﷺ: «الحكمة ضالة المؤمن، فحيث وجدها فهو أحق بها».</li>
                    </ul>
                </div>
            </div>

        </div>

        <!-- PAGE 2: Sources & Evidence -->
        <div id="tab2" class="page-content">
            
            <div class="accordion-item">
                <button class="accordion-header" onclick="toggleAccordion(this)">
                    <span>📜 الأدلة الشرعية من القرآن الكريم</span>
                    <span class="accordion-icon">✨</span>
                </button>
                <div class="accordion-body">
                    <ul>
                        <li>قوله تعالى: ﴿اهْدِنَا الصِّرَاطَ الْمُسْتَقِيمَ﴾ [الفاتحة: 6] - دعاء دائم بالهداية والوسطية.</li>
                        <li>قوله تعالى: ﴿وَقُل رَّبِّ زِدْنِي عِلْمًا﴾ [طه: 114] - الحث على الاستزادة من العلم النافع.</li>
                        <li>قوله تعالى: ﴿يَا أَهْلَ الْكِتابِ لا تَغْلُوا فِي دِينِكُمْ﴾ [النساء: 171] - النهي الصريح عن الغلو والتشدد.</li>
                    </ul>
                </div>
            </div>

            <div class="accordion-item">
                <button class="accordion-header" onclick="toggleAccordion(this)">
                    <span>💬 حديث نبوي شريف في نبذ الغلو</span>
                    <span class="accordion-icon">✨</span>
                </button>
                <div class="accordion-body">
                    <p style="margin-bottom: 10px;">عن أنس بن مالك رضي الله عنه أن نفراً من أصحاب النبي ﷺ سألوا عن عمله في السر، فقال بعضهم: لا أتزوج النساء، وقال بعضهم: لا آكل اللحم، وقال بعضهم: لا أنام على فراش، فحمد الله وأثنى عليه وقال:</p>
                    <p style="color: var(--accent-yellow); font-weight: 700;">«ما بال أقوام قالوا كذا وكذا؟ لكني أصلي وأنام، وأصوم وأفطر، وأتزوج النساء، فمن رغب عن سنتي فليس مني» [صحيح البخاري ومسلم].</p>
                </div>
            </div>

            <div class="accordion-item">
                <button class="accordion-header" onclick="toggleAccordion(this)">
                    <span>📚 المراجع والمصادر العلمية</span>
                    <span class="accordion-icon">✨</span>
                </button>
                <div class="accordion-body">
                    <ul>
                        <li><strong>القرآن الكريم والتفاسير المعتمدة.</strong></li>
                        <li><strong>صحيح البخاري وصحيح مسلم:</strong> أبواب الاعتصام بالكتاب والسنة والترغيب في العلم.</li>
                        <li><strong>أبحاث ومطبوعات بناء المجتمع الإسلامي:</strong> دراسات الوقاية من الغلو والانحراف الفكري.</li>
                    </ul>
                </div>
            </div>

        </div>

        <!-- PAGE 3: Quiz -->
        <div id="tab3" class="page-content">
            
            <div class="quiz-card">
                <p>1. أي مما يلي يُعد من أبرز مظاهر الانحراف الفكري؟</p>
                <div class="options-grid">
                    <button class="option-btn" onclick="checkAnswer(this, false)">الاستفادة من العلوم والابتكارات الحديثة</button>
                    <button class="option-btn" onclick="checkAnswer(this, true)">الطعن في الصحابة والسلف والتشكيك في ثوابت الدين</button>
                    <button class="option-btn" onclick="checkAnswer(this, false)">سلوك منهج الوسطية والاعتدال</button>
                </div>
            </div>

            <div class="quiz-card">
                <p>2. كيف وجه النبي ﷺ النفر الذين أعلنوا التشديد والانقطاع عن الطيبات؟</p>
                <div class="options-grid">
                    <button class="option-btn" onclick="checkAnswer(this, true)">بين لهم أن سنته تقوم على الاعتدال وقال «فمن رغب عن سنتي فليس مني»</button>
                    <button class="option-btn" onclick="checkAnswer(this, false)">أمرهم بمواصلة التشدد والاعتزال</button>
                    <button class="option-btn" onclick="checkAnswer(this, false)">شجعهم على الانقطاع التام عن الحياة</button>
                </div>
            </div>

            <div class="quiz-card">
                <p>3. الدليل الذي يحث فيه القرآن الكريم على طلب العلم والاستزادة منه هو:</p>
                <div class="options-grid">
                    <button class="option-btn" onclick="checkAnswer(this, false)">﴿وَاعْتَصِمُوا بِحَبْلِ اللَّهِ جَمِيعًا﴾</button>
                    <button class="option-btn" onclick="checkAnswer(this, true)">﴿وَقُل رَّبِّ زِدْنِي عِلْمًا﴾</button>
                    <button class="option-btn" onclick="checkAnswer(this, false)">﴿إِنَّا أَنزَلْنَاهُ فِي لَيْلَةِ الْقَدْرِ﴾</button>
                </div>
            </div>

        </div>

        <!-- Footer -->
        <div class="footer-tag">
            طور بواسطة لمار السعود
        </div>
    </div>

    <script>
        function closeModal() {
            document.getElementById('welcomeModal').style.display = 'none';
        }

        function switchTab(tabId, btn) {
            document.querySelectorAll('.page-content').forEach(p => p.classList.remove('active'));
            document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
            
            document.getElementById(tabId).classList.add('active');
            btn.classList.add('active');
        }

        function toggleAccordion(headerBtn) {
            const body = headerBtn.nextElementSibling;
            const icon = headerBtn.querySelector('.accordion-icon');
            
            body.classList.toggle('open');
            if (body.classList.contains('open')) {
                icon.style.transform = 'scale(1.3)';
                icon.style.color = '#ffb300';
            } else {
                icon.style.transform = 'scale(1)';
                icon.style.color = '#f57c00';
            }
        }

        function checkAnswer(btn, isCorrect) {
            const parent = btn.parentElement;
            const buttons = parent.querySelectorAll('.option-btn');
            
            buttons.forEach(b => {
                b.disabled = true;
                b.style.cursor = 'default';
            });

            if (isCorrect) {
                btn.classList.add('correct');
            } else {
                btn.classList.add('wrong');
            }
        }
    </script>
</body>
</html>
