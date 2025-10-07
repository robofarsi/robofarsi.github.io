---
title: Dynamic Page
layout: default
nav_order: 4
---

<div id="dynamic-content">Loading dynamic content...</div>

<script>
fetch('https://myapp.fly.dev/api/data')
  .then(response => response.json())
  .then(data => {
    document.getElementById('dynamic-content').innerHTML = `<p>${data.message}</p>`;
  })
  .catch(error => {
    document.getElementById('dynamic-content').innerHTML = `<p>Error loading data.</p>`;
    console.error(error);
  });
</script>
