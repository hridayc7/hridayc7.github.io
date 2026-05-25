---
title: "Ideas I Want to Explore"
permalink: /writing/ideas/
author_profile: true
---

<div id="locked-writing-content" style="display: none;">

Here is a running list of personal and technical ideas I am excited to explore:

- evals
- model architecture

<p style="margin-top: 40px;"><a href="/writing/" class="btn btn--light">← Back to Writing</a></p>
</div>

<div id="locked-writing-message" style="display: block; text-align: center; margin-top: 50px;">
  <p>🔒 This page is locked. Please complete the verification quiz first.</p>
  <p><a href="/writing/" class="btn btn--primary">Go to Verification Page</a></p>
</div>

<script>
  document.addEventListener("DOMContentLoaded", function() {
    if (localStorage.getItem("hriday_writing_unlocked") === "true") {
      document.getElementById("locked-writing-content").style.display = "block";
      document.getElementById("locked-writing-message").style.display = "none";
    }
  });
</script>
