<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1">

<title>Recommendations</title>

<style>

  body {

    font-family: Arial, sans-serif;

    margin: 20px;

  }

  .container {

    max-width: 600px;

    margin: auto;

  }

  form {

    display: flex;

    flex-direction: column;

  }

  input, textarea {

 margin-bottom: 18px;

    padding: 8px; font-size: 1em;

  }

  button {

    padding: 10px;

    background: #4a90e2;   color: white;

 border: none;

    cursor: pointer;

  }

  button:hover {

    background: #357abd;

  }

  #popup {

    display: none;

    position: fixed;

    top: 0; left: 0; right: 0; bottom: 0;

    background: rgba(0,0,0,0.5);

    justify-content: center;

    align-items: center;

  }

  #popup .message {

    background: white;

    padding: 20px;

    border-radius: 5px;

    text-align: center;

    max-width: 300px;

  }

  #close-btn {

    margin-top: 15px;

    padding: 8px 20px;

    cursor: pointer;

    background: #4a90e2;

    color: white;

    border: none;

  }

  #close-btn:hover {

    background: #357abd;

  }

</style>

</head>

<body>

<div class="container">

  <h2>Leave a Recommendation</h2>

  <form id="recForm">

    <input type="text" id="name" placeholder="Your Name" required>

    <textarea id="recommendation" rows="3" placeholder="Your Recommendation" required></textarea>

    <button type="submit">Submit</button>

  </form>

</div>



<div id="popup">

  <div class="message">

    <translate>Thank you for leaving a recommendation!</translate>

    <br>

    <button id="close-btn">Close</button>

  </div>

</div>



<script>

  const form = document.getElementById('recForm');

  const popup = document.getElementById('popup');

  const closeBtn = document.getElementById('close-btn');



  form.addEventListener('submit', function(e) {

    e.preventDefault();

    popup.style.display = 'flex';

    form.reset();

  });



  closeBtn.addEventListener('click', function() {

    popup.style.display = 'none';

  });

</script>

</body>

</html>

