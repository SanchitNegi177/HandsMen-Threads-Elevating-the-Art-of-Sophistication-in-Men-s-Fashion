# HandsMen Threads -  Elevating the Art of Sophistication in Men's Fashion

A dynamic Salesforce application for managing customers, products, inventory, orders, and marketing campaigns in the fashion industry, tailored to improve operational efficiency and enhance customer engagement.

## 📋 Overview

HandsMen Threads leverages Salesforce to streamline operations across customer management, order processing, inventory tracking, and loyalty programs. This system ensures real-time stock visibility, automates business-critical flows, and empowers the team with actionable insights.

## 🧵 Key Features

### Customer & Order Management
- **HandsMen Customer Records**: Centralized customer data with loyalty tracking
- **Order Confirmation Automation**: Ensures timely and accurate communication with customers
- **Bulk Order Processing**: Daily batch job to update order statuses and stock levels

### Inventory Management
- **Stock Deduction on Orders**: Real-time updates to inventory when orders are placed
- **Inventory Object**: Tracks product stock levels and availability
- **Stock Alert System**: Sends automatic notifications when stock is below threshold

### Loyalty Program
- **Dynamic Loyalty Updates**: Automatically adjusts customer loyalty tier based on purchase activity
- **Personalized Engagement**: Enables reward programs and targeted campaigns

### Marketing Campaigns
- **Campaign Object**: Organizes promotional activities and outreach programs
- **Customer Targeting**: Based on loyalty status and order history

## 🏗️ Technical Architecture

### Custom Objects
- `HandsMen_Customer__c` – Customer data and loyalty tracking  
- `HandsMen_Product__c` – Fashion products catalog  
- `HandsMen_Order__c` – Sales order records  
- `Inventory__c` – Stock and product availability  
- `Marketing_Campaign__c` – Campaigns for promotions and customer engagement  

### Apex Triggers

| Trigger Name           | Object               | Purpose                                                  |
|------------------------|----------------------|----------------------------------------------------------|
| Update_Order_Total     | HandsMen_Order__c    | Auto-calculate `Total_Amount__c` when order is saved     |
| Stock_Deduction        | Inventory__c         | Decrease inventory count on new order                    |
| LoyaltyStatusUpdateTrigger  | HandsMen_Order__c | Adjust loyalty tier after purchases                      |

### Flows & Processes

- **Loyalty Status Update Flow**: Auto-updates loyalty level for customers  
- **Order Confirmation Flow**: Sends confirmation email upon order creation  
- **Stock Alert Flow**: Notifies team when product stock drops below 5 units  

### Batch Jobs

- **Inventory Sync Batch Job**
  - **Purpose**: Sync stock levels with external warehouse
  - **Schedule**: Daily at 2:00 AM

## 📊 Key Business Processes

### Order Lifecycle
1. Customer places an order
2. System validates and confirms the order
3. Confirmation email sent automatically
4. Inventory is updated accordingly
5. Loyalty tier is re-evaluated post-purchase

### Inventory Sync & Alerts
- Inventory is synced with warehouse data every day at 2 AM
- Automated stock alert email triggered when inventory < 5

### Loyalty Management
- Loyalty level is dynamically updated based on cumulative order history
- Enables customer segmentation for marketing campaigns

## 📖 Documentation

For detailed documentation, refer to `HandsMen_Threads_Solution_Design.pdf` .

---


