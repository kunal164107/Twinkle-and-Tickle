# 📧 Contact Form Email Setup Guide

Your contact form is now configured to send enquiries directly to your email!

## 🚀 How It Works

The form uses **FormSubmit.co** - a FREE service that sends form submissions to your email without any backend code needed.

---

## ⚙️ Setup Instructions (5 Minutes)

### Step 1: Update Your Email Address

Open `index.html` and find line **649**:

```html
<form class="contact-form" id="contactForm" action="https://formsubmit.co/YOUR_EMAIL@example.com" method="POST">
```

**Replace** `YOUR_EMAIL@example.com` with your actual email address:

```html
<form class="contact-form" id="contactForm" action="https://formsubmit.co/your-real-email@gmail.com" method="POST">
```

### Step 2: Activate Your Email (One-time)

1. **Save** the index.html file with your email
2. **Deploy** your website or test locally
3. **Fill out** the contact form and submit it
4. **Check your email** - You'll receive an activation link from FormSubmit
5. **Click the activation link** to confirm
6. **Done!** All future form submissions will arrive in your inbox

---

## 📨 What You'll Receive

When someone fills out the contact form, you'll get an email with:

- **Subject**: "New Enquiry from Twinkle & Tickle Website"
- **From**: FormSubmit (noreply@formsubmit.co)
- **Content**:
  - Name
  - Email Address
  - Phone Number
  - Child's Age
  - Message

---

## 🔧 Customization Options

You can customize the form behavior by editing the hidden fields in `index.html` (lines 650-652):

### Change Email Subject
```html
<input type="hidden" name="_subject" value="Your Custom Subject Here">
```

### Redirect After Submission
Update line 652 with your actual website URL:
```html
<input type="hidden" name="_next" value="https://yourwebsite.com/thank-you.html">
```

Or keep it simple:
```html
<input type="hidden" name="_next" value="https://yourwebsite.com/#contact">
```

### Enable reCAPTCHA (Prevent Spam)
```html
<input type="hidden" name="_captcha" value="true">
```

### Custom Thank You Page (Optional)
Create a `thank-you.html` file or redirect back to your site with a success message.

---

## 🎯 Alternative Email Services (Free)

If you prefer other services, here are alternatives:

### 1. **Web3Forms** (https://web3forms.com)
- Free forever
- No activation needed
- Spam filtering

Update form action:
```html
<form action="https://api.web3forms.com/submit" method="POST">
    <input type="hidden" name="access_key" value="YOUR_ACCESS_KEY">
    <!-- rest of form -->
</form>
```

### 2. **Formspree** (https://formspree.io)
- 50 submissions/month free
- Email notifications
- Dashboard to view submissions

Update form action:
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

### 3. **EmailJS** (https://emailjs.com)
- 200 emails/month free
- JavaScript-based
- More control

Requires adding EmailJS library and JavaScript code.

### 4. **Google Forms** (Embed)
- Unlimited submissions
- Responses in Google Sheets
- Requires iframe embed

---

## 🔍 Testing Locally

Before deploying:

1. Make sure your website is running (http://localhost:8000)
2. Fill out the contact form
3. Click "Send Message"
4. You should be redirected to the contact section
5. Check your email for the activation link (first time only)
6. After activation, test again - you should receive the form data

---

## 🌐 After Deployment

Once you deploy to GitHub Pages, Netlify, or Vercel:

1. Update the `_next` field with your live website URL
2. Example for GitHub Pages:
```html
<input type="hidden" name="_next" value="https://YOUR_USERNAME.github.io/twinkle-and-tickle/#contact">
```

3. Example for Netlify:
```html
<input type="hidden" name="_next" value="https://twinkle-and-tickle.netlify.app/#contact">
```

---

## 🛡️ Spam Protection Tips

1. **Enable reCAPTCHA**:
```html
<input type="hidden" name="_captcha" value="true">
```

2. **Add Honeypot Field** (hidden field that bots fill):
```html
<input type="text" name="_honey" style="display:none">
```

3. **Limit to Your Domain**:
```html
<input type="hidden" name="_blacklist" value="spammy, viagra, pills">
```

---

## 📧 Email Not Working? Troubleshooting

### Check 1: Email Address Format
- Make sure there are no spaces
- Use lowercase
- Example: `info@twinkleandtickle.com`

### Check 2: Activation Required
- First submission requires email confirmation
- Check spam folder for activation email

### Check 3: Form Method
- Must be `method="POST"`
- Must have `action="https://formsubmit.co/YOUR_EMAIL"`

### Check 4: Input Names
- All inputs must have `name` attribute
- Example: `<input type="text" name="name">`

### Check 5: Internet Connection
- FormSubmit requires internet to work
- Won't work offline

---

## 💡 Pro Tips

1. **Create a dedicated email** for form submissions:
   - Example: `enquiry@twinkleandtickle.com`
   - or `twinkleandtickle.enquiry@gmail.com`

2. **Set up email filters** in Gmail:
   - Auto-label emails from FormSubmit
   - Create a "Website Enquiries" folder

3. **Auto-responder**: Use FormSubmit's `_autoresponse` feature:
```html
<input type="hidden" name="_autoresponse" value="Thank you for contacting Twinkle and Tickle! We'll get back to you soon.">
```

4. **CC yourself or team**:
```html
<input type="hidden" name="_cc" value="backup@example.com">
```

---

## ✅ Quick Checklist

- [ ] Replace `YOUR_EMAIL@example.com` with real email
- [ ] Save index.html
- [ ] Test form submission
- [ ] Check email and click activation link
- [ ] Test again to confirm it works
- [ ] Update `_next` URL with live website after deployment
- [ ] Add spam protection if needed
- [ ] Set up email filters for organization

---

## 📞 Current Setup Summary

**Your form currently:**
- ✅ Collects: Name, Email, Phone, Child's Age, Message
- ✅ Subject: "New Enquiry from Twinkle & Tickle Website"
- ✅ Redirects back to contact section after submission
- ✅ No captcha (can enable if spam becomes an issue)
- ✅ Works on all devices

**After you add your email:**
- You'll receive all enquiries directly in your inbox
- Each submission comes as a formatted email
- You can reply directly to the customer's email
- Free forever, no limits

---

## 🎉 That's It!

Your contact form is ready to collect enquiries. Just add your email and activate it!

**Need Help?** Check FormSubmit.co documentation: https://formsubmit.co

---

**Made with ❤️ for Twinkle and Tickle**
