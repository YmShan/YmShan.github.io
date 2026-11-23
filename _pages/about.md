---
permalink: /
title: "About Me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
I'm a **PhD candidate** in a joint program between:\
**University of Electronic Science and Technology of China (UESTC)**\
and the **Shenzhen Loop Area Institute (SLAI)**

My research interests include:
- **Brain-inspired Computing**
- **Spiking Neural Networks**
- **Neuromorphic Vision**
- **Single Object Tracking**

## Competition Awards

<p class="award-hint">Hover over an award to preview its certificate, or click to open the full image.</p>
<ul class="competition-awards">
  <li><a class="award-certificate" href="{{ '/images/awards/acm-mm-2026-certificate.png' | relative_url }}" target="_blank" rel="noopener noreferrer" data-certificate-alt="First Prize certificate for team Neuromorphic_Computing - UESTC, AdoDAS Challenge at ACM MM 2026, Track A2: DASS-21 Item Prediction and Reconstruction"><strong>ACM MM 2026 — First Prize</strong></a>, AdoDAS Challenge, Track A2: DASS-21 Item Prediction and Reconstruction (Team: Neuromorphic_Computing - UESTC).</li>
  <li><a class="award-certificate" href="{{ '/images/awards/ijcai-2025-spikecv-certificate.png' | relative_url }}" target="_blank" rel="noopener noreferrer" data-certificate-alt="Track 2 Best Dataset and Benchmark Award certificate for SDTrack-Team, the First SpikeCV Competition: Infinity – WUJI at IJCAI 2025"><strong>IJCAI 2025 — Track 2 Best Dataset &amp; Benchmark Award</strong></a>, The First SpikeCV Competition: Infinity – WUJI (Team: SDTrack-Team).</li>
</ul>

<div id="award-certificate-preview" aria-hidden="true" hidden>
  <img alt="" />
</div>

<style>
.competition-awards li {
  margin-bottom: 0.75em;
}
.award-hint {
  color: var(--global-text-color, #494e52);
  font-size: 0.9em;
}
.award-certificate:focus-visible {
  outline: 2px solid currentColor;
  outline-offset: 4px;
}
#award-certificate-preview {
  position: fixed;
  z-index: 1000;
  box-sizing: border-box;
  max-width: calc(100vw - 32px);
  padding: 8px;
  background: #fff;
  border: 1px solid #d7dce0;
  border-radius: 6px;
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.2);
}
#award-certificate-preview[hidden] {
  display: none;
}
#award-certificate-preview img {
  display: block;
  width: auto;
  height: auto;
  max-width: min(640px, calc(100vw - 50px));
  max-height: 65vh;
  margin: 0;
}
@media print {
  #award-certificate-preview, .award-hint { display: none; }
}
</style>

<script>
(function () {
  var preview = document.getElementById('award-certificate-preview');
  var image = preview.querySelector('img');
  var activeLink = null;
  var hideTimer;
  // Keep the fixed preview outside the theme's animated page container.
  document.body.appendChild(preview);

  function hidePreview() {
    clearTimeout(hideTimer);
    preview.hidden = true;
    activeLink = null;
  }

  function positionPreview() {
    if (!activeLink) return;
    var rect = activeLink.getBoundingClientRect();
    var margin = 16;
    var gap = 8;
    var below = window.innerHeight - rect.bottom - margin - gap;
    var above = rect.top - margin - gap;
    var space = Math.max(below, above);
    image.style.maxHeight = Math.max(1, Math.min(window.innerHeight * 0.65, space - 18)) + 'px';
    var box = preview.getBoundingClientRect();
    var top = below >= box.height ? rect.bottom + gap : rect.top - box.height - gap;
    preview.style.top = Math.max(margin, Math.min(top, window.innerHeight - box.height - margin)) + 'px';
    preview.style.left = Math.max(margin, Math.min(rect.left, window.innerWidth - box.width - margin)) + 'px';
  }

  function showPreview(link) {
    clearTimeout(hideTimer);
    activeLink = link;
    image.alt = link.getAttribute('data-certificate-alt');
    image.src = link.href;
    preview.hidden = false;
    positionPreview();
  }

  function scheduleHide() {
    clearTimeout(hideTimer);
    hideTimer = setTimeout(hidePreview, 150);
  }

  document.querySelectorAll('.award-certificate').forEach(function (link) {
    link.addEventListener('pointerenter', function (event) {
      if (event.pointerType !== 'touch') showPreview(link);
    });
    link.addEventListener('pointerleave', scheduleHide);
    link.addEventListener('focus', function () {
      if (link.matches(':focus-visible')) showPreview(link);
    });
    link.addEventListener('blur', scheduleHide);
    link.addEventListener('click', hidePreview);
  });
  preview.addEventListener('pointerenter', function () { clearTimeout(hideTimer); });
  preview.addEventListener('pointerleave', scheduleHide);
  image.addEventListener('load', positionPreview);
  image.addEventListener('error', hidePreview);
  document.addEventListener('keydown', function (event) {
    if (event.key === 'Escape') hidePreview();
  });
  window.addEventListener('scroll', hidePreview, { passive: true });
  window.addEventListener('resize', hidePreview);
}());
</script>

## Academic Service

I serve as a **reviewer** for the following venues:
- **CVPR 2026** (IEEE/CVF Conference on Computer Vision and Pattern Recognition)
- **NeurIPS 2026** (Conference on Neural Information Processing Systems)
- **ICLR 2025&2026&2027** (International Conference on Learning Representations)
- **ICML 2026** (International Conference on Machine Learning)
- **ECCV 2026** (European Conference on Computer Vision)
- **AAAI 2026&2027** (Annual AAAI Conference on Artificial Intelligence)
- **IJCNN 2025** (International Joint Conference on Neural Networks)
- **PRCV 2025** (Chinese Conference on Pattern Recognition and Computer Vision)
- **[TPAMI](https://www.computer.org/csdl/journal/tp/)** (IEEE Transactions on Pattern Analysis and Machine Intelligence, **IF 18.6**)
- **[TCYB](https://www.ieeesmc.org/publications/transactions-on-cybernetics/)** (IEEE Transactions on Cybernetics, **IF 10.5**)
- **[TCSVT](https://ieee-cas.org/publication/tcsvt)** (IEEE Transactions on Circuits and Systems for Video Technology, **IF 10.8**)
- **[TNNLS](https://cis.ieee.org/publications/t-neural-networks-and-learning-systems)** (IEEE Transactions on Neural Networks and Learning Systems, **IF 8.9**)
- **[TETCI](https://cis.ieee.org/publications/t-emerging-topics-in-ci)** (IEEE Transactions on Emerging Topics in Computational Intelligence, **IF 6.5**)
- **[TCDS](https://cis.ieee.org/publications/t-cognitive-and-developmental-systems)** (IEEE Transactions on Cognitive and Developmental Systems, **IF 4.9**)
- **[PR](https://www.sciencedirect.com/journal/pattern-recognition)** (Pattern Recognition, **IF 8.8**)
- **[neurocomputing](https://www.sciencedirect.com/journal/neurocomputing)**, **IF 6.5**
- **[TMLR](https://jmlr.org/tmlr/)** (Transactions on Machine Learning Research)
