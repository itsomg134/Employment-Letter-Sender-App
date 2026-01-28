# Employment Letter Sender App 

A professional, user-friendly web application for creating and sending employment letters to candidates. Built with HTML, CSS, and JavaScript.

![App Preview](https://via.placeholder.com/800x400/1a73e8/ffffff?text=Employment+Letter+Sender+App)

## Features ✨

- **Multiple Templates**: Choose from Job Offer, Rejection, and Appointment letter templates
- **Live Preview**: Real-time preview of your employment letter as you type
- **Form Validation**: Ensures all required fields are filled before sending
- **Character Counter**: Track custom message length with visual feedback
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- **Simulated Email Sending**: Demonstrates email functionality with realistic status updates
- **Clean UI**: Modern, professional interface with intuitive controls

## Screenshots 📸

![Form Section](https://via.placeholder.com/400x300/1a73e8/ffffff?text=Letter+Details+Form)
![Preview Section](https://via.placeholder.com/400x300/34a853/ffffff?text=Letter+Preview)

## Getting Started 🚀

### Prerequisites

No installation required! This is a pure frontend application that runs directly in your browser.

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/employment-letter-sender.git
```

2. Navigate to the project directory:
```bash
cd employment-letter-sender
```

3. Open `index.html` in your browser:
```bash
# On macOS
open index.html

# On Windows
start index.html

# On Linux
xdg-open index.html
```

Alternatively, you can simply double-click the `index.html` file.

## Usage 📝

1. **Select a Template**: Choose from Job Offer, Rejection, or Appointment templates
2. **Fill Candidate Details**: Enter the candidate's name, email, and job position
3. **Customize the Letter**: Add start date, salary, company details, and custom message
4. **Preview**: Click "Preview Letter" to see how your letter will look
5. **Send**: Click "Send Letter" to simulate email delivery

## File Structure 📁

```
employment-letter-sender/
├── index.html          # Main application file
├── README.md           # This documentation file
└── assets/             # (Optional) Directory for images and icons
```

## How It Works 🔧

The application uses vanilla JavaScript to:
- Dynamically update the letter preview as users type
- Validate form inputs before sending
- Simulate email sending with realistic delays
- Switch between different letter templates
- Maintain a log of all actions and status updates

## For Production Use 🏗️

To convert this demo into a production-ready application:

1. **Backend Integration**: Connect to an email service (SendGrid, AWS SES, Nodemailer)
2. **Authentication**: Add user login and account management
3. **Database**: Store templates and sent letters in a database
4. **Security**: Implement input sanitization and API security
5. **File Export**: Add PDF generation and download options

### Example Backend Integration

```javascript
// Node.js/Express example with Nodemailer
app.post('/send-letter', async (req, res) => {
  const { candidateEmail, subject, letterContent } = req.body;
  
  const transporter = nodemailer.createTransport({
    service: 'gmail',
    auth: {
      user: process.env.EMAIL_USER,
      pass: process.env.EMAIL_PASS
    }
  });
  
  const mailOptions = {
    from: process.env.EMAIL_USER,
    to: candidateEmail,
    subject: subject,
    text: letterContent
  };
  
  try {
    await transporter.sendMail(mailOptions);
    res.json({ success: true, message: 'Letter sent successfully' });
  } catch (error) {
    res.status(500).json({ success: false, error: error.message });
  }
});
```

## Browser Compatibility 🌐

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## Contributing 🤝

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Development Tasks

- [ ] Add more letter templates
- [ ] Implement PDF export functionality
- [ ] Add dark mode
- [ ] Create template management system
- [ ] Add multi-language support
- [ ] Implement undo/redo functionality

## License 📄

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📬 Contact

Om Gedam

GitHub: @itsomg134

Email: omgedam123098@gmail.com

Twitter (X): @omgedam

LinkedIn: Om Gedam

Portfolio: https://ogworks.lovable.app

### Deploy to GitHub Pages

1. Push your code to a GitHub repository
2. Go to Repository Settings > Pages
3. Select "main" branch and save
4. Your app will be live at `https://yourusername.github.io/employment-letter-sender`

### Deploy to Netlify

1. Drag and drop the `index.html` file to [Netlify Drop](https://app.netlify.com/drop)
2. Get a live URL instantly

### Deploy to Vercel

1. Install Vercel CLI: `npm i -g vercel`
2. Run `vercel` in the project directory
3. Follow the prompts to deploy
