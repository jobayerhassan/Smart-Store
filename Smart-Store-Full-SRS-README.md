# 🛒 Smart Store

## Full Software Requirements Specification (SRS) & Project Documentation

```{=html}
<p align="center">
```
`<img src="./banner.svg" width="850">`{=html}
```{=html}
</p>
```

------------------------------------------------------------------------

# Table of Contents

1.  Project Overview
2.  Problem Statement
3.  Objectives
4.  Scope
5.  Functional Requirements
6.  Non Functional Requirements
7.  System Modules
8.  Feature Implementation Details
9.  Workflow Design
10. Architecture
11. UML Design Overview
12. Class Design
13. Database Design
14. Algorithms
15. OOP Implementation
16. Design Patterns
17. Exception Handling
18. Testing Strategy
19. Team Distribution
20. Project Structure
21. Development Roadmap
22. Future Improvements

------------------------------------------------------------------------

# 1. Project Overview

Smart Store is a Java based intelligent grocery retail management system
developed as a university Object-Oriented Programming project.

The system is inspired by modern superstore applications but is an
independent academic implementation.

Smart Store combines traditional shopping operations with intelligent
features:

-   Smart shopping assistant
-   Recipe based grocery planning
-   Family budget management
-   Smart pantry
-   Inventory intelligence
-   Product substitution
-   Expiry based pricing
-   Stock reservation
-   Eco-friendly shopping

The goal is to demonstrate practical Java OOP concepts through a
realistic retail system.

------------------------------------------------------------------------

# 2. Problem Statement

Traditional grocery systems mainly provide product browsing and
purchasing.

Common problems:

-   Customers cannot efficiently plan groceries.
-   Budget management is difficult.
-   Recipe ingredients are forgotten.
-   Products become unavailable.
-   Expired products create waste.
-   Inventory management becomes complex.

Smart Store provides intelligent solutions for customers and store
administrators.

------------------------------------------------------------------------

# 3. Objectives

  Objective                Solution
  ------------------------ -----------------------
  Smart grocery planning   Recipe Planner
  Budget control           Family Budget Planner
  Reduce waste             Expiry Pricing
  Better recommendation    Substitute Engine
  Inventory control        Batch Inventory
  Prevent overselling      Reservation System
  Sustainability           Eco Container

------------------------------------------------------------------------

# 4. Functional Requirements

## FR-01 User Authentication

The system shall allow users to register and login.

Classes:

    User
    Customer
    Admin
    AuthService

------------------------------------------------------------------------

## FR-02 Product Management

Admin can:

-   Add products
-   Update products
-   Remove products
-   Manage categories

Classes:

    Product
    Category
    ProductService

------------------------------------------------------------------------

## FR-03 Smart Assistant

The system shall provide shopping assistance.

Input:

    Chicken roast for 5 people

Output:

    Ingredient list
    Required quantity
    Estimated cost

Classes:

    ChatAssistant
    ChatIntent
    RecipeIntent

------------------------------------------------------------------------

# 5. Non Functional Requirements

## Performance

The system should respond quickly during normal operations.

## Maintainability

The code should follow modular architecture.

## Security

User data should be protected.

## Reliability

Database operations should maintain consistency.

------------------------------------------------------------------------

# 6. System Modules

## Module 1: Authentication

Responsible for:

-   User registration
-   Login
-   Role management

------------------------------------------------------------------------

## Module 2: Smart Assistant

Responsible for:

-   Recipe processing
-   User query handling
-   Recommendation

------------------------------------------------------------------------

## Module 3: Planning System

Responsible for:

-   Budget planning
-   Pantry management

------------------------------------------------------------------------

## Module 4: Inventory System

Responsible for:

-   Products
-   Stock
-   Expiry
-   Pricing

------------------------------------------------------------------------

## Module 5: Transaction System

Responsible for:

-   Cart
-   Order
-   Payment

------------------------------------------------------------------------

# 7. Feature Implementation Details

# Smart Recipe Planner

## Purpose

Convert recipes into shopping requirements.

## Workflow

    Recipe Input

    ↓

    Ingredient Calculation

    ↓

    Inventory Check

    ↓

    Missing Items

    ↓

    Cart

## Classes

    Recipe
    RecipeIngredient
    RecipeService
    ShoppingList

## Database

Tables:

    recipes
    recipe_items
    products

------------------------------------------------------------------------

# Smart Pantry

## Purpose

Track customer's available household items.

Example:

    Required Rice: 2kg

    Available:
    Rice 5kg

    Purchase:
    0kg

Classes:

    Pantry
    PantryItem
    PantryService

------------------------------------------------------------------------

# Family Budget Planner

Purpose:

Create optimized grocery plans.

Inputs:

-   Family size
-   Budget
-   Priority items

Classes:

    FamilyProfile
    BudgetPlanner
    BudgetPlan
    Optimizer

------------------------------------------------------------------------

# Inventory Management

Features:

-   Product stock
-   Batch tracking
-   Expiry tracking

Classes:

    Product
    InventoryBatch
    InventoryService

------------------------------------------------------------------------

# FEFO Algorithm

First Expired First Out.

Logic:

    Sort inventory batches by expiry date

    Select earliest expiry batch

    Reduce quantity

    Continue until requirement completed

------------------------------------------------------------------------

# Smart Substitution Engine

Purpose:

Recommend alternatives.

Factors:

-   Category
-   Brand
-   Price
-   Size
-   Availability

Classes:

    SubstitutionStrategy
    SubstitutionService

------------------------------------------------------------------------

# Dynamic Pricing

Purpose:

Generate expiry based discounts.

Example:

    Normal:
    100%

    Near Expiry:
    Discount

    Expired:
    Unavailable

Classes:

    PricingRule
    ExpiryPricingRule
    PricingService

------------------------------------------------------------------------

# Cart and Order

Workflow:

    Cart

    ↓

    Reservation

    ↓

    Payment

    ↓

    Order

    ↓

    Receipt

Classes:

    Cart
    Order
    Payment
    Receipt

------------------------------------------------------------------------

# Stock Reservation

Purpose:

Prevent selling unavailable stock.

Classes:

    Reservation
    ReservationService

------------------------------------------------------------------------

# Eco Container System

Uses state management.

States:

    Available
    Issued
    Returned
    Refunded

------------------------------------------------------------------------

# Smart Rescue Basket

Creates discounted bundles from near expiry products.

Example:

    Milk
    Bread
    Egg

    =

    Breakfast Rescue Pack

------------------------------------------------------------------------

# 8. System Workflow

Customer:

    Register

    ↓

    Login

    ↓

    Dashboard

    ↓

    Smart Assistant / Shopping

    ↓

    Cart

    ↓

    Reservation

    ↓

    Payment

    ↓

    Order

    ↓

    Receipt

Admin:

    Admin Login

    ↓

    Dashboard

    ↓

    Product Management

    ↓

    Inventory Control

    ↓

    Reports

------------------------------------------------------------------------

# 9. Architecture

    Presentation Layer

            |

    Controller Layer

            |

    Service Layer

            |

    Repository Layer

            |

    Database Layer

------------------------------------------------------------------------

# 10. Database Design

Technology:

    SQLite + JDBC

Tables:

  Table               Purpose
  ------------------- -------------------
  users               User data
  products            Product data
  categories          Categories
  inventory_batches   Stock and expiry
  recipes             Recipe data
  pantry_items        Customer pantry
  carts               Shopping cart
  orders              Orders
  payments            Payments
  reservations        Stock reservation
  wallets             Wallet data

------------------------------------------------------------------------

# 11. OOP Implementation

## Encapsulation

Used in:

-   Product
-   User
-   Order

Private fields with getters and setters.

------------------------------------------------------------------------

## Inheritance

Example:

    User

    |

    Customer
    Admin

------------------------------------------------------------------------

## Polymorphism

Used in:

-   Payment
-   Pricing
-   Substitution

------------------------------------------------------------------------

## Abstraction

Interfaces:

    Payment
    PricingRule
    ChatIntent
    Repository

------------------------------------------------------------------------

# 12. Design Patterns

## Strategy Pattern

Used for:

-   Payment methods
-   Pricing rules
-   Substitution

## State Pattern

Used for:

-   Container lifecycle

## Repository Pattern

Used for:

-   Database access

------------------------------------------------------------------------

# 13. Exception Handling

Custom exceptions:

    UserNotFoundException

    ProductNotFoundException

    InsufficientStockException

    PaymentFailedException

------------------------------------------------------------------------

# 14. Testing Strategy

Testing:

-   Authentication
-   Recipe calculation
-   Budget optimization
-   Inventory
-   Pricing
-   Reservation
-   Payment
-   Order

------------------------------------------------------------------------

# 15. Team Distribution

  Member     Responsibility
  ---------- ----------------------------------
  Member 1   Authentication + Smart Assistant
  Member 2   Budget + Pantry
  Member 3   Inventory + Pricing
  Member 4   Cart + Order + Payment
  Member 5   Eco System + Dashboard

------------------------------------------------------------------------

# 16. Project Structure

    Smart-Store

    src

    ├── model
    ├── service
    ├── repository
    ├── database
    ├── assistant
    ├── inventory
    ├── planner
    ├── cart
    ├── order
    ├── payment
    ├── eco
    └── ui

------------------------------------------------------------------------

# 17. Development Roadmap

Phase 1:

-   Models
-   Database
-   Authentication

Phase 2:

-   Product
-   Inventory
-   Recipe
-   Budget

Phase 3:

-   Pricing
-   Reservation
-   Eco System

Phase 4:

-   Testing
-   UI
-   Documentation

------------------------------------------------------------------------

# 18. Future Improvements

-   Mobile application
-   AI chatbot
-   Online delivery
-   Supplier management
-   Analytics dashboard

------------------------------------------------------------------------

# Smart Store

Built with Java ❤️
