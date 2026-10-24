---
layout: default
title: Interpretation and power
permalink: /interpretation-and-power/
---

<section>
  <div class="kicker">INTERPRETATION & POWER / 04</div>

  <h1>Who gets to decide what a message means?</h1>

  <p class="intro">You can spend forever trying to write the perfect message, but that doesn't mean the person reading it will understand it the way you intended.</p>

  <p>Think about the last time someone misunderstood a text you sent. You knew exactly what you meant, but somehow they took it completely differently. That's because communication doesn't end when we press send.</p>

  <p>The person receiving the message has a role in creating its meaning, too.</p>

  <h2>Stuart Hall's encoding/decoding model</h2>

  <p>Communication theorist Stuart Hall explains that messages involve two important processes: <strong>encoding</strong> and <strong>decoding</strong>.</p>

  <p><strong>Encoding</strong> is when someone creates a message with a particular meaning in mind.</p>

  <p><strong>Decoding</strong> is when someone receives that message and interprets it based on their own experiences, beliefs, and understanding of the situation.</p>

  <p>Here's the important part: just because someone intends a message to mean one thing doesn't guarantee everyone will interpret it that way.</p>

  <h2>Three ways to read the same message</h2>

  <p>Hall identifies three general ways people can interpret a message:</p>

  <div class="feature-grid">
    <div class="feature-card">
      <span class="number">01 / DOMINANT</span>
      <h3>Accepting the message</h3>
      <p>You understand and accept the meaning the sender intended.</p>
    </div>

    <div class="feature-card">
      <span class="number">02 / NEGOTIATED</span>
      <h3>Agreeing, but not completely</h3>
      <p>You accept part of the intended meaning but interpret other parts differently.</p>
    </div>

    <div class="feature-card">
      <span class="number">03 / OPPOSITIONAL</span>
      <h3>Rejecting the message</h3>
      <p>You understand the intended meaning but disagree with or reject it.</p>
    </div>
  </div>

  <p>These different readings help explain why two people can see the exact same message and walk away with completely different reactions.</p>

  <h2>So what happens when AI gets involved?</h2>

  <p>Imagine receiving a really thoughtful apology from someone who hurt your feelings. At first, you might think they spent time reflecting on what happened and figuring out how to make things right.</p>

  <p>But what if you found out they used ChatGPT to write it?</p>

  <p>Some people might feel like the apology means less. Others might think the person still cared enough to send it, regardless of how they found the words.</p>

  <p>The message hasn't changed. But the way someone interprets it might.</p>
</section>


<section class="activity">
  <div class="kicker">INTERACTIVE EXPERIMENT / 02</div>

  <h2>Does knowing who wrote it change everything?</h2>

  <p>Imagine your friend sends you this message after an argument.</p>

  <div class="message">
    <p>"I've been thinking about what happened, and I realize I wasn't being fair to you. I really value our friendship, and I'm sorry for making you feel like I wasn't listening."</p>
  </div>

  <p><strong>Before you find out who wrote it, how sincere does this apology feel?</strong></p>

  <div class="choice-row" role="group" aria-label="Rate the sincerity of the apology">
    <button type="button" data-sincerity="sincere" aria-pressed="false">Sincere</button>
    <button type="button" data-sincerity="unsure" aria-pressed="false">Not sure</button>
    <button type="button" data-sincerity="insincere" aria-pressed="false">Not sincere</button>
  </div>

  <div id="sincerity-result" class="result" aria-live="polite" hidden>
    <p>Interesting! Now let's add one more piece of information.</p>
    <button type="button" id="reveal-ai">Reveal who wrote it</button>
  </div>

  <div id="ai-reveal-result" class="result" aria-live="polite" hidden>
    <h3>Surprise! This example was written with AI.</h3>

    <p>Did that change how you felt about it?</p>

    <p>The words stayed exactly the same. The only thing that changed was what you knew about how they were created.</p>

    <p>Think back to Hall's model. You might accept the apology as genuine, feel conflicted about it, or reject it because AI was involved. Your interpretation matters just as much as what the sender wanted you to think.</p>
  </div>
</section>


<section>
  <div class="kicker section-label">WHAT THE RESEARCH SAYS</div>

  <h2>Sometimes knowing AI was used changes everything.</h2>

  <p>Researchers Jiaqi Zhu and Andras Molnar studied how people reacted to messages when they knew AI had been involved in writing them.</p>

  <p>They found that people generally formed more negative impressions of senders when they were explicitly told a message was AI-generated. When they weren't told AI was involved, they often didn't suspect it and judged the senders more positively.</p>

  <p>I think that's really interesting because it suggests that the words themselves aren't always what changes someone's opinion. Sometimes it's just knowing how those words were created.</p>

  <h2>And that's where power comes in.</h2>

  <p>Hall's theory also makes us think about who has influence over communication. The sender can choose how to present a message, but they can't completely control how someone else interprets it.</p>

  <p>AI adds another layer to that. If an algorithm helps choose the words, tone, or ideas in a message, then it has helped shape what the receiver sees, even if a person is still the one pressing send.</p>

  <p>I don't think that automatically makes the message less meaningful. But I do think we should recognize that AI is becoming part of how messages are created, not just how they're delivered.</p>

  <div class="callout">
    <strong>The takeaway:</strong>
    We don't completely control how other people interpret our messages. And when AI is involved, knowing how something was written can become part of its meaning.
  </div>

  <p><small><strong>Research behind this section:</strong> Stuart Hall's encoding/decoding model; Daniel Chandler, <em>Semiotics: The Basics</em>, pp. 214–215; and Jiaqi Zhu and Andras Molnar, <em>Blissful (A)Ignorance</em>.</small></p>
</section>


<script>
(function () {
  const choices = document.querySelectorAll("[data-sincerity]");
  const sincerityResult = document.getElementById("sincerity-result");
  const revealButton = document.getElementById("reveal-ai");
  const revealResult = document.getElementById("ai-reveal-result");

  choices.forEach(function (button) {
    button.addEventListener("click", function () {
      choices.forEach(function (choice) {
        choice.setAttribute("aria-pressed", String(choice === button));
      });

      sincerityResult.hidden = false;
    });
  });

  if (revealButton && revealResult) {
    revealButton.addEventListener("click", function () {
      revealResult.hidden = false;
      revealButton.textContent = "Revealed!";
      revealButton.disabled = true;
    });
  }
})();
</script>


<p><a href="{{ '/interpretation-and-intention/' | relative_url }}">Next: AI's Influence →</a></p>
