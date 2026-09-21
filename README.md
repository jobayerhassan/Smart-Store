# Smart-Store
OOP lab project: a smart super-shop application built with Java
🛒 SmartStore AI
An Intelligent SuperShop Management System with AI Meal-Planner & Dynamic Pricing Engine

Find your daily groceries, plan family meals within budget, and shop smarter with automated discounts and inventory management.

📖 About the Project
SmartStore AI is a desktop application designed to modernize the traditional retail experience. Inspired by commercial super-shop platforms like Shwapno and Chaldal, this system bridges the gap between household meal planning and store inventory management.

Instead of searching for individual items, SmartStore AI allows users to bundle full recipe ingredients with a single click, optimizes monthly family budgets, automatically discounts near-expiry products to prevent food waste, and locks cart items in real time during checkout.

Developed as an Object-Oriented Programming (OOP) Lab Course Project at Daffodil International University (DIU).

🎯 Project Objectives
Modular Architecture: Build a desktop super-shop application using core object-oriented programming principles for a clean and modular architecture.

AI Meal Bundler: Implement a rule-based meal planner that automatically bundles required recipe ingredients into the shopping cart.

Family Budget Planner: Create an automated budget planner that generates optimized monthly grocery lists based on user constraints.

Smart Substitution: Provide intelligent product substitution suggestions whenever a requested inventory item is out of stock.

Dynamic Pricing: Apply dynamic discounts on near-expiry perishable goods to reduce store inventory wastage and improve sales.

Concurrency Control: Manage real-time temporary cart stock locking during checkout to prevent inventory double-booking conflicts.

🌟 Key Features
🍲 Rule-Based AI Meal Planner — Converts dish queries (e.g., Chicken Roast, Biryani) into single-click ingredient bundles mapped directly to active inventory.

📊 Family Monthly Budget Planner — Calculates daily dietary requirements and generates a balanced grocery list based on family size and budget limits.

⚠️ Smart Out-of-Stock Substitution — Automatically evaluates product categories, brand equivalents, and price tiers to suggest top 3 alternatives when an item is unavailable.

⏳ Dynamic Shelf-Life Pricing — Calculates tier-based discounts on perishable goods as expiry dates approach to reduce food waste.

🔒 Multi-Threaded Cart Reservation — Uses background threads to temporarily lock cart items for 3 minutes during checkout, avoiding race conditions.

👤 Role-Based Authentication — Separate panels for Customers and Store Managers/Admins for secure access.

🛠️ Tech Stack
Layer	Technology Used
Language	Java (JDK 17 or later)
User Interface	JavaFX / Java Swing
Data Persistence	File I/O (JSON / Text Storage)
Architecture	Model-View-Controller (MVC) & Design Patterns
Version Control	Git & GitHub
🏗️ OOP Pillars Implemented
Encapsulation: Sensitive properties (e.g., user passwords, inventory stock) are kept private and controlled via getter/setter validations.

Inheritance: Base class Product extended into PerishableProduct and NonPerishableProduct.

Polymorphism: Runtime price calculations overridden in subclasses using calculateFinalPrice().

Abstraction: File management and threading operations decoupled through dedicated interfaces (DataRepository, PaymentStrategy).

👥 Team Members
Section: 69_I1 | Institution: Daffodil International University (DIU)

Role	Student ID	Name	GitHub Profile
Team Lead	252-15-XXX	Jobayer Hassan	@your-username
Member 2	252-15-XXX	Member Name	@username
Member 3	252-15-XXX	Member Name	@username
Member 4	252-15-XXX	Member Name	@username
📜 License
This project is created strictly for academic evaluation in the Object-Oriented Programming Lab course at Daffodil International University (DIU).

Made with ❤️ by the SmartStore AI Team
