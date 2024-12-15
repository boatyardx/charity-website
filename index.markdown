---
layout: single
title: "Raise Funds, Break Bosses"
header:
  feature_image: /assets/images/poor_sorin.jpg
  # overlay_filter: 0.5  # Optional: adds a dark overlay for better text contrast
---

Se apropie Crăciunul — perioada în care, teoretic, nimeni nu cheltuie bani, nu-i așa? Ei bine, m-am gândit să profit un pic de generozitatea voastră, și nu doar atât. Vrem să strângem niște bănuți pentru a sprijini [Casa de Copii Căsuța Bucuriei](https://www.casutabucuriei.eu/).

Partea cea mai frumoasă este că l-am prins pe Sorin într-o dispoziție excelentă, iar anul acesta Boatyardx promite să dubleze fiecare leu pe care îl donăm noi!

Ho ho! Orice contribuție, oricât de mică, ajută enorm.

Cine dorește să ajute, poate trimite donațiile până pe 18 decembrie la:

**Revolut:** @razvanbalsan  
**ING:** RO93INGB0000999905486139  
**Nume:** Razvan Balsan  
**Detalii plată:** BYX Christmas

## Au mai ramas:
{: .text-center}

<div id="countdown" style="font-size:2em; font-weight:bold; text-align:center; margin-top:50px;"></div>

<script>
(function() {
  // Set the date and time of the countdown end in Bucharest time (UTC+2)
  var countDownDate = new Date("Dec 18, 2024 20:00:00 GMT+0200").getTime();

  // Update every 1 second
  var x = setInterval(function() {
    var now = new Date().getTime();
    var distance = countDownDate - now;

    // Time calculations for days/hours/minutes/seconds
    var days = Math.floor(distance / (1000 * 60 * 60 * 24));
    var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
    var seconds = Math.floor((distance % (1000 * 60)) / 1000);

    // Display the result
    document.getElementById("countdown").innerHTML = 
      days + "d " + hours + "h " + minutes + "m " + seconds + "s ";

    // If the countdown is over
    if (distance < 0) {
      clearInterval(x);
      document.getElementById("countdown").innerHTML = "IT'S TIME!";
    }
  }, 1000);
})();
</script>

