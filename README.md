# E-commerce Order Processing Automation

An automated e-commerce order processing system built with n8n.

The project demonstrates how an order submitted through a frontend can be received through a webhook, validated, checked against product and inventory data, processed using an AI Agent, stored in Google Sheets, and followed by an automated customer confirmation email.

## Workflow

Frontend Order Form
        ↓
n8n Webhook
        ↓
Validate Order
        ↓
Products / Inventory Check
        ↓
AI Agent
        ↓
Process Order
        ↓
Google Sheets
        ↓
Gmail
        ↓
Webhook Response

## Features

- Frontend order submission
- Webhook-based order intake
- Order validation
- Product and inventory lookup
- AI-based order processing
- Automatic total calculation
- Order storage in Google Sheets
- Automated customer confirmation email
- Webhook response to the frontend

## Technologies

- n8n
- Google Gemini
- Google Sheets
- Gmail
- Webhooks
- HTML
- CSS
- JavaScript

## Order Data

The system works with:

- Order ID
- Customer Name
- Email
- Product
- Quantity
- Price
- Total Amount
- Shipping Address
- Payment Method
- Payment Status
- Order Status
- Order Date

## Product Data

Product information is stored separately and includes:

- Product ID
- Product Name
- Price
- Stock

## How It Works

### 1. Order Submission

The customer submits an order through the frontend.

### 2. Webhook

The frontend sends the order data to the n8n production webhook.

### 3. Validation

The workflow validates the required customer and order information.

### 4. Product Check

The workflow retrieves the selected product and its current price and stock from Google Sheets.

### 5. AI Processing

Google Gemini processes the order information and product data and determines how the order should be handled.

### 6. Order Storage

The processed order is stored in the Ecommerce Orders Google Sheet.

### 7. Customer Notification

Gmail automatically sends an order confirmation to the customer.

### 8. Response

The workflow returns the order processing result to the frontend.

## Project Structure

```text
ecommerce-order-processing-automation/
│
├── workflow.json
├── ecommerce_order_frontend.html
└── README.md
