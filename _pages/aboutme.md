---
layout: archive
title: "Contact"
permalink: /aboutme/
description: "Contact Binzheng Zhang for research collaborations, student projects, and enquiries about computational space and planetary plasma physics."
---

<div class="contact-page">
  <section class="contact-intro" aria-labelledby="contact-intro-title">
    <p class="contact-kicker">Work with us</p>
    <h2 id="contact-intro-title">Let’s explore a difficult problem.</h2>
    <p>For research collaborations, prospective student enquiries, invited talks, or questions about our work, email is the best way to reach me.</p>
    <a class="contact-email-link" href="mailto:binzh@hku.hk">binzh@hku.hk <span aria-hidden="true">→</span></a>
  </section>

  <div class="contact-layout">
    <section class="contact-panel contact-panel--form" aria-labelledby="contact-form-title">
      <p class="contact-kicker">Send a message</p>
      <h2 id="contact-form-title">Start a conversation</h2>
      <p class="contact-panel__intro">Tell me briefly what you would like to discuss. Submitting this form opens a prepared message in your email app.</p>

      <form id="contact-form" class="contact-form" aria-describedby="contact-privacy">
        <div class="contact-form__row">
          <div class="contact-field">
            <label for="contact-name">Name</label>
            <input id="contact-name" name="name" type="text" autocomplete="name" required>
          </div>
          <div class="contact-field">
            <label for="contact-email">Your email</label>
            <input id="contact-email" name="email" type="email" autocomplete="email" required>
          </div>
        </div>

        <div class="contact-field">
          <label for="contact-topic">Topic</label>
          <select id="contact-topic" name="topic" required>
            <option value="" selected disabled>Select a topic</option>
            <option>Research collaboration</option>
            <option>Prospective postgraduate student</option>
            <option>Undergraduate research project</option>
            <option>Talk or academic visit</option>
            <option>Other enquiry</option>
          </select>
        </div>

        <div class="contact-field">
          <label for="contact-message">Message</label>
          <textarea id="contact-message" name="message" rows="7" placeholder="A short introduction and what you would like to discuss…" required></textarea>
        </div>

        <div class="contact-form__footer">
          <button class="contact-submit" type="submit">Prepare email</button>
          <p id="contact-privacy">Nothing entered here is stored on this website.</p>
        </div>
      </form>
      <noscript><p>Please email <a href="mailto:binzh@hku.hk">binzh@hku.hk</a> directly.</p></noscript>
    </section>

    <aside class="contact-sidebar" aria-label="Contact details">
      <section class="contact-panel">
        <p class="contact-kicker">Visit</p>
        <h2>Office</h2>
        <address>
          Room 303, James Lee Science Building<br>
          The University of Hong Kong<br>
          Pokfulam, Hong Kong
        </address>
        <a class="contact-text-link" href="https://www.earthsciences.hku.hk/people/academic_staff/63/">Department profile <span aria-hidden="true">→</span></a>
      </section>

      <section class="contact-panel contact-panel--accent">
        <p class="contact-kicker">Join the group</p>
        <h2>Students with curiosity are welcome.</h2>
        <p>Prospective postgraduate students interested in space plasma modelling, applied mathematics, and scientific computing should contact me <strong>before applying</strong> to HKU.</p>
        <p>Current HKU undergraduates are also welcome to ask about research projects.</p>
        <a class="contact-text-link" href="/team/">Meet the group <span aria-hidden="true">→</span></a>
      </section>
    </aside>
  </div>

  <section class="contact-personal" aria-labelledby="contact-personal-title">
    <div>
      <p class="contact-kicker">Beyond research</p>
      <h2 id="contact-personal-title">Science is one chapter of the adventure.</h2>
    </div>
    <p>I am a space physicist without a physics degree—a physicist, engineer, teacher, and geek. Away from simulations and manuscripts, I enjoy family time, Western and traditional music, Chinese calligraphy and painting, indoor and outdoor sports, and a good beer or whisky.</p>
    <blockquote>
      <p>Have a sense of humor. Don’t take yourself too seriously. Remember that academia is a place where the animals take over the zoo.</p>
      <cite>— Advice from my Ph.D. advisor, Bill Lotko</cite>
    </blockquote>
  </section>
</div>

<script>
(function () {
  var form = document.getElementById('contact-form');
  if (!form) return;

  form.addEventListener('submit', function (event) {
    event.preventDefault();
    var data = new FormData(form);
    var name = data.get('name');
    var email = data.get('email');
    var topic = data.get('topic');
    var message = data.get('message');
    var subject = '[Website enquiry] ' + topic + ' — ' + name;
    var body = 'Name: ' + name + '\nEmail: ' + email + '\nTopic: ' + topic + '\n\n' + message;

    window.location.href = 'mailto:binzh@hku.hk?subject=' + encodeURIComponent(subject) + '&body=' + encodeURIComponent(body);
  });
}());
</script>
