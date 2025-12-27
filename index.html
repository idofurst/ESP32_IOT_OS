<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ESP32 IoT Bridge - גשר IoT לחיבור FPGA לענן</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Arial, sans-serif;
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #0f3460 100%);
            min-height: 100vh;
            color: #e4e4e4;
            line-height: 1.8;
        }
        
        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            text-align: center;
            padding: 60px 20px;
            background: rgba(0, 0, 0, 0.3);
            border-radius: 20px;
            margin-bottom: 40px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .logo {
            font-size: 4rem;
            margin-bottom: 20px;
        }
        
        h1 {
            font-size: 2.5rem;
            color: #00d9ff;
            margin-bottom: 15px;
            text-shadow: 0 0 30px rgba(0, 217, 255, 0.5);
        }
        
        .subtitle {
            font-size: 1.3rem;
            color: #94a3b8;
            margin-bottom: 30px;
        }
        
        .badges {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }
        
        .badge {
            background: rgba(0, 217, 255, 0.2);
            color: #00d9ff;
            padding: 8px 20px;
            border-radius: 25px;
            font-size: 0.9rem;
            border: 1px solid rgba(0, 217, 255, 0.3);
        }
        
        .section {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 35px;
            margin-bottom: 30px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
        }
        
        h2 {
            color: #00d9ff;
            font-size: 1.6rem;
            margin-bottom: 25px;
            display: flex;
            align-items: center;
            gap: 12px;
        }
        
        h2 span {
            font-size: 1.8rem;
        }
        
        .architecture {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }
        
        .arch-box {
            background: linear-gradient(145deg, rgba(0, 217, 255, 0.1), rgba(0, 217, 255, 0.05));
            border: 2px solid rgba(0, 217, 255, 0.3);
            border-radius: 15px;
            padding: 25px;
            text-align: center;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .arch-box:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 40px rgba(0, 217, 255, 0.2);
        }
        
        .arch-box .icon {
            font-size: 3rem;
            margin-bottom: 15px;
        }
        
        .arch-box h3 {
            color: #00d9ff;
            margin-bottom: 10px;
        }
        
        .arch-box p {
            color: #94a3b8;
            font-size: 0.9rem;
        }
        
        .arrow {
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            color: #00d9ff;
        }
        
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
        }
        
        .feature {
            background: rgba(0, 0, 0, 0.2);
            padding: 25px;
            border-radius: 12px;
            border-right: 4px solid #00d9ff;
        }
        
        .feature h3 {
            color: #fff;
            margin-bottom: 12px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .feature p {
            color: #94a3b8;
        }
        
        .code-block {
            background: #0d1117;
            border-radius: 10px;
            padding: 20px;
            margin: 20px 0;
            overflow-x: auto;
            direction: ltr;
            text-align: left;
            border: 1px solid #30363d;
        }
        
        .code-block code {
            font-family: 'Consolas', 'Monaco', monospace;
            color: #c9d1d9;
            font-size: 0.9rem;
            line-height: 1.6;
        }
        
        .code-block .comment {
            color: #8b949e;
        }
        
        .code-block .keyword {
            color: #ff7b72;
        }
        
        .code-block .string {
            color: #a5d6ff;
        }
        
        .code-block .function {
            color: #d2a8ff;
        }
        
        .step-list {
            counter-reset: step;
        }
        
        .step {
            display: flex;
            gap: 20px;
            margin-bottom: 25px;
            align-items: flex-start;
        }
        
        .step-number {
            background: linear-gradient(135deg, #00d9ff, #0099cc);
            color: #000;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            flex-shrink: 0;
        }
        
        .step-content h3 {
            color: #fff;
            margin-bottom: 8px;
        }
        
        .step-content p {
            color: #94a3b8;
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }
        
        th, td {
            padding: 15px;
            text-align: right;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        th {
            background: rgba(0, 217, 255, 0.1);
            color: #00d9ff;
        }
        
        tr:hover {
            background: rgba(255, 255, 255, 0.05);
        }
        
        .warning {
            background: rgba(255, 193, 7, 0.1);
            border: 1px solid rgba(255, 193, 7, 0.3);
            border-radius: 10px;
            padding: 20px;
            margin: 20px 0;
            display: flex;
            gap: 15px;
            align-items: flex-start;
        }
        
        .warning-icon {
            font-size: 1.5rem;
        }
        
        .info-box {
            background: rgba(0, 217, 255, 0.1);
            border: 1px solid rgba(0, 217, 255, 0.3);
            border-radius: 10px;
            padding: 20px;
            margin: 20px 0;
        }
        
        .data-flow {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin: 25px 0;
        }
        
        .flow-item {
            background: rgba(0, 0, 0, 0.3);
            padding: 20px;
            border-radius: 10px;
            display: flex;
            align-items: center;
            gap: 20px;
        }
        
        .flow-direction {
            font-size: 2rem;
            min-width: 60px;
            text-align: center;
        }
        
        .flow-desc h4 {
            color: #00d9ff;
            margin-bottom: 5px;
        }
        
        footer {
            text-align: center;
            padding: 40px;
            color: #64748b;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            margin-top: 40px;
        }
        
        footer a {
            color: #00d9ff;
            text-decoration: none;
        }
        
        footer a:hover {
            text-decoration: underline;
        }
        
        .btn {
            display: inline-block;
            background: linear-gradient(135deg, #00d9ff, #0099cc);
            color: #000;
            padding: 15px 35px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            margin: 10px;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(0, 217, 255, 0.4);
        }
        
        .btn-secondary {
            background: transparent;
            border: 2px solid #00d9ff;
            color: #00d9ff;
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 1.8rem;
            }
            
            .subtitle {
                font-size: 1rem;
            }
            
            .section {
                padding: 20px;
            }
            
            .architecture {
                grid-template-columns: 1fr;
            }
            
            .arrow {
                transform: rotate(90deg);
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="logo">🔌</div>
            <h1>ESP32 IoT Bridge</h1>
            <p class="subtitle">גשר IoT לחיבור ALTERA FPGA לענן Firebase</p>
            <div class="badges">
                <span class="badge">ESP32</span>
                <span class="badge">ALTERA FPGA</span>
                <span class="badge">Firebase</span>
                <span class="badge">Arduino IDE</span>
                <span class="badge">Dual-Core</span>
            </div>
            <div style="margin-top: 30px;">
                <a href="https://github.com/YOUR_USERNAME/ESP32-IoT-Bridge" class="btn">📥 הורד מ-GitHub</a>
                <a href="#quickstart" class="btn btn-secondary">🚀 התחלה מהירה</a>
            </div>
        </header>

        <section class="section">
            <h2><span>📋</span> סקירה כללית</h2>
            <p>
                פרויקט זה מספק פתרון שלם לחיבור מערכת FPGA מבוססת ALTERA לענן Firebase 
                באמצעות מיקרובקר ESP32. המערכת מאפשרת העברת נתונים דו-כיוונית בזמן אמת 
                בין חיישנים/מפעילים המחוברים ל-FPGA לבין אפליקציית אינטרנט או מובייל.
            </p>
            
            <div class="architecture">
                <div class="arch-box">
                    <div class="icon">🔧</div>
                    <h3>ALTERA FPGA</h3>
                    <p>חיישנים ומפעילים<br>תקשורת Serial</p>
                </div>
                <div class="arrow">⟷</div>
                <div class="arch-box">
                    <div class="icon">📡</div>
                    <h3>ESP32</h3>
                    <p>גשר IoT<br>עיבוד Dual-Core</p>
                </div>
                <div class="arrow">⟷</div>
                <div class="arch-box">
                    <div class="icon">☁️</div>
                    <h3>Firebase</h3>
                    <p>Realtime Database<br>אחסון בענן</p>
                </div>
                <div class="arrow">⟷</div>
                <div class="arch-box">
                    <div class="icon">📱</div>
                    <h3>אפליקציה</h3>
                    <p>Web / Mobile<br>ממשק משתמש</p>
                </div>
            </div>
        </section>

        <section class="section">
            <h2><span>✨</span> תכונות עיקריות</h2>
            <div class="features">
                <div class="feature">
                    <h3>📶 ניהול WiFi חכם</h3>
                    <p>תמיכה בעד 3 רשתות WiFi עם מעבר אוטומטי. תמיכה ברשתות פתוחות ומוצפנות.</p>
                </div>
                <div class="feature">
                    <h3>📡 מצב Access Point</h3>
                    <p>כשאין רשת זמינה, המערכת יוצרת נקודת גישה לצורך הגדרות.</p>
                </div>
                <div class="feature">
                    <h3>🌐 ממשק הגדרות בעברית</h3>
                    <p>ממשק Web מלא בעברית עם תמיכה ב-RTL לנוחות מירבית.</p>
                </div>
                <div class="feature">
                    <h3>⚡ עיבוד Dual-Core</h3>
                    <p>Core 0 מטפל בתקשורת Serial, Core 1 מטפל ב-Firebase - ללא חסימות.</p>
                </div>
                <div class="feature">
                    <h3>🔄 תקשורת דו-כיוונית</h3>
                    <p>העברת נתונים מ-ALTERA לענן ומהענן ל-ALTERA בזמן אמת.</p>
                </div>
                <div class="feature">
                    <h3>💾 שמירת הגדרות</h3>
                    <p>כל ההגדרות נשמרות ב-Flash ונטענות אוטומטית בהפעלה.</p>
                </div>
            </div>
        </section>

        <section class="section" id="quickstart">
            <h2><span>🚀</span> התחלה מהירה</h2>
            
            <div class="step-list">
                <div class="step">
                    <div class="step-number">1</div>
                    <div class="step-content">
                        <h3>התקנת Arduino IDE</h3>
                        <p>הורד והתקן את <a href="https://www.arduino.cc/en/software" style="color: #00d9ff;">Arduino IDE</a> גרסה 2.0 ומעלה.</p>
                    </div>
                </div>
                
                <div class="step">
                    <div class="step-number">2</div>
                    <div class="step-content">
                        <h3>הוספת ESP32 Boards</h3>
                        <p>ב-File → Preferences הוסף את הקישור:<br>
                        <code style="background: #0d1117; padding: 5px 10px; border-radius: 5px; direction: ltr; display: inline-block;">
                            https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
                        </code></p>
                    </div>
                </div>
                
                <div class="step">
                    <div class="step-number">3</div>
                    <div class="step-content">
                        <h3>התקנת הבורד</h3>
                        <p>ב-Tools → Board → Boards Manager חפש "ESP32" והתקן את "esp32 by Espressif Systems".</p>
                    </div>
                </div>
                
                <div class="step">
                    <div class="step-number">4</div>
                    <div class="step-content">
                        <h3>בחירת הבורד</h3>
                        <p>ב-Tools → Board בחר "ESP32 Dev Module" או את הבורד הספציפי שלך.</p>
                    </div>
                </div>
                
                <div class="step">
                    <div class="step-number">5</div>
                    <div class="step-content">
                        <h3>העלאת הקוד</h3>
                        <p>פתח את הקובץ ESP32_IoT_Bridge.ino ולחץ על Upload.</p>
                    </div>
                </div>
                
                <div class="step">
                    <div class="step-number">6</div>
                    <div class="step-content">
                        <h3>הגדרות ראשוניות</h3>
                        <p>התחבר לרשת WiFi "ESP32_Config" וגש לכתובת 192.168.4.1 להגדרות.</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="section">
            <h2><span>🔌</span> חיבורי חומרה</h2>
            
            <table>
                <thead>
                    <tr>
                        <th>פין ESP32</th>
                        <th>חיבור</th>
                        <th>תיאור</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>GPIO 16 (RX2)</td>
                        <td>TX של ALTERA</td>
                        <td>קבלת נתונים מה-FPGA</td>
                    </tr>
                    <tr>
                        <td>GPIO 17 (TX2)</td>
                        <td>RX של ALTERA</td>
                        <td>שליחת נתונים ל-FPGA</td>
                    </tr>
                    <tr>
                        <td>GND</td>
                        <td>GND של ALTERA</td>
                        <td>אדמה משותפת</td>
                    </tr>
                    <tr>
                        <td>3.3V / 5V</td>
                        <td>VCC</td>
                        <td>אספקת מתח (בדוק תאימות)</td>
                    </tr>
                </tbody>
            </table>
            
            <div class="warning">
                <span class="warning-icon">⚠️</span>
                <div>
                    <strong>שים לב!</strong> ה-FPGA עשוי לעבוד במתח 5V. וודא שאתה משתמש ב-Level Shifter 
                    אם יש צורך להמיר בין 3.3V ל-5V כדי לא לפגוע ב-ESP32.
                </div>
            </div>
        </section>

        <section class="section">
            <h2><span>📊</span> פורמט נתונים</h2>
            
            <div class="data-flow">
                <div class="flow-item">
                    <div class="flow-direction">📤</div>
                    <div class="flow-desc">
                        <h4>ALTERA → Firebase</h4>
                        <p>הנתונים נשלחים כ-JSON בפורמט: <code>{"A": value1, "B": value2, "C": value3}</code></p>
                        <p>נשמרים ב-Firebase תחת הנתיב: <code>/fromAltera</code></p>
                    </div>
                </div>
                
                <div class="flow-item">
                    <div class="flow-direction">📥</div>
                    <div class="flow-desc">
                        <h4>Firebase → ALTERA</h4>
                        <p>ערך מספרי נקרא מהנתיב: <code>/toAltera</code></p>
                        <p>נשלח ל-ALTERA דרך Serial כמספר שלם</p>
                    </div>
                </div>
            </div>

            <div class="code-block">
<code><span class="comment">// דוגמה למבנה ב-Firebase Realtime Database</span>
{
  <span class="string">"fromAltera"</span>: {
    <span class="string">"A"</span>: <span class="keyword">25</span>,
    <span class="string">"B"</span>: <span class="keyword">100</span>,
    <span class="string">"C"</span>: <span class="keyword">42</span>
  },
  <span class="string">"toAltera"</span>: <span class="keyword">1</span>,
  <span class="string">"deviceIP"</span>: <span class="string">"192.168.1.105"</span>
}</code>
            </div>
        </section>

        <section class="section">
            <h2><span>🔥</span> הגדרת Firebase</h2>
            
            <div class="step-list">
                <div class="step">
                    <div class="step-number">1</div>
                    <div class="step-content">
                        <h3>יצירת פרויקט</h3>
                        <p>גש ל-<a href="https://console.firebase.google.com" style="color: #00d9ff;">Firebase Console</a> וצור פרויקט חדש.</p>
                    </div>
                </div>
                
                <div class="step">
                    <div class="step-number">2</div>
                    <div class="step-content">
                        <h3>יצירת Realtime Database</h3>
                        <p>ב-Build → Realtime Database לחץ "Create Database" ובחר מיקום.</p>
                    </div>
                </div>
                
                <div class="step">
                    <div class="step-number">3</div>
                    <div class="step-content">
                        <h3>הגדרת Rules</h3>
                        <p>לצורכי פיתוח, הגדר את ה-Rules הבאים:</p>
                        <div class="code-block">
<code>{
  <span class="string">"rules"</span>: {
    <span class="string">".read"</span>: <span class="keyword">true</span>,
    <span class="string">".write"</span>: <span class="keyword">true</span>
  }
}</code>
                        </div>
                    </div>
                </div>
                
                <div class="step">
                    <div class="step-number">4</div>
                    <div class="step-content">
                        <h3>העתקת ה-URL</h3>
                        <p>העתק את ה-Database URL (בפורמט: https://your-project.firebaseio.com) והכנס אותו בממשק ההגדרות.</p>
                    </div>
                </div>
            </div>
            
            <div class="info-box">
                <strong>💡 טיפ:</strong> לסביבת ייצור, מומלץ להשתמש ב-Database Secret במקום rules פתוחים.
                ניתן למצוא אותו ב-Project Settings → Service Accounts → Database Secrets.
            </div>
        </section>

        <section class="section">
            <h2><span>🏗️</span> ארכיטקטורת המערכת</h2>
            
            <div class="code-block">
<code><span class="comment">/*
 * ESP32 Dual-Core Architecture
 * ============================
 *
 * Core 0 (Protocol CPU):
 * ├── Task: serialTask
 * ├── Priority: 1
 * └── Responsibility:
 *     ├── Read data from ALTERA via Serial2
 *     ├── Parse 19-byte buffer
 *     ├── Extract values at positions [5, 11, 17]
 *     └── Store in shared variables
 *
 * Core 1 (Application CPU):
 * ├── Task: firebaseTask
 * ├── Priority: 1
 * └── Responsibility:
 *     ├── Send data to Firebase (HTTPClient)
 *     ├── Receive data via Firebase Streaming
 *     ├── Send received values to ALTERA
 *     └── Handle WiFi & Web Server
 *
 * Data Flow:
 * ALTERA ──Serial──> ESP32 ──HTTPS──> Firebase
 * ALTERA <──Serial── ESP32 <──Stream── Firebase
 */</span></code>
            </div>
        </section>

        <section class="section">
            <h2><span>❓</span> פתרון בעיות</h2>
            
            <table>
                <thead>
                    <tr>
                        <th>בעיה</th>
                        <th>פתרון</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>לא מתחבר ל-WiFi</td>
                        <td>בדוק את שם הרשת והסיסמה. וודא שזו רשת 2.4GHz.</td>
                    </tr>
                    <tr>
                        <td>לא מתחבר ל-Firebase</td>
                        <td>וודא שה-URL נכון ושה-Rules מאפשרים גישה.</td>
                    </tr>
                    <tr>
                        <td>נתונים לא מגיעים מ-ALTERA</td>
                        <td>בדוק את חיבורי ה-Serial ואת קצב ה-Baud (115200).</td>
                    </tr>
                    <tr>
                        <td>המערכת קופאת</td>
                        <td>וודא שה-ESP32 מחובר למתח יציב. בדוק את ה-Serial Monitor.</td>
                    </tr>
                    <tr>
                        <td>לא מצליח להעלות קוד</td>
                        <td>לחץ על כפתור BOOT ב-ESP32 בזמן ההעלאה.</td>
                    </tr>
                </tbody>
            </table>
        </section>

        <section class="section">
            <h2><span>📚</span> משאבים נוספים</h2>
            
            <div class="features">
                <div class="feature">
                    <h3>📖 תיעוד ESP32</h3>
                    <p><a href="https://docs.espressif.com/projects/esp-idf/en/latest/esp32/" style="color: #00d9ff;">ESP-IDF Documentation</a></p>
                </div>
                <div class="feature">
                    <h3>🔥 תיעוד Firebase</h3>
                    <p><a href="https://firebase.google.com/docs/database" style="color: #00d9ff;">Firebase Realtime Database</a></p>
                </div>
                <div class="feature">
                    <h3>🔧 Arduino Reference</h3>
                    <p><a href="https://www.arduino.cc/reference/en/" style="color: #00d9ff;">Arduino Language Reference</a></p>
                </div>
                <div class="feature">
                    <h3>💬 קהילה</h3>
                    <p><a href="https://github.com/YOUR_USERNAME/ESP32-IoT-Bridge/issues" style="color: #00d9ff;">GitHub Issues</a></p>
                </div>
            </div>
        </section>

        <footer>
            <p>🎓 פרויקט לימודי למכללה</p>
            <p>נוצר עם ❤️ לסטודנטים</p>
            <p style="margin-top: 20px;">
                <a href="https://github.com/YOUR_USERNAME/ESP32-IoT-Bridge">GitHub</a> • 
                <a href="#quickstart">התחלה מהירה</a> • 
                <a href="mailto:your@email.com">יצירת קשר</a>
            </p>
        </footer>
    </div>
</body>
</html>
