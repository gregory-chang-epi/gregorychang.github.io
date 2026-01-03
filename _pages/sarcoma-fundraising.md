---
title: "Sarcoma Fundraising"
permalink: /sarcoma-fundraising/
layout: single
author_profile: true
---

## Sarcoma Supper Club Fundraising

A rotating dinner club where friends take turns cooking and donate to my Steps for Sarcoma fundraiser.

<style>
  :root{
    /* 🎨 Change these 2 if you want a different palette */
    --steps1:#2563eb;   /* blue */
    --steps2:#06b6d4;   /* cyan */
    --supper1:#f97316;  /* orange */
    --supper2:#facc15;  /* yellow */

    --cardBorder:#e5e7eb;
    --cardBg:#ffffff;
    --muted:#6b7280;
  }

  .ssc-card {
    max-width: 760px;
    padding: 22px;
    border: 1px solid var(--cardBorder);
    border-radius: 18px;
    background: var(--cardBg);
    box-shadow: 0 10px 30px rgba(0,0,0,0.06);
  }

  .ssc-title { font-size: 20px; font-weight: 800; margin: 0 0 6px 0; }
  .ssc-total { font-size: 44px; font-weight: 900; margin: 0; line-height: 1.1; }
  .ssc-sub { margin: 6px 0 18px 0; color: var(--muted); font-weight: 600; }

  .ssc-bar {
    height: 20px;
    border-radius: 999px;
    overflow: hidden;
    display: flex;
    background: #f3f4f6;
    box-shadow: inset 0 1px 2px rgba(0,0,0,0.10);
  }

  .ssc-seg { height: 100%; }

  /* ✅ colorful segments (with subtle gradients) */
  .ssc-steps  { background: linear-gradient(90deg, var(--steps1), var(--steps2)); }
  .ssc-supper { background: linear-gradient(90deg, var(--supper1), var(--supper2)); }

  .ssc-legend { display: grid; gap: 10px; margin-top: 14px; }
  .ssc-row { display: flex; align-items: center; justify-content: space-between; gap: 12px; }
  .ssc-left { display: flex; align-items: center; gap: 10px; }

  .ssc-swatch { width: 12px; height: 12px; border-radius: 4px; }

  /* make swatches match the gradients */
  .ssc-swatch.ssc-steps  { background: linear-gradient(135deg, var(--steps1), var(--steps2)); }
  .ssc-swatch.ssc-supper { background: linear-gradient(135deg, var(--supper1), var(--supper2)); }

  .ssc-note { font-size: 14px; color: var(--muted); margin-top: 12px; }
  .ssc-mono { font-variant-numeric: tabular-nums; }
</style>


<div class="ssc-card">
  <p class="ssc-title">Sarcoma Supper Club Fundraising</p>
  <p class="ssc-total ssc-mono">$6,365</p>
  <p class="ssc-sub">Raised so far</p>

  <div class="ssc-bar" aria-label="Fundraising breakdown bar">
    <div class="ssc-seg ssc-steps" style="width:86.7%"></div>
    <div class="ssc-seg ssc-supper" style="width:13.3%"></div>
  </div>

  <div class="ssc-legend">
    <div class="ssc-row">
      <div class="ssc-left">
        <span class="ssc-swatch ssc-steps"></span>
        <strong>Steps for Sarcoma</strong>
      </div>
      <span class="ssc-mono">$5,520</span>
    </div>

    <div class="ssc-row">
      <div class="ssc-left">
        <span class="ssc-swatch ssc-supper"></span>
        <strong>Supper Club</strong>
      </div>
      <span class="ssc-mono">$845</span>
    </div>
  </div>

  <div class="ssc-note">
    Last updated: Jan 2, 2026
  </div>
</div>

