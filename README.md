# TonoEasy Marketplace

> A multi-vendor e-commerce, logistics, delivery, and operations platform connecting customers, stores, riders, marketers, and administrators through a unified marketplace ecosystem.

---

## Overview

**TonoEasy Marketplace** is a full-stack multi-vendor commerce platform designed to manage the complete journey from product discovery and ordering to store fulfilment, rider delivery, payment, tracking, and administrative oversight.

Rather than operating as a single website, TonoEasy is built as an ecosystem of interconnected portals, with each portal designed for a specific user group.

The platform includes:

- Customer marketplace
- Store management portal
- Rider delivery portal
- Marketers portal
- Administrative portal
- Payment processing
- Delivery management
- Live location tracking
- Promotions and advertising
- Customer reviews
- Notifications
- Role-based access control

---

# Platform Architecture

```text
                        ┌─────────────────────────┐
                        │       TONOEASY          │
                        │      MARKETPLACE        │
                        └────────────┬────────────┘
                                     │
              ┌──────────────────────┼──────────────────────┐
              │                      │                      │
              ▼                      ▼                      ▼
      Customer Marketplace      Store Portal        Marketers Portal
              │                      │
              │                      │
              └────────────┬─────────┘
                           │
                           ▼
                    Admin / Operations
                           │
                           ▼
                      Rider Portal
                           │
                           ▼
                        Delivery
```

---

# Portals

## Customer / Main Platform

The customer-facing marketplace allows users to discover products and stores, place orders, make payments, and track their purchases.

**Live Platform**

https://main.envirofitlpg.org

### Main Features

- Customer registration and authentication
- Product browsing
- Product search
- Category filtering
- Store filtering
- Nearby store discovery
- Product details
- Multiple product images
- Product reviews
- Shopping cart
- Quantity management
- Checkout
- Delivery selection
- Promotional codes
- Online payments
- Pay-on-delivery support
- Order history
- Order cancellation rules
- Delivery tracking
- Customer notifications
- Referral functionality

---

## Store Portal

The store portal provides registered vendors with tools to manage their operations within the marketplace.

**Portal**

https://stores.envirofitlpg.org

### Store Features

- Store authentication
- Store dashboard
- Store profile management
- Branch management
- Product management
- Product image management
- Category and brand management
- Pricing
- Inventory management
- Incoming order management
- Order preparation
- Mark orders as ready for delivery
- Promotions
- Discount management
- Customer review management
- Store notifications
- Role-based access

### Supported Store Roles

- Store Owner
- Branch Manager
- Staff

---

## Rider Portal

The rider application handles delivery operations and order fulfilment.

**Portal**

https://riders.envirofitlpg.org

### Rider Features

- Rider authentication
- Online/offline availability
- Delivery job notifications
- Accept or decline delivery jobs
- Pickup information
- Customer delivery details
- Map navigation
- Live location updates
- Delivery status management
- Multiple pickup support
- Customer drop-off management
- Delivery completion
- Rider notifications

### Delivery Workflow

```text
Assigned
   ↓
Accepted
   ↓
Pickup
   ↓
Picked Up
   ↓
In Transit
   ↓
Delivered
```

---

## Marketers Portal

The marketers portal provides dedicated functionality for marketers operating within the TonoEasy ecosystem.

**Portal**

https://marketers.envirofitlpg.org

The portal is designed to separate marketing operations from customer, store, rider, and administrative activities.

---

## Admin Portal

The administration portal provides centralized control over the entire marketplace.

**Portal**

https://admin.envirofitlpg.org

> Administrative access is restricted to authorized users.

### Administrative Features

- Dashboard
- Customer management
- Store management
- Store verification
- Rider management
- Order management
- Delivery management
- Rider assignment
- Marketplace monitoring
- Product monitoring
- Promotions management
- Advertisement management
- Review management
- Notifications
- Operational reporting
- Role-based permissions

---

# Order Workflow

The marketplace follows a structured order and delivery process.

```text
Customer Places Order
        ↓
      Pending
        ↓
Store Receives Order
        ↓
     Prepared
        ↓
Ready for Delivery
        ↓
 Rider Assigned
        ↓
    Picked Up
        ↓
   On the Way
        ↓
    Delivered
```

This workflow separates store fulfilment from rider delivery responsibilities.

---

# Multi-Store Ordering

TonoEasy supports orders involving products from multiple stores.

The platform manages:

- Store-specific order items
- Store preparation status
- Multiple pickup points
- Rider assignments
- Combined customer delivery
- Store-level amounts
- Delivery charges
- Overall order progress

This allows customers to purchase products from different vendors while the platform coordinates fulfilment and delivery.

---

# Location & Delivery Tracking

TonoEasy integrates location-based functionality to support both customers and delivery riders.

### Location Features

- Store coordinates
- Rider location
- Customer delivery location
- Nearby store discovery
- Distance calculations
- Rider tracking
- Last-known rider location
- Map-based navigation

Tracking becomes available during the delivery phase after the rider collects the order.

---

# Delivery Pricing

The platform supports configurable delivery calculations based on factors including:

- Base delivery fee
- Travel distance
- Product classification
- Heavy-item surcharge
- Oversized products

Example delivery logic:

```text
Delivery Fee =
Base Fee
+ Distance Charge
+ Additional Item Charges
```

Different delivery classes can be supported, including:

- Standard
- Heavy
- Oversized

---

# Payment System

TonoEasy supports multiple payment methods.

### Supported Payment Options

- Pay on Delivery
- Mobile Money
- Online Payment
- Paystack Integration

The checkout process can also apply:

- Promotional discounts
- Coupon codes
- Delivery fees
- Order-level calculations

---

# Promotions

Stores can create promotions for customers.

Promotional features include:

- Discount codes
- Percentage discounts
- Minimum order requirements
- Promotional campaigns

---

# Advertising System

The marketplace supports different advertising placements.

Available advertisement types include:

- Featured Products
- Homepage Banners
- Category Promotions
- Popup Advertisements

This allows stores and administrators to promote selected products or campaigns.

---

# Customer Reviews

Customers can submit reviews for products they have purchased.

Reviews can be linked directly to order items to improve review authenticity.

Administrators can control whether submitted reviews are approved for public display.

---

# Notifications

TonoEasy includes notification functionality across different portals.

Notifications may be generated for events such as:

- New orders
- Order status changes
- Store preparation
- Rider assignment
- Delivery updates
- Promotions
- Account-related activities

Audio notifications can also be used for time-sensitive activities such as new delivery jobs.

---

# Progressive Web App

Selected TonoEasy portals support Progressive Web App functionality.

Features include:

- Installable application experience
- Web app manifests
- Service workers
- Mobile optimization
- Offline support
- Application icons
- Notification support

This allows users to access parts of the platform with an app-like experience without requiring a traditional mobile application installation.

---

# Role-Based Access Control

Different users have access to different functions based on their assigned roles.

Example roles include:

```text
Administrator
Store Owner
Branch Manager
Store Staff
Rider
Marketer
Customer
```

Role restrictions help protect sensitive functionality and ensure that each user sees only the tools relevant to their responsibilities.

---

# Technologies

## Backend

- PHP
- MySQL
- MySQLi
- REST APIs
- Session Authentication

## Frontend

- HTML5
- CSS3
- JavaScript
- jQuery
- AJAX
- Bootstrap

## Data & Reporting

- MySQL
- DataTables
- CSV Processing
- Reporting Dashboards

## Integrations

- Paystack
- Google Maps
- Geolocation APIs
- External REST APIs

## Application Technology

- Progressive Web Apps
- Service Workers
- Web App Manifest
- Responsive Web Design

---

# Database Architecture

The application uses a relational MySQL database.

Major data areas include:

```text
Users
Customers
Addresses
Stores
Store Branches
Store Users
Products
Product Images
Categories
Brands
Orders
Order Items
Riders
Deliveries
Payments
Promotions
Advertisements
Reviews
Notifications
Referrals
```

Relationships between these records allow the different TonoEasy portals to operate as one connected marketplace.

---

# Responsive Design

TonoEasy is designed to support:

- Desktop
- Laptop
- Tablet
- Mobile

Bootstrap and responsive layouts are used to provide a consistent experience across different screen sizes.

---

# Security Considerations

The platform includes security measures such as:

- Session-based authentication
- Role-based authorization
- Restricted administrative functionality
- User access validation
- Server-side form validation
- Database query validation
- Protected payment credentials

Sensitive information should never be committed to this repository.

Files containing the following should remain private:

```text
Database passwords
API secret keys
Paystack secret keys
Production credentials
Customer personal information
Private configuration files
.env files
Database backups containing real customer data
```

Example environment/configuration values should be used instead.

---

# Project Structure

A simplified representation of the ecosystem:

```text
tonoeasy/
│
├── customer/
│   ├── marketplace
│   ├── products
│   ├── cart
│   ├── checkout
│   └── tracking
│
├── stores/
│   ├── dashboard
│   ├── products
│   ├── orders
│   └── promotions
│
├── riders/
│   ├── dashboard
│   ├── jobs
│   ├── tracking
│   └── deliveries
│
├── marketers/
│   └── marketing-tools
│
├── admin/
│   ├── dashboard
│   ├── users
│   ├── stores
│   ├── riders
│   ├── orders
│   └── reporting
│
└── shared/
    ├── assets
    ├── uploads
    ├── APIs
    └── configuration
```

---

# Demo

### Customer Platform

https://main.envirofitlpg.org

### Store Portal

https://stores.envirofitlpg.org

### Rider Portal

https://riders.envirofitlpg.org

### Marketers Portal

https://marketers.envirofitlpg.org

### Administration Portal

Administrative functionality is restricted.

A demonstration can be provided upon request.

---

# My Role

I worked on TonoEasy as the **Full-Stack Developer**, contributing to areas including:

- Platform architecture
- Database design
- Backend development
- Frontend development
- Authentication
- Role-based permissions
- Customer marketplace
- Store management
- Rider operations
- Administrative functionality
- AJAX functionality
- Payment integration
- Mapping and geolocation
- Order workflows
- Delivery workflows
- Notifications
- PWA configuration
- Responsive design
- Deployment
- Debugging
- Ongoing platform improvements

---

# Skills Demonstrated

TonoEasy demonstrates practical experience in:

- Full-stack web development
- Marketplace architecture
- E-commerce development
- PHP application development
- Relational database design
- Logistics systems
- Order management
- Delivery management
- Multi-role systems
- Payment gateway integration
- API integration
- Maps and geolocation
- Responsive application development
- Progressive Web Apps
- Business workflow automation
- Debugging and system maintenance

---

# Project Status

**Active Development**

TonoEasy continues to evolve as additional marketplace, operations, payment, logistics, and administrative functionality is introduced.

---

# Repository Notice

This repository may contain a portfolio/demo representation of the TonoEasy platform rather than the complete production source code.

Production credentials, customer information, private business logic, API secrets, and other sensitive configuration are intentionally excluded.

---

# Developer

**Benjamin Justice Arthur Tandoh**

Full-Stack Web Developer

**Opera Media Solutions**

---

## Contact

For collaboration, project enquiries, or a demonstration of the full TonoEasy platform, please contact the developer.

---

If you are viewing this project as part of my development portfolio, feel free to explore the available screenshots, documentation, and public platform links.
