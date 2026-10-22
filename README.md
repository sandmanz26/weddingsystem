# Bloomprint Decor Studio

A front-end-only decor estimator for couples planning a wedding in Australia, Europe, the UK or the US.

Couples upload an inspiration photo (or pick a style), describe their day and pick decor pieces. The page returns:

- **Blueprint** – a live front-view drawing of the selected pieces in the chosen palette
- **Estimate** – itemised totals per piece and per category, contingency and local tax (GST/VAT/sales tax)
- **Materials** – flower varieties, stems, bunches to order, rentals vs purchases, crew hours
- **Budgets** – Essential / Signature / Couture variations plus "ways to save"
- **To prepare** – a checklist built from the brief (venue details, decisions, on the day, paperwork)
- **Timeline** – dated milestones and a three-step payment schedule counted back from the wedding date

## Run it

No build step. Open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server 8000
```

## Notes

- Everything runs in the browser. The colour palette is extracted from the uploaded photo with a canvas; nothing is uploaded anywhere.
- The brief form does not send anything yet; it formats a brief the couple can copy.
- Prices are indicative assumptions (wholesale stem costs, rental rates, labour rates, FX) defined at the top of the script in `REGIONS`, `STEM`, `TIERS` and the `EL` piece list. Replace them with real supplier pricing before using with customers.
- The brief and checklist progress are remembered in `localStorage` in the viewer's browser only.
