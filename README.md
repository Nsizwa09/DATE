# 💖 Date Proposal Web Application

An interactive, multi-step web application built with HTML, CSS, and JavaScript designed to propose a date to someone special. The app features smooth animations, confetti effects, date/time scheduling, automatic WhatsApp redirection, and silent email notifications via EmailJS.

---

## ✨ Features

- **Interactive Flow**: Multi-step pages guiding the user smoothly from the initial proposal to preference selection and date scheduling.
- **Visual Effects**: Built-in CSS animations and dynamic HTML5 Canvas confetti celebrations.
- **WhatsApp Integration**: Automatically redirects the user to WhatsApp with all filled-in choices pre-formatted into a direct message.
- **Silent Email Forwarding**: Submits all user choices in the background to a designated email address using EmailJS without interrupting the user experience.
- **Responsive & Lightweight**: Pure HTML/CSS/JS with zero heavy external dependencies.

---

## 🛠️ Setup Instructions

### 1. Prerequisites
To enable the silent email notification feature, set up a free [EmailJS](https://www.emailjs.com/) account:

1. Sign up at [EmailJS](https://www.emailjs.com/).
2. Create an **Email Service** connected to your recipient email address (`zondolulama49@gmail.com`).
3. Create an **Email Template** using the following dynamic variable tags:
   - `{{first_choice}}`
   - `{{preference}}`
   - `{{date}}`
   - `{{time}}`
4. Copy your **Public Key**, **Service ID**, and **Template ID** from the EmailJS dashboard.

---

### 2. Configuration

Open `index.html` in your text editor and update the following placeholders:

#### A. EmailJS Credentials
Locate the EmailJS setup section in the `<script>` tag near the top:
```javascript
(function() {
  emailjs.init("YOUR_PUBLIC_KEY"); // Replace with your EmailJS Public Key
})();
