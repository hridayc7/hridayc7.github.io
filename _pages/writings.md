---
layout: archive
title: "Writings"
permalink: /writings/
author_profile: true
---

<!-- Quiz Lock Screen -->
<div id="writings-lock-screen" style="max-width: 550px; margin: 30px auto; padding: 20px; border: 1px solid #dbdbdb; border-radius: 4px;">
  
  <h2 style="margin-top: 0; border-bottom: 1px solid #eee; padding-bottom: 10px;">Hriday's Writings - Verification</h2>
  <p style="font-size: 0.95rem; line-height: 1.5; margin-bottom: 20px;">
    To unlock my personal writings, please answer these verification questions:
  </p>

  <p style="font-weight: bold; margin-bottom: 15px;">Question:</p>

  <div id="quiz-steps-container">
    
    <!-- Step 1: Paddington -->
    <div class="quiz-step" id="step-1">
      <p style="margin-bottom: 10px;"><strong>What is my favorite bear?</strong></p>
      <input type="text" id="ans-1" placeholder="Type your answer..." onkeydown="handleKeydown(event, 1)" style="width: 100%; padding: 8px; margin-bottom: 15px; border: 1px solid #ccc; border-radius: 4px; box-sizing: border-box;">
      <button onclick="nextStep(1)" class="btn btn--primary" style="margin: 0;">Next</button>
    </div>

    <!-- Step 2: Pickleball -->
    <div class="quiz-step" id="step-2" style="display: none;">
      <p style="margin-bottom: 10px;"><strong>What is my favorite sport to play?</strong></p>
      <input type="text" id="ans-2" placeholder="Type your answer..." onkeydown="handleKeydown(event, 2)" style="width: 100%; padding: 8px; margin-bottom: 15px; border: 1px solid #ccc; border-radius: 4px; box-sizing: border-box;">
      <button onclick="prevStep(2)" class="btn btn--light" style="margin: 0 10px 0 0;">Back</button>
      <button onclick="nextStep(2)" class="btn btn--primary" style="margin: 0;">Next</button>
    </div>

    <!-- Step 3: Catan -->
    <div class="quiz-step" id="step-3" style="display: none;">
      <p style="margin-bottom: 10px;"><strong>What is my favorite board game?</strong></p>
      <input type="text" id="ans-3" placeholder="Type your answer..." onkeydown="handleKeydown(event, 3)" style="width: 100%; padding: 8px; margin-bottom: 15px; border: 1px solid #ccc; border-radius: 4px; box-sizing: border-box;">
      <button onclick="prevStep(3)" class="btn btn--light" style="margin: 0 10px 0 0;">Back</button>
      <button onclick="nextStep(3)" class="btn btn--primary" style="margin: 0;">Next</button>
    </div>

    <!-- Step 4: Food (Picture Round using basic radio buttons) -->
    <div class="quiz-step" id="step-4" style="display: none;">
      <p style="margin-bottom: 10px;"><strong>Picture Round: Which of these 4 is my favorite food?</strong></p>
      
      <img src="{{ '/images/food_choices.png' | relative_url }}" alt="Food Choices" style="width: 100%; max-width: 280px; border: 1px solid #ccc; border-radius: 4px; margin-bottom: 15px; display: block;">
      
      <div style="margin-bottom: 15px; display: flex; flex-direction: column; gap: 8px; text-align: left;">
        <label><input type="radio" name="food-choice" value="pizza"> Pizza</label>
        <label><input type="radio" name="food-choice" value="sushi"> Sushi</label>
        <label><input type="radio" name="food-choice" value="burrito"> Burrito</label>
        <label><input type="radio" name="food-choice" value="ramen"> Ramen</label>
      </div>

      <button onclick="prevStep(4)" class="btn btn--light" style="margin: 0 10px 0 0;">Back</button>
      <button onclick="nextStep(4)" class="btn btn--primary" style="margin: 0;">Next</button>
    </div>

    <!-- Step 5: Steph Curry -->
    <div class="quiz-step" id="step-5" style="display: none;">
      <p style="margin-bottom: 10px;"><strong>Who is my favorite basketball player?</strong></p>
      <input type="text" id="ans-5" placeholder="Type your answer..." onkeydown="handleKeydown(event, 5)" style="width: 100%; padding: 8px; margin-bottom: 15px; border: 1px solid #ccc; border-radius: 4px; box-sizing: border-box;">
      <button onclick="prevStep(5)" class="btn btn--light" style="margin: 0 10px 0 0;">Back</button>
      <button onclick="nextStep(5)" class="btn btn--primary" style="margin: 0;">Next</button>
    </div>

    <!-- Step 6: Amsterdam -->
    <div class="quiz-step" id="step-6" style="display: none;">
      <p style="margin-bottom: 10px;"><strong>What is my top travel destination?</strong></p>
      <input type="text" id="ans-6" placeholder="Type your answer..." onkeydown="handleKeydown(event, 6)" style="width: 100%; padding: 8px; margin-bottom: 15px; border: 1px solid #ccc; border-radius: 4px; box-sizing: border-box;">
      <button onclick="prevStep(6)" class="btn btn--light" style="margin: 0 10px 0 0;">Back</button>
      <button onclick="nextStep(6)" class="btn btn--primary" style="margin: 0;">Finish</button>
    </div>

  </div>

  <div id="quiz-error" style="color: #c0392b; font-size: 0.9rem; display: none; margin-top: 15px; font-weight: bold;">
    Incorrect answer. Please try again.
  </div>
</div>

<!-- Writings Content (Hidden by default) -->
<div id="writings-content" style="display: none; border-top: 1px solid #eee; padding-top: 20px;">
  <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 30px;">
    <h2 style="margin: 0;">Personal Writings & Reflections</h2>
    <button onclick="lockWritings()" class="btn btn--light" style="margin: 0;">
      Lock Page
    </button>
  </div>

  <div class="writings-list">
    
    <article style="margin-bottom: 40px; border-bottom: 1px solid #eee; padding-bottom: 25px;">
      <h3 style="margin-top: 0; margin-bottom: 5px;"><a href="{{ '/writings/microblog/' | relative_url }}">Microblog</a></h3>
      <div style="font-size: 0.85rem; opacity: 0.6; margin-bottom: 15px;">Recent personal updates and reflections</div>
      <p style="line-height: 1.6; opacity: 0.85;">
        Access my personal microblog containing updates, thoughts, and reflections about my sports updates, teaching, and adventures.
      </p>
    </article>

  </div>
</div>

<!-- Quiz Logic -->
<script>
  // Check local storage on load
  document.addEventListener("DOMContentLoaded", function() {
    if (localStorage.getItem("hriday_writings_unlocked") === "true") {
      showContentDirectly();
    }
  });

  function showContentDirectly() {
    document.getElementById("writings-lock-screen").style.display = "none";
    document.getElementById("writings-content").style.display = "block";
  }

  function handleKeydown(event, stepNum) {
    if (event.key === "Enter") {
      nextStep(stepNum);
    }
  }

  function getSelectedFood() {
    const radios = document.getElementsByName("food-choice");
    for (let r of radios) {
      if (r.checked) {
        return r.value;
      }
    }
    return "";
  }

  function validateAnswer(stepNum) {
    document.getElementById("quiz-error").style.display = "none";
    
    if (stepNum === 1) {
      const val = document.getElementById("ans-1").value.trim().toLowerCase();
      return val === "paddington";
    }
    if (stepNum === 2) {
      const val = document.getElementById("ans-2").value.trim().toLowerCase();
      return val === "pickleball";
    }
    if (stepNum === 3) {
      const val = document.getElementById("ans-3").value.trim().toLowerCase();
      return val === "catan";
    }
    if (stepNum === 4) {
      return getSelectedFood() === "burrito";
    }
    if (stepNum === 5) {
      const val = document.getElementById("ans-5").value.trim().toLowerCase();
      return (val === "curry" || val === "steph curry" || val === "stephen curry");
    }
    if (stepNum === 6) {
      const val = document.getElementById("ans-6").value.trim().toLowerCase();
      return (val === "amsterdam" || val === "amsterdamn");
    }
    return false;
  }

  function nextStep(stepNum) {
    if (validateAnswer(stepNum)) {
      if (stepNum < 6) {
        document.getElementById("step-" + stepNum).style.display = "none";
        document.getElementById("step-" + (stepNum + 1)).style.display = "block";
      } else {
        localStorage.setItem("hriday_writings_unlocked", "true");
        document.getElementById("writings-lock-screen").style.display = "none";
        document.getElementById("writings-content").style.display = "block";
      }
    } else {
      document.getElementById("quiz-error").style.display = "block";
    }
  }

  function prevStep(stepNum) {
    document.getElementById("quiz-error").style.display = "none";
    document.getElementById("step-" + stepNum).style.display = "none";
    document.getElementById("step-" + (stepNum - 1)).style.display = "block";
  }

  function lockWritings() {
    localStorage.removeItem("hriday_writings_unlocked");
    
    // Reset inputs
    document.getElementById("ans-1").value = "";
    document.getElementById("ans-2").value = "";
    document.getElementById("ans-3").value = "";
    document.getElementById("ans-5").value = "";
    document.getElementById("ans-6").value = "";
    
    const radios = document.getElementsByName("food-choice");
    for (let r of radios) {
      r.checked = false;
    }
    
    // Reset steps
    for (let i = 2; i <= 6; i++) {
      document.getElementById("step-" + i).style.display = "none";
    }
    document.getElementById("step-1").style.display = "block";
    
    document.getElementById("writings-content").style.display = "none";
    document.getElementById("writings-lock-screen").style.display = "block";
  }
</script>
