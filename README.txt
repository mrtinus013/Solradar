PEARL · Solana Alpha Engine v7.1
=================================

Geen Axiom-account nodig.

Execution:
- PEARL controleert een ENTRY READY coin vóór de knop actief wordt.
- Jupiter-route beschikbaar en price impact <= 20% -> TRADE NU opent Jupiter in de Trust Wallet dApp-browser.
- Geen Jupiter-route, maar de token is een Pump.fun launch -> TRADE NU opent de coin op Pump.fun in Trust Wallet.
- Geen bruikbare route -> entryknop blijft geblokkeerd.
- Voor verkoop probeert PEARL eerst token -> SOL via Jupiter, met Pump.fun als fallback voor Pump launches.

Trust Wallet deep-link:
- gebruikt de officiële open_url DApp-browser route.
- PEARL vraagt nooit om seed phrase of private key.

De lifecycle-, falling-knife-, sizing-, X/KOL- en self-audit-logica van v7 blijft behouden.
