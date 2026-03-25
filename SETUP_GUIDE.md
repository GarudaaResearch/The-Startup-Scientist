# Setup Guide for Real-Time Feedback Integration

This guide will help you configure the real-time Google Sheets and email notifications for the Startup Scientist Program feedback system.

## 🎯 What's Already Implemented

✅ **Quiz System**: Interactive 10-question quiz with real-time scoring  
✅ **Feedback Form**: Comprehensive form with ratings and text feedback  
✅ **Data Collection**: Ready for real-time submission to Google Sheets and email  
✅ **Error Handling**: Automatic retry mechanism for failed submissions  
✅ **Responsive Design**: Works on all devices  

## 📋 Setup Steps

### Option 1: SheetDB.io (Recommended - Professional)

1. **Create SheetDB Account**
   - Go to https://sheetdb.io/
   - Sign up for a free account
   - Create a new API endpoint

2. **Set Up Google Sheet**
   - Create a new Google Sheet with these columns:
     ```
     name | email | department | year | feedback | suggestions | content_rating | relevance_rating | satisfaction_rating | quiz_score | quiz_percentage | newsletter | timestamp
     ```

3. **Get API Key**
   - From SheetDB dashboard, copy your API key
   - Replace `YOUR_SHEETDB_API_KEY` in the code

4. **Update the Code**
   ```javascript
   const SHEETDB_API_URL = 'https://sheetdb.io/api/v1/YOUR_ACTUAL_API_KEY';
   ```

### Option 2: Google Forms (Free Alternative)

1. **Create Google Form**
   - Go to Google Forms
   - Create fields matching the data structure
   - Get the form ID from the URL

2. **Get Entry IDs**
   - Inspect the form to find field entry IDs
   - Replace the placeholder IDs in the code

3. **Update the Code**
   ```javascript
   const GOOGLE_FORM_URL = 'https://docs.google.com/forms/d/e/YOUR_FORM_ID/formResponse';
   ```

## 📧 Email Setup

### Option 1: EmailJS (Recommended)

1. **Create EmailJS Account**
   - Go to https://www.emailjs.com/
   - Sign up for a free plan

2. **Set Up Email Service**
   - Add your email service (Gmail, Outlook, etc.)
   - Create an email template

3. **Get Credentials**
   - Service ID, Template ID, and Public Key
   - Update these in the code:

```javascript
const EMAILJS_SERVICE_ID = 'YOUR_SERVICE_ID';
const EMAILJS_TEMPLATE_ID = 'YOUR_TEMPLATE_ID';
const EMAILJS_PUBLIC_KEY = 'YOUR_PUBLIC_KEY';
```

### Option 2: Web3Forms (Alternative)

1. **Create Web3Forms Account**
   - Go to https://web3forms.com/
   - Get your access key
   - Update the code:

```javascript
const access_key = 'YOUR_WEB3FORMS_ACCESS_KEY';
```

## 🔧 Configuration Checklist

- [ ] Replace `YOUR_SHEETDB_API_KEY` with actual API key
- [ ] Replace `YOUR_FORM_ID` with Google Form ID (if using)
- [ ] Replace `YOUR_SERVICE_ID`, `YOUR_TEMPLATE_ID`, `YOUR_PUBLIC_KEY` with EmailJS credentials
- [ ] Replace `YOUR_WEB3FORMS_ACCESS_KEY` with Web3Forms key (if using)
- [ ] Test the feedback form end-to-end
- [ ] Verify data appears in Google Sheets
- [ ] Verify email notifications are received

## 🚀 Testing the System

1. **Open the HTML file** in your browser
2. **Take the quiz** to generate quiz results
3. **Fill out the feedback form** with test data
4. **Submit the form** and check:
   - Success message appears
   - Data appears in Google Sheets within seconds
   - Email notification arrives in your inbox
5. **Test error handling** by disconnecting internet and submitting

## 📊 Data Structure

The system collects:
- User information (name, email, department, year)
- Feedback text and suggestions
- Star ratings (content, relevance, satisfaction)
- Quiz scores and percentages
- Newsletter subscription preference
- Timestamp of submission

## 🔒 Security Notes

- API keys are client-side (acceptable for this use case)
- Consider rate limiting for production
- Validate all inputs on the backend for production use
- Use HTTPS in production

## 🛠️ Advanced Features Already Included

- **Automatic Retry**: Failed submissions are stored and retried
- **Multiple Fallbacks**: If one service fails, others are tried
- **Local Storage Backup**: Data is saved locally if all services fail
- **Real-time Validation**: Form validation before submission
- **Responsive Design**: Works on mobile and desktop
- **Progress Indicators**: Visual feedback during submission

## 📞 Support

For issues with:
- **SheetDB**: Check their documentation at https://sheetdb.io/docs
- **EmailJS**: Check their documentation at https://www.emailjs.com/docs/
- **Google Forms**: Ensure entry IDs are correct
- **Code Issues**: Check browser console for error messages

## 🎉 You're Ready!

Once configured, your feedback system will:
1. Collect quiz results and feedback in real-time
2. Store data in Google Sheets automatically
3. Send instant email notifications
4. Handle errors gracefully with automatic retries
5. Work seamlessly across all devices

The system is production-ready and will provide valuable insights into participant engagement and program effectiveness!
