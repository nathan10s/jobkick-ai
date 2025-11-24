
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>JobFinder – CV & Cover Letter Helper</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      /* More standout background */
      background: radial-gradient(circle at top, #0ea5e9 0, #0f172a 40%, #020617 100%);
      color: #e5e7eb;
      line-height: 1.6;
      font-size: 18px; /* Bigger base text */
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
      font-weight: 800;
      font-size: 1.5rem;
      color: #e5e7eb;
    }

    .logo span {
      color: #22c55e;
    }

    .pill {
      font-size: 0.85rem;
      border-radius: 999px;
      padding: 0.25rem 0.9rem;
      border: 1px solid #38bdf8;
      background: rgba(15, 23, 42, 0.8);
      backdrop-filter: blur(6px);
    }

    h1 {
      font-size: clamp(2.3rem, 4.2vw, 3rem);
      margin-bottom: 1.1rem;
    }

    .hero {
      display: grid;
      gap: 2rem;
    }

    @media (min-width: 768px) {
      .hero {
        grid-template-columns: 3fr 2.2fr;
        align-items: start;
      }
    }

    .badge {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      background: rgba(15, 23, 42, 0.9);
      border-radius: 999px;
      padding: 0.3rem 0.9rem;
      border: 1px solid #1f2937;
      font-size: 0.85rem;
      color: #9ca3af;
      margin-bottom: 0.85rem;
    }

    .hero p {
      color: #cbd5f5;
      margin-bottom: 1rem;
      font-size: 1rem;
    }

    .btn {
      border-radius: 999px;
      padding: 0.7rem 1.4rem;
      border: none;
      cursor: pointer;
      font-weight: 600;
      font-size: 0.95rem;
    }

    /* Eye-catching primary button */
    .btn-primary {
      background: linear-gradient(135deg, #22c55e, #a3e635);
      color: #022c22;
      margin-right: 0.5rem;
      box-shadow: 0 12px 30px rgba(34, 197, 94, 0.35);
      transition: transform 0.08s ease, box-shadow 0.08s ease;
    }

    .btn-primary:hover {
      transform: translateY(-1px);
      box-shadow: 0 16px 36px rgba(34, 197, 94, 0.45);
    }

    .meta {
      font-size: 0.85rem;
      color: #9ca3af;
      margin-top: 0.35rem;
    }

    .card {
      background: rgba(15, 23, 42, 0.95);
      border-radius: 1.1rem;
      padding: 1.4rem;
      border: 1px solid #1f2937;
      box-shadow: 0 18px 40px rgba(0,0,0,0.55);
      font-size: 1rem;
    }

    label {
      display: block;
      font-size: 0.9rem;
      margin-bottom: 0.25rem;
      color: #9ca3af;
    }

    input, select, textarea {
      width: 100%;
      border-radius: 0.8rem;
      border: 1px solid #1f2937;
      padding: 0.6rem 0.8rem;
      background: #020617;
      color: #e5e7eb;
      font-size: 0.95rem;
      margin-bottom: 0.8rem;
    }

    textarea { min-height: 80px; resize: vertical; }

    .output {
      background: #020617;
      border-radius: 0.9rem;
      border: 1px dashed #1f2937;
      padding: 0.85rem;
      font-size: 0.9rem;
      color: #9ca3af;
      white-space: pre-wrap;
      margin-top: 0.7rem;
    }

    .section {
      margin-top: 2.7rem;
    }

    .section h2 {
      font-size: 1.4rem;
      margin-bottom: 0.85rem;
      font-weight: 600;
    }

    .grid {
      display: grid;
      gap: 1rem;
    }

    @media (min-width: 768px) {
      .grid-3 { grid-template-columns: repeat(3, minmax(0, 1fr)); }
    }

    .feature {
      border-radius: 0.95rem;
      background: rgba(15, 23, 42, 0.95);
      border: 1px solid #1f2937;
      padding: 1rem;
      font-size: 0.95rem;
    }

    .feature h3 {
      font-size: 1.05rem;
      margin-bottom: 0.45rem;
      color: #e5e7eb;
    }

    footer {
      margin-top: 3rem;
      padding-top: 1.5rem;
      border-top: 1px solid #1f2937;
      font-size: 0.8rem;
      color: #9ca3af;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      gap: 0.75rem;
      align-items: center;
    }

    .money-box {
      padding: 0.9rem;
      border-radius: 0.95rem;
      border: 1px dashed #22c55e88;
      background: rgba(6, 78, 59, 0.9);
      font-size: 0.9rem;
      color: #bbf7d0;
      margin-top: 0.9rem;
    }

    .tip-btn {
      display: inline-block;
      margin-top: 0.55rem;
      border-radius: 999px;
      padding: 0.45rem 1rem;
      border: 1px solid #22c55e;
      background: #022c22;
      color: #bbf7d0;
      font-size: 0.85rem;
      cursor: pointer;
      text-decoration: none;
    }

    .tip-btn:hover {
      background: #065f46;
    }

    .recommended {
      background: rgba(15, 23, 42, 0.95);
      border: 1px solid #1f2937;
      border-radius: 12px;
      padding: 18px;
      margin-top: 24px;
      font-size: 0.95rem;
    }

    .recommended h2 {
      margin-bottom: 8px;
      font-size: 1.35rem;
    }

    .recommended ul {
      list-style: none;
      padding-left: 0;
      margin-bottom: 8px;
    }

    .recommended li {
      margin: 6px 0;
    }

    .recommended a {
      text-decoration: none;
      color: #38bdf8;
      font-weight: 500;
    }

    .recommended a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <div class="page">
    <header>
      <div class="logo">JobFinder<span>AI</span></div>
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
            JobFinder turns your skills and availability into clear CV summaries you can copy into your applications.
            Just choose a role, add your skills, and click “Generate”.
          </p>
          <button class="btn btn-primary" id="scrollToForm">Try the demo</button>
          <p class="meta">Free to use · Works best for first jobs and remote roles.</p>

          <div class="money-box">
            <strong>💸 Support JobFinder & keep it free:</strong><br />
            – Use the job boards and tools below when they’re helpful<br />
            – Share this site with friends who are job hunting
            <br />
            <a class="tip-btn"
               href="https://ko-fi.com/Nathan10s"
               target="_blank"
               rel="noopener">
              Tip the creator on Ko-fi
            </a>
          </div>
        </div>

        <div class="card" id="formCard">
          <h2 style="font-size:1.1rem; margin-bottom:0.6rem;">Quick demo</h2>
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

            <button type="submit" class="btn btn-primary" style="width:100%; margin-top:0.4rem;">
              Generate sample CV text
            </button>
          </form>

          <div id="output" class="output">
            Fill the form and click the button to see sample CV text.
          </div>
        </div>
      </section>

      <section class="section">
        <h2>How to use JobFinder</h2>
        <div class="feature">
          <p>Getting started is simple:</p>
          <ol style="margin-top:8px; padding-left:18px;">
            <li>Choose your target role from the dropdown.</li>
            <li>Add your skills, availability, and any experience or courses you’ve done.</li>
            <li>Click “Generate sample CV text” to get a starting point for your CV.</li>
            <li>Copy the parts you like into your CV and adjust them for each job.</li>
          </ol>
          <p style="margin-top:8px;">
            This tool is designed for beginners and people who want to apply for remote or flexible work
            without needing lots of experience.
          </p>
        </div>
      </section>

      <section class="recommended">
        <h2>Where to find remote & entry-level jobs</h2>
        <p>These job boards are a good place to start:</p>
        <ul>
          <li><a href="https://www.indeed.co.uk" target="_blank" rel="noopener">Indeed</a> – filter by “remote” and “entry level”.</li>
          <li><a href="https://www.reed.co.uk" target="_blank" rel="noopener">Reed</a> – lots of UK roles, including part-time and remote.</li>
          <li><a href="https://www.totaljobs.com" target="_blank" rel="noopener">Totaljobs</a> – good for admin, customer service, and office roles.</li>
          <li><a href="https://www.linkedin.com/jobs" target="_blank" rel="noopener">LinkedIn Jobs</a> – useful for following companies and saving roles.</li>
        </ul>
      </section>

      <section class="section">
        <h2>About JobFinder</h2>
        <div class="feature">
          <p>
            JobFinder is a small, focused tool to help people who are just getting started with remote work,
            part-time jobs, or their first office-style role. The goal is to make writing CVs and cover letters less stressful,
            especially if you don’t have much experience yet.
          </p>
          <p style="margin-top:8px;">
            If this site helps you get closer to a job, you can support it using the Ko-fi button above.
          </p>
        </div>
      </section>
    </main>

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

    document.getElementById('scrollToForm').addEventListener('click', () => {
      document.getElementById('formCard').scrollIntoView({ behavior: 'smooth' });
    });
  </script>

  <!-- Counter.dev analytics -->
  <script src="https://cdn.counter.dev/script.js"
          data-id="e1251182-0cdb-4b37-b4a6-6f3fb7d76485"
          data-utcoffset="0"></script>
</body>
</html>
