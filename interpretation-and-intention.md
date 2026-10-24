---
layout: default
title: Interpretation and intention
permalink: /interpretation-and-intention/
---

<section class="activity">
  <div class="kicker">INTERACTIVE EXPERIMENT / 03</div>
  <h2>How much control are you giving AI?</h2>

  <p>Move the slider to see how AI's role changes depending on how you use it.</p>

  <label for="ai-control-slider"><strong>Level of AI involvement</strong></label>

  <input
    type="range"
    id="ai-control-slider"
    min="0"
    max="2"
    value="1"
    step="1"
    style="width:100%; margin:1.5rem 0;"
  >

  <div class="message" aria-live="polite">
    <h3 id="ai-control-title">Level 2: Brainstorming</h3>
    <p id="ai-control-description">You ask AI for ideas, then choose which ones you want to use. AI is now helping shape your creative options.</p>
  </div>

  <p><strong>The theory:</strong> Evia and O'Keefe's idea of <em>intentio algorithmi</em> reminds us that algorithms influence the creative process, even when humans are still making the final decisions.</p>
</section>

<script>
(function () {
  const slider = document.getElementById("ai-control-slider");
  const title = document.getElementById("ai-control-title");
  const description = document.getElementById("ai-control-description");

  const levels = [
    {
      title: "Level 1: Editing",
      description: "You come up with the idea and write the message. AI helps fix grammar or make it clearer."
    },
    {
      title: "Level 2: Brainstorming",
      description: "You ask AI for ideas, then choose which ones you want to use. AI is now helping shape your creative options."
    },
    {
      title: "Level 3: Full generation",
      description: "You give AI a short prompt, and it writes the entire message. The algorithm has a much larger role in what gets communicated."
    }
  ];

  if (slider && title && description) {
    slider.addEventListener("input", function () {
      const level = levels[Number(slider.value)];
      title.textContent = level.title;
      description.textContent = level.description;
    });
  }
})();
</script>
