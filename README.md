# ESP32 IoT Bridge

**גשר IoT לחיבור ALTERA FPGA לענן Firebase**

---

## סקירה כללית

פרויקט זה מספק פתרון שלם לחיבור מערכת FPGA מבוססת ALTERA לענן Firebase באמצעות מיקרובקר ESP32. המערכת מאפשרת העברת נתונים דו-כיוונית בזמן אמת בין חיישנים/מפעילים המחוברים ל-FPGA לבין אפליקציית אינטרנט או מובייל.

```
ALTERA FPGA  <--Serial-->  ESP32  <--HTTPS-->  Firebase  <--API-->  App
```

---

## תכונות עיקריות

| תכונה | תיאור |
|--------|--------|
| **ניהול WiFi חכם** | תמיכה בעד 3 רשתות WiFi עם מעבר אוטומטי |
| **מצב Access Point** | יצירת נקודת גישה כשאין רשת זמינה |
| **ממשק עברי** | ממשק Web מלא בעברית עם תמיכה ב-RTL |
| **עיבוד Dual-Core** | Core 0 ל-Serial, Core 1 ל-Firebase |
| **תקשורת דו-כיוונית** | ALTERA→Firebase ו-Firebase→ALTERA |
| **שמירת הגדרות** | כל ההגדרות נשמרות ב-Flash |

---

## התחלה מהירה

### דרישות
- ESP32 Dev Module
- Arduino IDE 2.0+
- חשבון Firebase

### התקנה

1. **הוסף ESP32 ל-Arduino IDE:**
   - File → Preferences
   - הוסף ל-Additional Board URLs:
   ```
   https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
   ```

2. **התקן את הבורד:**
   - Tools → Board → Boards Manager
   - חפש "ESP32" והתקן

3. **העלה את הקוד:**
   - פתח את `ESP32_IoT_Bridge.ino`
   - בחר בורד: ESP32 Dev Module
   - לחץ Upload

4. **הגדרות ראשוניות:**
   - התחבר לרשת WiFi: `ESP32_Config`
   - גש לכתובת: `192.168.4.1`
   - הזן פרטי WiFi ו-Firebase

---

## חיבורי חומרה

| פין ESP32 | חיבור | תיאור |
|-----------|--------|--------|
| GPIO 16 (RX2) | TX של ALTERA | קבלת נתונים |
| GPIO 17 (TX2) | RX של ALTERA | שליחת נתונים |
| GND | GND | אדמה משותפת |

> **שים לב:** השתמש ב-Level Shifter אם ה-FPGA עובד ב-5V

---

## פורמט נתונים

### ALTERA → Firebase
```json
{
  "fromAltera": {
    "A": 25,
    "B": 100,
    "C": 42
  }
}
```

### Firebase → ALTERA
```json
{
  "toAltera": 1
}
```

---

## הגדרת Firebase

1. צור פרויקט ב-[Firebase Console](https://console.firebase.google.com)
2. צור Realtime Database
3. הגדר Rules (לפיתוח):
```json
{
  "rules": {
    ".read": true,
    ".write": true
  }
}
```
4. העתק את ה-Database URL והזן בממשק ההגדרות

---

## ארכיטקטורה

```
ESP32 Dual-Core Architecture
============================

Core 0 (Protocol CPU):
├── Task: serialTask
└── אחריות: קריאה מ-ALTERA

Core 1 (Application CPU):
├── Task: firebaseTask
└── אחריות: תקשורת עם Firebase
```

---

## פתרון בעיות

| בעיה | פתרון |
|------|--------|
| לא מתחבר ל-WiFi | בדוק שם רשת וסיסמה, וודא רשת 2.4GHz |
| לא מתחבר ל-Firebase | בדוק URL ו-Rules |
| נתונים לא מגיעים | בדוק חיבורי Serial ו-Baud Rate (115200) |
| לא מצליח להעלות קוד | לחץ על כפתור BOOT בזמן ההעלאה |

---

## קבצים

| קובץ | תיאור |
|------|--------|
| `ESP32_IoT_Bridge.ino` | קוד ה-ESP32 המלא |
| `docs/index.html` | דף מידע מעוצב |

---

## רישיון

פרויקט לימודי למכללה - חופשי לשימוש

---

**נוצר עם אהבה לסטודנטים**
