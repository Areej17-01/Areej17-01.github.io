
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
            font-family: 'Georgia', 'Times New Roman', serif;
            line-height: 1.6;
            color: #333;
            background: #fff;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        .header {
            padding: 40px 0;
            text-align: center;
            border-bottom: 2px solid #2c3e50;
            margin-bottom: 40px;
        }

        .header h1 {
            font-size: 2.2rem;
            font-weight: 400;
            margin-bottom: 8px;
            color: #2c3e50;
            letter-spacing: 0.5px;
        }

        .header .title {
            font-size: 1.1rem;
            color: #555;
            margin-bottom: 20px;
            font-style: italic;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 25px;
            flex-wrap: wrap;
        }

        .contact-link {
            color: #2c3e50;
            text-decoration: none;
            font-size: 0.9rem;
            transition: color 0.2s ease;
        }

        .contact-link:hover {
            color: #3498db;
        }

        /* Section styling */
        .section {
            margin-bottom: 35px;
        }

        .section h2 {
            font-size: 1.4rem;
            font-weight: 500;
            margin-bottom: 15px;
            color: #2c3e50;
            border-bottom: 1px solid #bdc3c7;
            padding-bottom: 5px;
        }

        /* About */
        .about-content p {
            font-size: 0.95rem;
            margin-bottom: 12px;
            color: #444;
            text-align: justify;
        }

        /* Compact tables */
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 15px 0;
            font-size: 0.9rem;
        }

        th, td {
            padding: 8px 12px;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }

        th {
            background: #f8f9fa;
            font-weight: 600;
            color: #2c3e50;
            font-size: 0.85rem;
        }

        /* Skills in compact format */
        .skills-compact {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin: 15px 0;
        }

        .skill-category {
            background: #f8f9fa;
            padding: 15px;
            border-radius: 4px;
        }

        .skill-category h3 {
            font-size: 1rem;
            margin-bottom: 8px;
            color: #2c3e50;
            font-weight: 600;
        }

        .skill-list {
            font-size: 0.85rem;
            color: #555;
            line-height: 1.4;
        }

        /* Compact projects */
        .projects-compact {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 20px;
            margin: 15px 0;
        }

        .project-item {
            border: 1px solid #ddd;
            padding: 18px;
            border-radius: 4px;
            background: #fafafa;
        }

        .project-item h3 {
            font-size: 1.1rem;
            margin-bottom: 8px;
            color: #2c3e50;
            font-weight: 600;
        }

        .project-item p {
            font-size: 0.85rem;
            color: #555;
            margin-bottom: 10px;
            line-height: 1.4;
        }

        .tech-inline {
            font-size: 0.8rem;
            color: #666;
            margin-bottom: 10px;
            font-style: italic;
        }

        .project-link {
            color: #3498db;
            text-decoration: none;
            font-size: 0.85rem;
            font-weight: 500;
        }

        .project-link:hover {
            text-decoration: underline;
        }

        /* Compact articles */
        .articles-compact {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 15px;
            margin: 15px 0;
        }

        .article-item {
            border-left: 3px solid #3498db;
            padding: 12px 15px;
            background: #f8f9fa;
        }

        .article-item h3 {
            font-size: 1rem;
            margin-bottom: 5px;
            color: #2c3e50;
            font-weight: 600;
        }

        .article-platform {
            font-size: 0.8rem;
            color: #3498db;
            margin-bottom: 8px;
            font-weight: 500;
        }

        .article-item p {
            font-size: 0.85rem;
            color: #555;
            margin-bottom: 8px;
            line-height: 1.3;
        }

        .article-link {
            color: #2c3e50;
            text-decoration: none;
            font-size: 0.8rem;
        }

        .article-link:hover {
            text-decoration: underline;
        }

        /* Compact certifications */
        .cert-compact {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 12px;
            margin: 15px 0;
        }

        .cert-item {
            background: #f8f9fa;
            padding: 12px;
            border-radius: 4px;
            border-left: 3px solid #27ae60;
        }

        .cert-item h4 {
            font-size: 0.95rem;
            margin-bottom: 4px;
            color: #2c3e50;
            font-weight: 600;
        }

        .cert-item p {
            font-size: 0.8rem;
            color: #666;
            margin: 2px 0;
        }

        /* Contact */
        .contact-section {
            text-align: center;
            margin-top: 40px;
            padding: 30px 0;
            border-top: 2px solid #2c3e50;
        }

        .contact-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin-top: 15px;
        }

        .contact-btn {
            background: #2c3e50;
            color: #fff;
            padding: 8px 16px;
            border-radius: 4px;
            text-decoration: none;
            font-weight: 500;
            font-size: 0.9rem;
            transition: background 0.2s ease;
        }

        .contact-btn:hover {
            background: #34495e;
        }

        /* Footer */
        .footer {
            text-align: center;
            padding: 20px 0;
            color: #666;
            font-size: 0.85rem;
            border-top: 1px solid #ddd;
            margin-top: 30px;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .container {
                padding: 0 15px;
            }
            
            .header h1 {
                font-size: 1.8rem;
            }
            
            .contact-info {
                flex-direction: column;
                gap: 10px;
            }
            
            .projects-compact {
                grid-template-columns: 1fr;
            }
            
            .articles-compact {
                grid-template-columns: 1fr;
            }
            
            table {
                font-size: 0.8rem;
            }
            
            th, td {
                padding: 6px 8px;
            }
        }

        @media print {
            body {
                font-size: 12px;
            }
            
            .contact-btn {
                background: #fff;
                color: #000;
                border: 1px solid #000;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <header class="header">
            <h1>Areej Mehboob</h1>
            <p class="title">NLP Researcher | Machine Learning Engineer</p>
            <div class="contact-info">
                <a href="mailto:mehboobareej01@gmail.com" class="contact-link">mehboobareej01@gmail.com</a>
                <a href="https://www.linkedin.com/in/areej-mehboob-396b7a207/" class="contact-link" target="_blank">LinkedIn</a>
                <a href="https://github.com/Areej17-01" class="contact-link" target="_blank">GitHub</a>
                <a href="https://huggingface.co/spaces/AreejMehboob17" class="contact-link" target="_blank">Hugging Face</a>
            </div>
        </header>

       <section class="section">
    <h2>Research Focus</h2>
    <div class="about-content">
        <ul>
            <li><strong>Agentic AI & Program Synthesis</strong> — autonomous agents, multi-agent systems, and code generation agents.</li>

            <li><strong>Retrieval Systems & RAG</strong> — design and optimization of dense, sparse, hybrid, and multimodal retrieval engines; RAG for complex reasoning.</li>

            <li><strong>LLM Evaluation & Benchmarking</strong> — evaluation pipelines, LLM-as-judge methodologies, and benchmark development for code, retrieval, and multimodal tasks.</li>

            <li><strong>Multimodal Document Understanding</strong> — parsing and reasoning across text, tables, and images, with dataset creation and empirical evaluation.</li>
        </ul>
    </div>
</section>

        <!-- Education -->
        <section class="section">
            <h2>Education</h2>
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
                        <td>Bachelor of Science in Computer Science</td>
                        <td>Karachi, Pakistan</td>
                        <td>January 2020 – January 2024</td>
                    </tr>
                </tbody>
            </table>
        </section>

        <!-- Research & Professional Experience -->
        <section class="section">
            <h2>Research & Professional Experience</h2>
            <table>
                <thead>
                    <tr>
                        <th>Position</th>
                        <th>Organization</th>
                        <th>Location</th>
                        <th>Duration</th>
                        <th>Research Focus</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>NLP Researcher</td>
                        <td>Traversaal.ai</td>
                        <td>California, USA (Remote)</td>
                        <td>October 2024 – Present</td>
                        <td>LLM evaluation, AI agents, advanced retrieval systems</td>
                    </tr>
                    <tr>
                        <td>ML Engineer</td>
                        <td>KDYS LAB (Pvt) Ltd</td>
                        <td>Karachi, Pakistan</td>
                        <td>March 2024 – October 2024</td>
                        <td>Agentic RAG systems, LangChain, LLM prompt optimization</td>
                    </tr>
                </tbody>
            </table>
        </section>

        <!-- Technical Expertise -->
        <section class="section">
            <h2>Technical Expertise</h2>
            <div class="skills-compact">
                <div class="skill-category">
                    <h3>AI/ML Frameworks</h3>
                    <div class="skill-list">Python, PyTorch, TensorFlow, Hugging Face Transformers, LangChain, LlamaIndex, CrewAI, Model Context Protocol (MCP)</div>
                </div>
                <div class="skill-category">
                    <h3>Research Specializations</h3>
                    <div class="skill-list">RAG Systems, AI Agents, Large Language Models, Multimodal AI, Vector Databases, LLM Evaluation, Fine-tuning</div>
                </div>
                <div class="skill-category">
                    <h3>Development Tools</h3>
                    <div class="skill-list">FastAPI, Docker, PostgreSQL, Git, Qdrant, Hugging Face Spaces, API Development</div>
                </div>
            </div>
        </section>


        <!-- Publications & Articles -->
        <section class="section">
            <h2>Technical Articles</h2>
            <div class="articles-compact">
                <div class="article-item">
                    <h3>Enabling Agentic AI Through the Model Context Protocol (MCP)</h3>
                    <div class="article-platform">Traversaal.ai Research</div>
                    <p>Analysis of MCP framework for seamless AI agent integration and cross-platform communication in agentic systems.</p>
                    <a href="https://www.notion.so/traversaal-ai/Enabling-Agentic-AI-Through-the-Model-Context-Protocol-MCP-1b59a2e5c4a6803b9df2fb9928944831" target="_blank" class="article-link">Read Article</a>
                </div>
                <div class="article-item">
                    <h3>Multi-Modal Enterprise RAG Architecture from Scratch</h3>
                    <div class="article-platform">Medium</div>
                    <p>Comprehensive guide to building scalable multimodal RAG systems for enterprise applications with advanced retrieval mechanisms.</p>
                    <a href="https://ai.gopubby.com/multi-modal-enterprise-rag-architecture-from-scratch-a3a12df0d055" target="_blank" class="article-link">Read Article</a>
                </div>
                <div class="article-item">
                    <h3>Initialization of Weights in Neural Networks</h3>
                    <div class="article-platform">Medium</div>
                    <p>Technical analysis of weight initialization techniques and their impact on neural network training performance and convergence rates.</p>
                    <a href="https://medium.com/@mehboobareej01/initialization-of-weights-in-neural-network-7243898988de" target="_blank" class="article-link">Read Article</a>
                </div>
                <div class="article-item">
                    <h3>Understanding TF-IDF: Formulas and sklearn Implementation</h3>
                    <div class="article-platform">Medium</div>
                    <p>Mathematical exposition of TF-IDF algorithm with detailed formula derivations and practical scikit-learn implementation.</p>
                    <a href="https://medium.com/@mehboobareej01/understanding-tf-idf-formulas-and-value-returned-output-from-sklearn-library-483cb2b02efa" target="_blank" class="article-link">Read Article</a>
                </div>
                <div class="article-item">
                    <h3>Feature Extraction Essentials for Image Similarity</h3>
                    <div class="article-platform">Medium</div>
                    <p>Technical guide to feature extraction methodologies for enhancing image similarity detection in computer vision applications.</p>
                    <a href="https://medium.com/@mehboobareej01/feature-extraction-essentials-enhancing-image-similarity-with-feature-extraction-f46473869d3a" target="_blank" class="article-link">Read Article</a>
                </div>
            </div>
        </section>

        <!-- Professional Certifications -->
        <section class="section">
            <h2>Professional Certifications</h2>
            <div class="cert-compact">
                <div class="cert-item">
                    <h4>Applied Data Science with Machine Learning</h4>
                    <p>Techmazone</p>
                    <p>2021-2022 • 96 CPD Hours</p>
                </div>
                <div class="cert-item">
                    <h4>LLM Mastery: Complete Guide To Transformers and GenAI</h4>
                    <p>Udemy</p>
                    <p>February 2025 • 7.5 Hours</p>
                </div>
                <div class="cert-item">
                    <h4>Mastering Agentic Design Patterns with Hands-on Projects</h4>
                     <p>Udemy</p>
                    <p>january 2026 • 5.5 Hours</p>
                </div>
                 <div class="cert-item">
                    <h4>Applied Generative AI and Natural Language Processing</h4>
                     <p>Udemy</p>
                    <p>january 2026 • 10 Hours</p>
                </div>
                <div class="cert-item">
                    <h4>Building Applications with Django and PostgreSQL</h4>
                    <p>March 2024 • 5 Hours</p>
                </div>
                <div class="cert-item">
                    <h4>Data Manipulation with Pandas</h4>
                    <p>August 2023 • 4 Hours</p>
                </div>
                <div class="cert-item">
                    <h4>Introduction to Statistics in Python</h4>
                    <p>September 2023 • 4 Hours</p>
                </div>
                <div class="cert-item">
                    <h4>Joining Data with Pandas</h4>
                    <p>September 2023 • 4 Hours</p>
                </div>
            </div>
        </section>

        <!-- Contact -->
        <section class="contact-section">
            <h2>Contact Information</h2>
            <div class="contact-links">
                <a href="https://huggingface.co/spaces/AreejMehboob17" class="contact-btn" target="_blank">Hugging Face</a>
                <a href="https://www.linkedin.com/in/areej-mehboob-396b7a207/" class="contact-btn" target="_blank">LinkedIn</a>
                <a href="mailto:mehboobareej01@gmail.com" class="contact-btn">Email</a>
                <a href="https://medium.com/@mehboobareej01" class="contact-btn" target="_blank">Medium</a>
            </div>
        </section>

        <!-- Footer -->
        <footer class="footer">
            <p>© 2024 Areej Mehboob. All rights reserved.</p>
        </footer>
    </div>
</body>
</html>
