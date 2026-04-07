# 🌾 AgriBlock - Agricultural Supply Chain Traceability System

[![Node.js](https://img.shields.io/badge/Node.js-18+-green.svg)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-19+-blue.svg)](https://reactjs.org/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0+-orange.svg)](https://www.mysql.com/)
[![Rust](https://img.shields.io/badge/Blockchain-Rust-orange.svg)](https://www.rust-lang.org/)
[![License](https://img.shields.io/badge/License-ISC-blue.svg)](LICENSE)


https://youtu.be/YPznCc7jqDc demo video

> **Semester Project for Information Security (IS) Course**  
> _Developed by Hamza - Volunteered to bring this innovative idea to life as part of our professor's lab work_

---

## 📋 Table of Contents

- [🌟 Overview](#-overview)
- [🎯 Why We Built AgriBlock](#-why-we-built-agriblock)
- [✨ Key Features](#-key-features)
- [🏗️ Architecture](#️-architecture)
- [🛠️ Technology Stack](#️-technology-stack)
- [🚀 Installation & Setup](#-installation--setup)
- [📖 Usage Guide](#-usage-guide)
- [🔗 API Endpoints](#-api-endpoints)
- [👥 User Roles & Dashboards](#-user-roles--dashboards)
- [🔐 Security Features](#-security-features)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)
- [👨‍💻 Authors](#-authors)

---

## 🌟 Overview

**AgriBlock** is a comprehensive, blockchain-powered agricultural supply chain traceability system that ensures complete transparency and accountability from farm to fork. Built as a semester project for our Information Security course, this platform revolutionizes how agricultural products are tracked, verified, and delivered to consumers.

### The Agricultural Supply Chain Journey

```
🌱 FARMER → 🌾 DISTRIBUTOR → 🚛 TRANSPORTER → 🏪 SHOPKEEPER → 👥 CONSUMER
     ↓         ↓            ↓            ↓            ↓
   Harvest   Process     Transport    Retail      Purchase
   Events    Events       Events      Events      Trace
```

Each stage in the supply chain is immutably recorded on our custom Rust blockchain, ensuring that consumers can trace every step of their food's journey.

---

## 🎯 Why We Built AgriBlock

### Academic Context

- **Course**: Information Security (IS) - Semester Project
- **Professor's Vision**: Our professor presented this innovative concept as lab work
- **Developer Initiative**: I volunteered to lead the development and bring this idea to life

### Real-World Problem Solving

- **Food Safety Crisis**: Recent food contamination scandals highlight the need for transparency
- **Consumer Trust**: Modern consumers demand to know the origin and journey of their food
- **Farmer Accountability**: Ensures fair compensation and proper credit for agricultural producers
- **Regulatory Compliance**: Helps meet growing food traceability regulations worldwide

### Learning Objectives

- **Blockchain Implementation**: Hands-on experience with distributed ledger technology
- **Security Best Practices**: JWT authentication, role-based access control, data encryption
- **Full-Stack Development**: MERN-like stack with custom blockchain integration
- **IoT Integration**: Incorporating sensor data for real-time monitoring

---

## ✨ Key Features

### 🔗 Complete Traceability

- **Batch Genealogy**: Track products from parent batches through splitting and processing
- **Event Timeline**: Immutable record of every action (harvest, transport, quality checks)
- **QR Code Integration**: Consumer scanning for instant product history
- **IoT Sensor Data**: Real-time temperature, humidity, and location monitoring

### 🛡️ Security & Authentication

- **JWT-Based Authentication**: Secure token-based user sessions
- **Role-Based Access Control (RBAC)**: Granular permissions for different user types
- **Blockchain Immutability**: Cryptographically secured transaction records
- **Data Encryption**: Protected sensitive information throughout the system

### 📊 Multi-Role Dashboard System

- **Farmer Dashboard**: Product creation, batch management, harvest logging
- **Distributor Dashboard**: Bulk processing, quality control, inventory management
- **Transporter Dashboard**: Shipment tracking, delivery confirmations
- **Shopkeeper Dashboard**: Retail sales, customer service
- **Consumer Dashboard**: Product tracing, purchase history
- **Admin Dashboard**: System oversight, user management

### 🛒 E-Commerce Integration

- **Marketplace**: Direct farmer-to-consumer sales platform
- **Order Management**: Complete order lifecycle tracking
- **Payment Integration**: Secure transaction processing
- **Inventory Tracking**: Real-time stock management

### 📎 Media & Documentation

- **Event Attachments**: Photos, certificates, lab reports as proof
- **Quality Documentation**: Lab test results, compliance certificates
- **Digital Proof**: Immutable evidence of product quality and handling

---

## 🏗️ Architecture

### System Components

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   React Frontend│    │  Express Backend │    │   MySQL Database │
│   (Port 5173)   │◄──►│   (Port 5000)    │◄──►│   (Port 3306)    │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                       │                       │
         └───────────────────────┼───────────────────────┘
                                 │
                    ┌─────────────────┐
                    │ Rust Blockchain │
                    │   (Port 8000)   │
                    └─────────────────┘
```

### Data Flow

1. **Frontend**: User interactions, dashboard displays
2. **Backend**: Business logic, API endpoints, authentication
3. **Database**: Persistent storage of users, products, events, orders
4. **Blockchain**: Immutable event logging, transaction validation

### Key Models

- **Users & Roles**: Multi-role user system with granular permissions
- **Products & Batches**: Hierarchical batch tracking with genealogy
- **Events & Attachments**: Timestamped actions with supporting documentation
- **Orders & Shipments**: Complete e-commerce workflow
- **IoT Devices**: Sensor data integration for quality monitoring

---

## 🛠️ Technology Stack

### Backend

- **Runtime**: Node.js 18+
- **Framework**: Express.js
- **Database**: MySQL 8.0+
- **Authentication**: JWT (JSON Web Tokens)
- **Password Hashing**: bcryptjs
- **CORS**: Cross-Origin Resource Sharing

### Frontend

- **Framework**: React 19+
- **Build Tool**: Vite
- **Styling**: Tailwind CSS
- **Routing**: React Router DOM
- **HTTP Client**: Axios
- **Icons**: Lucide React

### Blockchain

- **Language**: Rust
- **Consensus**: Proof-of-Work (SHA-256)
- **Data Storage**: JSON payloads for supply chain events
- **API**: RESTful HTTP endpoints

### Development Tools

- **Process Management**: Nodemon
- **Environment**: dotenv
- **UUID Generation**: uuid package
- **Database Pooling**: mysql2

---

## 🚀 Installation & Setup

### Prerequisites

- **Node.js** 18+ ([Download](https://nodejs.org/))
- **MySQL** 8.0+ ([Download](https://www.mysql.com/))
- **Rust** (for blockchain) ([Install](https://www.rust-lang.org/tools/install))
- **Git** ([Download](https://git-scm.com/))

### Database Setup

1. Install and start MySQL server
2. Create database user with credentials:
   - Username: `root`
   - Password: `sql@123`
   - Database: `agrichain` (auto-created by the app)

### Application Setup

#### 1. Clone the Repository

```bash
git clone <repository-url>
cd AgriBlock
```

#### 2. Backend Setup

```bash
# Install dependencies
npm install

# Seed the database (creates tables and sample data)
npm run seed

# Start the backend server
npm start
```

Backend runs on: `http://localhost:5000`

#### 3. Frontend Setup

```bash
cd client

# Install dependencies
npm install

# Start the development server
npm run dev
```

Frontend runs on: `http://localhost:5173`

#### 4. Blockchain Setup (Optional)

```bash
cd ../AgriBlock_rust_blockchain-main/AgriBlock_rust_blockchain-main

# Configure environment
# Create .env file with PORT=8000, DIFFICULTY=1, etc.

# Run the blockchain node
cargo run
```

Blockchain API runs on: `http://localhost:8000`

### Demo Credentials

All demo accounts use password: `password123`

| Role        | Username           | Notes                                   |
| ----------- | ------------------ | --------------------------------------- |
| Farmer      | `farmer_joe`       | Creates products and batches            |
| Distributor | `distributor_dave` | Processes and distributes ($50k wallet) |
| Transporter | `transporter_tom`  | Handles shipping and logistics          |
| Shopkeeper  | `shop_sarah`       | Retail sales ($20k wallet)              |
| Consumer    | `consumer_carl`    | Can trace product origins               |

---

## 📖 Usage Guide

### For Farmers

1. **Login** with farmer credentials
2. **Create Products**: Define crops, varieties, and details
3. **Generate Batches**: Create harvest batches with quantities
4. **Log Events**: Record planting, harvesting, quality checks
5. **Upload Proof**: Attach photos, certificates, lab reports

### For Distributors

1. **Receive Batches**: Accept farmer deliveries
2. **Process Products**: Split, package, or transform batches
3. **Quality Control**: Perform inspections and tests
4. **Transfer Ownership**: Send to transporters or shopkeepers

### For Consumers

1. **Purchase Products**: Browse marketplace or scan QR codes
2. **Trace Origins**: View complete product journey
3. **Verify Authenticity**: Check blockchain-recorded events
4. **Report Issues**: Flag suspicious or contaminated products

### Admin Functions

- User management and role assignments
- System monitoring and analytics
- Blockchain integration oversight
- Database maintenance and backups

---

## 🔗 API Endpoints

### Authentication

- `POST /api/auth/login` - User authentication
- `POST /api/auth/register` - User registration

### Farmer Operations

- `GET /api/farmer/products` - List farmer's products
- `POST /api/farmer/products` - Create new product
- `POST /api/farmer/batches` - Create harvest batch

### Traceability

- `GET /api/traceability/batch/:batch_code` - Get batch history
- `GET /api/traceability/product/:product_id` - Product genealogy

### Commerce

- `GET /api/commerce/products` - Marketplace products
- `POST /api/commerce/orders` - Place orders
- `GET /api/commerce/orders/:user_id` - User orders

### Events & Blockchain

- `POST /api/events` - Log supply chain events
- `GET /api/events/batch/:batch_id` - Batch event history

---

## 👥 User Roles & Dashboards

### Role Permissions Matrix

| Feature         | Farmer | Distributor | Transporter | Shopkeeper | Consumer | Admin |
| --------------- | ------ | ----------- | ----------- | ---------- | -------- | ----- |
| Create Products | ✅     | ❌          | ❌          | ❌         | ❌       | ✅    |
| Process Batches | ❌     | ✅          | ❌          | ❌         | ❌       | ✅    |
| Transport Goods | ❌     | ❌          | ✅          | ❌         | ❌       | ✅    |
| Sell Products   | ❌     | ❌          | ❌          | ✅         | ❌       | ✅    |
| Trace Products  | ❌     | ❌          | ❌          | ❌         | ✅       | ✅    |
| User Management | ❌     | ❌          | ❌          | ❌         | ❌       | ✅    |

### Dashboard Features

- **Real-time Notifications**: Event updates and alerts
- **Analytics**: Sales data, batch tracking, performance metrics
- **Document Management**: Upload and view certificates
- **IoT Monitoring**: Sensor data visualization
- **Blockchain Verification**: Transaction hash validation

---

## 🔐 Security Features

### Authentication & Authorization

- **JWT Tokens**: Stateless authentication with expiration
- **Password Hashing**: bcrypt with salt rounds
- **Role-Based Access**: Middleware-enforced permissions
- **Session Management**: Secure token handling

### Data Protection

- **Input Validation**: Sanitized user inputs
- **SQL Injection Prevention**: Parameterized queries
- **CORS Configuration**: Controlled cross-origin access
- **Environment Variables**: Sensitive data protection

### Blockchain Security

- **Cryptographic Hashing**: SHA-256 for block validation
- **Proof-of-Work**: Mining-based consensus
- **Immutable Ledger**: Tamper-proof transaction history
- **Digital Signatures**: Event authenticity verification

---

## 🤝 Contributing

This project was developed as part of an academic course. For educational purposes:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'Add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

### Development Guidelines

- Follow existing code style and structure
- Add tests for new features
- Update documentation for API changes
- Ensure security best practices are maintained

---

## 📄 License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Authors

**Hamza** - _Lead Developer & Project Manager_

- Volunteered to develop this system from concept to completion
- Implemented full-stack architecture with blockchain integration
- Designed security features and user experience

**Professor** - _Project Supervisor & Concept Creator_

- Provided the innovative blockchain traceability idea
- Guided the Information Security course implementation
- Mentored the development process

### Acknowledgments

- Special thanks to our Information Security professor for the inspiring project concept
- Gratitude to the open-source community for the amazing tools and libraries
- Appreciation for the agricultural industry partners who provided domain insights

---

## 🔗 Blockchain Component Details

### AgriBlock: Agricultural Supply Chain Blockchain

AgriBlock is a custom **Proof-of-Work blockchain** designed to track agricultural products across the entire supply chain. Instead of cryptocurrency balances, AgriBlock stores **immutable data events** such as harvesting, processing, transport, packaging, and more.

#### Key Blockchain Features

- **Immutable Ledger:** Core blockchain logic implemented in **Rust** for performance and safety.
- **Data-Centric Design:** Replaces financial "Account Balance" checks with **Data Validation** logic.
- **Flexible Payloads:** Supports JSON-based data storage (Crop type, Humidity, Temperature, Quality Grade).
- **Validator Node:** The mining node acts as a system validator, stamping every block with a cryptographic proof of validation.

#### Blockchain Architecture

The system uses a hybrid architecture to separate the consensus layer from the application layer:

1. **The Node (Rust):** Maintains the ledger, pools transactions, and performs Proof-of-Work (SHA-256) mining.
2. **The API (HTTP/JSON):** Exposes endpoints for data submission and history retrieval.

#### Block Structure

Transactions are structured to track batch ownership and state rather than financial value:

```json
{
  "batch_id": "WHEAT-2025-001",
  "event_type": "HARVEST",
  "sender": "000...FARMER_ID",
  "recipient": "000...WAREHOUSE_ID",
  "data": "{\"crop\": \"Wheat\", \"qty\": \"500kg\", \"grade\": \"A\"}"
}
```

#### Blockchain API Documentation

| Method   | Endpoint        | Description                         |
| -------- | --------------- | ----------------------------------- |
| **GET**  | `/blocks`       | Returns the full chain history.     |
| **POST** | `/transactions` | Submits a new event to the mempool. |

**Example POST Payload:**

```json
{
  "batch_id": "WHEAT-001",
  "event_type": "TRANSPORT",
  "sender": "000...111",
  "recipient": "000...222",
  "data": "{\"temp\": \"12C\", \"location\": \"M2 Motorway\"}"
}
```

---

## 📁 Project Structure

```
AgriBlock/
├── config/
│   └── db.js                 # Database connection pool
├── controllers/
│   ├── authController.js     # Authentication logic
│   ├── farmerController.js   # Farmer operations
│   ├── distributorController.js # Distributor operations
│   ├── transporterController.js # Transport operations
│   ├── shopRoutes.js         # Shopkeeper operations
│   ├── traceabilityController.js # Traceability engine
│   └── ...                   # Other controllers
├── routes/
│   ├── authRoutes.js         # Auth API routes
│   ├── farmerRoutes.js       # Farmer endpoints
│   └── ...                   # Other route files
├── database/
│   ├── schema.sql            # Database schema
│   └── seed.js               # Database seeder
├── middleware/
│   ├── authMiddleware.js     # JWT authentication
│   └── rbacMiddleware.js     # Role-based access control
├── models/
│   ├── User.js               # User model
│   ├── Product.js            # Product model
│   ├── Batch.js              # Batch model
│   └── ...                   # Other models
├── server.js                 # Express server
├── client/                   # React frontend
│   ├── src/
│   │   ├── context/
│   │   │   └── AuthContext.jsx # Global auth state
│   │   ├── pages/
│   │   │   ├── Login.jsx
│   │   │   ├── FarmerDashboard.jsx
│   │   │   ├── DistributorDashboard.jsx
│   │   │   ├── TransporterDashboard.jsx
│   │   │   ├── ShopkeeperDashboard.jsx
│   │   │   ├── ConsumerDashboard.jsx
│   │   │   └── AdminDashboard.jsx
│   │   ├── components/
│   │   │   └── ProtectedRoute.jsx # Route protection
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── package.json
├── scripts/
│   └── fix_marketplace_data.js # Data fixing scripts
├── utils/
│   └── batchCodeGenerator.js  # Batch code generation
└── package.json

AgriBlock_rust_blockchain-main/
└── AgriBlock_rust_blockchain-main/
    ├── Cargo.toml            # Rust dependencies
    ├── src/
    │   ├── main.rs           # Main blockchain node
    │   ├── api.rs            # HTTP API handlers
    │   ├── miner.rs          # Mining logic
    │   ├── model.rs          # Data models
    │   ├── peer.rs           # Peer networking
    │   └── util.rs           # Utilities
    ├── tests/                # Unit tests
    └── README.md             # Blockchain documentation
```

---

## 🎯 Features Implemented

✅ **Backend Authentication API** (`POST /api/auth/login`)
✅ **JWT Token Generation**
✅ **React Frontend with Tailwind CSS**
✅ **Role-Based Routing**
✅ **Protected Routes** (Role-specific access)
✅ **5 Role-Specific Dashboards**
✅ **Global Auth Context Management**
✅ **Professional Login UI**
✅ **Database Schema** (Users, Products, Batches, Events)
✅ **Blockchain Integration** (Rust PoW implementation)
✅ **IoT Device Support** (Sensor data logging)
✅ **Media Attachments** (Photos, certificates, reports)
✅ **E-commerce Marketplace**
✅ **Complete Traceability Engine**

---

## 🔄 Next Steps & Future Enhancements

Phase 3 and beyond will implement:

- Advanced analytics and reporting
- Mobile application development
- Multi-language support
- Advanced IoT sensor integration
- Smart contract automation
- Third-party API integrations
- Enhanced security features
- Performance optimizations

---

_Built with ❤️ as a semester project to demonstrate the power of blockchain in solving real-world supply chain challenges._</content>
<parameter name="filePath">c:\Users\hamza\Documents\NUST DOCS SEM 3\Assignment, Presentation\IS\project\README.md
