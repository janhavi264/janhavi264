 <!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Janhavi Yadav — AI/ML & Software Developer</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg: #0f1724; /* deep navy */
      --card: #0b1220;
      --accent: linear-gradient(90deg,#6ee7b7,#60a5fa);
      --glass: rgba(255,255,255,0.04);
      color-scheme: dark;
      color: #e6eef8;
      font-family: 'Inter', system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
    }
    *{box-sizing:border-box}
    body{margin:0; background: radial-gradient(1200px 600px at 10% 10%, rgba(96,165,250,0.06), transparent), var(--bg); min-height:100vh;}
    .wrap{max-width:1100px;margin:40px auto;padding:28px;display:grid;grid-template-columns:360px 1fr;gap:24px}

    /* Left card */
    .card{background:linear-gradient(180deg, rgba(255,255,255,0.03), rgba(255,255,255,0.02));border-radius:16px;padding:22px;box-shadow:0 6px 30px rgba(2,6,23,0.6);border:1px solid rgba(255,255,255,0.03)}
    .avatar{width:120px;height:120px;border-radius:14px;overflow:hidden;background:linear-gradient(135deg,#60a5fa,#7c3aed);display:flex;align-items:center;justify-content:center;font-weight:800;font-size:40px;color:white}
    h1{margin:6px 0 2px;font-size:20px}
    p.lead{margin:0;color:rgba(230,238,248,0.78)}
    .badges{display:flex;flex-wrap:wrap;gap:8px;margin-top:14px}
    .badge{background:var(--glass);padding:6px 10px;border-radius:999px;font-size:13px;border:1px solid rgba(255,255,255,0.02)}

    /* skills */
    .skills{display:grid;grid-template-columns:repeat(2,1fr);gap:8px;margin-top:16px}
    .skill{background:linear-gradient(180deg,rgba(255,255,255,0.01),transparent);padding:10px;border-radius:10px;font-size:14px}

    /* Right area */
    .header-row{display:flex;align-items:center;justify-content:space-between;gap:12px}
    .about{margin-top:8px;color:rgba(230,238,248,0.86)}

    /* stats */
    .stats{display:flex;gap:12px;margin-top:18px}
    .stat{flex:1;background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);padding:12px;border-radius:12px;text-align:center}
    .stat h3{margin:0;font-size:18px}
    .stat p{margin:6px 0 0;font-size:20px;font-weight:700}

    /* chart */
    .panel{margin-top:18px;padding:14px;border-radius:12px;background:linear-gradient(180deg, rgba(255,255,255,0.01), transparent);}

    /* project list */
    .projects{display:grid;gap:12px;margin-top:14px}
    .project{padding:12px;border-radius:10px;border:1px solid rgba(255,255,255,0.02)}
    .project:hover{transform:translateY(-6px);transition:all 0.28s cubic-bezier(.2,.9,.2,1)}

    footer{margin-top:20px;text-align:center;color:rgba(230,238,248,0.6);font-size:13px}

    /* small screens */
    @media (max-width:880px){.wrap{grid-template-columns:1fr; padding:14px}}

    /* animated hover effect for projects */
    .project .meta{opacity:0.8}
    .project:hover .meta{opacity:1}

    .cta{display:inline-flex;gap:8px;align-items:center;padding:8px 12px;border-radius:999px;border:1px solid rgba(255,255,255,0.04);background:linear-gradient(90deg,#111827,#0b1220);cursor:pointer}
    .small{font-size:13px}

    /* little sparkle */
    .spark{display:inline-block;width:8px;height:8px;border-radius:50%;background:linear-gradient(90deg,#6ee7b7,#60a5fa);box-shadow:0 6px 16px rgba(96,165,250,0.12)}
  </style>
</head>
<body>
  <div class="wrap">
    <aside class="card">
      <div style="display:flex;gap:14px;align-items:center">
        <div class="avatar">JY</div>
        <div>
          <h1>Janhavi Yadav</h1>
          <p class="lead">B.Tech — AI &amp; ML | Java · Python · Kotlin</p>
          <div class="badges">
            <span class="badge">AI / ML</span>
            <span class="badge">Full‑Stack</span>
            <span class="badge">Android</span>
            <span class="badge">Open to Collaboration</span>
          </div>
        </div>
      </div>

      <div class="skills">
        <div class="skill">HTML · CSS · JavaScript</div>
        <div class="skill">Python · pandas · numpy</div>
        <div class="skill">matplotlib · ML</div>
        <div class="skill">Java · Kotlin</div>
        <div class="skill">Git · GitHub</div>
        <div class="skill">VS Code · Android Studio</div>
      </div>

      <div style="margin-top:16px">
        <div style="display:flex;justify-content:space-between;align-items:center">
          <div class="small">Contact</div>
          <div class="small">LinkedIn · Email</div>
        </div>
      </div>

      <div style="margin-top:16px">
        <div class="small">Fun fact</div>
        <div style="margin-top:6px;color:rgba(230,238,248,0.72)">Blends logic + creativity to make impactful projects 🚀</div>
      </div>
    </aside>

    <main>
      <div class="card">
        <div class="header-row">
          <div>
            <h2 style="margin:0">Profile & Live Stats <span class="spark"></span></h2>
            <div class="about">Passionate B.Tech student exploring Java Development, Android (Kotlin), Web Development, and Machine Learning. Focus: building scalable projects using Java, Python, and modern web technologies.</div>
          </div>
          <div style="display:flex;gap:8px;align-items:center">
            <button class="cta" id="refreshBtn">Regenerate Stats</button>
          </div>
        </div>

        <div class="stats" style="margin-top:18px">
          <div class="stat">
            <h3>GitHub Streak</h3>
            <p id="streak">0</p>
          </div>
          <div class="stat">
            <h3>Monthly Commits</h3>
            <p id="commits">0</p>
          </div>
          <div class="stat">
            <h3>Open Issues</h3>
            <p id="issues">0</p>
          </div>
        </div>

        <div class="panel">
          <canvas id="activityChart" height="120"></canvas>
        </div>

        <div class="panel" style="display:flex;gap:12px;flex-direction:column">
          <div style="display:flex;justify-content:space-between;align-items:center">
            <h3 style="margin:0">Featured Projects</h3>
            <div class="small">Tech: Java · Python · JS · Kotlin</div>
          </div>

          <div class="projects">
            <div class="project">
              <div style="display:flex;justify-content:space-between;align-items:center">
                <div>
                  <div style="font-weight:700">AI-Based Personal Diary App</div>
                  <div class="meta small">Smart journaling with sentiment analysis & topic highlights</div>
                </div>
                <div class="small">Python · NLP</div>
              </div>
            </div>

            <div class="project">
              <div style="display:flex;justify-content:space-between;align-items:center">
                <div>
                  <div style="font-weight:700">BMI Calculator</div>
                  <div class="meta small">Desktop app for tracking fitness with recommendations</div>
                </div>
                <div class="small">Python · Tkinter</div>
              </div>
            </div>

            <div class="project">
              <div style="display:flex;justify-content:space-between;align-items:center">
                <div>
                  <div style="font-weight:700">E‑Commerce Website</div>
                  <div class="meta small">Responsive shopping website with cart & checkout</div>
                </div>
                <div class="small">HTML · CSS · JS</div>
              </div>
            </div>

            <div class="project">
              <div style="display:flex;justify-content:space-between;align-items:center">
                <div>
                  <div style="font-weight:700">Chatbot Application</div>
                  <div class="meta small">AI-powered chatbot to enhance human-computer interaction</div>
                </div>
                <div class="small">Python · NLP</div>
              </div>
            </div>

          </div>
        </div>

        <footer>“Code. Create. Innovate. Repeat.”</footer>
      </div>

      <div class="card" style="margin-top:16px">
        <h3 style="margin:0">Local Python (optional)</h3>
        <p class="small">Below is a ready-to-run Python snippet that uses <code>pandas</code>, <code>numpy</code>, and <code>matplotlib</code> to generate similar "live" stats from a CSV. Run locally to produce a PNG graph you can include in this page.</p>
        <pre style="background:#071022;padding:12px;border-radius:8px;overflow:auto;color:#dbeafe;font-size:13px">
# save this as generate_stats.py
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# simulate activity (replace with your GitHub data export if available)
days = pd.date_range(end=pd.Timestamp.today(), periods=30)
commits = np.random.poisson(lam=2, size=30).cumsum()  # cumulative commits

df = pd.DataFrame({
    'date': days,
    'daily_commits': np.random.poisson(lam=2, size=30)
})

df.to_csv('activity.csv', index=False)

plt.figure(figsize=(8,3))
plt.plot(df['date'], df['daily_commits'])
plt.title('Daily Commits (30 days)')
plt.tight_layout()
plt.savefig('daily_commits.png', dpi=150)
print('Saved activity.csv and daily_commits.png')
        </pre>
        <div class="small">Tip: install dependencies with <code>pip install pandas numpy matplotlib</code></div>
      </div>

    </main>
  </div>

  <!-- Chart.js CDN -->
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <script>
    // Helper to generate pseudo-realistic stats (these vary when regenerated)
    function genStats(){
      const streak = Math.floor(Math.random()*60) + 1; // 1-60 days
      const commits = Math.floor(Math.random()*200) + 5; // monthly commits
      const issues = Math.floor(Math.random()*10); // open issues
      // generate 30-day activity
      const labels = [];
      const values = [];
      for(let i=29;i>=0;i--){
        const d = new Date(); d.setDate(d.getDate()-i);
        labels.push(d.toISOString().slice(0,10));
        values.push(Math.max(0, Math.round(Math.random()*4)));
      }
      return {streak, commits, issues, labels, values};
    }

    // Update UI and chart
    const streakEl = document.getElementById('streak');
    const commitsEl = document.getElementById('commits');
    const issuesEl = document.getElementById('issues');

    const ctx = document.getElementById('activityChart').getContext('2d');
    let chart = null;

    function render(){
      const s = genStats();
      streakEl.textContent = s.streak + ' days';
      commitsEl.textContent = s.commits;
      issuesEl.textContent = s.issues;

      if(chart) chart.destroy();

      chart = new Chart(ctx, {
        type: 'line',
        data: {
          labels: s.labels,
          datasets: [{
            label: 'Daily commits',
            data: s.values,
            fill: true,
            tension: 0.3,
            pointRadius: 2,
          }]
        },
        options: {
          plugins: {legend:{display:false}},
          scales: {
            x:{display:false},
            y:{ticks:{beginAtZero:true, precision:0}}
          }
        }
      });
    }

    // initial render
    render();

    // regenerate when button clicked
    document.getElementById('refreshBtn').addEventListener('click', ()=>{
      render();
      // small pulse animation
      const btn = document.getElementById('refreshBtn');
      btn.style.transform = 'scale(0.98)';
      setTimeout(()=> btn.style.transform = 'scale(1)', 140);
    });

    // optionally animate small updates every 12s to simulate "live" behaviour
    setInterval(()=>{
      // subtle random nudge (don't regenerate completely)
      const newVal = Math.max(0, Math.round(Math.random()*4));
      if(chart){
        chart.data.datasets[0].data.shift();
        chart.data.datasets[0].data.push(newVal);
        chart.update();
      }
      // update commit number slightly
      const currentCommits = parseInt(commitsEl.textContent) || 0;
      commitsEl.textContent = Math.max(0, currentCommits + Math.round((Math.random()-0.4)*3));
    }, 12000);
  </script>
</body>
</html>

