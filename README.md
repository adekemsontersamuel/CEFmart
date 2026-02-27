# CEFMART – Staging Testing & Validation Guide  
**Prepared by Alpha N&S Technologies**  
**RC: 8289090**  
**Date: 27 February 2026**

---

## 📌 Overview

This document provides the official **Staging Testing & Validation Guidelines** for stakeholders conducting structured testing of the **CEFMART Application** prior to production deployment.

It defines:

- Environment configuration
- Scope of testing
- Security boundaries
- Infrastructure limitations
- Testing duration policy
- Production transition process

This README should be treated as the authoritative reference during staging validation.

---

# 🏗 Environment Status

## Current Deployment: **STAGING (Development Mode)**

The application is **NOT running in production**.

Staging allows:

- Full functional testing
- Simulated financial transactions
- Workflow validation
- Role-based testing (User / Vendor / Admin)

Staging restricts:

- Real financial processing
- Production API key usage
- Live merchant integration
- Sensitive environment exposure

---

# 🔐 Infrastructure Configuration

## 1️⃣ Payment Gateways

The following are configured in **Test Mode**:

- **Paystack (Test Keys Only)**
- **Flutterwave (Test Keys Only)**

Test keys:
- Simulate transactions
- Do not process real money
- Do not settle to live merchant accounts

⚠ Production payment keys are secured and will only be deployed in the live environment.

---

## 2️⃣ Database & Backend – Supabase

Staging uses:

- Supabase Test Project URL
- Supabase anon (public) test key
- Restricted service role access
- Test database records

Production-level credentials:
- Service role keys
- Elevated database privileges
- Production storage access

These remain protected and undisclosed during staging.

---

## 3️⃣ Authentication – Clerk

Staging uses:

- Clerk Test Publishable Key
- Clerk Test Secret Key
- Development JWT configuration

Production authentication secrets are not deployed in this environment.

---

## 4️⃣ Server & Environment Variables

The following remain secured:

- `.env` production variables
- Live payment API keys
- Supabase production service role keys
- Clerk production secrets
- Webhook signing secrets
- Admin-level credentials

These will only be injected during production deployment.

---

# 🌐 Domain & SSL Limitation

The current staging environment:

- Is not deployed under the final production domain
- Does not carry full production-grade SSL certification
- Is not linked to live financial monitoring accounts

Because of this:

- Live keys cannot be injected
- Real financial transactions are disabled
- Sensitive infrastructure remains isolated

This is standard security practice.

---

# ✅ Scope of Testing

Stakeholders are expected to test all modules within staging.

## 👤 User Module
- Registration
- Login
- Email verification flow
- Authentication redirects

## 🏪 Vendor Module
- Vendor onboarding
- Store setup
- Profile configuration

## 📦 Product Management
- Add product
- Edit product
- Delete product
- Upload images

## 🛒 Checkout & Payments (Simulated Only)
- Cart functionality
- Checkout workflow
- Test payment simulation

## 📊 Order Management
- Order creation
- Status updates
- Refund logic
- Tracking workflow

## 📝 Complaints & Grievance System
- Complaint submission
- Admin resolution flow
- Status tracking

## 🛠 Admin Dashboard
- Monitor users
- Monitor vendors
- Monitor transactions (test transactions only)

---

# 🔒 Data & Security Policy During Testing

During staging:

- Only test/dummy data must be used
- No real financial information should be entered
- No production keys should be requested
- No external merchant accounts should be connected

All production credentials remain under secure infrastructure managed by **Alpha N&S Technologies**.

---

# ⏳ Testing Window

The staging testing window is strictly limited to:

> **Maximum: 72 Hours**

Reason:

- Temporary environment
- Limited SSL configuration
- Security isolation from production
- Time-sensitive deployment schedule

Extended sandbox use is not permitted.

---

# 🚀 Transition to Production

Upon testing approval:

1. Production domain will be activated
2. Full SSL certification will be configured
3. Live payment keys will be injected
4. Supabase production project will be connected
5. Clerk production authentication will be activated
6. Joint financial monitoring account (Alpha + CEFTER) will be linked

Only after this process will real financial transactions be enabled.

---

# 🏢 Deployment Experience Reference

This is not our first commerce deployment.

Under our e-commerce arm, we operate:

- **Cityhackz**  
  https://www.cityhackz.com.ng  

- **Vendoor by Cityhackz**  
  https://vendoor.cityhackz.com.ng  

These platforms reflect our production-grade deployment standards.

---

# 📋 Stakeholder Responsibilities During Testing

Stakeholders are required to:

- Test all assigned modules thoroughly
- Document bugs clearly and structurally
- Provide consolidated feedback
- Avoid fragmented or repeated requests
- Respect infrastructure security boundaries

Operational entanglements or delayed responses may affect go-live timelines.

---

# ⚠ Important Clarification

### Staging Allows:
- Functional validation
- Workflow verification
- Role-based access testing
- Business logic validation
- System stability checks

### Staging Restricts:
- Real financial transactions
- Production API keys
- Live merchant integration
- Sensitive environment exposure

This separation protects:

- Financial integrity
- Data security
- Compliance requirements
- Platform stability


### Testilink:
- Find attached the testing link
https://cefmart-test.vercel.app/

This separation protects::
---

# 📞 Support & Contact

For clarification during testing:
**alphanstech@cityhackz.com.ng**
**Alpha N&S Technologies**  
RC: 8289090  

---

## Prepared By

**Adeke Msonter Samuel**  
Alpha N&S Technologies  

🔗 https://adekems.vercel.app/

