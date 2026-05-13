
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Areej Mehboob — NLP Researcher</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Playfair+Display:ital,wght@0,400;0,600;1,400&family=Epilogue:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg:           #b8c9ca;
            --surface:      #FFFFFF;
            --surface-2:    #aeb9c7;
            --border:       #DDD9D0;
            --border-dark:  #B8B3A8;
            --primary:      #2E4057;
            --accent:       #bf86bd;
            --accent-dim:   #E8946A;
            --green:        #3A6351;
            --text:         #1C1C1C;
            --text-mid:     #555047;
            --text-dim:     #9A9488;
            --tag-bg:       #EDE9E1;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        html { scroll-behavior: smooth; }

        body {
            font-family: 'Epilogue', sans-serif;
            background: var(--bg);
            color: var(--text);
            line-height: 1.7;
            min-height: 100vh;
        }

        /* ── HEADER ── */
        header {
            position: sticky; top: 0; z-index: 100;
            background: rgba(245, 243, 238, 0.94);
            backdrop-filter: blur(14px);
            border-bottom: 1px solid var(--border);
        }
        .header-inner {
            max-width: 1100px; margin: 0 auto;
            padding: 0 2rem;
            display: flex; align-items: center; justify-content: space-between;
            height: 60px;
        }
        .logo {
            font-family: 'Space Mono', monospace;
            font-size: 0.82rem; color: var(--primary);
            letter-spacing: 0.04em; text-decoration: none;
        }
        .logo span { color: var(--text-dim); }

        nav { display: flex; }
        .nav-btn {
            background: transparent; border: none;
            padding: 0.5rem 0.95rem;
            font-family: 'Epilogue', sans-serif;
            font-size: 0.76rem; font-weight: 600;
            color: var(--text-dim); cursor: pointer;
            letter-spacing: 0.07em; text-transform: uppercase;
            transition: color 0.2s; position: relative;
        }
        .nav-btn:hover { color: var(--text); }
        .nav-btn.active { color: var(--accent); }
        .nav-btn.active::after {
            content: '';
            position: absolute; bottom: -1px; left: 0.3rem; right: 0.3rem;
            height: 2px; background: var(--accent);
        }

        /* ── MAIN ── */
        main { max-width: 1100px; margin: 0 auto; padding: 3rem 2rem; }
        .tab-content { display: none; animation: fadeUp 0.35s ease-out; }
        .tab-content.active { display: block; }
        @keyframes fadeUp {
            from { opacity: 0; transform: translateY(12px); }
            to   { opacity: 1; transform: translateY(0); }
        }

        /* ── HERO ── */
        .hero {
            border: 1px solid var(--border); background: var(--surface);
            padding: 3rem 3.5rem; margin-bottom: 1.5rem;
            position: relative;
        }
        .hero::before {
            content: ''; position: absolute; top: 0; left: 0;
            width: 3px; height: 100%; background: var(--accent);
        }
        .hero-label {
            font-family: 'Space Mono', monospace;
            font-size: 0.68rem; color: var(--accent);
            letter-spacing: 0.14em; text-transform: uppercase;
            margin-bottom: 1.2rem;
        }
        .hero h1 {
            font-family: 'Playfair Display', serif;
            font-size: 3rem; font-weight: 600; color: var(--text);
            line-height: 1.12; margin-bottom: 0.45rem;
        }
        .hero-role {
            font-size: 0.8rem; color: var(--text-dim);
            letter-spacing: 0.09em; text-transform: uppercase;
            margin-bottom: 2rem; font-weight: 600;
        }
        .hero p {
            color: var(--text-mid); font-size: 0.97rem;
            max-width: 680px; margin-bottom: 0.9rem; line-height: 1.8;
        }
        .hero p strong { color: var(--text); font-weight: 600; }

        /* ── TWO-COL ── */
        .two-col {
            display: grid; grid-template-columns: 1fr 1fr;
            gap: 1.5rem; margin-bottom: 1.5rem;
        }
        .card { border: 1px solid var(--border); background: var(--surface); padding: 2rem; }
        .card-label {
            font-family: 'Space Mono', monospace;
            font-size: 0.65rem; color: var(--text-dim);
            letter-spacing: 0.14em; text-transform: uppercase; margin-bottom: 1rem;
        }
        .interests-list { list-style: none; }
        .interests-list li {
            padding: 0.5rem 0; color: var(--text-mid); font-size: 0.9rem;
            display: flex; align-items: flex-start; gap: 0.75rem;
            border-bottom: 1px solid var(--border);
        }
        .interests-list li:last-child { border-bottom: none; }
        .interests-list li::before {
            content: '▸'; color: var(--accent);
            font-size: 0.7rem; margin-top: 0.28rem; flex-shrink: 0;
        }
        .interests-list li strong { color: var(--text); }

        /* ── CONNECT STRIP ── */
        .connect-strip {
            border: 1px solid var(--border-dark); background: var(--primary);
            padding: 2rem 3rem;
            display: flex; align-items: center;
            justify-content: space-between; gap: 2rem;
            margin-bottom: 1.5rem;
        }
        .connect-strip h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.3rem; color: #F5F3EE;
            margin-bottom: 0.3rem; font-weight: 400;
        }
        .connect-strip p { color: rgba(245,243,238,0.6); font-size: 0.87rem; }

        /* ── BUTTONS ── */
        .btn {
            display: inline-block; padding: 0.7rem 1.6rem;
            background: var(--accent); color: #fff;
            text-decoration: none;
            font-family: 'Space Mono', monospace;
            font-size: 0.75rem; font-weight: 700;
            letter-spacing: 0.04em;
            transition: all 0.2s; white-space: nowrap; flex-shrink: 0;
        }
        .btn:hover { background: #a8501f; transform: translateY(-1px); }
        .btn-ghost {
            background: transparent; color: rgba(245,243,238,0.85);
            border: 1px solid rgba(245,243,238,0.3);
        }
        .btn-ghost:hover { background: rgba(245,243,238,0.1); }
        .btn-outline {
            background: transparent; color: var(--primary);
            border: 1px solid var(--primary);
        }
        .btn-outline:hover { background: var(--primary); color: #fff; }

        /* ── SECTION HEAD ── */
        .section-head {
            display: flex; align-items: baseline; gap: 1rem;
            margin-bottom: 1.25rem; padding-bottom: 0.6rem;
            border-bottom: 1px solid var(--border);
        }
        .section-head h2 {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem; color: var(--text); font-weight: 600;
        }
        .section-head .mono {
            font-family: 'Space Mono', monospace;
            font-size: 0.65rem; color: var(--text-dim); letter-spacing: 0.1em;
        }
        .mt-section { margin-top: 2.5rem; }

        /* ── TIMELINE ── */
        .timeline-item {
            border: 1px solid var(--border); background: var(--surface);
            padding: 1.6rem 2rem 1.6rem 2.25rem;
            margin-bottom: 1px; transition: border-color 0.2s;
            position: relative;
        }
        .timeline-item::before {
            content: ''; position: absolute; left: 0; top: 0; bottom: 0;
            width: 3px; background: var(--border); transition: background 0.2s;
        }
        .timeline-item:hover { border-color: var(--border-dark); }
        .timeline-item:hover::before { background: var(--accent); }
        .t-title { font-size: 1rem; font-weight: 700; color: var(--text); margin-bottom: 0.2rem; }
        .t-meta {
            font-family: 'Space Mono', monospace;
            font-size: 0.68rem; color: var(--text-dim);
            letter-spacing: 0.04em; margin-bottom: 0.65rem;
        }
        .t-meta .org { color: var(--primary); }
        .t-desc { color: var(--text-mid); font-size: 0.88rem; line-height: 1.65; }
        .badge {
            display: inline-block; background: var(--tag-bg);
            border: 1px solid var(--border); color: var(--accent);
            font-family: 'Space Mono', monospace; font-size: 0.6rem;
            padding: 0.18rem 0.6rem; letter-spacing: 0.08em;
            text-transform: uppercase; margin-bottom: 0.6rem;
        }

        /* ── SKILLS ROW ── */
        .skills-row {
            display: grid; grid-template-columns: repeat(3,1fr);
            gap: 1px; border: 1px solid var(--border); margin-bottom: 2rem;
        }
        .skill-block { background: var(--surface); padding: 1.4rem 1.6rem; }
        .skill-block h4 {
            font-family: 'Space Mono', monospace; font-size: 0.65rem;
            color: var(--accent); letter-spacing: 0.1em; text-transform: uppercase;
            margin-bottom: 0.65rem;
        }
        .skill-block p { color: var(--text-mid); font-size: 0.85rem; line-height: 1.6; }

        /* ── PAPER CARDS ── */
        .paper-card {
            border: 1px solid var(--border); background: var(--surface);
            padding: 2rem 2.25rem; margin-bottom: 1px; transition: border-color 0.2s;
        }
        .paper-card:hover { border-color: var(--border-dark); }
        .paper-card h3 {
            font-family: 'Playfair Display', serif; font-size: 1.2rem;
            color: var(--text); margin-bottom: 0.65rem;
            font-weight: 600; line-height: 1.4;
        }
        .paper-card p {
            color: var(--text-mid); font-size: 0.88rem;
            margin-bottom: 0.9rem; line-height: 1.65;
        }
        .paper-link {
            font-family: 'Space Mono', monospace; font-size: 0.72rem;
            color: var(--accent); text-decoration: none;
            letter-spacing: 0.03em; transition: color 0.2s;
        }
        .paper-link:hover { color: var(--primary); }

        /* ── PROJECT GRID ── */
        .projects-grid {
            display: grid; grid-template-columns: repeat(auto-fill, minmax(290px, 1fr));
            gap: 1px; border: 1px solid var(--border); margin-bottom: 2rem;
        }
        .proj-item { background: var(--surface); padding: 1.6rem; transition: background 0.2s; }
        .proj-item:hover { background: var(--surface-2); }
        .proj-icon {
            font-family: 'Space Mono', monospace; font-size: 0.62rem;
            color: var(--green); letter-spacing: 0.1em; margin-bottom: 0.65rem;
        }
        .proj-item h4 { font-size: 0.92rem; font-weight: 700; color: var(--text); margin-bottom: 0.45rem; }
        .proj-item p { color: var(--text-mid); font-size: 0.83rem; line-height: 1.55; margin-bottom: 0.9rem; }
        .proj-link {
            font-family: 'Space Mono', monospace; font-size: 0.68rem;
            color: var(--accent); text-decoration: none;
            letter-spacing: 0.03em; transition: color 0.2s;
        }
        .proj-link:hover { color: var(--primary); }

        /* ── DEMOS ── */
        .demo-grid {
            display: grid; grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
            gap: 1px; border: 1px solid var(--border); margin-bottom: 2rem;
        }
        .demo-item { background: var(--surface); padding: 1.6rem; transition: background 0.2s; }
        .demo-item:hover { background: var(--surface-2); }
        .demo-num {
            font-family: 'Space Mono', monospace; font-size: 0.6rem;
            color: var(--text-dim); letter-spacing: 0.1em; margin-bottom: 0.9rem;
        }
        .demo-item h4 { font-size: 0.92rem; font-weight: 700; color: var(--text); margin-bottom: 0.75rem; line-height: 1.35; }
        .demo-btn {
            display: inline-block;
            font-family: 'Space Mono', monospace; font-size: 0.68rem;
            color: var(--accent); text-decoration: none;
            letter-spacing: 0.03em;
            border-bottom: 1px solid var(--accent-dim); padding-bottom: 1px;
            transition: color 0.2s;
        }
        .demo-btn:hover { color: var(--primary); border-color: var(--primary); }

        /* ── ARTICLES ── */
        .article-item {
            border: 1px solid var(--border); background: var(--surface);
            padding: 1.4rem 2rem; margin-bottom: 1px;
            display: flex; align-items: flex-start; gap: 1.5rem;
            transition: border-color 0.2s;
        }
        .article-item:hover { border-color: var(--border-dark); }
        .article-num {
            font-family: 'Space Mono', monospace; font-size: 0.62rem;
            color: var(--text-dim); min-width: 2rem; margin-top: 0.2rem;
        }
        .article-body h4 { font-size: 0.92rem; font-weight: 600; color: var(--text); margin-bottom: 0.2rem; }
        .article-platform {
            font-family: 'Space Mono', monospace; font-size: 0.65rem;
            color: var(--primary); letter-spacing: 0.05em; margin-bottom: 0.45rem;
        }
        .article-body p { color: var(--text-mid); font-size: 0.83rem; margin-bottom: 0.45rem; line-height: 1.55; }
        .article-link {
            font-family: 'Space Mono', monospace; font-size: 0.67rem;
            color: var(--text-dim); text-decoration: none; transition: color 0.2s;
        }
        .article-link:hover { color: var(--accent); }

        /* ── CERTS ── */
        .cert-grid {
            display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 1px; border: 1px solid var(--border); margin-bottom: 2rem;
        }
        .cert-item {
            background: var(--surface);
            padding: 1.4rem 1.6rem 1.4rem 1.9rem;
            transition: background 0.2s; position: relative;
        }
        .cert-item::before {
            content: ''; position: absolute; left: 0; top: 0; bottom: 0;
            width: 2px; background: var(--border); transition: background 0.2s;
        }
        .cert-item:hover { background: var(--surface-2); }
        .cert-item:hover::before { background: var(--green); }
        .cert-item h4 { font-size: 0.85rem; font-weight: 600; color: var(--text); margin-bottom: 0.3rem; line-height: 1.4; }
        .cert-item p { font-family: 'Space Mono', monospace; font-size: 0.65rem; color: var(--text-dim); letter-spacing: 0.03em; }

        /* ── CONNECT HERO ── */
        .connect-hero {
            border: 1px solid var(--border); background: var(--primary);
            padding: 4rem 3.5rem; text-align: center;
            margin-bottom: 1.5rem; position: relative; overflow: hidden;
        }
        .connect-hero::after {
            content: '</>'; position: absolute; bottom: -2.5rem; right: 2rem;
            font-family: 'Space Mono', monospace; font-size: 9rem;
            color: rgba(245,243,238,0.05); pointer-events: none; line-height: 1;
        }
        .connect-hero .page-label {
            font-family: 'Space Mono', monospace; font-size: 0.68rem;
            color: var(--accent-dim); letter-spacing: 0.14em;
            text-transform: uppercase; margin-bottom: 1.25rem;
        }
        .connect-hero h2 {
            font-family: 'Playfair Display', serif; font-size: 2.6rem;
            color: #F5F3EE; font-weight: 600;
            margin-bottom: 0.75rem; line-height: 1.2;
        }
        .connect-hero p {
            color: rgba(245,243,238,0.6); font-size: 0.95rem;
            max-width: 460px; margin: 0 auto 2.25rem; line-height: 1.75;
        }
        .connect-links {
            display: flex; justify-content: center;
            gap: 0.75rem; flex-wrap: wrap; position: relative; z-index: 1;
        }
        .connect-row {
            display: grid; grid-template-columns: repeat(3, 1fr);
            gap: 1px; border: 1px solid var(--border);
        }
        .connect-item { background: var(--surface); padding: 1.4rem 1.75rem; }
        .ci-label {
            font-family: 'Space Mono', monospace; font-size: 0.62rem;
            color: var(--text-dim); letter-spacing: 0.1em;
            text-transform: uppercase; margin-bottom: 0.3rem;
        }
        .connect-item a {
            font-size: 0.88rem; color: var(--primary);
            text-decoration: none; font-weight: 600; transition: color 0.2s;
        }
        .connect-item a:hover { color: var(--accent); }

        /* ── RESPONSIVE ── */
        @media (max-width: 768px) {
            .hero { padding: 2rem; }
            .hero h1 { font-size: 2.1rem; }
            .two-col { grid-template-columns: 1fr; }
            .connect-strip { flex-direction: column; }
            .skills-row { grid-template-columns: 1fr; }
            .connect-row { grid-template-columns: 1fr; }
            .nav-btn { padding: 0.5rem 0.5rem; font-size: 0.65rem; }
            .connect-hero { padding: 2.5rem 1.5rem; }
            .connect-hero h2 { font-size: 1.9rem; }
        }
    </style>
</head>
<body>

<header>
    <div class="header-inner">
        <a href="#" class="logo">areej<span>.mehboob</span></a>
        <nav>
            <button class="nav-btn active"  onclick="showTab('about',this)">About</button>
            <button class="nav-btn" onclick="showTab('experience',this)">Experience</button>
            <button class="nav-btn" onclick="showTab('research',this)">Research</button>
            <button class="nav-btn" onclick="showTab('demos',this)">Demos</button>
            <button class="nav-btn" onclick="showTab('certs',this)">Certifications</button>
            <button class="nav-btn" onclick="showTab('connect',this)">Connect</button>
        </nav>
    </div>
</header>

<main>

    <!-- ════════ ABOUT ════════ -->
    <div id="about" class="tab-content active">

        <div class="hero">
            <p class="hero-label">// applied nlp researcher & ai systems engineer</p>
            <h1>Areej Mehboob</h1>
            <p class="hero-role">NLP Researcher &nbsp;·&nbsp; Karachi, Pakistan</p>
            <p>I research and build AI systems that make information more accessible — through better language understanding, reliable agents, and evaluation frameworks that actually measure what matters. My focus is on making <strong>agentic AI</strong> not just capable, but genuinely trustworthy.</p>
            <p>My work spans <strong>coding agents</strong>, <strong>LLM evaluation for agents and languages</strong>, retrieval system design, and benchmark development. I care about building agents that reason well, fail gracefully, and can be meaningfully assessed.</p>
        </div>

        <div class="two-col">
            <div class="card">
                <p class="card-label">// research focus</p>
                <ul class="interests-list">
                    <li><span><strong>Agentic AI & Program Synthesis</strong> — autonomous agents, multi-agent systems, code generation</span></li>
                    <li><span><strong>Retrieval Systems & RAG</strong> — dense, sparse, hybrid and multimodal retrieval engines</span></li>
                    <li><span><strong>LLM Evaluation for Agents & Languages</strong> — pipelines, LLM-as-judge, multilingual benchmarks</span></li>
                    <li><span><strong>Multimodal Document Understanding</strong> — reasoning across text, tables, and images</span></li>
                </ul>
            </div>
            <div class="card">
                <p class="card-label">// beyond the work</p>
                <ul class="interests-list">
                    <li><span><strong>History of Technology</strong> — from early computing machines to the modern AI stack</span></li>
                    <li><span><strong>Open Source</strong> — contributing to and building tools that lower barriers in AI research</span></li>
                </ul>
            </div>
        </div>

        <div class="connect-strip">
            <div>
                <h3>Want to connect or collaborate?</h3>
                <p>Open to being onboarded on open-source or other projects — reach out.</p>
            </div>
            <a href="mailto:mehboobareej01@gmail.com" class="btn">Get in Touch →</a>
        </div>

    </div>

    <!-- ════════ EXPERIENCE ════════ -->
    <div id="experience" class="tab-content">

        <div class="section-head">
            <h2>Education</h2>
            <span class="mono">// academic background</span>
        </div>
        <div style="margin-bottom:2rem">
            <div class="timeline-item">
                <p class="t-title">Bachelor of Science in Computer Science</p>
                <p class="t-meta"><span class="org">University of Karachi</span> &nbsp;·&nbsp; Karachi, Pakistan &nbsp;·&nbsp; Jan 2020 – Jan 2024</p>
            </div>
        </div>

        <div class="section-head mt-section">
            <h2>Professional Experience</h2>
            <span class="mono">// industry roles</span>
        </div>
        <div style="margin-bottom:2rem">
            <div class="timeline-item">
                <span class="badge">Current</span>
                <p class="t-title">NLP Researcher</p>
                <p class="t-meta"><span class="org">Traversaal.ai</span> &nbsp;·&nbsp; California, USA (Remote) &nbsp;·&nbsp; Oct 2024 – Present</p>
                <p class="t-desc">LLM evaluation methodologies, advanced AI agents, and retrieval systems for enterprise applications. Research spans benchmark development, coding agent evaluation, and multimodal document understanding.</p>
            </div>
            <div class="timeline-item">
                <p class="t-title">Machine Learning Engineer</p>
                <p class="t-meta"><span class="org">KDYS LAB (Pvt) Ltd</span> &nbsp;·&nbsp; Karachi, Pakistan &nbsp;·&nbsp; Mar 2024 – Oct 2024</p>
                <p class="t-desc">Developed agentic RAG systems using LangChain, optimized LLM prompts for production environments, and built scalable ML pipelines for real-world enterprise applications.</p>
            </div>
        </div>

        <div class="section-head mt-section">
            <h2>Fellowships</h2>
            <span class="mono">// selective programs</span>
        </div>
        <div style="margin-bottom:2rem">
            <div class="timeline-item">
                <span class="badge">Upcoming · Jul 2026</span>
                <p class="t-title">Fatima Fellowship</p>
                <p class="t-meta">9-month Advanced AI Program &nbsp;·&nbsp; Starting July 2026</p>
                <p class="t-desc">Advanced AI fellowship focused on game theory and optimization, with research in multi-agent systems and strategic decision-making algorithms.</p>
            </div>
            <div class="timeline-item">
                <p class="t-title">AMAL Academy Fellow</p>
                <p class="t-meta"><span class="org">Stanford-Funded Fellowship</span> &nbsp;·&nbsp; Jul 2022 – Oct 2022 &nbsp;·&nbsp; 150+ hours</p>
                <p class="t-desc">Selected from 5,200+ applicants. Designed and implemented a comprehensive career counseling program for school children, providing early career guidance and mentorship.</p>
            </div>
        </div>

        <div class="section-head mt-section">
            <h2>Technical Skills</h2>
            <span class="mono">// stack</span>
        </div>
        <div class="skills-row">
            <div class="skill-block">
                <h4>AI / ML</h4>
                <p>Python, PyTorch, TensorFlow, Hugging Face Transformers, LangChain, LlamaIndex, CrewAI, MCP</p>
            </div>
            <div class="skill-block">
                <h4>Specializations</h4>
                <p>RAG Systems, AI Agents, LLMs, Multimodal AI, Vector Databases, LLM Evaluation, Fine-tuning</p>
            </div>
            <div class="skill-block">
                <h4>Dev Tools</h4>
                <p>FastAPI, Docker, PostgreSQL, Git, Qdrant, Hugging Face Spaces, API Development</p>
            </div>
        </div>

    </div>

    <!-- ════════ RESEARCH ════════ -->
    <div id="research" class="tab-content">

        <div class="section-head">
            <h2>Research Papers</h2>
            <span class="mono">// papers</span>
        </div>
        <div style="margin-bottom:2.5rem">
            <div class="paper-card">
                <span class="badge">arXiv preprint</span>
                <h3>UrduBench: An Urdu Reasoning Benchmark using Contextually Ensembled Translations with Human-in-the-Loop</h3>
                <p>A comprehensive benchmark for evaluating reasoning capabilities of language models in Urdu — featuring contextually ensembled translations with human-in-the-loop validation to advance multilingual AI evaluation.</p>
                <a href="https://arxiv.org/abs/2601.21000" target="_blank" class="paper-link">arxiv.org/abs/2601.21000 →</a>
            </div>
            <div class="paper-card">
                <span class="badge">Empirical Study</span>
                <h3>Does Quantization Hurt Coding Agents? An Empirical Study on Quantized Agents</h3>
                <p>An empirical investigation into the effects of model quantization on coding agent performance — analyzing trade-offs between computational efficiency and code generation quality across quantization schemes.</p>
            </div>
        </div>

        <div class="section-head mt-section">
            <h2>Selected Research Projects</h2>
            <span class="mono">// benchmarks, datasets & eval systems</span>
        </div>
        <div class="projects-grid" style="margin-bottom:2.5rem">
            <div class="proj-item">
                <p class="proj-icon">// EVAL</p>
                <h4>DSBC Data Science Task Evaluation</h4>
                <p>Evaluation framework for assessing data science tasks and agent performance across multiple dimensions.</p>
                <a href="https://github.com/traversaal-ai/DSBC-Data-Science-Task-Evaluation" target="_blank" class="proj-link">github.com/traversaal-ai →</a>
            </div>
            <div class="proj-item">
                <p class="proj-icon">// DATASET</p>
                <h4>HYDRA-M3-V0 Dataset</h4>
                <p>Large-scale multimodal dataset for training and evaluating AI systems on diverse document understanding tasks.</p>
                <a href="https://huggingface.co/datasets/large-traversaal/HYDRA-M3-V0" target="_blank" class="proj-link">huggingface.co →</a>
            </div>
            <div class="proj-item">
                <p class="proj-icon">// BENCHMARK</p>
                <h4>UrduBench Leaderboard</h4>
                <p>Official leaderboard and evaluation infrastructure for the UrduBench reasoning benchmark, tracking model performance over time.</p>
                <a href="https://github.com/traversaal-ai/urdubench_leaderboard" target="_blank" class="proj-link">github.com/traversaal-ai →</a>
            </div>
            <div class="proj-item">
                <p class="proj-icon">// ANALYSIS</p>
                <h4>Nanbeige-4-3B Blindspots</h4>
                <p>Analysis of model blindspots and failure modes in Nanbeige-4-3B, with a curated dataset for targeted model improvement.</p>
                <a href="https://huggingface.co/datasets/AreejMehboob17/nanbeige4-3b-blindspots" target="_blank" class="proj-link">huggingface.co →</a>
            </div>
            <div class="proj-item">
                <p class="proj-icon">// NLP</p>
                <h4>PDF Parser & Table Extraction</h4>
                <p>FastAPI-based system for parsing PDFs and extracting structured tables with high accuracy using advanced NLP techniques.</p>
                <a href="https://github.com/traversaal-ai/pdf-parser-table-extraction-fast-api" target="_blank" class="proj-link">github.com/traversaal-ai →</a>
            </div>
            <div class="proj-item">
                <p class="proj-icon">// RETRIEVAL</p>
                <h4>RAG Comparison & Benchmarking</h4>
                <p>Systematic benchmarking and comparison of RAG approaches across architectures and retrieval configurations.</p>
                <a href="https://github.com/Areej17-01/RAG-Comparison-Benchmarking" target="_blank" class="proj-link">github.com/Areej17-01 →</a>
            </div>
        </div>

        <div class="section-head mt-section">
            <h2>Technical Articles</h2>
            <span class="mono">// writing</span>
        </div>
        <div>
            <div class="article-item">
                <span class="article-num">01</span>
                <div class="article-body">
                    <h4>Enabling Agentic AI Through the Model Context Protocol (MCP)</h4>
                    <p class="article-platform">Traversaal.ai Research</p>
                    <p>Analysis of the MCP framework for seamless AI agent integration and cross-platform communication.</p>
                    <a href="https://www.notion.so/traversaal-ai/Enabling-Agentic-AI-Through-the-Model-Context-Protocol-MCP-1b59a2e5c4a6803b9df2fb9928944831" target="_blank" class="article-link">Read →</a>
                </div>
            </div>
            <div class="article-item">
                <span class="article-num">02</span>
                <div class="article-body">
                    <h4>Multi-Modal Enterprise RAG Architecture from Scratch</h4>
                    <p class="article-platform">Medium</p>
                    <p>Comprehensive guide to building scalable multimodal RAG systems for enterprise applications.</p>
                    <a href="https://ai.gopubby.com/multi-modal-enterprise-rag-architecture-from-scratch-a3a12df0d055" target="_blank" class="article-link">Read →</a>
                </div>
            </div>
            <div class="article-item">
                <span class="article-num">03</span>
                <div class="article-body">
                    <h4>Initialization of Weights in Neural Networks</h4>
                    <p class="article-platform">Medium</p>
                    <p>Technical analysis of weight initialization techniques and their impact on training performance and convergence.</p>
                    <a href="https://medium.com/@mehboobareej01/initialization-of-weights-in-neural-network-7243898988de" target="_blank" class="article-link">Read →</a>
                </div>
            </div>
            <div class="article-item">
                <span class="article-num">04</span>
                <div class="article-body">
                    <h4>Understanding TF-IDF: Formulas and sklearn Implementation</h4>
                    <p class="article-platform">Medium</p>
                    <p>Mathematical exposition of TF-IDF with formula derivations and practical scikit-learn implementation.</p>
                    <a href="https://medium.com/@mehboobareej01/understanding-tf-idf-formulas-and-value-returned-output-from-sklearn-library-483cb2b02efa" target="_blank" class="article-link">Read →</a>
                </div>
            </div>
            <div class="article-item">
                <span class="article-num">05</span>
                <div class="article-body">
                    <h4>Feature Extraction Essentials for Image Similarity</h4>
                    <p class="article-platform">Medium</p>
                    <p>Technical guide to feature extraction methodologies for enhancing image similarity detection.</p>
                    <a href="https://medium.com/@mehboobareej01/feature-extraction-essentials-enhancing-image-similarity-with-feature-extraction-f46473869d3a" target="_blank" class="article-link">Read →</a>
                </div>
            </div>
        </div>

    </div>

    <!-- ════════ DEMOS ════════ -->
    <div id="demos" class="tab-content">

        <div class="section-head">
            <h2>Interactive Demos</h2>
            <span class="mono">// live on Hugging Face Spaces</span>
        </div>
        <div class="demo-grid" style="margin-bottom:2.5rem">
            <div class="demo-item">
                <p class="demo-num">DEMO / 01</p>
                <h4>Nexus Supply Chain Intelligence</h4>
                <a href="https://huggingface.co/spaces/AreejMehboob17/Nexus-Supply-Chain-Intelligence-Platform" target="_blank" class="demo-btn">Launch →</a>
            </div>
            <div class="demo-item">
                <p class="demo-num">DEMO / 02</p>
                <h4>LLMind Arena</h4>
                <a href="https://huggingface.co/spaces/AreejMehboob17/LLMindArena" target="_blank" class="demo-btn">Launch →</a>
            </div>
            <div class="demo-item">
                <p class="demo-num">DEMO / 03</p>
                <h4>VisionText RAG</h4>
                <a href="https://huggingface.co/spaces/AreejMehboob17/VisionText-RAG" target="_blank" class="demo-btn">Launch →</a>
            </div>
            <div class="demo-item">
                <p class="demo-num">DEMO / 04</p>
                <h4>LuminaFi</h4>
                <a href="https://huggingface.co/spaces/AreejMehboob17/LuminaFi" target="_blank" class="demo-btn">Launch →</a>
            </div>
        </div>

        <div class="section-head mt-section">
            <h2>Selected Projects</h2>
            <span class="mono">// engineering & dev</span>
        </div>
        <div class="projects-grid">
            <div class="proj-item">
                <p class="proj-icon">// AGENTS</p>
                <h4>Multi-Agent System with CrewAI</h4>
                <p>Sophisticated multi-agent systems using the CrewAI framework for collaborative, goal-directed task solving.</p>
                <a href="https://github.com/Areej17-01/MultiAgenticSystem-crewAI-" target="_blank" class="proj-link">View on GitHub →</a>
            </div>
            <div class="proj-item">
                <p class="proj-icon">// VIZ</p>
                <h4>DataLens</h4>
                <p>Advanced data visualization and analysis tool with interactive dashboards for exploratory analysis.</p>
                <a href="https://github.com/Areej17-01/DataLens" target="_blank" class="proj-link">View on GitHub →</a>
            </div>
            <div class="proj-item">
                <p class="proj-icon">// EDUCATION</p>
                <h4>Guide to Generative AI</h4>
                <p>End-to-end educational resource on LLMs, transformers, and training methodologies with implementations.</p>
                <a href="https://github.com/Areej17-01/Guide-To-Generative-AI-LLMs-and-Transformers-Training" target="_blank" class="proj-link">View on GitHub →</a>
            </div>
        </div>

    </div>

    <!-- ════════ CERTIFICATIONS ════════ -->
    <div id="certs" class="tab-content">

        <div class="section-head">
            <h2>Certifications</h2>
            <span class="mono">// credentials & training</span>
        </div>
        <div class="cert-grid">
            <div class="cert-item">
                <h4>Applied Data Science with Machine Learning</h4>
                <p>Techmazone &nbsp;·&nbsp; 2021–2022 &nbsp;·&nbsp; 96 CPD hrs</p>
            </div>
            <div class="cert-item">
                <h4>LLM Mastery: Complete Guide to Transformers & GenAI</h4>
                <p>Udemy &nbsp;·&nbsp; Feb 2025 &nbsp;·&nbsp; 7.5 hrs</p>
            </div>
            <div class="cert-item">
                <h4>Mastering Agentic Design Patterns with Hands-on Projects</h4>
                <p>Udemy &nbsp;·&nbsp; Jan 2026 &nbsp;·&nbsp; 5.5 hrs</p>
            </div>
            <div class="cert-item">
                <h4>Applied Generative AI and Natural Language Processing</h4>
                <p>Udemy &nbsp;·&nbsp; Jan 2026 &nbsp;·&nbsp; 10 hrs</p>
            </div>
            <div class="cert-item">
                <h4>Building Applications with Django and PostgreSQL</h4>
                <p>Mar 2024 &nbsp;·&nbsp; 5 hrs</p>
            </div>
            <div class="cert-item">
                <h4>Data Manipulation with Pandas</h4>
                <p>Aug 2023 &nbsp;·&nbsp; 4 hrs</p>
            </div>
            <div class="cert-item">
                <h4>Introduction to Statistics in Python</h4>
                <p>Sep 2023 &nbsp;·&nbsp; 4 hrs</p>
            </div>
            <div class="cert-item">
                <h4>Joining Data with Pandas</h4>
                <p>Sep 2023 &nbsp;·&nbsp; 4 hrs</p>
            </div>
        </div>

    </div>

    <!-- ════════ CONNECT ════════ -->
    <div id="connect" class="tab-content">

        <div class="connect-hero">
            <p class="page-label">// let's build something</p>
            <h2>Want to Connect<br>or Collaborate?</h2>
            <p>Open to research collaborations, open-source onboarding, or a conversation about agents, retrieval, and AI evaluation.</p>
            <div class="connect-links">
                <a href="mailto:mehboobareej01@gmail.com" class="btn">Email Me →</a>
                <a href="https://www.linkedin.com/in/areej-mehboob-396b7a207/" target="_blank" class="btn btn-ghost">LinkedIn</a>
                <a href="https://github.com/Areej17-01" target="_blank" class="btn btn-ghost">GitHub</a>
            </div>
        </div>

        <div class="connect-row">
            <div class="connect-item">
                <p class="ci-label">Email</p>
                <a href="mailto:mehboobareej01@gmail.com">mehboobareej01@gmail.com</a>
            </div>
            <div class="connect-item">
                <p class="ci-label">LinkedIn</p>
                <a href="https://www.linkedin.com/in/areej-mehboob-396b7a207/" target="_blank">linkedin.com/in/areej-mehboob</a>
            </div>
            <div class="connect-item">
                <p class="ci-label">GitHub</p>
                <a href="https://github.com/Areej17-01" target="_blank">github.com/Areej17-01</a>
            </div>
            <div class="connect-item">
                <p class="ci-label">Hugging Face</p>
                <a href="https://huggingface.co/AreejMehboob17" target="_blank">huggingface.co/AreejMehboob17</a>
            </div>
            <div class="connect-item">
                <p class="ci-label">Medium</p>
                <a href="https://medium.com/@mehboobareej01" target="_blank">medium.com/@mehboobareej01</a>
            </div>

            <div class="connect-item">
                <p class="ci-label">Google Scholar</p>
                <a href="https://scholar.google.com/citations?hl=en&view_op=list_works&gmla=AF9nlQuyR9ljGEZm0LViiB_u8Y9MqO4ZLTIGZChUtisxn3MH--6NuNsLxKhaKRihXLFXc60zuypI-5ft9wOQEQ&user=e-5va5UAAAAJ" target="_blank">scholar.google.com/citations</a>
            </div>
        </div>

    </div>

</main>

<script>
    function showTab(name, btn) {
        document.querySelectorAll('.tab-content').forEach(t => t.classList.remove('active'));
        document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
        document.getElementById(name).classList.add('active');
        if (btn) btn.classList.add('active');
        window.scrollTo({ top: 0, behavior: 'smooth' });
    }
</script>

</body>
</html>
