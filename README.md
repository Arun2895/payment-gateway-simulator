# PaySim - Payment Gateway Simulator
Built a front-end payment gateway simulation with secure transaction flow, multiple payment options, transaction history, and a basic fraud detection system using vanilla HTML, CSS, and JavaScript. Implemented localStorage for persistent user transaction data.

# 🚀 Features
Multiple Payment Methods: Switch between Credit/Debit Card, PayPal, and Bank Account payments.
Dynamic Form Validation: Real-time formatting for card numbers and expiry dates.
Transaction Simulation: Simulates successful, declined, and insufficient funds scenarios using test card numbers.
Fraud Detection: A basic rules-based engine checks for potential fraud indicators like high/low transaction amounts, use of test cards, and temporary email domains.
Tokenization Simulation: Demonstrates the concept of tokenizing sensitive payment information.
Persistent History: All transactions are saved to the browser's localStorage.
Tabbed Transaction View: Filter transaction history by 'All', 'Successful', 'Failed', and 'Fraud Flags'.
Responsive Design: A clean, modern UI that works well on both desktop and mobile devices.

# 🛠️ How It Works
Payment Processing
The simulator mimics an API call with a 2-second delay to create a realistic processing feel. It uses predefined test card numbers to trigger specific outcomes:

Success: 4242 4242 4242 4242
Decline: 4000 0000 0000 0002
Insufficient Funds: 4000 0000 0000 9995 Other card numbers and payment methods have a randomized success/failure rate.
Fraud Detection
The checkForFraud() function in script.js applies a set of simple rules to the transaction data. If any rule is triggered, the transaction is flagged. For example:

Is the transaction amount unusually high (e.g., > ₹100,000)?
Is a known temporary email service being used?
Is a test card number being used?
Data Persistence
All transaction records are stored as a JSON array in the browser's localStorage under the key paymentTransactions. This allows your history to remain even after you close the browser tab.

# 💻 Tech Stack
HTML5
CSS3 (with CSS Variables for easy theming)
Vanilla JavaScript (ES6+)
No external frameworks or libraries are used, except for Font Awesome for icons.
