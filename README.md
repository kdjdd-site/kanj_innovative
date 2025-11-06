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

    /* ====== SCHOLARSHIP STYLES ====== */
    .scholarship-box {
      background: #fff;
      border-radius: 10px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
      margin: 20px auto;
      max-width: 800px;
      overflow: hidden;
    }

    .toggle-btn {
      width: 100%;
      background: #004aad;
      color: white;
      border: none;
      padding: 15px 20px;
      text-align: left;
      font-size: 1.1rem;
      cursor: pointer;
      font-weight: 600;
      transition: background 0.3s;
    }

    .toggle-btn:hover {
      background: #0b63f6;
    }

    .details {
      display: none;
      background: #f9fbff;
      padding: 20px;
      border-top: 1px solid #cdd8f0;
      line-height: 1.7;
      color: #333;
    }

    .details a {
      color: #0056d6;
      text-decoration: underline;
    }

    .details p {
      margin-bottom: 10px;
    }

    .details ul {
      margin-left: 20px;
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
        Explore B.Tech, BE, M.Tech, ME, and Diploma engineering programs in Gujarat.
      </p>
    </section>

    <section id="colleges">
      <h2>Government Colleges</h2>
      <p>
        Discover Gujarat Government Colleges for Engineering and Diploma students.
      </p>
    </section>

    <!-- ====== SCHOLARSHIP SECTION ====== -->
    <section id="scholarship">
      <h2>Scholarship Section</h2>
      <p>Click on a scholarship title to view full details:</p>

      <!-- Scholarship 1 -->
      <div class="scholarship-box">
        <button class="toggle-btn" onclick="toggleDetails(this)">
          Mukhyamantri Yuva Swavalamban Yojana (MYSY)
        </button>
        <div class="details">
          <p><b>Link:</b> 
            <a href="https://www.myscheme.gov.in/schemes/mysy" target="_blank">
              https://www.myscheme.gov.in/schemes/mysy
            </a>
          </p>

          <p><b>Expected Amount:</b></p>
          <ul>
            <li>₹50,000 tuition fee grant for BE/B.Tech</li>
            <li>₹25,000 tuition fee grant for Diploma</li>
            <li>₹5,000 book/instrument grant for engineering courses</li>
            <li>₹3,000 for diploma students</li>
            <li>₹1,200/month hostel grant for away-from-home students</li>
          </ul>

          <p><b>Eligibility:</b></p>
          <ul>
            <li>Must be from Gujarat</li>
            <li>For Diploma: Class X with ≥80%</li>
            <li>For Degree: Class XII with ≥80%</li>
            <li>For Diploma to Degree: Diploma ≥65%</li>
            <li>Family income ≤ ₹6,00,000</li>
          </ul>

          <p><b>Documents Required:</b></p>
          <ul>
            <li>Income Certificate</li>
            <li>Self-Declaration Form</li>
            <li>Aadhaar Card</li>
            <li>10th & 12th Mark Sheets</li>
            <li>Institute Certificate</li>
            <li>Admission Letter & Fee Receipt</li>
            <li>Non-judicial Affidavit (₹20)</li>
            <li>Hostel Admission Letter (if applicable)</li>
          </ul>
        </div>
      </div>
      <!-- Scholarship 2 -->
      <div class="scholarship-box">
        <button class="toggle-btn" onclick="toggleDetails(this)">
         Digital Gujarat
        </button>
        <div class="details">
          <p><b>Link:</b> 
            <a href="[https://www.myscheme.gov.in/schemes/mysy](https://www.digitalgujarat.gov.in)" target="_blank">
             [ https://www.myscheme.gov.in/schemes/mysy](https://www.digitalgujarat.gov.in)
            </a>
          </p>

          <p><b>Eligibility Criteria:</b></p>
          <ul>
            <li>Must be a resident of Gujarat</li>
            <li>Must belong to SC/ST/OBC/EBC/Minority/Physically Disabled category</li>
            <li>Must be studying in a recognized college or university (in Gujarat or outside Gujarat)</li>
            <li>Annual family income limit (from all sources):
            SC/ST: ≤ ₹2,50,000
            OBC/EBC: ≤ ₹1,50,000 (rural) or ₹1,20,000 (urban)
            Minority: ≤ ₹2,00,000</li>
            <li>Must have passed the previous examination with at least 50% markss</li>
          </ul>

          <p><b>Documents Required:</b></p>
          <ul>
            <li>Income Certificate</li>
            <li>Passport Size Photoes</li>
            <li>Self-Declaration Form</li>
            <li>Caste Certificate</li>
            <li>Aadhaar Card</li>
            <li>10th & 12th Mark Sheets</li>
            <li>Institute Certificate</li>
            <li>Admission Letter & Fee Receipt</li>
            <li>Non-judicial Affidavit (₹20)</li>
            <li>Hostel Admission Letter (if applicable)</li>
          </ul>

          <p><b>Application Timeline (Usually):</b></p>
         <ul>
         <li>Opens: June–August every year</li>
         <li>Last Date: October–November (varies yearly)</li>
          </ul>
        </div>
    </section>

    <!-- ====== CONTACT ====== -->
    <section id="contact">
      <h2>Contact / Help</h2>
      <p>Naman Chauhaan: 9316027621</p>
    </section>
  </div>

  <!-- ====== SCRIPT ====== -->
  <script>
    function toggleDetails(button) {
      const details = button.nextElementSibling;
      const isVisible = details.style.display === "block";
      document.querySelectorAll(".details").forEach(d => d.style.display = "none");
      if (!isVisible) details.style.display = "block";
    }

    // Active link highlight
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
