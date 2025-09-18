<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Key2SuccessWithBB - Master Bollinger Band Strategies</title>
    <style>
        :root {
            --primary: #1a365d;
            --secondary: #2a4a7f;
            --accent: #e9b949;
            --light: #f5f7fa;
            --dark: #2d3748;
            --success: #38a169;
            --danger: #e53e3e;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Header Styles */
        header {
            background-color: var(--primary);
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--accent);
        }
        
        .logo span {
            color: white;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 1.5rem;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            padding: 0.5rem;
            border-radius: 4px;
        }
        
        nav ul li a:hover {
            color: var(--accent);
            background-color: rgba(255, 255, 255, 0.1);
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(to right, var(--primary), var(--secondary));
            color: white;
            padding: 4rem 0;
            text-align: center;
        }
        
        .hero h1 {
            font-size: 2.8rem;
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 2rem;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--accent);
            color: var(--dark);
            padding: 0.8rem 1.5rem;
            border-radius: 4px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
        }
        
        .btn:hover {
            background-color: #ffd166;
            transform: translateY(-3px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        
        /* Section Styles */
        section {
            padding: 4rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            color: var(--primary);
        }
        
        .section-title h2 {
            font-size: 2.2rem;
            position: relative;
            display: inline-block;
            padding-bottom: 0.5rem;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--accent);
        }
        
        /* Strategy Cards */
        .strategy-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }
        
        .card:hover {
            transform: translateY(-10px);
        }
        
        .card-img {
            height: 200px;
            background-color: #ddd;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
            font-weight: bold;
        }
        
        .card-content {
            padding: 1.5rem;
        }
        
        .card h3 {
            color: var(--primary);
            margin-bottom: 0.8rem;
        }
        
        /* Platform Section */
        .platform-section {
            background-color: #f1f5f9;
        }
        
        .platform-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        /* Testimonials */
        .testimonials {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .testimonial {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 1rem;
        }
        
        .testimonial-author {
            font-weight: 600;
            color: var(--primary);
        }
        
        /* Footer */
        footer {
            background-color: var(--primary);
            color: white;
            padding: 3rem 0 1.5rem;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }
        
        .footer-column h3 {
            color: var(--accent);
            margin-bottom: 1.2rem;
            font-size: 1.3rem;
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 0.8rem;
        }
        
        .footer-column ul li a {
            color: #cbd5e0;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-column ul li a:hover {
            color: white;
        }
        
        .copyright {
            text-align: center;
            padding-top: 1.5rem;
            border-top: 1px solid #2d3748;
            color: #cbd5e0;
        }
        
        /* Page Content */
        .page-content {
            display: none;
            padding: 2rem 0;
        }
        
        .page-content.active {
            display: block;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }
            
            nav ul {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                right: 0;
                background-color: var(--primary);
                flex-direction: column;
                padding: 1rem 0;
            }
            
            nav ul.show {
                display: flex;
            }
            
            nav ul li {
                margin: 0;
                text-align: center;
            }
            
            nav ul li a {
                display: block;
                padding: 1rem;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-content">
            <div class="logo">Key2Success<span>WithBB</span></div>
            <button class="mobile-menu-btn">☰</button>
            <nav>
                <ul id="nav-menu">
                    <li><a href="#" class="nav-link" data-page="home">Home</a></li>
                    <li><a href="#" class="nav-link" data-page="basics">BB Basics</a></li>
                    <li><a href="#" class="nav-link" data-page="tradingview">TradingView</a></li>
                    <li><a href="#" class="nav-link" data-page="ninjatrader">NinjaTrader 8</a></li>
                    <li><a href="#" class="nav-link" data-page="resources">Resources</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Home Page -->
    <div id="home" class="page-content active">
        <!-- Hero Section -->
        <section class="hero">
            <div class="container">
                <h1>Master Bollinger Band Strategies</h1>
                <p>Learn how to effectively use Bollinger Bands on TradingView and NinjaTrader 8 to improve your trading performance and maximize profits.</p>
                <a href="#" class="btn nav-link" data-page="basics">Get Started</a>
            </div>
        </section>

        <!-- Strategies Section -->
        <section>
            <div class="container">
                <div class="section-title">
                    <h2>Popular Bollinger Band Strategies</h2>
                </div>
                <div class="strategy-cards">
                    <div class="card">
                        <div class="card-img">Bollinger Band Squeeze Visualization</div>
                        <div class="card-content">
                            <h3>The Squeeze</h3>
                            <p>Identify periods of low volatility that often precede significant price movements. This strategy helps you anticipate breakout opportunities.</p>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-img">Bollinger Band Bounce Visualization</div>
                        <div class="card-content">
                            <h3>The Bounce</h3>
                            <p>Trade the bounce when price touches or crosses the bands, taking advantage of the mean reversion properties of Bollinger Bands.</p>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-img">Bollinger Band Breakout Visualization</div>
                        <div class="card-content">
                            <h3>Breakout Strategy</h3>
                            <p>Capture strong trending moves when price breaks outside the bands with momentum, indicating potential continuation.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Platform Section -->
        <section class="platform-section">
            <div class="container">
                <div class="section-title">
                    <h2>Platform Integration</h2>
                </div>
                <div class="platform-cards">
                    <div class="card">
                        <div class="card-img">TradingView Bollinger Band Chart</div>
                        <div class="card-content">
                            <h3>TradingView Implementation</h3>
                            <p>Learn how to set up and use Bollinger Bands on TradingView, including custom settings, alerts, and strategy backtesting.</p>
                            <a href="#" class="btn nav-link" data-page="tradingview">Learn More</a>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-img">NinjaTrader 8 Bollinger Band Chart</div>
                        <div class="card-content">
                            <h3>NinjaTrader 8 Implementation</h3>
                            <p>Discover how to implement Bollinger Band strategies in NinjaTrader 8, including automated strategies and indicator customization.</p>
                            <a href="#" class="btn nav-link" data-page="ninjatrader">Learn More</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Testimonials -->
        <section>
            <div class="container">
                <div class="section-title">
                    <h2>Success Stories</h2>
                </div>
                <div class="testimonials">
                    <div class="testimonial">
                        <p class="testimonial-text">"The Bollinger Band squeeze strategy completely transformed my trading. I've consistently identified high-probability breakouts since implementing these techniques."</p>
                        <p class="testimonial-author">- Michael T., Forex Trader</p>
                    </div>
                    <div class="testimonial">
                        <p class="testimonial-text">"Combining Bollinger Bands with volume analysis on NinjaTrader 8 has given me an edge in the markets. The step-by-step guides made implementation easy."</p>
                        <p class="testimonial-author">- Sarah L., Futures Trader</p>
                    </div>
                    <div class="testimonial">
                        <p class="testimonial-text">"The TradingView alerts setup using Bollinger Bands has helped me capture moves I would have otherwise missed. My profitability has increased by 35%."</p>
                        <p class="testimonial-author">- James K., Swing Trader</p>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- BB Basics Page -->
    <div id="basics" class="page-content">
        <div class="container">
            <div class="section-title">
                <h2>Bollinger Band Basics</h2>
            </div>
            
            <h3>What Are Bollinger Bands?</h3>
            <p>Bollinger Bands are a technical analysis tool developed by John Bollinger. They consist of:</p>
            <ul>
                <li><strong>Middle Band:</strong> A simple moving average (typically 20 periods)</li>
                <li><strong>Upper Band:</strong> Middle band + 2 standard deviations</li>
                <li><strong>Lower Band:</strong> Middle band - 2 standard deviations</li>
            </ul>
            
            <h3>Key Concepts</h3>
            <div class="strategy-cards">
                <div class="card">
                    <div class="card-content">
                        <h4>Volatility Measurement</h4>
                        <p>The distance between the bands indicates volatility. Wider bands suggest higher volatility, while narrower bands indicate lower volatility.</p>
                    </div>
                </div>
                <div class="card">
                    <div class="card-content">
                        <h4>Mean Reversion</h4>
                        <p>Prices tend to return to the middle band over time, creating potential reversal opportunities when prices approach the outer bands.</p>
                    </div>
                </div>
                <div class="card">
                    <div class="card-content">
                        <h4>Breakout Identification</h4>
                        <p>When price moves outside the bands, it can signal the beginning of a strong trend, especially when accompanied by high volume.</p>
                    </div>
                </div>
            </div>
            
            <h3>Basic Trading Signals</h3>
            <p>Bollinger Bands generate several types of trading signals:</p>
            <ul>
                <li><strong>Overbought/Oversold:</strong> When price touches or crosses the upper band, it may be overbought. When it touches or crosses the lower band, it may be oversold.</li>
                <li><strong>Squeeze:</strong> When bands narrow significantly, it often precedes a substantial price move.</li>
                <li><strong>Trend Continuation:</strong> During strong trends, price can ride the bands for extended periods.</li>
            </ul>
            
            <a href="#" class="btn nav-link" data-page="tradingview">Next: TradingView Implementation →</a>
        </div>
    </div>

    <!-- TradingView Page -->
    <div id="tradingview" class="page-content">
        <div class="container">
            <div class="section-title">
                <h2>Bollinger Bands on TradingView</h2>
            </div>
            
            <h3>Setting Up Bollinger Bands on TradingView</h3>
            <ol>
                <li>Open the chart for your desired trading instrument</li>
                <li>Click on the "Indicators" button at the top of the chart</li>
                <li>Search for "Bollinger Bands" and select it</li>
                <li>Customize the settings (length, standard deviations) if needed</li>
                <li>Click "OK" to apply to your chart</li>
            </ol>
            
            <h3>Recommended Settings</h3>
            <p>While the default settings (20 period SMA, 2 standard deviations) work well for most traders, you might consider:</p>
            <ul>
                <li><strong>For shorter timeframes:</strong> 10-15 period SMA with 1.5-2 standard deviations</li>
                <li><strong>For longer timeframes:</strong> 20-30 period SMA with 2-2.5 standard deviations</li>
                <li><strong>For volatile markets:</strong> 2.5-3 standard deviations to reduce false signals</li>
            </ul>
            
            <h3>Strategy Implementation</h3>
            <div class="strategy-cards">
                <div class="card">
                    <div class="card-content">
                        <h4>Squeeze Play Alert</h4>
                        <p>Set up alerts when the band width decreases to a certain percentage of the 100-period average, signaling a potential breakout.</p>
                    </div>
                </div>
                <div class="card">
                    <div class="card-content">
                        <h4>Double Bollinger Band Strategy</h4>
                        <p>Use two sets of bands (20,2) and (20,1) to create a "zone" system for more precise entries.</p>
                    </div>
                </div>
            </div>
            
            <h3>Backtesting Strategies</h3>
            <p>TradingView's Strategy Tester allows you to:</p>
            <ol>
                <li>Test Bollinger Band strategies on historical data</li>
                <li>Optimize parameters for specific instruments</li>
                <li>Evaluate performance metrics like win rate and profit factor</li>
            </ol>
            
            <a href="#" class="btn nav-link" data-page="ninjatrader">Next: NinjaTrader 8 Implementation →</a>
        </div>
    </div>

    <!-- NinjaTrader Page -->
    <div id="ninjatrader" class="page-content">
        <div class="container">
            <div class="section-title">
                <h2>Bollinger Bands on NinjaTrader 8</h2>
            </div>
            
            <h3>Adding Bollinger Bands to Your Chart</h3>
            <ol>
                <li>Right-click on your chart and select "Indicators"</li>
                <li>Find and select "Bollinger" from the list of available indicators</li>
                <li>Configure the parameters in the settings dialog:
                    <ul>
                        <li>Period: Number of bars for calculation (default 14)</li>
                        <li>Num Std Dev: Number of standard deviations (default 2)</li>
                        <li>Adjust colors and line styles as preferred</li>
                    </ul>
                </li>
                <li>Click "OK" to apply the indicator</li>
            </ol>
            
            <h3>Automated Strategy Development</h3>
            <p>NinjaTrader's Strategy Builder allows you to create automated Bollinger Band strategies without coding:</p>
            <ol>
                <li>Go to New > Strategy Builder</li>
                <li>Set conditions based on Bollinger Band position (e.g., price crosses below lower band)</li>
                <li>Configure entry and exit rules</li>
                <li>Set stop loss and profit target parameters</li>
                <li>Test and optimize your strategy</li>
            </ol>
            
            <h3>Advanced Customization</h3>
            <p>For more control, you can code custom strategies using NinjaScript:</p>
            <pre style="background: #f5f5f5; padding: 15px; border-radius: 5px; overflow: auto;">
// Example Bollinger Band crossover condition
if (CrossAbove(Close, Bollinger(2, 14).Upper, 1))
{
    EnterLong();
}
else if (CrossBelow(Close, Bollinger(2, 14).Lower, 1))
{
    EnterShort();
}
            </pre>
            
            <h3>Risk Management Techniques</h3>
            <ul>
                <li>Use band width to adjust position sizing (wider bands = smaller position)</li>
                <li>Set stops based on band opposite to your entry</li>
                <li>Combine with other indicators like RSI for confirmation</li>
            </ul>
            
            <a href="#" class="btn nav-link" data-page="resources">Next: Additional Resources →</a>
        </div>
    </div>

    <!-- Resources Page -->
    <div id="resources" class="page-content">
        <div class="container">
            <div class="section-title">
                <h2>Additional Resources</h2>
            </div>
            
            <h3>Recommended Reading</h3>
            <div class="strategy-cards">
                <div class="card">
                    <div class="card-content">
                        <h4>Bollinger on Bollinger Bands</h4>
                        <p>John Bollinger's definitive book explaining the theory and practical application of his bands.</p>
                    </div>
                </div>
                <div class="card">
                    <div class="card-content">
                        <h4>Technical Analysis of the Financial Markets</h4>
                        <p>John J. Murphy's classic text that provides context for using Bollinger Bands within broader technical analysis.</p>
                    </div>
                </div>
            </div>
            
            <h3>Video Tutorials</h3>
            <ul>
                <li>Bollinger Band Basics - Introduction to the indicator</li>
                <li>Advanced Squeeze Strategies - Capturing breakouts</li>
                <li>Combining Bollinger Bands with Other Indicators - RSI, MACD, Volume</li>
            </ul>
            
            <h3>Custom Indicators</h3>
            <p>Enhance your trading with these specialized Bollinger Band variants:</p>
            <ul>
                <li>Bollinger Band Width - Measures the difference between upper and lower bands</li>
                <li>Bollinger Band %B - Shows where price is relative to the bands</li>
                <li>Double Bollinger Band - Uses two sets of bands for more signals</li>
            </ul>
            
            <h3>Practice Exercises</h3>
            <ol>
                <li>Identify 10 squeeze patterns on historical charts</li>
                <li>Paper trade the bounce strategy for one week</li>
                <li>Backtest a simple band breakout strategy on multiple timeframes</li>
            </ol>
            
            <div class="section-title">
                <h2>Start Your Journey Today</h2>
            </div>
            <p style="text-align: center; margin-bottom: 2rem;">Mastering Bollinger Bands takes practice, but with these resources, you're well on your way to trading success.</p>
            <div style="text-align: center;">
                <a href="#" class="btn nav-link" data-page="basics">Begin Learning</a>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Key2SuccessWithBB</h3>
                    <p>Master Bollinger Band strategies for TradingView and NinjaTrader 8 to improve your trading performance.</p>
                </div>
                <div class="footer-column">
                    <h3>Navigation</h3>
                    <ul>
                        <li><a href="#" class="nav-link" data-page="home">Home</a></li>
                        <li><a href="#" class="nav-link" data-page="basics">BB Basics</a></li>
                        <li><a href="#" class="nav-link" data-page="tradingview">TradingView</a></li>
                        <li><a href="#" class="nav-link" data-page="ninjatrader">NinjaTrader 8</a></li>
                        <li><a href="#" class="nav-link" data-page="resources">Resources</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Legal</h3>
                    <ul>
                        <li><a href="#">Disclaimer</a></li>
                        <li><a href="#">Privacy Policy</a></li>
                        <li><a href="#">Terms of Service</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Key2SuccessWithBB. All rights reserved.</p>
                <p>This site is for educational purposes only. Trading involves risk.</p>
            </div>
        </div>
    </footer>

    <script>
        // Simple SPA navigation
        document.addEventListener('DOMContentLoaded', function() {
            const navLinks = document.querySelectorAll('.nav-link');
            const pages = document.querySelectorAll('.page-content');
            const mobileMenuBtn = document.querySelector('.mobile-menu-btn');
            const navMenu = document.getElementById('nav-menu');
            
            // Mobile menu toggle
            mobileMenuBtn.addEventListener('click', function() {
                navMenu.classList.toggle('show');
            });
            
            // Navigation click handler
            navLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    const targetPage = this.getAttribute('data-page');
                    
                    // Hide all pages
                    pages.forEach(page => {
                        page.classList.remove('active');
                    });
                    
                    // Show target page
                    document.getElementById(targetPage).classList.add('active');
                    
                    // Close mobile menu if open
                    navMenu.classList.remove('show');
                    
                    // Scroll to top
                    window.scrollTo(0, 0);
                });
            });
        });
    </script>
</body>
</html>
