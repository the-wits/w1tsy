---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
<div class="container">
  <div class="card">
    <div class="card_header">
      <a href="{{ '/ctf/' | relative_url }}">
        <img src="{{ "/assets/imgs/flag.png" | relative_url }}" alt="ctf_logo" class="card_image">
      </a>
    </div>
    <div class="card_body">
      <h2 class="card-title"><a class="card_link" href="{{ '/ctf/' | relative_url }}">CTF Challenges</a></h2>
      <p>Capture the flag and have fun!</p>
    </div>
  </div>

  <div class="card">
    <div class="card_header">
      <a href="{{ '/about/' | relative_url }}">
        <img src="{{ "/assets/imgs/who.png" | relative_url }}" alt="about_logo" class="card_image" id="who">
      </a>
    </div>
    <div class="card_body">
      <h2 class="card-title"><a class="card_link" href="{{ '/about/' | relative_url }}">whoami</a></h2>
      <p>Information about me and my blog</p>
    </div>
  </div>
</div>