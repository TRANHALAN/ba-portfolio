# Software Requirement Specification (SRS)

## 1. Project Information

### Project Name

Online Shopping Platform

### Business Goal

Provide customers with an online platform to browse products, place orders, make payments, and track deliveries.

---

# 2. Scope

The system shall allow:

* Customer registration and login
* Product browsing and searching
* Shopping cart management
* Checkout and payment
* Order tracking
* Admin product management

---

# 3. User Roles

## Customer

Can:

* Register account
* Login
* Browse products
* Add products to cart
* Place order
* Make payment
* Track order

## Admin

Can:

* Manage products
* Manage inventory
* View orders
* Update order status

---

# 4. Functional Requirements

## FR-01 Customer Registration

### Description

The system shall allow customers to create an account.

### Input

* Full Name
* Email
* Password

### Processing

* Validate email format
* Check duplicate email
* Encrypt password
* Save customer record

### Output

* Registration success message

### Business Rules

* Email must be unique.
* Password minimum 8 characters.

---

## FR-02 Customer Login

### Description

The system shall allow customers to login using email and password.

### Input

* Email
* Password

### Processing

* Validate credentials
* Generate authentication token

### Output

* Login success

### Business Rules

* Account locked after 5 failed attempts.

---

## FR-03 Product Search

### Description

Customers can search products.

### Input

* Keyword
* Category

### Processing

* Search product catalog

### Output

* Product list

### Business Rules

* Only active products are displayed.

---

## FR-04 Shopping Cart

### Description

Customers can manage products in cart.

### Actions

* Add item
* Remove item
* Update quantity

### Business Rules

* Quantity cannot exceed available stock.

---

## FR-05 Checkout

### Description

Customers can place orders.

### Input

* Delivery Address
* Payment Method

### Processing

* Validate cart
* Calculate total amount
* Create order

### Output

* Order Number

### Business Rules

* Order cannot be created if cart is empty.

---

## FR-06 Payment

### Description

Customers can pay for orders.

### Payment Methods

* Credit Card
* Bank Transfer
* E-wallet

### Processing

* Send payment request to payment gateway
* Receive payment result

### Output

* Payment Status

### Business Rules

* Payment timeout after 15 minutes.

---

## FR-07 Order Tracking

### Description

Customers can view order status.

### Status

* Pending
* Paid
* Processing
* Shipping
* Delivered
* Cancelled

---

## FR-08 Product Management

### Description

Admin can manage products.

### Actions

* Create Product
* Update Product
* Delete Product
* Activate Product
* Deactivate Product

---

## FR-09 Inventory Management

### Description

Admin can manage stock quantity.

### Actions

* Increase Stock
* Decrease Stock
* Stock Adjustment

### Business Rules

* Stock cannot be negative.

---

# 5. Non-Functional Requirements

## NFR-01 Performance

The system shall return search results within 3 seconds.

## NFR-02 Security

Passwords shall be encrypted.

## NFR-03 Availability

System availability shall be 99.9%.

## NFR-04 Audit Trail

All critical transactions shall be logged.

---

# 6. External Integrations

## Payment Gateway

Purpose:
Process customer payments.

Request:

* Order ID
* Amount
* Payment Method

Response:

* Transaction ID
* Payment Status

---

# 7. Assumptions

* Internet connection is available.
* Payment gateway service is operational.
