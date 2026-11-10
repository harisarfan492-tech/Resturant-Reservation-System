# 🍽️ Restaurant Reservation Automation

An automated restaurant table reservation system built with **n8n, Google Sheets, and Gmail**. Customers can submit reservation requests through a form, automatically check table availability, and receive email confirmations.

## 🚀 Features

- **Reservation Form:** Collects customer name, email, phone number, reservation date, time, guest count, and special requests.
- **Automated Availability Checking:** Checks existing reservations in Google Sheets to prevent duplicate bookings for the same date and time.
- **Automatic Booking Confirmation:** Confirms available reservations and records them in Google Sheets.
- **Reservation Tracking:** Generates a unique reservation ID and records the booking timestamp.
- **Email Notifications:** Sends confirmation emails to customers.
- **Conflict Detection:** Identifies already-booked time slots and generates an unavailable booking response.
- **No-Code Automation:** Entire workflow orchestrated through n8n.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| n8n | Workflow automation |
| Google Sheets | Reservation database |
| Gmail | Customer email notifications |
| JavaScript | Reservation availability logic |

## ⚙️ Workflow

1. Customer submits the reservation form.
2. Reservation details are processed and assigned metadata.
3. Existing reservations are retrieved from Google Sheets.
4. JavaScript checks whether the requested date and time are already booked.
5. An IF node determines the booking outcome:
   - **Available:** Reservation is recorded in Google Sheets and a confirmation email is sent.
   - **Unavailable:** The workflow generates a rejection response for the customer.
6. Customer receives the appropriate booking response.

## 📋 Reservation Information

The system collects:

- Customer Name
- Email
- Phone Number
- Date of Reservation
- Time of Reservation
- Number of Guests
- Special Requests

## 🔧 Setup

### Requirements

- n8n instance
- Google account
- Google Sheets
- Gmail account

### Installation

1. Download the workflow JSON from this repository.
2. Import it into your n8n instance.
3. Connect your Google Sheets OAuth credentials.
4. Connect your Gmail OAuth credentials.
5. Configure your reservation spreadsheet and column headers.
6. Activate the workflow.
7. Share the reservation form URL with customers.

## 📊 Reservation Database

Google Sheets is used to store reservation information, including:

- Reservation ID
- Customer details
- Booking date and time
- Number of guests
- Special requests
- Booking status
- Creation timestamp

## 📌 Project Purpose

This project demonstrates how business processes can be automated using n8n, integrating external services, implementing custom JavaScript logic, and handling customer communication automatically.

Built as a practical automation project and portfolio demonstration.

## 👨‍💻 Author

**Haris Arfan**

