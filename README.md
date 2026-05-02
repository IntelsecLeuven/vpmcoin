# vpmcoin

<style>
  @import url('https://fonts.googleapis.com/css2?family=Syne:wght@400;700;800&family=DM+Sans:wght@300;400;500&display=swap');
  *{box-sizing:border-box;margin:0;padding:0}
  .vpm-wrap{font-family:'DM Sans',sans-serif;color:var(--color-text-primary);padding:0 0 3rem}
  .hero{background:linear-gradient(135deg,#0a1628 0%,#0d2244 50%,#0a1628 100%);border-radius:var(--border-radius-lg);padding:3.5rem 3rem 3rem;position:relative;overflow:hidden;margin-bottom:2rem}
  .hero-bg{position:absolute;inset:0;background:radial-gradient(circle at 80% 40%,rgba(255,193,7,0.12) 0%,transparent 60%),radial-gradient(circle at 20% 80%,rgba(30,100,255,0.1) 0%,transparent 50%)}
  .coin-badge{display:inline-flex;align-items:center;gap:10px;background:rgba(255,193,7,0.15);border:1px solid rgba(255,193,7,0.35);border-radius:40px;padding:6px 18px 6px 10px;margin-bottom:1.5rem}
  .coin-icon{width:28px;height:28px;background:#FFC107;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:14px;font-weight:800;color:#0a1628;font-family:'Syne',sans-serif}
  .coin-badge-text{font-size:12px;font-weight:500;color:#FFC107;letter-spacing:1.5px;text-transform:uppercase}
  .hero h1{font-family:'Syne',sans-serif;font-size:2.8rem;font-weight:800;color:#fff;line-height:1.1;margin-bottom:0.5rem}
  .hero h1 span{color:#FFC107}
  .hero-sub{font-size:1rem;color:rgba(255,255,255,0.6);font-weight:300;max-width:480px;line-height:1.6;margin-bottom:2rem}
  .hero-stats{display:grid;grid-template-columns:repeat(3,1fr);gap:1px;background:rgba(255,255,255,0.08);border-radius:var(--border-radius-md);overflow:hidden;border:1px solid rgba(255,255,255,0.08)}
  .hstat{background:#0d1e3a;padding:1.2rem 1rem;text-align:center}
  .hstat-val{font-family:'Syne',sans-serif;font-size:1.5rem;font-weight:700;color:#FFC107;display:block}
  .hstat-lbl{font-size:11px;color:rgba(255,255,255,0.45);text-transform:uppercase;letter-spacing:1px;margin-top:2px;display:block}
  .section{margin-bottom:2rem}
  .section-label{font-size:11px;text-transform:uppercase;letter-spacing:2px;color:var(--color-text-secondary);margin-bottom:1rem;display:flex;align-items:center;gap:8px}
  .section-label::after{content:'';flex:1;height:1px;background:var(--color-border-tertiary)}
  .cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(180px,1fr));gap:12px}
  .card{background:var(--color-background-primary);border:0.5px solid var(--color-border-tertiary);border-radius:var(--border-radius-lg);padding:1.25rem}
  .card-icon{width:36px;height:36px;border-radius:8px;display:flex;align-items:center;justify-content:center;margin-bottom:0.85rem;font-size:18px}
  .card-icon.gold{background:rgba(255,193,7,0.12)}
  .card-icon.blue{background:rgba(24,95,165,0.12)}
  .card-icon.green{background:rgba(57,150,30,0.12)}
  .card-icon.red{background:rgba(220,60,50,0.12)}
  .card h3{font-size:14px;font-weight:500;margin-bottom:4px}
  .card p{font-size:12px;color:var(--color-text-secondary);line-height:1.5}
  .how-it-works{background:var(--color-background-secondary);border-radius:var(--border-radius-lg);padding:1.75rem;margin-bottom:2rem;border:0.5px solid var(--color-border-tertiary)}
  .steps{display:grid;grid-template-columns:repeat(auto-fit,minmax(140px,1fr));gap:1rem}
  .step{text-align:center;position:relative}
  .step-num{width:40px;height:40px;border-radius:50%;background:#FFC107;color:#0a1628;font-family:'Syne',sans-serif;font-weight:800;font-size:16px;display:flex;align-items:center;justify-content:center;margin:0 auto 0.75rem}
  .step h4{font-size:13px;font-weight:500;margin-bottom:3px}
  .step p{font-size:11px;color:var(--color-text-secondary);line-height:1.4}
  .step-arrow{position:absolute;right:-12px;top:18px;color:var(--color-text-secondary);font-size:14px}
  .reward-box{background:linear-gradient(135deg,#0a1628,#0d2244);border:1px solid rgba(255,193,7,0.25);border-radius:var(--border-radius-lg);padding:2rem;display:flex;align-items:center;gap:2rem;margin-bottom:2rem;flex-wrap:wrap}
  .reward-coin{width:80px;height:80px;background:radial-gradient(circle at 35% 35%,#FFD54F,#FF8F00);border-radius:50%;display:flex;align-items:center;justify-content:center;font-family:'Syne',sans-serif;font-size:22px;font-weight:800;color:#fff;flex-shrink:0;box-shadow:0 0 30px rgba(255,193,7,0.3)}
  .reward-text h3{font-family:'Syne',sans-serif;font-size:1.4rem;font-weight:700;color:#fff;margin-bottom:4px}
  .reward-text p{font-size:13px;color:rgba(255,255,255,0.6);line-height:1.5}
  .reward-badge{margin-top:12px;display:inline-block;background:rgba(255,193,7,0.15);border:1px solid rgba(255,193,7,0.3);border-radius:20px;padding:4px 14px;font-size:12px;color:#FFC107;font-weight:500}
  .tokenomics{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-bottom:2rem}
  .tcard{background:var(--color-background-primary);border:0.5px solid var(--color-border-tertiary);border-radius:var(--border-radius-lg);padding:1.25rem}
  .tcard-label{font-size:11px;text-transform:uppercase;letter-spacing:1px;color:var(--color-text-secondary);margin-bottom:4px}
  .tcard-val{font-family:'Syne',sans-serif;font-size:1.3rem;font-weight:700}
  .tcard-val.gold{color:#FF8F00}
  .tcard-val.blue{color:#185FA5}
  .bar-row{margin-top:10px;height:6px;background:var(--color-background-secondary);border-radius:3px;overflow:hidden}
  .bar-fill{height:100%;border-radius:3px}
  .cta-row{display:flex;gap:12px;flex-wrap:wrap}
  .btn-primary{flex:1;min-width:160px;padding:14px 24px;background:#FFC107;color:#0a1628;font-family:'Syne',sans-serif;font-weight:700;font-size:14px;border:none;border-radius:var(--border-radius-md);cursor:pointer;letter-spacing:0.5px;transition:opacity 0.15s}
  .btn-primary:hover{opacity:0.88}
  .btn-secondary{flex:1;min-width:160px;padding:14px 24px;background:transparent;color:var(--color-text-primary);font-family:'DM Sans',sans-serif;font-weight:500;font-size:14px;border:0.5px solid var(--color-border-secondary);border-radius:var(--border-radius-md);cursor:pointer;transition:background 0.15s}
  .btn-secondary:hover{background:var(--color-background-secondary)}
  .flag{display:inline-block;margin-right:5px}
</style>

<div class="vpm-wrap">

  <div class="hero">
    <div class="hero-bg"></div>
    <div style="position:relative;z-index:1">
      <div class="coin-badge">
        <div class="coin-icon">V</div>
        <span class="coin-badge-text">Initial Coin Offering · ERC-20</span>
      </div>
      <h1>VPM <span>Coin</span></h1>
      <p style="font-family:'Syne',sans-serif;font-size:1rem;color:rgba(255,255,255,0.5);letter-spacing:2px;text-transform:uppercase;margin-bottom:0.5rem">Virtual Private Money</p>
      <p class="hero-sub">De eerste Belgische loyalty token op de Ethereum blockchain — waarmee handelaars hun klanten belonen bij elke aankoop.</p>
      <div class="hero-stats">
        <div class="hstat"><span class="hstat-val">ERC-20</span><span class="hstat-lbl">Token standaard</span></div>
        <div class="hstat"><span class="hstat-val">100 VPM</span><span class="hstat-lbl">= €10 korting</span></div>
        <div class="hstat"><span class="hstat-val"><span class="flag">🇧🇪</span>BE</span><span class="hstat-lbl">Focusmarkt</span></div>
      </div>
    </div>
  </div>

  <div class="section">
    <div class="section-label">Waarom VPM Coin</div>
    <div class="cards">
      <div class="card">
        <div class="card-icon gold">🏆</div>
        <h3>Loyaliteit on-chain</h3>
        <p>Tokens worden on-chain bijgehouden. Geen pas, geen app — enkel een wallet.</p>
      </div>
      <div class="card">
        <div class="card-icon blue">🔗</div>
        <h3>Universele inwisseling</h3>
        <p>Elke VPM-aangesloten handelaar in België aanvaardt tokens als betaalmiddel.</p>
      </div>
      <div class="card">
        <div class="card-icon green">🛡️</div>
        <h3>Transparant & veilig</h3>
        <p>Ethereum blockchain garandeert onveranderlijkheid en fraude-resistentie.</p>
      </div>
      <div class="card">
        <div class="card-icon red">📈</div>
        <h3>Groeinetwerk</h3>
        <p>Hoe meer handelaars, hoe meer waarde voor elke tokenhouder in het netwerk.</p>
      </div>
    </div>
  </div>

  <div class="section">
    <div class="section-label">Hoe het werkt</div>
    <div class="how-it-works">
      <div class="steps">
        <div class="step">
          <div class="step-num">1</div>
          <h4>Aankoop</h4>
          <p>Klant koopt bij een VPM-handelaar</p>
          <span class="step-arrow">→</span>
        </div>
        <div class="step">
          <div class="step-num">2</div>
          <h4>Tokens ontvangen</h4>
          <p>VPM Coins worden automatisch gestort</p>
          <span class="step-arrow">→</span>
        </div>
        <div class="step">
          <div class="step-num">3</div>
          <h4>100 tokens</h4>
          <p>Klant bereikt de inwisselgrens</p>
          <span class="step-arrow">→</span>
        </div>
        <div class="step">
          <div class="step-num">4</div>
          <h4>€10 korting</h4>
          <p>Bij elke aangesloten handelaar te gebruiken</p>
        </div>
      </div>
    </div>
  </div>

  <div class="reward-box">
    <div class="reward-coin">VPM</div>
    <div class="reward-text">
      <h3>100 tokens = €10 aankoop</h3>
      <p>Zodra een klant 100 VPM Coins heeft verzameld, kan hij of zij voor €10 aankopen doen bij gelijk welke aangesloten handelaar in het VPM netwerk — zonder extra kosten.</p>
      <span class="reward-badge">Geldig bij alle VPM-partners in België</span>
    </div>
  </div>

  <div class="section">
    <div class="section-label">Token parameters</div>
    <div class="tokenomics">
      <div class="tcard">
        <div class="tcard-label">Netwerk</div>
        <div class="tcard-val blue">Ethereum</div>
        <div class="bar-row"><div class="bar-fill" style="width:100%;background:#185FA5"></div></div>
      </div>
      <div class="tcard">
        <div class="tcard-label">Standaard</div>
        <div class="tcard-val gold">ERC-20</div>
        <div class="bar-row"><div class="bar-fill" style="width:80%;background:#FF8F00"></div></div>
      </div>
      <div class="tcard">
        <div class="tcard-label">Inwisselwaarde</div>
        <div class="tcard-val gold">€0,10 / token</div>
        <div class="bar-row"><div class="bar-fill" style="width:60%;background:#FF8F00"></div></div>
      </div>
      <div class="tcard">
        <div class="tcard-label">Markt</div>
        <div class="tcard-val" style="color:var(--color-text-success)">België 🇧🇪</div>
        <div class="bar-row"><div class="bar-fill" style="width:50%;background:#3b6d11"></div></div>
      </div>
    </div>
  </div>

  <div class="section">
    <div class="section-label">Deelnemen</div>
    <div class="cta-row">
      <button class="btn-primary" onclick="sendPrompt('Hoe kan ik als handelaar aansluiten bij het VPM Coin netwerk?')">Word handelaar-partner ↗</button>
      <button class="btn-secondary" onclick="sendPrompt('Hoe werkt de technische integratie van VPM Coin in mijn kassasysteem?')">Technische integratie</button>
      <button class="btn-secondary" onclick="sendPrompt('Wat zijn de juridische en fiscale aspecten van VPM Coin in België?')">Juridisch & fiscaal</button>
    </div>
  </div>

</div>
