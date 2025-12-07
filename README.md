<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="اختبار الرخصة المهنية التفاعلي للمعلمين - إعداد المعلم فهد الخالدي">
<link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700;800&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<style>
/* الأنماط الأساسية تبقى كما كانت */
:root {
    --primary: #6C63FF;
    --primary-light: #9D95FF;
    --primary-dark: #4A42CC;
    --secondary: #FF6B8B;
    --secondary-light: #FF9EB5;
    --secondary-dark: #FF3D6A;
    --accent: #36D1DC;
    --accent-light: #6CE8F0;
    --accent-dark: #1FB9C5;
    --success: #00D09C;
    --success-light: #4DFFD6;
    --success-dark: #00A67C;
    --warning: #FFB74D;
    --warning-light: #FFD18A;
    --warning-dark: #FF9800;
    --danger: #FF5252;
    --danger-light: #FF8A80;
    --danger-dark: #D32F2F;
    --info: #42A5F5;
    --info-light: #80D6FF;
    --info-dark: #1976D2;
    
    --primary-gradient: linear-gradient(135deg, var(--primary) 0%, #9D4FFF 50%, var(--accent) 100%);
    --secondary-gradient: linear-gradient(135deg, var(--secondary) 0%, #FF8E6B 50%, #FFD166 100%);
    --accent-gradient: linear-gradient(135deg, var(--accent) 0%, #5A67FF 50%, var(--primary) 100%);
    --success-gradient: linear-gradient(135deg, var(--success) 0%, #00E5FF 50%, #00FFB3 100%);
    --warning-gradient: linear-gradient(135deg, var(--warning) 0%, #FF8A65 50%, #FFD54F 100%);
    --danger-gradient: linear-gradient(135deg, var(--danger) 0%, #FF8A80 50%, #FF5252 100%);
    --info-gradient: linear-gradient(135deg, var(--info) 0%, #42A5F5 50%, #2979FF 100%);
    --finish-gradient: linear-gradient(135deg, #FF5252 0%, #D32F2F 50%, #B71C1C 100%);
    
    --bg: linear-gradient(135deg, #0F0C29 0%, #302B63 25%, #24243E 50%, #302B63 75%, #0F0C29 100%);
    --card-bg: rgba(255, 255, 255, 0.12);
    --text: #FFFFFF;
    --light-text: #E0E0E0;
    --border: rgba(255, 255, 255, 0.15);
    --shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
    --shadow-hover: 0 25px 60px rgba(0, 0, 0, 0.4);
}

* {
    box-sizing: border-box;
    font-family: 'Tajawal', Tahoma, Arial, sans-serif;
    margin: 0;
    padding: 0;
}

body {
    background: var(--bg);
    color: var(--text);
    line-height: 1.7;
    overflow-x: hidden;
    padding-top: 70px;
    transition: all 0.5s ease;
    min-height: 100vh;
    background-attachment: fixed;
}

/* Header - تم تصغيره */
header {
    background: rgba(108, 99, 255, 0.15);
    backdrop-filter: blur(25px);
    color: white;
    position: fixed;
    top: 0;
    width: 100%;
    z-index: 1000;
    box-shadow: var(--shadow);
    border-bottom: 1px solid var(--border);
    padding: 10px 0;
    height: 70px;
}

.header-container {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 20px;
    height: 50px;
}

.title-section h1 {
    font-size: 1.3rem;
    font-weight: 800;
    background: var(--primary-gradient);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    line-height: 1.2;
}

.header-actions {
    display: flex;
    gap: 8px;
    flex-wrap: nowrap;
    align-items: center;
}

.translate-btn, .theme-btn, .back-btn, .whatsapp-btn {
    background: rgba(108, 99, 255, 0.25);
    color: white;
    border: 1px solid rgba(255, 255, 255, 0.2);
    padding: 6px 12px;
    border-radius: 10px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s ease;
    display: flex;
    align-items: center;
    gap: 5px;
    backdrop-filter: blur(20px);
    text-decoration: none;
    font-size: 0.8rem;
    height: 36px;
    white-space: nowrap;
}

.translate-btn:hover, .theme-btn:hover, .back-btn:hover, .whatsapp-btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
}

/* زر الترجمة */
.translate-btn {
    background: linear-gradient(135deg, #4CAF50 0%, #2E7D32 100%);
}

.translate-btn:hover {
    background: linear-gradient(135deg, #2E7D32 0%, #1B5E20 100%);
}

/* زر الواتساب المعدل */
.whatsapp-btn {
    background: linear-gradient(135deg, #25D366 0%, #128C7E 100%);
}

.whatsapp-btn:hover {
    background: linear-gradient(135deg, #128C7E 0%, #075E54 100%);
}

/* زر التحول بين الوضع الليلي والنهاري */
.theme-btn {
    position: relative;
    min-width: 40px;
    width: 40px;
    justify-content: center;
    padding: 6px;
}

.theme-btn .theme-text {
    display: none;
}

.theme-btn i {
    font-size: 1rem;
}

/* Main Content */
main {
    max-width: 1000px;
    margin: 30px auto;
    padding: 0 20px;
}

/* Hero Section */
.hero-section {
    background: linear-gradient(135deg, rgba(108, 99, 255, 0.2), rgba(255, 107, 139, 0.2));
    backdrop-filter: blur(35px);
    color: white;
    border-radius: 25px;
    padding: 50px 40px;
    margin-bottom: 40px;
    text-align: center;
    position: relative;
    overflow: hidden;
    box-shadow: 0 25px 70px rgba(108, 99, 255, 0.2);
}

.hero-title {
    font-size: 2.5rem;
    font-weight: 800;
    margin-bottom: 20px;
    background: linear-gradient(135deg, #fff 0%, #FF9EB5 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}

.hero-subtitle {
    font-size: 1.2rem;
    margin-bottom: 30px;
    opacity: 0.9;
    max-width: 700px;
    margin-left: auto;
    margin-right: auto;
    line-height: 1.8;
}

/* Card */
.card {
    background: rgba(255, 255, 255, 0.08);
    backdrop-filter: blur(35px);
    border-radius: 25px;
    padding: 40px;
    margin-bottom: 30px;
    box-shadow: 0 20px 50px rgba(0, 0, 0, 0.2);
    transition: all 0.4s ease;
    border: 1px solid rgba(255, 255, 255, 0.1);
    position: relative;
    overflow: hidden;
}

.card::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 6px;
    background: var(--primary-gradient);
}

/* View Mode Selector */
.view-mode-selector {
    background: rgba(255, 255, 255, 0.08);
    backdrop-filter: blur(35px);
    border-radius: 20px;
    padding: 30px;
    margin-bottom: 30px;
    text-align: center;
    border: 1px solid rgba(255, 255, 255, 0.1);
}

.view-mode-title {
    font-size: 1.4rem;
    margin-bottom: 20px;
    color: var(--text);
}

.view-mode-buttons {
    display: flex;
    gap: 20px;
    justify-content: center;
    flex-wrap: wrap;
}

.view-mode-btn {
    background: var(--card-bg);
    border: 2px solid var(--border);
    color: var(--text);
    padding: 15px 30px;
    border-radius: 15px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s ease;
    display: flex;
    align-items: center;
    gap: 10px;
    min-width: 200px;
    justify-content: center;
}

.view-mode-btn:hover {
    border-color: var(--primary);
    transform: translateY(-3px);
}

.view-mode-btn.active {
    background: var(--primary-gradient);
    border-color: transparent;
    color: white;
}

/* Question Box */
.question-box {
    background: var(--card-bg);
    backdrop-filter: blur(25px);
    padding: 35px;
    margin-bottom: 30px;
    border-radius: 25px;
    box-shadow: var(--shadow);
    border: 1px solid var(--border);
    transition: all 0.4s ease;
    position: relative;
}

.question-number {
    font-size: 1.4em;
    color: var(--primary-light);
    margin-bottom: 20px;
    font-weight: bold;
    display: flex;
    align-items: center;
    gap: 12px;
}

.question-text {
    font-size: 1.3em;
    margin-bottom: 30px;
    line-height: 1.8;
    color: var(--text);
    font-weight: 500;
}

/* Options */
.options {
    position: relative;
}

.options label {
    display: flex;
    align-items: center;
    padding: 20px 25px;
    margin: 15px 0;
    border: 2px solid var(--border);
    border-radius: 18px;
    cursor: pointer;
    transition: all 0.3s ease;
    background: rgba(255, 255, 255, 0.05);
    position: relative;
    overflow: hidden;
    font-weight: 500;
}

.options label:hover:not(.locked) {
    border-color: var(--primary);
    transform: translateX(-10px);
}

.options input[type="radio"] {
    margin-left: 15px;
    transform: scale(1.4);
}

.options label.selected {
    background: linear-gradient(135deg, rgba(108, 99, 255, 0.2), rgba(157, 79, 255, 0.2));
    border: 2px solid var(--primary);
}

.options label.correct-answer {
    background: linear-gradient(135deg, rgba(0, 208, 156, 0.25), rgba(0, 229, 255, 0.25));
    border: 2px solid var(--success);
}

.options label.wrong-answer {
    background: linear-gradient(135deg, rgba(255, 107, 139, 0.25), rgba(255, 142, 107, 0.25));
    border: 2px solid var(--secondary);
}

/* Buttons */
.btn {
    padding: 18px 35px;
    border-radius: 18px;
    font-weight: 700;
    text-decoration: none;
    transition: all 0.3s ease;
    display: inline-flex;
    align-items: center;
    gap: 12px;
    font-size: 1.1rem;
    border: none;
    cursor: pointer;
    position: relative;
    overflow: hidden;
}

.btn-primary {
    background: var(--primary-gradient);
    color: white;
    box-shadow: 0 10px 30px rgba(108, 99, 255, 0.4);
}

.btn-secondary {
    background: var(--secondary-gradient);
    color: white;
    box-shadow: 0 10px 30px rgba(255, 107, 139, 0.4);
}

.btn-success {
    background: var(--success-gradient);
    color: white;
    box-shadow: 0 10px 30px rgba(0, 208, 156, 0.4);
}

.btn-warning {
    background: var(--warning-gradient);
    color: white;
    box-shadow: 0 10px 30px rgba(255, 183, 77, 0.4);
}

.btn-danger {
    background: var(--danger-gradient);
    color: white;
    box-shadow: 0 10px 30px rgba(255, 82, 82, 0.4);
}

.btn-info {
    background: var(--info-gradient);
    color: white;
    box-shadow: 0 10px 30px rgba(66, 165, 245, 0.4);
}

.btn-finish {
    background: var(--finish-gradient);
    color: white;
    box-shadow: 0 10px 30px rgba(255, 82, 82, 0.4);
}

.btn:hover {
    transform: translateY(-5px);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
}

/* Progress Bar */
.progress-bar {
    height: 18px;
    background: rgba(255, 255, 255, 0.15);
    border-radius: 12px;
    margin-bottom: 40px;
    overflow: hidden;
    box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.2);
    position: relative;
}

.progress {
    height: 100%;
    background: var(--primary-gradient);
    box-shadow: 0 0 20px rgba(108, 99, 255, 0.5);
    width: 0%;
    transition: width 0.5s ease;
    border-radius: 12px;
}

/* Navigation */
.navigation {
    display: flex;
    justify-content: space-between;
    margin-top: 40px;
    gap: 25px;
}

/* Question Action Buttons */
.question-actions {
    display: flex;
    gap: 15px;
    margin-top: 30px;
    flex-wrap: wrap;
}

.action-btn {
    padding: 12px 25px;
    border-radius: 12px;
    font-weight: 600;
    border: none;
    cursor: pointer;
    transition: all 0.3s ease;
    display: flex;
    align-items: center;
    gap: 8px;
}

.feedback-btn {
    background: var(--info-gradient);
    color: white;
}

.remove-options-btn {
    background: linear-gradient(135deg, #FF9800 0%, #FF5722 100%);
    color: white;
}

/* زر التلميح الجديد */
.hint-btn {
    background: linear-gradient(135deg, #9C27B0 0%, #673AB7 100%);
    color: white;
}

/* Explanation */
.explanation {
    margin-top: 30px;
    padding: 30px;
    border-radius: 20px;
    display: none;
    background: linear-gradient(135deg, rgba(108, 99, 255, 0.1), rgba(54, 209, 220, 0.1));
    border-left: 5px solid var(--success);
}

.explanation.show {
    display: block;
    animation: fadeIn 0.5s ease;
}

/* Hint Box */
.hint-box {
    margin-top: 20px;
    padding: 25px;
    border-radius: 20px;
    display: none;
    background: linear-gradient(135deg, rgba(156, 39, 176, 0.1), rgba(103, 58, 183, 0.1));
    border-left: 5px solid #9C27B0;
    border-right: 5px solid #9C27B0;
    animation: fadeIn 0.5s ease;
}

.hint-box.show {
    display: block;
}

.hint-box i {
    color: #9C27B0;
    margin-left: 10px;
}

@keyframes fadeIn {
    from { opacity: 0; transform: translateY(-10px); }
    to { opacity: 1; transform: translateY(0); }
}

/* Controls */
.controls {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 40px;
    flex-wrap: wrap;
    gap: 25px;
}

.quiz-info {
    font-size: 1.1rem;
    color: var(--light-text);
    background: linear-gradient(135deg, rgba(108, 99, 255, 0.15), rgba(255, 107, 139, 0.15));
    padding: 12px 25px;
    border-radius: 30px;
    font-weight: 600;
}

#timer {
    font-size: 1.2rem;
    font-weight: bold;
    color: white;
    display: flex;
    align-items: center;
    gap: 10px;
    background: rgba(54, 209, 220, 0.25);
    padding: 12px 25px;
    border-radius: 30px;
    border: 2px solid rgba(54, 209, 220, 0.3);
}

/* Message Box */
.message-box {
    margin-top: 20px;
    padding: 20px;
    border-radius: 15px;
    background: linear-gradient(135deg, rgba(255, 193, 7, 0.1), rgba(255, 235, 59, 0.1));
    border: 2px solid var(--warning);
    display: none;
    animation: fadeIn 0.5s ease;
}

.message-box.show {
    display: block;
}

.message-box i {
    color: var(--warning);
    margin-left: 10px;
}

/* Questions Modal */
.overlay {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.7);
    z-index: 2000;
    backdrop-filter: blur(5px);
}

.questions-modal {
    display: none;
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 90%;
    max-width: 700px;
    max-height: 80vh;
    overflow-y: auto;
    background: var(--card-bg);
    backdrop-filter: blur(35px);
    border-radius: 25px;
    padding: 30px;
    box-shadow: 0 25px 60px rgba(0, 0, 0, 0.4);
    border: 1px solid var(--border);
    z-index: 2001;
    animation: modalFadeIn 0.3s ease;
}

@keyframes modalFadeIn {
    from { opacity: 0; transform: translate(-50%, -60%); }
    to { opacity: 1; transform: translate(-50%, -50%); }
}

.modal-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 25px;
    padding-bottom: 15px;
    border-bottom: 2px solid var(--border);
}

.modal-title {
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--text);
    display: flex;
    align-items: center;
    gap: 12px;
}

.close-modal {
    background: var(--danger-gradient);
    color: white;
    border: none;
    width: 40px;
    height: 40px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    font-size: 1.2rem;
    transition: all 0.3s ease;
}

.close-modal:hover {
    transform: rotate(90deg) scale(1.1);
}

.questions-grid-modal {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(60px, 1fr));
    gap: 12px;
    margin: 20px 0;
    padding: 10px;
}

.question-status-grid-modal {
    width: 60px;
    height: 60px;
    border: 2px solid var(--border);
    border-radius: 15px;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    font-weight: 700;
    transition: all 0.3s ease;
    background: var(--card-bg);
    font-size: 1.1rem;
}

.question-status-grid-modal:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(108, 99, 255, 0.3);
}

.question-status-grid-modal.current {
    background: var(--primary-gradient);
    border-color: transparent;
    box-shadow: 0 0 20px rgba(108, 99, 255, 0.5);
}

.question-status-grid-modal.answered {
    background: var(--success-gradient);
    border-color: transparent;
}

.question-status-grid-modal.marked {
    background: var(--warning-gradient);
    border-color: transparent;
}

.question-status-grid-modal.locked {
    cursor: not-allowed;
    opacity: 0.7;
}

/* Responsive */
@media (max-width: 768px) {
    body {
        padding-top: 70px;
    }
    
    .header-container {
        flex-direction: column;
        gap: 10px;
        text-align: center;
        height: auto;
        padding: 5px 10px;
    }
    
    header {
        height: auto;
        padding: 8px 0;
    }
    
    .title-section h1 {
        font-size: 1.1rem;
    }
    
    .hero-title {
        font-size: 2rem;
    }
    
    .hero-subtitle {
        font-size: 1.1rem;
    }
    
    .view-mode-buttons {
        flex-direction: column;
    }
    
    .view-mode-btn {
        min-width: 100%;
    }
    
    .navigation {
        flex-direction: column;
    }
    
    .btn {
        width: 100%;
        justify-content: center;
    }
    
    .controls {
        flex-direction: column;
        align-items: stretch;
    }
    
    .translate-btn, .theme-btn, .whatsapp-btn, .back-btn {
        padding: 5px 10px;
        font-size: 0.75rem;
        height: 32px;
    }
    
    .theme-btn {
        min-width: 32px;
        width: 32px;
    }
    
    .question-actions {
        flex-direction: column;
    }
    
    .action-btn {
        width: 100%;
        justify-content: center;
    }
    
    .questions-grid-modal {
        grid-template-columns: repeat(auto-fill, minmax(50px, 1fr));
        gap: 10px;
    }
    
    .question-status-grid-modal {
        width: 50px;
        height: 50px;
        font-size: 1rem;
    }
}

/* الوضع الداكن */
.dark-theme {
    --bg: linear-gradient(135deg, #0A0A1A 0%, #1A1A3E 50%, #0A0A1A 100%);
    --card-bg: rgba(26, 26, 62, 0.8);
    --text: #F0F0F0;
    --light-text: #C0C0C0;
    --border: rgba(255, 255, 255, 0.1);
}

.dark-theme .theme-btn {
    background: rgba(255, 193, 7, 0.25);
}

.dark-theme .whatsapp-btn {
    background: linear-gradient(135deg, #075E54 0%, #128C7E 100%);
}

/* تحسينات إضافية للهيدر */
.header-actions .translate-btn span,
.header-actions .whatsapp-btn span,
.header-actions .back-btn span {
    display: none;
}

@media (min-width: 992px) {
    .header-actions .translate-btn span,
    .header-actions .whatsapp-btn span,
    .header-actions .back-btn span {
        display: inline;
    }
    
    .header-actions .translate-btn,
    .header-actions .whatsapp-btn,
    .header-actions .back-btn {
        padding: 6px 15px;
    }
}
</style>
</head>
<body>
<!-- Header -->
<header class="glass-effect">
    <div class="header-container">
        <div class="title-section">
            <h1>English Teaching Professional License Simulator</h1>
        </div>
        <div class="header-actions">
            <button class="translate-btn" id="translateBtn" title="ترجمة التلميحات">
                <i class="fas fa-language"></i>
                <span class="translate-text">ترجمة</span>
            </button>
            <button class="theme-btn" id="themeBtn" title="الوضع الليلي/النهاري">
                <i class="fas fa-moon"></i>
            </button>
            <button class="whatsapp-btn" id="whatsappBtn" title="للملاحظات والأخطاء">
                <i class="fab fa-whatsapp"></i>
                <span>ملاحظات</span>
            </button>
            <a href="#" class="back-btn" title="العودة للرئيسية">
                <i class="fas fa-arrow-right"></i>
                <span>رئيسية</span>
            </a>
        </div>
    </div>
</header>

<!-- Main Content -->
<main>
    <!-- Hero Section -->
    <section class="hero-section">
        <div class="hero-content">
            <h1 class="hero-title">اختبار الرخصة المهنية للمعلمين</h1>
            <p class="hero-subtitle">تم إعداد هذا الاختبار التفاعلي لمحاكاة الاختبار الرسمي للرخصة المهنية، ويقدم تغذية راجعة فورية لجميع الإجابات</p>
            <div class="quiz-info">إعداد: المعلم فهد الخالدي</div>
        </div>
    </section>

    <!-- Progress Bar -->
    <div class="progress-bar">
        <div class="progress" id="progress"></div>
    </div>

    <!-- View Mode Selector -->
    <div class="view-mode-selector" id="viewModeSelector">
        <h3 class="view-mode-title">اختر طريقة عرض الأسئلة:</h3>
        <div class="view-mode-buttons">
            <button class="view-mode-btn active" onclick="setViewMode('single')">
                <i class="fas fa-file-alt"></i>
                سؤال واحد في الصفحة
                <small>(العرض الافتراضي)</small>
            </button>
            <button class="view-mode-btn" onclick="setViewMode('multi')">
                <i class="fas fa-th-large"></i>
                5 أسئلة في الصفحة
                <small>(للمراجعة السريعة)</small>
            </button>
        </div>
    </div>

    <!-- Quiz Container -->
    <div id="quiz"></div>

    <!-- Controls -->
    <div class="controls">
        <div class="quiz-info" id="quiz-info"></div>
        <div id="timer">⏱️ <span id="time-display">45:00</span></div>
        <div style="display: flex; gap: 15px; flex-wrap: wrap;">
            <button class="btn btn-primary" onclick="showQuestionsList()">
                <i class="fas fa-list"></i>
                قائمة الأسئلة
            </button>
            <button class="btn btn-warning" onclick="toggleMarkForReview()" id="mark-review-btn">
                <i class="fas fa-flag"></i>
                وضع علامة للمراجعة
            </button>
            <button class="btn btn-finish" onclick="finishQuiz()">
                <i class="fas fa-flag-checkered"></i>
                إنهاء الاختبار
            </button>
            <button class="btn btn-secondary" onclick="showCurrentScore()">
                <i class="fas fa-chart-bar"></i>
                عرض الدرجات الحالية
            </button>
        </div>
    </div>

    <!-- Current Score -->
    <div id="current-score" class="card" style="display: none;">
        <h3 style="color: var(--text); margin-bottom: 20px; display: flex; align-items: center; gap: 12px;">
            <i class="fas fa-chart-bar"></i>
            الدرجات الحالية
        </h3>
        <p id="current-correct" style="margin-bottom: 15px; font-size: 1.1rem;"></p>
        <p id="current-percentage" style="font-weight: bold; font-size: 1.3rem; color: var(--accent);"></p>
    </div>

    <!-- Final Results -->
    <div id="result-box" class="card" style="display: none;">
        <h3 id="result" style="color: var(--text); margin-bottom: 20px;"></h3>
        <p id="percentage" style="font-size: 1.4rem; margin-bottom: 15px;"></p>
        <p id="evaluation" style="font-weight: bold; font-size: 1.3rem;"></p>
    </div>
</main>

<!-- Questions List Modal -->
<div id="questions-overlay" class="overlay" onclick="hideQuestionsList()"></div>
<div id="questions-modal" class="questions-modal">
    <div class="modal-header">
        <h3 class="modal-title">
            <i class="fas fa-th-list"></i>
            قائمة الأسئلة
        </h3>
        <button class="close-modal" onclick="hideQuestionsList()">
            <i class="fas fa-times"></i>
        </button>
    </div>
    <div id="questions-grid-modal" class="questions-grid-modal"></div>
    <div style="display: flex; flex-wrap: wrap; gap: 15px; margin-top: 20px; justify-content: center;">
        <div style="display: flex; align-items: center; gap: 8px;">
            <div class="question-status-grid-modal" style="background: var(--primary-gradient);"></div>
            <span>السؤال الحالي</span>
        </div>
        <div style="display: flex; align-items: center; gap: 8px;">
            <div class="question-status-grid-modal" style="background: var(--success-gradient);"></div>
            <span>تمت الإجابة</span>
        </div>
        <div style="display: flex; align-items: center; gap: 8px;">
            <div class="question-status-grid-modal" style="background: var(--warning-gradient);"></div>
            <span>معلم للمراجعة</span>
        </div>
        <div style="display: flex; align-items: center; gap: 8px;">
            <div class="question-status-grid-modal" style="background: var(--card-bg); border-color: var(--border);"></div>
            <span>لم يتم الإجابة</span>
        </div>
    </div>
    <button class="btn btn-primary" onclick="hideQuestionsList()" style="margin-top: 25px; width: 100%;">
        <i class="fas fa-times"></i>
        إغلاق القائمة
    </button>
</div>

<script>
// المتغيرات الأساسية
let questions = [];
let currentQuestionIndex = 0;
let userAnswers = [];
let timeLeft = 45 * 60;
let timerInterval;
let markedQuestions = [];
let answerLocked = [];
let viewMode = 'single';
let removedOptions = {};
let feedbackVisible = {};
let hintVisible = {};
let removeOptionUsage = {};
let isTranslated = false; // حالة الترجمة
let originalHints = {}; // تخزين التلميحات الأصلية
let originalExplanations = {}; // تخزين الشروحات الأصلية

// تهيئة التطبيق
window.onload = function() {
    // تحميل تفضيل الوضع الداكن من localStorage
    const savedTheme = localStorage.getItem('theme');
    if (savedTheme === 'dark') {
        enableDarkMode();
    }
    
    loadQuiz();
    startTimer();
    
    // إعداد زر الواتساب
    document.getElementById('whatsappBtn').addEventListener('click', function() {
        const currentQuestion = currentQuestionIndex + 1;
        const questionText = getQuestionNumberText(currentQuestionIndex);
        const message = `السلام عليكم ورحمة الله وبركاته

أود الإبلاغ عن ملاحظة في اختبار الرخصة المهنية:

• ${questionText}
• الملاحظة: [يرجى كتابة الملاحظة هنا]

مع الشكر والتقدير`;

        const phoneNumber = '966597077245';
        const whatsappUrl = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`;
        window.open(whatsappUrl, '_blank');
    });
    
    // إعداد زر تبديل الوضع
    document.getElementById('themeBtn').addEventListener('click', toggleTheme);
    
    // إعداد زر الترجمة
    document.getElementById('translateBtn').addEventListener('click', toggleTranslation);
};

// تبديل الترجمة - نسخة محسنة تعمل بشكل فوري
async function toggleTranslation() {
    if (isTranslated) {
        // إرجاع النص الأصلي
        revertToOriginal();
        document.getElementById('translateBtn').innerHTML = '<i class="fas fa-language"></i><span class="translate-text">ترجمة</span>';
        document.getElementById('translateBtn').title = 'ترجمة التلميحات';
        isTranslated = false;
    } else {
        // ترجمة التلميحات والتغذية الراجعة
        await translateHintsAndExplanations();
        document.getElementById('translateBtn').innerHTML = '<i class="fas fa-undo"></i><span class="translate-text">إرجاع</span>';
        document.getElementById('translateBtn').title = 'إرجاع النص الأصلي';
        isTranslated = true;
    }
}

// دالة لترجمة التلميحات والتغذية الراجعة - نسخة محسنة
async function translateHintsAndExplanations() {
    // حفظ النصوص الأصلية أولاً
    saveOriginalTexts();
    
    // استخدام ترجمة فورية بدون API (يمكن إضافة API لاحقاً)
    for (let i = 0; i < questions.length; i++) {
        if (questions[i].hint && originalHints[i]) {
            const translatedHint = await translateTextLocal(originalHints[i]);
            questions[i].hint = translatedHint;
        }
        
        if (questions[i].explanations && originalExplanations[i]) {
            const translatedExplanation = await translateTextLocal(originalExplanations[i].correct);
            questions[i].explanations.correct = translatedExplanation;
        }
    }
    
    // إعادة تحميل السؤال الحالي
    loadQuiz();
}

// حفظ النصوص الأصلية
function saveOriginalTexts() {
    for (let i = 0; i < questions.length; i++) {
        if (questions[i].hint) {
            originalHints[i] = questions[i].hint;
        }
        
        if (questions[i].explanations) {
            originalExplanations[i] = {
                correct: questions[i].explanations.correct
            };
        }
    }
}

// إرجاع النصوص الأصلية
function revertToOriginal() {
    for (let i = 0; i < questions.length; i++) {
        if (originalHints[i]) {
            questions[i].hint = originalHints[i];
        }
        
        if (originalExplanations[i]) {
            questions[i].explanations.correct = originalExplanations[i].correct;
        }
    }
    
    // إعادة تحميل السؤال الحالي
    loadQuiz();
}

// دالة ترجمة محلية بدون API (نموذجية)
async function translateTextLocal(text) {
    // هذا مثال بسيط للترجمة، يمكن استبداله بـ API حقيقي
    const translations = {
        "[t] is produced by placing the tongue near the alveolar ridge and no vibration of the vocal cords.": "يتم إنتاج الصوت [t] بوضع اللسان بالقرب من الحافة السنخية دون اهتزاز الأحبال الصوتية.",
        "Think of the 'ch' sound at the start of 'chin.'": "فكر في صوت 'ch' في بداية كلمة 'chin'.",
        "Voiced sounds involve vibration of the vocal cords; feel your throat when pronouncing.": "تتضمن الأصوات المجهورة اهتزاز الأحبال الصوتية؛ اشعر بحلقك عند النطق.",
        "Velar sounds are made at the back of the mouth; voiceless plosive stops are sharp bursts.": "يتم إنتاج الأصوات اللهوية في مؤخرة الفم؛ التوقفات الانفجارية غير المجهورة هي انفجارات حادة.",
        "Both [t] and [d] share the same tongue position near the alveolar ridge.": "كلا الصوتين [t] و [d] يشتركان في نفس موضع اللسان بالقرب من الحافة السنخية.",
        "The [t] sound is produced by placing the tongue against the alveolar ridge (just behind the upper front teeth), stopping the airflow completely, and releasing it without vibration of the vocal cords. That makes it alveolar (place), stop/plosive (manner), and voiceless (voicing).": "يتم إنتاج الصوت [t] بوضع اللسان مقابل الحافة السنخية (خلف الأسنان الأمامية العلوية مباشرة)، وإيقاف تدفق الهواء تمامًا، ثم إطلاقه دون اهتزاز الأحبال الصوتية. وهذا يجعله سنخيًا (المكان)، توقف/انفجاري (الطريقة)، وغير مجهور (الجهر).",
        "The [ʧ] sound is a voiceless postalveolar affricate, produced by stopping the airflow completely and then releasing it with friction, as in 'chin.'": "الصوت [ʧ] هو احتكاكي ما بعد سنخي غير مجهور، يتم إنتاجه عن طريق إيقاف تدفق الهواء تمامًا ثم إطلاقه مع احتكاك، كما في كلمة 'chin'.",
        "[v] is a voiced labiodental fricative, meaning the vocal cords vibrate when producing it.": "[v] هو احتكاكي شفوي سني مجهور، مما يعني أن الأحبال الصوتية تهتز عند إنتاجه.",
        "[k] is produced by raising the back of the tongue to the velum (soft palate), stopping airflow completely, and releasing it without vocal cord vibration.": "يتم إنتاج [k] عن طريق رفع مؤخرة اللسان إلى الحنك الرخو (اللهاة)، وإيقاف تدفق الهواء تمامًا، ثم إطلاقه دون اهتزاز الأحبال الصوتية.",
        "Both [t] (voiceless) and [d] (voiced) are made by placing the tongue against the alveolar ridge.": "يتم إنتاج كل من [t] (غير مجهور) و [d] (مجهور) بوضع اللسان مقابل الحافة السنخية."
    };
    
    return translations[text] || text;
}

// دالة لتحويل الأرقام إلى نص عربي ترتيبي
function convertToArabicOrdinal(number) {
    const arabicOrdinals = {
        1: "الأول",
        2: "الثاني", 
        3: "الثالث",
        4: "الرابع",
        5: "الخامس",
        6: "السادس",
        7: "السابع",
        8: "الثامن",
        9: "التاسع",
        10: "العاشر"
    };
    
    return arabicOrdinals[number] || `(${number})`;
}

// دالة لإنشاء نص رقم السؤال بالترتيبي العربي
function getQuestionNumberText(index) {
    const arabicOrdinal = convertToArabicOrdinal(index + 1);
    return `السؤال ${arabicOrdinal}`;
}

// تبديل الوضع الليلي/النهاري
function toggleTheme() {
    if (document.body.classList.contains('dark-theme')) {
        disableDarkMode();
    } else {
        enableDarkMode();
    }
}

function enableDarkMode() {
    document.body.classList.add('dark-theme');
    document.getElementById('themeBtn').innerHTML = '<i class="fas fa-sun"></i>';
    document.getElementById('themeBtn').title = 'الوضع النهاري';
    localStorage.setItem('theme', 'dark');
}

function disableDarkMode() {
    document.body.classList.remove('dark-theme');
    document.getElementById('themeBtn').innerHTML = '<i class="fas fa-moon"></i>';
    document.getElementById('themeBtn').title = 'الوضع الليلي';
    localStorage.setItem('theme', 'light');
}

// بدء المؤقت
function startTimer() {
    updateTimerDisplay();
    timerInterval = setInterval(() => {
        timeLeft--;
        updateTimerDisplay();
        
        if (timeLeft <= 0) {
            clearInterval(timerInterval);
            finishQuiz();
        }
    }, 1000);
}

function updateTimerDisplay() {
    const minutes = Math.floor(timeLeft / 60);
    const seconds = timeLeft % 60;
    document.getElementById('time-display').textContent = 
        `${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
}

// تعيين وضع العرض
function setViewMode(mode) {
    viewMode = mode;
    
    // تحديث أزرار الوضع
    document.querySelectorAll('.view-mode-btn').forEach(btn => {
        btn.classList.remove('active');
    });
    event.target.classList.add('active');
    
    // إعادة تحميل الأسئلة
    loadQuiz();
}

// تحميل الاختبار
function loadQuiz() {
    const quizDiv = document.getElementById("quiz");
    const viewModeSelector = document.getElementById("viewModeSelector");
    
    if (questions.length === 0) {
        viewModeSelector.style.display = 'block';
        quizDiv.innerHTML = `
            <div class="card">
                <h3 style="color: var(--text); margin-bottom: 30px; text-align: center; font-size: 1.8rem;">
                    <i class="fas fa-info-circle" style="color: var(--primary-light); margin-left: 12px;"></i>
                    مرحبًا بكم في اختبار الرخصة المهنية
                </h3>
                <p style="text-align: center; color: var(--light-text); margin-bottom: 25px; font-size: 1.2rem; line-height: 1.8;">
                    اختر طريقة عرض الأسئلة ثم اضغط على زر "إبدأ الاختبار" لتحميل الأسئلة والبدء.
                </p>
                <div style="text-align: center;">
                    <button class="btn btn-finish" onclick="addSampleQuestions()">
                        <i class="fas fa-play-circle"></i>
                        إبدأ الاختبار
                    </button>
                </div>
            </div>
        `;
        return;
    }
    
    viewModeSelector.style.display = 'none';
    
    if (viewMode === 'single') {
        loadSingleQuestion();
    } else {
        loadMultipleQuestions();
    }
    
    updateProgressAndInfo();
    updateMarkButton();
}

// تحميل سؤال واحد
function loadSingleQuestion() {
    const quizDiv = document.getElementById("quiz");
    const question = questions[currentQuestionIndex];
    const isLocked = answerLocked[currentQuestionIndex];
    
    // تنظيف نص السؤال - إزالة علامة الاستفهام والمسافات الزائدة
    let questionText = cleanQuestionText(question.q);
    
    // الحصول على نص السؤال بالترتيبي العربي
    const questionNumberText = getQuestionNumberText(currentQuestionIndex);
    
    let html = `
        <div class="question-box">
            <div class="question-number">
                <i class="fas fa-question-circle"></i>
                ${questionNumberText}
                <span style="margin-right: auto; color: var(--light-text); font-size: 0.9rem; font-weight: normal;">
                    (${currentQuestionIndex + 1} من ${questions.length})
                </span>
                ${isLocked ? '<span style="color: var(--accent); margin-right: 10px;"><i class="fas fa-lock"></i> مقفل</span>' : ''}
            </div>
            <div class="question-text">${questionText}</div>
            <div class="options">
    `;
    
    question.options.forEach((opt, i) => {
        const isChecked = userAnswers[currentQuestionIndex] === i;
        const isDisabled = isLocked;
        let labelClass = '';
        const isRemoved = removedOptions[currentQuestionIndex] && removedOptions[currentQuestionIndex].includes(i);
        
        if (isRemoved) {
            labelClass = 'option-removed';
        } else if (isLocked) {
            labelClass = 'locked';
            if (isChecked) {
                labelClass += userAnswers[currentQuestionIndex] === question.answer ? ' correct-answer' : ' wrong-answer';
            } else if (i === question.answer) {
                labelClass += ' correct-answer';
            }
        } else if (isChecked) {
            labelClass = 'selected';
        }
        
        html += `
            <label class="${labelClass}" ${isRemoved ? 'style="opacity: 0.4; pointer-events: none; text-decoration: line-through;"' : ''}>
                <input type="radio" name="q${currentQuestionIndex}" value="${i}" ${isChecked ? 'checked' : ''} ${isDisabled || isRemoved ? 'disabled' : ''} onchange="selectAnswer(${i})">
                ${opt}
                ${isLocked && i === question.answer ? ' <i class="fas fa-check" style="color: var(--success-light); margin-right: 5px;"></i>' : ''}
            </label>
        `;
    });
    
    // حساب عدد المرات المتبقية لحذف الخيارات
    const remainingRemovals = 2 - (removeOptionUsage[currentQuestionIndex] || 0);
    const canRemoveOptions = remainingRemovals > 0 && !isLocked;
    
    html += `
            </div>
            
            <div class="question-actions">
                <button class="action-btn feedback-btn" onclick="toggleFeedback(${currentQuestionIndex})">
                    <i class="fas ${feedbackVisible[currentQuestionIndex] ? 'fa-eye-slash' : 'fa-eye'}"></i>
                    ${feedbackVisible[currentQuestionIndex] ? 'إخفاء التغذية الراجعة' : 'تغذية راجعة فورية'}
                </button>
                
                <button class="action-btn remove-options-btn" onclick="removeTwoWrongOptions(${currentQuestionIndex})" 
                    ${!canRemoveOptions ? 'disabled' : ''}>
                    <i class="fas fa-filter"></i>
                    ${remainingRemovals > 0 ? `حذف إجابتين خاطئة (${remainingRemovals} متبقية)` : 'تم الاستخدام'}
                </button>
                
                <button class="action-btn hint-btn" onclick="toggleHint(${currentQuestionIndex})">
                    <i class="fas fa-lightbulb"></i>
                    ${hintVisible[currentQuestionIndex] ? 'إخفاء التلميح' : 'تلميح'}
                </button>
            </div>
            
            <div id="message-${currentQuestionIndex}" class="message-box"></div>
            
            <div id="hint-${currentQuestionIndex}" class="hint-box ${hintVisible[currentQuestionIndex] ? 'show' : ''}"></div>
            
            <div id="explanation" class="explanation ${feedbackVisible[currentQuestionIndex] ? 'show' : ''}"></div>
        </div>
        <div class="navigation">
            <button class="btn btn-secondary" onclick="previousQuestion()" ${currentQuestionIndex === 0 ? 'disabled' : ''}>
                <i class="fas fa-arrow-right"></i>
                السابق
            </button>
            <button class="btn btn-primary" onclick="nextQuestion()" ${currentQuestionIndex === questions.length - 1 ? 'disabled' : ''}>
                التالي
                <i class="fas fa-arrow-left"></i>
            </button>
        </div>
    `;
    
    quizDiv.innerHTML = html;
    
    // إذا كان الشرح ظاهراً، عرضه
    if (feedbackVisible[currentQuestionIndex] && userAnswers[currentQuestionIndex] !== null) {
        showExplanation();
    }
    
    // إذا كان التلميح ظاهراً، عرضه
    if (hintVisible[currentQuestionIndex]) {
        showHint(currentQuestionIndex);
    }
}

// تحميل 5 أسئلة
function loadMultipleQuestions() {
    const quizDiv = document.getElementById("quiz");
    let html = '';
    
    // حساب بداية ونهاية الصفحة
    const startIndex = Math.floor(currentQuestionIndex / 5) * 5;
    const endIndex = Math.min(startIndex + 5, questions.length);
    
    for (let i = startIndex; i < endIndex; i++) {
        const question = questions[i];
        const isLocked = answerLocked[i];
        
        // تنظيف نص السؤال - إزالة علامة الاستفهام والمسافات الزائدة
        let questionText = cleanQuestionText(question.q);
        
        // الحصول على نص السؤال بالترتيبي العربي
        const questionNumberText = getQuestionNumberText(i);
        
        // حساب عدد المرات المتبقية لحذف الخيارات
        const remainingRemovals = 2 - (removeOptionUsage[i] || 0);
        const canRemoveOptions = remainingRemovals > 0 && !isLocked;
        
        html += `
            <div class="question-box" style="margin-bottom: 30px;">
                <div class="question-number">
                    <i class="fas fa-question-circle"></i>
                    ${questionNumberText}
                    <span style="margin-right: auto; color: var(--light-text); font-size: 0.9rem; font-weight: normal;">
                        (${i + 1} من ${questions.length})
                    </span>
                </div>
                <div class="question-text">${questionText}</div>
                <div class="options">
        `;
        
        question.options.forEach((opt, j) => {
            const isChecked = userAnswers[i] === j;
            const isDisabled = isLocked;
            let labelClass = '';
            const isRemoved = removedOptions[i] && removedOptions[i].includes(j);
            
            if (isRemoved) {
                labelClass = 'option-removed';
            } else if (isLocked) {
                labelClass = 'locked';
                if (isChecked) {
                    labelClass += userAnswers[i] === question.answer ? ' correct-answer' : ' wrong-answer';
                } else if (j === question.answer) {
                    labelClass += ' correct-answer';
                }
            } else if (isChecked) {
                labelClass = 'selected';
            }
            
            html += `
                <label class="${labelClass}" ${isRemoved ? 'style="opacity: 0.4; pointer-events: none; text-decoration: line-through;"' : ''}>
                    <input type="radio" name="q${i}" value="${j}" ${isChecked ? 'checked' : ''} ${isDisabled || isRemoved ? 'disabled' : ''} onchange="selectAnswerMulti(${i}, ${j})">
                    ${opt}
                </label>
            `;
        });
        
        html += `
                </div>
                
                <div class="question-actions">
                    <button class="action-btn feedback-btn" onclick="toggleFeedbackMulti(${i})">
                        <i class="fas ${feedbackVisible[i] ? 'fa-eye-slash' : 'fa-eye'}"></i>
                        تغذية راجعة
                    </button>
                    
                    <button class="action-btn remove-options-btn" onclick="removeTwoWrongOptions(${i})" 
                        ${!canRemoveOptions ? 'disabled' : ''}>
                        <i class="fas fa-filter"></i>
                        ${remainingRemovals > 0 ? `حذف خيارين (${remainingRemovals})` : 'تم'}
                    </button>
                    
                    <button class="action-btn hint-btn" onclick="toggleHintMulti(${i})">
                        <i class="fas fa-lightbulb"></i>
                        تلميح
                    </button>
                </div>
                
                <div id="message-${i}" class="message-box"></div>
                
                <div id="hint-${i}" class="hint-box" style="display: none;"></div>
                
                <div id="explanation-${i}" class="explanation" style="display: none;"></div>
            </div>
        `;
    }
    
    // أزرار التنقل بين صفحات 5 أسئلة
    const totalPages = Math.ceil(questions.length / 5);
    const currentPage = Math.floor(currentQuestionIndex / 5);
    
    html += `
        <div class="navigation">
            <button class="btn btn-secondary" onclick="previousPage()" ${currentPage === 0 ? 'disabled' : ''}>
                <i class="fas fa-arrow-right"></i>
                الصفحة السابقة
            </button>
            <button class="btn btn-primary" onclick="nextPage()" ${currentPage === totalPages - 1 ? 'disabled' : ''}>
                الصفحة التالية
                <i class="fas fa-arrow-left"></i>
            </button>
        </div>
    `;
    
    quizDiv.innerHTML = html;
    
    // عرض الشروح إذا كانت ظاهرة
    for (let i = startIndex; i < endIndex; i++) {
        if (feedbackVisible[i] && userAnswers[i] !== null) {
            const explanationDiv = document.getElementById(`explanation-${i}`);
            if (explanationDiv) {
                explanationDiv.style.display = 'block';
                showExplanationMulti(i);
            }
        }
        
        // عرض التلميحات إذا كانت ظاهرة
        if (hintVisible[i]) {
            const hintDiv = document.getElementById(`hint-${i}`);
            if (hintDiv) {
                hintDiv.style.display = 'block';
                showHint(i);
            }
        }
    }
}

// تنظيف نص السؤال
function cleanQuestionText(text) {
    // إزالة علامات الاستفهام من البداية
    let cleanedText = text.replace(/^[؟?]+/, '');
    // إزالة المسافات الزائدة من البداية والنهاية
    cleanedText = cleanedText.trim();
    // إضافة نقطة في النهاية إذا لم تكن موجودة
    if (cleanedText && !/[.!؟؟]$/.test(cleanedText)) {
        cleanedText += '.';
    }
    return cleanedText;
}

// اختيار إجابة
function selectAnswer(answerIndex) {
    if (answerLocked[currentQuestionIndex]) return;
    
    userAnswers[currentQuestionIndex] = answerIndex;
    answerLocked[currentQuestionIndex] = true;
    
    // إخفاء أي رسالة
    const messageBox = document.getElementById(`message-${currentQuestionIndex}`);
    if (messageBox) {
        messageBox.style.display = 'none';
    }
    
    // عرض التغذية الراجعة إذا كانت مفعلة
    if (feedbackVisible[currentQuestionIndex]) {
        showExplanation();
    }
    
    // تحديث الواجهة
    if (viewMode === 'single') {
        loadQuiz();
    }
    
    // تحديث قائمة الأسئلة إذا كانت ظاهرة
    if (document.getElementById('questions-overlay').style.display === 'block') {
        showQuestionsList();
    }
}

function selectAnswerMulti(questionIndex, answerIndex) {
    if (answerLocked[questionIndex]) return;
    
    userAnswers[questionIndex] = answerIndex;
    answerLocked[questionIndex] = true;
    
    // إخفاء أي رسالة
    const messageBox = document.getElementById(`message-${questionIndex}`);
    if (messageBox) {
        messageBox.style.display = 'none';
    }
    
    // تحديث الواجهة
    if (viewMode === 'multi') {
        loadQuiz();
    }
}

// تبديل عرض التغذية الراجعة
function toggleFeedback(questionIndex) {
    if (userAnswers[questionIndex] === null) {
        // عرض رسالة بدلاً من الشرح
        const messageBox = document.getElementById(`message-${questionIndex}`);
        if (messageBox) {
            messageBox.innerHTML = `
                <div style="display: flex; align-items: center; gap: 15px;">
                    <i class="fas fa-info-circle" style="font-size: 1.5em;"></i>
                    <div>
                        <h4 style="color: var(--warning); margin-bottom: 5px;">ملاحظة:</h4>
                        <p style="color: var(--light-text);">التغذية الراجعة ستظهر بعد اختيار الجواب النهائي للسؤال.</p>
                    </div>
                </div>
            `;
            messageBox.classList.add('show');
        }
        
        // إخفاء صندوق الشرح إذا كان ظاهراً
        const explanationDiv = document.getElementById('explanation');
        if (explanationDiv) {
            explanationDiv.style.display = 'none';
        }
        
        feedbackVisible[questionIndex] = false;
        return;
    }
    
    feedbackVisible[questionIndex] = !feedbackVisible[questionIndex];
    
    if (feedbackVisible[questionIndex]) {
        showExplanation();
        // إخفاء الرسالة إذا كانت ظاهرة
        const messageBox = document.getElementById(`message-${questionIndex}`);
        if (messageBox) {
            messageBox.classList.remove('show');
        }
    } else {
        // إخفاء الشرح
        const explanationDiv = document.getElementById('explanation');
        if (explanationDiv) {
            explanationDiv.style.display = 'none';
        }
    }
    
    loadQuiz();
}

function toggleFeedbackMulti(questionIndex) {
    if (userAnswers[questionIndex] === null) {
        // عرض رسالة بدلاً من الشرح
        const messageBox = document.getElementById(`message-${questionIndex}`);
        if (messageBox) {
            messageBox.innerHTML = `
                <div style="display: flex; align-items: center; gap: 15px;">
                    <i class="fas fa-info-circle" style="font-size: 1.5em;"></i>
                    <div>
                        <h4 style="color: var(--warning); margin-bottom: 5px;">ملاحظة:</h4>
                        <p style="color: var(--light-text);">التغذية الراجعة ستظهر بعد اختيار الجواب النهائي للسؤال.</p>
                    </div>
                </div>
            `;
            messageBox.classList.add('show');
        }
        
        // إخفاء صندوق الشرح إذا كان ظاهراً
        const explanationDiv = document.getElementById(`explanation-${questionIndex}`);
        if (explanationDiv) {
            explanationDiv.style.display = 'none';
        }
        
        feedbackVisible[questionIndex] = false;
        return;
    }
    
    feedbackVisible[questionIndex] = !feedbackVisible[questionIndex];
    
    const explanationDiv = document.getElementById(`explanation-${questionIndex}`);
    if (explanationDiv) {
        if (feedbackVisible[questionIndex]) {
            explanationDiv.style.display = 'block';
            showExplanationMulti(questionIndex);
            // إخفاء الرسالة إذا كانت ظاهرة
            const messageBox = document.getElementById(`message-${questionIndex}`);
            if (messageBox) {
                messageBox.classList.remove('show');
            }
        } else {
            explanationDiv.style.display = 'none';
        }
    }
}

// تبديل عرض التلميح
function toggleHint(questionIndex) {
    hintVisible[questionIndex] = !hintVisible[questionIndex];
    
    if (hintVisible[questionIndex]) {
        showHint(questionIndex);
    }
    
    loadQuiz();
}

function toggleHintMulti(questionIndex) {
    hintVisible[questionIndex] = !hintVisible[questionIndex];
    
    const hintDiv = document.getElementById(`hint-${questionIndex}`);
    if (hintDiv) {
        if (hintVisible[questionIndex]) {
            hintDiv.style.display = 'block';
            showHint(questionIndex);
        } else {
            hintDiv.style.display = 'none';
        }
    }
}

// عرض التلميح
function showHint(questionIndex) {
    const question = questions[questionIndex];
    const hintDiv = document.getElementById(`hint-${questionIndex}`);
    
    if (!hintDiv) return;
    
    let hintHTML = '';
    
    if (question.hint) {
        hintHTML = `
            <div style="display: flex; align-items: flex-start; gap: 15px;">
                <i class="fas fa-lightbulb" style="font-size: 1.5em; margin-top: 3px;"></i>
                <div>
                    <h4 style="color: #9C27B0; margin-bottom: 10px;">تلميح مفيد:</h4>
                    <p style="line-height: 1.7;">${question.hint}</p>
                </div>
            </div>
        `;
    } else {
        hintHTML = `
            <div style="display: flex; align-items: center; gap: 15px;">
                <i class="fas fa-info-circle" style="color: var(--info); font-size: 1.5em;"></i>
                <div>
                    <p style="color: var(--light-text);">لا يوجد تلميح خاص لهذا السؤال. حاول التفكير في المفهوم الرئيسي للسؤال.</p>
                </div>
            </div>
        `;
    }
    
    hintDiv.innerHTML = hintHTML;
}

// عرض الشرح
function showExplanation() {
    const question = questions[currentQuestionIndex];
    const userAnswer = userAnswers[currentQuestionIndex];
    
    if (userAnswer === null) return;
    
    let resultHTML = "";
    
    if (userAnswer === question.answer) {
        resultHTML = `<p class="correct"><i class="fas fa-check-circle"></i> إجابة صحيحة</p>`;
    } else {
        resultHTML = `
            <p class="wrong"><i class="fas fa-times-circle"></i> إجابة خاطئة — الإجابة الصحيحة: <span class="correct">${question.options[question.answer]}</span></p>
        `;
    }
    
    resultHTML += `
        <div style="margin-top: 20px;">
            <strong>التفسير الصحيح:</strong> ${question.explanations.correct}
        </div>
    `;
    
    document.getElementById("explanation").innerHTML = resultHTML;
}

function showExplanationMulti(questionIndex) {
    const question = questions[questionIndex];
    const userAnswer = userAnswers[questionIndex];
    
    if (userAnswer === null) return;
    
    let resultHTML = "";
    
    if (userAnswer === question.answer) {
        resultHTML = `<p class="correct"><i class="fas fa-check-circle"></i> إجابة صحيحة</p>`;
    } else {
        resultHTML = `
            <p class="wrong"><i class="fas fa-times-circle"></i> إجابة خاطئة — الإجابة الصحيحة: <span class="correct">${question.options[question.answer]}</span></p>
        `;
    }
    
    resultHTML += `
        <div style="margin-top: 20px;">
            <strong>التفسير الصحيح:</strong> ${question.explanations.correct}
        </div>
    `;
    
    const explanationDiv = document.getElementById(`explanation-${questionIndex}`);
    if (explanationDiv) {
        explanationDiv.innerHTML = resultHTML;
    }
}

// حذف إجابتين خاطئتين
function removeTwoWrongOptions(questionIndex) {
    const question = questions[questionIndex];
    
    // التحقق من عدد مرات الاستخدام المتبقية
    const remainingUses = 2 - (removeOptionUsage[questionIndex] || 0);
    if (remainingUses <= 0) {
        return;
    }
    
    // العثور على الخيارات الخاطئة غير المحذوفة مسبقاً
    const wrongOptions = [];
    for (let i = 0; i < question.options.length; i++) {
        if (i !== question.answer) {
            // التحقق من أن الخيار لم يتم حذفه مسبقاً
            if (!removedOptions[questionIndex] || !removedOptions[questionIndex].includes(i)) {
                wrongOptions.push(i);
            }
        }
    }
    
    // إذا لم يكن هناك خيارات خاطئة متبقية
    if (wrongOptions.length === 0) {
        alert("لا توجد خيارات خاطئة متبقية لحذفها!");
        return;
    }
    
    // عدد الخيارات المراد حذفها (إما 1 أو 2)
    const optionsToRemoveCount = Math.min(wrongOptions.length, remainingUses);
    
    // اختيار الخيارات بشكل عشوائي
    const optionsToRemove = [];
    const tempWrongOptions = [...wrongOptions];
    
    for (let i = 0; i < optionsToRemoveCount; i++) {
        const randomIndex = Math.floor(Math.random() * tempWrongOptions.length);
        optionsToRemove.push(tempWrongOptions.splice(randomIndex, 1)[0]);
    }
    
    // حفظ الخيارات المحذوفة
    if (!removedOptions[questionIndex]) {
        removedOptions[questionIndex] = [];
    }
    removedOptions[questionIndex].push(...optionsToRemove);
    
    // تحديث عدد مرات الاستخدام
    removeOptionUsage[questionIndex] = (removeOptionUsage[questionIndex] || 0) + optionsToRemoveCount;
    
    // تحديث الواجهة
    if (viewMode === 'single' && questionIndex === currentQuestionIndex) {
        loadQuiz();
    } else if (viewMode === 'multi') {
        loadQuiz();
    }
}

// التنقل بين الأسئلة
function nextQuestion() {
    if (currentQuestionIndex < questions.length - 1) {
        currentQuestionIndex++;
        loadQuiz();
    }
}

function previousQuestion() {
    if (currentQuestionIndex > 0) {
        currentQuestionIndex--;
        loadQuiz();
    }
}

// التنقل بين الصفحات (في وضع 5 أسئلة)
function nextPage() {
    const totalPages = Math.ceil(questions.length / 5);
    const currentPage = Math.floor(currentQuestionIndex / 5);
    
    if (currentPage < totalPages - 1) {
        currentQuestionIndex = (currentPage + 1) * 5;
        loadQuiz();
    }
}

function previousPage() {
    const currentPage = Math.floor(currentQuestionIndex / 5);
    
    if (currentPage > 0) {
        currentQuestionIndex = (currentPage - 1) * 5;
        loadQuiz();
    }
}

// تحديث التقدم والمعلومات
function updateProgressAndInfo() {
    // شريط التقدم
    const progress = document.getElementById('progress');
    if (questions.length > 0) {
        const answeredCount = userAnswers.filter(answer => answer !== null).length;
        progress.style.width = `${(answeredCount / questions.length) * 100}%`;
    } else {
        progress.style.width = '0%';
    }
    
    // معلومات الاختبار
    const quizInfo = document.getElementById('quiz-info');
    if (viewMode === 'single') {
        quizInfo.textContent = `السؤال ${currentQuestionIndex + 1} من ${questions.length}`;
    } else {
        const currentPage = Math.floor(currentQuestionIndex / 5) + 1;
        const totalPages = Math.ceil(questions.length / 5);
        quizInfo.textContent = `الصفحة ${currentPage} من ${totalPages}`;
    }
}

// عرض قائمة الأسئلة
function showQuestionsList() {
    const grid = document.getElementById('questions-grid-modal');
    grid.innerHTML = '';
    
    questions.forEach((_, index) => {
        const btn = document.createElement('div');
        btn.className = `question-status-grid-modal`;
        
        if (index === currentQuestionIndex) {
            btn.classList.add('current');
        }
        if (userAnswers[index] !== null) {
            btn.classList.add('answered');
        }
        if (markedQuestions.includes(index)) {
            btn.classList.add('marked');
        }
        if (answerLocked[index]) {
            btn.classList.add('locked');
        }
        
        btn.innerHTML = `<span>${index + 1}</span>`;
        btn.onclick = () => {
            if (!answerLocked[index]) {
                currentQuestionIndex = index;
                loadQuiz();
                hideQuestionsList();
            }
        };
        grid.appendChild(btn);
    });
    
    document.getElementById('questions-overlay').style.display = 'block';
    document.getElementById('questions-modal').style.display = 'block';
    document.body.style.overflow = 'hidden';
}

// إخفاء قائمة الأسئلة
function hideQuestionsList() {
    document.getElementById('questions-overlay').style.display = 'none';
    document.getElementById('questions-modal').style.display = 'none';
    document.body.style.overflow = 'auto';
}

// وضع علامة للمراجعة
function toggleMarkForReview() {
    const index = markedQuestions.indexOf(currentQuestionIndex);
    
    if (index === -1) {
        markedQuestions.push(currentQuestionIndex);
        document.getElementById('mark-review-btn').innerHTML = '<i class="fas fa-flag"></i> إزالة العلامة';
        document.getElementById('mark-review-btn').style.background = 'var(--warning-gradient)';
    } else {
        markedQuestions.splice(index, 1);
        document.getElementById('mark-review-btn').innerHTML = '<i class="fas fa-flag"></i> وضع علامة للمراجعة';
        document.getElementById('mark-review-btn').style.background = 'var(--success-gradient)';
    }
    
    // تحديث قائمة الأسئلة إذا كانت ظاهرة
    if (document.getElementById('questions-overlay').style.display === 'block') {
        showQuestionsList();
    }
}

// تحديث زر وضع العلامة
function updateMarkButton() {
    const markBtn = document.getElementById('mark-review-btn');
    if (markBtn) {
        if (markedQuestions.includes(currentQuestionIndex)) {
            markBtn.innerHTML = '<i class="fas fa-flag"></i> إزالة العلامة';
            markBtn.style.background = 'var(--warning-gradient)';
        } else {
            markBtn.innerHTML = '<i class="fas fa-flag"></i> وضع علامة للمراجعة';
            markBtn.style.background = 'var(--success-gradient)';
        }
    }
}

// إضافة أسئلة نموذجية مع تلميحات (باللغة الإنجليزية)
function addSampleQuestions() {
    questions = [
        {
            "id": 1,
            "q": "The [t] sound can be phonetically described as:",
            "options": ["Alveolar, stop, voiceless", "Alveolar, plosive, voiced", "Velar, plosive, voiced", "Velar, plosive, voiceless"],
            "answer": 0,
            "explanations": {
                "correct": "The [t] sound is produced by placing the tongue against the alveolar ridge (just behind the upper front teeth), stopping the airflow completely, and releasing it without vibration of the vocal cords. That makes it alveolar (place), stop/plosive (manner), and voiceless (voicing)."
            },
            "hint": "[t] is produced by placing the tongue near the alveolar ridge and no vibration of the vocal cords."
        },
        {
            "id": 2,
            "q": "The [ʧ] sound is found in:",
            "options": ["chin", "chemistry", "ship", "Christ"],
            "answer": 0,
            "explanations": {
                "correct": "The [ʧ] sound is a voiceless postalveolar affricate, produced by stopping the airflow completely and then releasing it with friction, as in 'chin'."
            },
            "hint": "Think of the 'ch' sound at the start of 'chin'."
        },
        {
            "id": 3,
            "q": "Which of the following sounds is voiced?",
            "options": ["[v]", "[k]", "[p]", "[t]"],
            "answer": 0,
            "explanations": {
                "correct": "[v] is a voiced labiodental fricative, meaning the vocal cords vibrate when producing it."
            },
            "hint": "Voiced sounds involve vibration of the vocal cords; feel your throat when pronouncing."
        },
        {
            "id": 4,
            "q": "Which of the following sounds can be described as velar, plosive, voiceless?",
            "options": ["[k]", "[g]", "[s]", "[n]"],
            "answer": 0,
            "explanations": {
                "correct": "[k] is produced by raising the back of the tongue to the velum (soft palate), stopping airflow completely, and releasing it without vocal cord vibration."
            },
            "hint": "Velar sounds are made at the back of the mouth; voiceless plosive stops are sharp bursts."
        },
        {
            "id": 5,
            "q": "The [t] and [d] sounds are:",
            "options": ["Velar", "Bilabial", "Alveolar", "Pharyngeal"],
            "answer": 2,
            "explanations": {
                "correct": "Both [t] (voiceless) and [d] (voiced) are made by placing the tongue against the alveolar ridge."
            },
            "hint": "Both [t] and [d] share the same tongue position near the alveolar ridge."
        }
    ];
    
    // تهيئة المصفوفات
    userAnswers = Array(questions.length).fill(null);
    answerLocked = Array(questions.length).fill(false);
    removedOptions = {};
    feedbackVisible = {};
    hintVisible = {};
    markedQuestions = [];
    removeOptionUsage = {}; // إعادة تهيئة عدد مرات الاستخدام
    
    // حفظ النصوص الأصلية
    saveOriginalTexts();
    
    // إعادة تحميل الاختبار
    loadQuiz();
    
    alert("تم تحميل 5 أسئلة بنجاح! استعن بالله وابدأ الاختبار");
}

// الدوال الأخرى
function finishQuiz() {
    clearInterval(timerInterval);
    
    let totalCorrect = 0;
    userAnswers.forEach((answer, index) => {
        if (answer === questions[index]?.answer) {
            totalCorrect++;
        }
    });
    
    const total = questions.length;
    const percentage = total > 0 ? ((totalCorrect / total) * 100).toFixed(2) : 0;
    
    let evaluation = "";
    if (percentage >= 90) {
        evaluation = "ممتاز";
    } else if (percentage >= 80) {
        evaluation = "جيد جداً";
    } else if (percentage >= 70) {
        evaluation = "جيد";
    } else {
        evaluation = "يحتاج تحسين";
    }
    
    document.getElementById("result-box").style.display = "block";
    document.getElementById("result").innerHTML = `النتيجة: ${totalCorrect} من ${total}`;
    document.getElementById("percentage").innerHTML = `النسبة المئوية: ${percentage}%`;
    document.getElementById("evaluation").innerHTML = `التقييم: ${evaluation}`;
    
    document.getElementById("quiz").style.display = "none";
    document.querySelector(".controls").style.display = "none";
}

function showCurrentScore() {
    let totalCorrect = 0;
    userAnswers.forEach((answer, index) => {
        if (answer === questions[index]?.answer) {
            totalCorrect++;
        }
    });
    
    const total = questions.length;
    const percentage = total > 0 ? ((totalCorrect / total) * 100).toFixed(2) : 0;
    
    document.getElementById("current-score").style.display = "block";
    document.getElementById("current-correct").innerHTML = `الإجابات الصحيحة: ${totalCorrect} من ${total}`;
    document.getElementById("current-percentage").innerHTML = `النسبة المئوية الحالية: ${percentage}%`;
}
</script>
</body>
</html>
