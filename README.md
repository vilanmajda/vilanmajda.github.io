# bled-outdoors.github.io
Hike. Climb. Ride. Fly. Experience the best outdoor adventures around Bled.
<!DOCTYPE html>
<html lang="sl">
<head>
  <meta charset="UTF-8" />
  <title>Gorski Izleti – Rezervacije & Plačilo</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style>
    :root {
      --bg: #0b1220;
      --bg-alt: #111827;
      --accent: #22c55e;
      --accent-soft: rgba(34,197,94,0.15);
      --text: #f9fafb;
      --muted: #9ca3af;
      --card-bg: #020617;
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background: radial-gradient(circle at top, #1e293b 0, #020617 55%, #000 100%);
      color: var(--text);
    }

    a {
      color: inherit;
    }

    header {
      position: sticky;
      top: 0;
      z-index: 50;
      backdrop-filter: blur(12px);
      background: linear-gradient(to bottom, rgba(15,23,42,0.95), rgba(15,23,42,0.7));
      border-bottom: 1px solid rgba(148,163,184,0.2);
    }

    .nav-inner {
      max-width: 1100px;
      margin: 0 auto;
      padding: 10px 16px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 16px;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 10px;
      font-weight: 600;
      letter-spacing: 0.04em;
      font-size: 16px;
    }

    .logo-mark {
      width: 32px;
      height: 32px;
      border-radius: 999px;
      background: radial-gradient(circle at 30% 20%, #4ade80, #22c55e 40%, #166534 100%);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 18px;
    }

    .nav-links {
      display: flex;
      gap: 18px;
      font-size: 14px;
    }

    .nav-links a {
      text-decoration: none;
      color: var(--muted);
      padding-bottom: 4px;
      border-bottom: 1px solid transparent;
    }

    .nav-links a:hover {
      color: var(--text);
      border-color: rgba(148,163,184,0.7);
    }

    .nav-cta {
      display: flex;
      align-items: center;
      gap: 10px;
      font-size: 13px;
    }

    .badge {
      font-size: 11px;
      padding: 3px 9px;
      border-radius: 999px;
      border: 1px solid rgba(148,163,184,0.6);
      color: var(--muted);
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 6px;
      padding: 9px 16px;
      border-radius: 999px;
      border: none;
      cursor: pointer;
      font-size: 14px;
      text-decoration: none;
      background: var(--accent);
      color: #022c22;
      font-weight: 500;
      box-shadow: 0 14px 30px rgba(34,197,94,0.35);
      transition: transform 0.12s ease, box-shadow 0.12s ease, opacity 0.12s ease;
      white-space: nowrap;
    }

    .btn:hover {
      transform: translateY(-1px);
      box-shadow: 0 18px 40px rgba(34,197,94,0.45);
      opacity: 0.97;
    }

    .btn-outline {
      background: transparent;
      border: 1px solid rgba(148,163,184,0.8);
      color: var(--muted);
      box-shadow: none;
    }

    .btn-outline:hover {
      border-color: var(--accent);
      color: var(--text);
    }

    main {
      max-width: 1100px;
      margin: 0 auto;
      padding: 24px 16px 80px;
    }

    .hero {
      display: grid;
      grid-template-columns: minmax(0, 1.4fr) minmax(0, 1fr);
      gap: 32px;
      align-items: center;
      padding: 32px 0 10px;
    }

    @media (max-width: 880px) {
      .hero {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    .hero-kicker {
      font-size: 12px;
      text-transform: uppercase;
      letter-spacing: 0.25em;
      color: var(--muted);
      margin-bottom: 10px;
    }

    .hero-title {
      font-size: clamp(32px, 4vw, 40px);
      line-height: 1.1;
      margin: 0 0 12px;
    }

    .hero-title span {
      color: #4ade80;
    }

    .hero-subtitle {
      font-size: 15px;
      color: var(--muted);
      max-width: 32rem;
      margin-bottom: 18px;
    }

    .hero-cta-row {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-bottom: 14px;
    }

    .hero-note {
      font-size: 12px;
      color: #6b7280;
    }

    .hero-media {
      position: relative;
      border-radius: 24px;
      overflow: hidden;
      border: 1px solid rgba(148,163,184,0.18);
      background: radial-gradient(circle at top, #064e3b 0, #020617 40%, #000 100%);
      padding: 18px;
      min-height: 220px;
      box-shadow: 0 20px 40px rgba(15,23,42,0.7);
    }

    .hero-media-inner {
      border-radius: 18px;
      border: 1px solid rgba(148,163,184,0.3);
      padding: 16px;
      background: linear-gradient(to bottom right, rgba(15,23,42,0.9), rgba(6,78,59,0.75));
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      gap: 16px;
    }

    .pill {
      font-size: 11px;
      padding: 5px 9px;
      border-radius: 999px;
      background: rgba(15,23,42,0.9);
      border: 1px solid rgba(148,163,184,0.5);
      display: inline-flex;
      align-items: center;
      gap: 6px;
      color: var(--muted);
    }

    .stat-row {
      display: flex;
      flex-wrap: wrap;
      gap: 16px;
      font-size: 12px;
      color: var(--muted);
    }

    .stat-box {
      flex: 1 1 80px;
      padding: 10px 12px;
      border-radius: 12px;
      background: rgba(15,23,42,0.95);
      border: 1px solid rgba(148,163,184,0.4);
    }

    .stat-label {
      font-size: 11px;
      color: #9ca3af;
    }

    .stat-value {
      font-size: 14px;
      font-weight: 600;
      color: #e5e7eb;
    }

    .offer-section {
      margin-top: 40px;
    }

    .section-eyebrow {
      font-size: 11px;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: var(--muted);
      margin-bottom: 6px;
    }

    .section-title {
      font-size: 22px;
      margin: 0 0 4px;
    }

    .section-subtitle {
      font-size: 14px;
      color: var(--muted);
      margin-bottom: 18px;
    }

    .offer-grid {
      display: grid;
      grid-template-columns: repeat(4, minmax(0,1fr));
      gap: 18px;
    }

    @media (max-width: 1000px) {
      .offer-grid {
        grid-template-columns: repeat(2, minmax(0,1fr));
      }
    }

    @media (max-width: 640px) {
      .offer-grid {
        grid-template-columns: minmax(0,1fr);
      }
    }

    .offer-card {
      border-radius: 18px;
      background: radial-gradient(circle at top left, rgba(34,197,94,0.08), rgba(15,23,42,0.9));
      border: 1px solid rgba(148,163,184,0.4);
      padding: 16px;
      display: flex;
      flex-direction: column;
      gap: 8px;
      position: relative;
      overflow: hidden;
    }

    .offer-badge {
      font-size: 11px;
      color: #bbf7d0;
      padding: 3px 8px;
      border-radius: 999px;
      background: rgba(34,197,94,0.16);
      display: inline-block;
      align-self: flex-start;
    }

    .offer-title {
      font-size: 15px;
      font-weight: 600;
    }

    .offer-meta {
      font-size: 12px;
      color: var(--muted);
    }

    .offer-price-row {
      display: flex;
      align-items: baseline;
      justify-content: space-between;
      gap: 6px;
      margin-top: 4px;
    }

    .offer-price {
      font-size: 18px;
      font-weight: 600;
    }

    .offer-per {
      font-size: 12px;
      color: var(--muted);
    }

    .offer-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 10px;
    }

    .pill-soft {
      font-size: 11px;
      padding: 4px 8px;
      border-radius: 999px;
      background: rgba(15,23,42,0.85);
      border: 1px solid rgba(148,163,184,0.5);
      color: var(--muted);
    }

    .highlight-section {
      margin-top: 40px;
      border-radius: 24px;
      background: radial-gradient(circle at top left, rgba(34,197,94,0.12), rgba(15,23,42,0.95));
      border: 1px solid rgba(148,163,184,0.45);
      padding: 18px 18px 16px;
      display: grid;
      grid-template-columns: minmax(0, 1.6fr) minmax(0, 1fr);
      gap: 16px;
      align-items: center;
    }

    @media (max-width: 880px) {
      .highlight-section {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    .badge-green {
      font-size: 11px;
      padding: 4px 10px;
      border-radius: 999px;
      background: var(--accent-soft);
      color: #bbf7d0;
      border: 1px solid rgba(74,222,128,0.7);
      display: inline-flex;
      align-items: center;
      gap: 6px;
      margin-bottom: 8px;
    }

    .highlight-list {
      display: grid;
      grid-template-columns: repeat(2, minmax(0,1fr));
      gap: 10px;
      font-size: 12px;
      color: var(--muted);
    }

    @media (max-width: 640px) {
      .highlight-list {
        grid-template-columns: minmax(0,1fr);
      }
    }

    .highlight-item {
      display: flex;
      align-items: flex-start;
      gap: 8px;
    }

    .dot {
      width: 16px;
      height: 16px;
      border-radius: 999px;
      background: rgba(34,197,94,0.22);
      border: 1px solid rgba(74,222,128,0.8);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 12px;
      flex-shrink: 0;
    }

    .highlight-aside {
      font-size: 12px;
      color: var(--muted);
      border-radius: 16px;
      background: rgba(15,23,42,0.9);
      border: 1px dashed rgba(148,163,184,0.7);
      padding: 12px;
    }

    .highlight-aside strong {
      color: #e5e7eb;
    }

    .contact-section {
      margin-top: 40px;
      display: grid;
      grid-template-columns: minmax(0,1.4fr) minmax(0,1fr);
      gap: 24px;
    }

    @media (max-width: 880px) {
      .contact-section {
        grid-template-columns: minmax(0,1fr);
      }
    }

    .contact-card {
      border-radius: 20px;
      background: rgba(15,23,42,0.95);
      border: 1px solid rgba(148,163,184,0.45);
      padding: 18px;
      font-size: 14px;
      color: var(--muted);
    }

    .contact-card h3 {
      margin-top: 0;
      font-size: 18px;
      color: var(--text);
    }

    .contact-row {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 8px;
      margin-top: 10px;
      font-size: 13px;
    }

    .contact-label {
      font-weight: 500;
      color: #e5e7eb;
    }

    footer {
      border-top: 1px solid rgba(148,163,184,0.35);
      margin-top: 40px;
      padding: 16px 0 26px;
      font-size: 12px;
      color: var(--muted);
      text-align: center;
    }

    /* MODAL */

    .modal-backdrop {
      position: fixed;
      inset: 0;
      background: rgba(15,23,42,0.7);
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.15s ease;
      z-index: 80;
    }

    .modal {
      position: fixed;
      inset: 0;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 16px;
      pointer-events: none;
      z-index: 90;
    }

    .modal[aria-hidden="true"] {
      visibility: hidden;
    }

    .modal[aria-hidden="false"] {
      pointer-events: auto;
      visibility: visible;
    }

    .modal[aria-hidden="false"] .modal-backdrop {
      opacity: 1;
      pointer-events: auto;
    }

    .modal-content {
      width: 100%;
      max-width: 420px;
      border-radius: 20px;
      background: #020617;
      border: 1px solid rgba(148,163,184,0.65);
      box-shadow: 0 22px 60px rgba(15,23,42,0.9);
      padding: 18px 18px 16px;
      transform: translateY(16px);
      opacity: 0;
      transition: transform 0.18s ease, opacity 0.18s ease;
    }

    .modal[aria-hidden="false"] .modal-content {
      transform: translateY(0);
      opacity: 1;
    }

    .modal-header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 8px;
      margin-bottom: 10px;
    }

    .modal-title {
      font-size: 16px;
      font-weight: 600;
    }

    .modal-close {
      border-radius: 999px;
      border: 1px solid rgba(148,163,184,0.6);
      background: transparent;
      color: var(--muted);
      width: 26px;
      height: 26px;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      font-size: 16px;
      cursor: pointer;
    }

    .modal-label {
      font-size: 12px;
      color: var(--muted);
      margin-bottom: 2px;
    }

    .modal-tour {
      font-size: 13px;
      background: rgba(15,23,42,0.9);
      border-radius: 999px;
      padding: 6px 10px;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      border: 1px solid rgba(148,163,184,0.7);
      margin-bottom: 8px;
    }

    .modal-tour span {
      font-weight: 500;
      color: #e5e7eb;
    }

    .form-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0,1fr));
      gap: 8px 10px;
      margin-top: 6px;
      margin-bottom: 6px;
    }

    .form-grid-full {
      grid-column: 1 / -1;
    }

    input, select, textarea {
      width: 100%;
      padding: 7px 9px;
      border-radius: 10px;
      border: 1px solid rgba(55,65,81,0.9);
      background: #020617;
      color: var(--text);
      font-size: 13px;
      font-family: inherit;
    }

    input::placeholder,
    textarea::placeholder {
      color: #6b7280;
    }

    textarea {
      resize: vertical;
      min-height: 60px;
      max-height: 120px;
    }

    .modal-footer {
      display: flex;
      flex-direction: column;
      gap: 6px;
      margin-top: 10px;
    }

    .modal-footer-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      align-items: center;
      justify-content: space-between;
    }

    .small-text {
      font-size: 11px;
      color: var(--muted);
    }

    .link-plain {
      font-size: 12px;
      text-decoration: underline;
      text-decoration-style: dotted;
      cursor: pointer;
    }

    .link-plain:hover {
      color: #e5e7eb;
    }

    @media (max-width: 480px) {
      .nav-links {
        display: none;
      }

      .nav-inner {
        justify-content: space-between;
      }
    }
  </style>
</head>
<body>
  <header>
    <div class="nav-inner">
      <div class="logo">
        <div class="logo-mark">⛰️</div>
        <div>GORSKI IZLETI</div>
      </div>
      <nav class="nav-links">
        <a href="#ponudba">Ponudba</a>
        <a href="#rezervacija">Rezervacija</a>
        <a href="#kontakt">Kontakt</a>
      </nav>
      <div class="nav-cta">
        <div class="badge">Majhne skupine · Lokalni vodnik</div>
        <a href="#rezervacija" class="btn">Rezerviraj izlet</a>
      </div>
    </div>
  </header>

  <main>
    <!-- HERO -->
    <section class="hero">
      <div>
        <div class="hero-kicker">Vodeni izleti v slovenske gore</div>
        <h1 class="hero-title">
          Varno v hribe, <span>brez organizacijskega stresa.</span>
        </h1>
        <p class="hero-subtitle">
          Izberi enega od štirih skrbno pripravljenih gorskih izletov, potrdi termin in po
          želji plačaj vnaprej – vse na eni strani.
        </p>

        <div class="hero-cta-row">
          <a href="#ponudba" class="btn">Poglej ponudbo</a>
          <a href="#rezervacija" class="btn btn-outline">Hitra rezervacija</a>
        </div>

        <div class="hero-note">
          ✔ Vključeno spremstvo licenciranega vodnika · ✔ Majhne skupine · ✔ Možnost
          predplačila preko spleta
        </div>
      </div>

      <div class="hero-media">
        <div class="hero-media-inner">
          <div class="pill">
            <span>✅</span> Rezervacije & predplačila sprejemamo za sezono 2026
          </div>

          <div class="stat-row">
            <div class="stat-box">
              <div class="stat-label">Lanski gorniki</div>
              <div class="stat-value">320+</div>
            </div>
            <div class="stat-box">
              <div class="stat-label">Povpr. ocena</div>
              <div class="stat-value">4.9 ★</div>
            </div>
            <div class="stat-box">
              <div class="stat-label">Max. velikost skupine</div>
              <div class="stat-value">8 oseb</div>
            </div>
          </div>

          <div class="stat-row">
            <div class="stat-box">
              <div class="stat-label">Zavarovana pot</div>
              <div class="stat-value">po dogovoru</div>
            </div>
            <div class="stat-box">
              <div class="stat-label">Možnost predplačila</div>
              <div class="stat-value">✔ na spletu</div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- PONUDBA -->
    <section id="ponudba" class="offer-section">
      <div class="section-eyebrow">Naša ponudba</div>
      <h2 class="section-title">4 gorski izleti za različne okuse</h2>
      <p class="section-subtitle">
        Izbereš termin, število oseb in nam pošlješ rezervacijo. Po potrditvi ti pošljemo račun
        ali povezavo za predplačilo.
      </p>

      <div class="offer-grid">
        <!-- IZLET 1 -->
        <article
          class="offer-card"
          data-tour-name="Sončni vzhod na vrhu"
          data-tour-id="svit"
          data-price="129"
          data-payment-link="https://primer.tvoja-povezava-za-placilo-1.com"
        >
          <span class="offer-badge">Najbolj priljubljen</span>
          <h3 class="offer-title">Sončni vzhod na vrhu</h3>
          <div class="offer-meta">
            Zgodnje jutro, lahka do srednje zahtevna tura z razgledom nad morjem oblakov. Idealno
            za dobro fizično pripravljene.
          </div>
          <div class="offer-price-row">
            <div>
              <span class="offer-price">129 €</span>
              <span class="offer-per">/ osebo</span>
            </div>
            <div class="pill-soft">5–6 h · 700–900 m višine</div>
          </div>
          <div class="offer-actions">
            <button class="btn book-btn" type="button">Rezerviraj</button>
            <button class="btn btn-outline pay-btn" type="button">Plačaj vnaprej</button>
          </div>
        </article>

        <!-- IZLET 2 -->
        <article
          class="offer-card"
          data-tour-name="Družinski pohod na planino"
          data-tour-id="druzina"
          data-price="89"
          data-payment-link="https://primer.tvoja-povezava-za-placilo-2.com"
        >
          <span class="offer-badge">Za družine</span>
          <h3 class="offer-title">Družinski pohod na planino</h3>
          <div class="offer-meta">
            Nežen vzpon do planine z igrišči, živalmi in kočo. Primerno za otroke od 5 let dalje.
          </div>
          <div class="offer-price-row">
            <div>
              <span class="offer-price">89 €</span>
              <span class="offer-per">/ odraslega</span>
            </div>
            <div class="pill-soft">3–4 h · 400 m višine</div>
          </div>
          <div class="offer-actions">
            <button class="btn book-btn" type="button">Rezerviraj</button>
            <button class="btn btn-outline pay-btn" type="button">Plačaj vnaprej</button>
          </div>
        </article>

        <!-- IZLET 3 -->
        <article
          class="offer-card"
          data-tour-name="Vikend tura v Julijce"
          data-tour-id="vikend"
          data-price="249"
          data-payment-link="https://primer.tvoja-povezava-za-placilo-3.com"
        >
          <span class="offer-badge">2-dnevna tura</span>
          <h3 class="offer-title">Vikend tura v Julijce</h3>
          <div class="offer-meta">
            Dvodnevna tura s spanjem v koči. Za pohodnike, ki si želijo malo daljše gorske
            avanture.
          </div>
          <div class="offer-price-row">
            <div>
              <span class="offer-price">249 €</span>
              <span class="offer-per">/ osebo</span>
            </div>
            <div class="pill-soft">2 dni · 1200 m višine</div>
          </div>
          <div class="offer-actions">
            <button class="btn book-btn" type="button">Rezerviraj</button>
            <button class="btn btn-outline pay-btn" type="button">Plačaj vnaprej</button>
          </div>
        </article>

        <!-- IZLET 4 -->
        <article
          class="offer-card"
          data-tour-name="Zimski snežni pohod"
          data-tour-id="zima"
          data-price="139"
          data-payment-link="https://primer.tvoja-povezava-za-placilo-4.com"
        >
          <span class="offer-badge">S krpljami</span>
          <h3 class="offer-title">Zimski snežni pohod</h3>
          <div class="offer-meta">
            Zimski pohod s krpljami in toplim čajem. Primeren za začetnike, oprema je vključena.
          </div>
          <div class="offer-price-row">
            <div>
              <span class="offer-price">139 €</span>
              <span class="offer-per">/ osebo</span>
            </div>
            <div class="pill-soft">3–4 h · krplje vključene</div>
          </div>
          <div class="offer-actions">
            <button class="btn book-btn" type="button">Rezerviraj</button>
            <button class="btn btn-outline pay-btn" type="button">Plačaj vnaprej</button>
          </div>
        </article>
      </div>
    </section>

    <!-- REZERVACIJA / PREDPLAČILO INFO -->
    <section id="rezervacija" class="highlight-section">
      <div>
        <div class="badge-green">
          💳 Predplačilo po potrjeni rezervaciji
        </div>
        <h2 class="section-title">Kako poteka rezervacija & plačilo</h2>
        <p class="section-subtitle">
          Rezervacijski obrazec nam pošlješ kot e-pošto. Mi ti odgovorimo s potrditvijo in povezavo
          za varno predplačilo (npr. bančno nakazilo, PayPal, Stripe …).
        </p>

        <div class="highlight-list">
          <div class="highlight-item">
            <div class="dot">1</div>
            <div>
              <strong>Izberi izlet</strong><br />
              v razdelku <em>Naša ponudba</em> klikneš na gumb <em>Rezerviraj</em> pri izbranem
              izletu.
            </div>
          </div>
          <div class="highlight-item">
            <div class="dot">2</div>
            <div>
              <strong>Izpolni obrazec</strong><br />
              izbereš termin, število oseb in dopišeš morebitne posebnosti (otroci, psi, želje …).
            </div>
          </div>
          <div class="highlight-item">
            <div class="dot">3</div>
            <div>
              <strong>Pošlji rezervacijo</strong><br />
              klik na <em>Pošlji rezervacijo</em> odpre tvoj e-poštni program z vnaprej izpolnjenimi
              podatki.
            </div>
          </div>
          <div class="highlight-item">
            <div class="dot">4</div>
            <div>
              <strong>Predplačilo</strong><br />
              po e-pošti ti pošljemo točne podatke za plačilo (račun ali povezavo za plačilo s
              kartico).
            </div>
          </div>
        </div>
      </div>

      <aside class="highlight-aside">
        <strong>Opomba za lastnika strani:</strong><br />
        predplačilo lahko urediš brez lastnega strežnika – z uporabo ponudnikov kot so PayPal,
        Stripe, Revolut Pay ali klasično bančno nakazilo. V kodo samo vpišeš svoje povezave za
        plačilo (glej spodaj v razlagi).
      </aside>
    </section>

    <!-- KONTAKT -->
    <section id="kontakt" class="contact-section">
      <div class="contact-card">
        <h3>Kontakt & vprašanja</h3>
        <p>
          Za dodatna vprašanja ali individualne ture nam piši ali pokliči. Z veseljem se prilagodimo
          tvojemu znanju in željam.
        </p>

        <div class="contact-row">
          <div>
            <div class="contact-label">E-pošta</div>
            <div>info@tvoji-izleti.si</div>
          </div>
          <a href="mailto:info@tvoji-izleti.si" class="btn btn-outline">Pošlji e-pošto</a>
        </div>

        <div class="contact-row">
          <div>
            <div class="contact-label">Telefon / WhatsApp</div>
            <div>+386 40 000 000</div>
          </div>
          <a href="tel:+38640000000" class="btn btn-outline">Pokliči</a>
        </div>

        <div style="margin-top: 14px; font-size: 12px;">
          📍 Tipična izhodišča: Gorenjska (Krnsko pogorje, Karavanke, Julijske Alpe) – po dogovoru
          tudi drugje.
        </div>
      </div>

      <div class="contact-card">
        <h3>Informacije za plačilo</h3>
        <p style="margin-bottom: 10px;">
          Tu lahko navedeš osnovne podatke, ki jih stranke potrebujejo za nakazilo.
        </p>
        <ul style="padding-left: 18px; margin: 0; font-size: 13px;">
          <li>Podjetje ali ime in priimek</li>
          <li>Naslov</li>
          <li>IBAN in banka</li>
          <li>Davčna številka (po potrebi)</li>
        </ul>
      </div>
    </section>
  </main>

  <!-- MODAL: REZERVACIJA -->
  <div class="modal" id="booking-modal" aria-hidden="true">
    <div class="modal-backdrop"></div>
    <div class="modal-content">
      <div class="modal-header">
        <div>
          <div class="modal-title">Rezervacija izleta</div>
          <div class="small-text">
            Izpolni podatke in pritisni <strong>Pošlji rezervacijo</strong>.
          </div>
        </div>
        <button class="modal-close" type="button" aria-label="Zapri">×</button>
      </div>

      <div class="modal-label">Izbran izlet</div>
      <div class="modal-tour">
        <span id="modal-tour-name">—</span>
        <span style="font-size:11px; color:#9ca3af;" id="modal-tour-price"></span>
      </div>

      <form id="booking-form">
        <div class="form-grid">
          <div class="form-grid-full">
            <label class="modal-label" for="date">Želeni datum</label>
            <input type="date" id="date" name="date" required />
          </div>

          <div>
            <label class="modal-label" for="people">Število oseb</label>
            <input type="number" id="people" name="people" min="1" value="2" required />
          </div>

          <div>
            <label class="modal-label" for="name">Ime in priimek</label>
            <input
              type="text"
              id="name"
              name="name"
              placeholder="Ime in priimek"
              required
            />
          </div>

          <div>
            <label class="modal-label" for="email">E-pošta</label>
            <input
              type="email"
              id="email"
              name="email"
              placeholder="tvoj@email.com"
              required
            />
          </div>

          <div>
            <label class="modal-label" for="phone">Telefon</label>
            <input
              type="tel"
              id="phone"
              name="phone"
              placeholder="+386 ..."
            />
          </div>

          <div class="form-grid-full">
            <label class="modal-label" for="note">Opombe (otroci, psi, želje …)</label>
            <textarea
              id="note"
              name="note"
              placeholder="Npr.: 2 odrasla, 2 otroka (7 in 10 let), radi bi bolj umirjen tempo."
            ></textarea>
          </div>
        </div>

        <input type="hidden" id="tour-id" name="tour-id" />
        <input type="hidden" id="tour-name" name="tour-name" />
        <input type="hidden" id="tour-price" name="tour-price" />

        <div class="modal-footer">
          <div class="modal-footer-row">
            <button class="btn" type="submit">Pošlji rezervacijo</button>
            <span class="small-text">
              S klikom se bo odprl tvoj e-poštni program z vnaprej izpolnjeno e-pošto.
            </span>
          </div>
          <div class="small-text">
            Predplačilo ni takoj obvezno – podatke za plačilo dobiš v povratnem e-mailu po
            potrditvi termina.
          </div>
        </div>
      </form>
    </div>
  </div>

  <footer>
    &copy; <span id="year"></span> Gorski izleti. Vse pravice pridržane.
  </footer>

  <script>
    // dinamično leto v footerju
    document.getElementById("year").textContent = new Date().getFullYear();

    // gladko skrolanje po sidrih
    document.querySelectorAll('a[href^="#"]').forEach(function (link) {
      link.addEventListener("click", function (e) {
        var targetId = this.getAttribute("href");
        if (targetId === "#") return;
        var target = document.querySelector(targetId);
        if (target) {
          e.preventDefault();
          window.scrollTo({
            top: target.offsetTop - 70,
            behavior: "smooth",
          });
        }
      });
    });

    // MODAL – odpiranje/zapiranje
    var modal = document.getElementById("booking-modal");
    var modalTourName = document.getElementById("modal-tour-name");
    var modalTourPrice = document.getElementById("modal-tour-price");

    var inputTourId = document.getElementById("tour-id");
    var inputTourName = document.getElementById("tour-name");
    var inputTourPrice = document.getElementById("tour-price");

    function openModal() {
      modal.setAttribute("aria-hidden", "false");
    }

    function closeModal() {
      modal.setAttribute("aria-hidden", "true");
    }

    document.querySelector(".modal-close").addEventListener("click", closeModal);
    modal.querySelector(".modal-backdrop").addEventListener("click", closeModal);

    // Gumbi "Rezerviraj"
    document.querySelectorAll(".book-btn").forEach(function (btn) {
      btn.addEventListener("click", function () {
        var card = this.closest(".offer-card");
        var name = card.getAttribute("data-tour-name");
        var price = card.getAttribute("data-price");
        var id = card.getAttribute("data-tour-id");

        modalTourName.textContent = name;
        modalTourPrice.textContent = "Približna cena: " + price + " € / osebo";
        inputTourId.value = id;
        inputTourName.value = name;
        inputTourPrice.value = price;

        openModal();
      });
    });

    // Gumbi "Plačaj vnaprej" – odprejo tvoj payment link
    document.querySelectorAll(".pay-btn").forEach(function (btn) {
      btn.addEventListener("click", function () {
        var card = this.closest(".offer-card");
        var link = card.getAttribute("data-payment-link");

        if (!link || link === "#" || link.indexOf("primer.tvoja-povezava") !== -1) {
          alert(
            "Povezava za plačilo še ni nastavljena.\nV HTML kodi zamenjaj data-payment-link z resnično povezavo (PayPal, Stripe, Revolut …)."
          );
          return;
        }

        window.open(link, "_blank");
      });
    });

    // Pošlji rezervacijo – sestavi mailto: link
    document.getElementById("booking-form").addEventListener("submit", function (e) {
      e.preventDefault();

      var tourName = inputTourName.value;
      var tourPrice = inputTourPrice.value;
      var tourId = inputTourId.value;
      var date = document.getElementById("date").value;
      var people = document.getElementById("people").value;
      var name = document.getElementById("name").value;
      var email = document.getElementById("email").value;
      var phone = document.getElementById("phone").value;
      var note = document.getElementById("note").value;

      // TODO: tukaj vpiši svoj pravi e-naslov, kamor želiš prejemati rezervacije
      var to = "info@tvoji-izleti.si";

      var subject = "Rezervacija gorskega izleta: " + tourName;
      var body =
        "Pozdravljeni,\n\nrad(a) bi rezerviral(a) naslednji izlet:\n\n" +
        "Izlet: " + tourName + " (" + tourId + ")\n" +
        "Predvidena cena: " + tourPrice + " € / osebo\n" +
        "Datum: " + date + "\n" +
        "Število oseb: " + people + "\n\n" +
        "Podatki o stranki:\n" +
        "Ime in priimek: " + name + "\n" +
        "E-pošta: " + email + "\n" +
        "Telefon: " + phone + "\n\n" +
        "Opombe:\n" + (note || "/") + "\n\n" +
        "Prosim za potrditev termina in podatke za predplačilo.\n\nLep pozdrav,\n" +
        name;

      var mailtoLink =
        "mailto:" +
        encodeURIComponent(to) +
        "?subject=" +
        encodeURIComponent(subject) +
        "&body=" +
        encodeURIComponent(body);

      window.location.href = mailtoLink;
    });
  </script>
</body>
</html>
<img width="368" height="477" alt="Screen Shot 2025-11-26 at 11 39 17" src="https://github.com/user-attachments/assets/c1a310a2-7846-4c0e-873b-a14572fb2a9e" />
