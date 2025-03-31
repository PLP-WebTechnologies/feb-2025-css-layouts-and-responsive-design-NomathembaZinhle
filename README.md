//HTML Structure
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Layout with Flexbox</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <nav>
      <ul class="nav-list">
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section class="content">
      <h1>Welcome to Our Website</h1>
      <p>This is a simple webpage layout using Flexbox and media queries.</p>
    </section>
    <section class="content">
      <h2>Our Services</h2>
      <p>Learn about our amazing services offered to clients worldwide.</p>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Company Name. All Rights Reserved.</p>
  </footer>
</body>
</html>

//CSS Styles (styles.css)
/* Reset some default margins and padding */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Body styling */
body {
  font-family: Arial, sans-serif;
  background-color: #f4f4f4;
  color: #333;
}

/* Header and Navigation */
header {
  background-color: #333;
  padding: 10px 0;
}

nav {
  max-width: 1200px;
  margin: 0 auto;
}

.nav-list {
  list-style: none;
  display: flex;
  justify-content: center;
}

.nav-list li {
  margin: 0 15px;
}

.nav-list a {
  color: white;
  text-decoration: none;
  font-size: 18px;
}

/* Main Content */
main {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin: 20px;
}

.content {
  flex: 1 1 45%; /* Flexbox layout, each content section takes up 45% of the width */
  margin: 10px;
  background-color: #fff;
  padding: 20px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

h1, h2 {
  color: #333;
}

/* Footer */
footer {
  background-color: #333;
  color: white;
  text-align: center;
  padding: 10px 0;
}

//Step 2: Media Queries for Responsiveness
/* Mobile Styles */
@media (max-width: 600px) {
  .nav-list {
    flex-direction: column; /* Stack the navigation links vertically */
    text-align: center;
  }

  .nav-list li {
    margin: 10px 0; /* Space between the links */
  }

  main {
    flex-direction: column; /* Stack the content sections vertically on mobile */
    margin: 10px;
  }

  .content {
    flex: 1 1 100%; /* Each section takes up the full width */
    margin: 5px 0;
  }
}

/* Tablet Styles */
@media (max-width: 900px) {
  main {
    flex-direction: column; /* Stack content sections vertically on tablets */
    margin: 20px;
  }

  .content {
    flex: 1 1 100%; /* Each section takes up the full width */
    margin: 10px 0;
  }
}

/* Desktop Styles (default - already set for larger screens) */
@media (min-width: 901px) {
  .nav-list {
    justify-content: space-between; /* Distribute nav items horizontally */
  }

  .content {
    flex: 1 1 45%; /* Ensure content sections take up 45% width */
    margin: 10px;
  }
}

