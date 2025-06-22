<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Areej Mehboob - NLP Researcher</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #000;
            color: #fff;
            font-family: 'Arial', sans-serif;
            overflow-x: hidden;
        }

        /* Animated Header */
        .header {
            height: 50vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            position: relative;
            overflow: hidden;
            flex-direction: column;
            padding-top: 20px;
        }

        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="%23000000" fill-opacity="0.1" d="M0,96L48,112C96,128,192,160,288,160C384,160,480,128,576,112C672,96,768,96,864,112C960,128,1056,160,1152,176C1248,192,1344,192,1392,192L1440,192L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path></svg>') repeat-x;
            animation: wave 10s linear infinite;
        }

        @keyframes wave {
            0% { transform: translateX(0); }
            100% { transform: translateX(-100%); }
        }

        .name-animation {
            font-size: 4rem;
            font-weight: bold;
            text-align: center;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #45b7d1, #96ceb4);
            background-size: 400% 400%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: gradient-shift 3s ease-in-out infinite;
        }

        @keyframes gradient-shift {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }

        .typing-animation {
            font-size: 1.5rem;
            margin-top: 20px;
            text-align: center;
            color: #4ecdc4;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 15px;
            flex-wrap: wrap;
        }

        .contact-link-header {
            color: #fff;
            text-decoration: none;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 5px;
            transition: all 0.3s ease;
        }

        .contact-link-header:hover {
            color: #ff6b6b;
            transform: translateY(-2px);
        }

        /* Header Buttons Container */
        .header-buttons {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 20px;
            z-index: 10;
            width: 100%; /* Ensure it takes full width */
        }

        .cv-button-header, .contact-button-header {
            background: linear-gradient(135deg, #ff6b6b, #4ecdc4);
            color: #000;
            padding: 12px 24px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: all 0.3s ease;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
            border: 2px solid rgba(255, 255, 255, 0.2);
        }

        .contact-button-header {
            background: linear-gradient(135deg, #667eea, #764ba2);
        }

        .cv-button-header:hover, .contact-button-header:hover {
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 8px 25px rgba(255, 107, 107, 0.4);
            color: #fff;
        }

        .cv-button-header:hover {
            background: linear-gradient(135deg, #ff6b6b, #ff6b6b);
        }

        .contact-button-header:hover {
            background: linear-gradient(135deg, #667eea, #667eea);
        }

        /* About Section */
        .about-section {
            padding: 60px 0;
            display: flex;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            gap: 50px;
        }

        .collaboration-animation {
            flex: 1;
            text-align: center;
        }

        .collab-text {
            font-size: 2rem;
            margin-bottom: 30px;
            color: #ff6b6b;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.7; }
        }

        .quote {
            font-style: italic;
            font-size: 1.2rem;
            color: #4ecdc4;
            margin-bottom: 20px;
        }

        .about-content {
            flex: 1;
            padding: 0 20px;
        }

        .about-content h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: #ff6b6b;
        }

        .about-content p {
            font-size: 1.1rem;
            line-height: 1.8;
            margin-bottom: 20px;
            color: #ddd;
        }

        .gif-container {
            text-align: center;
            margin-top: 30px;
        }

        .gif-container img {
            max-width: 400px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(255, 107, 107, 0.3);
        }

        /* Skills Moving Belt */
        .skills-belt {
            background: #111;
            padding: 40px 0;
            overflow: hidden;
            position: relative;
        }

        .skills-belt h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 40px;
            color: #4ecdc4;
        }

        .belt-container {
            display: flex;
            animation: scroll-left 20s linear infinite;
        }

        @keyframes scroll-left {
            0% { transform: translateX(100%); }
            100% { transform: translateX(-100%); }
        }

        .skill-item {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            margin: 0 15px;
            padding: 15px 30px;
            border-radius: 50px;
            white-space: nowrap;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 10px;
            min-width: 200px;
            justify-content: center;
        }

        /* Skills and Technology Section */
        .skills-tech {
            padding: 60px 0;
            max-width: 1200px;
            margin: 0 auto;
        }

        .skills-tech h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 40px;
            color: #ff6b6b;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            padding: 0 20px;
        }

        .skill-category {
            background: #111;
            padding: 30px;
            border-radius: 20px;
            text-align: center;
            border: 2px solid #333;
            transition: transform 0.3s ease;
        }

        .skill-category:hover {
            transform: translateY(-10px);
            border-color: #4ecdc4;
        }

        .skill-category h3 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: #4ecdc4;
        }

        .skill-badges {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            justify-content: center;
        }

        .badge {
            background: #333;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.9rem;
            border: 1px solid #555;
        }

        /* Compact Table Styles */
        .table-section {
            padding: 40px 0;
            max-width: 1200px;
            margin: 0 auto;
        }

        .table-section h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 30px;
            color: #ff6b6b;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            background: #111;
            border-radius: 10px;
            overflow: hidden;
            margin-bottom: 30px;
        }

        th, td {
            padding: 12px 15px;
            text-align: left;
            border-bottom: 1px solid #333;
        }

        th {
            background: #222;
            color: #4ecdc4;
            font-weight: bold;
        }

        tr:hover {
            background: #222;
        }

        /* Interactive Articles Section */
        .articles-section {
            padding: 60px 0;
            background: #111;
            overflow: hidden;
        }

        .articles-section h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 50px;
            color: #4ecdc4;
        }

        .articles-container {
            display: flex;
            animation: scroll-articles 25s linear infinite;
            gap: 30px;
        }

        @keyframes scroll-articles {
            0% { transform: translateX(100%); }
            100% { transform: translateX(-100%); }
        }

        .article-card {
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
            border-radius: 20px;
            padding: 25px;
            min-width: 350px;
            border: 2px solid #333;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            cursor: pointer;
        }

        .article-card:hover {
            transform: translateY(-10px);
            border-color: #4ecdc4;
            animation-play-state: paused;
        }

        .article-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, transparent, rgba(78, 205, 196, 0.1), transparent);
            transition: left 0.5s ease;
        }

        .article-card:hover::before {
            left: 100%;
        }

        .article-image {
            width: 100%;
            height: 150px;
            background: linear-gradient(45deg, #667eea, #764ba2);
            border-radius: 15px;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            position: relative;
            overflow: hidden;
        }

        .article-image::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, rgba(255,255,255,0.1), transparent);
            animation: shimmer 2s infinite;
        }

        @keyframes shimmer {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }

        .article-title {
            font-size: 1.3rem;
            color: #4ecdc4;
            margin-bottom: 10px;
            font-weight: bold;
        }

        .article-platform {
            color: #ff6b6b;
            font-size: 0.9rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .article-description {
            color: #ddd;
            font-size: 0.95rem;
            line-height: 1.6;
            margin-bottom: 20px;
        }

        .article-link {
            background: linear-gradient(135deg, #4ecdc4, #45b7d1);
            color: #000;
            padding: 8px 16px;
            border-radius: 20px;
            text-decoration: none;
            font-weight: bold;
            font-size: 0.9rem;
            transition: transform 0.3s ease;
            display: inline-block;
        }

        .article-link:hover {
            transform: scale(1.05);
        }

        /* Certificate Belt */
        .cert-belt {
            background: #111;
            padding: 50px 0;
            overflow: hidden;
        }

        .cert-belt h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 40px;
            color: #4ecdc4;
        }

        .cert-container {
            display: flex;
            animation: scroll-right 15s linear infinite;
        }

        @keyframes scroll-right {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }

        .cert-item {
            background: #222;
            margin: 0 20px;
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            min-width: 250px;
            border: 2px solid #333;
        }

        .cert-item img {
            width: 100%;
            height: auto;
            max-height: 150px;
            object-fit: contain;
            border-radius: 10px;
            margin-bottom: 15px;
        }

       /* Projects Section */
.projects {
    padding: 60px 0;
    max-width: 1500px; /* Increased to accommodate 4 projects */
    margin: 0 auto;
    overflow-x: auto; /* Allows horizontal scrolling if needed */
}

.projects h2 {
    text-align: center;
    font-size: 2.5rem;
    margin-bottom: 40px;
    color: #ff6b6b;
}

.project-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr); /* Fixed 4 columns */
    gap: 30px;
    padding: 0 20px;
    min-width: 1400px; /* Minimum width to prevent wrapping */
}

.project-card {
    background: #111;
    border-radius: 20px;
    padding: 30px;
    border: 2px solid #333;
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
    min-width: 350px; /* Minimum card width */
}

.project-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(45deg, transparent, rgba(255, 107, 107, 0.1), transparent);
    transition: left 0.5s ease;
}

.project-card:hover::before {
    left: 100%;
}

.project-card:hover {
    transform: translateY(-10px);
    border-color: #ff6b6b;
}

.project-card h3 {
    font-size: 1.5rem;
    margin-bottom: 15px;
    color: #4ecdc4;
}

.project-card p {
    color: #ddd;
    line-height: 1.6;
    margin-bottom: 20px;
}

.tech-stack {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-bottom: 20px;
}

.tech-tag {
    background: #333;
    padding: 5px 12px;
    border-radius: 15px;
    font-size: 0.8rem;
    color: #4ecdc4;
}

.project-link {
    display: inline-block;
    background: linear-gradient(135deg, #ff6b6b, #4ecdc4);
    color: #000;
    padding: 10px 20px;
    border-radius: 25px;
    text-decoration: none;
    font-weight: bold;
    transition: transform 0.3s ease;
}

.project-link:hover {
    transform: scale(1.05);
}

/* Responsive adjustments */
@media (max-width: 1600px) {
    .project-grid {
        min-width: 1200px;
    }
}

@media (max-width: 1400px) {
    .project-grid {
        grid-template-columns: repeat(4, 300px);
        gap: 20px;
    }
    .project-card {
        min-width: 300px;
        padding: 25px;
    }
}

@media (max-width: 768px) {
    .project-grid {
        grid-template-columns: repeat(4, 280px);
        gap: 15px;
    }
    .project-card {
        min-width: 280px;
        padding: 20px;
    }
} 
/* Enhanced Contact Section */
        .contact {
            padding: 80px 0;
            text-align: center;
            background: #111;
        }

        .contact h2 {
            font-size: 3rem;
            margin-bottom: 50px;
            color: #ff6b6b;
            position: relative;
            display: inline-block;
        }

        .contact h2::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: linear-gradient(90deg, #ff6b6b, #4ecdc4);
            border-radius: 2px;
        }

        .contact-links {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            max-width: 1000px;
            margin: 0 auto;
        }

        .contact-link {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #fff;
            padding: 20px 35px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 1.2rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            border: 2px solid rgba(255,255,255,0.1);
        }

        .contact-link:hover {
            transform: translateY(-5px) scale(1.03);
            box-shadow: 0 15px 30px rgba(255, 107, 107, 0.4);
        }

        .contact-link[download] {
            background: linear-gradient(135deg, #ff6b6b, #ff9e4f);
            font-size: 1.3rem;
            padding: 22px 40px;
        }

        /* Footer */
        .footer {
            background: #000;
            padding: 40px 0;
            text-align: center;
            border-top: 1px solid #333;
        }

        .footer h3 {
            color: #4ecdc4;
            margin-bottom: 20px;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .name-animation {
                font-size: 2.5rem;
            }
            
            .about-section {
                flex-direction: column;
                padding: 40px 20px;
            }
            
            .skills-grid {
                grid-template-columns: 1fr;
            }
            
            .project-grid {
                grid-template-columns: 1fr;
            }
            
            .contact-links {
                flex-direction: column;
                align-items: center;
                gap: 20px;
            }

            .contact-link {
                padding: 16px 25px;
                font-size: 1.1rem;
            }

            .contact-link[download] {
                padding: 18px 30px;
            }

            .article-card {
                min-width: 280px;
            }

            .table-section {
                padding: 30px 0;
            }

            .projects {
                padding: 40px 0;
            }

            .contact-info {
                flex-direction: column;
                align-items: center;
                gap: 10px;
            }

            .header-buttons {
                flex-direction: column;
                align-items: center;
                gap: 10px;
            }

            .contact h2 {
                font-size: 2.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header with Animated Name -->
    <section class="header">
        <div>
            <h1 class="name-animation">Areej Mehboob</h1>
            <div class="typing-animation">
                <span id="typing-text">NLP Researcher | LLMs | Retrieval Systems</span>
            </div>
            <div class="contact-info">
                <a href="mailto:mehboobareej01@gmail.com" class="contact-link-header">
                    ✉️ mehboobareej01@gmail.com
                </a>
                <a href="https://www.linkedin.com/in/areej-mehboob-396b7a207/" class="contact-link-header" target="_blank">
                    🔗 LinkedIn
                </a>
                <a href="https://github.com/Areej17-01" class="contact-link-header" target="_blank">
                    💻 GitHub
                </a>
                <a href="https://huggingface.co/spaces/AreejMehboob17" class="contact-link-header" target="_blank">
                    🤗 Hugging Face
                </a>
            </div>
            
            <!-- Buttons Container -->
            <div class="header-buttons">
                <a href="https://drive.google.com/uc?export=download&id=16Ma9jEKdb_2ONF6Oz1RE-W1Z5naS0SYQ" 
                   class="cv-button-header" 
                   download="Areej_Mehboob_CV.pdf">
                    <span style="font-size: 1.2em;">⬇️</span> Download CV
                </a>
                <a href="mailto:mehboobareej01@gmail.com" class="contact-button-header">
                    ✉️ Contact Me
                </a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about-section">
        <div class="collaboration-animation">
            <h2 class="collab-text">🤝 Open to Collaboration</h2>
            <p class="quote">💡 "The best way to predict the future is to create it." - Alan Kay</p>
            <div class="gif-container">
                <img src="https://media.giphy.com/media/L1R1tvI9svkIWwpVYr/giphy.gif" alt="Coding Animation">
            </div>
        </div>
        <div class="about-content">
            <h2>👩‍💻 About Me</h2>
            <p>I'm an <strong>NLP researcher</strong> with a background in machine learning engineering and a BSCS in Computer Science, currently focused on advancing Retrieval-Augmented Generation (RAG) systems, AI agents, and large language models (both traditional and multimodal).</p>
            <p>My work combines research and application development, building sophisticated retrieval engines, agentic RAG architectures, and autonomous AI agents while also creating practical applications. I have extensive hands-on experience in agent systems development and expertise in LLM evaluation methodologies and fine-tuning.</p>
        </div>
    </section>

    <!-- Skills Moving Belt -->
    <section class="skills-belt">
        <h2>🔥 Core Expertise</h2>
        <div class="belt-container">
            <div class="skill-item">🤖 RAG Systems</div>
            <div class="skill-item">🧠 AI Agents</div>
            <div class="skill-item">📊 LLMs</div>
            <div class="skill-item">🔍 Multimodal AI</div>
            <div class="skill-item">⚡ Vector Databases</div>
            <div class="skill-item">🚀 Retrieval Engines</div>
            <div class="skill-item">🎯 LLM Evaluation</div>
            <div class="skill-item">🔧 Fine-tuning</div>
        </div>
    </section>

    <!-- Education -->
    <section class="table-section">
        <h2>🎓 Education</h2>
        <table>
            <thead>
                <tr>
                    <th>Institution</th>
                    <th>Degree</th>
                    <th>Location</th>
                    <th>Duration</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>University of Karachi</td>
                    <td>BSCS</td>
                    <td>Karachi, Pakistan</td>
                    <td>January 2020 – January 2024</td>
                </tr>
                <tr>
                    <td>Techmazone</td>
                    <td>Applied Data Science with Machine Learning</td>
                    <td>Karachi, Pakistan</td>
                    <td>February 2021 – January 2022</td>
                </tr>
            </tbody>
        </table>
    </section>

    <!-- Work Experience -->
    <section class="table-section">
        <h2>💼 Work Experience</h2>
        <table>
            <thead>
                <tr>
                    <th>Position</th>
                    <th>Company</th>
                    <th>Location</th>
                    <th>Duration</th>
                    <th>Description</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>🔬 NLP Researcher</td>
                    <td>Traversaal.ai</td>
                    <td>California, USA (Remote)</td>
                    <td>October 2024 – Present</td>
                    <td>Working with evals, LLMs, Agents, and advanced retrieval systems</td>
                </tr>
                <tr>
                    <td>⚙️ ML Engineer</td>
                    <td>KDYS LAB (Pvt) Ltd</td>
                    <td>Karachi, Pakistan (Onsite)</td>
                    <td>March 2024 – October 2024</td>
                    <td>Worked on Agentic RAG with LangChain and LLM prompt wrapper APIs</td>
                </tr>
            </tbody>
        </table>
    </section>
    
    <!-- Featured Projects -->
   <!-- Projects Section -->
<!-- Projects Section -->
<section class="projects">
    <h2>🚀 Featured Projects</h2>
    <div class="project-grid">
        <div class="project-card">
            <h3>🤖 MultiAgenticSystem-crewAI</h3>
            <p>A sophisticated multi-agent system ,designed to perform automated tasks efficiently across various domains. Each agent operates independently, focusing on tasks like internet search, image classification, and retrieval-augmented generation (RAG) based queries.</p>
            <div class="tech-stack">
                <span class="tech-tag">Python</span>
                <span class="tech-tag">CrewAI</span>
                <span class="tech-tag">LangChain</span>
            </div>
            <a href="https://github.com/Areej17-01/MultiAgenticSystem-crewAI-" class="project-link" target="_blank">View Project</a>
        </div>
        <div class="project-card">
            <h3>❓Vision-Text RAG System</h3>
            <p>A comprehensive multimodal RAG architecture designed for processing images and text from pdf, Allowing user to talk with their pdf text and image content</p>
            <div class="tech-stack">
                <span class="tech-tag">Python</span>
                <span class="tech-tag">Transformer</span>
                <span class="tech-tag">qdrant DB</span>
            </div>
            <a href="https://huggingface.co/spaces/AreejMehboob17/VisionText-RAG" class="project-link" target="_blank">View Project</a>
        </div>
        <div class="project-card">
            <h3>🧠 Luminafi</h3>
            <p>AI-Powered Finance Analysis Workflow: Comprehensive financial analysis with real-time data, AI insights, and news updates</p>
            <div class="tech-stack">
                <span class="tech-tag">Python</span>
                <span class="tech-tag">PyTorch</span>
                <span class="tech-tag">Transformers</span>
            </div>
            <a href="https://huggingface.co/spaces/AreejMehboob17/LuminaFi" class="project-link" target="_blank">View Project</a>
        </div>
        <div class="project-card">
            <h3>🎭 LLMIND ARENA</h3>
            <p>An immersive AI experience powered by multiple LLMs, combining emotionally rich family drama roleplay and intelligent debate simulation—each character driven by a distinct language model for dynamic, realistic interactions.</p>
            <div class="tech-stack">
                <span class="tech-tag">Python</span>
                <span class="tech-tag">LLMs</span>
                <span class="tech-tag">Transformers</span>
            </div>
            <a href="https://huggingface.co/spaces/AreejMehboob17/LLMindArena" class="project-link" target="_blank">View Project</a>
        </div>
    </div>
</section>

    <!-- Interactive Articles Section -->
    <section class="articles-section">
        <h2>📝 Articles & Blog Posts</h2>
        <div class="articles-container">
            <div class="article-card">
                <div class="article-image">🤖</div>
                <div class="article-title">Enabling Agentic AI Through the Model Context Protocol (MCP)</div>
                <div class="article-platform">📋 Notion</div>
                <div class="article-description">Exploring how MCP enables seamless AI agent integration and communication across different platforms and systems.</div>
                <a href="https://www.notion.so/traversaal-ai/Enabling-Agentic-AI-Through-the-Model-Context-Protocol-MCP-1b59a2e5c4a6803b9df2fb9928944831" target="_blank" class="article-link">Read Article</a>
            </div>
            <div class="article-card">
                <div class="article-image">🔍</div>
                <div class="article-title">Multi-Modal Enterprise RAG Architecture from Scratch</div>
                <div class="article-platform">📝 Medium</div>
                <div class="article-description">A comprehensive guide to building scalable multimodal RAG systems for enterprise applications with advanced retrieval mechanisms.</div>
                <a href="https://ai.gopubby.com/multi-modal-enterprise-rag-architecture-from-scratch-a3a12df0d055" target="_blank" class="article-link">Read Article</a>
            </div>
            <div class="article-card">
                <div class="article-image">⚡</div>
                <div class="article-title">Initialization of Weights in Neural Networks</div>
                <div class="article-platform">📝 Medium</div>
                <div class="article-description">Deep dive into weight initialization techniques and their impact on neural network training performance and convergence.</div>
                <a href="https://medium.com/@mehboobareej01/initialization-of-weights-in-neural-network-7243898988de" target="_blank" class="article-link">Read Article</a>
            </div>
            <div class="article-card">
                <div class="article-image">📊</div>
                <div class="article-title">Understanding TF-IDF: Formulas and sklearn Implementation</div>
                <div class="article-platform">📝 Medium</div>
                <div class="article-description">Complete explanation of TF-IDF algorithm with mathematical formulas and practical implementation using scikit-learn.</div>
                <a href="https://medium.com/@mehboobareej01/understanding-tf-idf-formulas-and-value-returned-output-from-sklearn-library-483cb2b02efa" target="_blank" class="article-link">Read Article</a>
            </div>
            <div class="article-card">
                <div class="article-image">🖼️</div>
                <div class="article-title">Feature Extraction Essentials for Image Similarity</div>
                <div class="article-platform">📝 Medium</div>
                <div class="article-description">Comprehensive guide to feature extraction techniques for enhancing image similarity detection and computer vision applications.</div>
                <a href="https://medium.com/@mehboobareej01/feature-extraction-essentials-enhancing-image-similarity-with-feature-extraction-f46473869d3a" target="_blank" class="article-link">Read Article</a>
            </div>
        </div>
    </section>

    <!-- Certifications Moving Belt -->
    <section class="cert-belt">
        <h2>🏆 Certifications</h2>
        <div class="cert-container">
            <div class="cert-item">
                <img src="certs/1742035157859.jpg" alt="Applied Data Science with Machine Learning Certificate">
                <h4>Applied Data Science with ML</h4>
                <p>Techmazone</p>
                <p>2021-2022 (96 CPD Hours)</p>
            </div>
            <div class="cert-item">
                <img src="certs/1742035157859.jpg" alt="Applied Data Science with Machine Learning Certificate">
                <h4>Applied Data Science with ML</h4>
                <p>Techmazone</p>
                <p>2021-2022 (96 CPD Hours)</p>
            </div>
            <div class="cert-item">
                <img src="certs/UC-3062c044-d171-449a-b0dc-00e4221255d5 (1).jpg" alt="Machine Learning Associate Intended Certificate">
                <h4>Machine Learning Associate Intended</h4>
                <p>Jan 15, 2025 (23 Minutes)</p>
            </div>
            <div class="cert-item">
                <img src="certs/pandas.png" alt="Data Manipulation with pandas Certificate">
                <h4>Data Manipulation With Panda</h4>
                <p>Aug, 2023 (4 hours)</p>
            </div>
            <div class="cert-item">
                <img src="certs/stats.png" alt="Intro to stattistics Certificate">
                <h4>Introduction to Statistics In Python</h4>
                <p>Sep, 2023 (4 hours)</p>
            </div>
            <div class="cert-item">
                <img src="certs/Screenshot 2025-06-23 014313.png" alt="Joining data with pandas Certificate">
                <h4>Joining Data With Pandas</h4>
                <p>Sep, 2023 (4 hours)</p>
            </div>
    </section>

    <!-- Skills and Technology -->
    <section class="skills-tech">
        <h2>🛠️ Skills & Technologies</h2>
        <div class="skills-grid">
            <div class="skill-category">
                <h3>🧠 AI/ML</h3>
                <div class="skill-badges">
                    <span class="badge">Python</span>
                    <span class="badge">PyTorch</span>
                    <span class="badge">TensorFlow</span>
                    <span class="badge">🤗 Hugging Face</span>
                    <span class="badge">🦜 LangChain</span>
                    <span class="badge"> llamaIndex</span>
                    <span class="badge"> MCP</span>
                    <span class="badge"> CrewAI</span>
                </div>
            </div>
            <div class="skill-category">
                <h3>🤖 Specializations</h3>
                <div class="skill-badges">
                    <span class="badge">RAG Systems</span>
                    <span class="badge">AI Agents</span>
                    <span class="badge">LLMs</span>
                    <span class="badge">Multimodal AI</span>
                    <span class="badge">Vector DBs</span>
                </div>
            </div>
            <div class="skill-category">
                <h3>🔧 Tools</h3>
                <div class="skill-badges">
                    <span class="badge">FastAPI</span>
                    <span class="badge">Docker</span>
                    <span class="badge">PostgreSQL</span>
                    <span class="badge">Git</span>
                    <span class="badge">Hugging Face deployment</span>
                </div>
            </div>
        </div>
    </section>
    <!-- Contact -->
    <section class="contact">
        <h2>🔗 Let's Connect</h2>
        <div class="contact-links">
            <a href="https://huggingface.co/spaces/AreejMehboob17" class="contact-link" target="_blank">
                🤗 Hugging face
            </a>
            <a href="https://www.linkedin.com/in/areej-mehboob-396b7a207/" class="contact-link" target="_blank">
                💼 LinkedIn
            </a>
            <a href="mailto:mehboobareej01@gmail.com" class="contact-link">
                📧 Email
            </a>
            <a href="https://medium.com/@mehboobareej01" class="contact-link" target="_blank">
                📝 Medium
            </a>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <h3>🙏 Thanks for visiting! Let's build together! 🚀</h3>
        <p style="color: #666; margin-top: 10px;">© 2024 Areej Mehboob. All rights reserved.</p>
    </footer>
</footer>

    <script>
        // Typing animation
        const texts = [
            "NLP Researcher | LLMs | Retrieval Systems",
            "Building with AI ✨",
            "Open to Research & Collaboration!"
        ];
        let textIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        const typingElement = document.getElementById('typing-text');

        function typeText() {
            const currentText = texts[textIndex];
            
            if (isDeleting) {
                typingElement.textContent = currentText.substring(0, charIndex - 1);
                charIndex--;
            } else {
                typingElement.textContent = currentText.substring(0, charIndex + 1);
                charIndex++;
            }

            if (!isDeleting && charIndex === currentText.length) {
                setTimeout(() => isDeleting = true, 1000);
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                textIndex = (textIndex + 1) % texts.length;
            }

            const speed = isDeleting ? 50 : 100;
            setTimeout(typeText, speed);
        }

        typeText();

        // Smooth scrolling for any internal links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>

   
