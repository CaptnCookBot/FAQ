<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Captain Cook - FAQ</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #16213e 100%);
            color: #e0e0e0;
            line-height: 1.6;
            min-height: 100vh;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header */
        .header {
            text-align: center;
            padding: 40px 0 60px;
            border-bottom: 2px solid #333;
            margin-bottom: 40px;
        }

        .logo {
            width: 80px;
            height: 80px;
            margin: 0 auto 20px;
            background: linear-gradient(45deg, #00d4ff, #0099cc);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 36px;
            font-weight: bold;
            color: white;
            box-shadow: 0 8px 32px rgba(0, 212, 255, 0.3);
        }

        h1 {
            font-size: 2.5rem;
            margin-bottom: 15px;
            background: linear-gradient(45deg, #00d4ff, #ffffff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .subtitle {
            font-size: 1.2rem;
            color: #888;
            margin-bottom: 30px;
        }

        .intro {
            background: rgba(255, 255, 255, 0.05);
            padding: 20px;
            border-radius: 12px;
            border-left: 4px solid #00d4ff;
            backdrop-filter: blur(10px);
        }

        /* Search Bar */
        .search-container {
            margin-bottom: 40px;
            position: relative;
        }

        .search-input {
            width: 100%;
            padding: 15px 50px 15px 20px;
            background: rgba(255, 255, 255, 0.1);
            border: 2px solid rgba(255, 255, 255, 0.2);
            border-radius: 12px;
            color: white;
            font-size: 16px;
            transition: all 0.3s ease;
        }

        .search-input:focus {
            outline: none;
            border-color: #00d4ff;
            box-shadow: 0 0 20px rgba(0, 212, 255, 0.3);
        }

        .search-input::placeholder {
            color: #888;
        }

        .search-icon {
            position: absolute;
            right: 20px;
            top: 50%;
            transform: translateY(-50%);
            color: #888;
            font-size: 18px;
        }

        /* FAQ Items */
        .faq-item {
            background: rgba(255, 255, 255, 0.05);
            margin-bottom: 20px;
            border-radius: 12px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            overflow: hidden;
            transition: all 0.3s ease;
        }

        .faq-item:hover {
            border-color: rgba(0, 212, 255, 0.5);
            box-shadow: 0 8px 32px rgba(0, 212, 255, 0.1);
        }

        .faq-question {
            padding: 20px;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-weight: 600;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            user-select: none;
        }

        .faq-question:hover {
            background: rgba(0, 212, 255, 0.1);
        }

        .faq-question.active {
            background: rgba(0, 212, 255, 0.15);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .chevron {
            transition: transform 0.3s ease;
            font-size: 18px;
            color: #00d4ff;
        }

        .faq-question.active .chevron {
            transform: rotate(180deg);
        }

        .faq-answer {
            padding: 0 20px;
            max-height: 0;
            overflow: hidden;
            transition: all 0.3s ease;
        }

        .faq-answer.active {
            padding: 20px;
            max-height: 1000px;
        }

        .faq-answer p {
            margin-bottom: 15px;
            color: #ccc;
            line-height: 1.7;
        }

        .faq-answer img {
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            margin: 15px 0;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
        }

        .faq-answer video {
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            margin: 15px 0;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
        }

        .security-tip {
            background: rgba(255, 193, 7, 0.1);
            border-left: 4px solid #ffc107;
            padding: 15px;
            border-radius: 8px;
            margin: 15px 0;
            color: #ffd54f;
        }

        .hidden {
            display: none;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .container {
                padding: 15px;
            }

            h1 {
                font-size: 2rem;
            }

            .faq-question {
                padding: 15px;
                font-size: 1rem;
            }

            .faq-answer.active {
                padding: 15px;
            }
        }

        /* Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }

        ::-webkit-scrollbar-track {
            background: #1a1a1a;
        }

        ::-webkit-scrollbar-thumb {
            background: #333;
            border-radius: 4px;
        }

        ::-webkit-scrollbar-thumb:hover {
            background: #555;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <header class="header">
            <div class="logo">🍳</div>
            <h1>Captain Cook</h1>
            <p class="subtitle">Solana Trading Bot - Frequently Asked Questions</p>
            <div class="intro">
                <p>Welcome to the Captain Cook FAQ! Find answers to common questions about our Solana trading bot. From setup to advanced features, we've got you covered.</p>
            </div>
        </header>

        <!-- Search Bar -->
        <div class="search-container">
            <input type="text" class="search-input" placeholder="Search FAQ..." id="searchInput">
            <span class="search-icon">🔍</span>
        </div>

        <!-- FAQ Items -->
        <div class="faq-container">
            <div class="faq-item" data-keywords="setup start wallet telegram">
                <div class="faq-question">
                    <span>How do I set up the bot?</span>
                    <span class="chevron">▼</span>
                </div>
                <div class="faq-answer">
                    <p>To get started, simply send <strong>/start</strong> in the Captain Cook Telegram bot. A new Solana wallet will be created and linked to your Telegram ID.</p>
                    <img src="/images/setup-guide.png" alt="Setup Guide" onerror="this.style.display='none'">
                </div>
            </div>

            <div class="faq-item" data-keywords="buy token purchase trade">
                <div class="faq-question">
                    <span>How do I buy a token?</span>
                    <span class="chevron">▼</span>
                </div>
                <div class="faq-answer">
                    <p>Use <strong>/buy $TOKEN</strong> or click the "Buy" button when a call is posted. The bot will estimate the slippage and fees before confirming the transaction.</p>
                    <video controls onerror="this.style.display='none'">
                        <source src="/videos/how-to-buy.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video>
                </div>
            </div>

            <div class="faq-item" data-keywords="vip free premium subscription calls">
                <div class="faq-question">
                    <span>What's the difference between VIP and Free calls?</span>
                    <span class="chevron">▼</span>
                </div>
                <div class="faq-answer">
                    <p><strong>Free users</strong> see early low-cap tokens under 100k MC.</p>
                    <p><strong>VIP users</strong> get full access up to 5M MC, with scoring, winrate tracking, and PnL visuals.</p>
                </div>
            </div>

            <div class="faq-item" data-keywords="wallet export phantom backup seed">
                <div class="faq-question">
                    <span>Can I export my wallet and use it in Phantom?</span>
                    <span class="chevron">▼</span>
                </div>
                <div class="faq-answer">
                    <p>Yes — use <strong>/backup</strong> to get your 12-word seed phrase. It's compatible with Phantom, Backpack, or any Solana wallet.</p>
                    <div class="security-tip">
                        <strong>⚠️ Security tip:</strong> Never share your seed phrase with anyone!
                    </div>
                </div>
            </div>

            <div class="faq-item" data-keywords="gains calculate performance ath profit">
                <div class="faq-question">
                    <span>How are gains calculated for each call?</span>
                    <span class="chevron">▼</span>
                </div>
                <div class="faq-answer">
                    <p>The bot tracks the <strong>ATH (All-Time High)</strong> of the token <strong>after the call is posted</strong>. The performance is calculated based on the market cap multiple (x1.5, x2, etc.)</p>
                    <img src="/images/gain-example.png" alt="Gain Calculation Example" onerror="this.style.display='none'">
                </div>
            </div>
        </div>
    </div>

    <script>
        // FAQ Toggle Functionality
        document.addEventListener('DOMContentLoaded', function() {
            const faqQuestions = document.querySelectorAll('.faq-question');
            
            faqQuestions.forEach(question => {
                question.addEventListener('click', function() {
                    const answer = this.nextElementSibling;
                    const isActive = this.classList.contains('active');
                    
                    // Close all other FAQ items
                    faqQuestions.forEach(q => {
                        q.classList.remove('active');
                        q.nextElementSibling.classList.remove('active');
                    });
                    
                    // Toggle current item
                    if (!isActive) {
                        this.classList.add('active');
                        answer.classList.add('active');
                    }
                });
            });

            // Search Functionality
            const searchInput = document.getElementById('searchInput');
            const faqItems = document.querySelectorAll('.faq-item');

            searchInput.addEventListener('input', function() {
                const searchTerm = this.value.toLowerCase();
                
                faqItems.forEach(item => {
                    const question = item.querySelector('.faq-question span').textContent.toLowerCase();
                    const answer = item.querySelector('.faq-answer').textContent.toLowerCase();
                    const keywords = item.dataset.keywords.toLowerCase();
                    
                    if (question.includes(searchTerm) || 
                        answer.includes(searchTerm) || 
                        keywords.includes(searchTerm) ||
                        searchTerm === '') {
                        item.classList.remove('hidden');
                    } else {
                        item.classList.add('hidden');
                    }
                });

                // If searching, show message if no results
                const visibleItems = document.querySelectorAll('.faq-item:not(.hidden)');
                const existingNoResults = document.querySelector('.no-results');
                
                if (visibleItems.length === 0 && searchTerm !== '') {
                    if (!existingNoResults) {
                        const noResults = document.createElement('div');
                        noResults.className = 'no-results';
                        noResults.style.textAlign = 'center';
                        noResults.style.padding = '40px';
                        noResults.style.color = '#888';
                        noResults.innerHTML = '<p>No FAQ items found matching your search.</p>';
                        document.querySelector('.faq-container').appendChild(noResults);
                    }
                } else if (existingNoResults) {
                    existingNoResults.remove();
                }
            });
        });
    </script>
</body>
</html>
