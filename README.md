# Technical Documentation for Sand Fintech Project

**Project Name:** Sand  
**Target Market:** Western Africa (Mali, Senegal, Ivory Coast, etc.)  
**Purpose:** A fintech platform offering digital wallets, P2P transfers, cash payment integration, and reloadable virtual debit cards, similar to CashApp.

## 1. System Architecture

### Frontend:

- **Framework:** Next.js (React-based framework for SSR and client-side rendering).

**Features:**

- User dashboard for managing wallets, cards, and transactions.
- Responsive design for mobile and desktop users.

### Backend:

- **Framework:** Node.js with Express.js for RESTful APIs.

**Features:**

- Authentication (OAuth2.0, JWT).
- Card issuing via Stripe API.
- Integration with Orange Money API.
- Transaction processing and user management.

### Database:

- **Primary DB:** PostgreSQL (for transactional and relational data).
- **Cache:** Redis (for session management and real-time operations).

### Cloud Infrastructure:

- **Hosting:** AWS (scalable and reliable).

**Key Services:**

- **EC2:** Application servers.
- **RDS:** Managed PostgreSQL database.
- **S3:** Storage for user assets (e.g., profile pictures).
- **CI/CD Pipeline:** GitHub Actions for deployment automation.

### Payments and Cards:

- **Stripe:**
  - Card issuing and payment processing.
  - Webhooks for transaction monitoring.
- **Orange Money API:**
  - Enable cash-in and cash-out functionalities.

### Security:

- **Standards:** PCI-DSS compliance, data encryption.
- **Authentication:** Two-Factor Authentication (2FA), end-to-end encryption.

## 2. API Documentation

### Authentication

- **Endpoint:** `/api/auth/login`
- **Method:** POST

**Payload:**

```json
{
  "email": "user@example.com",
  "password": "password123"
}

