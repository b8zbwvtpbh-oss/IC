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
            background-image: radial-gradient(circle at 50% 0%, rgba(245, 124, 0, 0.25) 0%, rgba(230, 81, 0, 0.12) 35%, rgba(18, 18, 18, 0) 70%);
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
