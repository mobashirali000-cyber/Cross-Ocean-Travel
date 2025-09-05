<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Cross Ocean Travel Agency</title>
  <style>
    body {
      margin: 0;
      font-family: "Segoe UI", Arial, sans-serif;
      background-color: #f5f5f5;
      color: #333;
    }

    /* Hero Section */
    .hero {
      background: url('https://picsum.photos/1920/800?travel') center/cover no-repeat;
      padding: 80px 20px;
      text-align: center;
      color: #fff;
      position: relative;
    }
    .hero::after {
      content: "";
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      background: rgba(0, 0, 0, 0.5);
    }
    .hero-content {
      position: relative;
      z-index: 1;
      max-width: 800px;
      margin: auto;
    }
    .hero h1 {
      font-size: 48px;
      margin-bottom: 20px;
    }

    /* Search Box */
    .search-box {
      background: rgba(0, 51, 102, 0.95);
      padding: 30px;
      border-radius: 12px;
      margin-top: 20px;
    }
    .search-box h2 {
      color: #fff;
      margin-bottom: 20px;
    }
    .search-box label {
      color: #eee;
      font-weight: bold;
      display: block;
      margin-top: 10px;
      font-size: 14px;
    }
    .search-box input, 
    .search-box select {
      width: 100%;
      padding: 10px;
      margin-top: 6px;
      border: none;
      border-radius: 5px;
    }
    .search-box button {
      margin-top: 20px;
      background: #8bc34a;
      border: none;
      padding: 14px;
      color: #fff;
      font-weight: bold;
      font-size: 16px;
      width: 100%;
      border-radius: 5px;
      cursor: pointer;
      transition: background 0.3s ease;
    }
    .search-box button:hover {
      background: #689f38;
    }

    /* About Section */
    .about {
      padding: 60px 20px;
      background: #fff;
      text-align: center;
    }
    .about h2 {
      font-size: 32px;
      margin-bottom: 20px;
    }
    .about p {
      max-width: 800px;
      margin: auto;
      line-height: 1.6;
    }

    /* Airline Section */
    .airline {
      padding: 60px 20px;
      background: #f0f8ff;
      text-align: center;
    }
    .airline h2 {
      font-size: 32px;
      margin-bottom: 20px;
    }
    .airline img {
      max-width: 350px;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.2);
      margin-bottom: 15px;
    }
    .airline p {
      font-size: 18px;
      font-weight: bold;
    }

    /* Footer */
    footer {
      background: #003366;
      color: #fff;
      text-align: center;
      padding: 20px;
      margin-top: 40px;
    }
  </style>
</head>
<body>

  <!-- Hero -->
  <div class="hero">
    <div class="hero-content">
      <h1>Cross Ocean Travel</h1>
      <p>Find the best flights across the globe at unbeatable prices</p>

      <!-- Search Box -->
      <div class="search-box">
        <h2>Search Flights</h2>
        <form>
          <label>Flying From:</label>
          <input type="text" placeholder="Departure Airport">

          <label>Flying To:</label>
          <input type="text" placeholder="Destination Airport">

          <label>Departure Date:</label>
          <input type="date">

          <label>Return Date:</label>
          <input type="date">

          <label>Passengers:</label>
          <select>
            <option>1</option>
            <option>2</option>
            <option>3</option>
            <option>4+</option>
          </select>

          <label>Class of Service:</label>
          <select>
            <option>Economy</option>
            <option>Premium Economy</option>
            <option>Business</option>
            <option>First</option>
          </select>

          <label>Airline:</label>
          <select id="airlines"></select>

          <button type="button">Search Flights</button>
        </form>
      </div>
    </div>
  </div>

  <!-- About -->
  <div class="about">
    <h2>About Us</h2>
    <p>
      Cross Ocean Travel has been a leading supplier of VFR flight tickets for almost 40 years.
      We started with flights to the Middle East, and today we proudly serve Africa, India,
      and many other destinations worldwide. We also specialize in Hajj and Umrah flights.
    </p>
  </div>

  <!-- Featured Airline -->
  <div class="airline">
    <h2>Featured Airline</h2>
    <img src="https://upload.wikimedia.org/wikipedia/commons/d/d3/British_Airways_A380.jpg" alt="British Airways">
    <p>British Airways (BA)</p>
  </div>

  <!-- Footer -->
  <footer>
    <p>&copy; 2025 Cross Ocean Travel Agency. All Rights Reserved.</p>
  </footer>

  <script>
    // Airline IATA codes
    const airlines = [
      { code: "AA", name: "American Airlines" },
      { code: "AF", name: "Air France" },
      { code: "BA", name: "British Airways" },
      { code: "CX", name: "Cathay Pacific" },
      { code: "DL", name: "Delta Air Lines" },
      { code: "EK", name: "Emirates" },
      { code: "EY", name: "Etihad Airways" },
      { code: "LH", name: "Lufthansa" },
      { code: "QR", name: "Qatar Airways" },
      { code: "SQ", name: "Singapore Airlines" },
      { code: "TK", name: "Turkish Airlines" },
      { code: "UA", name: "United Airlines" },
      { code: "VS", name: "Virgin Atlantic" }
    ];

    const airlineSelect = document.getElementById("airlines");
    airlines.forEach(a => {
      const option = document.createElement("option");
      option.value = a.code;
      option.textContent = `${a.name} (${a.code})`;
      airlineSelect.appendChild(option);
    });
  </script>

</body>
</html>
