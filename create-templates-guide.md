# How to Create EmailJS Templates - Step by Step

## Step 1: Login to EmailJS Dashboard

1. Go to [https://www.emailjs.com/](https://www.emailjs.com/)
2. Login with your account
3. You should see your dashboard

## Step 2: Navigate to Email Templates

1. In the left sidebar, click on **"Email Templates"**
2. Click the **"Create New Template"** button

## Step 3: Create Template for Users

### Template 1: `template_user`

1. **Template Name**: `User Results Template`
2. **Template ID**: `template_user` (IMPORTANT: Must be exactly this)
3. **Subject**: `LTC Lab - Layihə Məsləhətçisi Nəticələriniz`

4. **Email Content** (copy this exactly):

```
Salam {{user_name}} {{user_surname}},

LTC Lab Layihə Məsləhətçisini tamamladığınız üçün təşəkkür edirik!

Sizin üçün ən uyğun layihə sahələri:

🥇 1. {{result1_name}} {{result1_icon}}
🥈 2. {{result2_name}} {{result2_icon}}
🥉 3. {{result3_name}} {{result3_icon}}

📝 Sizin cavablarınız:

{{student_choices}}

{{parent_choices}}

📅 Tarix: {{timestamp}}

Bu nəticələr əsasında LTC Lab komandası sizinlə əlaqə saxlayacaq.

Hörmətlə,
LTC Lab Komandası

---
Bu email avtomatik olaraq göndərilmişdir.
LTC Lab | Gələcəyi Quranlar
```

5. Click **"Save"**

## Step 4: Create Template for LTC Lab

1. Click **"Create New Template"** again

### Template 2: `template_ltc`

1. **Template Name**: `LTC Lab Internal Results`
2. **Template ID**: `template_ltc` (IMPORTANT: Must be exactly this)
3. **Subject**: `🆕 Yeni Sorğu Nəticəsi - {{user_name}} {{user_surname}}`

4. **Email Content** (copy this exactly):

```
🎯 YENİ SORĞU NƏTİCƏSİ

👤 İstifadəçi Məlumatları:
Ad Soyad: {{user_name}} {{user_surname}}
Email: {{user_email}}

🏆 Tövsiyə olunan layihə sahələri:
1️⃣ {{result1_name}} {{result1_icon}}
2️⃣ {{result2_name}} {{result2_icon}}
3️⃣ {{result3_name}} {{result3_icon}}

📋 ŞAGİRD CAVABLARI:
{{student_choices}}

👨‍👩‍👧‍👦 VALİDEYN CAVABLARI:
{{parent_choices}}

📅 Tarix: {{timestamp}}

---
Bu nəticə LTC Kids layihə məsləhətçisi tərəfindən avtomatik olaraq yaradılmışdır.
```

5. Click **"Save"**

## Step 5: Test Your Templates

1. Go back to your website
2. Fill out the form with test data
3. Complete the questionnaire
4. Check if emails are sent correctly

## Step 6: Verify Email Service Connection

1. In EmailJS dashboard, go to **"Email Services"**
2. Make sure you have a service connected (Gmail, Outlook, etc.)
3. The service should show as "Connected"

## Important Notes:

⚠️ **Template IDs must be EXACTLY:**
- `template_user` 
- `template_ltc`

⚠️ **Don't change the variable names** like `{{user_name}}`, `{{result1_name}}`, etc.

⚠️ **Make sure your email service is connected** in the "Email Services" section

## If You Get Errors:

1. **"Template not found"** → Check template IDs are exactly `template_user` and `template_ltc`
2. **"Service not found"** → Make sure `service_qycyzbh` exists in your account
3. **"Variables not showing"** → Template variables are case-sensitive
4. **"Emails not sending"** → Check your email service connection

## Testing Checklist:

- [ ] Template `template_user` created with correct ID
- [ ] Template `template_ltc` created with correct ID  
- [ ] Email service connected
- [ ] Public key updated in code
- [ ] Test email sent successfully
- [ ] Both user and LTC emails received
- [ ] All variables populated correctly

Once you complete these steps, your questionnaire will automatically send beautiful, formatted emails to both users and the LTC Lab team! 