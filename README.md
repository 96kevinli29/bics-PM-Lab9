<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Lab 9 – The “Future-Self” Career Project | Introduction to Project Management</title>

  <!-- Styles & Icons -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/js/all.min.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Playfair+Display:wght@600&display=swap" rel="stylesheet" />

  <style>
    :root {
      --primary: #020617;
      --accent: #6366f1;
      --accent-soft: #e0e7ff;
      --accent-dark: #4f46e5;
      --surface: #f8fafc;
      --surface-alt: #f1f5f9;
      --text: #020617;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: radial-gradient(circle at top left, #e0f2fe 0, #f8fafc 40%, #e5e7eb 100%);
      color: var(--text);
      -webkit-font-smoothing: antialiased;
      font-size: 15px;
    }

    .serif {
      font-family: 'Playfair Display', serif;
    }

    /* TOC */
    .toc-fixed {
      position: fixed;
      top: 0;
      left: 0;
      width: 270px;
      height: 100vh;
      background: linear-gradient(to bottom, #020617, #0b1120);
      color: #e2e8f0;
      padding: 1.75rem 1.4rem;
      overflow-y: auto;
      z-index: 50;
      border-right: 1px solid rgba(148, 163, 184, 0.2);
    }

    .toc-title {
      letter-spacing: .08em;
    }

    .toc-link {
      display: flex;
      align-items: center;
      gap: .45rem;
      padding: .4rem 0;
      font-size: .85rem;
      color: #cbd5e1;
      border-bottom: 1px solid rgba(51, 65, 85, 0.9);
      transition: .15s ease;
    }

    .toc-link span.step {
      font-size: .7rem;
      opacity: .8;
      min-width: 2rem;
    }

    .toc-link:hover {
      color: #fff;
      padding-left: .4rem;
    }

    .toc-link.active {
      color: #fff;
      font-weight: 600;
      border-left: 3px solid var(--accent);
      padding-left: .5rem;
      background: linear-gradient(to right, rgba(99, 102, 241, 0.16), transparent);
    }

    .main-content {
      margin-left: 270px;
      min-height: 100vh;
    }

    .hero-gradient {
      background: radial-gradient(circle at top, #e0e7ff 0, #eef2ff 35%, #f8fafc 100%);
      border-bottom: 1px solid #e2e8f0;
    }

    .card {
      background: #ffffff;
      border-radius: 1rem;
      box-shadow: 0 18px 45px rgba(15, 23, 42, 0.12);
      border: 1px solid #e5e7eb;
    }

    .card-soft {
      background: #f9fafb;
      border-radius: 1rem;
      border: 1px solid #e5e7eb;
    }

    .pill {
      display: inline-flex;
      align-items: center;
      gap: .45rem;
      border-radius: 999px;
      padding: .25rem .85rem;
      font-size: .72rem;
      font-weight: 600;
    }

    .pill-dark {
      background: rgba(15, 23, 42, 0.9);
      color: #e5e7eb;
    }

    .pill-soft {
      background: #e0e7ff;
      color: #3730a3;
    }

    .btn-primary {
      background: var(--accent);
      color: #fff;
      padding: .65rem 1.3rem;
      border-radius: .75rem;
      font-weight: 600;
      display: inline-flex;
      align-items: center;
      gap: .4rem;
      font-size: .85rem;
      box-shadow: 0 12px 30px rgba(79, 70, 229, 0.4);
      transition: background .2s ease, transform .15s ease, box-shadow .15s ease;
    }

    .btn-primary:hover {
      background: var(--accent-dark);
      transform: translateY(-1px);
      box-shadow: 0 18px 40px rgba(79, 70, 229, 0.55);
    }

    .step-badge {
      font-size: .75rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: .15em;
      color: #4f46e5;
    }

    .section-title {
      letter-spacing: .04em;
    }

    .focus-highlight {
      border-radius: 1.25rem;
      border: 1px solid rgba(79, 70, 229, 0.2);
      background: linear-gradient(135deg, rgba(129, 140, 248, 0.12), rgba(219, 234, 254, 0.5));
    }

    @media (max-width: 1024px) {
      .toc-fixed {
        transform: translateX(-100%);
        transition: transform .3s ease;
      }

      .toc-fixed.open {
        transform: translateX(0);
      }

      .main-content {
        margin-left: 0;
      }
    }
  </style>

  <base target="_blank">
</head>

<body class="text-slate-800">
  <!-- Mobile TOC toggle -->
  <button id="menuToggle" class="fixed top-4 left-4 z-50 bg-white p-2.5 rounded-full shadow-lg border border-slate-200 md:hidden">
    <i class="fas fa-bars text-slate-700 text-sm"></i>
  </button>

  <!-- TOC -->
  <nav class="toc-fixed" id="toc">
    <h3 class="toc-title text-xs font-semibold text-slate-400 uppercase mb-2">Lab 9</h3>
    <h2 class="text-base font-semibold text-slate-50 mb-4 leading-snug">
      The “Future-Self”<br />Career Project
    </h2>
    <div class="space-y-1 mt-4">
      <a class="toc-link" href="#intro">
        <span class="step">0.</span><span>Mission Briefing</span>
      </a>
      <a class="toc-link" href="#team">
        <span class="step">1.</span><span>Course Team</span>
      </a>
      <a class="toc-link" href="#objectives">
        <span class="step">2.</span><span>Learning Objectives</span>
      </a>
      <a class="toc-link" href="#tracks">
        <span class="step">3.</span><span>Choose Tech Track</span>
      </a>
      <a class="toc-link" href="#targets">
        <span class="step">4.</span><span>Pick Career Target</span>
      </a>
      <a class="toc-link" href="#plan">
        <span class="step">5.</span><span>2-Year Strategy</span>
      </a>
      <a class="toc-link" href="#deliverables">
        <span class="step">6.</span><span>Deliverables</span>
      </a>
      <a class="toc-link" href="#checklist">
        <span class="step">7.</span><span>LaTeX Checklist</span>
      </a>
      <a class="toc-link" href="#rubric">
        <span class="step">8.</span><span>Grading Rubric</span>
      </a>
      <a class="toc-link" href="#submission">
        <span class="step">9.</span><span>Submission</span>
      </a>
      <a class="toc-link" href="#value">
        <span class="step">10.</span><span>Why This Matters</span>
      </a>
    </div>
  </nav>

  <!-- MAIN CONTENT -->
  <main class="main-content">

    <!-- 0. MISSION BRIEFING -->
    <section class="hero-gradient" id="intro">
      <div class="max-w-6xl mx-auto px-6 lg:px-10 py-16 lg:py-20">
        <div class="grid lg:grid-cols-2 gap-10 items-center">
          <div>
            <div class="flex flex-wrap gap-2 mb-4 text-[11px]">
              <span class="pill pill-dark"><i class="fa-solid fa-diagram-project"></i> Introduction to Project Management</span>
              <span class="pill pill-dark"><i class="fa-solid fa-microchip"></i> Bachelor in Computer Science</span>
              <span class="pill pill-dark"><i class="fa-solid fa-building-columns"></i> FSTM · Uni. Luxembourg</span>
              <span class="pill pill-dark"><i class="fa-solid fa-calendar"></i> 2025–2026</span>
            </div>
            <h1 class="serif text-3xl md:text-4xl xl:text-5xl font-extrabold text-slate-900 leading-tight mb-3 tracking-tight">
              Lab 9: The “Future-Self” Career Project
            </h1>
            <p class="text-[15px] md:text-base text-slate-700 leading-relaxed mb-3">
              This is not a typical coding lab. In Lab 9, you are the <span class="font-semibold">project manager of your own career</span>
              for the next two years.
            </p>
            <p class="text-[14px] md:text-[15px] text-slate-700 leading-relaxed mb-4">
              Imagine yourself in the second half of your 3<sup>rd</sup> year, applying for a high-impact opportunity in AI:
              founding a startup, joining a top research lab, or interning at a world-class tech company. Your task now is to design
              the path from today to that moment.
            </p>
            <div class="flex flex-wrap gap-4 text-[13px] text-slate-600 mb-5">
              <span class="pill pill-soft"><i class="fas fa-clock text-[11px]"></i> Estimated time: 6–8 hours</span>
              <span class="pill pill-soft"><i class="fas fa-users text-[11px]"></i> Year 1 · BICS</span>
              <span class="pill pill-soft"><i class="fas fa-star text-[11px]"></i> 100 points</span>
            </div>
          </div>

          <div class="card p-6 md:p-7 lg:p-8 focus-highlight">
            <p class="step-badge mb-3">Mission Briefing</p>
            <p class="text-sm md:text-[15px] text-slate-800 leading-relaxed mb-3">
              You are no longer just a first-year student. You are a <strong>future version of yourself</strong>,
              looking back from the second half of your 3<sup>rd</sup> year.
            </p>
            <p class="text-sm md:text-[15px] text-slate-800 leading-relaxed mb-3">
              Your job in this lab is to:
            </p>
            <ul class="list-disc list-inside text-sm md:text-[15px] text-slate-800 space-y-1 mb-3">
              <li>Choose a <strong>technical track</strong> in Computer Science that excites you.</li>
              <li>Choose a <strong>career target</strong> (startup · research · industry).</li>
              <li>Design a <strong>2-year strategic plan</strong> that makes this target realistic.</li>
              <li>Write the <strong>future resume</strong> that you will send in your 3<sup>rd</sup> year.</li>
            </ul>
            <p class="text-[13px] text-slate-600">
              Treat this as your first real strategic project. The sponsor is your future self.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- 1. COURSE TEAM -->
    <section class="py-14 bg-white" id="team">
      <div class="max-w-6xl mx-auto px-6 lg:px-10">
        <div class="flex items-baseline justify-between gap-4 mb-6">
          <div>
            <div class="step-badge mb-1">1. Course Team</div>
            <h2 class="section-title serif text-2xl md:text-3xl font-bold text-slate-900">Who Runs This Lab?</h2>
          </div>
        </div>
        <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-5 text-sm">
          <div class="card-soft p-4 text-center">
            <div class="text-indigo-600 text-xl mb-1.5">
              <i class="fa-solid fa-user-tie"></i>
            </div>
            <h3 class="font-semibold text-slate-900 text-sm">Hongyang Li</h3>
            <p class="text-xs text-slate-500 mb-2">Lab 9 Coordinator</p>
            <a class="btn-primary text-[11px] justify-center" href="mailto:hongyang.li@uni.lu">
              <i class="fas fa-envelope text-[10px]"></i> Contact
            </a>
          </div>
          <div class="card-soft p-4 text-center">
            <div class="text-indigo-600 text-xl mb-1.5">
              <i class="fa-solid fa-user-graduate"></i>
            </div>
            <h3 class="font-semibold text-slate-900 text-sm">Daria Antropova</h3>
            <p class="text-xs text-slate-500 mb-2">Teaching Assistant</p>
            <a class="btn-primary text-[11px] justify-center" href="mailto:daria.antropova@ext.uni.lu">
              <i class="fas fa-envelope text-[10px]"></i> Contact
            </a>
          </div>
          <div class="card-soft p-4 text-center">
            <div class="text-indigo-600 text-xl mb-1.5">
              <i class="fa-solid fa-chalkboard-teacher"></i>
            </div>
            <h3 class="font-semibold text-slate-900 text-sm">Caesar Wu</h3>
            <p class="text-xs text-slate-500 mb-2">Teaching Assistant</p>
            <a class="btn-primary text-[11px] justify-center" href="mailto:caesar.wu@uni.lu">
              <i class="fas fa-envelope text-[10px]"></i> Contact
            </a>
          </div>
          <div class="card-soft p-4 text-center">
            <div class="text-indigo-600 text-xl mb-1.5">
              <i class="fa-solid fa-user-graduate"></i>
            </div>
            <h3 class="font-semibold text-slate-900 text-sm">Jingjing Xu</h3>
            <p class="text-xs text-slate-500 mb-2">Teaching Assistant</p>
            <a class="btn-primary text-[11px] justify-center" href="mailto:jingjing.xu@uni.lu">
              <i class="fas fa-envelope text-[10px]"></i> Contact
            </a>
          </div>
        </div>
      </div>
    </section>

    <!-- 2. LEARNING OBJECTIVES -->
    <section class="py-14 bg-slate-50" id="objectives">
      <div class="max-w-6xl mx-auto px-6 lg:px-10">
        <div class="flex items-baseline justify-between gap-4 mb-6">
          <div>
            <div class="step-badge mb-1">2. Learning Objectives</div>
            <h2 class="section-title serif text-2xl md:text-3xl font-bold text-slate-900">
              What You Will Learn
            </h2>
          </div>
        </div>
        <div class="grid md:grid-cols-3 gap-6 text-sm md:text-[15px]">
          <div class="card p-5">
            <h3 class="font-semibold text-slate-900 mb-2">Project Management</h3>
            <ul class="list-disc list-inside space-y-1 text-slate-700">
              <li>Apply project management thinking to your own career.</li>
              <li>Define scope, milestones, and risks for a 2-year plan.</li>
              <li>Connect day-to-day learning with long-term goals.</li>
            </ul>
          </div>
          <div class="card p-5">
            <h3 class="font-semibold text-slate-900 mb-2">Career Design</h3>
            <ul class="list-disc list-inside space-y-1 text-slate-700">
              <li>Analyse AI-related career paths.</li>
              <li>Choose a realistic but ambitious future target.</li>
              <li>Translate that target into courses, skills, and projects.</li>
            </ul>
          </div>
          <div class="card p-5">
            <h3 class="font-semibold text-slate-900 mb-2">LaTeX & Communication</h3>
            <ul class="list-disc list-inside space-y-1 text-slate-700">
              <li>Typeset a professional planning document in LaTeX.</li>
              <li>Create a future resume with a LaTeX CV template.</li>
              <li>Communicate your plan clearly to future supervisors or recruiters.</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- 3. CHOOSE TECH TRACK (INTEREST – SUPER HIGHLIGHT) -->
    <section class="py-16 bg-white" id="tracks">
      <div class="max-w-6xl mx-auto px-6 lg:px-10">
        <div class="focus-highlight p-6 md:p-8 mb-6">
          <p class="step-badge mb-1">Step 1 · Your Interest</p>
          <h2 class="section-title serif text-2xl md:text-3xl font-bold text-slate-900 mb-2">
            Choose Your AI/CS Track
          </h2>
          <p class="text-sm md:text-[15px] text-slate-700 max-w-3xl">
            This is the <strong>most important decision</strong> in the lab. Before thinking about companies or CVs,
            choose a direction in Computer Science that you are genuinely curious about.
          </p>
        </div>

        <div class="grid md:grid-cols-2 gap-6 text-sm md:text-[15px]">
          <div class="card p-6 border-l-4 border-indigo-500">
            <h3 class="font-semibold text-indigo-700 mb-2 flex items-center gap-2">
              <i class="fa-solid fa-brain"></i> Suggested Tracks
            </h3>
            <ul class="list-disc list-inside space-y-1 text-slate-700">
              <li>Large Language Models & AI Applications</li>
              <li>Autonomous Driving & Perception</li>
              <li>AI for Medical Diagnosis</li>
              <li>Robotics & Human–Robot Interaction</li>
              <li>Another frontier you define (explain in your plan)</li>
            </ul>
          </div>
          <div class="card p-6 bg-slate-50">
            <h3 class="font-semibold text-slate-900 mb-2 flex items-center gap-2">
              <i class="fa-solid fa-lightbulb"></i> Reflection Questions
            </h3>
            <ul class="list-disc list-inside space-y-1 text-slate-700">
              <li>Which kinds of problems do you enjoy thinking about?</li>
              <li>Do you prefer building products, systems, or theories?</li>
              <li>Which upcoming courses in the curriculum connect to this track?</li>
              <li>What sort of portfolio (projects, repos, demos) would impress yourself in 3 years?</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- 4. SET CAREER TARGET (GOAL – SUPER HIGHLIGHT) -->
    <section class="py-16 bg-slate-50" id="targets">
      <div class="max-w-6xl mx-auto px-6 lg:px-10">
        <div class="focus-highlight p-6 md:p-8 mb-6">
          <p class="step-badge mb-1">Step 2 · Your Target</p>
          <h2 class="section-title serif text-2xl md:text-3xl font-bold text-slate-900 mb-2">
            Decide Where You Want to Be in 2 Years
          </h2>
          <p class="text-sm md:text-[15px] text-slate-700 max-w-3xl">
            Now combine your <strong>interest (track)</strong> with a concrete <strong>career target</strong> for the
            second half of your 3<sup>rd</sup> year. Your entire 2-year plan will work backwards from this point.
          </p>
        </div>

        <div class="grid md:grid-cols-3 gap-6 text-sm md:text-[15px]">
          <div class="card p-6">
            <h3 class="font-semibold text-indigo-700 mb-1 flex items-center gap-2">
              <i class="fa-solid fa-rocket"></i> Path 1 · Startup Founder
            </h3>
            <p class="mb-1"><strong>Goal:</strong> After graduation, start an AI-tech company.</p>
            <p class="text-xs text-slate-600">
              Think of lean versions of companies building foundation models, code assistants, or vertical AI products.
            </p>
          </div>
          <div class="card p-6">
            <h3 class="font-semibold text-indigo-700 mb-1 flex items-center gap-2">
              <i class="fa-solid fa-flask"></i> Path 2 · Researcher
            </h3>
            <p class="mb-1"><strong>Goal:</strong> In 3rd year, join a top lab as a research intern (e.g. Stanford, MIT, CMU).</p>
            <p class="text-xs text-slate-600">
              Aimed at future MSc or direct PhD in AI/ML or related fields.
            </p>
          </div>
          <div class="card p-6">
            <h3 class="font-semibold text-indigo-700 mb-1 flex items-center gap-2">
              <i class="fa-solid fa-building"></i> Path 3 · Industry Engineer
            </h3>
            <p class="mb-1"><strong>Goal:</strong> Secure a high-quality internship at a leading tech company.</p>
            <p class="text-xs text-slate-600">
              Examples: NVIDIA, Google, Mistral, DeepSeek, or other strong players in your chosen track.
            </p>
          </div>
        </div>

        <p class="text-xs text-slate-600 mt-4">
          <strong>Important:</strong> In your plan, clearly state your chosen track + chosen path. That pair defines the scope of your project.
        </p>
      </div>
    </section>

    <!-- 5. 2-YEAR STRATEGIC PLAN -->
    <section class="py-16 bg-white" id="plan">
      <div class="max-w-6xl mx-auto px-6 lg:px-10">
        <div class="flex items-baseline justify-between gap-4 mb-6">
          <div>
            <div class="step-badge mb-1">Step 3 · 2-Year Strategy</div>
            <h2 class="section-title serif text-2xl md:text-3xl font-bold text-slate-900">
              Design Your 2-Year Career Project Plan
            </h2>
          </div>
        </div>
        <p class="text-sm md:text-[15px] text-slate-700 mb-5">
          You will now treat your career as a project that runs from today until the second half of your 3<sup>rd</sup> year
          (~2–2.5 years). Your strategic plan should be structured and realistic, but also ambitious.
        </p>

        <div class="grid md:grid-cols-2 gap-6 text-sm md:text-[15px] mb-6">
          <div class="card p-6">
            <h3 class="font-semibold text-indigo-700 mb-2">Required Components</h3>
            <ul class="list-disc list-inside space-y-1 text-slate-700">
              <li><strong>Course strategy:</strong> For each semester, list core modules and target grades.</li>
              <li><strong>Skill roadmap:</strong> Programming languages, frameworks, tools – with a rough order and timing.</li>
              <li><strong>Project pipeline:</strong> Course projects, personal projects, and/or open-source contributions tied to your track.</li>
              <li><strong>Portfolio plan:</strong> What will you show on a CV/GitHub page at the end of 2 years?</li>
            </ul>
          </div>
          <div class="card p-6">
            <h3 class="font-semibold text-indigo-700 mb-2">Project Management Elements</h3>
            <ul class="list-disc list-inside space-y-1 text-slate-700">
              <li><strong>Timeline & milestones:</strong> Key checkpoints (first serious project, first paper submission, first internship application, etc.).</li>
              <li><strong>Resources & stakeholders:</strong> People, communities, teachers, labs, events that can help.</li>
              <li><strong>Risk & mitigation:</strong> What might go wrong? What is Plan B?</li>
              <li><strong>Success criteria:</strong> How will you know your plan is working?</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- 6. DELIVERABLES -->
    <section class="py-16 bg-slate-50" id="deliverables">
      <div class="max-w-6xl mx-auto px-6 lg:px-10">
        <div class="flex items-baseline justify-between gap-4 mb-6">
          <div>
            <div class="step-badge mb-1">6. Deliverables (LaTeX)</div>
            <h2 class="section-title serif text-2xl md:text-3xl font-bold text-slate-900">
              What You Will Submit
            </h2>
          </div>
        </div>
        <div class="grid md:grid-cols-2 gap-6 text-sm md:text-[15px]">
          <div class="card p-6">
            <h3 class="font-semibold text-indigo-700 mb-2">6.1 Strategic Planning Document</h3>
            <p class="mb-2">A detailed, LaTeX-typeset 2-year career development plan.</p>
            <ul class="list-disc list-inside space-y-1 text-slate-700">
              <li><strong>Length:</strong> ~8–12 pages.</li>
              <li>Includes track, career target, and complete 2-year roadmap.</li>
              <li>Uses the language of project management (scope, timeline, risks, milestones).</li>
              <li>Written as a professional document you could show to a mentor or supervisor.</li>
            </ul>
          </div>
          <div class="card p-6">
            <h3 class="font-semibold text-indigo-700 mb-2">6.2 Future Resume</h3>
            <p class="mb-2">
              A 2-page resume for your future self in the second half of 3<sup>rd</sup> year.
            </p>
            <ul class="list-disc list-inside space-y-1 text-slate-700">
              <li>Tailored to your chosen target (startup founder / research intern / industry intern).</li>
              <li>Includes the projects, skills, and experiences predicted in your strategic plan.</li>
              <li>Uses a LaTeX CV template (e.g. <em>moderncv</em> or similar) with clean layout.</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- 7. LATEX CHECKLIST -->
    <section class="py-16 bg-white" id="checklist">
      <div class="max-w-6xl mx-auto px-6 lg:px-10">
        <div class="flex items-baseline justify-between gap-4 mb-6">
          <div>
            <div class="step-badge mb-1">7. LaTeX Skills Checklist</div>
            <h2 class="section-title serif text-2xl md:text-3xl font-bold text-slate-900">
              What We Expect to See in Your LaTeX
            </h2>
          </div>
        </div>
        <div class="card p-6 text-sm md:text-[15px]">
          <ul class="list-disc list-inside space-y-1 text-slate-800">
            <li>Appropriate document classes:
              <code>\documentclass{article}</code> (or similar) for the plan, and a CV class (e.g. <code>moderncv</code>) for the resume.
            </li>
            <li>Structured sections using <code>\section{}</code> and <code>\subsection{}</code> with meaningful titles.</li>
            <li>Text emphasis with <code>\textbf{}</code>, <code>\textit{}</code>, and <code>\texttt{}</code> (for commands or code).</li>
            <li>Use of <code>itemize</code> and <code>enumerate</code> for lists and steps.</li>
            <li>At least one clear table using <code>tabular</code> (e.g. semester plan, skills vs. level, milestones).</li>
            <li>Hyperlinks created with <code>\href{...}{...}</code> (GitHub, LinkedIn, course pages, etc.).</li>
            <li>Consistent margins and layout, ideally using the <code>geometry</code> package.</li>
            <li>Clean typography: no random spacing, consistent font sizes, nice page breaks.</li>
            <li>Reasonable file structure in Overleaf (plan and resume can be separate projects or separate .tex files).</li>
            <li>No major compilation errors; warnings kept under control.</li>
            <li><em>Optional bonus:</em> use of additional packages such as <code>biblatex</code> for references or a timeline diagram.</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- 8. RUBRIC -->
    <section class="py-16 bg-slate-50" id="rubric">
      <div class="max-w-6xl mx-auto px-6 lg:px-10">
        <div class="flex items-baseline justify-between gap-4 mb-6">
          <div>
            <div class="step-badge mb-1">8. Grading Rubric</div>
            <h2 class="section-title serif text-2xl md:text-3xl font-bold text-slate-900">
              How This Lab Will Be Graded (100 pts)
            </h2>
          </div>
        </div>
        <div class="overflow-x-auto card p-4">
          <table class="rubric-table w-full">
            <thead>
              <tr>
                <th class="w-2/5 text-left">Category</th>
                <th class="w-2/5 text-left">Criteria</th>
                <th class="w-1/5 text-center">Points</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td><strong>Strategic Plan Content</strong></td>
                <td>Clear, coherent 2-year roadmap; includes courses, skills, projects, networking, milestones.</td>
                <td class="text-center">/35</td>
              </tr>
              <tr>
                <td><strong>Future Resume</strong></td>
                <td>Consistent with plan; tailored to chosen target; strong bullet points; plausible and ambitious.</td>
                <td class="text-center">/25</td>
              </tr>
              <tr>
                <td><strong>LaTeX Proficiency</strong></td>
                <td>Uses structure, lists, tables, formatting, and hyperlinks; compiles cleanly; professional layout.</td>
                <td class="text-center">/25</td>
              </tr>
              <tr>
                <td><strong>Project Management Thinking</strong></td>
                <td>Shows awareness of timeline, risks, and dependencies; clear link to the 3rd-year target.</td>
                <td class="text-center">/15</td>
              </tr>
              <tr>
                <td colspan="2" class="text-right font-semibold">Total</td>
                <td class="text-center font-semibold">/100</td>
              </tr>
            </tbody>
          </table>
        </div>
        <p class="mt-3 text-xs text-slate-500">
          The final rubric details may be adjusted by the teaching team on Moodle.
        </p>
      </div>
    </section>

    <!-- 9. SUBMISSION -->
    <section class="py-16 bg-white" id="submission">
      <div class="max-w-6xl mx-auto px-6 lg:px-10">
        <div class="flex items-baseline justify-between gap-4 mb-6">
          <div>
            <div class="step-badge mb-1">9. Submission</div>
            <h2 class="section-title serif text-2xl md:text-3xl font-bold text-slate-900">
              How to Hand In Your Work
            </h2>
          </div>
        </div>
        <div class="card p-6 text-sm md:text-[15px] space-y-3">
          <p>Submit a single <code>.zip</code> file named:</p>
          <p class="font-mono text-xs bg-slate-900 text-slate-100 inline-block px-3 py-1 rounded">
            [YourStudentID]_Lab9_FutureSelf.zip
          </p>
          <p class="font-semibold mt-1.5">The ZIP must contain at least:</p>
          <ul class="list-disc list-inside space-y-1 text-slate-700">
            <li><code>plan.tex</code> and <code>plan.pdf</code> – your 2-year strategic planning document.</li>
            <li><code>resume_future.tex</code> and <code>resume_future.pdf</code> – your future 3rd-year resume.</li>
          </ul>
          <p class="text-slate-600 text-[13px]">
            Upload the ZIP to the Lab 9 activity on Moodle before the deadline. Both PDFs must compile correctly from the submitted source.
          </p>
        </div>
      </div>
    </section>

    <!-- 10. WHY THIS MATTERS -->
    <section class="py-16 bg-slate-900" id="value">
      <div class="max-w-6xl mx-auto px-6 lg:px-10 text-slate-100">
        <h2 class="section-title serif text-2xl md:text-3xl font-bold mb-3">
          10. Why This Project Matters
        </h2>
        <p class="text-sm md:text-[15px] mb-3 text-slate-200">
          Lab 9 turns <strong>Introduction to Project Management</strong> into something personal and concrete:
          you apply project management not to a fictional company, but to your own career.
        </p>
        <ul class="list-disc list-inside text-sm md:text-[15px] space-y-1 text-slate-200">
          <li>You leave the course with a realistic, actionable 2-year plan.</li>
          <li>You have a “future resume” that you can slowly turn into reality.</li>
          <li>You see how courses, skills, and projects fit together as a project, not just as a checklist.</li>
        </ul>
        <p class="mt-4 text-sm md:text-[15px] text-indigo-100 font-medium">
          If you do this well, Lab 9 will not just give you points — it will give you a roadmap that makes your future internship,
          research position, or startup much more likely.
        </p>
      </div>
    </section>

    <!-- FOOTER -->
    <footer class="bg-slate-950 text-slate-400 text-center text-[11px] py-5">
      <p>Introduction to Project Management · Bachelor in Computer Science · Faculty of Science, Technology and Medicine</p>
      <p>University of Luxembourg · Academic Year 2025–2026</p>
    </footer>

  </main>

  <!-- JS: TOC scroll & highlight & mobile toggle -->
  <script>
    // Smooth scroll
    document.querySelectorAll('.toc-link').forEach(link => {
      link.addEventListener('click', e => {
        e.preventDefault();
        const id = link.getAttribute('href').slice(1);
        const target = document.getElementById(id);
        if (target) {
          target.scrollIntoView({ behavior: 'smooth', block: 'start' });
        }
        document.getElementById('toc').classList.remove('open');
      });
    });

    // TOC active state
    const sections = document.querySelectorAll('section[id]');
    const tocLinks = document.querySelectorAll('.toc-link');
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          tocLinks.forEach(l => l.classList.remove('active'));
          const active = document.querySelector(`.toc-link[href="#${entry.target.id}"]`);
          if (active) active.classList.add('active');
        }
      });
    }, { rootMargin: '-30% 0px -70% 0px' });
    sections.forEach(sec => observer.observe(sec));

    // Mobile TOC toggle
    const menuBtn = document.getElementById('menuToggle');
    const toc = document.getElementById('toc');
    menuBtn.addEventListener('click', () => {
      toc.classList.toggle('open');
    });
  </script>
</body>

</html>
