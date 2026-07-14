  
For investment funds I have MyInvestor and for etfs and stocks I use trade republic. I will have to fill my tax papers manually for all the trade republic stuff.

Thank you, i just found out that since I am under beckham law it is better for me to use IBKR and then after end of the beckham law, move the money to myInvestor. Hopefully I'll be much more comfortable with Spanish then. I'll talk to a tax advisor though before doing anything.
Why does the Beckham law make IBKR better choice?

During 5 years if you have that regime you only pay on locally sourced income.


# Amazon Stocks blueprint

 Tax Withholding Election — What to choose

  The 3 options explained

  ```
  ┌──────────────────────────┬────────────────────────────────────────────────────────────┬──────────────────────────────┬───────────────────────────────────────────────────┐
  │          Method          │                    What happens at vest                    │      Shares you receive      │                     Best for                      │
  ├──────────────────────────┼────────────────────────────────────────────────────────────┼──────────────────────────────┼───────────────────────────────────────────────────┤
  │ Sell for Taxes (default) │ Broker sells enough shares to cover tax, you keep the rest │ Fewer shares, no cash needed │ Most people — zero effort                         │
  ├──────────────────────────┼────────────────────────────────────────────────────────────┼──────────────────────────────┼───────────────────────────────────────────────────┤
  │ Sell All                 │ ALL shares sold, taxes paid, cash remainder sent to you    │ 0 shares, cash in hand       │ People who want to immediately reinvest elsewhere │
  ├──────────────────────────┼────────────────────────────────────────────────────────────┼──────────────────────────────┼───────────────────────────────────────────────────┤
  │ Pay Cash                 │ You pre-deposit cash to cover taxes, no shares sold        │ ALL shares                   │ People who want maximum AMZN exposure             │
  └──────────────────────────┴────────────────────────────────────────────────────────────┴──────────────────────────────┴───────────────────────────────────────────────────┘
  
  ```

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
