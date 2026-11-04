# Features
- User registration and authentication
- Create and manage voting categories
- Cast votes for candidates within each category
- Real-time vote counting and results display
- Admin dashboard for managing the voting system
  
# Technologies Used

- HTML, CSS, JavaScript
- PHP
- XAMPP
- MySQL

An online voting application hosted on Microsoft Azure, with secure networking, centralized monitoring and logging, an AI chatbot that answers voter questions, and role-based access control (RBAC).

# Architecture

```mermaid
flowchart LR
    U([Voter]) -->|HTTPS| APP
    U -->|Chat| BOT[AI Bot Service]

    subgraph AZ[Microsoft Azure]
        subgraph NET[Virtual Network]
            NSG{{NSG rules}} --> APP[Azure VM<br/>Voting App]
        end
        BOT
        APP --> MON[Azure Monitor<br/>Log Analytics]
        BOT --> MON
        RBAC[Azure RBAC<br/>least-privilege roles] -.controls access.-> AZ
    end
```

# What I Built

- Azure Virtual Machine: deployed a VM to host the voting application.
- Virtual Network (VNET): created the network the VM runs in and controlled traffic with Network Security Group rules.
- Monitoring and logging: set up Azure Monitor to collect logs and metrics for visibility into the system.
- AI bot service: built and trained a chatbot to answer general voter questions, reducing the need for human interaction.
- Access control (RBAC): applied role-based access control so each user can access only the resources their role requires.
- CI/CD: GitHub Actions workflow that builds the app and deploys it to Azure (see .github/workflows/).

# Screenshots

# Virtual Network and NSG Rules
![VNET and NSG rules](docs/images/01-vnet-nsg.png)

# Role Assignments (RBAC)
![RBAC role assignments](docs/images/02-rbac-roles.png)

# Monitoring Dashboard
![Azure Monitor dashboard](docs/images/03-monitor-dashboard.png)

# AI Bot Conversation
![Voter bot conversation](docs/images/04-bot-conversation.png)

# Tech Stack

Azure: Virtual Machines, Virtual Network, Network Security Groups, Azure Monitor, Log Analytics, AI Bot Service, Azure RBAC

Tools: GitHub Actions, Git

Application: PHP, MySQL, HTML/CSS/JavaScript (from the original project)

# License

The original application is licensed under Apache 2.0. See the LICENSE file.
   
   `password:  mohan.sjbit`
