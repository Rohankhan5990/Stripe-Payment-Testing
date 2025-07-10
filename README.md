# Stripe Payment Testing

This project is a simple Node.js Express server that demonstrates how to create a payment intent using the Stripe API. It is intended for testing and learning purposes.

## Features
- Create payment intents with Stripe
- CORS enabled for cross-origin requests
- Uses environment variables for sensitive keys

## Prerequisites
- Node.js (v14 or higher recommended)
- A Stripe account (for API keys)

## Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/your-username/stripe-payment-test.git
cd stripe-payment-test/Stripe-Payment-Testing
```

### 2. Install dependencies
```bash
npm install
```

### 3. Set up environment variables
Create a `.env` file in the root directory and add your Stripe Secret Key:
```
SK_TEST=your_stripe_secret_key
PORT=3000 # Optional, defaults to 3000
```

### 4. Start the server
```bash
node index.js
```

The server will run on `http://localhost:3000` by default.

## API Endpoint

### POST `/create-payment-intent`
Create a new payment intent.

**Request Body:**
```json
{
  "amount": 1000
}
```
- `amount` is in the smallest currency unit (e.g., cents for USD).

**Response:**
```json
{
  "clientSecret": "..."
}
```

## License
This project is licensed under the MIT License.

