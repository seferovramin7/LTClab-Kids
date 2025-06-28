# EmailJS Setup Guide for LTC Kids Questionnaire

## 1. EmailJS Account Setup

1. Go to [EmailJS.com](https://www.emailjs.com/)
2. Create a free account
3. Go to "Email Services" and connect your email service (Gmail, Outlook, etc.)
4. Note your Service ID: `service_qycyzbh` (already configured)

## 2. Get Your Public Key

1. Go to "Account" → "General"
2. Copy your Public Key
3. Replace `"YOUR_PUBLIC_KEY"` in `index.html` with your actual public key

## 3. Create Email Templates

### Template 1: For Users (`template_user`)

**Template ID:** `template_user`

**Subject:** `LTC Lab - Layihə Məsləhətçisi Nəticələriniz`

**Template Content:**
```
Salam {{user_name}} {{user_surname}},

LTC Lab Layihə Məsləhətçisini tamamladığınız üçün təşəkkür edirik!

Sizin üçün ən uyğun layihə sahələri:

1. {{result1_name}} {{result1_icon}}
2. {{result2_name}} {{result2_icon}}  
3. {{result3_name}} {{result3_icon}}

Cavablarınız:

{{student_choices}}

{{parent_choices}}

Tarix: {{timestamp}}

Hörmətlə,
LTC Lab Komandası
```

### Template 2: For LTC Lab (`template_ltc`)

**Template ID:** `template_ltc`

**Subject:** `Yeni Sorğu Nəticəsi - {{user_name}} {{user_surname}}`

**Template Content:**
```
Yeni sorğu tamamlandı:

İstifadəçi: {{user_name}} {{user_surname}}
Email: {{user_email}}

Nəticələr:
1. {{result1_name}}
2. {{result2_name}}
3. {{result3_name}}

Şagird Cavabları:
{{student_choices}}

Valideyn Cavabları:
{{parent_choices}}

Tarix: {{timestamp}}
```

## 4. Template Variables

The following variables are available in your templates:

- `{{to_name}}` - Recipient name
- `{{user_name}}` - User's first name
- `{{user_surname}}` - User's last name  
- `{{user_email}}` - User's email
- `{{result1_name}}` - Top project category
- `{{result2_name}}` - Second project category
- `{{result3_name}}` - Third project category
- `{{result1_icon}}` - Icon for top category
- `{{result2_icon}}` - Icon for second category
- `{{result3_icon}}` - Icon for third category
- `{{student_choices}}` - All student answers formatted
- `{{parent_choices}}` - All parent answers formatted
- `{{timestamp}}` - Date and time of completion

## 5. Testing

1. Fill out the form on your website
2. Complete the questionnaire
3. Check both email addresses receive the results
4. Verify all template variables are populated correctly

## 6. GitHub Pages Deployment

This setup works perfectly with GitHub Pages since:
- EmailJS handles all email sending client-side
- No server-side code required
- All sensitive data (API keys) are handled by EmailJS
- Free tier supports 200 emails/month

## Troubleshooting

- Make sure your Public Key is correct
- Verify template IDs match exactly
- Check browser console for any errors
- Test with a simple template first
- Ensure email service is properly connected in EmailJS dashboard 