<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>منصة مستر محمد يوسف | الإمبراطورية التعليمية</title>
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"/>
    <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
    <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

    <style>
        :root {
            --primary: #00d2ff;
            --secondary: #3a7bd5;
            --chem-color: #8b5cf6;
            --accent: #ffd700;
            --dark-bg: #050a18;
            --card-bg: rgba(255, 255, 255, 0.05);
            --glass-border: rgba(255, 255, 255, 0.1);
            --text-main: #e2e8f0;
        }

        * { box-sizing: border-box; transition: all 0.3s ease; }
        body { margin: 0; font-family: 'Cairo', sans-serif; background: var(--dark-bg); color: var(--text-main); overflow-x: hidden; line-height: 1.6; }

        /* خلفية متحركة */
        .bg-glow { position: fixed; inset: 0; z-index: -1; background: radial-gradient(circle at 50% 50%, #1a2a6c 0%, #050a18 100%); opacity: 0.3; }

        /* الصفحة الرئيسية */
        #home-page { height: 100vh; display: flex; flex-direction: column; align-items: center; justify-content: center; text-align: center; background: url('https://www.transparenttextures.com/patterns/carbon-fibre.png'); padding: 20px; }
        .hero-title { font-size: clamp(2.5rem, 8vw, 5rem); font-weight: 900; margin-bottom: 10px; background: linear-gradient(to right, #fff, var(--primary), var(--chem-color)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; filter: drop-shadow(0 0 15px rgba(0,210,255,0.3)); }
        .designer-name { font-size: 1.2rem; color: #cbd5e1; margin-bottom: 40px; }
        .designer-name b { color: var(--accent); }

        .selection-cards { display: flex; gap: 20px; flex-wrap: wrap; justify-content: center; width: 100%; max-width: 900px; }
        .s-card { background: var(--card-bg); border: 1px solid var(--glass-border); padding: 40px; border-radius: 30px; cursor: pointer; width: 280px; backdrop-filter: blur(10px); }
        .s-card:hover { transform: translateY(-10px); background: rgba(255,255,255,0.1); border-color: #fff; }
        .s-card i { font-size: 3rem; margin-bottom: 15px; display: block; }

        /* تنسيق الدروس والمحتوى (كما في الكود الأصلي) */
        .content-area { display: none; padding: 100px 5% 50px; max-width: 1200px; margin: auto; }
        .chapter-card { background: var(--card-bg); padding: 30px; border-radius: 25px; margin-bottom: 40px; border: 1px solid var(--glass-border); backdrop-filter: blur(10px); }
        .lesson-card { background: rgba(255,255,255,0.03); border-radius: 15px; margin: 15px 0; border-right: 5px solid var(--primary); overflow: hidden; }
        .lesson-header { padding: 20px; cursor: pointer; display: flex; justify-content: space-between; align-items: center; font-size: 1.2rem; font-weight: 600; }
        .lesson-content { display: none; padding: 25px; border-top: 1px solid var(--glass-border); background: rgba(0,0,0,0.2); animation: fadeIn 0.5s ease; }
        
        /* صناديق القوانين والملاحظات */
        .law-box { background: rgba(0, 210, 255, 0.05); border: 1px solid var(--primary); padding: 20px; border-radius: 15px; margin: 20px 0; text-align: center; font-size: 1.4rem; color: var(--accent); }
        .note-box { background: rgba(255, 215, 0, 0.1); border-right: 4px solid var(--accent); padding: 15px; margin: 15px 0; }
        .unit-badge { background: var(--secondary); padding: 2px 8px; border-radius: 4px; font-size: 0.8rem; margin-right: 5px; }
        .equation-box { background: #000; padding: 1.2rem; border-radius: 12px; margin: 1rem 0; color: #a5b4fc; direction: ltr; text-align: center; border: 1px solid var(--chem-color); overflow-x: auto; }

        .btn-back { background: #ef4444; color: white; border: none; padding: 12px 30px; border-radius: 50px; cursor: pointer; font-weight: bold; margin-bottom: 30px; }

        @keyframes fadeIn { from { opacity: 0; transform: translateY(-10px); } to { opacity: 1; transform: translateY(0); } }
    </style>
</head>
<body>

    <div class="bg-glow"></div>

    <div id="home-page">
        <h1 class="hero-title animate__animated animate__zoomIn">منصة مستر محمد يوسف</h1>
        <p class="designer-name animate__animated animate__fadeInUp"> MR-
 <b>MOHMED-YOUSSEF</b></p>
        
        <div class="selection-cards">
            <div class="s-card animate__animated animate__fadeInLeft" onclick="showSection('physics-area')">
                <i class="fas fa-atom" style="color: var(--primary);"></i>
                <h3>كوكب الفيزياء</h3>
                <p>رحلة الـ 60 درجة</p>
            </div>
            <div class="s-card animate__animated animate__fadeInRight" onclick="showSection('chem-area')">
                <i class="fas fa-flask" style="color: var(--chem-color);"></i>
                <h3>متعة الكيمياء</h3>
                <p>إتقان العضوية</p>
            </div>
        </div>
        
        <a href="https://www.instagram.com/abodag00?igsh=MXQxYmQ5eDlsZGl1cw==" target="_blank" style="margin-top:30px; color:#aaa; text-decoration:none;">
            <i class="fab fa-instagram"></i> التواصل مع عبدالرحمن البلاصي
        </a>
    </div>

    <div id="physics-area" class="content-area">
        <button class="btn-back" onclick="goHome()">العودة للرئيسية</button>
        <div class="chapter-card animate__animated animate__fadeIn">
            <h2 style="color:var(--accent); border-bottom: 2px solid; display:inline-block; padding-bottom:10px;">
                <i class="fas fa-charging-station"></i> الفصل الأول: التيار الكهربي وقانون أوم
            </h2>
            
            <div class="lesson-card">
                <div class="lesson-header" onclick="toggleLesson('l1-1')">
                    <span>1. مفهوم التيار الكهربي وقانون أوم</span>
                    <i class="fas fa-chevron-down"></i>
                </div>
                <div id="l1-1" class="lesson-content">
                    <h3>💡 الشرح:</h3>
                    <p>التيار الكهربي هو سيل من الشحنات الكهربائية (الإلكترونات) التي تتدفق عبر موصل. لكي يمر تيار، نحتاج لمصدر (بطارية) ومسار مغلق.</p>
                    
                    <div class="note-box">
                        <strong>تنبيه:</strong> الاتجاه الاصطلاحي للتيار يكون من القطب الموجب إلى السالب خارج المصدر.
                    </div>

                    <div class="law-box">
                        $$I = \frac{Q}{t} \quad , \quad V = I \times R$$
                    </div>

                    <ul style="list-style: none; padding: 0;">
                        <li><span class="unit-badge">I</span> شدة التيار - تقاس بالأمبير (A)</li>
                        <li><span class="unit-badge">V</span> فرق الجهد - يقاس بالفولت (V)</li>
                        <li><span class="unit-badge">R</span> المقاومة - تقاس بالأوم (Ω )</li>
                    </ul>
                </div>
            </div>

            <div class="lesson-card">
                <div class="lesson-header" onclick="toggleLesson('l1-2')">
                    <span>2. توصيل المقاومات (توالي وتوازي)</span>
                    <i class="fas fa-chevron-down"></i>
                </div>
                <div id="l1-2" class="lesson-content">
                    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px;">
                        <div style="background: rgba(255,255,255,0.05); padding: 15px; border-radius: 10px;">
                            <h4 style="color: var(--primary)">🟢 التوصيل على التوالي</h4>
                            <ul>
                                <li>الغرض: الحصول على مقاومة كبيرة.</li>
                                <li>التيار (I) ثابت في جميع المقاومات.</li>
                                <li>الجهد يتجزأ بنسب طردية مع المقاومات.</li>
                            </ul>
                            <div class="law-box" style="font-size: 1.1rem;">$$R_{eq} = R_1 + R_2 + R_3...$$</div>
                        </div>
                        <div style="background: rgba(255,255,255,0.05); padding: 15px; border-radius: 10px;">
                            <h4 style="color: var(--primary)">🟡 التوصيل على التوازي</h4>
                            <ul>
                                <li>الغرض: الحصول على مقاومة صغيرة جداً.</li>
                                <li>فرق الجهد (V) ثابت.</li>
                                <li>التيار يتجزأ بنسب عكسية.</li>
                            </ul>
                            <div class="law-box" style="font-size: 1.1rem;">$$\frac{1}{R_{eq}} = \frac{1}{R_1} + \frac{1}{R_2}...$$</div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="lesson-card">
                <div class="lesson-header" onclick="toggleLesson('l1-4')">
                    <span>. قانونا كيرشوف (حل الدوائر المعقدة)</span>
                    <i class="fas fa-chevron-down"></i>
                </div>
                <div id="l1-4" class="lesson-content">
                    <p>نستخدم كيرشوف عندما تعجز قوانين أوم عن حل الدائرة (وجود أكثر من بطارية في أفرع مختلفة).</p>
                    <div class="law-box">
                        <strong>قانون المسارات (الثاني):</strong> $$\sum V_B = \sum (I \cdot R)$$
                        <br>
                        <strong>قانون العقدة (الأول):</strong> $$\sum I_{in} = \sum I_{out}$$
                    </div>
                </div>
            </div>
        </div>

        <div class="chapter-card">
            <h2 style="color:var(--accent); border-bottom: 2px solid; display:inline-block; padding-bottom:10px;">
                <i class="fas fa-magnet"></i> الفصل الثاني: التأثير المغناطيسي للتيار
            </h2>
            
            <div class="lesson-card">
                <div class="lesson-header" onclick="toggleLesson('l2-1')">
                    <span>1. الفيض المغناطيسي لسلك مستقيم</span>
                    <i class="fas fa-chevron-down"></i>
                </div>
                <div id="l2-1" class="lesson-content">
                    <p>عند مرور تيار في سلك، ينشأ حوله مجال مغناطيسي على شكل دوائر منتظمة المركز.</p>
                    <div class="law-box">
                        $$B = \frac{\mu \cdot I}{2\pi \cdot d}$$
                    </div>
                    <p>تستخدم <strong>قاعدة أمبير لليد اليمنى</strong> لتحديد اتجاه المجال.</p>
                </div>
            </div>

            <div class="lesson-card">
                <div class="lesson-header" onclick="toggleLesson('l2-3')">
                    <span>2. القوة المغناطيسية وعزم الازدواج</span>
                    <i class="fas fa-chevron-down"></i>
                </div>
                <div id="l2-3" class="lesson-content">
                    <p>القوة التي يؤثر بها مجال مغناطيسي على سلك يمر به تيار:</p>
                    <div class="law-box">$$F = B \cdot I \cdot L \cdot \sin(\theta)$$</div>
                    <p>أما عزم الازدواج فهو أساس عمل الموتور والجلفانومتر:</p>
                    <div class="law-box">$$\tau = B \cdot I \cdot A \cdot N \cdot \sin(\theta)$$</div>
                </div>
            </div>
        </div>
   <div class="lesson-card" style="border-right-color: #ffd700;">
    <div class="lesson-header" onclick="toggleLesson('l2-devices')">
        <span style="color: #ffd700;"><i class="fas fa-microchip"></i> 3. أجهزة القياس الكهربي (أسرار الأجهزة)</span>
        <i class="fas fa-chevron-down"></i>
    </div>
    <div id="l2-devices" class="lesson-content">
        
        <div class="device-box" style="background: rgba(0, 210, 255, 0.05); padding: 20px; border-radius: 15px; margin-bottom: 25px; border: 1px dashed var(--primary);">
            <h3 style="color: var(--primary)"><i class="fas fa-compass"></i> 1. الجلفانومتر الحساس (الأصل)</h3>
            <p>هو الجهاز الأساسي، يعتمد على <b>عزم الازدواج المغناطيسي</b>. وظيفته الاستدلال على التيارات الضعيفة جداً وتحديد اتجاهها.</p>
            
            

            <div class="note-box">
                <b>لماذا الأقطاب مقعرة؟</b> لجعل خطوط الفيض على هيئة أقطار، فيظل الملف دائماً موازياً للمجال وتكون (\£ = 90°)$، فتصبح العلاقة طردية بين زاوية الانحراف وشدة التيار.
            </div>
            <div class="law-box">الحساسية =  <br> <small>(درجة / ميكروأمبير)</small></div>
        </div>

        <div class="device-box" style="background: rgba(76, 175, 80, 0.05); padding: 20px; border-radius: 15px; margin-bottom: 25px; border: 1px solid #4caf50;">
            <h3 style="color: #4caf50;"><i class="fas fa-tachometer-alt"></i> 2. الأميتر (قياس تيار مستمر عالٍ)</h3>
            <p>هو جلفانومتر متصل معه مقاومة صغيرة جداً على <b>التوازي</b> تسمى (مجزئ التيار ).</p>
            
            

            <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin: 15px 0;">
                <div style="background:rgba(0,0,0,0.2); padding:10px; border-radius:10px; font-size:0.9rem;">
                    <b> وضيفتة مجزى التيار  :</b>
                    <ul style="padding-right:20px;">
                        <li>حماية ملف الجلفانومتر من الاحتراق.</li>
                        <li>زيادة مدى قياس الجهاز (يقيس تيار أكبر).</li>
                        <li>تقليل مقاومة الجهاز الكلية لزيادة الدقة.</li>
                    </ul>
                </div>
                <div class="law-box" style="margin:0; display:flex; align-items:center; justify-content:center;">
                    $$R_s = \frac{I_g R_g}{I - I_g}$$
                </div>
            </div>
            <p style="font-size: 0.9rem; color: #ff9800;">💡 <b>قاعدة مستر يوسف:</b>   <i class="fas fa-arrow-right"></i> يزداد المدى <i class="fas fa-arrow-right"></i> تقل الحساسية <i class="fas fa-arrow-right"></i> تزداد الدقة.</p>
        </div>

        <div class="device-box" style="background: rgba(156, 39, 176, 0.05); padding: 20px; border-radius: 15px; margin-bottom: 25px; border: 1px solid #9c27b0;">
            <h3 style="color: #9c27b0;"><i class="fas fa-bolt"></i> 3. الفولتميتر (قياس فرق جهد عالٍ)</h3>
            <p>هو جلفانومتر متصل معه مقاومة كبيرة جداً على <b>التوالي</b> تسمى (مضاعف الجهد ).</p>

            

            <div class="law-box">$$R_m = \frac{V - V_g}{I_g}$$</div>
            <div class="note-box" style="border-right-color: #9c27b0;">
                <b>الهدف من :</b> جعل مقاومة الفولتميتر الكلية كبيرة جداً، فلا يسحب تياراً كبيراً من الدائرة، مما يجعل القياس دقيقاً.
            </div>
        </div>

        <div class="device-box" style="background: rgba(255, 235, 59, 0.05); padding: 20px; border-radius: 15px; border: 1px solid #fbc02d;">
            <h3 style="color: #fbc02d;"><i class="fas fa-microchip"></i> 4. الأوميتر (قياس مقاومة مجهولة)</h3>
            <p><b>الفكرة العلمية:</b> العلاقة العكسية بين شدة التيار والمقاومة الكلية (قانون أوم).</p>
            
            

            <div class="law-box" style="font-size: 1.1rem;">
                $$I = \frac{V_B}{R_{device} + R_x}$$
            </div>
            <div style="background: #1a2244; padding: 15px; border-radius: 10px; border-right: 4px solid #fbc02d;">
                <b>ملاحظات هامة للحل السريع:</b>
                <ul style="margin: 5px 0;">
                   
                </ul>
            </div>
        </div>

    </div>
</div>
<div class="chapter-card animate__animated animate__fadeIn">
    <h2 style="color:var(--accent); border-bottom: 2px solid; display:inline-block; padding-bottom:10px;">
        <i class="fas fa-sync-alt"></i> الفصل الثالث: الحث الكهرومغناطيسي
    </h2>

    <div class="lesson-card">
        <div class="lesson-header" onclick="toggleLesson('l3-1')">
            <span>1. قانون فارادي ولينز</span>
            <i class="fas fa-chevron-down"></i>
        </div>
        <div id="l3-1" class="lesson-content">
            <p>يتولد تيار مستحث وقوة دافعة كهربائية مستحثة نتيجة قطع خطوط الفيض المغناطيسي.</p>
            
            <div class="law-box">
                $$emf = -N \frac{\Delta \phi_m}{\Delta t}$$
            </div>
            <div class="note-box">
                <strong>قاعدة لينز:</strong> التيار المستحث يعاكس التغير المسبب له (التعليل الفيزيائي للاشارة السالبة).
            </div>
        </div>
    </div>

    <div class="lesson-card">
        <div class="lesson-header" onclick="toggleLesson('l3-2')">
            <span>2. emf المستحثة في سلك مستقيم</span>
            <i class="fas fa-chevron-down"></i>
        </div>
        <div id="l3-2" class="lesson-content">
            <p>تتولد عند حركة سلك عمودياً على مجال مغناطيسي منتظم.</p>
            <div class="law-box">
                $$emf = - B \cdot L \cdot v \cdot \sin(\theta)$$
            </div>
            <p>تستخدم <strong>قاعدة اليد اليمنى لفليمنج</strong> لتحديد اتجاه التيار المستحث.</p>
        </div>
    </div>

    <div class="lesson-card">
        <div class="lesson-header" onclick="toggleLesson('l3-3')">
            <span>3. الحث المتبادل بين ملفين</span>
            <i class="fas fa-chevron-down"></i>
        </div>
        <div id="l3-3" class="lesson-content">
            <p>تأثير كهرومغناطيسي متبادل بين ملفين (ابتدائي وثانوي) يتغير في أحدهما التيار فيتولد في الآخر </p>
            
            <div class="law-box">
                $$emf_2 = -M \frac{\Delta I_1}{\Delta t}$$
            </div>
            <p>يقاس معامل الحث المتبادل (M) بوحدة <strong>الهنري (H)</strong>.</p>
        </div>
    </div>

    <div class="lesson-card">
        <div class="lesson-header" onclick="toggleLesson('l3-4')">
            <span>4. الحث الذاتي لملف</span>
            <i class="fas fa-chevron-down"></i>
        </div>
        <div id="l3-4" class="lesson-content">
            <p>ظاهرة تولد  مستحثة في نفس الملف عند تغير شدة التيار المار فيه.</p>
            <div class="law-box">
                $$emf = -L \frac{\Delta I}{\Delta t}$$
            </div>
            <div class="note-box">
                <strong>تذكر:</strong> معامل الحث الذاتي (L) يتوقف على (نفاذية الوسط، عدد اللفات، مساحة المقطع، طول الملف).
            </div>
        </div>
    </div>
          <div class="lesson-card" style="border-right-color: #ffd700;">
    <div class="lesson-header" onclick="toggleLesson('l3-5-updated')">
        <span style="color: #ffd700;"><i class="fas fa-bolt"></i> 5. المولد الكهربي (الدينامو) - القوانين الكاملة</span>
        <i class="fas fa-chevron-down"></i>
    </div>
    <div id="l3-5-updated" class="lesson-content">
        
        <div class="device-box" style="background: rgba(255, 255, 255, 0.05); padding: 15px; border-radius: 10px; margin-bottom: 20px;">
            <h4 style="color: var(--primary)">⚙️ السرعة والزمن والتردد</h4>
            <div class="law-box">
                $$\omega = 2\pi f = \frac{v}{r} \quad (rad/sec)$$
                $$f = \frac{N}{t} = \frac{1}{T} \quad , \quad T = \frac{t}{N} = \frac{1}{f}$$
                $$\theta = 2\pi f t \quad (\text{} \pi = 180^\circ)$$
            </div>
        </div>

        <div class="device-box" style="background: rgba(255, 255, 255, 0.05); padding: 15px; border-radius: 10px; margin-bottom: 20px;">
            <h4 style="color: var(--primary)">⚡ حساب القوة الدافعة الكهربية (emf)</h4>
            <div class="law-box">
                <strong>اللحظية:</strong> $$emf_{inst} = NBA\omega \sin \theta = emf_{max} \sin(2\pi f t)$$
                <strong>الفعالة:</strong> $$emf_{eff} = \frac{emf_{max}}{\sqrt{2}} = 0.707 \times emf_{max}$$
                <strong>المتوسطة (خلال ربع أو نصف دورة):</strong> $$emf_{avg} = \frac{2 \cdot emf_{max}}{\pi} = NBA \cdot 4f$$
                <strong>المتوسطة (خلال 3/4 دورة):</strong> $$emf_{avg} = \frac{2 \cdot emf_{max}}{3\pi} = \frac{4}{3} NBAf$$
            </div>
            <div class="note-box">
                * عند وضع الصفر (الوضع العمودي):  <br>
                * القيمة العظمى (الوضع الموازي) = °90 <br>
                * متوسط emf خلال دورة كاملة = <strong>صفر</strong>.
            </div>
        </div>

        <div class="device-box" style="background: rgba(255, 255, 255, 0.05); padding: 15px; border-radius: 10px; margin-bottom: 20px;">
            <h4 style="color: var(--primary)">🔌 حساب شدة التيار (I)</h4>
            <div class="law-box">
                $$I_{inst} = I_{max} \sin \theta \quad , \quad I_{max} = \frac{emf_{max}}{R}$$
                $$I_{eff} = \frac{I_{max}}{\sqrt{2}} = 0.707 \times I_{max}$$
                $$I_{avg} = \frac{2 I_{max}}{\pi} \text{ }$$
            </div>
        </div>

        <div class="device-box" style="background: rgba(255, 255, 255, 0.05); padding: 15px; border-radius: 10px; margin-bottom: 20px;">
            <h4 style="color: var(--primary)">🔥 الطاقة والقدرة (تستخدم القيم الفعالة فقط)</h4>
            <div class="law-box">
                <strong>القدرة:</strong> $$P_w = V_{eff} \cdot I_{eff} = I_{eff}^2 \cdot R = \frac{V_{eff}^2}{R}$$
                <strong>الطاقة:</strong> $$E = P_w \cdot t = I_{eff}^2 \cdot R \cdot t$$
            </div>
        </div>

        <div class="device-box" style="background: rgba(255, 215, 0, 0.1); padding: 15px; border-radius: 10px; border-right: 4px solid var(--accent);">
            <h4 style="color: var(--accent)">💡 ملاحظات ذهبية من السبورة:</h4>
            <ul style="list-style: none; padding-right: 10px;">
                <li>📍 <strong>للوصول لنصف القيمة العظمى:</strong> 《30°=£》 (لأول مرة).</li>
                <li>📍 <strong>للوصول للقيمة الفعالة:</strong> 《45°=£》.</li>
                <li>📍 <strong>عدد مرات الوصول للقيمة العظمى:</strong> 《2ft》 (من وضع الصفر).</li>
                <li>📍 <strong>عدد مرات الوصول للصفر:</strong> 《2ft + 1 》(من وضع الصفر).</li>
                <li>📍 <strong>علاقة الزمن بالزاوية:</strong> $$t = \frac{\theta}{360f}$$</li>
            </ul>
        </div>

    </div>
</div>


    <div class="lesson-card">
        <div class="lesson-header" onclick="toggleLesson('l3-6')">
            <span>6. المحول الكهربي</span>
            <i class="fas fa-chevron-down"></i>
        </div>
        <div id="l3-6" class="lesson-content">
            <p>يستخدم لرفع أو خفض الجهد المتردد. فكرة عمله: <strong>الحث المتبادل</strong>.</p>
        
            <div class="law-box">
                $$\frac{V_s}{V_p} = \frac{N_s}{N_p} = \frac{I_p}{I_s}$$
            </div>
            <p><strong>كفاءة المحول :</strong></p>
            <div class="law-box">
                $$\eta = \frac{P_s}{P_p} \times 100 = \frac{V_s I_s}{V_p I_p} \times 100$$
            </div>
        </div>
    </div>

    <div class="lesson-card">
        <div class="lesson-header" onclick="toggleLesson('l3-7')">
            <span>7. المحرك الكهربي (الموتور)</span>
            <i class="fas fa-chevron-down"></i>
        </div>
        <div id="l3-7" class="lesson-content">
            <p>يحول الطاقة الكهربائية إلى طاقة حركية. يعتمد على <strong>عزم الازدواج</strong>.</p>
            <div class="note-box">
                <strong>سر استمرار الدوران:</strong> وجود القوة الدافعة الكهربائية العكسية التي تعمل على <strong>انتظام</strong> سرعة دوران الموتور.
            </div>
            <p>يتم استخدام عدة ملفات بينها زوايا صغيرة لزيادة كفاءة الموتور وجعل العزم ثابتاً عند النهاية العظمى.</p>
        </div>
    </div>
</div>


        
        
    </div> <div style="padding: 0 5%; max-width: 1200px; margin: auto;">
        <button 
        </button>
    </div>


    <div id="chem-area" class="content-area">
        <button class="btn-back" onclick="goHome()">العودة للرئيسية</button>
        <h2 style="text-align:center; color:var(--chem-color); margin-bottom:30px;">منصة الكيمياء العضوية</h2>
        
    <div id="student-area">
        <div class="lesson-card">
            <div class="lesson-header" onclick="toggleLesson('l1')">
                <h3>1. مقدمة الكيمياء العضوية ونظرية برزيليوس</h3>
                <i class="fas fa-plus"></i>
            </div>
            <div id="l1" class="lesson-content">
                <div class="theory-block">
                    <h4>نظرية القوة الحيوية:</h4>
                    <p>افترض برزيليوس أن المركبات العضوية تتكون فقط داخل خلايا الكائنات الحية بواسطة قوة حيوية ولا يمكن تحضيرها في المختبر.</p>
                    <h4>تجربة فولر :</h4>
                    <p>تمكن من دحض النظرية بتحضير "اليوريا" (مركب عضوي) من تسخين محلول مائي لمركبين غير عضويين:</p>
                    <div class="equation-box">$$NH_4Cl + AgCNO \xrightarrow{\Delta} AgCl \downarrow + NH_4CNO$$</div>
                    <div class="equation-box">$$NH_4CNO \xrightarrow{\Delta} NH_2CONH_2 $$</div>
                </div>
            </div>
        </div>

        <div class="lesson-card">
            <div class="lesson-header" onclick="toggleLesson('l2')">
                <h3>2. الألكانات (البارافينات) - السلسلة المتجانسة</h3>
                <i class="fas fa-plus"></i>
            </div>
            <div id="l2" class="lesson-content">
                <div class="theory-block">
                    <h4>القانون العام:</h4>
                    <p>تخضع للصيغة العامة [Cn-H(2n+2)]. جميع روابطها أحادية من النوع سيجما (sigma) القوية صعبة الكسر.</p>
                    <h4>تسمية :</h4>
                    <p>تعتمد على تحديد أطول سلسلة كربونية مستمرة، والترقيم من الطرف الأقرب للتفرع.</p>
                </div>
            </div>
        </div>

        <div class="lesson-card">
            <div class="lesson-header" onclick="toggleLesson('l3')">
                <h3>3. غاز الميثان CH-4 </h3>
                <i class="fas fa-plus"></i>
            </div>
            <div id="l3" class="lesson-content">
                <div class="theory-block">
                    <h4>التحضير:</h4>
                    <p>بالتقطير الجاف لأسيتات الصوديوم مع الجير الصودي (NaOH + CaO):</p>
                    <div class="equation-box">CH_3COONa + NaOH --> CH_4 + Na2-CO3</div>
                    <h4>الأهمية الاقتصادية:</h4>
                    <p>1. الحصول على أسود الكربون (عند ° 1000 بمعزل عن الهواء).<br>2. الغاز المائي (عند°725  مع بخار الماء).</p>
                </div>
            </div>
        </div>

        <div class="lesson-card">
            <div class="lesson-header" onclick="toggleLesson('l4')">
                <h3>4. الألكينات (الأوليفينات)</h3>
                <i class="fas fa-plus"></i>
            </div>
            <div id="l4" class="lesson-content">
                <div class="theory-block">
                    <h4>الصيغة العامة:</h4>
                    <p>Cn-H(2n) (تحتوي على رابطة مزدوجة واحدة C=C).</p>
                    <h4>قاعدة ماركونيكوف:</h4>
                    <p>عند إضافة متفاعل غير متماثل (HX) إلى ألكين غير متماثل، فإن الهيدروجين يذهب لذرة الكربون الغنية بالهيدروجين، والهالوجين للفقيرة.</p>
                    <div class="equation-box">$$CH_3-CH=CH_2 + HBr \to CH_3-CH(Br)-CH_3$$</div>
                </div>
            </div>
        </div>

        <div class="lesson-card">
            <div class="lesson-header" onclick="toggleLesson('l5')">
                <h3>5. الألكاينات (الأسيتيلينات)</h3>
                <i class="fas fa-plus"></i>
            </div>
            <div id="l5" class="lesson-content">
                <div class="theory-block">
                    <h4>الصيغة:</h4>
                    <p>Cn-H(2n-2) (رابطة ثلاثية ).</p>
                    <h4>الهيدرة الحفزية للإيثاين:</h4>
                    <p>تنتج الأسيتالدهيد الذي يتأكسد لحمض أسيتيك أو يُختزل لإيثانول.</p>
                    <div class="equation-box">$$C_2H_2 + H_2O \xrightarrow{H_2SO_4/HgSO_4} CH_3CHO$$</div>
                </div>
            </div>
        </div>

        <div class="lesson-card">
            <div class="lesson-header" onclick="toggleLesson('l6')">
                <h3>6. الهيدروكربونات الحلقية (الأليفاتية المشبعة)</h3>
                <i class="fas fa-plus"></i>
            </div>
            <div id="l6" class="lesson-content">
                <div class="theory-block">
                    <h4>الاستقرار:</h4>
                    <p>⚙️ سيتوفر قريبا
                </div>
            </div>
        </div>

        <div class="lesson-card">
            <div class="lesson-header" onclick="toggleLesson('l7')">
                <h3>7. البنزين العطري (C6H6)</h3>
                <i class="fas fa-plus"></i>
            </div>
            <div id="l7" class="lesson-content">
                <div class="theory-block">
                    <h4>التحضير:</h4>
                    <p>1. بلمرة ثلاثية للإيثاين. <br> 2. إعادة تشكيل محفزة للهكسان العادي.</p>
                    <h4>تفاعلات الفريدل كرافت (الألكلة):</h4>
                    <div class="equation-box">$$C_6H_6 + CH_3Cl \xrightarrow{AlCl_3} C_6H_5-CH_3 (Toluene) + HCl$$</div>
                </div>
            </div>
        </div>

        <div class="lesson-card">
            <div class="lesson-header" onclick="toggleLesson('l8')">
                <h3>8. تسمية وتحضير الكحولات</h3>
                <i class="fas fa-plus"></i>
            </div>
            <div id="l8" class="lesson-content">
                <div class="theory-block">
                    <h4>التحضير العام:</h4>
                    <p>تحلل مائي لهاليدات الألكيل في وسط قلوي قوي (KOH):</p>
                    <div class="equation-box">$$R-X + KOH \xrightarrow{\Delta} R-OH + KX$$</div>
                </div>
            </div>
        </div>

        <div class="lesson-card">
            <div class="lesson-header" onclick="toggleLesson('l9')">
                <h3>9. الخواص العامة للكحولات</h3>
                <i class="fas fa-plus"></i>
            </div>
            <div id="l9" class="lesson-content">
                <div class="theory-block">
                    <h4>الأكسدة:</h4>
                    <p>الكحولات الأولية تتأكسد على مرحلتين (ألديهيد ثم حمض)، الثانوية على مرحلة (كيتون)، الثالثية لا تتأكسد لعدم وجود هيدروجين على كربونول.</p>
                </div>
            </div>
        </div>

        <div class="lesson-card">
            <div class="lesson-header" onclick="toggleLesson('l10')">
                <h3>10. الفينولات</h3>
                <i class="fas fa-plus"></i>
            </div>
            <div id="l10" class="lesson-content">
                <div class="theory-block">
                    <h4>الحامضية:</h4>
                    <p>الفينول أكثر حامضية من الكحول (حمض الكربوليك) لأن حلقة البنزين تسحب الإلكترونات فتطول الرابطة (O-H) وتسهل انفصال البروتون.</p>
                    <div class="equation-box">$$C_6H_5OH + NaOH \to C_6H_5ONa + H_2O$$</div>
                </div>
            </div>
        </div>

        <div class="lesson-card">
            <div class="lesson-header" onclick="toggleLesson('l11')">
                <h3>11. الأحماض الكربوكسيلية</h3>
                <i class="fas fa-plus"></i>
            </div>
            <div id="l11" class="lesson-content">
                <div class="theory-block">
                    <h4>المجموعة الوظيفية:</h4>
                    <p>مجموعة الكربوكسيل (-COOH).</p>
                    <h4>الخاصية الحامضية:</h4>
                    <p>تتفاعل مع الفلزات، الأكاسيد، الهيدروكسيدات، والكربونات (كشف الحامضية).</p>
                </div>
            </div>
        </div>

        <div class="lesson-card">
            <div class="lesson-header" onclick="toggleLesson('l12')">
                <h3>12. الاسترات</h3>
                <i class="fas fa-plus"></i>
            </div>
            <div id="l12" class="lesson-content">
                <div class="theory-block">
                    <h4>تفاعل الأسترة:</h4>
                    <div class="equation-box">$$R-COOH + R'-OH \rightleftharpoons R-COOR' + H_2O$$</div>
                    <p>الاسترات كزيوت ودهون، التصبن هو التحلل المائي للاستر في وسط قلوي.</p>
                </div>
            </div>
        </div>

    <script>
        function showSection(id) {
            document.getElementById('home-page').style.display = 'none';
            document.querySelectorAll('.content-area').forEach(a => a.style.display = 'none');
            document.getElementById(id).style.display = 'block';
            window.scrollTo(0,0);
            if(window.MathJax) MathJax.typeset();
        }

        function goHome() {
            document.querySelectorAll('.content-area').forEach(a => a.style.display = 'none');
            document.getElementById('home-page').style.display = 'flex';
        }

        function toggleLesson(id) {
            let content = document.getElementById(id);
            content.style.display = content.style.display === 'block' ? 'none' : 'block';
            if(window.MathJax) MathJax.typeset();
        }
    </script>
</body>
</html>
