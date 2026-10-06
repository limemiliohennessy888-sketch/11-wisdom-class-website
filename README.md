<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>11 WISDOM</title>
    <style>
      :root {
        --navy: #0d1b3d;
        --gold: #d9b75f;
        --cream: #f8f5ef;
        --white: #ffffff;
        --text: #1d2435;
        --muted: #5b6474;
        --shadow: 0 10px 30px rgba(13, 27, 61, 0.12);
      }

      * {
        box-sizing: border-box;
      }

      html {
        scroll-behavior: smooth;
      }

      body {
        margin: 0;
        font-family: Arial, Helvetica, sans-serif;
        background: linear-gradient(to bottom, #f5f2ea 0%, #ffffff 100%);
        color: var(--text);
      }

      a {
        text-decoration: none;
        color: inherit;
      }

      .topbar {
        background: var(--navy);
        color: var(--white);
        position: sticky;
        top: 0;
        z-index: 1000;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
      }

      .container {
        width: min(1200px, calc(100% - 32px));
        margin: 0 auto;
      }

      .nav-wrap {
        display: flex;
        align-items: center;
        justify-content: space-between;
        min-height: 72px;
        gap: 20px;
      }

      .brand {
        font-size: 2rem;
        font-weight: 700;
        letter-spacing: 1px;
        color: var(--gold);
      }

      .nav-links {
        display: flex;
        flex-wrap: wrap;
        justify-content: flex-end;
        gap: 18px;
      }

      .nav-links a {
        color: var(--white);
        font-weight: 600;
        padding: 10px 12px;
        border-radius: 8px;
        transition: 0.2s ease;
      }

      .nav-links a:hover {
        background: rgba(217, 183, 95, 0.15);
        color: var(--gold);
      }

      .hero {
        padding: 80px 0 60px;
        background: linear-gradient(135deg, rgba(13, 27, 61, 0.96), rgba(31, 48, 90, 0.9)),
          url("https://images.unsplash.com/photo-1522202176988-66273c2fd55f?auto=format&fit=crop&w=1600&q=80") center/cover no-repeat;
        color: var(--white);
      }

      .hero-inner {
        display: grid;
        grid-template-columns: 1.2fr 0.8fr;
        gap: 30px;
        align-items: center;
      }

      .hero h1 {
        font-size: clamp(2.5rem, 5vw, 5rem);
        margin: 0 0 18px;
        line-height: 1.05;
        letter-spacing: 1px;
      }

      .hero p {
        font-size: 1.1rem;
        line-height: 1.7;
        color: rgba(255, 255, 255, 0.85);
        max-width: 620px;
      }

      .hero-cta {
        display: flex;
        gap: 16px;
        margin-top: 28px;
        flex-wrap: wrap;
      }

      .btn {
        display: inline-block;
        padding: 14px 26px;
        border-radius: 999px;
        font-weight: 700;
        transition: 0.2s ease;
      }

      .btn-primary {
        background: var(--gold);
        color: var(--navy);
      }

      .btn-primary:hover {
        transform: translateY(-2px);
        box-shadow: var(--shadow);
      }

      .btn-secondary {
        background: transparent;
        border: 2px solid rgba(255, 255, 255, 0.6);
        color: var(--white);
      }

      .hero-card {
        background: rgba(255, 255, 255, 0.08);
        backdrop-filter: blur(10px);
        border: 1px solid rgba(255, 255, 255, 0.14);
        border-radius: 22px;
        padding: 24px;
        box-shadow: var(--shadow);
      }

      .hero-card h3 {
        margin: 0 0 18px;
        font-size: 1.4rem;
        color: var(--gold);
      }

      .mini-stat {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 14px 0;
        border-bottom: 1px solid rgba(255, 255, 255, 0.18);
      }

      .mini-stat:last-child {
        border-bottom: none;
      }

      .mini-stat span {
        color: rgba(255, 255, 255, 0.8);
      }

      .mini-stat strong {
        font-size: 1.1rem;
      }

      section {
        padding: 80px 0;
      }

      .section-title {
        text-align: center;
        margin-bottom: 34px;
      }

      .section-title h2 {
        margin: 0 0 10px;
        font-size: clamp(2rem, 3vw, 3rem);
        color: var(--navy);
      }

      .section-title p {
        margin: 0;
        color: var(--muted);
        font-size: 1.05rem;
      }

      .cards {
        display: grid;
        grid-template-columns: repeat(3, minmax(0, 1fr));
        gap: 24px;
      }

      .card {
        background: var(--white);
        border-radius: 20px;
        overflow: hidden;
        box-shadow: var(--shadow);
        border: 1px solid rgba(13, 27, 61, 0.06);
      }

      .card-image {
        height: 200px;
        background: linear-gradient(135deg, #dde6f7, #f5e9c8);
      }

      .card-content {
        padding: 24px;
      }

      .card-content h3 {
        margin: 0 0 12px;
        font-size: 1.5rem;
        color: var(--navy);
      }

      .card-content p {
        margin: 0 0 16px;
        color: var(--muted);
        line-height: 1.7;
      }

      .tag {
        display: inline-block;
        background: rgba(13, 27, 61, 0.08);
        color: var(--navy);
        font-size: 0.8rem;
        padding: 8px 12px;
        border-radius: 999px;
        font-weight: 700;
      }

      .info-grid {
        display: grid;
        grid-template-columns: repeat(2, minmax(0, 1fr));
        gap: 24px;
      }

      .info-box {
        background: var(--white);
        border-radius: 18px;
        padding: 26px;
        box-shadow: var(--shadow);
      }

      .info-box h3 {
        margin: 0 0 16px;
        color: var(--navy);
        font-size: 1.6rem;
      }

      .info-box ul {
        margin: 0;
        padding-left: 18px;
        color: var(--muted);
        line-height: 2;
      }

      .statement-box {
        background: linear-gradient(135deg, #f9f2dc, #f3f7ff);
        border-left: 6px solid var(--gold);
      }

      .directory-table-wrap {
        background: var(--white);
        border-radius: 20px;
        overflow: hidden;
        box-shadow: var(--shadow);
      }

      table {
        width: 100%;
        border-collapse: collapse;
      }

      th, td {
        padding: 18px 20px;
        text-align: left;
        border-bottom: 1px solid rgba(13, 27, 61, 0.08);
      }

      th {
        background: var(--navy);
        color: var(--white);
        font-weight: 700;
      }

      td {
        color: var(--text);
      }

      tr:last-child td {
        border-bottom: none;
      }

      .occasion-grid {
        display: grid;
        grid-template-columns: repeat(3, minmax(0, 1fr));
        gap: 24px;
      }

      .occasion-item {
        background: var(--white);
        border-radius: 20px;
        padding: 22px;
        box-shadow: var(--shadow);
        border-top: 5px solid var(--gold);
      }

      .occasion-item h3 {
        margin: 0 0 10px;
        color: var(--navy);
      }

      .occasion-item p {
        margin: 0;
        color: var(--muted);
        line-height: 1.7;
      }

      .members-grid {
        display: grid;
        grid-template-columns: repeat(4, minmax(0, 1fr));
        gap: 24px;
      }

      .member-card {
        background: var(--white);
        padding: 26px 22px;
        border-radius: 20px;
        text-align: center;
        box-shadow: var(--shadow);
      }

      .avatar {
        width: 90px;
        height: 90px;
        border-radius: 50%;
        background: linear-gradient(135deg, #d9b75f, #0d1b3d);
        color: var(--white);
        display: grid;
        place-items: center;
        font-size: 2rem;
        font-weight: 700;
        margin: 0 auto 16px;
      }

      .member-card h3 {
        margin: 0 0 8px;
        color: var(--navy);
      }

      .member-card p {
        margin: 0;
        color: var(--muted);
      }

      footer {
        background: var(--navy);
        color: var(--white);
        padding: 28px 0;
        text-align: center;
      }

      @media (max-width: 900px) {
        .hero-inner,
        .cards,
        .info-grid,
        .occasion-grid,
        .members-grid {
          grid-template-columns: 1fr;
        }

        .nav-wrap {
          flex-direction: column;
          justify-content: center;
          padding: 18px 0;
        }

        .nav-links {
          justify-content: center;
        }
      }
    </style>
  </head>
  <body>
    <header class="topbar">
      <div class="container nav-wrap">
        <div class="brand">11 WISDOM</div>
        <nav class="nav-links" aria-label="Main navigation">
          <a href="#new">What's New</a>
          <a href="#info">Information</a>
          <a href="#statements">Statements</a>
          <a href="#directory">Directory</a>
          <a href="#occasions">Occasions</a>
          <a href="#members">Members</a>
        </nav>
      </div>
    </header>

    <section class="hero">
      <div class="container hero-inner">
        <div>
          <h1>11 WISDOM</h1>
          <p>
            A bright and inspiring class community built on excellence, unity,
            and shared success. We celebrate achievement, support one another,
            and create memorable moments throughout the school year.
          </p>
          <div class="hero-cta">
            <a class="btn btn-primary" href="#members">Meet the Class</a>
            <a class="btn btn-secondary" href="#new">View Updates</a>
          </div>
        </div>

        <div class="hero-card">
          <h3>Class Highlights</h3>
          <div class="mini-stat">
            <span>Students</span>
            <strong>45</strong>
          </div>
          <div class="mini-stat">
            <span>Programs</span>
            <strong>12</strong>
          </div>
          <div class="mini-stat">
            <span>Events</span>
            <strong>8</strong>
          </div>
          <div class="mini-stat">
            <span>Achievements</span>
            <strong>24</strong>
          </div>
        </div>
      </div>
    </section>

    <section id="new">
      <div class="container">
        <div class="section-title">
          <h2>What's New</h2>
          <p>Latest updates, achievements, and class announcements</p>
        </div>

        <div class="cards">
          <article class="card">
            <div class="card-image" style="background: linear-gradient(135deg,#dfe9ff,#fff0c6);"></div>
            <div class="card-content">
              <span class="tag">Announcement</span>
              <h3>Class Assembly</h3>
              <p>
                Our next class assembly will highlight student leadership,
                classroom achievements, and upcoming event updates.
              </p>
            </div>
          </article>

          <article class="card">
            <div class="card-image" style="background: linear-gradient(135deg,#e5f7ee,#dfe9ff);"></div>
            <div class="card-content">
              <span class="tag">Achievement</span>
              <h3>Academic Excellence</h3>
              <p>
                Several students received recognition for outstanding performance,
                teamwork, and dedication this month.
              </p>
            </div>
          </article>

          <article class="card">
            <div class="card-image" style="background: linear-gradient(135deg,#fff0d9,#f0e1ff);"></div>
            <div class="card-content">
              <span class="tag">Event</span>
              <h3>Upcoming Program</h3>
              <p>
                We are preparing for an exciting activity day filled with fun,
                creativity, and class spirit.
              </p>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section id="info" style="background: #f9f7f2;">
      <div class="container">
        <div class="section-title">
          <h2>Information</h2>
          <p>Important details about our class and community</p>
        </div>

        <div class="info-grid">
          <div class="info-box">
            <h3>Class Goals</h3>
            <ul>
              <li>Encourage teamwork and mutual respect.</li>
              <li>Support academic growth and confidence.</li>
              <li>Promote creativity, discipline, and responsibility.</li>
              <li>Build a positive class culture for every learner.</li>
            </ul>
          </div>

          <div class="info-box statement-box">
            <h3>Class Values</h3>
            <ul>
              <li>Kindness and cooperation</li>
              <li>Honesty and commitment</li>
              <li>Dedication to excellence</li>
              <li>Unity in every challenge</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <section id="statements">
      <div class="container">
        <div class="section-title">
          <h2>Statements</h2>
          <p>Thoughts and commitments that guide us</p>
        </div>

        <div class="cards">
          <article class="card">
            <div class="card-content">
              <span class="tag">Mission</span>
              <h3>Our Mission</h3>
              <p>
                To inspire learning, nurture confidence, and create a joyful
                class environment where every learner can thrive.
              </p>
            </div>
          </article>

          <article class="card">
            <div class="card-content">
              <span class="tag">Vision</span>
              <h3>Our Vision</h3>
              <p>
                To become a class known for unity, excellence, and strong character,
                both in school and beyond.
              </p>
            </div>
          </article>

          <article class="card">
            <div class="card-content">
              <span class="tag">Promise</span>
              <h3>Our Promise</h3>
              <p>
                We commit to supporting each other, trying our best, and making
                every opportunity a meaningful one.
              </p>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section id="directory" style="background: #f9f7f2;">
      <div class="container">
        <div class="section-title">
          <h2>Directory</h2>
          <p>Class contact and student directory overview</p>
        </div>

        <div class="directory-table-wrap">
          <table>
            <thead>
              <tr>
                <th>Name</th>
                <th>Role</th>
                <th>Contact</th>
                <th>Status</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>Maria Lopez</td>
                <td>Class President</td>
                <td>maria@school.edu</td>
                <td>Active</td>
              </tr>
              <tr>
                <td>James Carter</td>
                <td>Vice President</td>
                <td>james@school.edu</td>
                <td>Active</td>
              </tr>
              <tr>
                <td>Anna Smith</td>
                <td>Secretary</td>
                <td>anna@school.edu</td>
                <td>Active</td>
              </tr>
              <tr>
                <td>Daniel Reed</td>
                <td>Event Coordinator</td>
                <td>daniel@school.edu</td>
                <td>Active</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </section>

    <section id="occasions">
      <div class="container">
        <div class="section-title">
          <h2>Occasions</h2>
          <p>Celebrations and memorable moments</p>
        </div>

        <div class="occasion-grid">
          <div class="occasion-item">
            <h3>Class Birthday</h3>
            <p>
              A joyful celebration that brings laughter, surprises, and a
              stronger sense of belonging.
            </p>
          </div>

          <div class="occasion-item">
            <h3>Sports Day</h3>
            <p>
              A day of courage, teamwork, and healthy competition that unites
              everyone in spirit and effort.
            </p>
          </div>

          <div class="occasion-item">
            <h3>Graduation Day</h3>
            <p>
              A proud milestone marking growth, success, and the strong
              memories built together.
            </p>
          </div>
        </div>
      </div>
    </section>

    <section id="members" style="background: #f9f7f2;">
      <div class="container">
        <div class="section-title">
          <h2>Members</h2>
          <p>Meet the people who make 11 WISDOM special</p>
        </div>

        <div class="members-grid">
          <div class="member-card">
            <div class="avatar">ML</div>
            <h3>Maria L.</h3>
            <p>Class Leader</p>
          </div>

          <div class="member-card">
            <div class="avatar">JC</div>
            <h3>James C.</h3>
            <p>Student Rep</p>
          </div>

          <div class="member-card">
            <div class="avatar">AS</div>
            <h3>Anna S.</h3>
            <p>Creative Team</p>
          </div>

          <div class="member-card">
            <div class="avatar">DR</div>
            <h3>Daniel R.</h3>
            <p>Event Manager</p>
          </div>
        </div>
      </div>
    </section>

    <footer>
      <div class="container">
        <p>© 2026 11 WISDOM • Building a brighter future together</p>
      </div>
    </footer>
  </body>
</html>
