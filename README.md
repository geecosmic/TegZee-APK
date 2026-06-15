# TegZee — Ride‑Hailing Platform

> A modern ride‑hailing platform connecting passengers with verified drivers through a fast, secure, and real‑time experience.

Built with **Flutter**, **Django**, and **Supabase**.

---

## Overview

TegZee is a full‑stack ride‑hailing solution designed to support passenger transportation, driver operations, wallet management, scheduling, referrals, and real‑time ride tracking.

The platform provides:

- Real‑time ride booking and tracking
- Driver onboarding and verification
- Secure wallet and payment processing
- Scheduled rides
- Admin management tools
- Scalable cloud architecture

---

# Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Flutter (Dart) |
| Backend | Django (Python) |
| Database | PostgreSQL (Supabase) |
| Authentication | Supabase Auth |
| Payments | Paystack |
| Realtime | Supabase Realtime |
| Notifications | OneSignal + Firebase Cloud Messaging |
| Maps | Google Maps API |

---

# Project Structure

```text
ridefi/
├── auth/              # Authentication & account management
├── legal/             # Privacy policy & terms
├── models/            # Core application models
├── pilot/             # Driver module
├── profile/           # User profile & wallet
├── providers/         # Riverpod state management
├── referral/          # Referral system
├── ride/              # Ride lifecycle
├── services/          # APIs & business services
└── widgets/           # Shared UI components
```

---

# Core Features

## Passenger Experience

- User registration and authentication
- Ride request with pickup & destination selection
- Real‑time driver tracking
- Wallet funding via Paystack
- Wallet and cash payment support
- Ride scheduling
- Saved locations
- Ride history
- Referral rewards
- Emergency contacts & SOS
- Driver ratings and reviews
- Help and support center

---

## Driver Experience

- Driver onboarding & verification
- Vehicle profile management
- Online / offline availability
- Ride acceptance workflow
- Navigation to pickup location
- Ride start and completion
- Earnings analytics
- Withdrawal requests
- Bank account management
- Cash ride debt tracking

---

## Admin Dashboard

- User administration
- Driver approval workflow
- Ride monitoring
- Withdrawal processing
- Platform wallet visibility
- Dynamic content management

---

# Application Screens

| Screen | Purpose |
|---|---|
| Authentication | Login & registration |
| Home | Search, suggestions & promotions |
| Ride Request | Pickup & destination |
| Nearby Drivers | Driver discovery |
| Driver Tracking | Live ride updates |
| Wallet | Funding & transaction history |
| Profile | Account management |
| Driver Dashboard | Driver operations |
| Vehicle Information | Vehicle management |
| Bank Accounts | Withdrawals |
| Emergency | SOS & emergency contacts |
| Referral | Rewards & invitations |
| Help Center | Support |
| Saved Places | Favorites |

---

# User Flows

## Book a Ride

1. Open TegZee
2. Enter pickup & destination
3. Search available drivers
4. Confirm request
5. Driver accepts
6. Track ride in real time
7. Complete payment
8. Submit ride rating

---

## Driver Onboarding

1. Register account
2. Request driver access
3. Complete verification
4. Add vehicle details
5. Add payout account
6. Go online

---

## Wallet Flow

1. Add funds
2. Complete Paystack payment
3. Wallet updates automatically
4. Pay for rides
5. Withdraw earnings

---

# API Endpoints

| Endpoint | Description |
|---|---|
| `/api/payments/login/` | JWT authentication |
| `/api/payments/wallet/balance/` | Wallet balance |
| `/api/payments/wallet/add/` | Fund wallet |
| `/api/payments/wallet/deduct/` | Debit wallet |
| `/api/payments/withdrawal/request/` | Withdrawal |
| `/api/payments/platform-wallet/` | Platform wallet |
| `/api/payments/webhook/` | Paystack webhook |

---

# Database Overview

## Profiles

```text
uid
email
display_name
phone
user_type
is_verified
status
wallet_balance
car_model
license_plate
driver_photo
vehicle_image
```

## Ride Collections

```text
ride_requests
active_rides
future_rides
```

## Payment Models

```text
Wallet
WalletTransaction
WithdrawalRequest
PlatformWallet
```

---

# Environment Variables

## Flutter

```dart
const djangoBaseUrl =
'https://your-backend.com/api/payments';
```

## Django

```env
PAYSTACK_SECRET_KEY=
PAYSTACK_PUBLIC_KEY=
SUPABASE_URL=
SUPABASE_ANON_KEY=
```

---


## Deployment Status

| Component | Status | Platform |
|-----------|--------|----------|
| Flutter App | Ready | Github |
| Django Backend | Ready | Hugging Face |
| Database | Live | Supabase (PostgreSQL) |
| Storage | Live | Supabase Storage |

## Current Status

- ✅ Core features complete
- ✅ Payment integration working
- ✅ Driver/passenger flows tested
- ⏳ Pending: Production deployment
- ⏳ Pending: App store submission

## Deployment Targets (Future)

| Component | Target Platform |
|-----------|-----------------|
| Flutter App | Google Play Store, Apple App Store |
|  Django Backend (future) | Render / Railway / DigitalOcean|
| Database | Supabase (already live) |

---

# Getting Started

## Flutter

```bash
flutter pub get
flutter run
```

## Django

```bash
python -m venv venv
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

---

# Contributors

**George Eyo**  
Lead Developer

---

# License

All Rights Reserved.

Commercial licensing and full source access available upon request.