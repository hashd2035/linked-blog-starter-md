```toc
```
## Redirect to 3rd party payment processor

Here's how a merchant server redirects a user checkout to a 3rd party payment processor and receives notification upon successful payment:

**Components:**

1. **User's Browser (Client):** Initiates the checkout process.
2. **Merchant Server:** Manages shopping cart and redirects to payment processor.
3. **Payment Gateway:** Securely facilitates communication between merchant and processor.
4. **Payment Processor:** Handles payment authorization, settlement, and notification.
5. **User's Bank:** Authorizes or declines the payment based on available funds.

![[Payment Processing 2024-03-23 18.09.09.excalidraw]]

**Handshake:**

1. **User Checkout:**
    
    - User completes checkout on the merchant's website.
    - Merchant server sends a POST request to the payment gateway containing the order details and payment information.
2. **Payment Gateway:**
    
    - Receives the request from the merchant server.
    - Encrypts the payment information for secure transmission.
    - Forwards the request to the payment processor.
3. **Payment Processor:**
    
    - Decrypts the payment information received from the gateway.
    - Connects to the user's bank for authorization.
        - Sends an authorization request containing payment details.
4. **User's Bank:**
    
    - Receives the authorization request from the processor.
    - Verifies the user's account information and available funds.
    - Sends an authorization response (approved or declined) to the processor.
5. **Payment Processor:**
    
    - Receives the authorization response from the user's bank.
    - If approved:
        - Captures the payment (deducts funds from the user's account).
        - Sends a payment confirmation notification to the payment gateway.
    - If declined:
        - Sends a payment failure notification to the payment gateway.
6. **Payment Gateway:**
    
    - Receives the notification from the processor (confirmation or failure).
    - Forwards the notification to the merchant server.
7. **Merchant Server:**
    
    - Receives the notification from the payment gateway.
    - If successful payment:
        - Updates the order status to "paid" in its database.
        - Displays a success message to the user, confirming the purchase.
        - May send an order confirmation email to the user.
    - If payment failed:
        - Informs the user about the payment failure.
        - May allow the user to retry payment or choose another payment method.

**Additional Considerations:**

- **Security:** All communication should be encrypted using HTTPS and secure protocols (e.g., PCI DSS compliance).
- **Real-time vs. Asynchronous:** Notifications might be real-time or asynchronous depending on the integration method.
- **Fraud Detection:** Payment processors can implement fraud detection measures to prevent fraudulent transactions.

This is a general design, and specific implementations may vary depending on the payment processor and merchant's needs.


## Merchant Redirect to Payment Processor Website

In some cases, the merchant server might choose to redirect the user directly to the payment processor's website for checkout instead of handling the payment flow itself. This approach can offer several advantages:

- **Security:** The user enters their payment information directly on the payment processor's secure website, reducing the risk of data breaches on the merchant's server.
- **Compliance:** Payment processors handle PCI compliance, which can be a complex and costly burden for merchants.
- **Flexibility:** Payment processors often offer a wider range of payment options than the merchant might be able to integrate directly.

Here's how the process works with a redirect:

1. **User Checkout:**
    
    - User completes checkout on the merchant's website.
    - Merchant server sends a redirect response to the user's browser.
    - The redirect response includes the URL of the payment processor's checkout page.
2. **User Redirect:**
    
    - User's browser receives the redirect response.
    - User's browser automatically sends a GET request to the payment processor's checkout URL.
3. **Payment Processor Checkout:**
    
    - User arrives at the payment processor's secure checkout page.
    - The user enters their payment information directly into the processor's website.
    - The processor communicates with the user's bank for authorization (similar to the previous design).
4. **Payment Notification:**
    
    - After payment authorization, the processor redirects the user back to the merchant's website.
        - The redirect URL may include a success or failure code indicating the payment outcome.
    - Alternatively, the processor might directly notify the merchant server of the payment status using a secure API call.
5. **Merchant Update:**
    
    - The merchant server receives the notification (either from the redirect or API).
    - Based on the notification, the merchant updates the order status and informs the user about the purchase success or failure.

**Advantages and Considerations:**

- **Security:** While this approach offers stronger security, the user experience might be slightly disrupted by the redirect.
- **Customization:** The merchant might have less control over the checkout page's look and feel compared to handling it on their server.
- **Integration Complexity:** Integrating with the payment processor's API for notification might be more complex than handling redirects.

This approach is often used for one-time payments or when the merchant prioritizes security and compliance.