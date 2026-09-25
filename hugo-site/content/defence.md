---
title: "PhD Defence"
layout: standalone
bookToc: false
---

<div id="defence-hero" style="position: relative; width: 100vw; left: 50%; right: 50%; margin-left: -50vw; margin-right: -50vw; height: 100vh; display: flex; align-items: center; justify-content: center; margin-bottom: 4rem; overflow: hidden; background: #6f8fae;">
  <img id="defence-cover" src="/papers/defence-cover.jpg" alt="" style="position: absolute; top: 0; left: 0; max-width: none; transform-origin: 0 0; will-change: transform;">
  <script>
    (function() {
      var hero = document.getElementById('defence-hero');
      var img = document.getElementById('defence-cover');
      // Main ship in the painting, as fractions of the image: hull spans x 14-51%, centre ~33%; hull at y ~77%.
      var SHIP_X = 0.33, SHIP_Y = 0.77;
      var layout = null;
      function clamp(v, lo, hi) { return Math.min(Math.max(v, lo), hi); }
      function measure() {
        var iw = img.naturalWidth, ih = img.naturalHeight;
        if (!iw || !ih) return;
        var W = hero.clientWidth, H = hero.clientHeight;
        // Cover the hero vertically and leave at least 35% extra width to pan across.
        var s = Math.max(H / ih, 1.35 * W / iw);
        var RW = iw * s, RH = ih * s;
        var minX = W - RW;
        // Start with the ship slightly right of centre, end with it towards the left: it stays in frame throughout.
        var x0 = clamp(0.6 * W - SHIP_X * RW, minX, 0);
        var x1 = clamp(x0 - 0.35 * W, minX, 0);
        if (x0 - x1 < 0.25 * W) x0 = clamp(x1 + 0.35 * W, minX, 0);
        // Put the hull in the lower part of the screen without exposing an edge.
        var y = clamp(0.72 * H - SHIP_Y * RH, H - RH, 0);
        img.style.width = RW + 'px';
        img.style.height = RH + 'px';
        layout = { x0: x0, x1: x1, y: y, H: H };
        update();
      }
      function update() {
        if (!layout) return;
        var p = clamp(window.scrollY / (layout.H * 0.6), 0, 1);
        var x = layout.x0 + (layout.x1 - layout.x0) * p;
        img.style.transform = 'translate3d(' + x + 'px,' + layout.y + 'px,0)';
      }
      var ticking = false;
      window.addEventListener('scroll', function() {
        if (ticking) return;
        ticking = true;
        requestAnimationFrame(function() { ticking = false; update(); });
      }, { passive: true });
      window.addEventListener('resize', measure);
      if (img.complete) measure(); else img.addEventListener('load', measure);
    })();
  </script>
  <div style="position: absolute; inset: 0; background: rgba(0,0,0,0.45);"></div>
  <div style="position: relative; text-align: center; padding: 2rem; color: #fff;">
    <p style="font-size: 0.8rem; letter-spacing: 0.12em; text-transform: uppercase; color: rgba(255,255,255,0.65); margin: 0 0 1.5rem;">You are cordially invited to the public defence of the doctoral thesis.</p>
    <h1 style="font-size: 2rem; line-height: 1.35; font-weight: 700; margin: 0 0 1rem; color: #fff;">A Dual Perspective on Large Language Models for Code and Security</h1>
    <p style="font-size: 1.05rem; margin: 0 0 0.5rem; color: rgba(255,255,255,0.75);">Ali Al-Kaswan</p>
    <p style="font-size: 0.9rem; margin: 0; color: rgba(255,255,255,0.55);">16 December 2026</p>
  </div>
  <div style="position: absolute; bottom: 2rem; left: 2rem; display: flex; flex-direction: column; gap: 0.4rem;">
    <a href="#details" style="font-size: 0.75rem; letter-spacing: 0.1em; text-transform: uppercase; color: rgba(255,255,255,0.6); text-decoration: none;">Details</a>
    <a href="#programme" style="font-size: 0.75rem; letter-spacing: 0.1em; text-transform: uppercase; color: rgba(255,255,255,0.6); text-decoration: none;">Programme</a>
    <a href="#rsvp" style="font-size: 0.75rem; letter-spacing: 0.1em; text-transform: uppercase; color: rgba(255,255,255,0.6); text-decoration: none;">RSVP</a>
  </div>
</div>

<div style="padding-top: 3rem;">

  <div id="details" style="border-top: 1px solid var(--gray-500, #ccc); border-bottom: 1px solid var(--gray-500, #ccc); padding: 1.5rem 0; margin-bottom: 3rem;">
    <table style="display: table; width: 100%; border-collapse: collapse; table-layout: fixed;">
      <colgroup><col style="width: 10rem;"><col></colgroup>
      <tr>
        <td style="padding: 0.5rem 2rem 0.5rem 0; color: var(--gray-500, #888); font-size: 0.8rem; text-transform: uppercase; letter-spacing: 0.1em; white-space: nowrap; vertical-align: top;">Date &amp; Time</td>
        <td style="padding: 0.5rem 0; vertical-align: top;">Wednesday, 16 December 2026 at 17:30</td>
      </tr>
      <tr>
        <td style="padding: 0.5rem 2rem 0.5rem 0; color: var(--gray-500, #888); font-size: 0.8rem; text-transform: uppercase; letter-spacing: 0.1em; white-space: nowrap; vertical-align: top;">Location</td>
        <td style="padding: 0.5rem 0; vertical-align: top;">Aula Congress Centre, TU Delft</td>
      </tr>
      <tr>
        <td style="padding: 0.5rem 2rem 0.5rem 0; color: var(--gray-500, #888); font-size: 0.8rem; text-transform: uppercase; letter-spacing: 0.1em; white-space: nowrap; vertical-align: top;">Reception</td>
        <td style="padding: 0.5rem 0; vertical-align: top;">Followed by a reception and dinner at a location to be determined.</td>
      </tr>
    </table>
  </div>

  <div id="programme" style="margin-bottom: 3rem;">
    <h2 style="font-size: 0.8rem; text-transform: uppercase; letter-spacing: 0.12em; color: var(--gray-500, #888); margin: 0 0 0.6rem;">Programme</h2>
    <table style="display: table; width: 100%; border-collapse: collapse; table-layout: fixed;">
      <colgroup><col style="width: 10rem;"><col></colgroup>
      <tr>
        <td style="padding: 0.5rem 2rem 0.5rem 0; color: var(--gray-500, #888); font-size: 0.9rem; white-space: nowrap; vertical-align: top;">17:30</td>
        <td style="padding: 0.5rem 0; vertical-align: top;">Informal talk</td>
      </tr>
      <tr>
        <td style="padding: 0.5rem 2rem 0.5rem 0; color: var(--gray-500, #888); font-size: 0.9rem; white-space: nowrap; vertical-align: top;">17:40</td>
        <td style="padding: 0.5rem 0; vertical-align: top;">Public defence</td>
      </tr>
      <tr>
        <td style="padding: 0.5rem 2rem 0.5rem 0; color: var(--gray-500, #888); font-size: 0.9rem; white-space: nowrap; vertical-align: top;">18:30</td>
        <td style="padding: 0.5rem 0; vertical-align: top;">Reception</td>
      </tr>
    </table>
  </div>

  <div id="rsvp">
    <h2 style="font-size: 0.8rem; text-transform: uppercase; letter-spacing: 0.12em; color: var(--gray-500, #888); margin: 0 0 0.6rem;">RSVP</h2>
    <p style="margin: 0 0 1.5rem; color: var(--body-font-color);">Please let me know if you plan to attend so I can get an accurate headcount.</p>
    <iframe width="640px" height="480px" src="https://forms.cloud.microsoft/e/rhCHUUh3Ej?embed=true" frameborder="0" marginwidth="0" marginheight="0" style="border: none; max-width: 100%; max-height: 100vh;" allowfullscreen webkitallowfullscreen mozallowfullscreen msallowfullscreen> </iframe>
  </div>
</div>
