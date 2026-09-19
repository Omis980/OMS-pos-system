# OMS POS System

A browser-based Point of Sale (POS) system designed for use on computers, tablets and mobile devices.

The system uses a single HTML frontend hosted through GitHub Pages and a Google Apps Script backend connected to Google Sheets.

---

## Features

### POS

- Product and combo selection
- Product categories
- Current order management
- Quantity controls
- Order total calculation
- Order confirmation
- Automatic order number generation
- Order history
- Cashier identification
- Shift statistics

### User Accounts

The POS includes an account-based login system.

Supported roles:

- `admin`
- `cashier`

Each account can have:

- Username
- Password
- Role
- Active/inactive status

Passwords are stored as SHA-256 hashes rather than plain text.

### Admin Panel

Administrators can:

- View registered users
- Create new users
- Change user roles
- Activate users
- Deactivate users
- Reset user passwords
- Manage the POS user system

### Responsive Design

The POS is designed to work on:

- Desktop computers
- Laptops
- Tablets
- Mobile phones

On smaller screens, the three main POS sections are automatically rearranged into a vertical layout.

---

## Architecture

The project consists of two main parts:

```text
┌──────────────────────────────┐
│          POS Frontend        │
│                              │
│        HTML / CSS / JS       │
│                              │
│        GitHub Pages          │
└──────────────┬───────────────┘
               │
               │ HTTPS requests
               ▼
┌──────────────────────────────┐
│      Google Apps Script      │
│                              │
│       Backend / API          │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│        Google Sheets         │
│                              │
│  Меню                       │
│  История                    │
│  Users                      │
└──────────────────────────────┘
