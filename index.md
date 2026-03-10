---
title: Home
---

{% include figure.html img="HADR_IROS.png" alt="Workshop Logo" width="100%" %}

<div id="typewriter">
  <h1>Robots for...</h1>
  <i><h2 id="line" class="line"></h2></i>
</div>

<script>
  const lines = [
    "Humanitarian Assistance ",
    "Disaster Relief ",
    "",
    "HARD Problems ",
  ];
  let lineIndex = 0;
  let charIndex = 0;
  const typingSpeed = 100;   // Typing speed in ms
  const delayBetweenLines = 1500; // Delay before switching to next line

  function typeLine() {
    const lineElement = document.getElementById("line");
    lineElement.innerHTML = `${lines[lineIndex].slice(0, charIndex + 1)}&nbsp;`;

    if (charIndex < lines[lineIndex].length) {
      charIndex++;
      setTimeout(typeLine, typingSpeed);
    } else {
      setTimeout(() => {
        charIndex = 0;
        lineIndex = (lineIndex + 1) % lines.length;
        lineElement.innerHTML = "<br>";
        setTimeout(typeLine, typingSpeed);
      }, delayBetweenLines);
    }
  }

  typeLine();
</script>


## Abstract

This workshop focuses on robotics and autonomous systems for Humanitarian Assistance and Disaster Relief (HADR), bringing interdisciplinary technologies to address complex emergency response challenges. It will convene researchers and practitioners from robotics, disaster science, emergency and field medicine, and systems engineering to explore problems spanning small-scale incidents to large-scale catastrophes while identifying common underlying challenges. Topics include field-deployable aerial and ground platforms, resilient perception and mapping in degraded environments, human–robot teaming, and decision support under uncertainty, alongside theoretical perspectives that frame HADR as a coherent scientific problem space. The workshop will also emphasize retrospective analyses of past deployments, strategies for collecting and sharing operationally relevant datasets, and the development of meaningful benchmarking methodologies that reflect the constraints of real disaster environments.

**Location:** Pittsburgh, PA 

**Date:** September 27, 2026

**Duration:** Full Day

<div style="text-align: center;">
  <a href="./2-contributing.html" class="button">Submit Your Work!</a>
  <a href="" class="button">Register</a>
  <a href="https://forms.gle/3dRso1c3vBp9bHTt6" class="button">Get Updates</a>
</div>

<style>
.button {
  display: inline-block;
  padding: 15px 30px;
  font-size: 24px;
  color: white;
  background-color: #dca735ff;
  text-decoration: none;
  border-radius: 5px;
  transition: background 0.3s;
}

.button:hover {
  background-color: #fff395ff;
}

.button:visited,
.button:active,
.button:focus {
  color: white !important;
  text-decoration: none;
}
</style>