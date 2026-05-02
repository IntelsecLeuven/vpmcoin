VPM COIN
Virtual Private Money
ERC-20 Loyalty Token — Belgisch Handelaarsnetwerk

WHITEPAPER v1.0
Belgie — 2025
 
1. Samenvatting (Executive Summary)
VPM Coin (ticker: VPM) is een ERC-20 smart contract token op de Ethereum blockchain, specifiek ontwikkeld als loyaliteitstoken voor het Belgische handelslandschap. De token stelt handelaars in staat hun klanten te belonen na elke aankoop, waarbij een transparant en fraudebestendig systeem on-chain wordt geregistreerd.

De kernregel is eenvoudig: wie 100 VPM Coins heeft verzameld, kan voor 10 euro aankopen doen bij elke aangesloten VPM-partner in Belgie. Dit creert een gedeeld loyaliteitsnetwerk dat de kracht van individuele stempelkaarten overstijgt.

Parameter	Waarde
Token naam	VPM Coin
Ticker symbool	VPM
Blockchain	Ethereum Mainnet
Token standaard	ERC-20
Totale supply	250.000.000 VPM
Decimalen	18
Inwisselgrens	100 VPM = EUR 10,00
Impliciete tokenwaarde	EUR 0,10 per token

2. Probleemstelling
2.1 Versnipperde loyaliteitssystemen
De Belgische detailhandel kent een wirwar van loyaliteitsprogrammas: papieren stempelkaarten, proprietary apps, puntenkaarten van supermarktketens en winkeltegoeden. Dit creeert drie fundamentele problemen:
•	Klantenfragmentatie: consumenten beheren tientallen afzonderlijke loyaliteitsprogrammas
•	Handelaarslast: KMO's missen de middelen voor eigen digitale loyaliteitsinfrastructuur
•	Waardeverlies: ongebruikte punten en vervallen kaarten vertegenwoordigen jaarlijks miljoenen euros

2.2 Gebrek aan interoperabiliteit
Geen enkel bestaand Belgisch loyaliteitsprogramma is interoperabel. Een klant die trouw is aan een bakker, slager en boekhandel, moet drie aparte systemen bijhouden. VPM Coin lost dit op door een gedeeld, neutraal tokenplatform te bieden.

3. De VPM Coin Oplossing
3.1 Architectuur
VPM Coin is een permissioned ERC-20 token met een uitgebreid loyaliteitslaag. De smart contract architectuur omvat:
•	Merkant-registry: alleen geverifieerde handelaars kunnen tokens uitgeven
•	Loyalty issuance: handelaars sturen VPM tokens naar klanten na een aankoop
•	Redemption mechanisme: klanten wisselen 100 VPM in voor EUR 10 korting
•	On-chain audittrail: alle transacties zijn transparant en onveranderlijk

3.2 Token Flow
Stap	Actor	Actie	Resultaat
1	Eigenaar (Foundation)	Distribueert tokens aan handelaars	Handelaar ontvangt VPM reserve
2	Handelaar	Geeft tokens aan klant na aankoop	Klant ontvangt VPM in wallet
3	Klant	Verzamelt tokens over meerdere aankopen	Balance groeit richting 100 VPM
4	Klant	Roept redeemTokens() aan bij handelaar	100 VPM worden afgetrokken, klant krijgt EUR 10 korting
5	Handelaar	Ontvangt 100 VPM terug in reserve	Tokens circuleren opnieuw in het netwerk

 
4. Tokenomics
4.1 Totale Supply
De totale supply bedraagt 250.000.000 VPM tokens, vast vastgelegd in het smart contract. Er is geen mintfunctie na de initialisatie; de supply is deflatoir door redemptie-cycli die tokens terugsturen naar handelsreserves.

4.2 Distributieverdeling
Categorie	Tokens (VPM)	Percentage	Doel
Handelaarsreserve (jaar 1)	125.000.000	50%	Initieel uitgifte aan partner-handelaars
Groei & uitbreiding (jaar 2-5)	75.000.000	30%	Nieuwe handelaars en regio-uitbreiding
Foundation & operations	25.000.000	10%	Ontwikkeling, marketing, juridisch
Community & promotie	12.500.000	5%	Klant onboarding campagnes
Reserve & noodfonds	12.500.000	5%	Liquiditeitsback-up

4.3 Token Waarde & Stabiliteit
De token heeft een vaste functionele waarde: 100 VPM = EUR 10. Dit geeft elke token een impliciete waarde van EUR 0,10 voor redemptiedoeleinden. De marktprijs op exchanges kan afwijken, maar de utility-waarde binnen het netwerk is contractueel vastgelegd.

5. Technische Specificaties
5.1 Smart Contract Functies
Functie	Toegang	Beschrijving
registerMerchant()	Eigenaar	Registreert een nieuwe handelaar in het netwerk
removeMerchant()	Eigenaar	Verwijdert een handelaar uit het netwerk
issueLoyaltyTokens()	Handelaar	Geeft VPM tokens aan klant na aankoop
redeemTokens()	Klant	Wisselt 100 VPM in voor EUR 10 korting
distributeMerchantAllocation()	Eigenaar	Verdeelt tokens vanuit hoofdreserve
availableRedemptions()	Publiek	Hoeveel keer een klant kan inwisselen
tokensUntilNextRedemption()	Publiek	Tokens nog nodig tot volgende reward

5.2 Beveiligingsmaatregelen
•	Role-based access control: eigenaar en handelaar rollen gescheiden
•	Geen mintfunctie na deployment: supply is onveranderlijk
•	Reentrancy-veilig: token transfers voor state changes
•	Zero-address checks op alle externe parameters
•	Aanbeveling: audit door gecertificeerd Solidity security lab voor mainnet deployment

 
6. Roadmap
Fase	Periode	Mijlpalen
Fase 1 — Fundament	Q1 2025	Smart contract ontwikkeling, juridische analyse, whitepaper
Fase 2 — Piloot	Q2 2025	10-20 piloothandelaars in Antwerpen & Brussel, wallet integratie
Fase 3 — Lancering	Q3 2025	ICO, token distributie, publieke wallet app, 100+ handelaars
Fase 4 — Groei	Q4 2025	Uitbreiding naar alle Belgische provincies, 500+ handelaars
Fase 5 — Europees	2026+	Uitbreiding naar Nederland, Luxemburg, nord-Frankrijk

7. Juridische Overwegingen
VPM Coin is ontworpen als een utility token, niet als een financieel instrument of waardepapier. De token heeft uitsluitend een loyaliteitsfunctie binnen het VPM handelaarsnetwerk.

•	MiCA-conformiteit: classificatie als utility token onder EU Markets in Crypto-Assets regulation
•	GDPR: geen persoonlijke gegevens on-chain; walletadressen zijn pseudoniem
•	Fiscaal: loyaliteitsvoordelen voor particulieren zijn in Belgie doorgaans belastingvrij tot bepaalde limieten
•	Aanbeveling: raadpleeg een Belgisch advocatenkantoor gespecialiseerd in fintech voor finalisatie

8. Risicoanalyse
Risico	Ernst	Mitigatie
Smart contract bug	Hoog	Externe security audit voor mainnet launch
Lage handelaarsadoptie	Gemiddeld	Incentiveprogramma voor early adopters
Regulatoire wijziging	Gemiddeld	Nauwe opvolging MiCA en NBB richtlijnen
Ethereum gas fees	Laag-Middel	Layer-2 migratie overwegen (Polygon, Arbitrum)
Token koersvariatie	Laag	Utility waarde onafhankelijk van marktprijs

9. Conclusie
VPM Coin vertegenwoordigt een pragmatische toepassing van blockchain-technologie voor de Belgische lokale economie. Door loyaliteit te tokeniseren op een gedeeld, open netwerk, krijgen zowel kleine handelaars als consumenten toegang tot een modern beloningssysteem zonder proprietary lock-in.

Met een totale supply van 250.000.000 tokens, een helder inwisselingsmechanisme en een transparant smart contract, is VPM Coin klaar om het Belgische handelaarslandschap te transformeren.

VPM Coin Foundation — Belgie
info@vpmcoin.be  |  www.vpmcoin.be

