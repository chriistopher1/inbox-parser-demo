# 📬  Inbox Parser

Turn messy emails and their attachments into clean, structured Excel data, automatically.

INBOX PARSER receives emails at a dedicated inbox address, extracts the information inside the email body and its attachments, and delivers it as a structured spreadsheet. It is built for small businesses that receive orders, invoices, and reports by email and are tired of copying them into Excel by hand.

> **Portfolio showcase.** This repository is published to demonstrate my work. It is **not** an open-source project and is not licensed for reuse, redistribution, or contributions.

---

## 📸 VIDEO DEMO
https://youtu.be/5Y_MNANsMUc

## 📖 About the Project

Many businesses run on email: purchase orders, invoices, booking confirmations, and delivery notes all arrive as unstructured text and attachments. Someone then has to read each one and retype the data into a spreadsheet, which is slow and error-prone.

ParseKoi automates that workflow. Forward or send emails to your parser inbox, and the data you care about is extracted and organized into rows and columns, ready to download as an Excel file. It is inspired by tools like [Parseur](https://parseur.com), with a focus on the needs of Indonesian small and medium businesses, including local payment support.

---

## ✨ Features

- **Dedicated inbox address:** receive emails into your own parser inbox
- **Email content parsing:** extract structured fields from the email body
- **Attachment parsing:** pull data out of attached documents as well
- **Excel export:** get results as a structured `.xlsx` file
- **Subscription & payments:** pay with local Indonesian payment methods via Xendit
- **Authentication & user data:** secure accounts and per-user data storage

---

## 🛠️ Tech Stack

| Purpose | Technology |
|---|---|
| **Framework** | Next.js |
| **Backend / Database / Auth** | Supabase |
| **UI Components** | shadcn/ui |
| **Payments** | Xendit |
| **Inbound Email (Webhook)** | Resend |

---

## 🏗️ How It Works

```
 Incoming email
       │
       ▼
┌──────────────┐   webhook   ┌──────────────┐   store   ┌──────────────┐
│    Resend    │ ──────────► │   Next.js    │ ────────► │   Supabase   │
│ (inbound)    │             │  API routes  │           │ (DB/Storage) │
└──────────────┘             └──────┬───────┘           └──────────────┘
                                    │ parse email + attachments
                                    ▼
                             Structured data
                                    │
                                    ▼
                              Excel (.xlsx)
```

1. An email arrives at the user's parser address.
2. Resend forwards it to the app through a webhook.
3. The app parses the email content and attachments into structured data.
4. Results are stored in Supabase and made available as an Excel download.
5. Xendit handles subscription payments for paid plans.

---

## 🎯 What I Learned / Highlights

- Handling inbound email through webhooks and processing payloads reliably
- Parsing unstructured content and attachments into structured data
- Integrating a local payment gateway (Xendit) into a SaaS-style product
- Using Supabase for authentication, database, and file storage
- Building a clean, accessible UI with shadcn/ui on Next.js
- Designing a product around a real market need

---

## 🚀 Roadmap (Ideas)

- [ ] Custom parsing templates per sender or document type
- [ ] Integrations (Google Sheets, webhooks, Zapier)
- [ ] Parsing history and usage analytics
- [ ] Team accounts and shared inboxes

---

## 📄 License & Usage

This project is a **personal portfolio showcase**. All rights reserved. The source code is shared for viewing purposes only and may not be copied, modified, or distributed without permission.

---

## 👤 Author

**Chris** : Full stack developer
