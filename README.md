<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Economic Equality Now - Fighting for Fair Wages and Economic Justice</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f8f9fa;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header and Navigation */
        header {
            background: linear-gradient(135deg, #2c3e50, #3498db);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo h1 {
            font-size: 1.8rem;
            font-weight: bold;
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            cursor: pointer;
        }
        
        nav a:hover {
            color: #f39c12;
        }
        
        /* Main Content */
        main {
            margin-top: 80px;
        }
        
        .page {
            display: none;
            min-height: 70vh;
            padding: 2rem 0;
        }
        
        .page.active {
            display: block;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(44, 62, 80, 0.8), rgba(52, 152, 219, 0.8)), 
                        url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 600"><rect fill="%232980b9" width="1200" height="600"/><g fill="%23ecf0f1" opacity="0.1"><circle cx="200" cy="150" r="80"/><circle cx="800" cy="400" r="100"/><circle cx="1000" cy="200" r="60"/></g></svg>');
            background-size: cover;
            color: white;
            text-align: center;
            padding: 4rem 0;
        }
        
        .hero h2 {
            font-size: 3rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }
        
        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .cta-button {
            display: inline-block;
            background: #e74c3c;
            color: white;
            padding: 15px 30px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            font-size: 1.1rem;
            transition: all 0.3s;
            box-shadow: 0 4px 15px rgba(231, 76, 60, 0.3);
        }
        
        .cta-button:hover {
            background: #c0392b;
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(231, 76, 60, 0.4);
        }
        
        /* Stats Section */
        .stats {
            background: white;
            padding: 3rem 0;
            margin: 2rem 0;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            text-align: center;
        }
        
        .stat-item {
            padding: 1.5rem;
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            color: #e74c3c;
            display: block;
        }
        
        .stat-label {
            font-size: 1.1rem;
            color: #666;
            margin-top: 0.5rem;
        }
        
        /* Content Sections */
        .content-section {
            background: white;
            margin: 2rem 0;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .content-section h3 {
            font-size: 2rem;
            color: #2c3e50;
            margin-bottom: 1rem;
            border-bottom: 3px solid #3498db;
            padding-bottom: 0.5rem;
        }
        
        .content-section p {
            margin-bottom: 1rem;
            font-size: 1.1rem;
            line-height: 1.7;
        }
        
        /* Pull Quote */
        .pull-quote {
            background: #ecf0f1;
            border-left: 5px solid #e74c3c;
            padding: 1.5rem;
            margin: 2rem 0;
            font-style: italic;
            font-size: 1.2rem;
            color: #2c3e50;
        }
        
        /* Action Items */
        .action-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .action-item {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            text-align: center;
            transition: transform 0.3s;
        }
        
        .action-item:hover {
            transform: translateY(-5px);
        }
        
        .action-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        
        /* Team Grid */
        .team-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .team-member {
            text-align: center;
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .team-avatar {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            background: linear-gradient(135deg, #3498db, #2c3e50);
            margin: 0 auto 1rem;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            color: white;
        }
        
        /* Footer */
        footer {
            background: #2c3e50;
            color: white;
            text-align: center;
            padding: 2rem 0;
            margin-top: 3rem;
        }
        
        /* Citations */
        .citation {
            font-size: 0.9rem;
            color: #666;
            margin-top: 0.5rem;
        }
        
        .references {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            margin: 2rem 0;
        }
        
        .references ol {
            padding-left: 2rem;
        }
        
        .references li {
            margin-bottom: 1rem;
            line-height: 1.6;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 1rem;
            }
            
            nav ul {
                flex-direction: column;
                gap: 1rem;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <h1>Economic Equality Now</h1>
                </div>
                <nav>
                    <ul>
                        <li><a onclick="showPage('home')">Home</a></li>
                        <li><a onclick="showPage('about')">About</a></li>
                        <li><a onclick="showPage('crisis')">The Crisis</a></li>
                        <li><a onclick="showPage('solutions')">Solutions</a></li>
                        <li><a onclick="showPage('references')">References</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <main>
        <!-- HOME PAGE -->
        <div id="home" class="page active">
            <section class="hero">
                <div class="container">
                    <h2>The Time for Economic Justice is NOW</h2>
                    <p>Millions of hardworking Americans struggle to make ends meet while wealth concentrates at the top. Together, we can build an economy that works for everyone, not just the privileged few.</p>
                    <a href="#" class="cta-button" onclick="showPage('crisis')">Learn About the Crisis</a>
                </div>
            </section>

            <div class="container">
                <section class="stats">
                    <div class="stats-grid">
                        <div class="stat-item">
                            <span class="stat-number">$7.25</span>
                            <div class="stat-label">Federal minimum wage since 2009</div>
                        </div>
                        <div class="stat-item">
                            <span class="stat-number">35%</span>
                            <div class="stat-label">Increase needed to afford basic housing</div>
                        </div>
                        <div class="stat-item">
                            <span class="stat-number">2.2M</span>
                            <div class="stat-label">Full-time workers earning minimum wage</div>
                        </div>
                        <div class="stat-item">
                            <span class="stat-number">$15</span>
                            <div class="stat-label">Living wage needed in most states</div>
                        </div>
                    </div>
                </section>

                <section class="content-section">
                    <h3>Our Mission</h3>
                    <p>Economic Equality Now fights for policies that ensure every working American can afford basic necessities like housing, healthcare, and education. We believe that full-time work should provide a living wage, and that economic opportunity should be accessible to all.</p>
                    
                    <div class="pull-quote">
                        "No one who works full time should have to choose between paying rent and buying groceries. Economic dignity is a fundamental right."
                    </div>
                    
                    <p>Through research, advocacy, and grassroots organizing, we work to create an economy where prosperity is shared, not hoarded by the wealthy few.</p>
                </section>
            </div>
        </div>

        <!-- ABOUT PAGE -->
        <div id="about" class="page">
            <div class="container">
                <section class="content-section">
                    <h3>About Economic Equality Now</h3>
                    <p>Founded in 2020 in response to the growing wealth gap exacerbated by the pandemic, Economic Equality Now emerged from a coalition of economists, labor organizers, and concerned citizens who recognized that our economic system was failing working families.</p>
                    
                    <p>Our organization was born out of the recognition that while corporate profits soared, millions of Americans faced eviction, hunger, and impossible choices between basic necessities. We saw that the problem wasn't just individual hardship, but systemic inequality built into our economic structures.</p>
                    
                    <p>Today, we work with policy makers, community organizations, and grassroots activists to advocate for concrete solutions: raising the minimum wage, strengthening worker protections, and creating pathways to economic mobility for all Americans.</p>
                </section>

                <section class="content-section">
                    <h3>Our Leadership Team</h3>
                    <div class="team-grid">
                        <div class="team-member">
                            <div class="team-avatar">Dr. M</div>
                            <h4>Dr. Maria Rodriguez</h4>
                            <p><strong>Executive Director</strong></p>
                            <p>Labor economist with 15 years of experience studying wage policy and economic inequality. Former advisor to the Department of Labor.</p>
                        </div>
                        <div class="team-member">
                            <div class="team-avatar">J.K.</div>
                            <h4>James Kim</h4>
                            <p><strong>Policy Director</strong></p>
                            <p>Former legislative aide specializing in economic policy. Instrumental in drafting state-level minimum wage legislation.</p>
                        </div>
                        <div class="team-member">
                            <div class="team-avatar">S.J.</div>
                            <h4>Sarah Johnson</h4>
                            <p><strong>Grassroots Coordinator</strong></p>
                            <p>Community organizer with deep roots in labor advocacy. Coordinates our nationwide network of local chapters.</p>
                        </div>
                    </div>
                </section>

                <section class="content-section">
                    <h3>Our Values</h3>
                    <p><strong>Economic Dignity:</strong> Every person deserves to earn enough to live with dignity and security.</p>
                    <p><strong>Data-Driven Advocacy:</strong> Our campaigns are grounded in rigorous economic research and evidence-based policy solutions.</p>
                    <p><strong>Inclusive Growth:</strong> Economic prosperity must be shared across all communities, regardless of race, gender, or geography.</p>
                    <p><strong>Systemic Change:</strong> We address root causes of inequality, not just symptoms.</p>
                </section>
            </div>
        </div>

        <!-- THE CRISIS PAGE -->
        <div id="crisis" class="page">
            <div class="container">
                <section class="content-section">
                    <h3>The Economic Inequality Crisis</h3>
                    <p>The United States faces an unprecedented crisis of economic inequality that threatens the foundation of our democracy and the promise of the American Dream. While productivity has increased dramatically over the past four decades, wages for working families have stagnated, creating a chasm between the wealthy and everyone else.</p>
                    
                    <div class="pull-quote">
                        "The federal minimum wage of $7.25 per hour has not increased since 2009, while the cost of living has risen by over 20% during the same period" (Economic Policy Institute, 2024).
                    </div>
                </section>

                <section class="content-section">
                    <h3>Real Stories, Real Impact</h3>
                    <p><strong>Case Study: Maria's Story</strong></p>
                    <p>Maria works two minimum-wage jobs—one at a fast-food restaurant and another cleaning offices at night. Despite working 65 hours per week, she cannot afford a one-bedroom apartment in her city and lives in a shared room with her two children. Her story is not unique; it represents the reality for millions of Americans.</p>
                    
                    <p>Research from the National Low Income Housing Coalition shows that nowhere in America can a worker afford a modest two-bedroom apartment on minimum wage alone. This housing crisis forces families into overcrowded conditions, long commutes, and impossible financial decisions.</p>
                </section>

                <section class="content-section">
                    <h3>The Numbers Don't Lie</h3>
                    <p>According to the Bureau of Labor Statistics, approximately 2.2 million Americans work full-time for minimum wage. These workers are not primarily teenagers earning spending money—the average age is 35, and many support families.</p>
                    
                    <p>Meanwhile, CEO compensation has grown by 1,460% since 1978, while typical worker compensation has increased by just 18% over the same period (Economic Policy Institute, 2023). This disparity represents not just numbers on a spreadsheet, but a fundamental shift in how economic gains are distributed in our society.</p>
                    
                    <div class="pull-quote">
                        "When the minimum wage fails to provide a living wage, taxpayers end up subsidizing profitable corporations through food stamps, Medicaid, and housing assistance for their underpaid workers."
                    </div>
                </section>

                <section class="content-section">
                    <h3>Why This Matters in 2025</h3>
                    <p>The economic inequality crisis has reached a tipping point that demands immediate action. Post-pandemic inflation has made the purchasing power of minimum wage even weaker, while corporate profits have reached record highs. Without intervention, this trend will continue to hollow out the middle class and undermine economic stability.</p>
                    
                    <p>Young adults face particular challenges, with many unable to afford homeownership or even rent without multiple roommates. This economic stress affects mental health, family formation, and long-term economic growth. A generation locked out of economic opportunity cannot contribute fully to our society's prosperity.</p>
                </section>
            </div>
        </div>

        <!-- SOLUTIONS PAGE -->
        <div id="solutions" class="page">
            <div class="container">
                <section class="content-section">
                    <h3>Solutions That Work</h3>
                    <p>Economic inequality is not inevitable. Countries around the world and states across America have implemented policies that create more equitable economic outcomes while maintaining strong economic growth. The evidence is clear: we can build an economy that works for everyone.</p>
                </section>

                <section class="content-section">
                    <h3>Policy Solutions</h3>
                    <p><strong>Raise the Federal Minimum Wage to $15</strong></p>
                    <p>Multiple economic studies demonstrate that raising the minimum wage to $15 per hour would lift millions out of poverty without significant job losses. States like California and New York have successfully implemented $15 minimum wages with positive economic outcomes.</p>
                    
                    <p><strong>Strengthen Worker Bargaining Power</strong></p>
                    <p>Countries with stronger labor unions have lower inequality and higher social mobility. Supporting collective bargaining rights gives workers a voice in their economic destiny and helps ensure that productivity gains are shared with those who create the value.</p>
                    
                    <p><strong>Invest in Skills and Education</strong></p>
                    <p>Public investment in workforce development, community colleges, and apprenticeship programs creates pathways to middle-class careers. Germany's apprenticeship system provides a model for connecting education with economic opportunity.</p>
                </section>

                <section class="content-section">
                    <h3>Take Action Today</h3>
                    <div class="action-grid">
                        <div class="action-item">
                            <div class="action-icon">📧</div>
                            <h4>Contact Your Representatives</h4>
                            <p>Tell your senators and representatives to support the Raise the Wage Act. Personal stories from constituents make a difference.</p>
                            <a href="#" class="cta-button">Find Your Rep</a>
                        </div>
                        <div class="action-item">
                            <div class="action-icon">🗳️</div>
                            <h4>Vote in Every Election</h4>
                            <p>Local elections often have the biggest impact on economic policy. Research candidates' positions on minimum wage and worker rights.</p>
                            <a href="#" class="cta-button">Voter Guide</a>
                        </div>
                        <div class="action-item">
                            <div class="action-icon">🤝</div>
                            <h4>Join Our Movement</h4>
                            <p>Add your voice to thousands of Americans demanding economic justice. Together, we're stronger.</p>
                            <a href="#" class="cta-button">Sign Up</a>
                        </div>
                    </div>
                </section>

                <section class="content-section">
                    <h3>Success Stories</h3>
                    <p>Change is possible. In 2023, voters in Missouri approved a ballot measure to gradually increase the minimum wage to $15 by 2026. This victory came after years of organizing by workers and advocates who refused to accept that full-time work should mean poverty wages.</p>
                    
                    <p>Similarly, cities across the country have implemented living wage ordinances for city contractors and employees, proving that government can lead by example in creating good jobs that support families.</p>
                    
                    <div class="pull-quote">
                        "When Seattle raised its minimum wage to $15, the local economy grew stronger, not weaker. Higher wages mean more consumer spending, which benefits all businesses" (University of Washington, 2022).
                    </div>
                </section>
            </div>
        </div>

        <!-- REFERENCES PAGE -->
        <div id="references" class="page">
            <div class="container">
                <section class="references">
                    <h3>Works Cited</h3>
                    <ol>
                        <li>Bureau of Labor Statistics. (2024). "Characteristics of Minimum Wage Workers, 2023." U.S. Department of Labor. Retrieved from https://www.bls.gov/opub/reports/minimum-wage/2023/home.htm</li>
                        
                        <li>Cooper, David, and Teresa Kroeger. (2023). "CEO Compensation Has Grown 1,460% Since 1978." Economic Policy Institute. Retrieved from https://www.epi.org/publication/ceo-pay-in-2022/</li>
                        
                        <li>Economic Policy Institute. (2024). "The Federal Minimum Wage Has Been Stuck at $7.25 for Over a Decade." Retrieved from https://www.epi.org/minimum-wage-tracker/</li>
                        
                        <li>Jardim, Ekaterina, et al. (2022). "Minimum Wage Increases and Individual Employment Trajectories." University of Washington. Journal of Labor Economics, 40(4), 825-857.</li>
                        
                        <li>National Low Income Housing Coalition. (2024). "Out of Reach 2024: The High Cost of Housing." Retrieved from https://nlihc.org/oor</li>
                        
                        <li>Reich, Michael, and Anna Godøy. (2023). "Minimum Wage Effects in Low-Wage Areas." Journal of Labor Economics, 41(2), 337-375.</li>
                        
                        <li>Schmitt, John, and Heidi Shierholz. (2023). "Why Does the Minimum Wage Have No Discernible Effect on Employment?" Economic Policy Institute. Retrieved from https://www.epi.org/publication/why-does-the-minimum-wage-have-no-discernible-effect-on-employment/</li>
                        
                        <li>Wiltshire, Jenifer, et al. (2024). "State Minimum Wage Laws: A Comprehensive Analysis." Policy Studies Journal, 52(1), 89-112.</li>
                    </ol>
                </section>

                <section class="content-section">
                    <h3>Additional Resources</h3>
                    <p>For more information about economic inequality and policy solutions, we recommend visiting:</p>
                    <ul>
                        <li>Economic Policy Institute (epi.org)</li>
                        <li>Fight Inequality Alliance (fightinequality.org)</li>
                        <li>National Employment Law Project</li>
                        <li>Center on Budget and Policy Priorities</li>
                    </ul>
                </section>
            </div>
        </div>
    </main>

    <footer>
        <div class="container">
            <p>&copy; 2025 Economic Equality Now. Fighting for economic justice for all Americans.</p>
            <p>Contact us: info@economicequalitynow.org | (555) 123-4567</p>
        </div>
    </footer>

    <script>
        function showPage(pageId) {
            // Hide all pages
            const pages = document.querySelectorAll('.page');
            pages.forEach(page => page.classList.remove('active'));
            
            // Show selected page
            document.getElementById(pageId).classList.add('active');
            
            // Scroll to top
            window.scrollTo(0, 0);
        }
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth'
                    });
                }
            });
        });
    </script>
</body>
</html>
