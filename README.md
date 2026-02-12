Nexthink NQL Library
A curated collection of NQL queries for Nexthink Infinity — ready to import, customize, and deploy.

Part of Butler DEX Enterprise — At Your Enterprise's Service.


📋 Query Categories
CategoryDescriptionCountDevice HealthUptime, disk space, performance baselines—Software & ComplianceLicense usage, unauthorized installs, patch status—User ExperienceLogin times, app crashes, sentiment signals—Cost OptimizationUnused software, underutilized hardware, reclamation candidates—

Device Health
Long Uptime Devices
File: device-health/long-uptime.nql
What it finds: Devices that haven't rebooted in X days (configurable threshold).
Why it matters: Unrebooted devices miss patches, accumulate memory leaks, and degrade over time. This is usually the #1 quick win in any DEX engagement.
nql// Example query structure — actual query in file
devices
| where device.last_reboot_duration > 7d
| list device.name, device.last_reboot_duration, device.operating_system

📁 Repository Structure
nexthink-nql-library/
├── README.md
├── LICENSE
├── device-health/
│   ├── long-uptime.nql
│   ├── low-disk-space.nql
│   └── README.md
├── software-compliance/
│   ├── unauthorized-browsers.nql
│   └── README.md
├── user-experience/
│   ├── slow-login-times.nql
│   └── README.md
└── cost-optimization/
    ├── unused-software.nql
    └── README.md

🚀 How to Use

Browse the category that matches your need
Open the .nql file and review the query
Adjust parameters (thresholds, filters) for your environment
Create an API NQL query in Nexthink and paste the query
Run manually or schedule via the NexthinkAPI PowerShell module


🤝 Contributing
Have a useful NQL query? We'd love to include it.

Fork this repo
Add your query in the appropriate category folder
Include a brief description in the folder's README
Submit a Pull Request


📄 License
MIT License — free to use, modify, and contribute.
