# Basic Stock Portfolio

## Overview

This project is a back-end implementation for a stock portfolio management system, enabling users to track stocks, calculate returns, and analyze investment performance.

## Features

- View and add stocks to a portfolio
- Automatically generate market price and purchase price
- Calculate stock returns and return percentage
- Determine profit or loss status
- Compute cumulative portfolio performance

## Demo

### Live Preview
- **StackBlitz:** [Live Demo](https://stackblitz.com/edit/stackblitz-starters-3ehxqx?file=index.js)
- **Vercel Deployment:** [Live Site](https://basic-stock-portfolio-akshay-v1.vercel.app/)

---
### Video Demo
<div>
    <a href="https://www.loom.com/share/0a649aa27e20464897026167441abfce">
      <p>Basic-Stock-Portfolio-Live-DemoVideo - Watch Video</p>
    </a>
    <a href="https://www.loom.com/share/0a649aa27e20464897026167441abfce">
      <img style="max-width:300px;" src="https://cdn.loom.com/sessions/thumbnails/0a649aa27e20464897026167441abfce-695b2180d9509ce0-full-play.gif">
    </a>
  </div>

---

## API Endpoints

### Portfolio Management

#### Calculate Stock Returns
**GET** `/stocks/returns?boughtAt={price}&marketPrice={price}&quantity={qty}`
- Returns the total return value for a stock.
- **Example Call:** `/stocks/returns?boughtAt=300&marketPrice=400&quantity=2`
- **Expected Output:** `200`

#### Calculate Total Portfolio Returns
**GET** `/portfolio/total-returns?stock1={value}&stock2={value}&stock3={value}&stock4={value}`
- Computes the total return from all stocks.
- **Example Call:** `/portfolio/total-returns?stock1=100&stock2=200&stock3=200&stock4=400`
- **Expected Output:** `900`

#### Calculate Return Percentage
**GET** `/stocks/return-percentage?boughtAt={price}&returns={value}`
- Calculates the return percentage of a stock.
- **Example Call:** `/stocks/return-percentage?boughtAt=400&returns=200`
- **Expected Output:** `50`

#### Calculate Total Portfolio Return Percentage
**GET** `/portfolio/total-return-percentage?stock1={value}&stock2={value}&stock3={value}&stock4={value}`
- Computes the total return percentage across all stocks.
- **Example Call:** `/portfolio/total-return-percentage?stock1=10&stock2=20&stock3=20&stock4=40`
- **Expected Output:** `90`

#### Determine Stock Status (Profit/Loss)
**GET** `/stocks/status?returnPercentage={value}`
- Identifies whether a stock is in **Profit** or **Loss**.
- **Example Call:** `/stocks/status?returnPercentage=90`
- **Expected Output:** `profit`

## Deployment

To deploy, follow these steps:

1. Deploy your backend to Vercel or another hosting provider.
2. Copy the deployed URL.
3. Configure the frontend to use this backend by updating the API base URL in the frontend settings.

## Installation & Setup

1. Clone the repository:
   ```sh
   git clone https://github.com/AkshAI-2030/Basic-Stock-Portfolio.git
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Start the server:
   ```sh
   node index.js
   ```

## Tech Stack

- Node.js
- Express.js
- CORS

## License

This project is licensed under the MIT License.

