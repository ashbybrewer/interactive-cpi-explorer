# The Chart of the Century — interactive edition

An interactive explorer for one of the most striking patterns in the modern U.S. economy: **since 2000, prices in sectors exposed to competition collapsed, while prices in regulated and subsidized sectors soared.**

It is a single, self-contained `index.html` file with **no build step and no dependencies** — open it in any browser or drop it straight onto GitHub Pages. Every number is computed from official U.S. government data.

The framing follows economist Mark J. Perry's long-running "Chart of the Century."

---

## What's inside

- **The Divergence** — an animated line chart where all 15 categories start together at zero in 2000 and fan apart over 24 years. Play, pause, and scrub by year; hover for a full readout.
- **The Ranking** — a diverging bar chart of total 2000–2024 price change, with reference guides for overall inflation (+82%) and average wage growth (+115%), so you can see what beat your paycheck.
- **Why the Split** — a short, balanced explainer of the forces pushing prices down (trade, automation, near-zero marginal cost, competition) versus up (third-party payment, restricted supply, subsidized demand, Baumol's cost disease), plus an honest caveat about quality adjustment.
- **The Personal Test** — an "are you actually better off?" calculator. Pick a household profile or move the sliders to describe how *you* spend; it builds your **personal inflation rate** from the real category data and weighs it against your income.

## Headline numbers (Jan 2000 → 2024, CPI-U)

| Shielded from competition |        | Exposed to competition |       |
| ------------------------- | ------ | ---------------------- | ----- |
| Hospital services         | +258%  | New cars               | +25%  |
| College tuition           | +182%  | Clothing               | +2%   |
| College textbooks         | +141%  | Cellphone service      | −38%  |
| Child care                | +135%  | Toys                   | −74%  |
| Medical care              | +130%  | Software               | −92%  |
| _Overall inflation_       | _+82%_ | Televisions            | −98%  |

_Average hourly wages over the same period: **+115%**._

## Data & sources

All figures are annual averages, indexed so that the year 2000 = 0%, measured through 2024 (the last complete year).

- **Prices** — U.S. Bureau of Labor Statistics, Consumer Price Index for All Urban Consumers (CPI-U), not seasonally adjusted, U.S. city average. <https://www.bls.gov/cpi/>
- **Wages** — BLS, average hourly earnings of production and nonsupervisory employees, total private (CES).
- **Household income** — U.S. Census Bureau median household income: $42,148 (2000) and $83,730 (2024), current dollars. <https://www.census.gov/topics/income-poverty/income.html>

The underlying series are included in [`data/`](data/) as both CSV and JSON for full reproducibility.

## Run it

Just open `index.html` — that's the whole app. An internet connection only fetches the two web fonts (it falls back to system fonts offline).

### Publish on GitHub Pages

1. Push this repository to GitHub.
2. **Settings → Pages → Source:** deploy from the `main` branch, root folder.
3. Your site goes live at `https://<your-username>.github.io/<repo-name>/`.

## A note on interpretation

These are **price indices, not measures of value for money.** The BLS quality-adjusts goods like televisions, which deepens their measured price drop; health care and education improved in quality too, but those gains are harder to price. The chart shows what happened to the sticker — it does not, on its own, settle whether any sector delivers more for what you pay.

## License

Code released under the MIT License. The underlying data is produced by U.S. federal agencies and is in the public domain; please cite BLS and the U.S. Census Bureau.
