<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Selvin Sanjay</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f5f5f5;
            color: #333;
            transition: all 0.3s ease;
        }
        
        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* Login Page Styles */
        .login-container {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: linear-gradient(135deg, #6e8efb, #a777e3);
        }
        
        .login-box {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            width: 350px;
            text-align: center;
        }
        
        .login-box h1 {
            margin-bottom: 30px;
            color: #333;
        }
        
        .form-group {
            margin-bottom: 20px;
            text-align: left;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
        }
        
        .form-group input {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
            box-sizing: border-box;
        }
        
        .login-btn {
            background: #6e8efb;
            color: white;
            border: none;
            padding: 12px 30px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            width: 100%;
            transition: background 0.3s;
        }
        
        .login-btn:hover {
            background: #5a7bf0;
        }
        
        /* Main Content Styles (after login) */
        .main-content {
            display: none;
        }
        
        header {
            background: linear-gradient(135deg, #6e8efb, #a777e3);
            color: white;
            padding: 20px 0;
            text-align: center;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }
        
        nav {
            background: white;
            padding: 15px 0;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        
        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            padding: 0;
            margin: 0;
        }
        
        nav ul li {
            margin: 0 15px;
        }
        
        nav ul li a {
            text-decoration: none;
            color: #333;
            font-weight: bold;
            padding: 8px 15px;
            border-radius: 5px;
            transition: all 0.3s;
        }
        
        nav ul li a:hover {
            background: #6e8efb;
            color: white;
        }
        
        .page {
            display: none;
            padding: 40px 20px;
            min-height: 60vh;
        }
        
        .active {
            display: block;
        }
        
        /* Animation Page Styles */
        .animation-container {
            text-align: center;
            margin-top: 50px;
        }
        
        .animated-text {
            font-size: 36px;
            font-weight: bold;
            color: #6e8efb;
            margin-bottom: 30px;
            opacity: 0;
            transform: translateY(20px);
            animation: fadeInUp 1s forwards;
        }
        
        .animated-box {
            width: 150px;
            height: 150px;
            background: #a777e3;
            margin: 30px auto;
            border-radius: 15px;
            opacity: 0;
            transform: scale(0.5);
            animation: scaleIn 1s 0.5s forwards;
        }
        
        @keyframes fadeInUp {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes scaleIn {
            to {
                opacity: 1;
                transform: scale(1);
            }
        }
        
        /* About Me Page Styles */
        .about-container {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 40px;
        }
        
        .profile-image {
            flex: 1;
            min-width: 300px;
            text-align: center;
        }
        
        .profile-image img {
            width: 100%;
            max-width: 350px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }
        
        .bio {
            flex: 2;
            min-width: 300px;
        }
        
        .bio h1 {
            color: #6e8efb;
            margin-bottom: 20px;
        }
        
        .bio p {
            line-height: 1.8;
            font-size: 17px;
        }
        
        /* Social Links Page Styles */
        .social-links {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 30px;
            margin-top: 50px;
        }
        
        .social-card {
            background: white;
            padding: 30px;
            border-radius: 10px;
            width: 300px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .social-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }
        
        .social-card i {
            font-size: 50px;
            margin-bottom: 20px;
            color: #6e8efb;
        }
        
        .social-card h2 {
            margin-bottom: 15px;
            color: #333;
        }
        
        .social-card a {
            display: inline-block;
            background: #6e8efb;
            color: white;
            padding: 10px 20px;
            border-radius: 5px;
            text-decoration: none;
            margin-top: 15px;
            transition: background 0.3s;
        }
        
        .social-card a:hover {
            background: #5a7bf0;
        }
        
        footer {
            text-align: center;
            padding: 20px;
            background: #333;
            color: white;
            margin-top: 50px;
        }

        /* Error message styling */
        .error-message {
            color: #ff4444;
            margin-top: 10px;
            font-size: 14px;
            display: none;
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <!-- Login Page -->
    <div class="login-container" id="login-page">
        <div class="login-box">
            <h1>Welcome</h1>
            <div class="form-group">
                <label for="username">Username</label>
                <input type="text" id="username" placeholder="Enter your username" required>
            </div>
            <div class="form-group">
                <label for="password">Password</label>
                <input type="password" id="password" placeholder="Enter your password" required>
            </div>
            <div class="error-message" id="error-message"></div>
            <button class="login-btn" onclick="login()">Login</button>
        </div>
    </div>
    
    <!-- Main Content (hidden until login) -->
    <div class="main-content" id="main-content">
        <header>
            <h1>Selvin Sanjay</h1>
            <p>Keyboardist | Engineering Student | Aspiring Entrepreneur</p>
        </header>
        
        <nav>
            <ul>
                <li><a href="#" onclick="showPage('animation-page'); return false;">Home</a></li>
                <li><a href="#" onclick="showPage('about-page'); return false;">About Me</a></li>
                <li><a href="#" onclick="showPage('linkedin-page'); return false;">LinkedIn</a></li>
                <li><a href="#" onclick="showPage('instagram-page'); return false;">Instagram</a></li>
            </ul>
        </nav>
        
        <!-- Animation Page -->
        <div class="page container" id="animation-page">
            <div class="animation-container">
                <div class="animated-text">Welcome to My Personal Website</div>
                <div class="animated-box"></div>
                <p>Use the navigation menu above to explore different sections</p>
            </div>
        </div>
        
        <!-- About Me Page -->
        <div class="page container" id="about-page">
            <div class="about-container">
                <div class="profile-image">
                    <!-- Placeholder for image - make sure to replace with actual image -->
                    <img src="ddd.jpg" alt="Selvin Sanjay" onerror="this.src='https://via.placeholder.com/350x450?text=Selvin+Sanjay'">
                </div>
                <div class="bio">
                    <h1>Hello! I am Selvin Sanjay</h1>
                    <p>
                        A passionate keyboardist and a second-year engineering student at AAA College of Engineering and Technology. 
                        Currently, I am working on a concept for Selvinxstore and planning to launch my own software startup. 
                        Apart from coding, I enjoy graphic design and have created over 200 designs on Canva.
                    </p>
                    <p>
                        In my free time, I love exploring music, technology, and innovation. Looking forward to new opportunities 
                        and collaborations!
                    </p>
                </div>
            </div>
        </div>
        
        <!-- LinkedIn Page -->
        <div class="page container" id="linkedin-page">
            <h2 style="text-align: center; color: #6e8efb;">Connect with me on LinkedIn</h2>
            <div class="social-links">
                <div class="social-card">
                    <i class="fab fa-linkedin"></i>
                    <h2>LinkedIn Profile</h2>
                    <p>Connect with me on LinkedIn to explore professional opportunities</p>
                    <a href="https://www.linkedin.com/in/selvin-sanjay-96325a28b/" target="_blank" rel="noopener noreferrer">Visit LinkedIn</a>
                </div>
            </div>
        </div>
        
        <!-- Instagram Page -->
        <div class="page container" id="instagram-page">
            <h2 style="text-align: center; color: #6e8efb;">Follow me on Instagram</h2>
            <div class="social-links">
                <div class="social-card">
                    <i class="fab fa-instagram"></i>
                    <h2>Instagram Profile</h2>
                    <p>Follow me on Instagram to see my creative side</p>
                    <a href="https://www.instagram.com/__selvin_._?utm_source=ig_web_button_share_sheet&igsh=ZDNlZDc0MzIxNw==" target="_blank" rel="noopener noreferrer">Visit Instagram</a>
                </div>
            </div>
        </div>
        
        <footer>
            <p>&copy; <span id="current-year"></span> Selvin Sanjay. All Rights Reserved.</p>
        </footer>
    </div>
    
    <script>
        // Set current year in footer
        document.getElementById('current-year').textContent = new Date().getFullYear();

        function login() {
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            const errorElement = document.getElementById('error-message');
            
            // Basic validation
            if (!username || !password) {
                errorElement.textContent = 'Please enter both username and password';
                errorElement.style.display = 'block';
                return;
            }
            
            if (username === 'selvinsanjay' && password === '31205') {
                document.getElementById('login-page').style.display = 'none';
                document.getElementById('main-content').style.display = 'block';
                showPage('animation-page');
            } else {
                errorElement.textContent = 'Invalid username or password. Please try again.';
                errorElement.style.display = 'block';
            }
        }
        
        function showPage(pageId) {
            // Hide all pages
            const pages = document.querySelectorAll('.page');
            pages.forEach(page => {
                page.classList.remove('active');
            });
            
            // Show the selected page
            document.getElementById(pageId).classList.add('active');
        }

        // Add keyboard support for login
        document.addEventListener('keypress', function(e) {
            if (e.key === 'Enter' && document.getElementById('login-page').style.display !== 'none') {
                login();
            }
        });

        // Initially show the login page
        document.getElementById('login-page').style.display = 'flex';
    </script>
</body>
</html>
