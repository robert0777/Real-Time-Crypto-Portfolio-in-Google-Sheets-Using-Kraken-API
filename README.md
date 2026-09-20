# Real-Time Crypto Portfolio in Google Sheets Using Kraken API

Automate your cryptocurrency portfolio tracking — fetch live market data from the Kraken API directly into Google Sheets using Google Apps Script. Build a self-updating dashboard with prices, allocation, profit/loss, and risk metrics.

## 📄 About This Project

This repository contains the JavaScript code referenced in the Medium article:

**[How to Build a Real-Time Crypto Portfolio in Google Sheets Using Kraken API](https://chomchom216.medium.com/how-to-build-a-real-time-crypto-portfolio-in-google-sheets-using-kraken-api-ea7351e18935)**

The article explains, step by step, how to connect to the Kraken public API, retrieve cryptocurrency OHLC (Open, High, Low, Close) data, and automatically populate a Google Sheets spreadsheet. This repository provides ready-to-use scripts for over a dozen crypto and fiat assets, so you can implement the solution immediately.

> **Problem:** Manual tracking is tedious, error-prone, and lacks real-time insight.  
> **Solution:** Automate everything with Google Sheets, Kraken API, and a bit of Google Apps Script magic.  
> **Expectation:** By the end, you'll have a live, auto-updating portfolio tracker.

## 📁 Repository Contents

All scripts are located in the folder [`JavaScript code to fetch data`](https://github.com/robert0777/Real-Time-Crypto-Portfolio-in-Google-Sheets-Using-Kraken-API/tree/main/JavaScript%20code%20to%20fetch%20data).

Each `.txt` file contains a complete Google Apps Script function ready to be copied into your Apps Script project. The following data series are included:

| Script File | Data Series | Description |
|-------------|-------------|-------------|
| `Bitcoin.txt` | Bitcoin (BTC/USD) | Daily OHLC data for Bitcoin |
| `Ethereum.txt` | Ethereum (ETH/USD) | Daily OHLC data for Ethereum |
| `Cardano.txt` | Cardano (ADA/USD) | Daily OHLC data for Cardano |
| `Doge.txt` | Dogecoin (DOGE/USD) | Daily OHLC data for Dogecoin |
| `Litecoin.txt` | Litecoin (LTC/USD) | Daily OHLC data for Litecoin |
| `Ripple.txt` | Ripple (XRP/USD) | Daily OHLC data for Ripple |
| `Shiba Inu.txt` | Shiba Inu (SHIB/USD) | Daily OHLC data for Shiba Inu |
| `Tether.txt` | Tether (USDT/USD) | Daily OHLC data for Tether |
| `Dai.txt` | Dai (DAI/USD) | Daily OHLC data for Dai |
| `Binance USD.txt` | Binance USD (BUSD/USD) | Daily OHLC data for Binance USD |
| `PayPal.txt` | PayPal (PYPL) | Daily OHLC data for PayPal |
| `Mexican Peso USD.txt` | MXN/USD | Daily exchange rate for Mexican Peso |
| `Kraken Crypto Currencies.txt` | Crypto list | Fetches the list of available Kraken currency pairs |
| `Import All Crypto Currencies.txt` | **All series** | Master script that fetches all the above series in one execution |
| `On Open Menu.txt` | — | Custom menu that adds a "Crypto Data" menu to Google Sheets for manual refreshes |

## 🚀 Getting Started

### Prerequisites

1. A **Google Account** with access to Google Sheets.
2. A **Kraken API key** (free, no trading required). You can obtain one here: [Kraken API Documentation](https://docs.kraken.com/api/)
3. Basic familiarity with **Google Apps Script** (the article covers this).

### Installation & Usage

1. **Open your Google Sheets** spreadsheet.
2. Go to **Extensions → Apps Script**.
3. **Copy the content** of one of the `.txt` files from this repository into the Apps Script editor (or use `Import All Crypto Currencies.txt` for all series).
4. **Run the function** (e.g., `importKrakenData`) from the Apps Script editor.
5. The script will create a new sheet in your spreadsheet with the downloaded data.

> **Note:** The scripts use the Kraken public API, which does not require an API key for market data. However, if you plan to access private endpoints (e.g., account balances), you will need a Kraken API key.

### Scheduling Automatic Refreshes

You can set a **time-driven trigger** in Apps Script to run the import function automatically (e.g., daily or hourly):

1. In the Apps Script editor, click the **Triggers** icon (clock icon) on the left panel.
2. Click **Add Trigger**.
3. Select your import function, choose **Time-driven**, and set the desired frequency.

### Custom Menu

The `On Open Menu.txt` script creates a custom menu in your Google Sheets. Copy its content into your Apps Script project and uncomment the `onOpen()` function to add a "Crypto Data" menu with buttons to run the imports manually.

## 🔗 Related Article

This repository is the companion code for the Medium article:

**[How to Build a Real-Time Crypto Portfolio in Google Sheets Using Kraken API](https://chomchom216.medium.com/how-to-build-a-real-time-crypto-portfolio-in-google-sheets-using-kraken-api-ea7351e18935)**

The article provides:
- A conceptual introduction to the Kraken API and real-time portfolio tracking.
- Step-by-step instructions to set up your Google Sheet structure (Dashboard, Holdings, API Data, Calculations, Log).
- Detailed explanation of the JavaScript code.
- Instructions for building risk & return metrics (volatility, covariance, VaR).
- Instructions for scheduling automatic refreshes and visualizing your portfolio.

## ⚠️ Important Notes

- **API Rate Limits:** The Kraken public API has rate limits. The scripts include a `Utilities.sleep(2000)` delay to prevent rate limiting. Adjust if needed.
- **Data Formatting:** The scripts convert Unix timestamps to dates and format price values as currency. You may need to adjust formatting depending on your locale.
- **Pair Names:** Each script uses a specific Kraken pair (e.g., `XBTUSD` for Bitcoin). If you want to fetch a different pair, look up its name in the [Kraken API documentation](https://docs.kraken.com/api/docs/rest-api/get-ohlc-data) and update the script accordingly.
- **Terms of Use:** Respect Kraken's terms of service and API usage limits.

## 👤 Author

**Dr. Robert Hernández Martínez**  
*Consultant in Actuarial Science, Finance, Risk Modeling, and Applied AI*

* 📝 [Articles on Medium](https://chomchom216.medium.com/)
* 🎓 [Academic Publications](https://unam1.academia.edu/Robert_Hernandez_Martinez)
* 🏆 [Credentials on Credly](https://www.credly.com/users/robert-hernandez.89bffe7b)
* 🐙 [GitHub Profile](https://github.com/robert0777)
* 📧 Email: [robert@actuariayfinanzas.net](mailto:robert@actuariayfinanzas.net)

## 📜 License

This project is provided for educational and professional use. Please refer to the original article and Kraken's API terms for usage guidelines.