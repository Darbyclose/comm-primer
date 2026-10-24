---
layout: default
title: Home
permalink: /
---

<section class="hero">
  <div class="kicker">AI × COMMUNICATION × REAL LIFE</div>

  <h1>When AI speaks for us, <em>what happens to our voice?</em></h1>

  <p class="intro">We ask AI to write emails, birthday messages, apologies, and even the things we don't know how to say. That's convenient. But does a better-written message always make for better communication?</p>

  <p>This isn't an argument to stop using AI. It's a guide to using it without losing the human part of communicating.</p>

  <a class="button-link" href="#try-it">Try the message experiment ↓</a>
</section>


<section id="try-it" class="activity">
  <div class="kicker">INTERACTIVE / 01</div>

  <h2>Which birthday text feels more personal?</h2>

  <p>Imagine it's your birthday and you get these two messages. Both are sweet in their own way, but which one would mean more to you?</p>

  <div class="message-grid">
    <div class="message">
      <strong>MESSAGE A</strong>
      <p>Happy birthday! I'm so grateful to have you in my life. You bring joy to everyone around you, and I hope your day is as wonderful as you are!</p>
    </div>

    <div class="message">
      <strong>MESSAGE B</strong>
      <p>HAPPY BIRTHDAY!! Still can't believe we survived that road trip when you got us lost for three hours. Love you, but I'm never letting you navigate again.</p>
    </div>
  </div>

  <p><strong>Which one would mean more to you?</strong></p>

  <div class="choice-row" role="group" aria-label="Choose a birthday message">
    <button type="button" data-choice="a" aria-pressed="false">Message A</button>
    <button type="button" data-choice="b" aria-pressed="false">Message B</button>
    <button type="button" data-choice="both" aria-pressed="false">Both / it depends</button>
  </div>

  <div id="message-result" class="result" aria-live="polite" hidden></div>
</section>


<section>
  <div class="kicker section-label">THINK ABOUT IT</div>

  <h2>Maybe the words aren't the whole story.</h2>

  <p>Both messages say happy birthday. Both are meant to make someone feel appreciated. But they probably don't feel exactly the same.</p>

  <p>So what makes one message feel more personal than another? Is it the words themselves? The memories behind them? Or just knowing who wrote them?</p>

  <p>Now imagine finding out that one of those messages was written by AI. Would that change your answer?</p>

  <p>That's what I want to explore. Because as AI becomes part of more of our everyday conversations, I think it's worth asking what makes communication feel human in the first place.</p>
</section>


<script>
(function () {
  const messages = {
    a: "You picked Message A! Maybe you appreciate a thoughtful, well-written message. But here's something to consider: would you feel differently if you found out AI wrote it?",

    b: "You picked Message B! Maybe the inside joke and shared memory made it feel more personal. But what if AI had been given those details and wrote the message instead?",

    both: "You picked both / it depends! That's interesting, because the relationship, the situation, and who wrote the message could all change how you feel about it."
  };

  const result = document.getElementById("message-result");

  document.querySelectorAll("[data-choice]").forEach(button => {
    button.addEventListener("click", () => {
      document.querySelectorAll("[data-choice]").forEach(b => {
        b.setAttribute("aria-pressed", String(b === button));
      });

      result.textContent = messages[button.dataset.choice];
      result.hidden = false;
    });
  });
})();
</script>


<p><a href="{{ '/ai-assisted-message/' | relative_url }}">Next: The Problem →</a></p>
