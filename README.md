
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Pizza Order</title>
</head>
<body>
  <h1>Pizza Order</h1>
  <form id="pizza-form">
    <label for="theme">What do you want to do?</label>
    <select id="theme" name="theme">
      <option value="order-pizza">Order a pizza</option>
      <option value="make-reservation">Make a reservation</option>
      <option value="ask-hours">Ask opening hours</option>
      <option value="talk-receptionist">Talk to the receptionist</option>
    </select>

    <label for="size">What size do you need?</label>
    <select id="size" name="size">
      <option value="jumbo">Jumbo</option>
      <option value="large">Large</option>
      <option value="standard">Standard</option>
      <option value="medium">Mediuiuuum</option>
      <option value="small">Small</option>
      <option value="micro">Micro</option>
    </select>

    <button type="submit">Submit</button>
  </form>

  <div id="result"></div>

  <script>
    const form = document.getElementById('pizza-form');
    form.addEventListener('submit', (event) => {
      event.preventDefault();

      const theme =  document.getElementById('theme').value;
      const size = document.getElementById('size').value;

      const result = {
        theme: theme,
        size: size.toLocaleLowerCase()
      };

      document.getElementById('result').textContent = JSON.stringify(result, null, 2);
    });
  </script>
</body>
</html>
