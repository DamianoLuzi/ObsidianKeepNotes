  
For investment funds I have MyInvestor and for etfs and stocks I use trade republic. I will have to fill my tax papers manually for all the trade republic stuff.

Thank you, i just found out that since I am under beckham law it is better for me to use IBKR and then after end of the beckham law, move the money to myInvestor. Hopefully I'll be much more comfortable with Spanish then. I'll talk to a tax advisor though before doing anything.
Why does the Beckham law make IBKR better choice?

During 5 years if you have that regime you only pay on locally sourced income.


# Amazon Stocks blueprint

 Tax Withholding Election — What to choose

  The 3 options explained

  For YOUR situation (IBKR investor, buying VUAA)

  If your plan is to sell AMZN anyway and put the money into VUAA on IBKR, choose "Sell All."

  Here's why:

  Sell All flow:
    12 RSUs vest → all sold automatically → cash in MS/Fidelity
    → wire USD to Interactive Brokers ($7.50 MS / $0 Fidelity)
    → convert to EUR at IBKR (~2 bps)
    → buy VUAA

  Sell for Taxes flow (default):
    12 RSUs vest → ~5 shares sold for tax → 7 shares remain
    → you then manually sell those 7 shares later
    → same wire/convert/buy process
    → BUT: you're now exposed to AMZN price movements between vest and manual sale
    → extra step + potential trading window restrictions

  Sell All eliminates the manual step and timing risk. The broker sells everything on vest day at the average price, taxes are handled, you get clean cash ready to wire.

  If you want to KEEP some AMZN

  Then stay on Sell for Taxes and your remaining shares sit in the broker account. You can sell or hold them on your own timeline (subject to insider trading windows).

  Fractional Share Election

  Your current setting is Cash Refund (default). This means:
  - If selling 5.3 shares covers your taxes but broker can only sell whole shares (6), the extra ~$140 goes back to you via payroll

  If you switch to Fractional Shares:
  - Broker sells exactly 5.3 shares, you keep 6.7 shares (including the 0.7 fraction)

  For Sell All: This setting is irrelevant — everything is sold anyway.

  For Sell for Taxes: Fractional Shares is marginally better if you want to maximize shares retained, since you don't lose value to rounding.

  My recommendation for your workflow

  ```
  ┌───────────────────┬─────────────────────────────────────────────────────────┐
  │      Setting      │                         Choose                          │
  ├───────────────────┼─────────────────────────────────────────────────────────┤
  │ Broker            │ Fidelity — $0 USD wire to IBKR (saves $7.50/vest vs MS) │
  ├───────────────────┼─────────────────────────────────────────────────────────┤
  │ Tax election      │ Sell All — if you plan to put proceeds into VUAA anyway │
  ├───────────────────┼─────────────────────────────────────────────────────────┤
  │ Fractional shares │ Doesn't matter with Sell All                            │
  └───────────────────┴─────────────────────────────────────────────────────────┘
  ```

  Flow: RSUs vest → auto-sold → wire USD to IBKR (free) → convert at 2bps → buy VUAA BVME

  This is the cheapest path from Amazon RSU → diversified portfolio. Total cost per vest: essentially just IBKR's ~$2 FX fee.

1. Broker: Fidelity

  ┌────────────────────────────┬───────────────────────────────┬──────────────────────────┬──────────────────────────────────────────────────────────────┐
  │           Factor           │        Morgan Stanley         │         Fidelity         │                           Verdict                            │
  ├────────────────────────────┼───────────────────────────────┼──────────────────────────┼──────────────────────────────────────────────────────────────┤
  │ USD wire to IBKR           │ $7.50/transfer                │ $0                       │ Fidelity saves $7.50 every vest                              │
  ├────────────────────────────┼───────────────────────────────┼──────────────────────────┼──────────────────────────────────────────────────────────────┤
  │ Online trade               │ $0                            │ $0                       │ Tie                                                          │
  ├────────────────────────────┼───────────────────────────────┼──────────────────────────┼──────────────────────────────────────────────────────────────┤
  │ Phone trade                │ $0                            │ $4.95                    │ Irrelevant — you'll use Sell All (automatic)                 │
  ├────────────────────────────┼───────────────────────────────┼──────────────────────────┼──────────────────────────────────────────────────────────────┤
  │ Currency conversion        │ 160 bps                       │ 75-250 bps               │ Irrelevant — you'll convert at IBKR for ~2 bps instead       │
  ├────────────────────────────┼───────────────────────────────┼──────────────────────────┼──────────────────────────────────────────────────────────────┤
  │ Non-US ACH (EUR)           │ Available                     │ Not available            │ Irrelevant — you're wiring USD to IBKR, not EUR to your bank │
  ├────────────────────────────┼───────────────────────────────┼──────────────────────────┼──────────────────────────────────────────────────────────────┤
  │ Wire speed to IBKR         │ Same (USD domestic/intl wire) │ Same                     │ Tie                                                          │
  ├────────────────────────────┼───────────────────────────────┼──────────────────────────┼──────────────────────────────────────────────────────────────┤
  │ Phone support              │ No Italian/Spanish            │ Italian, Spanish, German │ Fidelity                                                     │
  ├────────────────────────────┼───────────────────────────────┼──────────────────────────┼──────────────────────────────────────────────────────────────┤
  │ International satisfaction │ 79.6%                         │ 75.7%                    │ Slight MS edge, but offset by everything else                │
  ├────────────────────────────┼───────────────────────────────┼──────────────────────────┼──────────────────────────────────────────────────────────────┤
  │ Sell All execution         │ Same                          │ Same                     │ Tie                                                          │
  └────────────────────────────┴───────────────────────────────┴──────────────────────────┴──────────────────────────────────────────────────────────────┘

  Why Fidelity: The main advantages of Morgan Stanley (Non-US ACH in EUR, flat conversion rate) don't matter for your workflow because you're not converting at the stock plan broker. You're sending USD straight to IBKR. So the only real differentiator is
  the $0 wire fee at Fidelity vs $7.50 at MS. Over years of vests that adds up for zero extra effort.

  ---
  2. Tax Withholding: Sell All

  ┌──────────────────────────────────────────────────────┬────────────────┬──────────────────────────────────────────────────────────────────────────┐
  │                       Scenario                       │ Best election  │                                   Why                                    │
  ├──────────────────────────────────────────────────────┼────────────────┼──────────────────────────────────────────────────────────────────────────┤
  │ You want to reinvest in VUAA/ETFs via IBKR           │ Sell All       │ Automatic, no manual selling, no timing risk, no trading window concerns │
  ├──────────────────────────────────────────────────────┼────────────────┼──────────────────────────────────────────────────────────────────────────┤
  │ You want to hold some AMZN long-term                 │ Sell for Taxes │ Keeps remaining shares; sell manually when ready                         │
  ├──────────────────────────────────────────────────────┼────────────────┼──────────────────────────────────────────────────────────────────────────┤
  │ You have cash sitting around and are bullish on AMZN │ Pay Cash       │ Keep 100% of shares, but you need to pre-fund 5 trading days before vest │
  └──────────────────────────────────────────────────────┴────────────────┴──────────────────────────────────────────────────────────────────────────┘

  Why Sell All for you: You're already building your portfolio in IBKR with VUAA. Holding individual AMZN stock on top of that means you're overweight Amazon (you already get AMZN exposure through VUAA since it's ~6% of S&P 500). Sell All automates the
  entire process — no manual intervention, no insider trading window worries, no timing decisions.

  ---
  3. Fractional Share Election: Doesn't matter

  With Sell All, everything is sold. This setting only applies to Sell for Taxes. No action needed.

  ---
  Your optimal end-to-end flow

  Every vest (e.g., Nov 15 — 12 RSUs):

  4. [Automatic] Fidelity sells all 12 shares at market
  5. [Automatic] Taxes withheld and remitted to authorities
  6. [You] Net cash lands in Fidelity (~2-3 business days)
  7. [You] Wire USD to Interactive Brokers (free, 1-3 days)
  8. [You] Convert USD → EUR in IBKR (~2 bps = ~$0.20 per $1,000)
  9. [You] Buy VUAA BVME (or whatever else you want)

  Total cost per vest: ~$2 (IBKR minimum FX fee)

  Compare to the "default" path most people take:
  Morgan Stanley → Sell for Taxes → hold shares → eventually sell →
  convert USD→EUR at 160 bps at MS → wire to bank ($7.50) →
  deposit to IBKR → buy VUAA

  Total cost: ~$50+ per vest on a 12-RSU vest at ~$200/share

  ---
  Action items

  10. Certify your W-8BEN at Morgan Stanley NOW (before you switch) — otherwise 24% extra withholding on Nov 15 vest
  11. Switch broker to Fidelity on amazonstock.com (can do anytime except 7 days before vest)
  12. Set tax election to "Sell All" once your Fidelity account is set up
  13. Set up USD wire instructions in Fidelity pointing to your IBKR account

