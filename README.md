# Supply Chain Tracking System

A Solidity-based smart contract designed to track goods through various stages in a supply chain. This project allows authorized entities to update shipment statuses while providing visibility to users. Role-based access control ensures secure and streamlined operations.

---

## Features

### **Role-Based Access Control**
- **Admin:**  
  The deployer of the contract is automatically assigned the Admin role.
- **Updater:**  
  The Admin can grant or revoke updater roles. Only updaters are authorized to modify shipment statuses.

### **Shipment Tracking**
- Each shipment is stored in the contract with a unique ID.
- Shipment statuses can be updated (e.g., *In Transit*, *Delivered*).

### **Events**
- `ShipmentStatusUpdated`: Logs changes in shipment status.
- `UpdaterRoleChanged`: Logs changes to updater roles.

### **Utility Functions**
- `addUpdater`: Admin grants updater roles.
- `removeUpdater`: Admin revokes updater roles.
- `getShipment`: Fetches details of a shipment (description, status, and last updated by).

---

## Prerequisites

To work with this project, you need:
- **Remix IDE** or other Solidity-compatible development environments.
- **MetaMask Wallet** for deploying and interacting with the contract.
- A test blockchain environment such as **Ganache**.

---

## Setup and Deployment

### **Step 1: Clone the Repository**
```bash
git clone https://github.com/your-username/supplychain-tracking.git
cd supplychain-tracking
