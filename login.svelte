<script>
    let username = '';
    let password = '';
  
    function handleSubmit(event) {
        event.preventDefault();
        console.log("Username:", username);
        console.log("Password:", password);
        // You can handle form submission here, e.g., send data to a server
    }
  </script>
  
  <style lang="css">
    body {
        font-family: Arial, sans-serif;
        margin: 0;
        padding: 0;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
        background-color: #e6e6e6; /* Light grey background */
    }
  
    .login-container {
        background-color: #38ad5e; /* Green background */
        padding: 40px;
        border-radius: 30px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        text-align: center;
        color: white;
        max-width: 400px;
        width: 100%;
    }
  
    h1 {
        margin-bottom: 20px;
        font-size: 24px;
        font-weight: bold;
    }
  
    .input-group {
        margin-bottom: 20px;
        position: relative;
    }
  
    .input-group .icon {
        position: absolute;
        left: 10px;
        top: 50%;
        transform: translateY(-50%);
        color: #ccc;
        font-size: 20px;
    }
  
    input[type="text"],
    input[type="password"] {
        width: 100%;
        padding: 10px 40px; /* Space for the icon */
        border-radius: 5px;
        border: none;
        background-color: #1b3a4b; /* Dark blue background */
        color: #ccc; /* Light grey text color */
    }
  
    button {
        width: 100%;
        padding: 10px;
        border: none;
        border-radius: 5px;
        background-color: #ff3e00; /* Bright orange */
        color: white;
        font-size: 18px;
        cursor: pointer;
        transition: background-color 0.3s ease;
    }
  
    button:hover {
        background-color: #e63600;
    }
  </style>
  
  <div class="login-container">
    <h1>USER LOGIN</h1>
    <form on:submit={handleSubmit}>
        <div class="input-group">
            <span class="icon">&#128100;</span>
            <input type="text" placeholder="Username" bind:value={username} required>
        </div>
        <div class="input-group">
            <span class="icon">&#128274;</span>
            <input type="password" placeholder="Password" bind:value={password} required>
        </div>
        <button type="submit">LOGIN</button>

        
        
    </form>
  </div>
  
