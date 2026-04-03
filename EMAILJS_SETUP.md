# 📧 EmailJS Setup Guide for Contact Form

Your contact form is now integrated with EmailJS to send emails directly to your inbox. Follow these steps to set it up:

## 🚀 Quick Setup (5 minutes)

### Step 1: Create EmailJS Account
1. Go to [https://www.emailjs.com](https://www.emailjs.com)
2. Click "Sign Up" and create a free account
3. Verify your email address

### Step 2: Create Email Service
1. In EmailJS dashboard, click "Email Services"
2. Click "Add New Service"
3. Choose your email provider:
   - **Gmail** (recommended for personal use)
   - **Outlook/Hotmail**
   - **Yahoo Mail**
   - Or any other provider
4. Follow the connection steps for your provider
5. **Copy your Service ID** (e.g., "service_abc123")

### Step 3: Create Email Template
1. Go to "Email Templates" in dashboard
2. Click "Create New Template"
3. Use this template content:

**Subject:** New Inquiry from {{from_name}} - Twinkle & Tickle

**Content:**
```
Dear {{to_name}},

You have received a new inquiry from your website!

📋 INQUIRY DETAILS:
------------------------
👤 Name: {{from_name}}
📧 Email: {{from_email}}
📱 Phone: {{phone}}
👶 Child's Age: {{child_age}}

💬 Message:
{{message}}

------------------------
Reply to this inquiry by responding to {{from_email}}

Best regards,
Your Website Contact Form
```

4. **Copy your Template ID** (e.g., "template_xyz789")

### Step 4: Get Your User ID
1. Go to "Account" → "General"
2. **Copy your User ID/Public Key** (e.g., "user_abc123def456")

### Step 5: Update Your Website
1. Open `js/script.js` file
2. Replace the placeholders:

```javascript
// Line 163: Replace YOUR_EMAILJS_USER_ID
emailjs.init("YOUR_ACTUAL_USER_ID_HERE");

// Line 189: Replace YOUR_SERVICE_ID and YOUR_TEMPLATE_ID
emailjs.send('YOUR_ACTUAL_SERVICE_ID', 'YOUR_ACTUAL_TEMPLATE_ID', templateParams)
```

**Example:**
```javascript
emailjs.init("user_abc123def456");
emailjs.send('service_gmail123', 'template_contact456', templateParams)
```

### Step 6: Test Your Form
1. Refresh your website
2. Fill out the contact form
3. Click "Send Message"
4. Check your email inbox!

## 📱 Alternative: Simple Mailto Fallback

If you prefer a simpler solution without EmailJS setup, I can modify the form to use a direct mailto link that opens the user's email client. Just let me know!

## 🔧 Troubleshooting

**Form not sending?**
- Check browser console (F12) for errors
- Verify your EmailJS credentials are correct
- Ensure your email service is properly connected

**Not receiving emails?**
- Check spam folder
- Verify the email address in your EmailJS template
- Test with a different email address

**EmailJS quota exceeded?**
- Free plan: 200 emails/month
- Upgrade to paid plan if needed

## 📋 What Happens Now

✅ **Immediate Benefits:**
- Professional email notifications
- All form data organized and formatted
- Automatic replies possible
- No server/backend needed
- Works on all static hosting platforms

✅ **Email Format You'll Receive:**
```
Subject: New Inquiry from John Doe - Twinkle & Tickle

Dear Twinkle and Tickle Team,

You have received a new inquiry from your website!

📋 INQUIRY DETAILS:
------------------------
👤 Name: John Doe
📧 Email: john.doe@example.com
📱 Phone: +91 9876-5432
👶 Child's Age: 6 years

💬 Message:
Hi! I'm interested in the 12-class package for my 6-year-old daughter. 
Could you please provide more details about the curriculum and schedule?

------------------------
Reply to this inquiry by responding to john.doe@example.com
```

## 🎯 Pro Tips

1. **Set up auto-reply:** Create a second template for automatic confirmation emails to customers
2. **Create multiple templates:** Different templates for different types of inquiries
3. **Add filters:** Use EmailJS filters to organize emails by inquiry type
4. **Track conversions:** See which marketing channels bring most inquiries

---

**Need Help?** If you face any issues with setup, just let me know and I'll help you configure it step by step!
