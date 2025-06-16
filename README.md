# PRODIGY_DS_01
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Interactive Nav Menu</title>
  <style>
    /* Reset default margin/padding */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      line-height: 1.6;
    }

    /* Navigation Styles */
    .navbar {
      position: fixed;
      top: 0;
      width: 100%;
      background-color: transparent;
      display: flex;
      justify-content: center;
      gap: 40px;
      padding: 20px 0;
      transition: background-color 0.3s ease, box-shadow 0.3s ease;
      z-index: 1000;
    }

    .navbar.scrolled {
      background-color: #333;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
    }

    .navbar a {
      color: #fff;
      text-decoration: none;
      font-size: 18px;
      padding: 8px 16px;
      transition: color 0.3s ease, border-bottom 0.3s ease;
    }

    .navbar a:hover {
      color: #ffcc00;
      border-bottom: 2px solid #ffcc00;
    }

    /* Add spacing to see scroll effect */
    .content {
      padding-top: 100px;
      padding: 40px;
      height: 2000px;
      background: linear-gradient(to bottom, #f0f0f0, #e0e0e0);
    }
  </style>
</head>
<body>

  <!-- Navigation Bar -->
  <nav class="navbar" id="navbar">
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#services">Services</a>
    <a href="#contact">Contact</a>
  </nav>

  <!-- Sample Content -->
  <div class="content">
    <h1>Welcome to My Website</h1>
    <p>Scroll down to see the nav bar change.</p>
  </div>

  <!-- JavaScript -->
  <script>
    const navbar = document.getElementById('navbar');

    window.addEventListener('scroll', () => {
      if (window.scrollY > 50) {
        navbar.classList.add('scrolled');
      } else {
        navbar.classList.remove('scrolled');
      }
    });
  </script>

</body>
</html>
