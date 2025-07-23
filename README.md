# decenterlised-banking
# Centralised Banking FinTech System

## Overview

This project is a centralized fintech platform that leverages modern web technologies to provide a seamless, secure, and real-time banking experience. powered through centralized bank APIs, this system enables users to send, receive, and store money via wallets, perform bank verifications, and interact with mobile money recipients without needing traditional bank accounts.

We propose the development of a centralized fintech platform that allows users to create a wallet, link their bank accounts using secure bank APIs, transfer funds between wallets in real time, and redeem wallet funds as mobile money even without traditional bank accounts.

The system adopts Web3-inspired principles (like wallet interoperability and P2P transfers) while relying on centralized, secure infrastructure to maintain compliance, reduce costs, and speed up integration with local banks.

🔹 Core Objectives
Provide a modern financial access platform for users with and without bank accounts.

Enable secure, real-time peer-to-peer wallet transfers.

Integrate with South Africa’s main banks via APIs to allow balance checks and deposits/withdrawals.

Allow mobile-based redemptions and withdrawals for unbanked users.

Implement transaction-based revenue model similar to PayGate or Yoco.

🔹 MVP Architecture
👤 User Authentication
OAuth 2.0 (using Supabase Auth) for secure sign-up/sign-in with email, phone, or social providers.

💳 Bank Integration
Use standardized APIs from major South African banks (e.g., Absa, FNB, Standard Bank) for:

Account verification

Balance checks

Transfers to/from wallet

💰 Wallet System
Each user gets a virtual wallet.

Wallets can:

Receive/send money to other wallets instantly.

Pull/push funds from connected bank accounts.

Send funds to mobile phone numbers for redemption later.

🔔 Notifications
Integrated using OneSignal for push notifications:

Transaction alerts

Security warnings

Promotional messages

📦 Backend + Database
Supabase (PostgreSQL) for database, authentication, and edge functions.

Real-time data sync

Cost-effective and predictable pricing

No need to manage servers

Optional future expansion to Node.js middleware if banking API needs orchestration.

📱 Frontend
React Native (Expo or bare) for Android and iOS apps.

Focus on:

Simplicity

Clean UI/UX

Easy wallet interactions

🔹 Revenue Model
We’ll adopt a PayGate-style revenue model:

Feature	Model
Wallet-to-wallet transfers	Free (initially)
Bank integration fees	% of transaction
Mobile redemption	Small flat fee
Partnered merchant tools	Premium API access

We earn a small % per transaction that flows through the platform.

🔹 Benefits for the User
Accessible financial services without needing a bank account

Real-time money movement between wallets

Easy mobile redemptions and deposits

No need for crypto understanding or management

🔹 Team & Development Plan
Team: 2 developers

Backend and integration: Developer A

Frontend and mobile: Developer B

Development Timeline (MVP): ~6–8 weeks

Week 1–2: Supabase setup, auth, wallet schema

Week 3–4: Bank API integration + OneSignal

Week 5–6: Wallet logic, send/receive, mobile payout

Week 7–8: UI polish, testing, deployment

🔹 Scalability & Future Phases
Add identity verification (KYC) using services like Smile Identity or Yoti

Expand to other African markets with mobile-first banking systems

Add analytics, merchant tools, and reporting dashboard

Optional Web version or desktop PWA

🔹 Tech Stack Summary
Layer	Technology
Frontend	React Native
Backend	Supabase (DB + Auth)
Notifications	OneSignal
Bank APIs	Open Banking Standards
Payments	Mobile Money APIs

Key Differentiators Compared to Existing Market Solutions
1. Unified Wallet Ecosystem Bridging Banked & Unbanked
Most existing solutions in South Africa (like Capitec, Nedbank Money App, FNB, or even SnapScan) target customers who already have bank accounts. Your solution:

Allows users without bank accounts to receive funds via mobile money (or virtual wallet),

Funds can later be redeemed or used without needing a traditional account,

Bridges the gap between fully banked, underbanked, and unbanked users.

🟢 This inclusive model is not well-covered in the existing app ecosystem.

2. Real-Time Inter-Bank Wallet System via Bank APIs
While banks provide apps that only work within their own ecosystem, your proposal:

Uses OAuth + Banking APIs (e.g., Stitch, TrueID, Yoco Bank Integration, or BankservAfrica if accessible),

Enables users to view and move money across multiple banks from one platform,

Real-time bank balance updates and transfers.

🟢 Existing banking apps don’t offer this level of cross-bank interaction.

3. Peer-to-Peer Transfers with Centralized Infrastructure
Unlike pure Web3 wallets that rely on cryptocurrencies and blockchains:

system allows P2P transfers between users inside the app, mimicking Web3-style flow,

But built with centralized control, making it:

Faster,

Cheaper,

Legally compliant with SARB/KYC rules.

🟢 Most Web3 wallets are crypto-first and don’t integrate with banks.
🟢 Most bank apps don’t allow wallet-to-wallet transfers outside their ecosystem.

4. Built-in Offline/Mobile Money Redemption System
Many rural or informal workers:

Do not have smartphones or bank apps,

Cannot receive eWallets that require smartphone apps.

Your model supports:

Redeeming wallet funds via mobile money or voucher code,

Agent-based withdrawal system, similar to how MTN MoMo or Flash works but open to all banks.

🟢 Existing bank and fintech apps don’t universally support mobile-to-cash redemption across banks.

5. Affordable & Scalable Tech Stack
Unlike many legacy or bloated FinTech systems:

Your MVP uses:

Supabase (PostgreSQL + auth + serverless),

OneSignal for push,

React Native for cross-platform mobile development.

Lean team of 2, meaning faster iterations, lower burn rate, and custom features for niche audiences.

🟢 Most competitors use complex, expensive legacy systems with limited innovation velocity.

6. Revenue Model Built into Transaction Layer
Your model earns via:

A small fee or % from every transaction (like PayGate or Yoco),

Future potential to offer:

Premium features (virtual cards, FX),

Business accounts and payroll integrations,

Micro-loans.

🟢 Competitors often rely on ads, upsells, or banking partnerships alone.

🔹 Final Notes
This MVP is designed to be cost-effective, scalable, and realistic for a two-person team. It focuses on interoperability, speed, and financial inclusion — bridging the gap between the unbanked and digital wallets through modern fintech patterns.

---

## 👥 Team

Built by a team of 2 passionate developers focused on delivering a secure, accessible, and scalable fintech solution.

---

## 🧠 Key Features

- 🔐 **OAuth Sign-in**: Secure user authentication via phone number or email.
- 💳 **Wallet System**: Users hold balances in wallets for instant transactions.
- 🔄 **Bank Integrations**: Real-time bank balance checks and transactions via major South African bank APIs.
- 🧾 **Transaction Ledger**: Complete record of all wallet and bank interactions.
- 💸 **Send & Receive Funds**: 
  - Between wallet users.
  - To unbanked mobile recipients (redeemable via code at mobile money outlets).
- 🔔 **Push Notifications**: Realtime updates via OneSignal.
- 📈 **Analytics & Logs**: Monitor usage and flows through integrated dashboards (planned).

---

## 🏦 Tech Stack

| Layer               | Stack                       |
|--------------------|-----------------------------|
| Frontend (App)     | React Native                |
| Backend Services   | Supabase (Postgres + Auth)  |
| Messaging/Push     | OneSignal                   |
| Bank Integrations  | OAuth + REST APIs (Capitec, FNB, Standard Bank, etc.) |
| Cloud Hosting      | Supabase + OneSignal        |
| Payments Revenue   | Paygate-style % per transaction |

---

## 💰 Monetization Strategy

- **Transaction Fee**: Earn a small % fee on each wallet or mobile money transaction, similar to a paygate or airtime recharge model.

---

## 🔧 Setup Instructions

1. **Clone this repo**  
   ```bash
   git clone https://github.com/yourusername/fintech-web3.git
Install dependencies

bash
Copy
Edit
npm install
Set up Supabase

Create a project on https://supabase.io

Copy your keys to .env

Configure OneSignal

Create an account on https://onesignal.com

Add your App ID to your project

Run the App

bash
Copy
Edit
npm start
📱 User Flow Summary
User signs up using phone/email via OAuth.

A wallet is created on account.

User can:

View wallet balance

Connect bank account for syncing

Send funds to:

Another wallet

Mobile number (unbanked recipient)

Mobile recipient gets SMS or app code to redeem funds.

Push notifications update all parties in real-time.

📌 Roadmap
 MVP planning & architecture

 Build and test wallet system

 Integrate bank APIs

 Enable mobile redemption

 Launch closed beta

🛡 Security
Secure OAuth sign-in

End-to-end encryption where required

Data stored securely via Supabase Postgres

All API interactions are authenticated
