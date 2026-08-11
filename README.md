# 10xcapitalandcode.github.io
<!DOCTYPE html>
<html lang="en" data-theme="light">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abhinav Mishra - FS Transformation Leader</title>
    <style>
        :root {
            /* Dark Theme */
            --bg-main: #09090b;
            --bg-card: #18181b;
            --text-primary: #fafafa;
            --text-secondary: #a1a1aa;
            --accent: #ea580c;
            --border-color: #27272a;
            --nav-bg: rgba(9, 9, 11, 0.8);
            --icon-color: #fafafa;
            --font-main: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
        }

        [data-theme="light"] {
            /* Light Theme (Default) */
            --bg-main: #ffffff;
            --bg-card: #f4f4f5;
            --text-primary: #09090b;
            --text-secondary: #52525b;
            --accent: #ea580c;
            --border-color: #e4e4e7;
            --nav-bg: rgba(255, 255, 255, 0.8);
            --icon-color: #09090b;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: var(--font-main);
            background-color: var(--bg-main);
            color: var(--text-primary);
            line-height: 1.6;
            -webkit-font-smoothing: antialiased;
            transition: background-color 0.3s ease, color 0.3s ease;
        }

        a {
            color: var(--accent);
            text-decoration: none;
            transition: opacity 0.2s ease;
        }

        a:hover {
            opacity: 0.8;
        }

        /* Navigation */
        nav {
            position: sticky;
            top: 0;
            background: var(--nav-bg);
            backdrop-filter: blur(12px);
            border-bottom: 1px solid var(--border-color);
            z-index: 1000;
            transition: background-color 0.3s ease, border-color 0.3s ease;
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 1.5rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .nav-brand {
            font-weight: 700;
            font-size: 1.25rem;
            letter-spacing: -0.025em;
        }

        .nav-controls {
            display: flex;
            align-items: center;
            gap: 2rem;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
        }

        .nav-links a {
            color: var(--text-secondary);
            font-size: 0.95rem;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--text-primary);
        }

        .theme-toggle {
            background: none;
            border: none;
            cursor: pointer;
            padding: 0.5rem;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            transition: background-color 0.2s ease;
        }

        .theme-toggle:hover {
            background-color: var(--border-color);
        }

        .theme-toggle svg {
            width: 20px;
            height: 20px;
            fill: none;
            stroke: var(--icon-color);
            stroke-width: 2;
            stroke-linecap: round;
            stroke-linejoin: round;
        }

        [data-theme="dark"] .sun-icon { display: none; }
        [data-theme="light"] .moon-icon { display: none; }

        /* Layout constraints */
        main {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        /* Header / Hero Section */
        header {
            padding: 8rem 0 6rem;
            border-bottom: 1px solid var(--border-color);
        }

        .hero-tag {
            color: var(--accent);
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.05em;
            font-size: 0.875rem;
            margin-bottom: 1.5rem;
            display: block;
        }

        h1 {
            font-size: clamp(2.5rem, 6vw, 4.5rem);
            line-height: 1.1;
            letter-spacing: -0.04em;
            margin-bottom: 2rem;
            font-weight: 800;
        }

        h1 span {
            color: var(--text-secondary);
            transition: color 0.3s ease;
        }

        .hero-desc {
            font-size: clamp(1.125rem, 2vw, 1.5rem);
            color: var(--text-secondary);
            max-width: 900px;
            margin-bottom: 4rem;
            line-height: 1.5;
            transition: color 0.3s ease;
        }

        .metrics-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
        }

        .metric {
            display: flex;
            flex-direction: column;
            gap: 0.25rem;
        }

        .metric-value {
            font-size: 2rem;
            font-weight: 700;
            color: var(--text-primary);
        }

        .metric-label {
            font-size: 0.875rem;
            color: var(--text-secondary);
            text-transform: uppercase;
            letter-spacing: 0.05em;
        }

        /* Content Sections */
        section {
            padding: 6rem 0;
            border-bottom: 1px solid var(--border-color);
            transition: border-color 0.3s ease;
        }

        .section-intro {
            max-width: 700px;
            margin-bottom: 4rem;
        }

        .section-tag {
            color: var(--text-secondary);
            font-size: 1rem;
            margin-bottom: 0.5rem;
            display: block;
            text-transform: uppercase;
            letter-spacing: 0.05em;
            font-weight: 600;
        }

        h2 {
            font-size: clamp(2rem, 4vw, 3rem);
            letter-spacing: -0.025em;
            line-height: 1.2;
            margin-bottom: 1.5rem;
        }

        .section-intro p {
            color: var(--text-secondary);
            font-size: 1.125rem;
        }

        /* Grid Layouts */
        .grid-2 {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }

        .card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 16px;
            padding: 3rem;
            transition: background-color 0.3s ease, border-color 0.3s ease;
        }

        .card h3 {
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
            letter-spacing: -0.025em;
        }

        .card p {
            color: var(--text-secondary);
            margin-bottom: 1.5rem;
        }

        .card ul {
            list-style: none;
        }

        .card li {
            position: relative;
            padding-left: 1.5rem;
            margin-bottom: 1rem;
            color: var(--text-secondary);
        }

        .card li::before {
            content: "→";
            position: absolute;
            left: 0;
            color: var(--accent);
        }

        .card li strong {
            color: var(--text-primary);
        }

        /* Background Section Elements */
        .timeline-item {
            margin-bottom: 2.5rem;
            padding-left: 2rem;
            border-left: 2px solid var(--border-color);
            position: relative;
        }

        .timeline-item::before {
            content: "";
            position: absolute;
            left: -7px;
            top: 6px;
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: var(--accent);
        }

        .timeline-date {
            font-size: 0.875rem;
            color: var(--accent);
            font-weight: 600;
            margin-bottom: 0.5rem;
            text-transform: uppercase;
            letter-spacing: 0.05em;
        }

        .timeline-title {
            font-size: 1.25rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            color: var(--text-primary);
        }

        .timeline-subtitle {
            color: var(--text-secondary);
            font-size: 1rem;
            line-height: 1.6;
        }

        /* Contact Section */
        .cta-section {
            text-align: center;
            border-bottom: none;
        }

        .cta-container {
            max-width: 1000px;
            margin: 0 auto;
        }

        .cta-container p {
            color: var(--text-secondary);
            margin-bottom: 2.5rem;
            font-size: 1.125rem;
        }

        .cta-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-block;
            padding: 0.875rem 1.75rem;
            border-radius: 8px;
            font-weight: 600;
            font-size: 1rem;
            transition: transform 0.2s ease, box-shadow 0.2s ease, opacity 0.2s ease;
        }

        .btn:hover {
            transform: translateY(-2px);
        }

        .btn-primary {
            background-color: var(--accent);
            color: #ffffff;
            box-shadow: 0 4px 14px rgba(234, 88, 12, 0.3);
        }

        .btn-primary:hover {
            opacity: 0.9;
        }

        .btn-secondary {
            background-color: transparent;
            border: 1px solid var(--border-color);
            color: var(--text-primary);
        }

        .btn-secondary:hover {
            background-color: var(--bg-card);
        }

        footer {
            padding: 4rem 2rem;
            text-align: center;
            color: var(--text-secondary);
            font-size: 0.875rem;
            border-top: 1px solid var(--border-color);
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            .grid-2 {
                grid-template-columns: 1fr;
            }
            .card {
                padding: 2rem;
            }
        }
    </style>
</head>
<body>

    <nav>
        <div class="nav-container">
            <div class="nav-brand"><a href="#top">Abhinav Mishra</a></div>
            <div class="nav-controls">
                <div class="nav-links">
                    <a href="#modernizing">Modernizing</a>
                    <a href="#building">Building</a>
                    <a href="#transformation">Transforming</a>
                    <a href="#background">Background</a>
                    <a href="#contact">Contact</a>
                </div>
                <button class="theme-toggle" id="theme-toggle" aria-label="Toggle Dark/Light Mode">
                    <svg class="moon-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                        <path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"></path>
                    </svg>
                    <svg class="sun-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                        <circle cx="12" cy="12" r="5"></circle>
                        <line x1="12" y1="1" x2="12" y2="3"></line>
                        <line x1="12" y1="21" x2="12" y2="23"></line>
                        <line x1="4.22" y1="4.22" x2="5.64" y2="5.64"></line>
                        <line x1="18.36" y1="18.36" x2="19.78" y2="19.78"></line>
                        <line x1="1" y1="12" x2="3" y2="12"></line>
                        <line x1="21" y1="12" x2="23" y2="12"></line>
                        <line x1="4.22" y1="19.78" x2="5.64" y2="18.36"></line>
                        <line x1="18.36" y1="5.64" x2="19.78" y2="4.22"></line>
                    </svg>
                </button>
            </div>
        </div>
    </nav>

    <main id="top">
        <header>
            <span class="hero-tag">Transformation & Innovation</span>
            <h1>Modernizing what exists. <span>Transforming the future of Financial Services.</span></h1>
            <p class="hero-desc">I architect, build and modernise enterprise-scale product platforms, execute run-the-bank operational excellence, and enable transformation towards AI-native target operating models for C-suite leaders.</p>

            <div class="metrics-grid">
                <div class="metric">
                    <div class="metric-value">US$30Tn</div>
                    <div class="metric-label">Client Assets Supported</div>
                </div>
                <div class="metric">
                    <div class="metric-value">US$1Bn</div>
                    <div class="metric-label">Path to Savings Created</div>
                </div>
                <div class="metric">
                    <div class="metric-value">US$15M</div>
                    <div class="metric-label">AI Investment Capacity</div>
                </div>
                <div class="metric">
                    <div class="metric-value">20 years</div>
                    <div class="metric-label">Transformation Leadership</div>
                </div>
            </div>
        </header>

        <section id="modernizing">
            <div class="section-intro">
                <span class="section-tag">Legacy Modernization</span>
                <h2>Modernizing trillion-dollar financial systems.</h2>
                <p>Driving the modernization of legacy financial markets and securities platforms at the world's most complex institutions, setting the foundation for AI enablement and immense operational savings.</p>
            </div>

            <div class="grid-2">
                <div class="card">
                    <h3>Enterprise Securities Platforms</h3>
                    <p>Modernized and rationalized core legacy platforms across tier-one global banking institutions.</p>
                    <ul>
                        <li><strong>JPMorgan:</strong> Athena and Evolution platforms.</li>
                        <li><strong>Bank of America:</strong> Quartz platform.</li>
                        <li><strong>Standard Chartered:</strong> Sabre and Cortex platforms.</li>
                    </ul>
                </div>
                <div class="card">
                    <h3>Scale & Systemic Impact</h3>
                    <p>Delivering architectural consolidation that translates directly to the bottom line.</p>
                    <ul>
                        <li><strong>Unprecedented Scale:</strong> Supported over US$30Tn in client assets and US$20Bn in revenue.</li>
                        <li><strong>Billion-Dollar Impact:</strong> Created a path for up to US$1bn savings through operational efficiencies.</li>
                        <li><strong>Value Drivers:</strong> Achieved through process simplification, AI enablement, and application platform rationalization.</li>
                    </ul>
                </div>
            </div>
        </section>

        <section id="building">
            <div class="section-intro">
                <span class="section-tag">AI-Native Product & TOM</span>
                <h2>Building what's next, from zero.</h2>
                <p>Engineering AI-native platforms and advising executive leadership on implementing outcomes-led AI transformations across complex customer value chains.</p>
            </div>

            <div class="grid-2">
                <div class="card">
                    <h3>Value3 & algoCRED</h3>
                    <p>Built algoCRED as an AI-platform for independent, predictive, and automated credit ratings.</p>
                    <ul>
                        <li><strong>Market Intelligence:</strong> Delivering investment research and portfolio risk intelligence for asset and wealth managers in both public and private markets.</li>
                        <li><strong>Award-Winning Excellence:</strong> Received Best FinTech in Capital Markets award across Singapore, India, Switzerland, and the UK.</li>
                        <li><strong>Enterprise Adoption:</strong> Adopted as the core AI platform driving a regulated credit rating agency in Europe and by a leading Asset Manager in Singapore.</li>
                    </ul>
                </div>
                <div class="card">
                    <h3>Enterprise AI Advisory</h3>
                    <p>Advising major financial institutions' leadership on comprehensive Enterprise AI transformation.</p>
                    <ul>
                        <li><strong>Outcomes-Led Approach:</strong> Focusing on measurable ROI when transforming legacy processes into highly efficient agentic workflows.</li>
                        <li><strong>Agnostic Architecture:</strong> Designing target ecosystems that remain both LLM and cloud agnostic for long-term resilience.</li>
                        <li><strong>Value-Chain Integration:</strong> Deploying AI seamlessly across the entire customer value chain to enhance user experience and backend efficiency.</li>
                    </ul>
                </div>
            </div>
        </section>

        <section id="transformation">
            <div class="section-intro">
                <span class="section-tag">Outcome-based Enterprise Transformation across Customer Value Chain</span>
                <h2>Re-architecting the operating model for scale.</h2>
                <p>Leading strategic operational shifts from the boardroom to the technology stack. Enabling thorough diagnostics to rebuild the target operating model for global markets.</p>
            </div>

            <div class="grid-2">
                <div class="card">
                    <h3>Discovery & Diagnostics</h3>
                    <p>Establishing a data-driven baseline before executing transformation, ensuring precision in strategy.</p>
                    <ul>
                        <li><strong>Operating Model Maturity:</strong> Comprehensive assessments to benchmark current-state enterprise architecture.</li>
                        <li><strong>Data Maturity Assessment:</strong> Evaluating data health to enable downstream AI and operational strategies.</li>
                        <li><strong>Process Diagnostics:</strong> Pinpointing bottlenecks, historically improving Banking Operations Productivity by up to 30% within 12 months.</li>
                    </ul>
                </div>
                <div class="card">
                    <h3>Target Operating Model (TOM)</h3>
                    <p>Designing the future state of enterprise banking operations, integrating modern SaaS scalability.</p>
                    <ul>
                        <li><strong>Zero-Based Design:</strong> Rethinking workflows via zero-based process redesign and comprehensive work redesign.</li>
                        <li><strong>AI Readiness:</strong> Establishing robust data strategies to ensure systems are primed for AI adoption.</li>
                        <li><strong>Process, Risk and Controls Taxonomy:</strong> Utilizing comprehensive industry taxonomy blueprints to guide structural transitions and transformation roadmap.</li>
                    </ul>
                </div>
            </div>
        </section>


        <section id="background">
            <div class="section-intro">
                <span class="section-tag">Two Decades of Transformation and Innovation</span>
                <h2>Building the Future of Financial Services</h2>
            </div>

            <div class="grid-2">
                <div>
                    <div class="timeline-item">
                        <div class="timeline-date">JPM, BofA, SCB</div>
                        <div class="timeline-title">Institutional Builder and Operator</div>
                        <div class="timeline-subtitle">Held senior accountability for architecting, building and scaling client-facing product platforms for cross-asset trading, pricing, risk, prime brokerage, and post-trade solutions supporting >US$30Tn in client assets and US$20Bn in global revenue, delivering >US$1Bn in structural efficiencies.</div>
                    </div>

                    <div class="timeline-item">
                        <div class="timeline-date">Value3 AI</div>
                        <div class="timeline-title">FinTech CEO & Chief Product Officer</div>
                        <div class="timeline-subtitle">Built and commercially scaled a proprietary AI-powered credit ratings, investment research & risk intelligence platform for Asset & Wealth managers. Secured the MAS AIDA Grant, attracted VC funding, and earned global recognition (Top Asia FinTech Leader, Best FinTech Award, Most Innovative Fintech Solution).</div>
                    </div>

                    <div class="timeline-item">
                        <div class="timeline-date">PwC Southeast Asia Consulting</div>
                        <div class="timeline-title">Transformation Advisory Leader</div>
                        <div class="timeline-subtitle">Lead FS Strategy & Operations Transformation across ASEAN. Advise Boards, CxO and ExCo leaders on product management, enterprise operating models, platform modernisation, and Agentic AI workflow orchestration to drive business growth, efficiency and resilience at scale.</div>
                    </div>
                </div>

                <div class="card">
                    <h3>Foundations</h3>
                    <ul>
                        <li><strong>Education:</strong> Master of Science in Risk Management from New York University (NYU); Bachelor of Engineering in Information Technology from the University of Mumbai.</li>
                        <li><strong>Industry Recognition:</strong> Recognised amongst Top Asia FinTech Leaders by the Singapore FinTech Association.</li>
                        <li><strong>Grants & Innovation:</strong> Recipient of the AIDA Grant from the Monetary Authority of Singapore (MAS) for Applied AI in Financial Services.</li>
                        <li><strong>Network & Mentorship:</strong> Backed and mentored by prominent industry leaders, including executive sponsorship from angel investor Hsieh Fu Hua and leading academecians like <a href="https://profiles.imperial.ac.uk/m.kacperczyk">Prof. Marcin Kacperczyk</a> from Imperial College London and <a href="https://www.stern.nyu.edu/faculty/bio/thomas-pugel">Prof. Tom Pugel</a> from NYU Stern School of Businenss.</li>
                        <li><strong>Speaking Engagements and Thought Leadership:</strong> Regular speaker on Financial Markets Valuation & Risk Modelling, and Applied AI in Financial Services at industry conferences and FinTech ecosystem.</li>
                    </ul>
                </div>
            </div>
        </section>

        <section id="contact" class="cta-section">
            <div class="cta-container">
                <h2>Let's Connect</h2>
                <p>I work at the intersection of business, product, data and technology.</p>
                <p>Join me in building the future of financial services at scale, <br>an operating model where humans and AI agents co-exist and cooperate effectively. </p>
                <div class="cta-buttons">
                    <a href="https://sg.linkedin.com/in/abhinavpmishra" target="_blank" class="btn btn-primary">Connect on LinkedIn</a>
                    <a href="mailto:abhinav.mishra.nyu@gmail.com" class="btn btn-secondary">Send an Email</a>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <p>Abhinav Mishra &copy; 2026. Building for the future of financial services.</p>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const themeToggle = document.getElementById('theme-toggle');
            const htmlElement = document.documentElement;

            // Check for saved user preference
            const savedTheme = localStorage.getItem('theme');

            // If saved theme exists, apply it. Otherwise, defaults to light mode as set in HTML
            if (savedTheme) {
                htmlElement.setAttribute('data-theme', savedTheme);
            }

            themeToggle.addEventListener('click', () => {
                const currentTheme = htmlElement.getAttribute('data-theme');
                const newTheme = currentTheme === 'dark' ? 'light' : 'dark';

                htmlElement.setAttribute('data-theme', newTheme);
                localStorage.setItem('theme', newTheme);
            });
        });
    </script>
</body>
</html>
