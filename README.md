# AI Equity Research Toolkit

Built during IESE's AI-Augmented Productivity for Finance course.

## What it does

- Values a company against its peers from live SEC EDGAR data
- Screens a 16-company universe on growth and margins — criteria as dials
- Writes grounded investment rationales and audits every number in them
- Runs a governed research agent with hard limits and a human gate

## Trust features

- Every model output is validated at the boundary (Pydantic schemas)
- Every figure in generated prose is traced to source data or flagged
- Nothing is saved without explicit human approval

## Run it

```bash
pip install -r requirements.txt
```

and later:

```text
```bash
jupyter lab notebooks/

When you open the README on GitHub, it will render nicely as code boxes.

**So: everything in the big block I gave you goes into `README.md`; none of it goes into Terminal.**