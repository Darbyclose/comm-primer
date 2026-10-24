---
layout: default
title: Interpretation and intention
permalink: /interpretation-and-intention/
---

<section>
  <div class="kicker">AI'S INFLUENCE / 05</div>

  <h1>When AI helps create something, whose idea is it?</h1>

  <p class="intro">AI doesn't just help us find better words anymore. It can suggest ideas, change our tone, and sometimes create an entire message before we've even figured out what we want to say.</p>

  <p>And that's what makes AI different from a lot of the tools we've used before. A keyboard lets me type my own thoughts. Spellcheck fixes my mistakes. But ChatGPT can actually suggest what I should think about, what I should say, and how I should say it.</p>

  <p>That raises a question I think is worth asking: if AI helps come up with the idea, how much of the final message is really mine?</p>

  <h2>First, let's talk about intention.</h2>

  <p>Umberto Eco's work on interpretation gives us a useful starting point. He distinguishes between the intention of the author, the possibilities and limits of the text itself, and the interpretation of the reader.</p>

  <p>These are often discussed using three terms:</p>

  <div class="feature-grid">
    <div class="feature-card">
      <span class="number">01 / INTENTIO AUCTORIS</span>
      <h3>What the author means</h3>
      <p>The meaning or intention the person creating the message wants to communicate.</p>
    </div>

    <div class="feature-card">
      <span class="number">02 / INTENTIO OPERIS</span>
      <h3>What the text communicates</h3>
      <p>The meaning supported by the actual words, structure, and details of the message.</p>
    </div>

    <div class="feature-card">
      <span class="number">03 / INTENTIO LECTORIS</span>
      <h3>What the reader understands</h3>
      <p>The interpretation someone brings to the message based on their experiences and perspective.</p>
    </div>
  </div>

  <p>Basically, what I mean to say, what my message actually communicates, and what someone else takes from it aren't always exactly the same thing.</p>

  <h2>But now there's a fourth influence.</h2>

  <p>In <em>The Uninvited Author</em>, Carlos Evia and Sarah O'Keefe introduce the idea of <em>intentio algorithmi</em>, or algorithmic intention.</p>

  <p>Their argument is that when AI helps create content, we have to consider the influence of the algorithm alongside the author, the text, and the reader.</p>

  <p>That doesn't mean AI has human feelings or intentions. It means the system's patterns, outputs, and suggestions can influence what gets created.</p>

  <p>For example, imagine I'm writing an email to someone I'm upset with. I know what I want to say, but I ask ChatGPT to make it sound more professional.</p>

  <p>Maybe it removes some of my frustration, softens my wording, or suggests a completely different way to approach the conversation.</p>

  <p>That might be helpful! But it also means the final message doesn't necessarily sound exactly like what I originally had in mind.</p>

  <div class="callout">
    <strong>The big idea:</strong>
    AI isn't always just delivering our messages. Sometimes it's helping decide what those messages become.
  </div>
</section>


<section class="activity">
  <div class="kicker">INTERACTIVE EXPERIMENT / 03</div>

  <h2>How much control are you giving AI?</h2>

  <p>Not all AI use is the same. There's a pretty big difference between asking ChatGPT to fix a typo and asking it to write an entire message for you.</p>

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

  <p><strong>Think about it:</strong> At what point does AI stop feeling like a tool and start feeling like a collaborator?</p>
</section>


<section>
  <div class="kicker section-label">WHY THIS MATTERS</div>

  <h2>Are we skipping part of the creative process?</h2>

  <p>I think one of the most interesting things about creativity is that it isn't always easy. Sometimes you have a bad idea, change it, try something else, and eventually come up with something you really like.</p>

  <p>But AI can give us a polished answer almost immediately.</p>

  <p>That's obviously convenient, especially when you're stuck. But I wonder whether constantly having an answer available makes us less willing to work through our own ideas.</p>

  <p>For example, if I'm brainstorming something for a project, AI might suggest an idea I never would've thought of. That could make my work better.</p>

  <p>But if I automatically ask AI for ideas before trying to think of anything myself, I might miss out on the process of actually being creative.</p>

  <p>And I think there's a difference between those two situations.</p>

  <h2>Does AI automatically make something less creative?</h2>

  <p>I don't think so.</p>

  <p>Research by Yue Fu and her colleagues on AI-assisted interpersonal communication found that people recognized benefits such as help with wording, confidence, and communication across language barriers. Participants also expressed concerns about unnatural responses and becoming too dependent on AI.</p>

  <p>To me, that shows why this isn't a simple good-or-bad argument. AI can help people communicate things they might otherwise struggle to express.</p>

  <p>But the way we use it matters.</p>

  <p>If AI helps me organize an idea I already have, that's different from letting it come up with the entire idea and simply putting my name on it.</p>

  <p>Neither situation automatically tells us whether the final message is meaningful. But it does change how much of the creative process I contributed.</p>

  <h2>So who is really in control?</h2>

  <p>Even when AI creates the first draft, we're still making choices. We decide what to ask, what to keep, what to change, and whether to send it.</p>

  <p>But those choices happen after AI has already influenced what options we're looking at.</p>

  <p>That's why I think <em>intentio algorithmi</em> is such an interesting concept. It gives us a way to recognize AI's influence without pretending the algorithm is a person or assuming the human has no control.</p>

  <div class="callout">
    <strong>The takeaway:</strong>
    Using AI doesn't automatically mean giving up your creativity. But it's worth paying attention to whether AI is helping you develop your ideas or replacing the process of coming up with them.
  </div>

  <p><small><strong>Research behind this section:</strong> Umberto Eco, <em>Intentio Lectoris</em>; Carlos Evia and Sarah O'Keefe, <em>The Uninvited Author</em>; and Yue Fu et al., <em>From Text to Self</em> (2023).</small></p>
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


<p><a href="{{ '/what-the-reader-should-do/' | relative_url }}">Next: The Toolkit →</a></p>
