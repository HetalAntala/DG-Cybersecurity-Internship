📌 Objective
To deploy software automatically to domain users or computers using Group Policy Object (GPO) in a Windows Server environment.

🛠 Tools & Environment

OS: Windows Server 2022
Role: Active Directory Domain Services
Tool: Group Policy Management
Client: Windows domain-joined system

🔧 Prerequisites

Server promoted as Domain Controller
Domain created (e.g., dg.local)
Client system joined to domain

.msi installer available

⚙ Task Performed
1. Create Shared Folder
Created a shared folder for software deployment.
C:\Software
Right-click → Properties → Sharing → Advanced Sharing
Enabled sharing
Gave Read access to Domain Computers

2. Create New GPO

Opened Group Policy Management
Created GPO:
Software_Deployment_GPO
Linked GPO to domain

3. Configure Software Deployment

Edited GPO:

Computer Configuration
 → Policies
 → Software Settings
 → Software Installation

Selected New → Package
Chose MSI file using UNC path:
\\ServerName\Software\app.msi
Selected Assigned

4. Policy Update

On client machine:
gpupdate /force
Restarted system to apply policy.

🧪 Verification

Software installed automatically on client system
Verified in Programs & Features

⚠ Issues Faced
Software did not install initially

Solution
Ensured MSI path used UNC path
Verified domain permissions on shared folder

🧠 Learning Outcome

Learned centralized software deployment
Understood importance of permissions and UNC paths
Gained experience in enterprise endpoint management

📝 Conclusion
Successfully deployed software using Group Policy, demonstrating automated system administration.