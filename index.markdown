---
layout: single
title: "Falimentează firma pentru o cauză bună"
header:
  image: /assets/images/poor_sorin.jpg
  teaser: /assets/images/poor_sorin.jpg
  # overlay_filter: 0.5  # Optional: adds a dark overlay for better text contrast
footer:
  content: "© 2024 Boatyardx Team Christmas Charity."
---

Se apropie Crăciunul — perioada în care, teoretic, nimeni nu cheltuie bani, nu-i așa? Ei bine, m-am gândit să profit un pic de generozitatea voastră, și nu doar atât. Vrem să strângem niște bănuți pentru a sprijini [Casa de Copii Căsuța Bucuriei](https://www.casutabucuriei.eu/).

Partea cea mai frumoasă este că l-am prins pe Sorin într-o dispoziție excelentă, iar anul acesta Boatyardx o să dubleze fiecare leu pe care îl donăm noi!

Ho ho! Orice contribuție, oricât de mică, ajută enorm.

Cine dorește să ajute, poate trimite donațiile până pe 20 decembrie la:

**Revolut:** @razvanbalsan  
**ING:** RO93INGB0000999905486139  
**Nume:** Razvan Balsan  
**Detalii plată:** BYX Christmas

## Au mai ramas:
{: .text-center}

<div id="fetched-value" style="font-size:1.5em; font-weight:bold; text-align:center; margin-top:20px;"></div>
<div id="countdown" style="font-size:2em; font-weight:bold; text-align:center; margin-top:50px;"></div>


<script>
(function() {
  var fetchedValue = "";

  // Fetch the CSV
  fetch('https://docs.google.com/spreadsheets/d/1Paq5nh6lSCZO0No33WxFRFE9AqQ7OxKxgABWBCuHXyI/pub?output=csv')
    .then(response => response.text())
    .then(data => {
      const rows = data.split('\n').map(row => row.split(','));
      fetchedValue = rows[0][0]; 
      // Show the fetched value in the fetched-value div
      document.getElementById('fetched-value').textContent = `Pana acum Boatyardx e cu ${fetchedValue} lei mai saraca`;
    })
    .catch(error => console.error('Error:', error));

  // Set the countdown end time
  var countDownDate = new Date("Dec 20, 2024 20:00:00 GMT+0200").getTime();

  // Update the countdown every second
  var x = setInterval(function() {
    var now = new Date().getTime();
    var distance = countDownDate - now;

    if (distance < 0) {
      clearInterval(x);
      document.getElementById("countdown").textContent = "DING DING DING!";
      return;
    }

    var days = Math.floor(distance / (1000 * 60 * 60 * 24));
    var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
    var seconds = Math.floor((distance % (1000 * 60)) / 1000);

    document.getElementById("countdown").textContent = 
      days + " zile " + hours + " ore " + minutes + " min " + seconds + " sec ";
  }, 1000);
})();
</script>


