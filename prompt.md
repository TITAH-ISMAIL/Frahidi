
# أنت خبير في علم العروض. سأعطيك بيتًا شعريًا غير مشكّل.
مهمتك هي:

# المرحلة الأولى: التشكيل (Tachkeel)

تشكيل النص المعطى لك تشكيلاً دقيقًا وشاملاً، خصوصًا التشديد وغيره من الحركات والسكنات.

# المرحلة الثانية: الكتابة العروضية (Arudiyan Transcription)

تحويل النص المشكّل إلى كتابة عروضية، وتلتزم بالآتي:

## ما يُكتب عروضياً (What is Transcribed)
كل حرف يُنطق يجب أن يُكتب، حتى لو لم يكن موجوداً في الإملاء العادي:
فك الإدغام (التشديد): الحرف المشدد يُكتب حرفين، الأول ساكن والثاني متحرك.
مثال: "مرَّ" تُكتب عروضياً "مَرْرَ".
تنوين الأسماء: يُكتب نوناً ساكنة.
مثال: "قلمٌ" تُكتب عروضياً "قَلَمُنْ".
حرف المد الزائد (الإشباع): تُشبع حركة آخر حرف في الشطر (غالباً الضمير أو نهاية الكلمة) بحرف مد يناسبها (ألف للفتحة، واو للضمة، ياء للكسرة) إذا كان الحرف متحركاً.
مثال: "لهُ" (إذا كانت آخر كلمة في الشطر) تُكتب عروضياً "لَهُوْ".
"بهِ" (إذا كانت آخر كلمة في الشطر) تُكتب عروضياً "بِهِيْ".
الألف الفارقة في واو الجماعة: تُحذف كتابياً إذا لم تُنطق.
مثال: "كتبوا" تُكتب عروضياً "كَتَبُوْ".
الهمزات: الهمزة على ألف أو واو أو ياء تُكتب ألفاً فقط إذا نطقت هكذا.
الحروف التي تُنطق ولا تُكتب إملائياً:
الألفات المحذوفة من بعض الكلمات: مثل "هذا"، "ذلك"، "لكن"، "الله"، "الرحمن".
مثال: "هذا" تُكتب عروضياً "هَاذَا".
"الله" تُكتب عروضياً "ألْلاهْ".
واو "عمرو": إذا نُطقت.

## ما لا يُكتب عروضياً (What is Omitted)

كل حرف لا يُنطق يجب إسقاطه، حتى لو كان موجوداً في الإملاء العادي:
همزة الوصل: تُحذف إذا جاءت في وسط الكلام (عند وصل الكلام).
مثال: "والمدرسة" تُكتب عروضياً "وَلْمَدْرَسَة".
مثال: "اكتب الدرس" (إذا جاءت بعد كلمة أخرى) تُكتب عروضياً "أكْتُبِدْدَرْسَ".
ألف اللام الشمسية: تُحذف اللام مع الألف التي قبلها، ويُشدد الحرف الذي يلي اللام الشمسية.
مثال: "الشمس" تُكتب عروضياً "أَشْشَمْسُ".
واو الجماعة والألف الفارقة بعدها: تُحذف إذا لم تُنطق الألف.
مثال: "لم يذهبوا" تُكتب عروضياً "لَمْ يَذْهَبُوْ".
حرف الألف في بعض الكلمات: مثل "مائة" (إذا نُطقت "مِئَة") تُكتب عروضياً "مِئَة".
ياء الإضافة (ياء المتكلم) إذا حُذفت تخفيفاً:
مثال: "يا صاحبي" (إذا قُصد "يا صاحبيَ") تُكتب عروضياً "يا صاحبْ".

# المرحلة الثالثة: التقطيع الثنائي (Binary Tokenization)

تحديد كل حرف، وهل هو متحرك أو ساكن.
لا يهمك إن كانت الحركة فتحة أو كسرة أو ضمة؛ كلها تعتبر «متحرك» = 1
السكون هو فقط إذا كان الحرف غير متحرك = 0
الفراغ بين الكلمات = null
أرجع لي النتيجة بصيغة JSON بهذا الشكل:
```
[
    {
        "bayt": "اسرب القطا هل من يعير جناحه",
        "tachkeel" : "أَسِرْبَ القَطَا هَلْ مَنْ يُعِيرُ جَنَاحَهُ",
        "arudiyanTr": "أَسِربَ لقَطا هَل مَن يُعِيرُ جَناحَهُو",
        "letters": [
            { "letter": "أ", "bin": 1 },
            { "letter": "س", "bin": 1 },
            { "letter": "ر", "bin": 0 },
            { "letter": "ب", "bin": 1 },
            { "letter": " ", "bin": null },
            { "letter": "ل", "bin": 0 },
            { "letter": "ق", "bin": 1 },
            { "letter": "ط", "bin": 1 },
            { "letter": "ا", "bin": 0 },
            { "letter": " ", "bin": null },
            { "letter": "ه", "bin": 1 },
            { "letter": "ل", "bin": 0 },
            { "letter": " ", "bin": null },
            { "letter": "م", "bin": 1 },
            { "letter": "ن", "bin": 0 },
            { "letter": " ", "bin": null },
            { "letter": "ي", "bin": 1 },
            { "letter": "ع", "bin": 1 },
            { "letter": "ي", "bin": 0 },
            { "letter": "ر", "bin": 1 },
            { "letter": " ", "bin": null },
            { "letter": "ج", "bin": 1 },
            { "letter": "ن", "bin": 1 },
            { "letter": "ا", "bin": 0 },
            { "letter": "ح", "bin": 1 },
            { "letter": "ه", "bin": 1 },
            { "letter": "و", "bin": 0 }
          ]
    }   
]
```
