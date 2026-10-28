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
            color: var(--text-white);
            line-height: 1.8;
            padding-bottom: 50px;
        }

        /* Modal / Popup */
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
            font-size: 1.4rem;
            font-weight: 700;
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

        /* Container & Header */
        .container {
            max-width: 850px;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            text-align: center;
            padding: 40px 0 20px;
            border-bottom: 1px solid var(--border-color);
            margin-bottom: 30px;
        }

        header h1 {
            color: var(--accent-yellow);
            font-size: 2.2rem;
            margin-bottom: 10px;
        }

        header p {
            color: var(--text-muted);
        }

        /* Sections */
        .section-card {
            background: var(--bg-card);
            border-radius: 12px;
            padding: 25px;
            margin-bottom: 25px;
            border: 1px solid var(--border-color);
        }

        .section-title {
            font-size: 1.3rem;
            color: var(--primary-orange);
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        ul {
            list-style: none;
            padding-right: 0;
        }

        li {
            position: relative;
            padding-right: 20px;
            margin-bottom: 12px;
            color: var(--text-white);
        }

        li::before {
            content: "•";
            color: var(--accent-yellow);
            font-size: 1.5rem;
            position: absolute;
            right: 0;
            top: -5px;
        }

        /* Accordion / Dropdown Sources */
        .accordion-btn {
            width: 100%;
            background: var(--bg-card);
            border: 1px solid var(--primary-orange);
            color: var(--accent-yellow);
            padding: 15px 20px;
            border-radius: 12px;
            font-size: 1.1rem;
            font-weight: 700;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: 0.3s;
            margin-top: 30px;
        }

        .accordion-btn:hover {
            background: rgba(245, 124, 0, 0.15);
        }

        .accordion-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.4s ease-out;
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-top: none;
            border-radius: 0 0 12px 12px;
            padding: 0 20px;
        }

        .accordion-content.open {
            padding: 20px;
            max-height: 500px;
        }

        /* Quiz Styling */
        .quiz-question {
            background: var(--bg-hover);
            border-radius: 8px;
            padding: 15px;
            margin-bottom: 15px;
        }

        .quiz-question p {
            font-weight: 700;
            margin-bottom: 10px;
            color: var(--accent-yellow);
        }

        .options-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 8px;
        }

        .option-btn {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            color: var(--text-white);
            padding: 10px 15px;
            border-radius: 6px;
            text-align: right;
            cursor: pointer;
            transition: 0.2s;
        }

        .option-btn:hover {
            border-color: var(--primary-orange);
            background: rgba(245, 124, 0, 0.05);
        }

        .option-btn.correct {
            background: #2e7d32 !important;
            border-color: #4caf50 !important;
            color: #fff;
        }

        .option-btn.wrong {
            background: #c62828 !important;
            border-color: #ef5350 !important;
            color: #fff;
        }

        .sources-card {
            text-align: center;
            margin-top: 30px;
            font-size: 0.95rem;
            color: var(--text-muted);
        }

        @media (max-width: 600px) {
            header h1 { font-size: 1.7rem; }
            .container { padding: 15px; }
        }
    </style>
</head>
<body>

    <!-- Popup Modal -->
    <div class="modal-overlay" id="welcomeModal">
        <div class="modal-card">
            <button class="close-btn" onclick="closeModal()">✕</button>
            <div class="modal-title">تذكير</div>
            <div class="verse-box">
                <div class="verse-text">« اهْدِنَا الصِّرَاطَ الْمُسْتَقِيمَ »</div>
                <div class="verse-label">سورة الفاتحة</div>
            </div>
            <div class="developer-tag">
                طور بواسطة لمار السعود
            </div>
        </div>
    </div>

    <!-- Main Content -->
    <div class="container">
        <header>
            <h1>الانحراف الفكري بالشريعة الإسلامية</h1>
            <p>دراسة شرعية تحليلية شاملة للمفهوم والأسباب والأحكام</p>
        </header>

        <!-- Section 1 -->
        <div class="section-card">
            <div class="section-title">📌 المفهوم الشامل والمظاهر</div>
            <p style="margin-bottom: 10px;"><strong>تعريف الانحراف الفكري:</strong> وهو الميل عن السوائية والعدول عن الصراط المستقيم وضوابط الدين القويم، مما يؤدي إلى تبني أفكار خاطئة تهدم معالم الدين وتخل بأمن المجتمع.</p>
            <ul>
                <li>اعتناق المذاهب والأفكار الهدامة المنافية لثوابت الشريعة كالقومية أو العلمانية.[span_0](start_span)[span_0](end_span)</li>
                <li>انتقاص أحكام الشريعة الإسلامية واعتقاد عدم وجوب التحتيم والعمل بما أنزل الله.[span_1](start_span)[span_1](end_span)</li>
                <li>الطعن في صحابة رسول الله ﷺ والتشكيك في منهج السلف الصالح والمؤسسات الفقهية الراسخة.[span_2](start_span)[span_2](end_span)</li>
                <li>التشكيك في مقومات الحضارة الإسلامية المترسخة والتهوين من قيمها.[span_3](start_span)[span_3](end_span)</li>
                <li>الفهم الخاطئ والتأويل العليل لبعض مفاهيم وأركان العقيدة كالقضاء والقدر والجماعة والولاء والبراء.[span_4](start_span)[span_4](end_span)</li>
                <li>التشدد والغلو في الدين أو الإفراط والتفريط والخروج عن منهج الوسطية والاعتدال.[span_5](start_span)[span_5](end_span)</li>
            </ul>
        </div>

        <!-- Section 2 -->
        <div class="section-card">
            <div class="section-title">📌 الأسباب العميقة للانحراف الفكري</div>
            <ul>
                <li><strong>الجهل بمقاصد الشريعة:</strong> الفهم السطحي للنصوص، والأخذ بالمتشابهات وترك المحكمات بمعزل عن فهم العلماء الراسخين.</li>
                <li><strong>عزلة المرجعية الشرعية:</strong> انقطاع الشباب عن العلماء الربانيين واستقاء الفتاوى والأفكار من منصات التواصل ومصادر مشبوهة.</li>
                <li><strong>الفراغ الفكري والروحي:</strong> غياب التحصين الذاتي وغياب التفكير الناقد يجعل الفرد صيداً سهلاً للتأثيرات الفكرية الخارجية.</li>
                <li><strong>الشبهات الإعلامية والغزو الثقافي:</strong> التأثر بالدعايات المضللة والتشكيك الثقافي بغير علم ولا هدى.</li>
            </ul>
        </div>

        <!-- Section 3 -->
        <div class="section-card">
            <div class="section-title">📌 الأمن الثقافي والحصانة الفكرية</div>
            <ul>
                <li><strong>رد النبي ﷺ على التشدد:</strong> أنكر النبي ﷺ على النفر الثلاثة الذين أعلنوا الغلو (أحدهم يصوم ولا يفطر، والثاني يقوم الليل دائماً، والثالث يعتزل النساء)، مؤكداً منهج الاعتدال: «فمن رغب عن سنتي فليس مني».[span_6](start_span)[span_6](end_span)</li>
                <li><strong>الحصانة الفكرية المبكرة:</strong> وجوب تحصين النشء والشباب بتعلم معالم الدين العامة والقواعد الكلية للإسلام قبل الانفتاح على الثقافات والأفكار الخارجية لضمان أمن العقول.[span_7](start_span)[span_7](end_span)[span_8](start_span)[span_8](end_span)</li>
            </ul>
        </div>

        <!-- Section 4 -->
        <div class="section-card">
            <div class="section-title">📌 موقف الشريعة من العلوم والابتكار النافع</div>
            <ul>
                <li><strong>قصة صحيفة التوراة:</strong> موقف النبي ﷺ حين رأى مع عمر بن الخطاب رضي الله عنه صحيفة من التوراة، موضحاً كفاية وكمال القرآن والسنة الشريفة في هداية البشرية.[span_9](start_span)[span_9](end_span)</li>
                <li><strong>الانفتاح المعرفي النافع:</strong> الشريعة لا ترفض العلوم النافعة أو التطور والابتكار الثقافي البناء بل تحث عليه.[span_10](start_span)[span_10](end_span)</li>
                <li><strong>الدليل القرآني:</strong> قوله تعالى: ﴿وَقُل رَّبِّ زِدْنِي عِلْمًا﴾ [طه: 114].[span_11](start_span)[span_11](end_span)</li>
                <li><strong>الدليل من السنة:</strong> قوله ﷺ: «الحكمة ضالة المؤمن، فحيث وجدها فهو أحق بها».[span_12](start_span)[span_12](end_span)</li>
            </ul>
        </div>

        <!-- Quiz Section -->
        <div class="section-card">
            <div class="section-title">📝 أسئلة تفاعلية وتقييم فهم</div>
            
            <div class="quiz-question">
                <p>1. ما هو المعيار الشرعي الأساسي لمعرفة الانحراف الفكري؟</p>
                <div class="options-grid">
                    <button class="option-btn" onclick="checkAnswer(this, false)">مخالفة الآراء الشخصية للمجتمع</button>
                    <button class="option-btn" onclick="checkAnswer(this, true)">الخروج والعدول عن منهج الوسطية والاعتدال وما جاء به الشرع الحنيف</button>
                    <button class="option-btn" onclick="checkAnswer(this, false)">التعلم من التجارب والعلوم النافعة</button>
                </div>
            </div>

            <div class="quiz-question">
                <p>2. كيف عالج السنة النبوية الشريفة غلو النفر الثلاثة الذين حاولوا التشديد على أنفسهم؟</p>
                <div class="options-grid">
                    <button class="option-btn" onclick="checkAnswer(this, true)">أقر النبي ﷺ منهج الوسطية والاعتدال وقال: «فمن رغب عن سنتي فليس مني»</button>
                    <button class="option-btn" onclick="checkAnswer(this, false)">شجعهم على مواصلة الانقطاع والشدة</button>
                    <button class="option-btn" onclick="checkAnswer(this, false)">أمرهم بالتوقف عن العبادة نهائياً</button>
                </div>
            </div>

            <div class="quiz-question">
                <p>3. الشريعة الإسلامية تحث على التعلم والانفتاح على العلوم النافعة والدليل قوله تعالى:</p>
                <div class="options-grid">
                    <button class="option-btn" onclick="checkAnswer(this, false)">﴿وَاعْتَصِمُوا بِحَبْلِ اللَّهِ جَمِيعًا﴾</button>
                    <button class="option-btn" onclick="checkAnswer(this, true)">﴿وَقُل رَّبِّ زِدْنِي عِلْمًا﴾</button>
                    <button class="option-btn" onclick="checkAnswer(this, false)">﴿إِنَّمَا يَخْشَى اللَّهَ مِنْ عِبَادِهِ الْعُلَمَاءُ﴾</button>
                </div>
            </div>
        </div>

        <!-- Dropdown Sources Button -->
        <button class="accordion-btn" onclick="toggleSources()">
            <span>📚 المراجع والمصادر العلمية المعتمدة</span>
            <span id="accordionIcon">▼</span>
        </button>

        <div class="accordion-content" id="sourcesDropdown">
            <ul>
                <li><strong>القرآن الكريم</strong> وكتب التفسير المعتمدة.[span_13](start_span)[span_13](end_span)</li>
                <li><strong>صحيح البخاري وصحيح مسلم:</strong> أحاديث النهي عن الغلو واجتناب الشبهات والترغيب في طلب العلم.[span_14](start_span)[span_14](end_span)[span_15](start_span)[span_15](end_span)</li>
                <li><strong>دراسات الفقه والسياسة الشرعية:</strong> أسباب الانحراف الفكري وعلاجه الشامل في الإسلام (دراسة شرعية تحليلية).</li>
                <li><strong>أبحاث الأمن الفكري:</strong> المنهج النبوي في معالجة الانحراف الفكري وحماية الشباب (مجلة الجامعة العراقية).</li>
                <li><strong>بحوث ومؤلفات علماء المسلمين:</strong> كتب الاقتصاد والفكر وبناء المجتمع الإسلامي.[span_16](start_span)[span_16](end_span)[span_17](start_span)[span_17](end_span)[span_18](start_span)[span_18](end_span)</li>
            </ul>
        </div>

        <div class="sources-card">
            <p>تم الإعداد والتطوير بواسطة: <strong>لمار السعود</strong></p>
        </div>
    </div>

    <script>
        function closeModal() {
            document.getElementById('welcomeModal').style.display = 'none';
        }

        function toggleSources() {
            const content = document.getElementById('sourcesDropdown');
            const icon = document.getElementById('accordionIcon');
            content.classList.toggle('open');
            
            if (content.classList.contains('open')) {
                icon.innerText = '▲';
            } else {
                icon.innerText = '▼';
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
