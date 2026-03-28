# AuthSystem — Bootstrap 5 Authentication UI

## Project Description

A complete, fully responsive authentication system UI built with **Bootstrap 5**,
**Bootstrap Icons**, and custom CSS. No templates, no frameworks beyond Bootstrap —
original design only.

---

## Tech Stack

| Layer     | Technology                        |
|-----------|-----------------------------------|
| Markup    | Semantic HTML5                    |
| Styling   | Bootstrap 5.3 (CDN) + styles.css  |
| Icons     | Bootstrap Icons 1.11 (CDN)        |
| Fonts     | Google Fonts — Poppins            |
| Scripting | Vanilla JavaScript (ES6+)         |

---

## Project Structure

```
authentication-system-styled/
├── index.html            ← Login page
├── register.html         ← Registration page
├── forgot-password.html  ← Forgot password page
├── reset-password.html   ← Reset password page
├── dashboard.html        ← User dashboard
├── styles.css            ← All custom styles
└── README.md
```

---

## Pages

| File                   | Purpose                           |
|------------------------|-----------------------------------|
| `index.html`           | Login with email + password       |
| `register.html`        | New user registration             |
| `forgot-password.html` | Request a password reset link     |
| `reset-password.html`  | Set a new password                |
| `dashboard.html`       | Authenticated user dashboard      |

---

## Navigation Flow

```
Login (index.html)
  ├── Submit form        → dashboard.html
  ├── "Create one"       → register.html
  └── "Forgot password?" → forgot-password.html

Register (register.html)
  ├── Submit form        → index.html
  └── "Sign in"          → index.html

Forgot Password (forgot-password.html)
  ├── Submit email       → success state → reset-password.html
  └── "Back to Login"    → index.html

Reset Password (reset-password.html)
  ├── Submit new password → index.html
  └── "Back to Login"     → index.html

Dashboard (dashboard.html)
  └── Logout             → index.html
```

---

## Features

### All Pages
- Bootstrap 5 + Bootstrap Icons via CDN
- Single shared `styles.css`
- Fully responsive: 320px → 768px → 1366px → 1920px+
- Dark mode toggle (persisted via `localStorage`)
- Smooth 0.28s transitions on all interactive elements
- Animated gradient background blobs

### Login (`index.html`)
- Email + password inputs with icon prefixes
- Show / hide password toggle (Bootstrap Icons)
- Remember me checkbox
- Client-side validation with inline error messages
- Loading spinner on submit → redirect to dashboard
- Google + GitHub social login buttons (UI only)

### Register (`register.html`)
- Full Name, Email, Password, Confirm Password
- Real-time password strength bar (Weak / Fair / Good / Strong)
- Password requirements checklist (length, uppercase, number, special char)
- Bootstrap `is-valid` / `is-invalid` states on all fields
- Terms & conditions checkbox
- Loading spinner on submit → redirect to login

### Forgot Password (`forgot-password.html`)
- Email input with validation
- Loading spinner on submit
- Animated success state replaces form after submission
- "Continue to Reset" CTA → reset-password.html

### Reset Password (`reset-password.html`)
- New Password + Confirm Password
- Show / hide toggle on both fields
- Real-time strength bar + requirements checklist
- Validation with custom error messages
- Loading spinner on submit → redirect to login

### Dashboard (`dashboard.html`)
- Sticky navbar with brand, user chip, dark mode toggle, logout
- Welcome banner with gradient + decorative circles
- 4 stat cards (Users, Sessions, Uptime, Alerts) with trend badges
- Recent activity feed with colour-coded dots
- Quick actions grid (Edit Profile, Change Password, Security, Notifications)
- Profile completion progress bar
- Security score progress bar

---

## Custom CSS Highlights (`styles.css`)

- CSS custom properties for light + dark themes
- Google Fonts: Poppins
- Animated radial-gradient background blobs on auth pages
- Card slide-up entrance animation
- Brand icon pulse animation
- Icon-prefixed inputs
- Gradient primary button with hover lift + glow
- 4-segment password strength bar with colour transitions
- Requirements checklist with live check / cross icons
- Fully dark-mode aware via `[data-theme="dark"]`

---

## GitHub Repository

```
https://github.com/Sultan0211-stu/html-authentication-poc
```


---

## Important Notes

- This is a **front-end only** POC — no backend or real authentication logic
- No CSS frameworks other than Bootstrap 5 are used
- No JavaScript frameworks or libraries are used
- Dark mode preference persists across all pages via `localStorage`
- Repository should be set to **public**
