---
layout: default
title: What the reader should do
permalink: /what-the-reader-should-do/
---

<section class="activity">
  <div class="kicker">THE COMMUNICATION TOOLKIT / 04</div>
  <h2>Should you use AI for this?</h2>

  <p>Not every message needs the same level of AI assistance. Choose a situation to see what communication theory suggests.</p>

  <label for="ai-situation"><strong>What are you trying to write?</strong></label>

  <select id="ai-situation" style="display:block; width:100%; max-width:400px; padding:.8rem; margin:1rem 0; font:inherit;">
    <option value="">Choose a situation...</option>
    <option value="professor">An email to a professor</option>
    <option value="apology">An apology to a friend</option>
    <option value="birthday">A birthday message</option>
    <option value="creative">A creative project</option>
  </select>

  <div id="ai-advice" class="message" aria-live="polite" hidden>
    <h3 id="ai-advice-title"></h3>
    <p id="ai-advice-description"></p>
  </div>
</section>

<script>
(function () {
  const select = document.getElementById("ai-situation");
  const result = document.getElementById("ai-advice");
  const title = document.getElementById("ai-advice-title");
  const description = document.getElementById("ai-advice-description");

  const advice = {
    professor: {
      title: "AI can be a useful editor.",
      description: "Write down what you need to communicate, then use AI to make it clearer and more professional. Shannon and Weaver's model helps explain why clarity matters."
    },
    apology: {
      title: "Keep the actual apology yours.",
      description: "AI can help you organize your thoughts, but the responsibility and feelings should come from you. Think about how the other person might interpret your message."
    },
    birthday: {
      title: "Make it personal.",
      description: "Use your own memories, jokes, and specific details. Semiotics shows how shared experiences create meaning that generic language often can't capture."
    },
    creative: {
      title: "Brainstorm together, but make the choices yourself.",
      description: "AI can suggest possibilities, but be intentional about which ideas you choose and how you develop them. That's where intentio algorithmi comes in."
    }
  };

  if (select && result && title && description) {
    select.addEventListener("change", function () {
      const selected = advice[select.value];

      if (!selected) {
        result.hidden = true;
        return;
      }

      title.textContent = selected.title;
      description.textContent = selected.description;
      result.hidden = false;
    });
  }
})();
</script>
