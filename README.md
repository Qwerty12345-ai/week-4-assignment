# week-4-assignment
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Layout</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header class="navbar">
    <nav class="nav-links">
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#services">Services</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>
  <main class="content">
    <section class="grid-item" id="home">Home Content</section>
    <section class="grid-item" id="about">About Content</section>
    <section class="grid-item" id="services">Services Content</section>
    <section class="grid-item" id="contact">Contact Content</section>
  </main>
  <footer class="footer">© 2025 My Website</footer>
</body>
</html>

### css
/* Base Styles */
body {
  margin: 0;
  font-family: Arial, sans-serif;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;
  background-color: #333;
  color: white;
}

.nav-links a {
  color: white;
  text-decoration: none;
  margin: 0 1rem;
}

.nav-links a:hover {
  text-decoration: underline;
}

.content {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1rem;
  padding: 1rem;
}

.grid-item {
  background-color: #f4f4f4;
  padding: 1rem;
  border: 1px solid #ddd;
  border-radius: 5px;
}

.footer {
  text-align: center;
  padding: 1rem;
  background-color: #333;
  color: white;
}

/* Media Queries */
@media (max-width: 1200px) {
  .content {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (max-width: 768px) {
  .content {
    grid-template-columns: repeat(2, 1fr);
  }

  .nav-links {
    display: none;
  }
}

@media (max-width: 480px) {
  .content {
    grid-template-columns: 1fr;
  }

  .navbar {
    flex-direction: column;
    align-items: flex-start;
  }

  .nav-links {
    display: flex;
    flex-direction: column;
    width: 100%;
  }

  .nav-links a {
    margin: 0.5rem 0;
  }
}
