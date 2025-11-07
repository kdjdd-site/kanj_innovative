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
      color: #fff;
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
      box-shadow: 4px 0 12px rgba(0, 0, 0, 0.2);
      z-index: 10;
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
      width: calc(100% - 230px);
      overflow-x: hidden;
    }

    section {
      position: relative;
      padding: 100px 40px;
      min-height: 100vh;
      color: #fff;
    }

    section::before {
      content: "";
      position: absolute;
      inset: 0;
      background: rgba(0, 0, 0, 0.45); /* overlay */
      z-index: 0;
    }

    section h2,
    section p {
      position: relative;
      z-index: 1;
    }

    section h2 {
      font-size: 2rem;
      color: #fff;
      margin-bottom: 15px;
      text-shadow: 0 2px 5px rgba(0,0,0,0.3);
    }

    section p {
      max-width: 900px;
      line-height: 1.7;
      font-size: 1.05rem;
    }

    /* ====== BACKGROUND IMAGES ====== */
    #home {
      background: url('images/home-bg.jpg') center center / cover no-repeat fixed;
    }
    #Courses\/Exams {
      background: url('images/courses-bg.jpg') center center / cover no-repeat fixed;
    }
    #Colleges {
      background: url('images/colleges-bg.jpg') center center / cover no-repeat fixed;
    }
    #scholarship {
      background: url('images/scholarship-bg.jpg') center center / cover no-repeat fixed;
    }
    #Contact {
      background: url('images/contact-bg.jpg') center center / cover no-repeat fixed;
    }

    /* ====== SCHOLARSHIP STYLES ====== */
    .scholarship-box {
      background: rgba(255, 255, 255, 0.15);
      border-radius: 10px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.3);
      margin: 20px auto;
      max-width: 800px;
      overflow: hidden;
      backdrop-filter: blur(8px);
    }

    .toggle-btn {
      width: 100%;
      background: rgba(0, 74, 173, 0.9);
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
      background: rgba(255, 255, 255, 0.1);
      padding: 20px;
      border-top: 1px solid #cdd8f0;
      line-height: 1.7;
      color: #fff;
    }

    .details a {
      color: #a8d0ff;
      text-decoration: underline;
    }

    .details ul {
      margin-left: 20px;
    }

    /* ====== TEAM SECTION ====== */
    #Contact h2 {
      color: #fff;
      font-size: 2rem;
      margin-bottom: 15px;
    }

    .team-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
      gap: 25px;
      justify-items: center;
      position: relative;
      z-index: 1;
    }

    .team-member {
      background: rgba(255, 255, 255, 0.15);
      border-radius: 15px;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.4);
      padding: 20px;
      width: 230px;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      backdrop-filter: blur(6px);
      color: #fff;
    }

    .team-member:hover {
      transform: translateY(-8px);
      box-shadow: 0 8px 25px rgba(0, 0, 0, 0.5);
    }

    .team-member img {
      width: 100%;
      height: 210px;
      object-fit: cover;
      border-radius: 12px;
      margin-bottom: 12px;
    }

    .team-member h3 {
      color: #fff;
      font-size: 1.1rem;
      margin-bottom: 5px;
    }

    .team-member .role {
      color: #b0cfff;
      font-size: 0.95rem;
      font-weight: 500;
      margin-bottom: 8px;
    }

    .team-member .phone,
    .team-member .email {
      color: #e8e8e8;
      font-size: 0.9rem;
      margin: 3px 0;
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
        margin-left: 0;
        width: 100%;
      }
      section {
        padding-top: 100px;
      }
      .team-member {
        width: 90%;
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
      <li><a href="#Courses/Exams">Courses</a></li>
      <li><a href="#Colleges">Colleges</a></li>
      <li><a href="#scholarship">Scholarship</a></li>
      <li><a href="#Contact">Contact</a></li>
    </ul>
  </div>

  <!-- ====== MAIN CONTENT ====== -->
  <div class="content">

    <section id="home">
      <h2>Welcome</h2>
      <p>Welcome to <b>Only For Student</b> — your one-stop platform for Gujarat students after 12th. Explore courses, government colleges, scholarships, eligibility criteria, and application links — all in one place.</p>
    </section>

    <section id="Courses/Exams">
      <h2>Courses/Exams</h2>
      <p>Explore B.Tech, BE, M.Tech, ME, and Diploma engineering programs in Gujarat.</p>
    </section>

   <section id="Colleges">
      <h2>College Section</h2>
      <p>Click on a College title to view full details:</p>
	  
      <div class="Colleges-box">
        <button class="toggle-btn" onclick="toggleDetails(this)">
          Lalbhai Dalpatbhai College of Engineering
        </button>
        <div class="details">
          <p><b>Link:</b> 
            <a href="http://ldce.ac.in/" target="_blank">
              L. D. College of Engineering
            </a>
          </p>

          <p><b>Fee Structure</b></p>
          <ul>
            <li>Boy:1500+college Stationary fee</li>
            <li>Girls:College Stationary Fee</li>
            <li>few student: only College Stationary Fee</li>
          </ul>

          <p><b>Branch</b></p>
          <ul>
            <li>Computer Science</li>
            <li>Civil Engineering</li>
            <li>Meachanical Engineering</li>
            <li>Electrical Engineering</li>
            <li>Rubber Engineering</li>
 	    <li>AIML Engineering</li>
	    <li>EC Engineering</li>
	    <li>More</li>
          </ul>

          <p><b>feedback</b></p>
          <ul>
            <li>Campus big</li>
            <li>Placement good</li>
            <li>large activitys</li>
            <li>many culture Program</li>
            <li>Many visits</li>
          </ul>
        </div>
      </div>
	  <!-- College 2 -->
      <div class="College-box">
        <button class="toggle-btn" onclick="toggleDetails(this)">
           Government Engineering College (GEC), rajkot
        </button>
        <div class="details">
          <p><b>Link:</b> 
            <a href="https://gecrajkot.ac.in/" target="_blank">
            https://gecrajkot.ac.in/
            </a>
          </p>

          <p><b>Fee Structure</b></p>
          <ul>
            <li>Boy:1500+college Stationary fee</li>
            <li>Girls:College Stationary Fee</li>
            <li>few student: only College Stationary Fee</li>
          </ul>

          <p><b>Branch</b></p>
          <ul>
            <li>Automobile Engineering </li>
            <li>Information Technology (IT)</li>
            <li>Civil Engineering</li>
            <li>Electrical Engineering</li>
            <li>Rubber Engineering</li>
 	    <li>AIML Engineering</li>
	    <li>EC Engineering</li>
	    <li>More</li>
          </ul>

          <p><b>feedback</b></p>
          <ul>
            <li>Good infrastructure,</li>
            <li>many culture Program</li>
            <li>best feculty</li>
            <li>helpful feculty</li>
            <li>Many visits</li>
          </ul>
        </div>
      </div>
	  <!-- College 3 -->
      <div class="College-box">
        <button class="toggle-btn" onclick="toggleDetails(this)">
          Government Engineering College (GEC), Bhavnagar
        </button>
        <div class="details">
          <p><b>Link:</b> 
            <a href="https://gecbhavnagar.ac.in/" target="_blank">
           https://gecbhavnagar.ac.in/
            </a>
          </p>

          <p><b>Fee Structure</b></p>
          <ul>
            <li>Boy:1500+college Stationary fee</li>
            <li>Girls:College Stationary Fee</li>
            <li>few student: only College Stationary Fee</li>
          </ul>

          <p><b>Branch</b></p>
          <ul>
            <li>Electronics & Communication Engineering </li>
            <li>production Engineering</li>
            <li>biosystem Engineering</li>
            <li>Electrical Engineering</li>
            <li>Rubber Engineering</li>
 	    <li>AIML Engineering</li>
	    <li>EC Engineering</li>
	    <li>More</li>
          </ul>

          <p><b>feedback</b></p>
          <ul>
            <li>qualified & helpful feculty</li>
            <li>Better placements in CSE/IT branches</li>
            <li>Hostel & canteen facilities average</li>
            <li>many culture Program</li>
            <li>Many visits</li>
          </ul>
        </div>
      </div>
	  <!-- College 4 -->
      <div class="College-box">
        <button class="toggle-btn" onclick="toggleDetails(this)">
          Government engineering college gandhinagar
        </button>
        <div class="details">
          <p><b>Link:</b> 
            <a href="https://www.gecg28.ac.in/cells/14/" target="_blank">
              GEC Gandhinagar 
            </a>
          </p>

          <p><b>Fee Structure</b></p>
          <ul>
            <li>Boy:1500+college Stationary fee</li>
            <li>Girls:College Stationary Fee</li>
            <li>few student: only College Stationary Fee</li>
          </ul>

          <p><b> Bachelour of Engineering Branch</b></p>
          <ul>
            <li>Computer Science</li>
            <li>Civil Engineering</li>
            <li>Meachanical Engineering</li>
            <li>Electrical Engineering</li>
            <li>Rubber Engineering</li>
 	    <li>AIML Engineering</li>
	    <li>EC Engineering</li>
	    <li>Biomedical Engineering</li>
        <li>Metallurgy Engineering</li>
	<p><b> master  of Engineering Branch</b></p>
        <li>Biomedical  Engineering</li>
        <li>computer  Engineering</li>
          </ul>
          <p><b>feedback</b></p>
          <ul>
            <li>Campus big</li>
            <li>Placement good</li>
            <li>large activitys</li>
            <li>many culture Program</li>
            <li>Many visits</li>
          </ul>
        </div>
      </div>
	  
	  <!-- College 5 -->
	  <div class="College-box">
        <button class="toggle-btn" onclick="toggleDetails(this)">
          Vishwakarma Government engineering college
        </button>
        <div class="details">
          <p><b>Link:</b> 
            <a href="https://www.vgecg.ac.in/" target="_blank">
            </a>
          </p>
          <p><b>Fee Structure</b></p>
          <ul>
            <li>Boy:1500+college Stationary fee</li>
            <li>Girls:College Stationary Fee</li>
            <li>few student: only College Stationary Fee</li>
          </ul>
          <p><b>Branch</b></p>
          <ul>
            <li>Computer Science</li>
            <li>Civil Engineering</li>
            <li>Mechanical Engineering</li>
            <li>Electrical Engineering</li>
            <li>Rubber Engineering</li>
 	    <li>AIML Engineering</li>
	    <li>EC Engineering</li>
	    <li>textile enginnering</li>
          </ul>
          <p><b>feedback</b></p>
          <ul>
            <li>Campus big</li>
            <li>Placement good</li>
            <li>large activitys</li>
            <li>many culture Program</li>
            <li>Many visits</li>
          </ul>
        </div>
      </div>
	  <!-- College 6 -->
      <div class="College-box">
        <button class="toggle-btn" onclick="toggleDetails(this)">
          The Maharaja Sayajirao University of Baroda
        </button>
        <div class="details">
          <p><b>Link:</b> 
            <a href="https://msubaroda.ac.in/" target="_blank">
            https://msubaroda.ac.in/
            </a>
          </p>

          <p><b>Fee Structure</b></p>
          <ul>
            <li>Boy:1500+college Stationary fee</li>
            <li>Girls:College Stationary Fee</li>
            <li>few student: only College Stationary Fee</li>
          </ul>

          <p><b>Branch</b></p>
          <ul>
            <li>chemical Engineering </li>
            <li>textile Engineering</li>
            <li>biosystem Engineering</li>
            <li>Electrical Engineering</li>
            <li>Rubber Engineering</li>
 	    <li>AIML Engineering</li>
	    <li>EC Engineering</li>
	    <li>More</li>
          </ul>

          <p><b>feedback</b></p>
          <ul>
            <li>good enviroment</li>
            <li>Placement good</li>
            <li>best feculty</li>
            <li>many culture Program</li>
            <li>Many visits</li>
          </ul>
        </div>
      </div>
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
        </div>
        <!-- Scholarship 3 -->
      <div class="scholarship-box">
    <button class="toggle-btn" onclick="toggleDetails(this)">
      Reliance Foundation Scholarship
    </button>
    <div class="details">
      <p><b>Link:</b><br>
        <a href="https://www.reliancefoundation.org/education/scholarships" target="_blank">
          https://www.reliancefoundation.org/education/scholarships
        </a>
      </p>

    <p><b>Expected Amount:</b></p>
    <ul>
      <li>Up to ₹2,00,000 per year for Undergraduate students</li>
      <li>Up to ₹6,00,000 total for Postgraduate students</li>
      <li>Additional mentorship, networking, and leadership training benefits</li>
    </ul>

    <p><b>Eligibility Criteria:</b></p>
    <ul>
      <li>Must be an Indian citizen</li>
      <li>Must be enrolled in a recognized undergraduate or postgraduate program in India</li>
      <li>For UG: Must have passed Class 12 with at least 60% marks</li>
      <li>For PG: Must have completed a relevant undergraduate degree with good academic record</li>
      <li>Family income must be ≤ ₹15,00,000 per annum (priority for ≤ ₹2,50,000)</li>
      <li>Selection based on merit and aptitude test performance</li>
    </ul>

    <p><b>Documents Required:</b></p>
    <ul>
      <li>Aadhaar Card</li>
      <li>Class 10th & 12th Mark Sheets</li>
      <li>Income Certificate</li>
      <li>Bonafide Certificate from current institute</li>
      <li>Recent Passport-size Photograph</li>
      <li>Bank Account Proof (student’s name printed)</li>
      <li>Academic transcripts (UG/PG as applicable)</li>
    </ul>

    <p><b>Application Timeline:</b></p>
    <ul>
      <li>Opens: August every year</li>
      <li>Closes: Around October</li>
    </ul>

    <p><b>Selection Process:</b></p>
    <ul>
      <li>Online application submission</li>
      <li>Aptitude test (online)</li>
      <li>Personal interview (for shortlisted candidates)</li>
    </ul>
      </div>
    </div>
    <!-- Scholarship 4 -->
    <div class="scholarship-box">
      <button class="toggle-btn" onclick="toggleDetails(this)">
        NSP Post-Matric Scholarship (SC/ST/OBC)
      </button>
      <div class="details">
        <p><b>Link:</b><br>
          <a href="https://scholarships.gov.in" target="_blank">
            https://scholarships.gov.in
          </a>
        </p>

    <p><b>Expected Amount:</b></p>
    <ul>
      <li>₹3,000 to ₹12,000 per year (depending on category & course)</li>
      <li>Full or partial tuition fee reimbursement</li>
      <li>Hostel maintenance allowance: ₹1,200/month</li>
    </ul>

    <p><b>Eligibility Criteria:</b></p>
    <ul>
      <li>Must belong to SC/ST/OBC category</li>
      <li>Studying in Class 11 or higher (recognized institution)</li>
      <li>Annual family income ≤ ₹2,50,000 (SC/ST) or ₹1,50,000 (OBC)</li>
    </ul>

    <p><b>Documents Required:</b></p>
    <ul>
      <li>Caste Certificate</li>
      <li>Income Certificate</li>
      <li>Bonafide Certificate</li>
      <li>Mark Sheets (previous exam)</li>
      <li>Aadhaar Card</li>
      <li>Bank Passbook copy</li>
    </ul>
    </div>
      </div>
  <!-- Scholarship 5 -->
    <div class="scholarship-box">
      <button class="toggle-btn" onclick="toggleDetails(this)">
        AICTE Pragati Scholarship for Girls
      </button>
      <div class="details">
        <p><b>Link:</b><br>
          <a href="https://www.aicte-pragati-saksham-gov.in" target="_blank">
            https://www.aicte-pragati-saksham-gov.in
          </a>
        </p>

    <p><b>Expected Amount:</b></p>
    <ul>
      <li>₹50,000 per annum for tuition fees</li>
      <li>Additional ₹2,000 per month for 10 months (book allowance)</li>
      <li>Valid for up to 4 years (UG) or duration of course</li>
    </ul>

    <p><b>Eligibility Criteria:</b></p>
    <ul>
      <li>Girl student admitted to AICTE-approved technical institution</li>
      <li>Family income ≤ ₹8,00,000 per annum</li>
      <li>Maximum two girls per family eligible</li>
    </ul>

    <p><b>Documents Required:</b></p>
    <ul>
      <li>Aadhaar Card</li>
      <li>Family Income Certificate</li>
      <li>Admission proof (AICTE-approved institute)</li>
      <li>10th & 12th Mark Sheets</li>
      <li>Bank Account details</li>
      <li>Bonafide Certificate from Institute</li>
    </ul>
      </div>
    </div>
<!-- Scholarship 7 -->
    <div class="scholarship-box">
      <button class="toggle-btn" onclick="toggleDetails(this)">
        ONGC Foundation Scholarship (For Engineering Students)
      </button>
    
      <div class="details">
        <p><b>Link:</b><br>
          <a href="https://www.ongcfoundation.org/scholarship" target="_blank">
            https://www.ongcfoundation.org/scholarship
          </a>
        </p>

    <p><b>Expected Amount:</b></p>
    <ul>
      <li>₹48,000 per year for 4 years (Total ₹1,92,000)</li>
      <li>For full-time Engineering (B.E./B.Tech) students in India</li>
      <li>Scholarship paid annually directly to student’s bank account</li>
    </ul>

    <p><b>Eligibility Criteria:</b></p>
    <ul>
      <li>Must be an Indian citizen and a resident of Gujarat</li>
      <li>Studying in the first year of Engineering (AICTE-approved institute)</li>
      <li>Minimum 60% marks in Class 12 (PCM group)</li>
      <li>Family annual income limit:
        <ul>
          <li>SC/ST category: ≤ ₹4,50,000</li>
          <li>OBC/General category: ≤ ₹2,00,000</li>
        </ul>
      </li>
      <li>Age below 30 years as of 31st December of the academic year</li>
      <li>Selection based purely on merit and eligibility</li>
    </ul>

    <p><b>Documents Required:</b></p>
    <ul>
      <li>Aadhaar Card</li>
      <li>Income Certificate (issued by competent authority)</li>
      <li>Caste Certificate (if applicable)</li>
      <li>10th & 12th Mark Sheets</li>
      <li>Admission Letter / Fee Receipt</li>
      <li>Bonafide Certificate from Institute</li>
      <li>Bank Passbook copy (student’s name must be printed)</li>
      <li>Passport-size Photograph</li>
    </ul>

    <p><b>Application Timeline:</b></p>
    <ul>
      <li>Usually opens: October – November</li>
      <li>Last date: December (varies each year)</li>
      <li>Apply through ONGC Foundation official website</li>
    </ul>

    <p><b>Selection Process:</b></p>
    <ul>
      <li>Online application submission via ONGC Foundation portal</li>
      <li>Shortlisting based on academic performance and income</li>
      <li>Verification and approval by ONGC Foundation committee</li>
    </ul>
      </div>
    </div>

        </section>


    <section id="Contact">
      <h2>Our Team</h2>
      <p>Meet the <b>Only For Student</b> team — helping Gujarat students with all opportunities in one place.</p>

      <div class="team-container">
        <div class="team-member">
          <img src="images/krish.jpg" alt="Krish Dodiya">
          <h3>Krish Dodiya</h3>
          <p class="role">Developer</p>
          <p class="phone">📞 +91 98765 41070</p>
          <p class="email">✉️ 24eedod@ldce.ac.in</p>
        </div>

        <div class="team-member">
          <img src="3.jpg" alt="Abhishek Makwana">
          <h3>Abhishek Makwana</h3>
          <p class="role">Creator</p>
          <p class="phone">📞 +91 93160 27621</p>
          <p class="email">✉️ 24eeabh@ldce.ac.in</p>
        </div>

        <div class="team-member">
          <img src="1.jpg" alt="Naman Chauhaan">
          <h3>Naman Chauhaan</h3>
          <p class="role">Researcher + Designer</p>
          <p class="phone">📞 +91 98245 11234</p>
          <p class="email">✉️ 24eenam@ldce.ac.in</p>
        </div>

        <div class="team-member">
          <img src="2.jpg" alt="Jaydeep Makvana">
          <h3>Jaydeep Makvana</h3>
          <p class="role">Researcher</p>
          <p class="phone">📞 +91 98765 55678</p>
          <p class="email">✉️ 24eejay@ldce.ac.in</p>
        </div>
      </div>
    </section>
  </div>

  <script>
    function toggleDetails(button) {
      const details = button.nextElementSibling;
      const isVisible = details.style.display === "block";
      document.querySelectorAll(".details").forEach(d => d.style.display = "none");
      if (!isVisible) details.style.display = "block";
    }
  </script>
</body>
</html>
