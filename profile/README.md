# PredictaMarket | The Prediction Market

This is a prediction market platform, where users can make predictions about the outcome of future events. Users can buy and sell predictions, and the system handles trade execution, market resolution, and provides real-time updates. The platform is designed using a microservice architecture, with each microservice handling a specific part of the system.

### 1. Trade Engine Microservice
The Trade Engine handles the core functionality of executing trades, managing market prices, and resolving markets based on event outcomes.

#### Responsibilities:
- **Trade Execution**: Handles the execution of buy/sell orders.
- **Managing Buy/Sell Prices**: Updates and maintains the current market prices.
- **Market State Management**: Tracks the state of active markets.
- **Market Resolution**: Resolves markets based on the outcomes of events.

---

### 2. Notification Microservice
The Notification Service is responsible for sending alerts and notifications to users regarding their transactions and market conditions.

#### Responsibilities:
- **Trigger Alerts**: Sends notifications for significant market changes or events.
- **Order Confirmation/Alerts/Invoices**: Provides transactional notifications to users, such as order confirmations and invoices.

---

### 3. User Management Microservice
The User Management Service handles user accounts, wallets, and admin functionality, including managing events and setting alerts.

#### Responsibilities:
- **Client and Admin Management**: Manages user roles and permissions.
- **Wallet Management**: Tracks user wallet balances and transaction history.
- **Set Alerts**: Allows users to configure alerts for specific events or market changes.
- **View Orders/Transactions**: Provides a history of user transactions and orders.

---

### 4. Price Streaming Service
The Price Streaming Service provides real-time updates to users about market prices, predictions, and events.

#### Responsibilities:
- **Provide Real-Time Updates**: Streams live market data to users.
- **Market Condition Updates**: Keeps users informed about significant market changes and predictions.

---

### 5. Orchestrator Microservice
The Orchestrator is the central controller that coordinates the flow of operations between the various microservices based on specific events and conditions.

#### Responsibilities:
- **Flow Control**: Manages the order in which microservices are triggered, ensuring each step is executed based on prior actions or events.
- **Event Outcome Processing**: Determines the next steps based on results of market resolutions or other events.
- **Coordinating Distributed Tasks**: Ensures that tasks are distributed across microservices correctly and efficiently.
- **Transaction Lifecycle Management**: Oversees the start, execution, and resolution of transactions, coordinating responses from other microservices.
