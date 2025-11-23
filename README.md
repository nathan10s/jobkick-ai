JobFinder
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title> – CV & Cover Letter Helper</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background: #020617;
      color: #e5e7eb;
      line-height: 1.5;
    }
    a { color: #38bdf8; text-decoration: none; }
    a:hover { text-decoration: underline; }
    .page {
      max-width: 960px;
      margin: 0 auto;
      padding: 1.5rem;
    }
    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 2rem;
    }
    .logo {
      font-weight: 700;
      font-size: 1.25rem;
      color: #38bdf8;
    }
    .pill {
      font-size: 0.8rem;
      border-radius: 999px;
      padding: 0.25rem 0.75rem;
      border: 1px solid #38bdf8;
    }
    h1 {
      font-size: clamp(2rem, 3vw, 2.6rem);
      margin-bottom: 1rem;
    }
    .hero {
      display: grid;
      gap: 2rem;
    }
    @media (min-width: 768px) {
      .hero {
        grid-template-columns: 3fr 2fr;
        align-items: start;
      }
    }
    .badge {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      background: #020617;
      border-radius: 999px;
      padding: 0.25rem 0.75rem;
      border: 1px solid #1f2937;
      font-size: 0.8rem;
      color: #9ca3af;
      margin-bottom: 0.75rem;
    }
    .hero p { color: #9ca3af; margin-bottom: 1rem; }
    .btn {
      border-radius: 999px;
      padding: 0.6rem 1.2rem;
      border: none;
      cursor: pointer;
      font-weight: 600;
      font-size: 0.9rem;
    }
    .btn-primary {
      background: linear-gradient(135deg, #38bdf8, #22c55e);
      color: #020617;
      margin-right: 0.5rem;
    }
    .meta { font-size: 0.8rem; color: #6b7280; }
    .card {
      background: #020617;
      border-radius: 1rem;
      padding: 1rem;
      border: 1px solid #1f2937;
      box-shadow: 0 18px 40px rgba(0,0,0,0.5);
      font-size: 0.9rem;
    }
    label {
      display: block;
      font-size: 0.8rem;
      margin-bottom: 0.25rem;
      color: #9ca3af;
    }
    input, select, textarea {
      width: 100%;
      border-radius: 0.75rem;
      border: 1px solid #1f2937;
      padding: 0.55rem 0.75rem;
      background: #020617;
      color: #e5e7eb;
      font-size: 0.9rem;
      margin-bottom: 0.7rem;
    }
    textarea { min-height: 70px; resize: vertical; }
    .output {
      background: #020617;
      border-radius: 0.75rem;
      border: 1px dashed #1f2937;
      padding: 0.75rem;
      font-size: 0.85rem;
      color: #9ca3af;
      white-space: pre-wrap;
      margin-top: 0.5rem;
    }
    .section { margin-top: 2.5rem; }
    .section h2 { font-size: 1.2rem; margin-bottom: 0.75rem; }
    .grid {
      display: grid;
      gap: 1rem;
    }
    @media (min-width: 768px) {
      .grid-3 { grid-template-columns: repeat(3, minmax(0, 1fr)); }
    }
    .feature {
      border-radius: 0.9rem;
      background: #020617;
      border: 1px solid #1f2937;
      padding: 0.9rem;
      font-size: 0.85rem;
    }
    .feature h3 {
      font-size: 0.95rem;
      margin-bottom: 0.4rem;
      color: #e5e7eb;
    }
    footer {
      margin-top: 3rem;
      padding-top: 1.5rem;
      border-top: 1px solid #1f2937;
      font-size: 0.8rem;
      color: #6b7280;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      gap: 0.75rem;
      align-items: center;
    }
    .money-box {
      padding: 0.75rem;
      border-radius: 0.9rem;
      border: 1px dashed #22c55e55;
      background: #022c22;
      font-size: 0.85rem;
      color: #bbf7d0;
      margin-top: 0.5rem;
    }
    .tip-btn {
      display: inline-block;
      margin-top: 0.5rem;
      border-radius: 999px;
      padding: 0.4rem 0.9rem;
      border: 1px solid #22c55e;
      background: #022c22;
      color: #bbf7d0;
      font-size: 0.8rem;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div class="page">
    <header>
      <div class="logo">JobKick<span style="color:#22c55e">AI</span></div>
      <div class="pill">Remote · No Experience · UK Friendly</div>
    </header>

    <main>
      <section class="hero">
        <div>
          <div class="badge">
            <span>🧑‍💻</span>
            <span>Built for first jobs & remote applications</span>
          </div>
        <h1>Create stronger CVs and cover letters for remote & entry-level jobs.</h1>
<p>
  JobFinder helps you turn your skills and availability into clear CV summaries and simple cover letters
  you can use when applying for data entry, chat support, admin, and junior tech roles.
</p>

          <button class="btn btn-primary" id="scrollToForm">Try the demo</button>
          <p class="meta">
  Free CV & cover letter helper for entry-level and remote roles.
</p>


       <div class="money-box">
  <strong>💸 Support JobFinder & keep it free:</strong><br />
  – Use the recommended tools below when they’re helpful<br />
  – Share this site with friends who are job hunting
  <br />
  <a class="tip-btn"
     href="https://ko-fi.com/Nathan10s"
     target="_blank"
     rel="noopener">
    Tip the creator on Ko-fi
  </a>
</div>



        <div class="card" id="formCard">
          <h2 style="font-size:1.05rem; margin-bottom:0.5rem;">Quick demo</h2>
          <form id="demoForm">
            <label for="role">Target role</label>
            <select id="role" name="role">
              <option value="Data Entry Clerk">Data Entry Clerk (Remote)</option>
              <option value="Chat Support Agent">Chat Support Agent (Remote)</option>
              <option value="Content Moderator">Content Moderator</option>
              <option value="Junior Frontend Developer">Junior Frontend Developer</option>
            </select>

            <label for="skills">Your skills</label>
            <input id="skills" placeholder="typing, computer literacy, attention to detail" />

            <label for="hours">Availability</label>
            <input id="hours" placeholder="afternoons, evenings, weekends" />

            <label for="experience">Experience (optional)</label>
            <textarea id="experience"
              placeholder="No formal work yet, but I’ve completed online work experience and personal projects."></textarea>

            <button type="submit" class="btn btn-primary" style="width:100%; margin-top:0.25rem;">
              Generate sample CV text
            </button>
          </form>

          <div id="output" class="output">
            Fill the form and click the button to see sample CV text.
          </div>
        </div>


      <section class="section">
        <h2>Recommended resources (monetise with affiliate links later)</h2>
        <div class="grid grid-3">
          <div class="feature">
            <h3>Remote job boards</h3>
            <p>List 3–4 sites you genuinely like. Later, turn these into affiliate or referral links.</p>
          </div>
          <div class="feature">
            <h3>Courses you trust</h3>
            <p>Link to beginner HTML/CSS or CV-writing courses. Add affiliate tracking once you join their partner program.</p>
          </div>
          <div class="feature">
            <h3>Tools you use</h3>
            <p>Editors, portfolio hosts, CV builders. Many offer referral rewards when people sign up.</p>
          </div>
        </div>
      </section>

      <section class="section">
  <h2>Work with JobFinder</h2>
  <div class="feature">
    <p>
      JobFinder is a free tool designed to help people create better CVs and cover letters for entry-level and remote roles.
      In the future, this space may be used for partnerships with training providers, job boards, or tools that genuinely help job seekers.
    </p>
  </div>
</section>

  

<footer>
  <span>© <span id="year"></span> JobFinder – CV & Cover Letter Helper</span>
  <span>Built to help beginners apply for remote and entry-level jobs.</span>
</footer>

  </div>

  <script>
    document.getElementById('year').textContent = new Date().getFullYear();

    const form = document.getElementById('demoForm');
    const output = document.getElementById('output');

    form.addEventListener('submit', (e) => {
      e.preventDefault();
      const role = document.getElementById('role').value;
      const skillsRaw = document.getElementById('skills').value.trim();
      const hours = document.getElementById('hours').value.trim() || 'flexible afternoons and evenings';
      const exp = document.getElementById('experience').value.trim() || 'No formal work yet, but motivated to start and learn on the job.';

      const skills = skillsRaw || 'reliable, hard-working, willing to learn';
      const skillsList = skills.split(',').map(s => s.trim()).filter(Boolean);

      const text =
`CV Summary – ${role}
——————————
Reliable and motivated individual seeking a remote ${role.toLowerCase()}. Confident using computers and online tools, with skills in ${skills}. Able to work ${hours}, follow written instructions, and stay focused on accurate, consistent work.

Experience
——————————
Entry-level candidate – building experience through online work experience and self-study.
${exp}

Key Skills
——————————
${skillsList.map(s => '• ' + s).join('\n')}
• Strong attention to detail
• Able to work independently and meet deadlines
• Positive attitude and open to feedback`;

      output.textContent = text;
    });
<script src="https://cdn.counter.dev/script.js" data-id="e1251182-0cdb-4b37-b4a6-6f3fb7d76485" data-utcoffset="0"></script>
 
