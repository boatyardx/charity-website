---
layout: single
title: "Raise Funds, Break Bosses"
---

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

