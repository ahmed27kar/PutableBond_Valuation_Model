# AI-Assisted Valuation of Putable Corporate Bonds

## Project Overview
This project values a **7-Year Putable Bond** (3% Coupon) using a **Vasicek stochastic model**. It simulates the investor's protection against rising interest rates.

## 1. Modeling Assumptions
* **Bond Structure:** Face Value $1000, 3% Coupon, Putable at Par ($1000) after Year 3.
* **Valuation Logic:** Backward Induction using `max(Hold_Value, Put_Price)`.

## 2. Market Scenarios
### Scenario A: "Inflation Shock" (Rates Rise)
* **Narrative:** Rates drift to 10%.
* **Outcome:** The Put Option is **Deep in the Money**. The bond price is floored at $1,000, protecting the investor.

### Scenario B: "Deflationary Trap" (Rates Fall)
* **Narrative:** Rates drop to 1%.
* **Outcome:** The Put Option is **Out of the Money**. The bond appreciates naturally.

## 3. AI Usage
* **GitHub:** Used for version control and independent data creation.
* **AI Tools:** Used to assist in inverting the pricing logic from Callable (min) to Putable (max).
