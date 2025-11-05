<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Only For Student</title>

  <style>
    /* ====== BASIC STYLES ====== */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
      font-family: "Poppins", sans-serif;
    }

    body {
      display: flex;
      min-height: 100vh;
      background: #f5faff;
      color: #222;
    }

    /* ====== SIDEBAR ====== */
    .sidebar {
      width: 230px;
      background: #004aad;
      color: #fff;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 30px 0;
      position: fixed;
      height: 100%;
      box-shadow: 4px 0 12px rgba(0, 0, 0, 0.1);
    }

    .sidebar h1 {
      font-size: 1.4rem;
      margin-bottom: 40px;
      text-align: center;
      letter-spacing: 1px;
    }

    .nav-links {
      list-style: none;
      width: 100%;
    }

    .nav-links li {
      width: 100%;
    }

    .nav-links a {
      display: block;
      padding: 14px 20px;
      color: #fff;
      text-decoration: none;
      transition: 0.3s;
      font-size: 1rem;
    }

    .nav-links a:hover {
      background: #0d6efd;
      padding-left: 25px;
    }

    /* ====== CONTENT AREA ====== */
    .content {
      margin-left: 230px;
      padding: 50px;
      width: 100%;
    }

    section {
      padding: 80px 20px;
      min-height: 100vh;
      border-bottom: 1px solid #ddd;
    }

    section h2 {
      font-size: 2rem;
      color: #004aad;
      margin-bottom: 15px;
    }

    section p {
      max-width: 900px;
      line-height: 1.7;
      font-size: 1.05rem;
      color: #333;
    }

    /* ====== RESPONSIVE ====== */
    @media (max-width: 768px) {
      .sidebar {
        position: relative;
        width: 100%;
        flex-direction: row;
        justify-content: space-around;
        height: auto;
      }
      .content {
        margin: 0;
      }
      section {
        padding-top: 100px;
      }
    }
  </style>
</head>

<body>
  <!-- ====== SIDEBAR ====== -->
  <div class="sidebar">
    <h1>Only For Student</h1>
    <ul class="nav-links">
      <li><a href="#home">Home</a></li>
      <li><a href="#courses">Courses</a></li>
      <li><a href="#colleges">Colleges</a></li>
      <li><a href="#scholarship">Scholarship</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </div>

  <!-- ====== MAIN CONTENT ====== -->
  <div class="content">
    <section id="home">
      <h2>Welcome</h2>
      <p>
        Welcome to <b>Only For Student</b> — your one-stop platform for Gujarat
        students after 12th. Explore courses, government colleges, scholarships,
        eligibility criteria, and application links — all in one place.
      </p>
    </section>

    <section id="courses">
      <h2>Courses</h2>
      <p>
        Available engineering courses under Gujarat Government:
        <br /><br />
        • B.Tech / B.E. – Bachelor of Engineering/Technology<br />
        • M.Tech / M.E. – Master of Engineering/Technology<br />
        • Diploma Engineering – Technical foundation after 10th or 12th<br /><br />
        Check eligibility, entrance exams, and seat availability in respective
        government institutes.
      </p>
    </section>

    <section id="colleges">
      <h2>Government Colleges</h2>
      <p>
        Here you’ll find details of Gujarat Government engineering colleges —
        including course offerings, admission process, cut-offs, and official
        apply links (coming soon).
      </p>
    </section>

    <section id="scholarship">
      <h2>Scholarship Section</h2>
      <p>
        Explore available Gujarat Government scholarships for engineering and
        diploma students. Click any scholarship to see:
      </p>
      <ul>
        <li>✅ Eligibility criteria</li>
        <li>📄 List of required documents</li>
        <li>📝 Application process & link</li>
      </ul>
      <p><br />Scholarship data & forms will be integrated here soon.</p>
    </section>

    <section id="contact">
      <h2>Contact / Help</h2>
      <p>
        Need guidance or help? Contact your college helpdesk or official Gujarat
        education portals. In future updates, this section will include direct
        student support and query forms.
      </p>
    </section>
  </div>

  <script>
    // Optional JS for active link highlight
    const links = document.querySelectorAll(".nav-links a");
    links.forEach(link => {
      link.addEventListener("click", () => {
        links.forEach(l => l.classList.remove("active"));
        link.classList.add("active");
      });
    });
  </script>
</body>
</html>
