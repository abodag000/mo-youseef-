 <html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>إمبراطورية الفيزياء | مستر محمد يوسف</title>
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"/>
    
    <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
    <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

    <style>
        :root {
            --primary: #00d2ff;
            --secondary: #3a7bd5;
            --accent: #ffd700;
            --dark-bg: #050a18;
            --card-bg: rgba(255, 255, 255, 0.05);
            --glass-border: rgba(255, 255, 255, 0.1);
            --text-main: #e2e8f0;
        }

        * { box-sizing: border-box; transition: all 0.3s ease; }

        body {
            margin: 0;
            font-family: 'Cairo', sans-serif;
            background: var(--dark-bg);
            color: var(--text-main);
            overflow-x: hidden;
            line-height: 1.6;
        }

        /* Background Animation */
        .bg-glow {
            position: fixed;
            inset: 0;
            z-index: -1;
            background: radial-gradient(circle at 50% 50%, #1a2a6c 0%, #b21f1f 50%, #fdbb2d 100%);
            opacity: 0.15;
            filter: blur(100px);
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 15px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: rgba(5, 10, 24, 0.8);
            backdrop-filter: blur(15px);
            z-index: 1000;
            border-bottom: 1px solid var(--glass-border);
        }

        .logo { font-size: 1.6rem; font-weight: 900; letter-spacing: 1px; }
        .logo span { color: var(--primary); text-shadow: 0 0 10px var(--primary); }

        /* Buttons */
        .btn-glow {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            border: none;
            padding: 12px 35px;
            border-radius: 50px;
            font-weight: bold;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(0, 210, 255, 0.4);
            text-decoration: none;
            display: inline-block;
        }

        .btn-glow:hover {
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 6px 20px rgba(0, 210, 255, 0.6);
        }

        /* Hero Section */
        #home-page {
            height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            background: url('https://www.transparenttextures.com/patterns/carbon-fibre.png');
        }

        h1.hero-title {
            font-size: clamp(2rem, 8vw, 4rem);
            margin-bottom: 10px;
            background: linear-gradient(to right, #fff, var(--primary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        /* Student Area */
        #student-area { display: none; padding: 120px 5%; max-width: 1200px; margin: auto; }

        .chapter-card {
            background: var(--card-bg);
            padding: 30px;
            border-radius: 25px;
            margin-bottom: 40px;
            border: 1px solid var(--glass-border);
            backdrop-filter: blur(10px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }

        .lesson-card {
            background: rgba(255,255,255,0.03);
            border-radius: 15px;
            margin: 15px 0;
            border-right: 5px solid var(--primary);
            overflow: hidden;
        }

        .lesson-header {
            padding: 20px;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 1.2rem;
            font-weight: 600;
        }

        .lesson-header:hover { background: rgba(255,255,255,0.08); }

        .lesson-content {
            display: none;
            padding: 25px;
            border-top: 1px solid var(--glass-border);
            background: rgba(0,0,0,0.2);
            animation: fadeIn 0.5s ease;
        }

        /* Physics Elements */
        .law-box {
            background: rgba(0, 210, 255, 0.05);
            border: 1px solid var(--primary);
            padding: 20px;
            border-radius: 15px;
            margin: 20px 0;
            text-align: center;
            font-size: 1.4rem;
            color: var(--accent);
            box-shadow: inset 0 0 15px rgba(0, 210, 255, 0.1);
        }

        .note-box {
            background: rgba(255, 215, 0, 0.1);
            border-right: 4px solid var(--accent);
            padding: 15px;
            margin: 15px 0;
            font-size: 0.95rem;
        }

        .unit-badge {
            background: var(--secondary);
            padding: 2px 8px;
            border-radius: 4px;
            font-size: 0.8rem;
            margin-right: 5px;
        }

        /* Modals */
        .modal-overlay {
            position: fixed;
            inset: 0;
            background: rgba(0,0,0,0.85);
            backdrop-filter: blur(8px);
            display: none;
            align-items: center;
            justify-content: center;
            z-index: 2000;
        }

        .modal-box {
            background: #0c1433;
            padding: 40px;
            border-radius: 30px;
            width: 90%;
            max-width: 450px;
            border: 1px solid var(--primary);
            text-align: center;
            box-shadow: 0 0 50px rgba(0, 210, 255, 0.2);
        }

        input {
            width: 100%;
            padding: 15px;
            margin: 15px 0;
            border-radius: 12px;
            border: 1px solid var(--glass-border);
            background: #1a2244;
            color: white;
            font-size: 1rem;
            outline: none;
        }

        input:focus { border-color: var(--primary); }

        @keyframes fadeIn { from { opacity: 0; transform: translateY(-10px); } to { opacity: 1; transform: translateY(0); } }

    </style>
</head>
<body>

    <div class="bg-glow"></div>

    <nav>
        <div class="logo">MOHMED_YOUSSEF <span>PHYSICS</span></div>
        <button onclick="showModal('teacher')" style="background:none; border:1px solid var(--primary); color:white; padding:8px 20px; border-radius:10px; cursor:pointer;">إدارة</button>
    </nav>

    <div id="home-page">
        <h1 class="hero-title animate__animated animate__zoomIn">كوكب الفيزياء 🦅</h1>
        <p class="animate__animated animate__fadeInUp" style="font-size: 1.4rem; color:#cbd5e1; margin-bottom: 30px;">طريقك نحو الـ 60 درجة مع ستر محمد يوسف</p>
        <button class="btn-glow animate__animated animate__pulse animate__infinite" onclick="showModal('student')">
            ابدأ رحلة التفوق الآن <i class="fas fa-bolt" style="margin-right:10px"></i>
        </button>
    </div>

    <div id="student-area">
        <div id="welcome-banner" style="text-align: center; margin-bottom: 50px;">
            <h2 id="welcome-txt" style="font-size: 2.5rem; color: var(--primary);"></h2>
            <p>"الطريق إلى النجاح مليء بالتحديات، لكن الثبات هو ما يحقق النصر".</p>
        </div>
        
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
                        <li><span class="unit-badge">R</span> المقاومة - تقاس بالأوم ($\Omega$)</li>
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
                                <li>التيار ($I$) ثابت في جميع المقاومات.</li>
                                <li>الجهد يتجزأ بنسب طردية مع المقاومات.</li>
                            </ul>
                            <div class="law-box" style="font-size: 1.1rem;">$$R_{eq} = R_1 + R_2 + R_3...$$</div>
                        </div>
                        <div style="background: rgba(255,255,255,0.05); padding: 15px; border-radius: 10px;">
                            <h4 style="color: var(--primary)">🟡 التوصيل على التوازي</h4>
                            <ul>
                                <li>الغرض: الحصول على مقاومة صغيرة جداً.</li>
                                <li>فرق الجهد ($V$) ثابت.</li>
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
                    <p>أما عزم الازدواج ($\tau$) فهو أساس عمل الموتور والجلفانومتر:</p>
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


        <button class="btn-glow" style="background:#ef4444; width:100%; margin-top:50px;" onclick="location.reload()">تسجيل خروج</button>
        
    </div>
               <button class="btn-glow" style="background:#1a2244; width:100%; margin-top:50px;" onclick="location.reload()">𝐴𝐵𝐷𝐸𝐿𝑅𝑈𝐻𝑀𝐴𝑁 𝐸𝐿𝐵𝐿𝐴𝑆𝑌</button>
    <div id="modal-student" class="modal-overlay">
        <div class="modal-box animate__animated animate__backInUp">
            <i class="fas fa-user-grad" style="font-size: 3rem; color: var(--primary); margin-bottom: 20px;"></i>
            <h2>دخول منطقة العباقرة</h2>
            <input type="text" id="s-code" placeholder="أدخل كود الاشتراك الخاص بك">
            <button class="btn-glow" style="width:100%" onclick="loginStudent()">دخول الآن</button>
            <p onclick="hideModals()" style="cursor:pointer; opacity:0.6; margin-top:20px;">إغلاق النافذة</p>
        </div>
    </div>

    <div id="modal-teacher" class="modal-overlay">
        <div class="modal-box">
            <h2>لوحة التحكم الإدارية</h2>
            <input type="text" id="t-user" placeholder="اسم المستخدم">
            <input type="password" id="t-pass" placeholder="كلمة المرور">
            <button class="btn-glow" style="width:100%" onclick="loginTeacher()">دخول</button>
            <p onclick="hideModals()" style="cursor:pointer; opacity:0.6; margin-top:20px;">رجوع</p>
        </div>
    </div>

    <div id="dashboard" style="display:none; padding:120px 5%; max-width: 800px; margin: auto;">
        <div class="chapter-card">
            <h3><i class="fas fa-plus-circle"></i> توليد أكواد جديدة</h3>
            <input type="text" id="new-name" placeholder="اسم الطالب الثلاثي">
            <button class="btn-glow" style="width:100%" onclick="generateCode()">إنشاء الكود</button>
            <div id="codes-list" style="margin-top:30px; text-align: right; background: rgba(0,0,0,0.3); padding: 20px; border-radius: 15px;"></div>
        </div>
    </div>

    <script>
        let db = JSON.parse(localStorage.getItem('phys_db')) || [{name: "  محمد يوسف", code: "PH-2008"}];

        function showModal(id) { document.getElementById('modal-'+id).style.display = 'flex'; }
        function hideModals() { document.querySelectorAll('.modal-overlay').forEach(m => m.style.display = 'none'); }
        
        function toggleLesson(id) {
            let content = document.getElementById(id);
            let isVisible = content.style.display === 'block';
            
            // Close all first for accordion effect (optional)
            // document.querySelectorAll('.lesson-content').forEach(c => c.style.display = 'none');
            
            content.style.display = isVisible ? 'none' : 'block';
            
            // Re-render MathJax if needed
            if(window.MathJax) {
                MathJax.typeset();
            }
        }

        function generateCode() {
            let name = document.getElementById('new-name').value;
            if(!name) return alert("اكتب اسم الطالب!");
            let code = "PH-" + Math.floor(1000 + Math.random()*9000);
            db.push({name, code});
            localStorage.setItem('phys_db', JSON.stringify(db));
            renderCodes();
            document.getElementById('new-name').value = "";
        }

        function renderCodes() {
            document.getElementById('codes-list').innerHTML = "<h4>الأكواد المسجلة:</h4>" + 
                db.map(s => `<div style="border-bottom:1px solid #333; padding:10px 0;">${s.name} : <b style="color:var(--primary)">${s.code}</b></div>`).join('');
        }

        function loginTeacher() {
            if(document.getElementById('t-user').value === "Joo" && document.getElementById('t-pass').value === "joo") {
                document.getElementById('home-page').style.display = 'none';
                document.getElementById('dashboard').style.display = 'block';
                hideModals(); renderCodes();
            } else { alert("بيانات الإدارة خطأ!"); }
        }

        function loginStudent() {
            let code = document.getElementById('s-code').value;
            let student = db.find(s => s.code === code);
            if(student) {
                document.getElementById('home-page').style.display = 'none';
                document.getElementById('student-area').style.display = 'block';
                document.getElementById('welcome-txt').innerText = `يا أهلاً بالدكتور : ${student.name} ❤️`;
                hideModals();
            } else { alert("كود الاشتراك غير صحيح أو انتهت صلاحيته!"); }
        }
    </script>
</body>
</html>
