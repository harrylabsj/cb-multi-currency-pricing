---
name: Multi-currency Pricing Strategist
description: Dynamic pricing strategies across currencies and markets for cross-border e-commerce
version: 1.1.0
type: descriptive
language: en
author: Harry (code agent)
category: cross-border-ecommerce
slug: cb-multi-currency-pricing
tags: [cross-border, currency-management, pricing-strategy, forex]
---

# Multi-currency Pricing Strategist

## Overview

Dynamic pricing strategies across currencies and markets for cross-border e-commerce. Calculates PPP-adjusted local prices, provides competitive positioning analysis, currency risk assessment, and pricing strategy frameworks. Pure descriptive skill. No code execution, API calls, or network access.

## Trigger Keywords

Use this skill when the user mentions or asks about:
- multi-currency pricing for international markets
- price products in different currencies (EUR, GBP, JPY, AUD, etc.)
- pricing strategy for Germany, Japan, UK, Australia, Brazil, India
- exchange rate and currency risk management
- competitive pricing in international markets

### Primary Triggers
- "multi-currency pricing for my electronics product at $100 for Germany Japan and Australia"
- "help me price my apparel at $50 for UK Canada and Brazil"
- "how should I price products in multiple currencies premium strategy"

## Workflow

1. Receive input — Parse base USD price, target markets, product category, strategy focus (premium/competitive/balanced)
2. Calculate prices — Apply PPP adjustment, currency conversion, margin based on volatility and price sensitivity
3. Strategy framework — Build pricing strategy based on stated focus
4. Risk assessment — Provide currency risk by market with volatility levels and review frequency
5. Competitive positioning — Compare against local market equivalents

## Input Format

Accepts natural language or structured JSON describing base USD price, target markets, product category, and pricing strategy focus.

### Supported Markets

| Market | Currency | Code | PPP Index | Price Sensitivity | Volatility |
|--------|----------|------|-----------|-------------------|------------|
| Germany | Euro | EUR | 0.83 | Medium | Low |
| Japan | Japanese Yen | JPY | 102.0 | Low | Medium |
| United Kingdom | British Pound | GBP | 0.73 | Medium | Low |
| Australia | Australian Dollar | AUD | 1.44 | Medium-High | Medium |
| Canada | Canadian Dollar | CAD | 1.26 | Medium | Low |
| France | Euro | EUR | 0.83 | Medium | Low |
| Brazil | Brazilian Real | BRL | 2.85 | High | High |
| India | Indian Rupee | INR | 22.5 | High | High |
| South Korea | Korean Won | KRW | 850 | Medium-High | Medium |
| United States | US Dollar | USD | 1.0 | Low | Minimal |

## Reference Exchange Rates (USD Base)

Approximate rates for reference (verify current rates before use):
- USD/EUR: 0.92
- USD/GBP: 0.79
- USD/JPY: 149.5
- USD/AUD: 1.53
- USD/CAD: 1.36
- USD/BRL: 4.97
- USD/INR: 83.2
- USD/KRW: 1320
- USD/CHF: 0.88

## PPP Adjustment Methodology

Purchasing Power Parity (PPP) adjustment accounts for the relative cost of living across markets. Products that cost $100 USD may need to be priced differently in local currency to maintain equivalent real value for consumers and preserve margin health for sellers.

## Output Structure

Returns JSON with:
- multi_currency_pricing: per-market prices with currency, PPP-adjusted values, recommended retail, competitor comparison
- pricing_strategy_framework: strategy (premium/competitive/balanced) with adjustment factor and rationale
- currency_risk_management: per-market volatility, annual range, recommended review frequency
- competitive_positioning: local market equivalents and competition level analysis
- disclaimer: safety disclaimer

## Safety and Disclaimer

Descriptive guidance only. Not professional legal, tax, financial, or business advice. Currency exchange rates fluctuate. Verify current rates before setting prices. This provides frameworks, not guaranteed pricing.

## Examples

### Example 1: Electronics at $100 to Germany, Japan, Australia
Input: "multi-currency pricing for my electronics product at $100 for Germany Japan and Australia"
Output: EUR/GBP/JPY/AUD prices with PPP adjustments, margin based on currency volatility, pricing position vs local competitors, currency risk assessment.

### Example 2: Apparel at $50 Competitive Pricing
Input: "help me price my apparel at $50 for UK Canada and Brazil competitive pricing"
Output: Local currency prices with competitive adjustment, GBP/CAD/BRL amounts, risk-adjusted margins, competitive positioning vs local brands.


## Usage Scenarios

### Scenario 1

**User Input:** "Set up pricing for our $49 USD product across EUR, GBP, JPY, and AUD. I want to protect against 5% currency swings."

**Expected Output:** Price grid: €52.95 (5% buffer), £43.50, ¥6,980, A$78.00. Each includes the buffer calculation, rounded to local psychological price points, with a note on which gateway can settle in that currency.

### Scenario 2

**User Input:** "The JPY has weakened 8% against USD this quarter. Should I reprice or absorb the loss?"

**Expected Output:** Impact analysis: current margin erosion, competitor repricing behavior, customer price sensitivity in Japan. Recommendation: partial 3% increase with localized messaging, absorb remaining 5% short-term.

### Scenario 3

**User Input:** "Build a dynamic pricing rule set: if a currency moves more than 3% in 30 days, trigger a price review alert with the recommended adjustment."

**Expected Output:** Rule engine specification: monitored pairs, 3% threshold, 30-day rolling window, alert template with new suggested price, margin-impact calculation, and competitor-price re-check prompt.


### Scenario 4: 多币种定价换算太麻烦了
**User input:** "我们产品在亚马逊美国站卖$19.99，现在想上日本站和欧洲站。日元/欧元/英镑怎么定价格不亏？"
**Expected output:** 多币种定价策略——第一步：算基础价（人民币成本×目标利润率=美元出价，锁定美元基准价）；第二步：按购买力平价调价（日本用$19.99×110=¥2199而非按汇率直接换算¥2999，人均收入高的国家可以加价）；第三步：检查各平台的定价规则（亚马逊日本站习惯含税价格显示，欧洲站必须含VAT）；第四步：用定价工具自动化（SellerSprite/卖家精灵有自动汇率换算+竞品价格参考）；第五步：定期复盘（每月检查汇率变动>3%要及时调价，但不要频繁调价让客户困惑）。关键工具：AMZScout/XSellco的自动定价功能。

## Acceptance Criteria

- Calculates local prices for at least 3 markets with currency conversion and PPP adjustment
- Provides pricing strategy framework (premium/competitive/balanced) with rationale
- Includes currency risk assessment with volatility levels and review frequency
- Lists competitive positioning analysis vs local market prices
- Returns valid JSON with all documented fields present
- Contains complete safety disclaimer in every output
- Includes input_analysis summarizing parsed input
- Pure descriptive — no code execution, API calls, network access
