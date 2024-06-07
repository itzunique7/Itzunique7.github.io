<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Love Calculator</title>
<style>
  body {
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    flex-direction: column;
  }
  #result {
    margin-top: 20px;
  }
</style>
</head>
<body>
  <h1>Love Calculator</h1>
  <div>
    <input type="text" id="name1" placeholder="Your Name">
    <input type="text" id="name2" placeholder="Your Crush's Name">
    <button onclick="calculateLove()">Calculate</button>
  </div>
  <div id="result"></div>

<script>
function calculateLove() {
  var name1 = document.getElementById('name1').value;
  var name2 = document.getElementById('name2').value;

  if (name1 == '' || name2 == '') {
    alert('Please enter both names.');
    return;
  }

  // A simple algorithm to calculate love percentage (for fun)
  var loveScore = Math.floor(Math.random() * 100) + 1;

  // Displaying the result
  var resultElement = document.getElementById('result');
  resultElement.innerHTML = name1 + ' and ' + name2 + 
                            ' have a ' + loveScore + '% chance of love compatibility!';
}
</script>
</body>
</html>
