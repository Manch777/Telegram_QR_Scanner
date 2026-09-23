# Telegram QR Scanner

A lightweight, mobile-friendly web QR scanner designed as a companion application for the **Telegram QR Event Bot**.

The scanner uses the device camera to read ticket QR codes and forwards the scanned payload to the Telegram bot through a deep link for ticket validation.

## Features

- QR code scanning directly in the browser
- Mobile-friendly responsive interface
- Device camera access
- QR recognition with ZXing Browser
- Automatic redirect to the Telegram bot after scanning
- Telegram deep-link integration
- No separate backend required
- Suitable for event entrance and ticket validation workflows

## How It Works

1. An event administrator opens the scanner web application.
2. The browser requests access to the device camera.
3. The administrator scans a guest's QR ticket.
4. The scanner reads the QR payload.
5. The payload is passed to the Telegram bot using a deep link.
6. The Telegram bot validates the ticket and processes the admission workflow.

## Tech Stack

- HTML5
- CSS3
- JavaScript
- ZXing Browser
- Telegram Deep Links
- Static web hosting

## Project Structure

```text
Telegram_QR_Scanner/
├── index.html
└── README.md
```

The application is intentionally lightweight and does not require a separate backend or database.

## Running Locally

Clone the repository:

```bash
git clone https://github.com/Manch777/Telegram_QR_Scanner.git
cd Telegram_QR_Scanner
```

Because camera access may require a secure context, it is recommended to run the application through a local development server instead of opening `index.html` directly.

For example:

```bash
python -m http.server 8000
```

Then open the local server in your browser.

## Deployment

The scanner is a static web application and can be deployed using services such as:

- Vercel
- GitHub Pages
- Netlify
- Any static web hosting service

## Telegram Integration

After a QR code is successfully scanned, its payload is forwarded to the Telegram bot using a deep link:

```text
https://t.me/<bot_username>?start=<qr_payload>
```

Ticket validation and admission logic are handled by the Telegram bot rather than by the scanner itself.

## Companion Project

This scanner is part of the **Telegram QR Event Bot** project.

The main application provides:

- Event registration
- Ticket management
- Payment workflows
- QR ticket generation
- Ticket validation
- Administrative tools
- PostgreSQL data storage
- Event configuration and management

Main repository:

**Telegram QR Event Bot**  
https://github.com/Manch777/Telegram_QR_Event_Bot

## Security and Privacy

- No Telegram bot token is stored in the scanner.
- No database credentials are required by the scanner.
- The scanner does not implement its own ticket validation logic.
- Ticket validation is performed by the Telegram bot backend.
- Sensitive backend configuration remains separate from the frontend scanner.

## Use Case

The scanner is designed for event staff who need a simple mobile interface for checking QR tickets at an entrance.

Together with the Telegram bot, it provides a complete workflow:

```text
Registration
    ↓
Payment
    ↓
QR Ticket
    ↓
Web Scanner
    ↓
Telegram Bot
    ↓
Ticket Validation
    ↓
Admission
```

## Project Status

The application is functional and serves as the scanning component of the Telegram QR Event Bot project.

## License

This project is provided for portfolio and demonstration purposes.
