<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Una ang Ginoo - Register</title>
    <link rel="stylesheet" href="css/styles.css">
    <style>
        .register-container {
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(135deg, var(--dark-navy) 0%, var(--navy-blue) 100%);
            padding: 2rem;
            position: relative;
            overflow: hidden;
        }

        .register-container::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(196, 167, 125, 0.1) 1px, transparent 1px);
            background-size: 50px 50px;
            animation: moveBackground 20s linear infinite;
        }

        @keyframes moveBackground {
            0% {
                transform: translate(0, 0);
            }
            100% {
                transform: translate(50px, 50px);
            }
        }

        .register-box {
            background: var(--white);
            padding: 3rem;
            border-radius: 20px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
            max-width: 500px;
            width: 100%;
            position: relative;
            z-index: 1;
            animation: slideUp 0.6s ease-out;
        }

        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .register-header {
            text-align: center;
            margin-bottom: 2rem;
        }

        .register-logo {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .register-header h1 {
            color: var(--navy-blue);
            font-size: 2rem;
            margin-bottom: 0.5rem;
        }

        .register-header p {
            color: var(--text-color);
            font-size: 0.95rem;
            opacity: 0.8;
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1rem;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: var(--navy-blue);
            font-weight: 600;
            font-size: 0.95rem;
        }

        .form-group input,
        .form-group select {
            width: 100%;
            padding: 0.9rem;
            border: 2px solid #e0e0e0;
            border-radius: 10px;
            font-size: 1rem;
            transition: all 0.3s ease;
            font-family: inherit;
        }

        .form-group input:focus,
        .form-group select:focus {
            outline: none;
            border-color: var(--khaki);
            box-shadow: 0 0 0 3px rgba(196, 167, 125, 0.1);
        }

        .terms-agreement {
            display: flex;
            align-items: flex-start;
            gap: 0.5rem;
            margin-bottom: 1.5rem;
            font-size: 0.9rem;
        }

        .terms-agreement input[type="checkbox"] {
            margin-top: 0.2rem;
            cursor: pointer;
        }

        .terms-agreement a {
            color: var(--khaki);
            text-decoration: none;
        }

        .terms-agreement a:hover {
            text-decoration: underline;
        }

        .register-btn {
            width: 100%;
            padding: 1rem;
            background: linear-gradient(135deg, var(--navy-blue), var(--dark-navy));
            color: var(--white);
            border: none;
            border-radius: 10px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            font-family: inherit;
        }

        .register-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 20px rgba(0, 13, 71, 0.4);
        }

        .register-btn:active {
            transform: translateY(0);
        }

        .register-btn:disabled {
            background: #ccc;
            cursor: not-allowed;
            transform: none;
        }

        .divider {
            text-align: center;
            margin: 1.5rem 0;
            position: relative;
        }

        .divider::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 0;
            width: 100%;
            height: 1px;
            background: #e0e0e0;
        }

        .divider span {
            background: var(--white);
            padding: 0 1rem;
            position: relative;
            color: #888;
            font-size: 0.9rem;
        }

        .login-link {
            text-align: center;
            margin-top: 1.5rem;
        }

        .login-link a {
            color: var(--khaki);
            text-decoration: none;
            font-weight: 600;
            transition: color 0.3s ease;
        }

        .login-link a:hover {
            color: var(--navy-blue);
            text-decoration: underline;
        }

        .back-link {
            text-align: center;
            margin-top: 1rem;
        }

        .back-link a {
            color: #888;
            text-decoration: none;
            font-size: 0.9rem;
            transition: color 0.3s ease;
        }

        .back-link a:hover {
            color: var(--navy-blue);
        }

        .alert {
            padding: 0.8rem;
            border-radius: 8px;
            margin-bottom: 1.5rem;
            display: none;
        }

        .alert-success {
            background: #d4edda;
            color: #155724;
            border: 1px solid #c3e6cb;
        }

        .alert-error {
            background: #f8d7da;
            color: #721c24;
            border: 1px solid #f5c6cb;
        }

        .password-strength {
            margin-top: 0.5rem;
            font-size: 0.85rem;
        }

        .strength-bar {
            height: 4px;
            background: #e0e0e0;
            border-radius: 2px;
            margin-top: 0.3rem;
            overflow: hidden;
        }

        .strength-bar-fill {
            height: 100%;
            width: 0%;
            transition: all 0.3s ease;
            border-radius: 2px;
        }

        .strength-weak { background: #dc3545; width: 33%; }
        .strength-medium { background: #ffc107; width: 66%; }
        .strength-strong { background: #28a745; width: 100%; }

        @media (max-width: 600px) {
            .register-box {
                padding: 2rem 1.5rem;
            }

            .register-header h1 {
                font-size: 1.6rem;
            }

            .form-row {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="register-container">
        <div class="register-box">
            <div class="register-header">
                <div class="register-logo">✝️</div>
                <h1>Create Account</h1>
                <p>Join our faith-based community</p>
            </div>

            <div id="alertBox" class="alert"></div>

            <form id="registerForm">
                <div class="form-row">
                    <div class="form-group">
                        <label for="firstName">First Name</label>
                        <input type="text" id="firstName" name="firstName" placeholder="Juan" required>
                    </div>

                    <div class="form-group">
                        <label for="lastName">Last Name</label>
                        <input type="text" id="lastName" name="lastName" placeholder="Dela Cruz" required>
                    </div>
                </div>

                <div class="form-group">
                    <label for="email">Email Address</label>
                    <input type="email" id="email" name="email" placeholder="juan@example.com" required>
                </div>

                <div class="form-group">
                    <label for="username">Username</label>
                    <input type="text" id="username" name="username" placeholder="Choose a username" required>
                </div>

                <div class="form-group">
                    <label for="password">Password</label>
                    <input type="password" id="password" name="password" placeholder="Create a strong password" required>
                    <div class="password-strength">
                        <div class="strength-bar">
                            <div id="strengthBarFill" class="strength-bar-fill"></div>
                        </div>
                        <span id="strengthText"></span>
                    </div>
                </div>

                <div class="form-group">
                    <label for="confirmPassword">Confirm Password</label>
                    <input type="password" id="confirmPassword" name="confirmPassword" placeholder="Re-enter your password" required>
                </div>

                <div class="terms-agreement">
                    <input type="checkbox" id="terms" name="terms" required>
                    <label for="terms">I agree to the <a href="#" onclick="showTerms(event)">Terms of Service</a> and <a href="#" onclick="showPrivacy(event)">Privacy Policy</a></label>
                </div>

                <button type="submit" class="register-btn">Create Account</button>
            </form>

            <div class="divider">
                <span>Already have an account?</span>
            </div>

            <div class="login-link">
                <a href="login.html">Login Here</a>
            </div>

            <div class="back-link">
                <a href="landing.html">← Back to Home</a>
            </div>
        </div>
    </div>

    <script>
        const registerForm = document.getElementById('registerForm');
        const passwordInput = document.getElementById('password');
        const confirmPasswordInput = document.getElementById('confirmPassword');
        const alertBox = document.getElementById('alertBox');
        const strengthBarFill = document.getElementById('strengthBarFill');
        const strengthText = document.getElementById('strengthText');

        // Password strength checker
        passwordInput.addEventListener('input', function() {
            const password = this.value;
            let strength = 0;
            
            if (password.length >= 8) strength++;
            if (password.match(/[a-z]/) && password.match(/[A-Z]/)) strength++;
            if (password.match(/[0-9]/)) strength++;
            if (password.match(/[^a-zA-Z0-9]/)) strength++;

            strengthBarFill.className = 'strength-bar-fill';
            
            if (password.length === 0) {
                strengthText.textContent = '';
                strengthBarFill.style.width = '0%';
            } else if (strength <= 2) {
                strengthBarFill.classList.add('strength-weak');
                strengthText.textContent = 'Weak password';
                strengthText.style.color = '#dc3545';
            } else if (strength === 3) {
                strengthBarFill.classList.add('strength-medium');
                strengthText.textContent = 'Medium strength';
                strengthText.style.color = '#ffc107';
            } else {
                strengthBarFill.classList.add('strength-strong');
                strengthText.textContent = 'Strong password';
                strengthText.style.color = '#28a745';
            }
        });

        // Form submission
        registerForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            const firstName = document.getElementById('firstName').value;
            const lastName = document.getElementById('lastName').value;
            const email = document.getElementById('email').value;
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            const confirmPassword = document.getElementById('confirmPassword').value;
            const terms = document.getElementById('terms').checked;
            
            // Validation
            if (!terms) {
                showAlert('Please agree to the Terms of Service and Privacy Policy', 'error');
                return;
            }
            
            if (password !== confirmPassword) {
                showAlert('Passwords do not match!', 'error');
                return;
            }
            
            if (password.length < 6) {
                showAlert('Password must be at least 6 characters long', 'error');
                return;
            }
            
            // Success
            showAlert('Account created successfully! Redirecting...', 'success');
            
            // Store user data in sessionStorage
            sessionStorage.setItem('username', username);
            sessionStorage.setItem('firstName', firstName);
            sessionStorage.setItem('email', email);
            sessionStorage.setItem('isRegistered', 'true');
            sessionStorage.setItem('isLoggedIn', 'true');
            
            // Redirect to main page after 2 seconds using replace to prevent back navigation
            setTimeout(function() {
                window.location.replace('index.html');
            }, 2000);
        });

        function showAlert(message, type) {
            alertBox.className = 'alert alert-' + type;
            alertBox.textContent = message;
            alertBox.style.display = 'block';
            
            if (type === 'error') {
                setTimeout(function() {
                    alertBox.style.display = 'none';
                }, 4000);
            }
        }

        function showTerms(e) {
            e.preventDefault();
            alert('Terms of Service: This is a demo website for educational purposes. By using this site, you agree to maintain respect and integrity in all interactions.');
        }

        function showPrivacy(e) {
            e.preventDefault();
            alert('Privacy Policy: This is a demo website. No actual data is stored or transmitted. All information entered is stored locally in your browser session only.');
        }
    </script>
</body>
</html>

