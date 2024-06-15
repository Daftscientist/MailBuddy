# 📧 MailBuddy

Welcome to the **MailBuddy Library**! This is a Python utility designed to make sending formatted emails a breeze! With support for both plain text and HTML email bodies, dynamic content injection, and easy SMTP server configuration, MailBuddy takes the hassle out of email composition. 🎉

## 🚀 Features

- **SMTP Server Configuration**: Easily set up your SMTP server with the `host` and `port` parameters.
- **Flexible Email Body Input**: Add email bodies as plain text, HTML, or even read from files.
- **Dynamic Content Injection**: Use format variables to personalize your email content.
- **Easy Email Sending**: Send emails with a single method call.

## 🛠️ Installation

Clone the repository:

```bash
git clone https://github.com/daftscientist/MailBuddy.git
```

Navigate to the project directory:

```bash
cd MailBuddy
```

## 🌟 Usage

Here's a quick example to get you started:

```python
from MailBuddy import Email

# Create an email object
email = Email(
    host='smtp.example.com',
    port=587,
    sender='sender@example.com'
)

# Add email body
email.add_plain_body('Hello, {name}!')
email.add_html_body('<h1>Hello, {name}!</h1>')
email.add_format_variables({'name': 'Alice'})

# Send the email
email.send(
    recipient='recipient@example.com',
    subject='Greetings'
)
```

## 📋 Method Details

- **`Email(host: str, port: int, sender: str)`**: Initializes the `Email` object with SMTP server details and the sender's email address.
- **`add_html_body_from_file(file_path: str)`**: Adds an HTML body to the email from a file.
- **`add_format_variables(format_variables: dict)`**: Adds a dictionary of variables for formatting the email body, with the item to be replaced as the key.
- **`add_html_body(html_body: str)`**: Adds an HTML body to the email.
- **`add_plain_body(self, plain_body: str)`**: Adds a plain text body to the email.
- **`send(self, recipient: str, subject: str)`**: Composes and sends the email. The `recipient` parameter is the email address of the person receiving the email.

## 💬 Contributing

We welcome contributions! Feel free to open issues or submit pull requests. Let's make MailBuddy even better together! 🤝

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 📧 Contact

For any questions or suggestions, feel free to open an issue or reach out via email at [contact@leojohnston.tech
](mailto:contact@leojohnston.tech).

---

Happy emailing! 🚀📧✨

---
