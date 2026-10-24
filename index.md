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

<section>
  <div class="kicker section-label">THE EVERYDAY PROBLEM</div>
  <h2>A perfectly written message can still miss the point.</h2>
  <p>Imagine getting an apology from a friend. The wording is flawless. Then you learn they asked ChatGPT to write the entire thing. Would you feel the same? Maybe. Maybe not. That difference is what communication theory helps us understand.</p>
  <div class="callout"><strong>The big idea:</strong> Communication isn't only about sending the right words. It's about shared meaning, relationships, interpretation, and the choices behind a message.</div>
</section>

<section id="try-it" class="activity">
  <div class="kicker">INTERACTIVE / 01</div>
  <h2>Which birthday text feels more personal?</h2>
  <p>Read these two made-up examples. Neither is automatically better. What matters is what you notice.</p>

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
  <div class="kicker section-label">FOUR WAYS TO SEE WHAT'S HAPPENING</div>
  <h2>The theory, without the textbook headache.</h2>

  <div class="feature-grid">
    <a class="feature-card" href="{{ '/transmission-view-and-its-limits/' | relative_url }}">
      <span class="number">01 / SHANNON & WEAVER</span>
      <h3>Clear isn't always caring.</h3>
      <p>AI can make words clearer. But does that guarantee connection?</p>
    </a>

    <a class="feature-card" href="{{ '/meaning-and-culture/' | relative_url }}">
      <span class="number">02 / SEMIOTICS</span>
      <h3>Inside jokes matter.</h3>
      <p>How memories and shared context make words personal.</p>
    </a>

    <a class="feature-card" href="{{ '/interpretation-and-power/' | relative_url }}">
      <span class="number">03 / STUART HALL</span>
      <h3>The reader gets a say.</h3>
      <p>Why the same AI-written message can feel thoughtful to one person and impersonal to another.</p>
    </a>

    <a class="feature-card" href="{{ '/interpretation-and-intention/' | relative_url }}">
      <span class="number">04 / ALGORITHMIC INTENTION</span>
      <h3>Who's shaping the message?</h3>
      <p>When AI suggests your words, it influences more than grammar.</p>
    </a>
  </div>
</section>

<section>
  <div class="kicker section-label">THE SOLUTION</div>
  <h2>Use the tool. Keep your voice.</h2>
  <p>AI doesn't have to replace your creativity. A useful starting point is to decide which parts of a message should come from you and which parts could use some help.</p>

  <ol class="checklist">
    <li><strong>Start with your own thought.</strong> What do you actually want this person to know?</li>
    <li><strong>Use AI for support.</strong> Ask it to organize, clarify, or edit your words rather than invent your feelings.</li>
    <li><strong>Put the personal details back.</strong> Keep your memories, jokes, and specific examples.</li>
    <li><strong>Read it before sending.</strong> Would you actually say this? Does it mean what you intend?</li>
    <li><strong>Think about the relationship.</strong> A routine work email and an apology to a friend don't carry the same stakes.</li>
  </ol>

  <p><a class="button-link" href="{{ '/what-the-reader-should-do/' | relative_url }}">Explore the full communication toolkit →</a></p>
</section>

<section>
  <div class="kicker section-label">ABOUT THIS PROJECT</div>
  <h2>Why look at something as ordinary as a text?</h2>
  <p>Because the little things we do every day are communication, too. This site builds on my communication theory primer, <em>When AI Does the Creating: Are We Losing Human Connection and Creativity?</em>, and uses those theories to make an everyday problem easier to see—and easier to handle.</p>
  <p>Read more about <a href="{{ '/ai-assisted-message/' | relative_url }}">the problem</a>, or see <a href="{{ '/how-i-built-this-site/' | relative_url }}">how this site was built</a>.</p>
</section>

<script>
(function () {
  const messages = {
    a: "You picked the polished message. That is a valid reading! Stuart Hall's encoding/decoding model helps explain why the receiver's interpretation matters—not just what the sender intended.",
    b: "You picked the inside joke. Semiotics helps explain why shared memories and personal context can give ordinary words special meaning.",
    both: "Exactly: context and relationships matter. Semiotics and Stuart Hall's encoding/decoding model show why no single message has the same meaning for everyone."
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
