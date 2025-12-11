---
layout: single
title: "Donații de Crăciun 2025"
footer:
  content: "© 2025 Boatyardx Team Christmas Charity."
---

![Donații de Crăciun pentru Casa AKSZA](/assets/images/byx_christmas3.png){: .align-center}

Se apropie Crăciunul, și ne-am gândit că e momentul perfect să facem ceva frumos împreună. Anul acesta vrem să strângem bani pentru [Casa AKSZA](https://www.facebook.com/Aksza2000/?locale=ro_RO) — vecinii noștri de pe Emil Racoviță nr. 59, un loc care face diferența în viețile copiilor care au cel mai mare nevoie de ajutor.

Știu că fiecare deja avem cheltuieli de sărbători, dar chiar și o sumă mică poate însemna enorm pentru acești copii. Când ne strângem cu toții, fiecare contribuție se adună și devine ceva cu adevărat special.

Orice sumă ajută — nu contează cât.

Cine dorește să contribuie, poate trimite donații până pe 22 decembrie la:

**Revolut:** @razvanbalsan  
**ING:** RO93INGB0000999905486139  
**Nume:** Razvan Balsan  
**Detalii plată:** BYX Christmas

<div id="fetched-value" style="font-size:1.5em; font-weight:bold; text-align:center; margin-top:20px;"></div>

## Au mai ramas:
{: .text-center}

<div id="countdown" style="font-size:2em; font-weight:bold; text-align:center; margin-top:50px;"></div>


<script>
(function() {
  var countDownDate = new Date("Dec 22, 2025 20:00:00 GMT+0200").getTime();

  // Function to fetch and update the fetched value
function fetchAndUpdateValue() {
  fetch('https://docs.google.com/spreadsheets/d/e/2PACX-1vROjsHIF-GmltYCqh3cwRwqpMIhvXZGOT_aXMEzmCZFmcCwspGeTs7AQfkf21nYp0fDZXJS7GXc__J1/pub?gid=0&single=true&output=csv', {
    cache: "no-cache"
  })
    .then(response => response.text())
    .then(data => {
      const rows = data.split('\n').map(row => row.split(','));
      const fetchedValue = rows[0][0]; 
      
      // Update the fetched value in the DOM with multi-line text
      const fetchedValueDiv = document.getElementById('fetched-value');
      fetchedValueDiv.innerHTML = `
        <div style="text-align: center;">Până acum, am reușit să strângem</div>
        <div style="text-align: center; font-size: 1.5em; font-weight: bold; color: red;">${fetchedValue} lei</div>
      `;
    })
    .catch(error => console.error('Error:', error));
}


  // Function to update the countdown
  function updateCountdown() {
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

    // Update the countdown text
    const countdownDiv = document.getElementById("countdown");
    countdownDiv.textContent = 
      days + " zile " + hours + " ore " + minutes + " min " + seconds + " sec ";

    // Change countdown colour to red if 1 day or less is remaining
    if (days < 1) {
      countdownDiv.style.color = "red";
      countdownDiv.style.fontWeight = "bold";
    } else {
      countdownDiv.style.color = ""; // Reset to default
      countdownDiv.style.fontWeight = "";
    }
  }

  // Fetch value and update countdown initially
  fetchAndUpdateValue();
  updateCountdown();

  // Auto-update the fetched value every 5 seconds
  setInterval(fetchAndUpdateValue, 10000);

  // Update the countdown every second
  var x = setInterval(updateCountdown, 1000);
})();
</script>
