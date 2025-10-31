# 📧 Email Cleaner Pro - Professional Email Validation Tool

<div align="center">

![Logo](https://raw.githubusercontent.com/Hai-Elkaim/Email-Cleaner-Assets/main/logo/logo-kalel.png)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Hai-Elkaim/Email-Cleaner-Pro/blob/main/EmailCleanerPro.ipynb)

**Professional email validation with bounce analysis, risk scoring, and beautiful visualizations**

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

</div>

---

## 🚀 Quick Start

1. **Click the Colab badge above** to open the notebook
2. **Run all cells** in order (username déjà configuré: `Hai-Elkaim`)
3. **Start validating emails!**

---

## ✨ Features

### 🔍 **Email Validation**
- **Format Validation** - RFC 5322 compliant email syntax checking
- **DNS Verification** - Checks MX and A records for deliverability
- **Disposable Detection** - Identifies temporary/fake email services
- **Risk Scoring** - 0-100 scale from EXCELLENT to CRITICAL
- **Suspicious Patterns** - Detects unusual email patterns

### 📊 **Beautiful Visualizations**
- **Risk Distribution** - Interactive donut chart showing risk levels
- **Top Risk Emails** - Bar chart highlighting highest risk addresses
- **GeoIP Mapping** - World map showing email locations (with GeoLite)

### 📧 **Bounce Analysis**
- **DSN Header Parsing** - Extracts detailed bounce information
- **Bounce Classification** - Hard/Soft bounce detection
- **CSV Export** - Save detailed bounce analysis results

### 💾 **Export Options**
- **CSV Export** - Clean validation results
- **Excel Export** - Professional spreadsheet format
- **Bounce Summary** - Comprehensive bounce analysis reports

---

## 🎯 Perfect For

| Use Case | Description |
|----------|-------------|
| **📧 Email Marketers** | Clean and validate email lists before campaigns |
| **🏢 Business Owners** | Verify customer email addresses |
| **👨‍💻 Developers** | Test email validation logic and APIs |
| **📊 Data Analysts** | Analyze email quality and deliverability |
| **🔍 Anyone** | Improve email deliverability and reduce bounces |

---

## 📋 Requirements

### **GitHub Assets Repository**
You need a public GitHub repository with these assets:

```
Email-Cleaner-Assets/
├── logo/
│   └── logo-kalel.png
├── geolite/
│   └── GeoLite2-Country.mmdb
└── bounces/
    ├── hard_bounce_example.eml
    ├── soft_bounce_full_example.eml
    └── soft_bounce_temp_example.eml
```

### **Asset URLs**
- **Logo**: `https://raw.githubusercontent.com/Hai-Elkaim/Email-Cleaner-Assets/main/logo/logo-kalel.png`
- **GeoLite2**: `https://raw.githubusercontent.com/Hai-Elkaim/Email-Cleaner-Assets/main/geolite/GeoLite2-Country.mmdb`
- **Bounce Examples**: `https://raw.githubusercontent.com/Hai-Elkaim/Email-Cleaner-Assets/main/bounces/`

---

## 🛠️ How It Works

### **Step 1: Configuration**
- Set your GitHub username
- Builds asset URLs automatically
- Downloads required files

### **Step 2: Installation**
- Installs Python packages (ipywidgets, plotly, folium, pandas, etc.)
- Sets up async processing
- Loads GeoIP database

### **Step 3: Validation**
- Paste emails or upload files
- Concurrent processing for speed
- Real-time progress updates

### **Step 4: Analysis**
- Beautiful charts and visualizations
- Risk scoring and classification
- GeoIP mapping (if available)

### **Step 5: Export**
- Save results as CSV or Excel
- Detailed bounce analysis
- Professional reports

---

## 📊 Risk Scoring System

| Score Range | Level | Description |
|-------------|-------|-------------|
| **0-19** | ✅ **EXCELLENT** | Perfect email, high deliverability |
| **20-39** | 🟢 **LOW** | Good email, minor issues |
| **40-59** | 🟡 **MEDIUM** | Moderate risk, needs attention |
| **60-79** | 🟠 **HIGH** | High risk, likely to bounce |
| **80-100** | 🔴 **CRITICAL** | Very high risk, avoid sending |

---

## 🌍 GeoIP Mapping

The tool can show email locations on an interactive world map using the GeoLite2 database:

- **Automatic Download** - Gets GeoLite2 from your GitHub assets
- **Interactive Map** - Click markers for details
- **Country Analysis** - See email distribution by country
- **Visual Insights** - Understand your audience geography

---

## 📧 Bounce Analysis

Parse bounce emails to extract valuable information:

- **DSN Headers** - Delivery Status Notification details
- **Bounce Types** - Hard bounces vs soft bounces
- **Recipient Analysis** - Which emails are bouncing
- **Domain Statistics** - Top bouncing domains
- **Export Reports** - Save analysis to CSV

---

## 🔧 Technical Details

### **Libraries Used**
- `ipywidgets` - Interactive UI components
- `plotly` - Beautiful charts and graphs
- `folium` - Interactive maps
- `pandas` - Data manipulation
- `dnspython` - DNS lookups
- `aiohttp` - Async HTTP requests
- `maxminddb` - GeoIP database reader

### **Performance**
- **Concurrent Processing** - Validates multiple emails simultaneously
- **Async Operations** - Non-blocking DNS lookups
- **Efficient Caching** - Reuses DNS results
- **Memory Optimized** - Handles large email lists

---

## 📝 Usage Examples

### **Basic Email Validation**
```python
# Paste emails in the text area
user1@example.com
user2@test.com
user3@company.org

# Click "Validate Emails"
# View results and charts
```

### **Bounce Analysis**
```python
# Paste bounce email content
From: mailer-daemon@example.com
Subject: Delivery Status Notification (Failure)
X-Bounce-Category: hard
Final-Recipient: user@example.com
Action: failed
Status: 5.1.1

# Click "Analyze Bounce"
# View parsed information
```

### **Export Results**
```python
# After validation, click:
# "Export CSV" - for validation results
# "Export Excel" - for professional format
# "Export Bounces" - for bounce analysis
```

---

## 🚨 Important Notes

### **GeoLite License**
- MaxMind's GeoLite2 database has specific licensing terms
- You can host your own copy in your assets repository
- Or upload the `.mmdb` file manually in Colab

### **Rate Limits**
- DNS lookups may be rate-limited by your ISP
- Large email lists may take time to process
- Consider processing in batches for very large lists

### **Privacy**
- All processing happens in your Colab session
- No data is sent to external services (except DNS)
- You control all your data

---

## 🆘 Troubleshooting

### **Common Issues**

| Problem | Solution |
|---------|----------|
| **"No emails provided"** | Paste emails in the text area first |
| **"Installation failed"** | Re-run the installation cell |
| **"GeoLite download failed"** | Upload GeoLite2-Country.mmdb manually |
| **"DNS lookup failed"** | Check your internet connection |
| **"Export failed"** | Validate emails before exporting |

### **Getting Help**
- Check the error messages in the output
- Re-run cells if something fails
- Make sure your GitHub assets are public
- Verify your GitHub username is correct

---

## 📈 Performance Tips

- **Batch Processing** - Process emails in groups of 100-500
- **Network Stability** - Use stable internet connection
- **Resource Management** - Close other Colab tabs if needed
- **Regular Saves** - Download results frequently

---

## 🤝 Contributing

We welcome contributions! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch**
3. **Make your changes**
4. **Submit a pull request**

### **Areas for Improvement**
- Additional validation checks
- More visualization options
- Better error handling
- Performance optimizations

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Hai Elkaim**
- **Organization**: KalEl Group
- **Email**: hai@kal-el.group
- **Website**: https://kal-el.group/

---

## 🙏 Acknowledgments

- **MaxMind** - For the GeoLite2 database
- **Plotly** - For beautiful visualizations
- **Folium** - For interactive maps
- **Jupyter** - For the notebook environment
- **Google Colab** - For the free computing platform

---

## 📞 Support

Need help? Here's how to get support:

- **📧 Email**: hai@kal-el.group
- **🌐 Website**: https://kal-el.group/
- **📱 Issues**: Create an issue on GitHub
- **💬 Discussions**: Use GitHub Discussions

---

<div align="center">

**⭐ Star this repository if you find it helpful!**

[![GitHub stars](https://img.shields.io/github/stars/Hai-Elkaim/Email-Cleaner-Pro?style=social)](https://github.com/Hai-Elkaim/Email-Cleaner-Pro)
[![GitHub forks](https://img.shields.io/github/forks/Hai-Elkaim/Email-Cleaner-Pro?style=social)](https://github.com/Hai-Elkaim/Email-Cleaner-Pro)

Made with ❤️ by [KalEl Group](https://kal-el.group/)

</div>
