# Agent research memo

**Task:** Analyze Apple (ticker AAPL) and compare it with Sony (ticker SONY): which is better positioned on growth and profitability?

## Apple is better positioned than Sony on profitability, despite Sony's higher historical revenue growth

**Stance:** prefer first | **Confidence:** medium

## Key points

- Profitability: Apple's FY2025 (ended 2025-09-27) operating margin was 31.97% and net margin 26.92%, versus Sony's FY2025 (ended 2025-03-31) operating margin of 10.86% and net margin of 8.95% — Apple's margins are roughly 3x Sony's, and this gap has held across all four fiscal years shown, not just the latest one.
- Growth trend: Apple's revenue growth accelerated to 6.43% in FY2025 (unitless, from $391.0bn to $416.2bn USD) after a dip in FY2023 (-2.8%), while Sony's growth swung from 18.65% in FY2024 to -0.49% in FY2025 (¥13,020.8bn to ¥12,957.1bn JPY) — Sony's growth is higher on a 3-year CAGR basis (9.31% vs Apple's 1.81%) but far more volatile and just turned negative.
- Currencies differ (Apple reports in USD, Sony in JPY), so absolute revenue/income figures are not directly comparable; all comparisons above use unitless growth rates and margins as required.
- Forward view: forecast_revenue projects Apple FY+1 revenue of $448.1bn (holdout error 5%) and Sony FY+1 revenue of ¥14,479.3bn (holdout error 8.1%); Apple's forecast carries a smaller measured error, giving it somewhat higher confidence even before considering currency non-comparability.

## Risks

- Apple's margin advantage relies heavily on Services mix and share buybacks (net margin held near 25-27% even as revenue dipped in FY2023); a slowdown in iPhone/Services demand or regulatory action on App Store fees could compress margins toward Sony's range.
- Sony's higher revenue CAGR (9.31%) reflects a diversified base (gaming, imaging sensors, entertainment, financial) that could re-accelerate growth if any segment (e.g., image sensors for AI/mobile) scales faster than Apple's more concentrated hardware-plus-services model — the FY2025 growth dip may be temporary.

## What would change this view

If Sony's operating margin closed to within a few points of Apple's for two consecutive fiscal years while sustaining double-digit revenue growth, the profitability edge favoring Apple would no longer hold.

## Audit trail (every tool call the agent made)

- step 1: get_financials({"ticker": "AAPL"})
- step 1: get_financials({"ticker": "SONY"})
- step 1: compare_metrics({"tickers": ["AAPL", "SONY"]})
- step 1: forecast_revenue({"ticker": "AAPL"})
- step 1: forecast_revenue({"ticker": "SONY"})
- step 1: read_skill({"name": "memo-style"})
- step 2: record_recommendation({"headline": "Apple is better positioned than Sony on profitability, despite Sony's higher historical revenue growth", "stance": "prefer_first", "key_points": "\n<parameter name=\"key_points\">[\"Profitability: Apple's FY2025 (ended 2025-09-27) operating margin was 31.97% and net margin 26.92%, versus Sony's FY2025 (ended 2025-03-31) operating margin of 10.86% and net margin of 8.95% \u2014 Apple's margins are roughly 3x Sony's, and this gap has held across all four fiscal years shown, not just the latest one.\", \"Growth trend: Apple's revenue growth accelerated to 6.43% in FY2025 (unitless, from $391.0bn to $416.2bn USD) after a dip in FY2023 (-2.8%), while Sony's growth swung from 18.65% in FY2024 to -0.49% in FY2025 (\u00a513,020.8bn to \u00a512,957.1bn JPY) \u2014 Sony's growth is higher on a 3-year CAGR basis (9.31% vs Apple's 1.81%) but far more volatile and just turned negative.\", \"Currencies differ (Apple reports in USD, Sony in JPY), so absolute revenue/income figures are not directly comparable; all comparisons above use unitless growth rates and margins as required.\", \"Forward view: forecast_revenue projects Apple FY+1 revenue of $448.1bn (holdout error 5%) and Sony FY+1 revenue of \u00a514,479.3bn (holdout error 8.1%); Apple's forecast carries a smaller measured error, giving it somewhat higher confidence even before considering currency non-comparability.\"]", "risks": "\n<parameter name=\"risks\">[\"Apple's margin advantage relies heavily on Services mix and share buybacks (net margin held near 25-27% even as revenue dipped in FY2023); a slowdown in iPhone/Services demand or regulatory action on App Store fees could compress margins toward Sony's range.\", \"Sony's higher revenue CAGR (9.31%) reflects a diversified base (gaming, imaging sensors, entertainment, financial) that could re-accelerate growth if any segment (e.g., image sensors for AI/mobile) scales faster than Apple's more concentrated hardware-plus-services model \u2014 the FY2025 growth dip may be temporary.\"]", "confidence": "medium", "what_would_change_my_mind": "If Sony's operating margin closed to within a few points of Apple's for two consecutive fiscal years while sustaining double-digit revenue growth, the profitability edge favoring Apple would no longer hold."})
- step 2: record_recommendation REJECTED (['$.key_points: expected array, got str', '$.risks: expected array, got str'])
- step 3: record_recommendation({"headline": "Apple is better positioned than Sony on profitability, despite Sony's higher historical revenue growth", "stance": "prefer_first", "key_points": ["Profitability: Apple's FY2025 (ended 2025-09-27) operating margin was 31.97% and net margin 26.92%, versus Sony's FY2025 (ended 2025-03-31) operating margin of 10.86% and net margin of 8.95% \u2014 Apple's margins are roughly 3x Sony's, and this gap has held across all four fiscal years shown, not just the latest one.", "Growth trend: Apple's revenue growth accelerated to 6.43% in FY2025 (unitless, from $391.0bn to $416.2bn USD) after a dip in FY2023 (-2.8%), while Sony's growth swung from 18.65% in FY2024 to -0.49% in FY2025 (\u00a513,020.8bn to \u00a512,957.1bn JPY) \u2014 Sony's growth is higher on a 3-year CAGR basis (9.31% vs Apple's 1.81%) but far more volatile and just turned negative.", "Currencies differ (Apple reports in USD, Sony in JPY), so absolute revenue/income figures are not directly comparable; all comparisons above use unitless growth rates and margins as required.", "Forward view: forecast_revenue projects Apple FY+1 revenue of $448.1bn (holdout error 5%) and Sony FY+1 revenue of \u00a514,479.3bn (holdout error 8.1%); Apple's forecast carries a smaller measured error, giving it somewhat higher confidence even before considering currency non-comparability."], "risks": ["Apple's margin advantage relies heavily on Services mix and share buybacks (net margin held near 25-27% even as revenue dipped in FY2023); a slowdown in iPhone/Services demand or regulatory action on App Store fees could compress margins toward Sony's range.", "Sony's higher revenue CAGR (9.31%) reflects a diversified base (gaming, imaging sensors, entertainment, financial) that could re-accelerate growth if any segment (e.g., image sensors for AI/mobile) scales faster than Apple's more concentrated hardware-plus-services model \u2014 the FY2025 growth dip may be temporary."], "confidence": "medium", "what_would_change_my_mind": "If Sony's operating margin closed to within a few points of Apple's for two consecutive fiscal years while sustaining double-digit revenue growth, the profitability edge favoring Apple would no longer hold."})

---
*Coursework artifact (IESE AI-Finance bootcamp) — data: SEC EDGAR. Not investment advice.*
