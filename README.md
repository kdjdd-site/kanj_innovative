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
       
      </p>
    </section>

    <section id="colleges">
      <h2>Government Colleges</h2>
      <p>
       
      </p>
    </section>

   <section id="scholarship">
  <h2>Scholarship Section</h2>
  <p>Click a scholarship to view details:</p>

  <div class="scholarship-box">
    <button class="toggle-btn">Mukhyamantri Yuva Swavalamban Yojana (MYSY)</button>
    <div class="details">
      <p><b>Link:</b> <a href="https://www.myscheme.gov.in/schemes/mysy" target="_blank">https://www.myscheme.gov.in/schemes/mysy</a></p>
      <p><b>Expected Amount:</b><br>
        • ₹50,000 tuition fee grant for BE/B.Tech<br>
        • ₹25,000 tuition fee grant for Diploma<br>
        • ₹5,000 book/instrument grant for engineering courses<br>
        • ₹3,000 for diploma students<br>
        • ₹1,200/month hostel grant for away-from-home students
      </p>
      <p><b>Eligibility:</b><br>
        • Must be from Gujarat<br>
        • For Diploma: Class X with ≥80%<br>
        • For Degree: Class XII (Science/General) with ≥80%<br>
        • For Diploma to Degree: Diploma ≥65%<br>
        • Family income ≤ ₹6,00,000
      </p>
      <p><b>Documents Required:</b><br>
        • Income Certificate<br>
        • Self-Declaration Form<br>
        • Aadhaar Card<br>
        • 10th & 12th Mark Sheets<br>
        • Institute Certificate (for new students)<br>
        • Admission Letter & Fee Receipt<br>
        • Non-judicial affidavit (₹20)<br>
        • Hostel Admission Letter (if applicable)
      </p>
    </div>
  </div>
</section>

    <section id="contact">
      <h2>Contact / Help</h2>
   <p>Naman Chauhaan:-9316027621</p>
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
