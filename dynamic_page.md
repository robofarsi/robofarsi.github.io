---
title: Dynamic Page
layout: default
nav_order: 4
---

<div id="dynamic-content">Loading dynamic content...</div>

<script>
fetch('https://backend-ho98.onrender.com')
  .then(response => response.text())
  .then(data => {
    document.getElementById('dynamic-content').innerHTML = `<p>${data}</p>`;
  })
  .catch(error => {
    document.getElementById('dynamic-content').innerHTML = `<p>Error loading data.</p>`;
    console.error(error);
  });
</script>
