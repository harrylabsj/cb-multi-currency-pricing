# Multi-currency Pricing Strategist

Dynamic pricing strategies across currencies and markets for cross-border e-commerce.

## Tags

`cross-border` `currency-management` `pricing-strategy` `forex`

## Usage Scenarios

### 场景一：多币种定价换算太麻烦了

**用户输入：** "我们产品在亚马逊美国站卖$19.99，现在想上日本站和欧洲站。日元/欧元/英镑怎么定价格不亏？"

**预期输出：** 多币种定价策略——第一步：算基础价（人民币成本×目标利润率=美元出价，锁定美元基准价）；第二步：按购买力平价调价（日本用$19.99×110=¥2199而非按汇率直接换算¥2999，人均收入高的国家可以加价）；第三步：检查各平台的定价规则（亚马逊日本站习惯含税价格显示，欧洲站必须含VAT）；第四步：用定价工具自动化（SellerSprite/卖家精灵有自动汇率换算+竞品价格参考）；第五步：定期复盘（每月检查汇率变动>3%要及时调价，但不要频繁调价让客户困惑）。关键工具：AMZScout/XSellco的自动定价功能。

### Scenario 2: Currency Buffer Pricing

**User Input:** "Set up pricing for our $49 USD product across EUR, GBP, JPY, and AUD. I want to protect against 5% currency swings."

**Expected Output:** Price grid: €52.95 (5% buffer), £43.50, ¥6,980, A$78.00. Each includes the buffer calculation, rounded to local psychological price points, with a note on which gateway can settle in that currency.

### Scenario 3: Dynamic Pricing Rule Set

**User Input:** "Build a dynamic pricing rule set: if a currency moves more than 3% in 30 days, trigger a price review alert with the recommended adjustment."

**Expected Output:** Rule engine specification: monitored pairs, 3% threshold, 30-day rolling window, alert template with new suggested price, margin-impact calculation, and competitor-price re-check prompt.
