# Building Your Custom Financial Model in Google Sheets
**Lab 9: From Unit Economics to Automated Financial Projections**

---

## 🎯 Overview

Now that you've calculated your **CAC** and **LTV** using the unit economics template, it's time to build a complete **12-month financial model** that uses YOUR actual numbers.

Instead of manually building spreadsheets from scratch, we'll use **Google Sheets Apps Script** to automatically generate a professional financial model with all the formulas, formatting, and structure you need.

**What You'll Build:**
- Complete 12-month revenue and cost projections
- Automated P&L statement
- Cash flow tracking with runway
- Unit economics dashboard
- All using YOUR team's actual assumptions

---

## 📋 Prerequisites: Complete Your Unit Economics FIRST

**Before building the financial model, you MUST complete:**

### ✅ Step 1: Calculate Your CAC

**Refer back to:** `lab-9-template-unit-economics.md` Section: Customer Acquisition Cost

**You should have calculated:**
```
CAC = Total Sales & Marketing Spend / New Customers Acquired
CAC = $______ per customer
```

**Example:**
- Total S&M Spend (Month 1): $1,600
- New Customers: 8
- **CAC = $200**

**Your CAC:** $______

---

### ✅ Step 2: Calculate Your LTV

**Refer back to:** `lab-9-template-unit-economics.md` Section: Lifetime Value

**You should have calculated:**
```
LTV = ARPU × Gross Margin % × (1 / Churn Rate)
LTV = $______ per customer
```

**Example:**
- ARPU: $50/month
- Gross Margin: 80%
- Monthly Churn: 5%
- **LTV = $800**

**Your LTV:** $______

---

### ✅ Step 3: Gather Your Other Key Assumptions

**From your unit economics work, you should have:**

| Assumption | Your Value | Notes |
|------------|------------|-------|
| **PRICING** | | |
| Monthly subscription price | $______ | What you charge per user |
| ARPU (Average Revenue Per User) | $______ | From unit economics |
| **CUSTOMER METRICS** | | |
| Starting customers (Month 1) | ______ | How many you have now |
| Monthly growth rate | ______% | How fast you're growing |
| Monthly churn rate | ______% | From LTV calculation |
| **COSTS** | | |
| COGS per customer % | ______% | Delivery costs |
| CAC (from above) | $______ | Acquisition cost |
| Monthly burn rate | $______ | From Week 10 if available |
| **TEAM** | | |
| Developer salaries | $______ /mo | Total team cost |
| Marketing spend | $______ /mo | Ads, content, tools |
| **FUNDING** | | |
| Starting cash balance | $______ | What you have now |

**Don't have all these?** Make reasonable estimates and document them as "Estimated - to be validated"

---
Here is a Shortcut: - **[Professor Zeshan AI Financial Modelor] https://aistudio.google.com/apps/drive/1f4HhQVSoAEN6Q7S5s9FaBVf127vjZkdP?fullscreenApplet=true&showPreview=true&showAssistant=true
## 🚀 Building Your Financial Model: Step-by-Step

### Step 1: Open a New Google Sheet

1. Go to [sheets.google.com](https://sheets.google.com)
2. Click **+ Blank** to create a new spreadsheet
3. Name it: `[YourTeamName]-Financial-Model-12mo`

---

### Step 2: Open Apps Script Editor

1. In your Google Sheet, go to **Extensions** > **Apps Script**
2. You'll see a code editor with some default code
3. **Delete everything** in the editor (including `function myFunction()...`)

---

### Step 3: Customize the Script with YOUR Numbers

**Copy the script below, but FIRST customize these sections with YOUR team's actual data:**

---

## 📜 Your Custom Financial Model Script

**⚠️ IMPORTANT: Replace the values in the `Assumptions` section (lines 25-34) with YOUR actual numbers from Steps 1-3 above!**

```javascript
function createFinancialModel() {
  var ss = SpreadsheetApp.getActiveSpreadsheet();
  
  // ============================================================
  // 1. CREATE INSTRUCTIONS TAB
  // ============================================================
  var sheetInst = ss.getSheetByName("Sheet1");
  if (sheetInst) { 
    sheetInst.setName("Instructions"); 
  } else { 
    sheetInst = ss.insertSheet("Instructions"); 
  }
  
  sheetInst.getRange("A1").setValue("📊 12-Month Financial Model").setFontWeight("bold").setFontSize(16);
  sheetInst.getRange("A2").setValue("Lab 9 - Product Development Course").setFontSize(12);
  sheetInst.getRange("A4").setValue("Team Name:").setFontWeight("bold");
  sheetInst.getRange("B4").setValue("[Your Team Name Here]");
  sheetInst.getRange("A5").setValue("Date Created:").setFontWeight("bold");
  sheetInst.getRange("B5").setValue(new Date());
  
  sheetInst.getRange("A7").setValue("📖 How to Use This Model:").setFontWeight("bold").setFontSize(12);
  sheetInst.getRange("A8").setValue("1. Go to the 'Assumptions' tab first");
  sheetInst.getRange("A9").setValue("2. Blue cells = Your inputs (edit these)");
  sheetInst.getRange("A10").setValue("3. Black cells = Calculated formulas (don't edit)");
  sheetInst.getRange("A11").setValue("4. Check 'Dashboard' tab for summary");
  sheetInst.getRange("A12").setValue("5. Adjust assumptions and watch the model update automatically!");
  
  sheetInst.getRange("A14").setValue("⚠️ Important:").setFontWeight("bold").setFontColor("red");
  sheetInst.getRange("A15").setValue("• All your unit economics (CAC, LTV) are built into this model");
  sheetInst.getRange("A16").setValue("• Change assumptions to see different scenarios");
  sheetInst.getRange("A17").setValue("• Save versions for Pessimistic/Base/Optimistic cases");
  
  // ============================================================
  // 2. CREATE ASSUMPTIONS TAB
  // ============================================================
  var sheetAssump = ss.getSheetByName("Assumptions") || ss.insertSheet("Assumptions");
  sheetAssump.clear();
  
  // ⚠️⚠️⚠️ CUSTOMIZE THESE VALUES WITH YOUR TEAM'S ACTUAL NUMBERS! ⚠️⚠️⚠️
  var assumpData = [
    ["Category", "Assumption", "Value", "Notes / Source"],
    ["", "", "", ""],
    ["💰 PRICING", "", "", ""],
    ["", "Monthly Subscription Price ($)", 50, "🔵 INPUT: What you charge per user/month"],
    ["", "Annual Discount (%)", 0, "🔵 INPUT: Discount for annual plans (0 = no discount)"],
    ["", "", "", ""],
    ["📈 GROWTH", "", "", ""],
    ["", "Starting Customers (Month 1)", 10, "🔵 INPUT: How many customers you have now"],
    ["", "Monthly Customer Growth Rate (%)", 0.20, "🔵 INPUT: 0.20 = 20% growth per month"],
    ["", "When Growth Slows (Month #)", 6, "🔵 INPUT: Month when growth rate cuts in half"],
    ["", "", "", ""],
    ["📉 CHURN", "", "", ""],
    ["", "Monthly Churn Rate (%)", 0.05, "🔵 INPUT: From your LTV calculation (0.05 = 5%)"],
    ["", "When Churn Starts (Month #)", 2, "🔵 INPUT: Month when customers start churning"],
    ["", "", "", ""],
    ["💸 COSTS - COGS", "", "", ""],
    ["", "Hosting/Infrastructure (Fixed)", 50, "🔵 INPUT: Monthly hosting cost"],
    ["", "COGS per User ($)", 5, "🔵 INPUT: Variable cost per user (APIs, support, etc)"],
    ["", "Payment Processing Fee (%)", 0.03, "🔵 INPUT: Stripe/payment processor fee (0.03 = 3%)"],
    ["", "", "", ""],
    ["📢 COSTS - Sales & Marketing", "", "", ""],
    ["", "Monthly Ad Spend ($)", 500, "🔵 INPUT: Facebook, Google, etc."],
    ["", "Marketing Tools ($)", 100, "🔵 INPUT: Email, analytics, etc."],
    ["", "Content Creation ($)", 200, "🔵 INPUT: Blog, videos, design"],
    ["", "Sales Team Salaries ($)", 0, "🔵 INPUT: If you have sales team"],
    ["", "", "", ""],
    ["💻 COSTS - Development", "", "", ""],
    ["", "Developer Salaries ($)", 4000, "🔵 INPUT: Total monthly team cost"],
    ["", "Development Tools ($)", 200, "🔵 INPUT: GitHub, hosting, APIs"],
    ["", "", "", ""],
    ["🏢 COSTS - General & Admin", "", "", ""],
    ["", "Legal/Accounting ($)", 200, "🔵 INPUT: Monthly professional services"],
    ["", "Insurance ($)", 50, "🔵 INPUT: Business insurance"],
    ["", "Office/Admin ($)", 100, "🔵 INPUT: Office, supplies, misc"],
    ["", "", "", ""],
    ["💰 FUNDING", "", "", ""],
    ["", "Starting Cash Balance ($)", 50000, "🔵 INPUT: Cash you have now"],
    ["", "Funding to Raise ($)", 0, "🔵 INPUT: How much you're raising"],
    ["", "Funding Month", 6, "🔵 INPUT: When funding arrives"]
  ];
  
  sheetAssump.getRange(1, 1, assumpData.length, 4).setValues(assumpData);
  
  // Format assumptions tab
  sheetAssump.getRange("A1:D1").setFontWeight("bold").setBackground("#d9ead3").setFontSize(12);
  sheetAssump.setColumnWidth(1, 150);
  sheetAssump.setColumnWidth(2, 300);
  sheetAssump.setColumnWidth(3, 100);
  sheetAssump.setColumnWidth(4, 350);
  
  // Highlight INPUT cells in blue
  var blueCells = ["C4", "C5", "C8", "C9", "C10", "C13", "C14", "C17", "C18", "C19", 
                   "C22", "C23", "C24", "C25", "C28", "C29", "C32", "C33", "C34",
                   "C37", "C38", "C39"];
  for (var i = 0; i < blueCells.length; i++) {
    sheetAssump.getRange(blueCells[i]).setBackground("#cfe2f3").setFontWeight("bold");
  }
  
  // Format currency and percentages
  sheetAssump.getRange("C4:C4").setNumberFormat("$#,##0");
  sheetAssump.getRange("C5:C5").setNumberFormat("0%");
  sheetAssump.getRange("C9:C9").setNumberFormat("0%");
  sheetAssump.getRange("C13:C13").setNumberFormat("0%");
  sheetAssump.getRange("C17:C39").setNumberFormat("$#,##0");
  sheetAssump.getRange("C19:C19").setNumberFormat("0%");
  
  // ============================================================
  // 3. CREATE REVENUE MODEL TAB
  // ============================================================
  var sheetRev = ss.getSheetByName("Revenue Model") || ss.insertSheet("Revenue Model");
  sheetRev.clear();
  
  // Headers
  var headers = ["Metric"];
  for (var i = 1; i <= 12; i++) { headers.push("Month " + i); }
  sheetRev.getRange(1, 1, 1, 13).setValues([headers]).setFontWeight("bold").setBackground("#434343").setFontColor("white");
  
  // Revenue model labels
  var revLabels = [
    ["📊 CUSTOMER ACQUISITION"],
    ["New Customers Acquired"],
    ["Churned Customers"],
    ["Net New Customers"],
    ["Total Active Customers"],
    [""],
    ["💰 REVENUE"],
    ["MRR from New Customers"],
    ["MRR from Existing Customers"],
    ["Total MRR"],
    ["One-Time Revenue"],
    ["Total Monthly Revenue"],
    [""],
    ["📈 METRICS"],
    ["MoM Revenue Growth %"],
    ["Customer Count Growth %"],
    ["ARPU (Avg Rev Per User)"]
  ];
  sheetRev.getRange(2, 1, revLabels.length, 1).setValues(revLabels);
  sheetRev.getRange("A2").setFontWeight("bold").setBackground("#d9ead3");
  sheetRev.getRange("A8").setFontWeight("bold").setBackground("#d9ead3");
  sheetRev.getRange("A15").setFontWeight("bold").setBackground("#d9ead3");
  
  // MONTH 1 FORMULAS
  sheetRev.getRange("B3").setFormula("=Assumptions!C8"); // Starting customers
  sheetRev.getRange("B4").setValue(0); // No churn Month 1
  sheetRev.getRange("B5").setFormula("=B3-B4"); // Net new
  sheetRev.getRange("B6").setFormula("=B3"); // Total active
  
  sheetRev.getRange("B9").setFormula("=B3*Assumptions!$C$4"); // MRR from new
  sheetRev.getRange("B10").setValue(0); // No existing customers Month 1
  sheetRev.getRange("B11").setFormula("=B9+B10"); // Total MRR
  sheetRev.getRange("B12").setValue(0); // One-time revenue
  sheetRev.getRange("B13").setFormula("=B11+B12"); // Total revenue
  
  sheetRev.getRange("B18").setFormula("=IF(B6>0, B13/B6, 0)"); // ARPU
  
  // MONTH 2-6 FORMULAS (High growth phase)
  for (var col = 3; col <= 7; col++) {
    var colLetter = String.fromCharCode(64 + col);
    var prevCol = String.fromCharCode(64 + col - 1);
    
    sheetRev.getRange(colLetter + "3").setFormula("=ROUND(" + prevCol + "3*(1+Assumptions!$C$9), 0)"); // New customers with growth
    sheetRev.getRange(colLetter + "4").setFormula("=IF(" + colLetter + "1>=Assumptions!$C$14, " + prevCol + "6*Assumptions!$C$13, 0)"); // Churn if past start month
    sheetRev.getRange(colLetter + "5").setFormula("=" + colLetter + "3-" + colLetter + "4"); // Net new
    sheetRev.getRange(colLetter + "6").setFormula("=" + prevCol + "6+" + colLetter + "5"); // Total active
    
    sheetRev.getRange(colLetter + "9").setFormula("=" + colLetter + "3*Assumptions!$C$4"); // MRR new
    sheetRev.getRange(colLetter + "10").setFormula("=(" + prevCol + "6-" + colLetter + "4)*Assumptions!$C$4"); // MRR existing
    sheetRev.getRange(colLetter + "11").setFormula("=" + colLetter + "9+" + colLetter + "10"); // Total MRR
    sheetRev.getRange(colLetter + "12").setValue(0); // One-time
    sheetRev.getRange(colLetter + "13").setFormula("=" + colLetter + "11+" + colLetter + "12"); // Total rev
    
    sheetRev.getRange(colLetter + "16").setFormula("=IF(" + prevCol + "13>0, (" + colLetter + "13-" + prevCol + "13)/" + prevCol + "13, 0)"); // MoM growth
    sheetRev.getRange(colLetter + "17").setFormula("=IF(" + prevCol + "6>0, (" + colLetter + "6-" + prevCol + "6)/" + prevCol + "6, 0)"); // Customer growth
    sheetRev.getRange(colLetter + "18").setFormula("=IF(" + colLetter + "6>0, " + colLetter + "13/" + colLetter + "6, 0)"); // ARPU
  }
  
  // MONTH 7-12 FORMULAS (Growth slows down)
  for (var col = 8; col <= 13; col++) {
    var colLetter = String.fromCharCode(64 + col);
    var prevCol = String.fromCharCode(64 + col - 1);
    
    sheetRev.getRange(colLetter + "3").setFormula("=ROUND(" + prevCol + "3*(1+(Assumptions!$C$9/2)), 0)"); // Growth rate cuts in half
    sheetRev.getRange(colLetter + "4").setFormula("=IF(" + colLetter + "1>=Assumptions!$C$14, " + prevCol + "6*Assumptions!$C$13, 0)");
    sheetRev.getRange(colLetter + "5").setFormula("=" + colLetter + "3-" + colLetter + "4");
    sheetRev.getRange(colLetter + "6").setFormula("=" + prevCol + "6+" + colLetter + "5");
    
    sheetRev.getRange(colLetter + "9").setFormula("=" + colLetter + "3*Assumptions!$C$4");
    sheetRev.getRange(colLetter + "10").setFormula("=(" + prevCol + "6-" + colLetter + "4)*Assumptions!$C$4");
    sheetRev.getRange(colLetter + "11").setFormula("=" + colLetter + "9+" + colLetter + "10");
    sheetRev.getRange(colLetter + "12").setValue(0);
    sheetRev.getRange(colLetter + "13").setFormula("=" + colLetter + "11+" + colLetter + "12");
    
    sheetRev.getRange(colLetter + "16").setFormula("=IF(" + prevCol + "13>0, (" + colLetter + "13-" + prevCol + "13)/" + prevCol + "13, 0)");
    sheetRev.getRange(colLetter + "17").setFormula("=IF(" + prevCol + "6>0, (" + colLetter + "6-" + prevCol + "6)/" + prevCol + "6, 0)");
    sheetRev.getRange(colLetter + "18").setFormula("=IF(" + colLetter + "6>0, " + colLetter + "13/" + colLetter + "6, 0)");
  }
  
  // Format revenue tab
  sheetRev.setColumnWidth(1, 250);
  sheetRev.getRange("B9:M13").setNumberFormat("$#,##0");
  sheetRev.getRange("B16:M17").setNumberFormat("0.0%");
  sheetRev.getRange("B18:M18").setNumberFormat("$#,##0.00");
  sheetRev.getRange("B3:M6").setNumberFormat("#,##0");
  
  // ============================================================
  // 4. CREATE COST MODEL TAB
  // ============================================================
  var sheetCost = ss.getSheetByName("Cost Model") || ss.insertSheet("Cost Model");
  sheetCost.clear();
  sheetCost.getRange(1, 1, 1, 13).setValues([headers]).setFontWeight("bold").setBackground("#434343").setFontColor("white");
  
  var costLabels = [
    ["💸 COST OF GOODS SOLD (COGS)"],
    ["Hosting (Fixed)"],
    ["Variable COGS (per user)"],
    ["Payment Processing Fees"],
    ["Total COGS"],
    ["Gross Profit"],
    ["Gross Margin %"],
    [""],
    ["📢 SALES & MARKETING"],
    ["Ad Spend"],
    ["Marketing Tools"],
    ["Content Creation"],
    ["Sales Salaries"],
    ["Total S&M"],
    ["CAC (Cost per Customer)"],
    [""],
    ["💻 RESEARCH & DEVELOPMENT"],
    ["Developer Salaries"],
    ["Development Tools"],
    ["Total R&D"],
    [""],
    ["🏢 GENERAL & ADMINISTRATIVE"],
    ["Legal/Accounting"],
    ["Insurance"],
    ["Office/Admin"],
    ["Total G&A"],
    [""],
    ["💰 TOTAL COSTS"],
    ["Total Operating Expenses (OpEx)"],
    ["Total Costs (COGS + OpEx)"]
  ];
  sheetCost.getRange(2, 1, costLabels.length, 1).setValues(costLabels);
  sheetCost.getRange("A2").setFontWeight("bold").setBackground("#f4cccc");
  sheetCost.getRange("A9").setFontWeight("bold").setBackground("#f4cccc");
  sheetCost.getRange("A17").setFontWeight("bold").setBackground("#f4cccc");
  sheetCost.getRange("A22").setFontWeight("bold").setBackground("#f4cccc");
  sheetCost.getRange("A28").setFontWeight("bold").setBackground("#f4cccc");
  
  // COGS formulas
  sheetCost.getRange("B3:M3").setFormula("=Assumptions!$C$17"); // Hosting
  sheetCost.getRange("B4:M4").setFormula("='Revenue Model'!B6*Assumptions!$C$18"); // Variable COGS
  sheetCost.getRange("B5:M5").setFormula("='Revenue Model'!B13*Assumptions!$C$19"); // Payment fees
  sheetCost.getRange("B6:M6").setFormula("=SUM(B3:B5)"); // Total COGS
  sheetCost.getRange("B7:M7").setFormula("='Revenue Model'!B13-B6"); // Gross profit
  sheetCost.getRange("B8:M8").setFormula("=IF('Revenue Model'!B13>0, B7/'Revenue Model'!B13, 0)"); // GM%
  
  // S&M formulas
  sheetCost.getRange("B10:M10").setFormula("=Assumptions!$C$22"); // Ad spend
  sheetCost.getRange("B11:M11").setFormula("=Assumptions!$C$23"); // Tools
  sheetCost.getRange("B12:M12").setFormula("=Assumptions!$C$24"); // Content
  sheetCost.getRange("B13:M13").setFormula("=Assumptions!$C$25"); // Sales salaries
  sheetCost.getRange("B14:M14").setFormula("=SUM(B10:B13)"); // Total S&M
  sheetCost.getRange("B15:M15").setFormula("=IF('Revenue Model'!B3>0, B14/'Revenue Model'!B3, 0)"); // CAC
  
  // R&D formulas
  sheetCost.getRange("B18:M18").setFormula("=Assumptions!$C$28"); // Dev salaries
  sheetCost.getRange("B19:M19").setFormula("=Assumptions!$C$29"); // Tools
  sheetCost.getRange("B20:M20").setFormula("=SUM(B18:B19)"); // Total R&D
  
  // G&A formulas
  sheetCost.getRange("B23:M23").setFormula("=Assumptions!$C$32"); // Legal
  sheetCost.getRange("B24:M24").setFormula("=Assumptions!$C$33"); // Insurance
  sheetCost.getRange("B25:M25").setFormula("=Assumptions!$C$34"); // Office
  sheetCost.getRange("B26:M26").setFormula("=SUM(B23:B25)"); // Total G&A
  
  // Total costs
  sheetCost.getRange("B29:M29").setFormula("=B14+B20+B26"); // Total OpEx
  sheetCost.getRange("B30:M30").setFormula("=B6+B29"); // Total costs
  
  // Format cost tab
  sheetCost.setColumnWidth(1, 250);
  sheetCost.getRange("B3:M7").setNumberFormat("$#,##0");
  sheetCost.getRange("B8:M8").setNumberFormat("0%");
  sheetCost.getRange("B10:M15").setNumberFormat("$#,##0");
  sheetCost.getRange("B18:M20").setNumberFormat("$#,##0");
  sheetCost.getRange("B23:M26").setNumberFormat("$#,##0");
  sheetCost.getRange("B29:M30").setNumberFormat("$#,##0");
  
  // ============================================================
  // 5. CREATE P&L TAB
  // ============================================================
  var sheetPL = ss.getSheetByName("P&L") || ss.insertSheet("P&L");
  sheetPL.clear();
  sheetPL.getRange(1, 1, 1, 13).setValues([headers]).setFontWeight("bold").setBackground("#434343").setFontColor("white");
  
  var plLabels = [
    ["📊 PROFIT & LOSS STATEMENT"],
    ["Total Revenue"],
    ["Total COGS"],
    ["Gross Profit"],
    ["Gross Margin %"],
    [""],
    ["Operating Expenses"],
    ["Total OpEx"],
    ["EBITDA"],
    ["EBITDA Margin %"],
    [""],
    ["💰 CASH FLOW"],
    ["Starting Cash Balance"],
    ["+ Cash In (Revenue)"],
    ["- Cash Out (Costs)"],
    ["+ Funding Received"],
    ["= Ending Cash Balance"],
    [""],
    ["📉 BURN & RUNWAY"],
    ["Monthly Burn Rate"],
    ["Runway (Months)"],
    ["Break-Even Status"]
  ];
  sheetPL.getRange(2, 1, plLabels.length, 1).setValues(plLabels);
  sheetPL.getRange("A2").setFontWeight("bold").setBackground("#d9ead3");
  sheetPL.getRange("A12").setFontWeight("bold").setBackground("#d9ead3");
  sheetPL.getRange("A19").setFontWeight("bold").setBackground("#d9ead3");
  
  // P&L formulas
  sheetPL.getRange("B3:M3").setFormula("='Revenue Model'!B13"); // Revenue
  sheetPL.getRange("B4:M4").setFormula("='Cost Model'!B6"); // COGS
  sheetPL.getRange("B5:M5").setFormula("=B3-B4"); // Gross profit
  sheetPL.getRange("B6:M6").setFormula("=IF(B3>0, B5/B3, 0)"); // GM%
  
  sheetPL.getRange("B8:M8").setFormula("='Cost Model'!B29"); // OpEx
  sheetPL.getRange("B9:M9").setFormula("=B5-B8"); // EBITDA
  sheetPL.getRange("B10:M10").setFormula("=IF(B3>0, B9/B3, 0)"); // EBITDA margin
  
  // Cash flow - Month 1
  sheetPL.getRange("B13").setFormula("=Assumptions!$C$37"); // Starting cash
  sheetPL.getRange("B14").setFormula("=B3"); // Cash in
  sheetPL.getRange("B15").setFormula("='Cost Model'!B30"); // Cash out
  sheetPL.getRange("B16").setFormula("=IF(B1=Assumptions!$C$39, Assumptions!$C$38, 0)"); // Funding
  sheetPL.getRange("B17").setFormula("=B13+B14-B15+B16"); // Ending cash
  
  // Cash flow - Month 2-12
  for (var col = 3; col <= 13; col++) {
    var colLetter = String.fromCharCode(64 + col);
    var prevCol = String.fromCharCode(64 + col - 1);
    sheetPL.getRange(colLetter + "13").setFormula("=" + prevCol + "17"); // Starting = prev ending
    sheetPL.getRange(colLetter + "14").setFormula("=" + colLetter + "3");
    sheetPL.getRange(colLetter + "15").setFormula("='Cost Model'!" + colLetter + "30");
    sheetPL.getRange(colLetter + "16").setFormula("=IF(" + colLetter + "1=Assumptions!$C$39, Assumptions!$C$38, 0)");
    sheetPL.getRange(colLetter + "17").setFormula("=" + colLetter + "13+" + colLetter + "14-" + colLetter + "15+" + colLetter + "16");
  }
  
  // Burn & runway
  sheetPL.getRange("B20:M20").setFormula("=B15-B14"); // Burn rate
  sheetPL.getRange("B21:M21").setFormula("=IF(B20>0, B17/B20, 999)"); // Runway
  sheetPL.getRange("B22:M22").setFormula("=IF(B9>=0, \"✓ Profitable\", \"✗ Burning Cash\")"); // Status
  
  // Format P&L
  sheetPL.setColumnWidth(1, 250);
  sheetPL.getRange("B3:M5").setNumberFormat("$#,##0");
  sheetPL.getRange("B6:M6").setNumberFormat("0%");
  sheetPL.getRange("B8:M10").setNumberFormat("$#,##0");
  sheetPL.getRange("B10:M10").setNumberFormat("0%");
  sheetPL.getRange("B13:M17").setNumberFormat("$#,##0");
  sheetPL.getRange("B20:M21").setNumberFormat("$#,##0");
  sheetPL.getRange("B21:M21").setNumberFormat("0.0");
  
  // Conditional formatting for cash balance (red if low)
  var cashRule = SpreadsheetApp.newConditionalFormatRule()
    .whenNumberLessThan(5000)
    .setBackground("#f4cccc")
    .setRanges([sheetPL.getRange("B17:M17")])
    .build();
  var rules = sheetPL.getConditionalFormatRules();
  rules.push(cashRule);
  sheetPL.setConditionalFormatRules(rules);
  
  // ============================================================
  // 6. CREATE DASHBOARD TAB
  // ============================================================
  var sheetDash = ss.getSheetByName("Dashboard") || ss.insertSheet("Dashboard");
  sheetDash.clear();
  
  sheetDash.getRange("A1").setValue("📊 FINANCIAL DASHBOARD").setFontWeight("bold").setFontSize(18);
  sheetDash.getRange("A2").setValue("12-Month Summary").setFontSize(12);
  
  // Key metrics summary
  sheetDash.getRange("A4").setValue("💰 KEY METRICS (Month 12)").setFontWeight("bold").setFontSize(14).setBackground("#d9ead3");
  
  var dashLabels = [
    [""],
    ["Monthly Recurring Revenue (MRR)"],
    ["Total Customers"],
    ["Revenue Growth (M1→M12)"],
    [""],
    ["CAC (Customer Acq Cost)"],
    ["ARPU (Avg Revenue Per User)"],
    ["LTV (Lifetime Value)"],
    ["LTV:CAC Ratio"],
    ["Payback Period (months)"],
    [""],
    ["Gross Margin %"],
    ["Monthly Burn Rate"],
    ["Cash Runway (months)"],
    ["Ending Cash Balance"],
    [""],
    ["Break-Even Month"]
  ];
  sheetDash.getRange("A5:A21").setValues(dashLabels);
  
  // Dashboard formulas
  sheetDash.getRange("B6").setFormula("='Revenue Model'!M11"); // MRR
  sheetDash.getRange("B7").setFormula("='Revenue Model'!M6"); // Customers
  sheetDash.getRange("B8").setFormula("=('Revenue Model'!M13/'Revenue Model'!B13)-1"); // Growth
  
  sheetDash.getRange("B10").setFormula("='Cost Model'!M15"); // CAC
  sheetDash.getRange("B11").setFormula("='Revenue Model'!M18"); // ARPU
  sheetDash.getRange("B12").setFormula("=(B11*'Cost Model'!M8)/Assumptions!$C$13"); // LTV
  sheetDash.getRange("B13").setFormula("=B12/B10"); // LTV:CAC
  sheetDash.getRange("B14").setFormula("=B10/(B11*'Cost Model'!M8)"); // Payback
  
  sheetDash.getRange("B16").setFormula("='Cost Model'!M8"); // GM%
  sheetDash.getRange("B17").setFormula("='P&L'!M20"); // Burn
  sheetDash.getRange("B18").setFormula("='P&L'!M21"); // Runway
  sheetDash.getRange("B19").setFormula("='P&L'!M17"); // Cash
  
  sheetDash.getRange("B21").setFormula("=IFERROR(MATCH(TRUE, 'P&L'!B9:M9>=0, 0), \"Not Yet\")"); // Break-even
  
  // Format dashboard
  sheetDash.setColumnWidth(1, 300);
  sheetDash.setColumnWidth(2, 150);
  sheetDash.getRange("B6:B19").setNumberFormat("$#,##0");
  sheetDash.getRange("B8").setNumberFormat("0%");
  sheetDash.getRange("B13:B14").setNumberFormat("0.0");
  sheetDash.getRange("B16").setNumberFormat("0%");
  
  // Health indicators
  sheetDash.getRange("A23").setValue("🎯 UNIT ECONOMICS HEALTH CHECK").setFontWeight("bold").setFontSize(14).setBackground("#d9ead3");
  sheetDash.getRange("A24").setValue("LTV:CAC Ratio (Target: >3:1)");
  sheetDash.getRange("B24").setFormula("=IF(B13>=3, \"✓ Healthy\", \"✗ Needs Work\")");
  sheetDash.getRange("A25").setValue("Payback Period (Target: <12 months)");
  sheetDash.getRange("B25").setFormula("=IF(B14<=12, \"✓ Healthy\", \"✗ Needs Work\")");
  sheetDash.getRange("A26").setValue("Gross Margin (Target: >70%)");
  sheetDash.getRange("B26").setFormula("=IF(B16>=0.7, \"✓ Healthy\", \"✗ Needs Work\")");
  sheetDash.getRange("A27").setValue("Cash Runway (Target: >6 months)");
  sheetDash.getRange("B27").setFormula("=IF(B18>6, \"✓ Healthy\", \"✗ Needs Work\")");
  
  SpreadsheetApp.flush();
  SpreadsheetApp.getUi().alert("✅ Financial Model Created Successfully!\\n\\nNext steps:\\n1. Go to 'Assumptions' tab\\n2. Update blue cells with your team's actual numbers\\n3. Check 'Dashboard' for results\\n\\nAll done!");
}
```

---

### Step 4: Paste and Run the Script

1. **Paste the entire script** into the Apps Script editor
2. Click the **💾 Save** icon (or press Ctrl+S / Cmd+S)
3. Name your project: `Financial Model Builder`
4. Click the **▶️ Run** button at the top

---

### Step 5: Grant Permissions

**First time running:**
1. You'll see: "Authorization required"
2. Click **Review Permissions**
3. Choose your Google account
4. Click **Advanced** → **Go to Financial Model Builder (unsafe)**
5. Click **Allow**

**Why "unsafe"?** It's your own code! Google shows this for any custom script.

---

### Step 6: Wait for Build (30-60 seconds)

The script will:
- ✅ Create 6 tabs (Instructions, Assumptions, Revenue Model, Cost Model, P&L, Dashboard)
- ✅ Add all formulas automatically
- ✅ Format everything professionally
- ✅ Set up conditional formatting

You'll see: **"✅ Financial Model Created Successfully!"**

---

## ✅ Step 7: Customize Your Assumptions

**Now update the blue cells in the Assumptions tab with YOUR actual numbers:**

### 💰 Pricing Section (Rows 3-5)
- **Monthly Subscription Price:** Your actual price (from unit economics)
- **Annual Discount:** If you offer yearly plans at a discount

### 📈 Growth Section (Rows 7-10)
- **Starting Customers:** How many you have now
- **Monthly Growth Rate:** From your projections (e.g., 0.20 = 20%)
- **When Growth Slows:** Pick a month when growth rate cuts in half

### 📉 Churn Section (Rows 12-14)
- **Monthly Churn Rate:** From your LTV calculation (e.g., 0.05 = 5%)
- **When Churn Starts:** Month when customers start churning (usually Month 2)

### 💸 Costs Sections (Rows 16-34)
- **Hosting, COGS, Marketing, Development, Admin:** Your actual costs
- **This is where your CAC calculation components go!**

**Example from your unit economics:**
- If your CAC is $200 with $500 ad spend for 10 customers
- Set "Monthly Ad Spend" to $500
- Model will calculate CAC automatically

### 💰 Funding Section (Rows 36-39)
- **Starting Cash:** What you have now
- **Funding to Raise:** How much you're seeking
- **Funding Month:** When you expect it to arrive

---

## 🎯 Step 8: Review Your Model

### Check the Dashboard Tab:

**It should show:**
- ✅ Your MRR projections for 12 months
- ✅ Customer count growth
- ✅ CAC calculated from your S&M spend
- ✅ LTV calculated from your assumptions
- ✅ LTV:CAC ratio (target: >3:1)
- ✅ Payback period (target: <12 months)
- ✅ Cash runway
- ✅ Health check indicators

**Do the numbers look right?**
- If LTV:CAC ratio is green (✓ Healthy), you're good!
- If red (✗ Needs Work), adjust your assumptions

---

## 💾 Step 9: Save and Submit

### Save Your Model:

1. **File → Make a copy** to create versions:
   - `[TeamName]-Financial-Model-Pessimistic`
   - `[TeamName]-Financial-Model-Base`
   - `[TeamName]-Financial-Model-Optimistic`

2. **Get shareable link:**
   - Click **Share** → **Change to Anyone with the link**
   - Copy the link

### Submit to GitHub:

Create file: `/04-gtm/financials/12-month-model-link.md`

```markdown
# 12-Month Financial Model

**Team:** [Your Team Name]  
**Date:** December 5, 2025

## Google Sheets Link

[View Financial Model](https://docs.google.com/spreadsheets/d/YOUR_SHEET_ID_HERE)

## Model Summary

- **Starting MRR:** $______
- **Month 12 MRR:** $______
- **CAC:** $______
- **LTV:** $______
- **LTV:CAC Ratio:** ___:1
- **Cash Runway:** ___ months

## Versions

- **Base Case:** [Link]
- **Pessimistic:** [Link]
- **Optimistic:** [Link]

## Notes

[Any assumptions or important notes about your model]
```

---

## 🔧 Troubleshooting

### "I see #REF! or #DIV/0! errors"

**Fix:** Go to Assumptions tab and make sure all blue cells have numbers (not blank)

### "My CAC is $0 or wrong"

**Fix:** 
- Check "Monthly Ad Spend" and other S&M costs in Assumptions
- Make sure "New Customers Acquired" is >0 in Revenue Model
- CAC = Total S&M / New Customers

### "My LTV seems too high/low"

**Fix:**
- Check your churn rate (C13 in Assumptions)
- Verify ARPU is correct (C4 in Assumptions)
- LTV = (ARPU × Gross Margin%) / Churn Rate

### "Formulas broke when I edited something"

**Fix:**
- Don't edit BLACK cells (formulas)
- Only edit BLUE cells (inputs)
- If broken, re-run the script to rebuild

### "The model doesn't match my unit economics"

**Check:**
- Is your "Monthly Subscription Price" correct?
- Are your S&M costs accurate?
- Is your churn rate from your LTV calculation entered?

---

## 📊 Using Your Model for Lab 9 Deliverables

### From This Model, You Can Now:

✅ **Complete Unit Economics Analysis**
- CAC: From Dashboard (pulls from your S&M costs)
- LTV: From Dashboard (uses your churn rate)
- Ratios: All calculated automatically

✅ **Show 12-Month Projections**
- Revenue growth: Revenue Model tab
- Cost scaling: Cost Model tab
- Cash flow: P&L tab

✅ **Calculate Burn & Runway**
- Monthly burn: P&L tab, row 20
- Runway: Dashboard, automatically calculated
- Break-even: Dashboard shows which month

✅ **Build Scenarios**
- Copy model 3 times
- Adjust assumptions for Pessimistic/Base/Optimistic
- Compare valuations based on different outcomes

---

## ✅ Quality Checks

**Before submitting, verify:**

- [ ] All blue cells in Assumptions filled with YOUR numbers
- [ ] Dashboard shows your actual CAC and LTV
- [ ] LTV:CAC ratio makes sense (ideally >3:1)
- [ ] Revenue grows month-over-month
- [ ] Costs scale with customer growth
- [ ] Cash balance tracked properly
- [ ] No #REF! or #DIV/0! errors
- [ ] Model connects to your unit economics work
- [ ] Link saved in GitHub

---

## 🎯 Key Differences from Generic Model

**Your custom model includes:**

1. **Your Unit Economics Built In**
   - CAC calculated from YOUR S&M spend
   - LTV calculated from YOUR churn rate
   - ARPU from YOUR pricing

2. **Dynamic Growth**
   - Fast growth early (Months 1-6)
   - Slowing growth later (Months 7-12)
   - Customizable growth rates

3. **Automatic Health Checks**
   - LTV:CAC ratio health indicator
   - Payback period assessment
   - Gross margin check
   - Runway warning

4. **Scenario Planning**
   - Easy to copy and adjust
   - All formulas stay linked
   - Compare different assumptions

---

## 💡 Pro Tips

### Make It Your Own:

1. **Add Your Logo:** Insert image in Instructions tab
2. **Color Code:** Use your brand colors for headers
3. **Add Notes:** Use Comments feature to explain assumptions
4. **Track Versions:** Name copies clearly (Date + Scenario)

### Advanced Customization:

**Want to add/change something?**
1. Go to Extensions → Apps Script
2. Find the section you want to modify
3. Update the values or add new rows
4. Save and re-run

**Common customizations:**
- Add more cost categories
- Change growth assumptions by month
- Add seasonal patterns
- Include equity/dilution tracking

---

## 🆘 Getting Help

**If you're stuck:**

1. **Check the original template** (`lab-9-template-financial-model-structure.md`) for guidance
2. **Review your unit economics** to make sure inputs are correct
3. **Ask during lab** or office hours (Tuesdays 2-4 PM)
4. **Email:** zeshan.ahmad@kiu.edu.ge with your Google Sheets link

---

## 📚 What You've Built

**Congratulations! You now have:**

✅ Automated 12-month financial projection  
✅ Unit economics calculator (CAC, LTV, ratios)  
✅ P&L statement with cash flow  
✅ Professional dashboard with health checks  
✅ Scenario planning capability  
✅ Investor-ready financial model  

**This feeds into:**
- Your valuation calculation (Week 11)
- Your pitch deck (Week 12)
- Your investor data room
- Your final capstone project

---

## 🎓 Learning Objectives Met

By completing this exercise, you've:

✅ Applied your unit economics to a complete financial model  
✅ Learned to automate complex spreadsheets with code  
✅ Built projections based on realistic assumptions  
✅ Created scenario analyses for different outcomes  
✅ Developed investor-grade financial materials  

---

**Ready to go? Start with Step 1 and build your model! 🚀**

---

**Questions?** See you in lab tomorrow!
