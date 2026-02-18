Active Directory Setup & Structure

This document outlines the configuration of Active Directory within the enterprise sysadmin lab environment, including Organizational Units (OUs), users, and security groups.

🏢 Purpose of Active Directory in This Lab

Active Directory is used to:

Centrally manage users and computers

Organize departments using Organizational Units

Apply security and access control using groups

Simulate a real enterprise identity structure

📂 Organizational Unit (OU) Design

Created OUs to represent departments:

IT

HR

Sales

Management

(Additional departments can be added as the lab expands.)


👥 User Accounts

Created multiple test users within each OU to simulate employees.

Example:

IT: ituser1, ituser2

HR: hruser1, hruser2

Sales: salesuser1, salesuser2

Users were created inside their respective departmental OUs.

🔐 Security Groups

Created security groups for role-based access:

IT_Security_Group

HR_Security_Group

Sales_Security_Group

Management_Security_Group

Group Strategy:

Users added to their department’s security group

Permissions will later be assigned to groups (not individual users)

This follows best practice enterprise access control.

🧠 Best Practice Used

✔ Separation by department
✔ Group-based permissions
✔ Scalable structure
✔ Simplified management

✅ Validation

Confirmed:

OUs created correctly

Users located in correct OUs

Users successfully added to security groups

Active Directory Users & Computers reflecting proper hierarchy

📸 Related Screenshots

Located in:

screenshots/


Examples:

OU structure

User accounts in each OU

Security group membership

🎯 Outcome

Active Directory is now structured to support:

Scalable user growth

Secure access control

Group Policy implementation

Enterprise-style administration

🚀 Next Steps

This structure will be used for:

File server permissions

Group Policy Objects (GPOs)

Role-based access management (Next part of the project)

