PEARL · Solana Alpha Engine v7
================================

Dit is een volledige herbouw. Geen v5/v6 buy-scorelogica.

Kern:
- market refresh ~2 sec, discovery ~7 sec;
- lifecycle state machine:
  DISCOVERY → FORMING → ACCUMULATION → BREAKOUT
  en expliciet EUPHORIA / DISTRIBUTION / DUMP / RECLAIM;
- falling-knife guard;
- BUY/ENTRY alleen bij bevestigde BREAKOUT of RECLAIM;
- hogere-low / hogere-high / microtrend / flow-trend worden meegenomen;
- RugCheck op topkandidaten;
- best-effort KOL Explorer intelligence;
- directe Axiom tokenpagina als execution terminal;
- survival sizing: 0.5–2% van de ingestelde tradingpot;
- self-audit: elk ENTRY READY signaal wordt 30s/2m/5m gemeten;
- circuit breaker: slechte reeks signalen zet PEARL 30 min in COOLDOWN;
- positie-monitor met HOLD / DERISK / RUNNER / EXIT;
- bij 2x: advies om principal te de-risken en een runner-bag te laten lopen.

Optionele PumpPortal speed feed:
- subscribeNewToken + subscribeMigration;
- géén subscribeTokenTrade/accountTrade, dus PEARL activeert de betaalde trade-event stream niet;
- API-key wordt alleen lokaal in de browser opgeslagen.

Axiom:
- configureer daar zelf slippage, MEV protection en eventueel Quick Buy presets;
- PEARL voert nooit zelfstandig een transactie uit.

Belangrijk:
Geen enkele score voorspelt betrouwbaar een 100x. De opzet is gericht op asymmetrische
kansen terwijl één fout signaal de tradingpot niet mag domineren.
