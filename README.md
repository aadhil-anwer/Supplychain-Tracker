Supply Chain Tracking System
A Solidity-based smart contract designed to track goods through various stages in a supply chain. This project allows authorized entities to update shipment statuses while providing visibility to users. Role-based access control ensures secure operations.

Features
Role-Based Access Control:

Admin: The deployer of the contract is assigned as the admin.
Updater: Admin can grant or revoke updater roles. Only updaters can modify shipment statuses.
Shipment Tracking:

Each shipment is stored in the contract with a unique ID.
Shipment statuses can be updated (e.g., In Transit, Delivered).
Events:

ShipmentStatusUpdated: Logs changes in shipment status.
UpdaterRoleChanged: Logs changes to updater roles.
Utility Functions:

addUpdater: Admin grants updater roles.
removeUpdater: Admin revokes updater roles.
getShipment: Fetches details of a shipment (description, status, and last updated by).
Prerequisites
To work with this project, you need:

Remix IDE or other Solidity-compatible development environments.
Metamask Wallet for deploying and interacting with the contract.
A test blockchain environment such as Ganache.
Setup and Deployment
Step 1: Clone the Repository
bash
Copy code
git clone https://github.com/your-username/supplychain-tracking.git
cd supplychain-tracking
Step 2: Open in Remix IDE
Open Remix IDE.
Navigate to the SupplyChain.sol file.
Compile the contract using the Solidity compiler (version ^0.8.0).
Step 3: Deploy the Contract
Deploy the contract using the "Deploy & Run Transactions" tab in Remix.
Set the deployer address as the Admin during the deployment process.
Usage
1. Adding an Updater
Only the Admin can authorize an updater.

solidity
Copy code
addUpdater(address updaterAddress);
2. Removing an Updater
Only the Admin can revoke an updater's role.

solidity
Copy code
removeUpdater(address updaterAddress);
3. Updating Shipment Status
Authorized Updaters can modify shipment details.

solidity
Copy code
updateShipmentStatus(uint256 shipmentId, string description, string status);
4. Viewing Shipment Details
Anyone can view the details of a shipment.

solidity
Copy code
getShipment(uint256 shipmentId);
