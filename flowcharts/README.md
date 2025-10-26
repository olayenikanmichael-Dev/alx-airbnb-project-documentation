# 🧭 Airbnb Clone – Property Booking Workflow 

## 📋 Overview
This flowchart breaks down the **Property Booking** backend process into detailed sub-steps, illustrating authentication, data handling, payment, and communication workflows.

It complements the Level 1 overview diagram and provides developers with insight into system logic and integration points.



## 🧩 Workflow Steps

| Step | Description |
|------|--------------|
| **1. User selects property and dates** | The user initiates the booking by choosing available dates. |
| **2. Validate user session** | Backend verifies the user’s authentication via JWT token or session cookie. |
| **3. Check if user is authenticated** | Prevents unauthorized access or booking attempts. |
| **4. Fetch property details** | Retrieves property data (price, host info, availability) from the database. |
| **5. Check and reserve availability** | Temporarily locks selected dates to prevent double-booking. |
| **6. Is property available?** | Decides if booking can proceed or aborts the process. |
| **7. Calculate total cost** | Includes nightly rate, service fees, and tax. |
| **8. Send payment request** | Integrates with Stripe or PayPal for payment authorization. |
| **9. Payment success check** | Verifies transaction confirmation. |
| **10. Create booking record** | Updates database with confirmed booking and payment details. |
| **11. Send confirmation emails** | Notifies both guest and host of successful booking. |

---

## 🧠 Key Insights
- Backend systems rely on **atomic operations** for reliability (booking + payment must succeed together).
- Temporary date locking prevents **double-booking conflicts**.
- Using **transactional databases** ensures payment and booking consistency.
- Integrating external APIs (Stripe/PayPal) introduces asynchronous workflows — handled via webhooks or callbacks.

---

## 📊 Diagram Information
- **File Name:** `property-booking-workflow-level2.png`
- **Tool:** Draw.io
- **Directory:** `workflow-diagram/`
- **Repository:** `alx-airbnb-project-documentation`

---

## 🧾 Submission Summary
| Item | Description |
|------|--------------|
| **Diagram** | Property Booking Workflow (Level 2) |
| **Export Format** | PNG |
| **Saved in** | `workflow-diagram/` |
| **GitHub Repo** | `alx-airbnb-project-documentation` |

