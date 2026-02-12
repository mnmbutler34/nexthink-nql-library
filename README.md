# Nexthink NQL Library

A curated collection of NQL queries for Nexthink Infinity — ready to import, customize, and deploy.

> **Part of [Butler DEX Enterprise](https://github.com/ButlerDEXEnterprise)** — At Your Enterprise's Service.

---

## 📋 Query Categories

| Category | Description | Count |
|---|---|---|
| [Device Health](#device-health) | Uptime, disk space, performance baselines | — |
| [Software & Compliance](#software--compliance) | License usage, unauthorized installs, patch status | — |
| [User Experience](#user-experience) | Login times, app crashes, sentiment signals | — |
| [Cost Optimization](#cost-optimization) | Unused software, underutilized hardware, reclamation candidates | — |

---

## Device Health

### Long Uptime Devices
**File:** `device-health/long-uptime.nql`

**What it finds:** Devices that haven't rebooted in X days (configurable threshold).

**Why it matters:** Unrebooted devices miss patches, accumulate memory leaks, and degrade over time. This is usually the #1 quick win in any DEX engagement.

```nql
// Example query structure — actual query in file
devices
| where device.last_reboot_duration > 7d
| list device.name, device.last_reboot_duration, device.operating_system
```

---

## 📁 Repository Structure

```
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
```

---

## 🚀 How to Use

1. Browse the category that matches your need
2. Open the `.nql` file and review the query
3. Adjust parameters (thresholds, filters) for your environment
4. Create an API NQL query in Nexthink and paste the query
5. Run manually or schedule via the [NexthinkAPI PowerShell module](https://github.com/NexthinkGuru/NexthinkAPI)

---

## 🤝 Contributing

Have a useful NQL query? We'd love to include it.

1. Fork this repo
2. Add your query in the appropriate category folder
3. Include a brief description in the folder's README
4. Submit a Pull Request

---

## 📄 License

MIT License — free to use, modify, and contribute.
