# 🛒 SmartCommerce AI

A modern, full-stack E-Commerce platform built with **Next.js 16**, **Sanity CMS**, **Stripe**, and **Clerk**, featuring an autonomous **AI Shopping Copilot** powered by **Google Gemini** & **Vercel AI SDK**.

---

## 🌟 About the App

**SmartCommerce AI** is an intelligent e-commerce store designed to deliver a fast, real-time shopping experience. Customers can explore a dynamic product catalog, filter products in real-time, manage a persistent cart, and interact with a conversational AI agent that can recommend products, search inventory with filters, and track past orders.

---

## ✨ Core Functionalities

* 🤖 **AI Shopping Copilot**: Conversational assistant powered by Google Gemini that searches products by category, material, color, and price range, and checks order statuses for signed-in users.
* ⚡ **Real-Time Live Catalog**: Uses Sanity Live Content API (`defineLive`) so inventory and catalog updates appear instantly without page refreshes.
* 🔍 **Multi-Attribute Filtering**: Instant product filtering by category, material, color, price slider, and stock availability.
* 🛍️ **Persistent Shopping Cart**: Fast, responsive cart operations managed with Zustand with optimistic updates.
* 💳 **Secure Stripe Checkout**: Server-side stock and price validation before session creation to prevent price manipulation.
* 🔄 **Idempotent Webhooks & Atomic Inventory**: Stripe webhook handler with signature verification and atomic Sanity transactions to prevent duplicate orders and overselling.
* 🔐 **Authentication & Customer Sync**: User authentication via Clerk, automatically synchronized with Stripe Customer IDs and Sanity records.
* 📊 **Admin Dashboard & CMS**: Built-in inventory tracking, order management, and Sanity Studio mounted at `/studio`.

---

## 💳 Testing Payments with Stripe

You can test the full checkout flow without real money using Stripe's standard test card:

| Field | Test Value |
| :--- | :--- |
| **Card Number** | `4242 4242 4242 4242` |
| **Expiration Date** | Any future date (e.g., `12/30`) |
| **CVC / CVV** | Any 3 digits (e.g., `123`) |
| **Postal Code** | Any valid postal code (e.g., `90210` or `SW1A 1AA`) |

---

## 🛠️ Tech Stack

* **Frontend**: Next.js 16 (App Router), React 19, TypeScript, Tailwind CSS
* **AI & Agent**: Vercel AI SDK, Google Gemini API (`@ai-sdk/google`)
* **CMS & Database**: Sanity CMS (Live Content API, GROQ, Sanity Studio)
* **Payments**: Stripe API, Stripe Checkout & Webhooks
* **Authentication**: Clerk Auth
* **State Management**: Zustand

---

## 🚀 Quick Setup

```bash
# 1. Clone the repository
git clone https://github.com/solvingop/ecommerce-ai-platform.git

# 2. Install dependencies
npm install

# 3. Start development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to view the app or [http://localhost:3000/studio](http://localhost:3000/studio) for Sanity Studio.
