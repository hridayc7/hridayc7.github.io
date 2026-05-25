---
title: "Ideas I Want to Explore"
permalink: /writing/ideas/
author_profile: true
---

<div id="locked-writing-content" style="display: none;">

Here is a running list of personal and technical ideas I am excited to brainstorm, prototype, or explore:

### 1. WebGPU-Powered Local Agentic Orchestration
*   **The Concept**: Running ultra-compact 1.5B/2B parameter LLMs directly in the client browser to perform context-aware micro-tasks (DOM parsing, form filling, text summaries) without sending any user data to external servers.
*   **Key Challenge**: Minimizing initial model download size and managing WebGPU VRAM allocation elegantly in multi-tab environments.

### 2. Multi-Device Haptic Syncing for Accessibility (AR/VR)
*   **The Concept**: Extending the work from SoundWatch and Simulus to sync Apple Watch haptics directly with Meta Quest spatial environments. Activating localized physical haptic cues to guide Deaf and Hard of Hearing users in immersive AR scenarios.
*   **Key Challenge**: Synchronizing Bluetooth haptic packets with low-latency spatial graphics.

### 3. Origin Private File System (OPFS) + On-Device RAG
*   **The Concept**: Building a zero-backend, fully local semantic search engine that indexes personal research PDFs directly into the browser's OPFS, running local embedding models and FAISS vector databases client-side.
*   **Key Challenge**: Implementing efficient chunking and indexing inside a lightweight JS worker thread.

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
