# Survey_Form

<!DOCTYPE html>
<html>
<head>
  <title>Survey Form</title>
  <link rel="stylesheet" href="utils.css">
</head>
<body>
  <div class="container">
    <h1>Survey Form</h1>
    <form action="/submit-survey" method="post">
      <div class="row">
        <label for="firstName">First Name:</label>
        <input type="text" id="firstName" name="firstName" required>
      </div>
      <div class="row">
        <label for="lastName">Last Name:</label>
        <input type="text" id="lastName" name="lastName" required>
      </div>
      <div class="row">
        <label for="Date">DOB:</label>
        <input type="date" id="DOB" name="DOB" required>
      </div>
      <div class="row">
        <label for="country">Country:</label>
        <select id="country" name="country" required>
            <option>India</option>
            <option>Canada</option>
            <option>USA</option>
            <option>Russia</option>
            <option>Londan</option>
            <option>other</option>
        </select>
      </div>

      <div class="inline">
        <label for="gender">Gender:</label>
        <input type="radio"  id="gender" name="gender" required>Male
        <input type="radio"  id="gender" name="gender" required>female
        <input type="radio"  id="gender" name="gender" required>Other
      </div> <br>

      <div class="row">
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>
      </div>
      <div class="row">
        <label for="profession">Profession:</label>
        <input type="text" id="profession" name="profession" required>
      </div>
      <div class="row">
        <label for="phone">Phone Number :</label>
        <input type="tel" id="phone" name="phone" required>
      </div>

        <button type="submit">Submit</button>
        <button type="reset">Reset</button>
      </div>
    </form>
  </div>
  <script> 
    const form = document.querySelector('form');

form.addEventListener('submit', function(event) {
  const requiredFields = ['firstName', 'lastName','DOB','country','gender','email', 'profession', 'phone'];
  for (const field of requiredFields) {
    const input = document.querySelector(`[name="${field}"]`);
    if (input.value === '') {
      alert('Please fill in all the required fields.');
      event.preventDefault();
      return;
    }
  }

  this.submit();
});
  </script>
</body>
</html>

--------------------------CSS CODE---------------------------
.container {
    width: 400px;
    margin: 0 auto;
  }
  
  h1 {
    text-align: center;
    color:#460404;
  }
  
  form {
    margin-top: 20px;
  }
  
  .row {
    margin-bottom: 10px;
  }
  
  label {
    display: block;
    margin-bottom: 5px;
    color:#460404;
    font-weight: bold;
  }
  
  input,
  select,
  textarea {
    width: 100%;
    padding: 5px;
    border: 1px solid #ccc;
    border-radius: 3px;
  }
  
  textarea {
    height: 100px;
  }
  
  button {
    margin: 10px;
    text-align: center;
    background-color:#460404;
    color: #fff;
    padding: 10px 20px;
    border: 10px;
    border-radius: 3px;
  }

.inline{
    display: flex
    
    
}
