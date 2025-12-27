<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>عالم يوسف فرج الزيدي - شاعر العراق المميز</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <link href="https://fonts.googleapis.com/css2?family=Scheherazade+New:wght@400;700&family=Amiri:wght@400;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Amiri', serif;
            background: linear-gradient(135deg, #0c2461 0%, #1e3799 50%, #4a69bd 100%);
            color: #f7f1e3;
            overflow-x: hidden;
            line-height: 1.8;
        }

        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(12, 36, 97, 0.9);
            padding: 1rem 2rem;
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }

        .logo {
            font-family: 'Scheherazade New', serif;
            font-size: 2.2rem;
            font-weight: 700;
            color: #f7f1e3;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }

        .logo span {
            color: #eccc68;
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav li {
            margin: 0 1rem;
        }

        nav a {
            color: #f7f1e3;
            text-decoration: none;
            font-size: 1.2rem;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            transition: all 0.3s ease;
        }

        nav a:hover {
            background-color: #eccc68;
            color: #0c2461;
        }

        .container {
            display: flex;
            min-height: 100vh;
            padding-top: 80px;
        }

        .sidebar {
            width: 300px;
            background: rgba(30, 55, 153, 0.85);
            padding: 2rem;
            overflow-y: auto;
            border-left: 3px solid #eccc68;
        }

        .main-content {
            flex: 1;
            padding: 2rem;
            position: relative;
        }

        #scene-container {
            width: 100%;
            height: 600px;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            margin-bottom: 2rem;
        }

        .section-title {
            font-family: 'Scheherazade New', serif;
            font-size: 2.2rem;
            color: #eccc68;
            margin-bottom: 1.5rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid #eccc68;
            text-align: center;
        }

        .poem-card {
            background: rgba(247, 241, 227, 0.1);
            border-radius: 10px;
            padding: 1.5rem;
            margin-bottom: 1.5rem;
            transition: transform 0.3s ease;
            cursor: pointer;
            border-right: 4px solid #eccc68;
        }

        .poem-card:hover {
            transform: translateX(-10px);
            background: rgba(236, 204, 104, 0.2);
        }

        .poem-title {
            font-size: 1.5rem;
            color: #eccc68;
            margin-bottom: 0.5rem;
        }

        .poem-excerpt {
            font-size: 1.2rem;
            color: #f7f1e3;
            line-height: 1.8;
        }

        .about-section {
            background: rgba(30, 55, 153, 0.7);
            border-radius: 15px;
            padding: 2rem;
            margin-bottom: 2rem;
            border: 1px solid #4a69bd;
        }

        .quote {
            font-size: 1.5rem;
            font-style: italic;
            text-align: center;
            padding: 2rem;
            color: #eccc68;
            border-top: 1px solid #4a69bd;
            border-bottom: 1px solid #4a69bd;
            margin: 2rem 0;
        }

        .stats {
            display: flex;
            justify-content: space-around;
            margin: 2rem 0;
        }

        .stat-box {
            text-align: center;
            padding: 1.5rem;
            background: rgba(236, 204, 104, 0.15);
            border-radius: 10px;
            flex: 1;
            margin: 0 1rem;
        }

        .stat-number {
            font-size: 2.5rem;
            color: #eccc68;
            font-weight: bold;
        }

        .stat-label {
            font-size: 1.2rem;
            margin-top: 0.5rem;
        }

        .btn {
            display: inline-block;
            background: #eccc68;
            color: #0c2461;
            padding: 0.8rem 2rem;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.2rem;
            margin: 1rem 0;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
        }

        .btn:hover {
            background: #f7f1e3;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(236, 204, 104, 0.4);
        }

        .btn i {
            margin-left: 0.5rem;
        }

        .interactive-section {
            background: rgba(12, 36, 97, 0.7);
            border-radius: 15px;
            padding: 2rem;
            margin-top: 2rem;
            text-align: center;
        }

        footer {
            background: rgba(12, 36, 97, 0.95);
            text-align: center;
            padding: 2rem;
            margin-top: 3rem;
            border-top: 3px solid #eccc68;
        }

        .social-icons {
            margin-top: 1rem;
        }

        .social-icons a {
            color: #f7f1e3;
            font-size: 1.5rem;
            margin: 0 1rem;
            transition: all 0.3s ease;
        }

        .social-icons a:hover {
            color: #eccc68;
            transform: translateY(-5px);
        }

        /* تصميم متجاوب */
        @media (max-width: 1024px) {
            .container {
                flex-direction: column;
            }
            
            .sidebar {
                width: 100%;
                border-left: none;
                border-bottom: 3px solid #eccc68;
            }
            
            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }
            
            nav li {
                margin: 0.5rem;
            }
        }

        @media (max-width: 768px) {
            .logo {
                font-size: 1.8rem;
            }
            
            .section-title {
                font-size: 1.8rem;
            }
            
            .stats {
                flex-direction: column;
            }
            
            .stat-box {
                margin: 0.5rem 0;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="logo">عالم <span>يوسف فرج الزيدي</span></div>
        <nav>
            <ul>
                <li><a href="#home"><i class="fas fa-home"></i> الرئيسية</a></li>
                <li><a href="#poems"><i class="fas fa-book-open"></i> القصائد</a></li>
                <li><a href="#about"><i class="fas fa-user"></i> عن الشاعر</a></li>
                <li><a href="#interact"><i class="fas fa-comments"></i> تفاعل</a></li>
            </ul>
        </nav>
    </header>

    <div class="container">
        <div class="main-content">
            <h1 class="section-title" id="home">رحابة الروح.. عالم يوسف فرج الزيدي الشعري</h1>
            
            <div id="scene-container">
                <!-- سيتم إنشاء المشهد ثلاثي الأبعاد هنا -->
            </div>
            
            <div class="about-section" id="about">
                <h2 class="section-title">من هو يوسف فرج الزيدي؟</h2>
                <p>شاعر عراقي مبدع، ولد في أرض الرافدين التي تغذي روحه الإبداعية. يتميز يوسف بشعره العميق الذي يمزج بين الأصالة العراقية والرؤى الإنسانية المعاصرة. برغم من أنه لم يجد من يفهمه بعد بالكامل، إلا أن قصائده تلمس شغاف القلوب وتنقل تجارب إنسانية فريدة.</p>
                <p>يوسف يؤمن بأن الجمال يكمن في التفاصيل الصغيرة، وفي قدرة الكلمة على خلق عوالم موازية. يعيش في العراق لكن أحلامه لا تعرف حدوداً.</p>
                
                <div class="quote">
                    "أنا لا أكتب لأُفهم.. أكتب لأن الكلمات تبحث عن منازل في قلوب لا تعرف الغربة"
                </div>
                
                <div class="stats">
                    <div class="stat-box">
                        <div class="stat-number">١٥+</div>
                        <div class="stat-label">سنة من الإبداع</div>
                    </div>
                    <div class="stat-box">
                        <div class="stat-number">٢٠٠+</div>
                        <div class="stat-label">قصيدة مكتوبة</div>
                    </div>
                    <div class="stat-box">
                        <div class="stat-number">٣</div>
                        <div class="stat-label">دواوين شعرية</div>
                    </div>
                </div>
            </div>
            
            <div class="interactive-section" id="interact">
                <h2 class="section-title">شارك في فهم يوسف</h2>
                <p>كن أنت من يفهم هذا الشاعر المميز. اقرأ قصائده، شاركنا رأيك، وساعد في نشر إبداعه.</p>
                <button class="btn" id="understand-btn">
                    <i class="fas fa-heart"></i> أنا أفهمك يا يوسف
                </button>
                <p id="understanding-counter">عدد المتفهمين: <span id="counter">١٣٧</span> شخص</p>
            </div>
        </div>
        
        <div class="sidebar">
            <h2 class="section-title" id="poems">قصائد مختارة</h2>
            
            <div class="poem-card" onclick="showPoem('نهر الذكريات')">
                <h3 class="poem-title">نهر الذكريات</h3>
                <p class="poem-excerpt">دجلة يحمل في ضفافه أسرار قرون.. وأنا أحمل في كلماتي شوقاً لنهر لم يعد يعرفني.. ذكريات كالسفن البعيدة تبحر في عيني ولا تصل إلى شطآن قلبك.</p>
            </div>
            
            <div class="poem-card" onclick="showPoem('قهوة البادية')">
                <h3 class="poem-title">قهوة البادية</h3>
                <p class="poem-excerpt">في فنجان القهوة المرّة أرى وجه العراق.. ترسبات الألم في القاع و رغوة الأمل تطفو على السطح.. و بين هذا وذاك، عطر النخيل يذكرني بأن الجذور لا تموت.</p>
            </div>
            
            <div class="poem-card" onclick="showPoem('ليل بغداد')">
                <h3 class="poem-title">ليل بغداد</h3>
                <p class="poem-excerpt">ليل بغداد يحمل أنين التاريخ في صمته.. وأنت تحملين غيابك كجرح لا يندمل.. المصابيح القديمة تومض كذكريات متعبة، والشوارع تحتفظ بأنفاس العابرين ككنوز مفقودة.</p>
            </div>
            
            <div class="poem-card" onclick="showPoem('حروف منسية')">
                <h3 class="poem-title">حروف منسية</h3>
                <p class="poem-excerpt">أكتب بقلم من أشواك النخيل.. على ورق من سعف الذكريات.. حروفي تبحث عن معانٍ في قلوب لا تقرأ إلا لغة الفراق.. وأنا هنا، أحاول أن أترجم صمتك إلى قصيدة.</p>
            </div>
            
            <div class="poem-card" onclick="showPoem('ألوان الوطن')">
                <h3 class="poem-title">ألوان الوطن</h3>
                <p class="poem-excerpt">أزرق دجلة، ذهب الصحراء، أخضر النخيل.. وأسود العيون التي تراقص النجوم.. في لوحة العراق، أكون أنا الظل الذي يحمي الألوان من بهتان الزمن.</p>
            </div>
            
            <h2 class="section-title" style="margin-top: 3rem;">سمات شعره</h2>
            <ul style="padding-right: 1.5rem; font-size: 1.2rem;">
                <li style="margin-bottom: 0.8rem;">عمق في التعبير عن الهوية العراقية</li>
                <li style="margin-bottom: 0.8rem;">استخدام الصور البلاغية المبتكرة</li>
                <li style="margin-bottom: 0.8rem;">الربط بين الذاتي والجماعي</li>
                <li style="margin-bottom: 0.8rem;">التركيز على الجماليات في التفاصيل</li>
                <li style="margin-bottom: 0.8rem;">نبرة حزينة لكنها مليئة بالأمل</li>
            </ul>
        </div>
    </div>
    
    <footer>
        <p>موقع تفاعلي ثلاثي الأبعاد مخصص للشاعر العراقي يوسف فرج الزيدي</p>
        <p>صمم بكثير من التقدير لفن لم يجد من يفهمه بعد</p>
        <div class="social-icons">
            <a href="#"><i class="fab fa-twitter"></i></a>
            <a href="#"><i class="fab fa-facebook"></i></a>
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="#"><i class="fas fa-envelope"></i></a>
        </div>
        <p style="margin-top: 1rem; font-size: 0.9rem;">© 2023 عالم يوسف فرج الزيدي الشعري. جميع الحقوق محفوظة.</p>
    </footer>

    <script>
        // المشهد ثلاثي الأبعاد الأساسي
        function init3DScene() {
            const container = document.getElementById('scene-container');
            
            // إنشاء المشهد
            const scene = new THREE.Scene();
            scene.background = new THREE.Color(0x0c2461);
            
            // الكاميرا
            const camera = new THREE.PerspectiveCamera(75, container.clientWidth / container.clientHeight, 0.1, 1000);
            camera.position.z = 5;
            
            // العارض
            const renderer = new THREE.WebGLRenderer({ antialias: true });
            renderer.setSize(container.clientWidth, container.clientHeight);
            container.appendChild(renderer.domElement);
            
            // الإضاءة
            const ambientLight = new THREE.AmbientLight(0xffffff, 0.6);
            scene.add(ambientLight);
            
            const directionalLight = new THREE.DirectionalLight(0xeccc68, 0.8);
            directionalLight.position.set(5, 5, 5);
            scene.add(directionalLight);
            
            // إنشاء كائنات ثلاثية الأبعاد
            const geometry = new THREE.IcosahedronGeometry(1.5, 1);
            const material = new THREE.MeshPhongMaterial({ 
                color: 0xeccc68,
                shininess: 100,
                transparent: true,
                opacity: 0.9
            });
            const mesh = new THREE.Mesh(geometry, material);
            scene.add(mesh);
            
            // إنشاء نجوم في الخلفية
            const starGeometry = new THREE.SphereGeometry(0.05, 8, 8);
            const starMaterial = new THREE.MeshBasicMaterial({ color: 0xffffff });
            
            for (let i = 0; i < 200; i++) {
                const star = new THREE.Mesh(starGeometry, starMaterial);
                star.position.x = (Math.random() - 0.5) * 30;
                star.position.y = (Math.random() - 0.5) * 30;
                star.position.z = (Math.random() - 0.5) * 30;
                scene.add(star);
            }
            
            // إنشاء أهرامات صغيرة (رمز للعراق القديم)
            const pyramidGeometry = new THREE.ConeGeometry(0.5, 1, 4);
            const pyramidMaterial = new THREE.MeshPhongMaterial({ color: 0x4a69bd });
            
            for (let i = 0; i < 5; i++) {
                const pyramid = new THREE.Mesh(pyramidGeometry, pyramidMaterial);
                pyramid.position.x = (Math.random() - 0.5) * 8;
                pyramid.position.y = -2;
                pyramid.position.z = (Math.random() - 0.5) * 8;
                scene.add(pyramid);
            }
            
            // التحريك
            function animate() {
                requestAnimationFrame(animate);
                
                mesh.rotation.x += 0.005;
                mesh.rotation.y += 0.01;
                
                renderer.render(scene, camera);
            }
            
            animate();
            
            // تغيير حجم المشهد عند تغيير حجم النافذة
            window.addEventListener('resize', function() {
                camera.aspect = container.clientWidth / container.clientHeight;
                camera.updateProjectionMatrix();
                renderer.setSize(container.clientWidth, container.clientHeight);
            });
        }
        
        // تفعيل المشهد ثلاثي الأبعاد عند تحميل الصفحة
        window.addEventListener('load', function() {
            init3DScene();
        });
        
        // وظيفة عرض القصائد
        function showPoem(title) {
            alert(`ستفتح الآن قصيدة "${title}" في نافذة جديدة. في النسخة الكاملة من الموقع، ستعرض القصيدة كاملة مع مؤثرات بصرية وسمعية.`);
        }
        
        // تفاعل "أنا أفهمك يا يوسف"
        document.getElementById('understand-btn').addEventListener('click', function() {
            let counter = document.getElementById('counter');
            let currentCount = parseInt(counter.textContent);
            currentCount++;
            counter.textContent = currentCount;
            
            // تغيير نص الزر مؤقتاً
            const btn = this;
            const originalText = btn.innerHTML;
            btn.innerHTML = '<i class="fas fa-check"></i> شكراً لفهمك!';
            btn.style.backgroundColor = '#4a69bd';
            
            setTimeout(function() {
                btn.innerHTML = originalText;
                btn.style.backgroundColor = '';
            }, 2000);
            
            // عرض رسالة تأكيد
            alert('شكراً لك! أنت الآن واحد ممن يفهمون الشاعر يوسف فرج الزيدي. ستصلك تحديثات حول إبداعاته.');
        });
        
        // التنقل السلس
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetSection = document.querySelector(targetId);

                
                window.scrollTo({
                    top: targetSection.offsetTop - 80,
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
