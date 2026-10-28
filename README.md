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
            line-height: 1.7;
            padding-bottom: 50px;
        }

        /* Modal / Popup */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.85);
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
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
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
            background: var(--bg-card);
            border-radius: 12px;
            padding: 20px;
            text-align: center;
            border: 1px solid var(--border-color);
            margin-top: 40px;
            font-size: 0.9rem;
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
            <p>دراسة ومفاهيم مستنبطة من المنهج الشرعي</p>
        </header>

        <!-- Section 1 -->
        <div class="section-card">
            <div class="section-title">📌 المفهوم والمظاهر (صفحة 72)</div>
            <p style="margin-bottom: 10px;"><strong>تعريف الانحراف الفكري:</strong> وهو أصل كل انحراف، حيث يعتنق الشباب أفكاراً غير سوية تهدم معالم الدين.</p>
            <ul>
                <li>اعتناق المذاهب الهدامة كالعلمانية والقومية.[span_0](start_span)[span_0](end_span)</li>
                <li>انتقاص أحكام الإسلام واعتقاد عدم وجوب الحكم بما أنزل الله.[span_1](start_span)[span_1](end_span)</li>
                <li>انتقاص الصحابة والسلف الصالح والطعن فيهم.[span_2](start_span)[span_2](end_span)</li>
                <li>التشكيك في الحضارة الإسلامية ومقوماتها.[span_3](start_span)[span_3](end_span)</li>
                <li>الفهم الخاطئ لبعض المفاهيم الشرعية كالقضاء والقدر.[span_4](start_span)[span_4](end_span)</li>
                <li>التشدد والغلو في الأخذ بتعاليم الدين وأحكامه.[span_5](start_span)[span_5](end_span)</li>
            </ul>
        </div>

        <!-- Section 2 -->
        <div class="section-card">
            <div class="section-title">📌 الأمن الثقافي والحصانة (صفحة 84)</div>
            <ul>
                <li><strong>موقف النبي ﷺ من الغلو:</strong> رد النبي ﷺ على النفر الثلاثة الذين أعلنوا التشدد (أحدهم يصوم ولا يفطر، والآخر يصلي الليل دائماً، والثالث يعتزل النساء)، موضحاً أن سنته تقوم على الاعتدال والوسطية: "فمن رغب عن سنتي فليس مني".[span_6](start_span)[span_6](end_span)</li>
                <li><strong>الحصانة الفكرية:</strong> ضرورة بناء حصانة للشباب توعيهم بالمعالم العامة للدين قبل التعمق في الثقافات والأفكار غير الإسلامية لتعصمهم من الانزلاق.[span_7](start_span)[span_7](end_span)[span_8](start_span)[span_8](end_span)</li>
            </ul>
        </div>

        <!-- Section 3 -->
        <div class="section-card">
            <div class="section-title">📌 موقف الشريعة من العلوم والابتكار (صفحة 85)</div>
            <ul>
                <li><strong>قصة صحيفة التوراة:</strong> موقف النبي ﷺ حين رأى مع عمر بن الخطاب رضي الله عنه صحيفة من التوراة، فبين له أن الكفاية والكمال فيما جاء به القرآن والسنة.[span_9](start_span)[span_9](end_span)</li>
                <li><strong>الانفتاح النافع:</strong> الإسلام لا يمنع من الابتكار والتجديد والاستفادة من العلوم النافعة لدى الثقافات الأخرى.[span_10](start_span)[span_10](end_span)</li>
                <li><strong>الدليل من القرآن:</strong> قوله تعالى: ﴿وَقُل رَّبِّ زِدْنِي عِلْمًا﴾ [طه: 114].[span_11](start_span)[span_11](end_span)</li>
                <li><strong>الدليل من السنة:</strong> قوله ﷺ: "الحكمة ضالة المؤمن، فحيث وجدها فهو أحق بها".[span_12](start_span)[span_12](end_span)</li>
            </ul>
        </div>

        <!-- Quiz Section -->
        <div class="section-card">
            <div class="section-title">📝 أسئلة تفاعلية استيعابية</div>
            
            <div class="quiz-question">
                <p>1. أي مما يلي يُعد من مظاهر الانحراف الفكري المذكورة في ص 72؟</p>
                <div class="options-grid">
                    <button class="option-btn" onclick="checkAnswer(this, false)">تعلم العلوم الحديثة والنافعة</button>
                    <button class="option-btn" onclick="checkAnswer(this, true)">انتقاص الصحابة والسلف الصالح والتشكيك بالحضارة</button>
                    <button class="option-btn" onclick="checkAnswer(this, false)">الأخذ بالوسطية والاعتدال</button>
                </div>
            </div>

            <div class="quiz-question">
                <p>2. كيف كان موقف النبي ﷺ مع النفر الثلاثة الذين أرادوا التشدد؟ (ص 84)</p>
                <div class="options-grid">
                    <button class="option-btn" onclick="checkAnswer(this, true)">أنكر عليهم وبين أن سنته هي الاعتدال والوسطية</button>
                    <button class="option-btn" onclick="checkAnswer(this, false)">وافقهم على أفعالهم وشجعهم</button>
                    <button class="option-btn" onclick="checkAnswer(this, false)">طلب منهم الاعتزال التام عن الناس</button>
                </div>
            </div>

            <div class="quiz-question">
                <p>3. الآية التي استُدل بها على طلب العلم النافع والزيادة فيه هي: (ص 85)</p>
                <div class="options-grid">
                    <button class="option-btn" onclick="checkAnswer(this, false)">﴿وَاعْتَصِمُوا بِحَبْلِ اللَّهِ جَمِيعًا﴾</button>
                    <button class="option-btn" onclick="checkAnswer(this, true)">﴿وَقُل رَّبِّ زِدْنِي عِلْمًا﴾</button>
                    <button class="option-btn" onclick="checkAnswer(this, false)">﴿اقْرَأْ بِاسْمِ رَبِّكَ الَّذِي خَلَقَ﴾</button>
                </div>
            </div>
        </div>

        <!-- Sources Card -->
        <div class="sources-card">
            <p><strong>المصادر والمراجع:</strong> المحتوى والأدلة مستخرجة ومطابقة للمنهج الدراسي (الصفحات: 72، 84، 85)[span_13](start_span)[span_13](end_span)[span_14](start_span)[span_14](end_span)[span_15](start_span)[span_15](end_span)</p>
            <p style="margin-top: 8px;">إعداد وتطوير: <strong>لمار السعود</strong></p>
        </div>
    </div>

    <script>
        function closeModal() {
            document.getElementById('welcomeModal').style.display = 'none';
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
