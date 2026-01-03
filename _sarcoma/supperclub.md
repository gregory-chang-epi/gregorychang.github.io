
<style>
  .ssc-card { max-width: 760px; padding: 20px; border: 1px solid #e5e7eb; border-radius: 16px; }
  .ssc-title { font-size: 20px; font-weight: 700; margin: 0 0 6px 0; }
  .ssc-total { font-size: 44px; font-weight: 800; margin: 0; line-height: 1.1; }
  .ssc-sub { margin: 6px 0 18px 0; color: #6b7280; }
  .ssc-bar { height: 18px; border-radius: 999px; overflow: hidden; display: flex; background: #f3f4f6; }
  .ssc-seg { height: 100%; }
  .ssc-steps { background: #111827; }  /* Steps for Sarcoma */
  .ssc-supper { background: #9ca3af; } /* Supper Club */
  .ssc-legend { display: grid; gap: 10px; margin-top: 14px; }
  .ssc-row { display: flex; align-items: center; justify-content: space-between; gap: 12px; }
  .ssc-left { display: flex; align-items: center; gap: 10px; }
  .ssc-swatch { width: 12px; height: 12px; border-radius: 3px; }
  .ssc-note { font-size: 14px; color: #6b7280; margin-top: 12px; }
  .ssc-mono { font-variant-numeric: tabular-nums; }
</style>

<div class="ssc-card" id="ssc-widget">
  <p class="ssc-title">Sarcoma Supper Club Fundraising</p>
  <p class="ssc-total ssc-mono" id="ssc-total">$0</p>
  <p class="ssc-sub" id="ssc-subtitle">Raised so far</p>

  <div class="ssc-bar" aria-label="Fundraising breakdown bar">
    <div class="ssc-seg ssc-steps" id="ssc-steps-seg" style="width:0%"></div>
    <div class="ssc-seg ssc-supper" id="ssc-supper-seg" style="width:0%"></div>
  </div>

  <div class="ssc-legend">
    <div class="data-row ssc-row">
      <div class="ssc-left">
        <span class="ssc-swatch ssc-steps"></span>
        <strong>Steps for Sarcoma</strong>
      </div>
      <span class="ssc-mono" id="ssc-steps-label">$0 (0.0%)</span>
    </div>

    <div class="ssc-row">
      <div class="ssc-left">
        <span class="ssc-swatch ssc-supper"></span>
        <strong>Supper Club</strong>
      </div>
      <span class="ssc-mono" id="ssc-supper-label">$0 (0.0%)</span>
    </div>
  </div>

  <div class="ssc-note">
    Last updated: <span id="ssc-updated">Jan 2, 2026</span>
  </div>
</div>

<script>
  // ✅ Update these two numbers only:
  const stepsForSarcoma = 5520;
  const supperClub = 845;

  const total = stepsForSarcoma + supperClub;

  const pct = (x) => total === 0 ? 0 : (x / total) * 100;
  const money = new Intl.NumberFormat('en-US', { style: 'currency', currency: 'USD', maximumFractionDigits: 0 });

  document.getElementById('ssc-total').textContent = money.format(total);

  const stepsPct = pct(stepsForSarcoma);
  const supperPct = pct(supperClub);

  document.getElementById('ssc-steps-seg').style.width = stepsPct.toFixed(3) + '%';
  document.getElementById('ssc-supper-seg').style.width = supperPct.toFixed(3) + '%';

  document.getElementById('ssc-steps-label').textContent =
    `${money.format(stepsForSarcoma)} (${stepsPct.toFixed(1)}%)`;

  document.getElementById('ssc-supper-label').textContent =
    `${money.format(supperClub)} (${supperPct.toFixed(1)}%)`;
</script>
