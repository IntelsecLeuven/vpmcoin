<div align="center">

<img src="https://img.shields.io/badge/VPM%20Coin-Virtual%20Private%20Money-gold?style=for-the-badge&logo=ethereum&logoColor=white" alt="VPM Coin"/>

# 🪙 VPM Coin — Virtual Private Money

**De eerste Belgische ERC-20 loyaliteitstoken voor het lokale handelsnetwerk**

[![Solidity](https://img.shields.io/badge/Solidity-0.8.20-363636?style=flat-square&logo=solidity)](https://soliditylang.org/)
[![ERC-20](https://img.shields.io/badge/Standard-ERC--20-blue?style=flat-square&logo=ethereum)](https://eips.ethereum.org/EIPS/eip-20)
[![Network](https://img.shields.io/badge/Network-Ethereum-627EEA?style=flat-square&logo=ethereum)](https://ethereum.org/)
[![Supply](https://img.shields.io/badge/Supply-250%2C000%2C000%20VPM-gold?style=flat-square)]()
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)
[![Belgium](https://img.shields.io/badge/Market-Belgium%20🇧🇪-black?style=flat-square)]()

---

> **100 VPM = €10 aankoop bij elke aangesloten Belgische handelaar**

</div>

---

## 📋 Inhoudsopgave

- [Wat is VPM Coin?](#-wat-is-vpm-coin)
- [Hoe werkt het?](#-hoe-werkt-het)
- [Token Specificaties](#-token-specificaties)
- [Tokenomics](#-tokenomics)
- [Smart Contract](#-smart-contract)
- [Contract Functies](#-contract-functies)
- [Installatie & Deployment](#-installatie--deployment)
- [Gebruik (Code Voorbeelden)](#-gebruik-code-voorbeelden)
- [Roadmap](#-roadmap)
- [Voor Handelaars](#-voor-handelaars)
- [Beveiliging](#-beveiliging)
- [Juridisch](#-juridisch)
- [Contact](#-contact)

---

## 💡 Wat is VPM Coin?

VPM Coin is een **ERC-20 utility token** op de Ethereum blockchain, ontworpen als het universele loyaliteitssysteem voor Belgische handelaars. In plaats van tientallen losse stempelkaarten of proprietary apps, werkt VPM als één gedeeld beloningsnetwerk.

```
Klant koopt bij handelaar A  →  ontvangt VPM tokens
Klant koopt bij handelaar B  →  ontvangt VPM tokens
Klant heeft 100 VPM          →  €10 korting bij ELKE VPM-partner
```

### Waarom VPM Coin?

| Probleem (vandaag) | Oplossing (VPM Coin) |
|---|---|
| Versnipperde stempelkaarten per winkel | Één universele token voor alle partners |
| Dure loyaliteitsplatformen voor KMO's | Geen abonnement, enkel tokeninvestering |
| Geen interoperabiliteit tussen winkels | Tokens geldig bij alle VPM-handelaars |
| Fraude en verlies van papieren kaarten | On-chain, fraudebestendig en transparant |
| Klantdata gecentraliseerd bij platforms | Pseudoniem, GDPR-conform, self-custody |

---

## 🔄 Hoe werkt het?

```
┌─────────────────────────────────────────────────────────────────┐
│                        VPM Coin Flow                            │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  1. AANKOOP          2. TOKENS           3. VERZAMELEN          │
│  ──────────          ────────            ──────────────         │
│  Klant betaalt  →    Handelaar stuurt →  Klant wallet           │
│  bij handelaar       VPM tokens          groeit naar 100        │
│                      naar wallet                                │
│                                                                 │
│  4. INWISSELEN       5. KORTING          6. CIRCULATIE          │
│  ─────────────       ──────────          ────────────           │
│  Klant roept    →    €10 korting    →    100 VPM terug          │
│  redeemTokens()      bij ELKE            naar handelaar         │
│  aan                 VPM-partner         reserve                │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### Token Flow Diagram

```
[VPM Foundation]
       │
       │  distributeMerchantAllocation()
       ▼
[Handelaar Reserve]  ◄──────────────────────────┐
       │                                         │
       │  issueLoyaltyTokens()                   │
       ▼                                         │
[Klant Wallet]                          redeemTokens() — 100 VPM
       │                                terug naar handelaar
       │  balance >= 100 VPM?
       │  JA → redeemTokens()
       └──────────────────────────────────────────┘
```

---

## 📊 Token Specificaties

| Parameter | Waarde |
|---|---|
| **Naam** | VPM Coin |
| **Ticker** | `VPM` |
| **Blockchain** | Ethereum Mainnet |
| **Standaard** | ERC-20 |
| **Solidity versie** | `^0.8.20` |
| **Totale supply** | `250,000,000 VPM` |
| **Decimalen** | `18` |
| **Inwisseldrempel** | `100 VPM` |
| **Inwisselwaarde** | `€10,00` |
| **Impliciete tokenwaarde** | `€0,10 per VPM` |
| **Mintable** | ❌ Nee (vaste supply) |
| **Burnable** | ❌ Nee |
| **Pausable** | ❌ Nee |

---

## 💰 Tokenomics

```
Totale Supply: 250,000,000 VPM
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  50% ████████████████████░░░░░░░░░░░░░░░░░░░░  Handelaarsreserve jaar 1
  30% ████████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░  Groei & uitbreiding
  10% ████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  Foundation & operations
   5% ██░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  Community & promotie
   5% ██░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  Reserve & noodfonds
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

| Categorie | Tokens | % | Doel |
|---|---|---|---|
| Handelaarsreserve (jaar 1) | 125,000,000 | 50% | Uitgifte aan piloot-handelaars |
| Groei & uitbreiding | 75,000,000 | 30% | Nieuwe partners, regio-uitbreiding |
| Foundation & operations | 25,000,000 | 10% | Dev, marketing, juridisch |
| Community & promotie | 12,500,000 | 5% | Klant onboarding campagnes |
| Reserve & noodfonds | 12,500,000 | 5% | Liquiditeitsback-up |
| **Totaal** | **250,000,000** | **100%** | |

---

## 📜 Smart Contract

Het VPM Coin contract is te vinden in [`VPMCoin.sol`](./VPMCoin.sol).

### Architectuur

```
VPMCoin.sol
├── IERC20 interface
└── VPMCoin contract
    ├── Token metadata (naam, symbool, decimalen)
    ├── Supply constants (250,000,000 VPM)
    ├── Loyalty constants (100 VPM threshold, €10 waarde)
    ├── Role management (owner, merchants)
    ├── ERC-20 core (transfer, approve, allowance)
    ├── Merchant management (register, remove)
    ├── Loyalty logic (issue, redeem)
    ├── Distribution (owner → merchant)
    └── View helpers (availableRedemptions, tokensUntilNext)
```

### Rollen

| Rol | Adres | Rechten |
|---|---|---|
| `owner` | Foundation multisig | Merchants beheren, tokens distribueren, eigendom overdragen |
| `isMerchant` | Geregistreerde handelaar | Loyalty tokens uitgeven aan klanten |
| Klant | Elke wallet | Tokens ontvangen, inwisselen bij handelaar |

---

## 🔧 Contract Functies

### Owner-only functies

```solidity
// Registreer een nieuwe handelaar
function registerMerchant(address merchant, string calldata storeName) external onlyOwner

// Verwijder een handelaar
function removeMerchant(address merchant) external onlyOwner

// Distribueer tokens naar handelaar vanuit hoofdreserve
function distributeMerchantAllocation(address merchant, uint256 amount) external onlyOwner

// Draag eigenaarschap over
function transferOwnership(address newOwner) external onlyOwner
```

### Merchant-only functies

```solidity
// Geef loyalty tokens aan een klant na aankoop
function issueLoyaltyTokens(address customer, uint256 amount) external onlyMerchant
```

### Klant functies

```solidity
// Wissel 100 VPM in voor €10 korting bij een handelaar
function redeemTokens(address merchant) external
```

### Publieke view functies

```solidity
// Hoeveel keer kan een klant nu inwisselen?
function availableRedemptions(address customer) external view returns (uint256)

// Hoeveel tokens nog nodig tot volgende reward?
function tokensUntilNextRedemption(address customer) external view returns (uint256)
```

### Events

```solidity
event MerchantRegistered(address indexed merchant, string name);
event MerchantRemoved(address indexed merchant);
event LoyaltyIssued(address indexed merchant, address indexed customer, uint256 amount);
event LoyaltyRedeemed(address indexed customer, address indexed merchant, uint256 tokensUsed);
event OwnershipTransferred(address indexed previous, address indexed newOwner);
```

### Constanten

```solidity
uint256 public constant REDEMPTION_THRESHOLD = 100 * 10 ** 18;  // 100 VPM
uint256 public constant REDEMPTION_VALUE_EUROCENT = 1000;        // €10,00
```

---

## 🚀 Installatie & Deployment

### Vereisten

- [Node.js](https://nodejs.org/) v18+
- [Hardhat](https://hardhat.org/) of [Foundry](https://getfoundry.sh/)
- Een Ethereum wallet met ETH voor gas
- [MetaMask](https://metamask.io/) of andere Web3 wallet

### Optie A — Remix IDE (eenvoudigst)

1. Ga naar [remix.ethereum.org](https://remix.ethereum.org)
2. Maak nieuw bestand `VPMCoin.sol` aan
3. Plak de contractcode
4. Compileer met Solidity `0.8.20`
5. Deploy via **Injected Provider** (MetaMask)

### Optie B — Hardhat

```bash
# Clone repository
git clone https://github.com/vpmcoin/vpmcoin-contracts.git
cd vpmcoin-contracts

# Installeer dependencies
npm install

# Compileer
npx hardhat compile

# Test
npx hardhat test

# Deploy op testnet (Sepolia)
npx hardhat run scripts/deploy.js --network sepolia

# Deploy op mainnet
npx hardhat run scripts/deploy.js --network mainnet
```

### Deploy script voorbeeld

```javascript
// scripts/deploy.js
const { ethers } = require("hardhat");

async function main() {
  const [deployer] = await ethers.getSigners();
  console.log("Deploying with:", deployer.address);

  const VPMCoin = await ethers.getContractFactory("VPMCoin");
  const vpm = await VPMCoin.deploy();
  await vpm.waitForDeployment();

  console.log("VPMCoin deployed to:", await vpm.getAddress());
  console.log("Total supply:", ethers.formatEther(await vpm.totalSupply()), "VPM");
}

main().catch(console.error);
```

---

## 💻 Gebruik (Code Voorbeelden)

### Handelaar registreren

```javascript
// Als owner: registreer een nieuwe bakkerij
await vpmCoin.registerMerchant(
  "0xHandelaarWalletAdres...",
  "Bakkerij De Gouden Korst"
);
```

### Tokens distribueren aan handelaar

```javascript
// 10.000 VPM sturen naar handelaar (vanuit owner reserve)
const amount = ethers.parseEther("10000");
await vpmCoin.distributeMerchantAllocation(merchantAddress, amount);
```

### Loyalty tokens uitgeven na aankoop

```javascript
// Als handelaar: geef 25 VPM aan klant na aankoop van €25
const tokens = ethers.parseEther("25");
await vpmCoin.connect(merchant).issueLoyaltyTokens(customerAddress, tokens);
```

### Tokens inwisselen (klant)

```javascript
// Als klant: wissel 100 VPM in voor €10 korting
await vpmCoin.connect(customer).redeemTokens(merchantAddress);
```

### Saldo & voortgang controleren

```javascript
// Hoeveel VPM heeft de klant?
const balance = await vpmCoin.balanceOf(customerAddress);
console.log("Saldo:", ethers.formatEther(balance), "VPM");

// Hoeveel tokens nog nodig?
const needed = await vpmCoin.tokensUntilNextRedemption(customerAddress);
console.log("Nog nodig:", ethers.formatEther(needed), "VPM");

// Hoeveel keer kan klant nu inwisselen?
const redemptions = await vpmCoin.availableRedemptions(customerAddress);
console.log("Beschikbare rewards:", redemptions.toString());
```

---

## 🗺️ Roadmap

```
2025 Q1  ████ Fundament
         Smart contract ontwikkeling
         Whitepaper & juridische analyse
         GitHub repository opzetten

2025 Q2  ████ Piloot
         10–20 piloothandelaars (Antwerpen & Brussel)
         Handelaars-app (iOS/Android) beta
         Wallet integratie & QR flow

2025 Q3  ████ Lancering
         ICO & token distributie
         Publieke wallet app release
         100+ actieve handelaars

2025 Q4  ████ Groei
         Uitbreiding alle Belgische provincies
         500+ handelaars
         Layer-2 verkenning (Polygon/Arbitrum)

2026+    ░░░░ Europees
         Nederland, Luxemburg, Noord-Frankrijk
         B2B API voor kassasystemen
         DAO governance structuur
```

---

## 🏪 Voor Handelaars

Wilt u VPM Coin integreren in uw zaak?

### Instappakketten

| Pakket | Tokens | Investering | Ideaal voor |
|---|---|---|---|
| 🥉 Starter | 10,000 VPM | €500 | Kleine zelfstandigen |
| 🥈 Business | 50,000 VPM | €2,000 | Middelgrote winkels |
| 🥇 Premium | 250,000 VPM | €7,500 | Ketens & franchises |

### ROI Indicatie

Bij 200 actieve klanten met +20% retentie-uplift door VPM:

```
Zonder VPM:  €120,000 jaaromzet
Met VPM:     €144,000 jaaromzet  (+€24,000)
Investering: €2,000/jaar
Netto winst: +€22,000/jaar
```

📧 **Aanmelden:** [partners@vpmcoin.be](mailto:partners@vpmcoin.be)
🌐 **Meer info:** [www.vpmcoin.be/handelaar](https://www.vpmcoin.be/handelaar)

---

## 🔒 Beveiliging

### Ingebouwde bescherming

- ✅ **Role-based access control** — owner en merchant rollen strikt gescheiden
- ✅ **Vaste supply** — geen mint functie na deployment, supply onveranderlijk
- ✅ **Zero-address checks** — op alle externe adressen
- ✅ **Overflow bescherming** — Solidity 0.8.x ingebouwde overflow checks
- ✅ **Reentrancy-veilig** — state updates voor externe calls

### Aanbevelingen voor productie

> ⚠️ **Audit vereist voor mainnet deployment.**

- [ ] Externe security audit (OpenZeppelin, Certik, of equivalent)
- [ ] Multisig wallet voor `owner` adres (Gnosis Safe aanbevolen)
- [ ] Bug bounty programma lanceren voor community review
- [ ] Formele verificatie van kritieke functies

### Bekende beperkingen

- Gas fees op Ethereum Mainnet kunnen hoog zijn bij drukke periodes — Layer-2 migratie staat op de roadmap
- Het contract heeft geen upgrade-mechanisme (intentioneel voor vertrouwen)

---

## ⚖️ Juridisch

VPM Coin is ontworpen als een **utility token**, niet als een financieel instrument of waardepapier.

| Aspect | Status |
|---|---|
| **MiCA classificatie** | Utility token |
| **GDPR** | Pseudoniem (walletadressen), geen PII on-chain |
| **Fiscaal (BE)** | Loyaliteitsvoordelen doorgaans belastingvrij voor particulieren |
| **NBB** | Geen banklicentie vereist voor utility tokens |

> 📌 Raadpleeg een Belgisch advocatenkantoor gespecialiseerd in fintech/crypto voor finalisatie voor uw specifieke situatie.

---

## 📁 Repository Structuur

```
vpmcoin-contracts/
├── VPMCoin.sol                    # Hoofd smart contract
├── README.md                      # Deze documentatie
├── VPM_Coin_Whitepaper.docx       # Technisch & economisch whitepaper
├── VPM_Coin_Businessplan_Handelaars.docx  # Handelaars businessplan
├── scripts/
│   └── deploy.js                  # Deployment script
├── test/
│   └── VPMCoin.test.js            # Unit tests
└── docs/
    └── MERCHANT_GUIDE.md          # Handelaars handleiding
```

---

## 📞 Contact

<div align="center">

| | |
|---|---|
| 🌐 Website | [www.vpmcoin.be](https://www.vpmcoin.be) |
| 📧 Algemeen | [info@vpmcoin.be](mailto:info@vpmcoin.be) |
| 🤝 Handelaars | [partners@vpmcoin.be](mailto:partners@vpmcoin.be) |
| 🔐 Security | [security@vpmcoin.be](mailto:security@vpmcoin.be) |
| 🐦 Twitter/X | [@VPMCoin](https://twitter.com/vpmcoin) |
| 💬 Telegram | [t.me/vpmcoin](https://t.me/vpmcoin) |

</div>

---

<div align="center">

**Gebouwd in Belgie 🇧🇪 — voor Belgische handelaars**

*VPM Coin Foundation — 2025*

[![MIT License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)
[![ERC-20](https://img.shields.io/badge/ERC--20-Compliant-blue?style=flat-square)](https://eips.ethereum.org/EIPS/eip-20)
[![Solidity](https://img.shields.io/badge/Solidity-0.8.20-363636?style=flat-square)](https://soliditylang.org/)

</div>
