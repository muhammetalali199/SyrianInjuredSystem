# SyrianInjuredSystem

نظام محلي لإدارة استقبال وتقييم المصابين باستخدام Django.

## التشغيل المحلي

1. تثبيت المتطلبات:

```bash
pip install -r requirements.txt
```

2. إنشاء قاعدة البيانات المحلية:

```bash
python manage.py migrate
```

3. إنشاء مستخدم مدير عند الحاجة:

```bash
python manage.py createsuperuser
```

4. تشغيل الموقع محليا فقط:

```bash
python manage.py runserver 127.0.0.1:8000
```

## ملاحظات الأمان

- الإعدادات مخصصة للتشغيل الداخلي فقط على `127.0.0.1` أو `localhost`.
- لا توجد ملفات نشر خارجي مثل Railway أو Gunicorn أو WhiteNoise.
- قاعدة البيانات الافتراضية SQLite محلية داخل ملف `db.sqlite3`.
- لا ترفع ملف `db.sqlite3` أو مجلد `media/` أو ملف `.env` إلى GitHub.
