---
layout: default
title: Interpretation and power
permalink: /interpretation-and-power/
---

<section class="activity">
  <div class="kicker">INTERACTIVE EXPERIMENT / 02</div>
  <h2>Does knowing who wrote it change everything?</h2>

  <p>Imagine your friend sends you this message after an argument.</p>

  <div class="message">
    <p>"I've been thinking about what happened, and I realize I wasn't being fair to you. I really value our friendship, and I'm sorry for making you feel like I wasn't listening."</p>
  </div>

  <p>Does this apology feel sincere to you?</p>

  <div class="choice-row">
    <button type="button" id="reveal-ai">Reveal who wrote it</button>
  </div>

  <div id="ai-reveal-result" class="result" hidden>
    <h3>Surprise! This example was written with AI.</h3>
    <p>Did that change how you felt about it?</p>
    <p>The words stayed exactly the same. The only thing that changed was what you knew about how they were created.</p>
    <p><strong>The theory:</strong> Stuart Hall's encoding/decoding model explains why the meaning someone takes from a message isn't always the meaning the sender intended. Research by Zhu and Molnar also found that knowing AI was involved can influence how people judge a sender.</p>
  </div>
</section>

<script>
(function () {
  const button = document.getElementById("reveal-ai");
  const result = document.getElementById("ai-reveal-result");

  if (button && result) {
    button.addEventListener("click", function () {
      result.hidden = false;
      button.textContent = "Revealed!";
      button.disabled = true;
    });
  }
})();
</script>

