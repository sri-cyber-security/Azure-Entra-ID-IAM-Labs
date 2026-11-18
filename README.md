# Lab 1: Identity & Access Management (IAM) in Microsoft Entra ID

## Objective
To implement Identity and Access Management (IAM) controls, enforce Multi-Factor Authentication (MFA), and configure Role-Based Access Control (RBAC) following the principle of Least Privilege.

## Tools & Platforms
* **Cloud Platform:** Microsoft Azure
* **Identity Provider:** Microsoft Entra ID 

## Lab Steps Performed

### 1. Identity Creation
Created a new administrative user and a security group (`IT Department`) in Entra ID.
<img width="1920" height="967" alt="entra user creation" src="https://github.com/user-attachments/assets/21ee8e7d-8abc-407a-9959-f82fa40ca175" />
<img width="1920" height="982" alt="entra group" src="https://github.com/user-attachments/assets/54db0fd6-6bf4-41a2-a4dc-e410736ad7e0" />

### 2. RBAC Assignment
Assigned the `User Administrator` role to the specific user instead of Global Admin, adhering to the Least Privilege principle.
<img width="1920" height="908" alt="entra roles kumar" src="https://github.com/user-attachments/assets/40396d01-1202-42e7-b05c-69111cdc6866" />

### 3. Multi-Factor Authentication (MFA) Enforcement
During the initial login of the newly created Admin account, Azure's Security Defaults enforced a mandatory MFA registration. Successfully registered and authenticated the account using the Microsoft Authenticator app to ensure secure administrative access. 
<img width="1920" height="1023" alt="kumar entra mfa" src="https://github.com/user-attachments/assets/e7020651-5ee0-4e1a-9092-b42283427745" />

### 4. Verification & Access Control Testing
Logged in as the newly created Admin (Kumar) and verified the dashboard view. To validate the assigned `User Administrator` role permissions, successfully provisioned a new dummy user account (`testing`).
<img width="1920" height="1006" alt="kumar user admin" src="https://github.com/user-attachments/assets/12e53654-f928-4414-a8ea-e6d29d40b466" />

### 5. Proof of Least Privilege (RBAC Boundary)
To verify the RBAC boundaries, attempted to delete the Global Admin account using the User Administrator account. The system successfully blocked the action, proving the principle of least privilege.
<img width="1920" height="1013" alt="entra kumar-unable to del glob admin" src="https://github.com/user-attachments/assets/a41f2740-491d-4c26-9eb0-d81985b83b12" />
