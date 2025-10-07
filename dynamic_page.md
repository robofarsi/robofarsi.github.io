---
title: Dynamic Page
layout: default
nav_order: 4
---

<div id="dynamic-content">Loading dynamic content...</div>

<script>
fetch('https://c2a3b3c0-f933-441b-9c69-3c642a2e1d41-00-loselnm7rp9b.spock.replit.dev/api/data')
  .then(response => response.json())
  .then(data => {
    document.getElementById('dynamic-content').innerHTML = `<p>${data.message}</p>`;
  })
  .catch(error => {
    document.getElementById('dynamic-content').innerHTML = `<p>Error loading data.</p>`;
    console.error(error);
  });
</script>
