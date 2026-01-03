# ============================================================================
# COMPLETE SETUP GUIDE - GitHub & Google Drive
# ============================================================================

import os

print("=" * 80)
print("ASSIGNMENT SUBMISSION SETUP GUIDE")
print("=" * 80)

# ============================================================================
# STEP 1: ORGANIZE YOUR FILES
# ============================================================================

print("\n" + "=" * 80)
print("STEP 1: FILE ORGANIZATION")
print("=" * 80)

print("""
📁 YOUR LOCAL FOLDER STRUCTURE:

ds_<your_name>/
├── README.md                      # Generated from script
├── notebook_1.ipynb              # Downloaded from Colab
├── notebook_2.ipynb              # Downloaded from Colab
├── ds_report.pdf                 # Your written report
├── .gitignore                    # See below
├── csv_files/                    # All CSV outputs
│   ├── merged_daily_data.csv
│   ├── sentiment_insights.csv
│   ├── trader_performance_by_sentiment.csv
│   └── README.md                 # Note about Drive location
└── outputs/                      # All visualizations
    ├── 01_sentiment_distribution.png
    ├── 02_volume_analysis.png
    ├── ... (all 11 PNG files)
    └── README.md                 # Note about Drive location
""")

# ============================================================================
# STEP 2: CREATE .gitignore
# ============================================================================

print("\n" + "=" * 80)
print("STEP 2: CREATE .gitignore FILE")
print("=" * 80)

gitignore_content = """# Data files (too large for GitHub)
csv_files/*.csv

# Image outputs (optional - can upload selectively)
outputs/*.png
outputs/*.jpg

# Python
__pycache__/
*.py[cod]
*$py.class
*.so
.Python
env/
venv/

# Jupyter Notebook
.ipynb_checkpoints

# macOS
.DS_Store

# Windows
Thumbs.db

# IDE
.vscode/
.idea/
"""

# Save .gitignore
with open('.gitignore', 'w') as f:
    f.write(gitignore_content)

print("✅ .gitignore file created!")
print("\nThis file tells Git to ignore large CSV and PNG files.")

# ============================================================================
# STEP 3: CREATE PLACEHOLDER READMEs
# ============================================================================

print("\n" + "=" * 80)
print("STEP 3: CREATE PLACEHOLDER READMEs FOR DATA FOLDERS")
print("=" * 80)

# CSV folder README
csv_readme = """# CSV Data Files

Due to file size limitations, CSV files are hosted on Google Drive.

## 📁 Access Data Files

**Google Drive Link:** [Add your Drive link here]

## 📋 Available Files

1. `merged_daily_data.csv` - Daily aggregated trading metrics with sentiment
2. `sentiment_insights.csv` - Summary statistics by sentiment category
3. `trader_performance_by_sentiment.csv` - Individual trader analysis

## 📊 File Descriptions

### merged_daily_data.csv
- **Rows:** 479 daily observations
- **Columns:** 16 features including PnL, volume, sentiment classification
- **Date Range:** December 2024

### sentiment_insights.csv
- **Rows:** 4 (one per sentiment category)
- **Metrics:** Average daily PnL, win rate, volume, traders, buy/sell ratio

### trader_performance_by_sentiment.csv
- **Rows:** Individual trader records grouped by sentiment
- **Columns:** Account, classification, total PnL, average PnL, trade count
"""

# Create csv_files folder if doesn't exist
os.makedirs('csv_files', exist_ok=True)
with open('csv_files/README.md', 'w') as f:
    f.write(csv_readme)

print("✅ csv_files/README.md created!")

# Outputs folder README
outputs_readme = """# Visualization Outputs

Due to file size, visualization files are hosted on Google Drive.

## 📁 Access Visualizations

**Google Drive Link:** [Add your Drive link here]

## 📊 Available Visualizations

### Core Analysis (Notebook 1)
1. `01_sentiment_distribution.png` - Market sentiment over time
2. `02_volume_analysis.png` - Trading volume by sentiment (4-panel)
3. `03_profitability_analysis.png` - PnL and win rates (4-panel)
4. `04_buy_sell_behavior.png` - Buy vs Sell patterns
5. `05_correlation_matrix.png` - Correlation heatmap
6. `06_sentiment_vs_pnl.png` - Sentiment value vs performance

### Advanced Analysis (Notebook 2)
7. `07_sharpe_ratio.png` - Risk-adjusted returns
8. `08_volatility_analysis.png` - Volatility metrics
9. `09_momentum_analysis.png` - Moving averages and trends
10. `10_sentiment_transitions.png` - Transition day analysis
11. `11_extreme_sentiment.png` - Extreme fear vs greed

## 📐 Specifications
- **Format:** PNG
- **Resolution:** 300 DPI
- **Style:** Professional with consistent color schemes
"""

# Create outputs folder if doesn't exist
os.makedirs('outputs', exist_ok=True)
with open('outputs/README.md', 'w') as f:
    f.write(outputs_readme)

print("✅ outputs/README.md created!")

# ============================================================================
# STEP 4: GITHUB SETUP COMMANDS
# ============================================================================

print("\n" + "=" * 80)
print("STEP 4: GITHUB SETUP COMMANDS")
print("=" * 80)

github_commands = """
# Navigate to your project folder
cd ds_<your_name>

# Initialize Git repository
git init

# Add all files (respects .gitignore)
git add .

# Create initial commit
git commit -m "Initial commit: Trader behavior vs sentiment analysis"

# Create GitHub repo (do this on github.com first!)
# Recommended repo name: ds-trader-sentiment-analysis

# Add remote (replace with your actual repo URL)
git remote add origin https://github.com/yourusername/ds-trader-sentiment-analysis.git

# Push to GitHub
git branch -M main
git push -u origin main
"""

print("🔧 Run these commands in your terminal:")
print(github_commands)

# ============================================================================
# STEP 5: GOOGLE DRIVE SETUP
# ============================================================================

print("\n" + "=" * 80)
print("STEP 5: GOOGLE DRIVE SETUP")
print("=" * 80)

print("""
📁 GOOGLE DRIVE ORGANIZATION:

1. Create a folder: "ds_<your_name>_submission"

2. Upload these folders:
   ├── csv_files/          (with all 3 CSV files)
   └── outputs/            (with all 11 PNG files)

3. Set sharing permissions:
   - Right-click folder → Share
   - Change to "Anyone with the link can view"
   - Copy the link

4. Update your README.md with the Drive links

5. (OPTIONAL) You can also share the complete folder including notebooks
""")

# ============================================================================
# STEP 6: UPDATE README WITH LINKS
# ============================================================================

print("\n" + "=" * 80)
print("STEP 6: UPDATE README WITH YOUR LINKS")
print("=" * 80)

readme_links_section = """
# Add this section to your README.md

## 🔗 Important Links

### GitHub Repository
- **Code & Documentation:** https://github.com/yourusername/ds-trader-sentiment-analysis

### Google Colab Notebooks
- **Notebook 1 (Main Analysis):** https://colab.research.google.com/drive/YOUR_LINK_1
- **Notebook 2 (Advanced Analysis):** https://colab.research.google.com/drive/YOUR_LINK_2

### Google Drive (Data & Outputs)
- **CSV Files:** https://drive.google.com/drive/folders/YOUR_CSV_FOLDER_ID
- **Visualizations:** https://drive.google.com/drive/folders/YOUR_OUTPUTS_FOLDER_ID
- **Complete Submission:** https://drive.google.com/drive/folders/YOUR_COMPLETE_FOLDER_ID

*All links are set to "Anyone with the link can view"*
"""

print(readme_links_section)

# ============================================================================
# STEP 7: FINAL CHECKLIST
# ============================================================================

print("\n" + "=" * 80)
print("STEP 7: FINAL SUBMISSION CHECKLIST")
print("=" * 80)

checklist = """
BEFORE SUBMITTING:

GitHub:
□ Repository created with clear name
□ README.md includes all sections
□ notebook_1.ipynb uploaded
□ notebook_2.ipynb uploaded
□ ds_report.pdf uploaded
□ .gitignore file present
□ Placeholder READMEs in csv_files/ and outputs/
□ Repository is PUBLIC

Google Drive:
□ Folder created and organized
□ All CSV files uploaded
□ All PNG files uploaded
□ Folder permissions set to "Anyone with the link can view"
□ Links tested and working

Google Colab:
□ Notebook 1 shared with "Anyone with the link can view"
□ Notebook 2 shared with "Anyone with the link can view"
□ Both notebooks run successfully end-to-end

Documentation:
□ README.md has all your actual links (not placeholders)
□ ds_report.pdf is complete and professional
□ All links in README.md are tested and working
□ Folder structure matches requirements exactly

Email:
□ Resume attached
□ GitHub link included
□ Email subject: "Junior Data Scientist – Trader Behavior Insights"
□ Sent to: saami@bajarangs.com, nagasai@bajarangs.com, chetan@bajarangs.com
□ CC: sonika@primetrade.ai
"""

print(checklist)

# ============================================================================
# STEP 8: RECOMMENDED REPO NAME
# ============================================================================

print("\n" + "=" * 80)
print("STEP 8: RECOMMENDED REPOSITORY NAME")
print("=" * 80)

print("""
🎯 RECOMMENDED GITHUB REPO NAMES (pick one):

1. ds-trader-sentiment-analysis        ⭐ BEST
2. web3-trading-behavior-analysis
3. crypto-sentiment-trading-study
4. ds-<your_name>-web3-trading
5. hyperliquid-trader-analysis

✅ Name should be:
- All lowercase
- Use hyphens (not underscores)
- Descriptive and professional
- Easy to remember

❌ Avoid:
- "assignment", "homework", "test"
- Generic names like "data-science-project"
- Numbers like "project1", "ds-assignment-2"
""")

print("\n" + "=" * 80)
print("✅ SETUP GUIDE COMPLETE!")
print("=" * 80)
print("\nFollow each step carefully and you'll have a perfect submission!")
print("Good luck with your application! 🚀")
print("=" * 80)
