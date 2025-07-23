# SecureHER
Women safety app with panic alert and health tracker 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SecureHer - Women's Digital Protection</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #7c3aed;
            --secondary: #3b0764;
            --accent: #f0abfc;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f8fafc;
        }
        
        .gradient-bg {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
        }
        
        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }
        
        .password-meter {
            height: 5px;
            transition: width 0.3s ease;
        }
        
        #strength-indicator {
            transition: all 0.3s ease;
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="gradient-bg text-white shadow-lg">
        <div class="container mx-auto px-6 py-3 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <i class="fas fa-shield-alt text-2xl text-amber-300"></i>
                <span class="font-bold text-xl">SecureHer</span>
            </div>
            <div class="hidden md:flex space-x-8">
                <a href="#" class="hover:text-amber-200">Home</a>
                <a href="#features" class="hover:text-amber-200">Features</a>
                <a href="#tools" class="hover:text-amber-200">Security Tools</a>
                <a href="#about" class="hover:text-amber-200">About</a>
            </div>
            <button class="md:hidden text-white focus:outline-none">
                <i class="fas fa-bars text-2xl"></i>
            </button>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="gradient-bg text-white py-20">
        <div class="container mx-auto px-6 flex flex-col md:flex-row items-center">
            <div class="md:w-1/2 mb-10 md:mb-0">
                <h1 class="text-4xl md:text-5xl font-bold mb-6 leading-tight">
                    Your Digital Safety,<br>
                    <span class="text-amber-300">Our Priority</span>
                </h1>
                <p class="text-lg mb-8">
                    Comprehensive digital protection designed specifically for women's security needs.
                    Take control of your online privacy today.
                </p>
                <button class="bg-amber-400 hover:bg-amber-500 text-purple-900 font-bold py-3 px-8 rounded-full transition duration-300 shadow-lg transform hover:scale-105">
                    Get Protected Now <i class="fas fa-arrow-right ml-2"></i>
                </button>
            </div>
            <div class="md:w-1/2 flex justify-center">
                <img src="https://placehold.co/600x400" alt="Illustration of a woman surrounded by digital security shields and locks with purple and amber tones" class="rounded-lg shadow-2xl"/>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="py-16 bg-white">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl font-bold text-center text-gray-800 mb-12">
                Advanced Protection Features
            </h2>
            <div class="grid md:grid-cols-3 gap-8">
                <!-- Feature 1 -->
                <div class="feature-card bg-white p-8 rounded-lg shadow-md transition duration-300">
                    <div class="text-purple-600 mb-4">
                        <i class="fas fa-lock text-4xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-3">Encrypted Communication</h3>
                    <p class="text-gray-600">
                        Secure end-to-end encryption for all your messages and calls, ensuring private conversations stay private.
                    </p>
                </div>
                
                <!-- Feature 2 -->
                <div class="feature-card bg-white p-8 rounded-lg shadow-md transition duration-300">
                    <div class="text-purple-600 mb-4">
                        <i class="fas fa-user-shield text-4xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-3">Emergency Alerts</h3>
                    <p class="text-gray-600">
                        Instant emergency notifications with location sharing to trusted contacts with a single tap.
                    </p>
                </div>
                
                <!-- Feature 3 -->
                <div class="feature-card bg-white p-8 rounded-lg shadow-md transition duration-300">
                    <div class="text-purple-600 mb-4">
                        <i class="fas fa-mask text-4xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-3">Digital Footprint Control</h3>
                    <p class="text-gray-600">
                        Tools to manage and minimize your online presence, reducing exposure to potential threats.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Security Tools Section -->
    <section id="tools" class="py-16 bg-gray-50">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl font-bold text-center text-gray-800 mb-12">
                Personal Security Tools
            </h2>
            
            <!-- Password Strength Checker -->
            <div class="bg-white rounded-xl shadow-md overflow-hidden mb-10">
                <div class="p-8">
                    <div class="flex items-center mb-6">
                        <i class="fas fa-key text-2xl text-purple-600 mr-3"></i>
                        <h3 class="text-xl font-bold">Password Strength Analyzer</h3>
                    </div>
                    <div class="mb-4">
                        <input type="password" id="password-input" placeholder="Test your password security..." 
                               class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-purple-500">
                        <div class="flex mt-2">
                            <div id="strength-indicator" class="text-sm font-medium"></div>
                            <div class="ml-2" id="strength-score"></div>
                        </div>
                        <div class="w-full bg-gray-200 rounded-full h-2 mt-2">
                            <div id="password-meter" class="password-meter h-2 rounded-full"></div>
                        </div>
                    </div>
                    <ul id="password-feedback" class="text-sm text-gray-600 mt-4 space-y-1"></ul>
                </div>
            </div>
            
            <!-- Security Tips -->
            <div class="grid md:grid-cols-2 gap-8">
                <div class="bg-white p-6 rounded-lg shadow-md">
                    <h3 class="text-xl font-bold mb-4 flex items-center">
                        <i class="fas fa-lightbulb text-amber-500 mr-2"></i>
                        Security Tip
                    </h3>
                    <p class="text-gray-700 mb-3">
                        Always enable two-factor authentication on important accounts. It adds an extra layer of security beyond just passwords.
                    </p>
                    <button class="text-purple-600 font-medium hover:text-purple-800">
                        Learn more about 2FA <i class="fas fa-chevron-right ml-1"></i>
                    </button>
                </div>
                
                <div class="bg-white p-6 rounded-lg shadow-md">
                    <h3 class="text-xl font-bold mb-4 flex items-center">
                        <i class="fas fa-exclamation-triangle text-red-500 mr-2"></i>
                        Red Flags
                    </h3>
                    <ul class="list-disc pl-5 text-gray-700 space-y-1">
                        <li>Requests for sensitive info via email</li>
                        <li>Links with misspelled domain names</li>
                        <li>Too-good-to-be-true offers</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-16 bg-white">
        <div class="container mx-auto px-6">
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-8 md:mb-0 md:pr-12">
                    <img src="https://placehold.co/500x350" alt="Diverse group of women discussing digital security around a laptop" class="rounded-lg shadow-md"/>
                </div>
                <div class="md:w-1/2">
                    <h2 class="text-3xl font-bold text-gray-800 mb-6">
                        About SecureHer
                    </h2>
                    <p class="text-gray-600 mb-4">
                        SecureHer was founded in 2023 to address the unique digital security challenges faced by women worldwide. Our mission is to empower women with knowledge and tools to protect their digital lives.
                    </p>
                    <p class="text-gray-600 mb-6">
                        We believe security shouldn't be complicated. Our team of cybersecurity experts and designers work together to create solutions that are both powerful and accessible.
                    </p>
                    <div class="flex space-x-4">
                        <button class="bg-purple-600 hover:bg-purple-700 text-white px-6 py-2 rounded-lg transition">
                            Our Team
                        </button>
                        <button class="border border-purple-600 text-purple-600 hover:bg-purple-50 px-6 py-2 rounded-lg transition">
                            Contact
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials -->
    <section class="py-16 bg-gray-50">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl font-bold text-center text-gray-800 mb-12">
                What Our Users Say
            </h2>
            <div class="grid md:grid-cols-3 gap-8">
                <!-- Testimonial 1 -->
                <div class="bg-white p-6 rounded-lg shadow-md">
                    <div class="flex items-center mb-4">
                        <img src="https://placehold.co/60x60" alt="Portrait of Maria, a young professional woman" class="rounded-full w-12 h-12 object-cover mr-4"/>
                        <div>
                            <h4 class="font-bold">Maria</h4>
                            <div class="flex text-amber-400">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                            </div>
                        </div>
                    </div>
                    <p class="text-gray-600 italic">
                        "As a frequent traveler, SecureHer gives me peace of mind knowing I can quickly alert my friends if I feel unsafe."
                    </p>
                </div>
                
                <!-- Testimonial 2 -->
                <div class="bg-white p-6 rounded-lg shadow-md">
                    <div class="flex items-center mb-4">
                        <img src="https://placehold.co/60x60" alt="Portrait of Priya, a business woman" class="rounded-full w-12 h-12 object-cover mr-4"/>
                        <div>
                            <h4 class="font-bold">Priya</h4>
                            <div class="flex text-amber-400">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star-half-alt"></i>
                            </div>
                        </div>
                    </div>
                    <p class="text-gray-600 italic">
                        "The digital footprint tools helped me remove personal information from risky data broker sites. Highly recommended!"
                    </p>
                </div>
                
                <!-- Testimonial 3 -->
                <div class="bg-white p-6 rounded-lg shadow-md">
                    <div class="flex items-center mb-4">
                        <img src="https://placehold.co/60x60" alt="Portrait of Aisha, a student" class="rounded-full w-12 h-12 object-cover mr-4"/>
                        <div>
                            <h4 class="font-bold">Aisha</h4>
                            <div class="flex text-amber-400">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                            </div>
                        </div>
                    </div>
                    <p class="text-gray-600 italic">
                        "Finally a security app that explains things clearly! The tutorials helped me secure all my social media accounts."
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="gradient-bg text-white py-12">
        <div class="container mx-auto px-6">
            <div class="grid md:grid-cols-4 gap-8">
                <div class="md:col-span-2">
                    <div class="flex items-center mb-4">
                        <i class="fas fa-shield-alt text-2xl text-amber-300 mr-2"></i>
                        <span class="font-bold text-xl">SecureHer</span>
                    </div>
                    <p class="text-gray-300 mb-4">
                        Empowering women through digital security awareness and protection tools.
                    </p>
                    <div class="flex space-x-4">
                        <a href="#" class="text-white hover:text-amber-300">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                        <a href="#" class="text-white hover:text-amber-300">
                            <i class="fab fa-twitter"></i>
                        </a>
                        <a href="#" class="text-white hover:text-amber-300">
                            <i class="fab fa-instagram"></i>
                        </a>
                        <a href="#" class="text-white hover:text-amber-300">
                            <i class="fab fa-linkedin-in"></i>
                        </a>
                    </div>
                </div>
                
                <div>
                    <h3 class="text-lg font-semibold mb-4">Resources</h3>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-300 hover:text-white">Blog</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white">Guides</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white">Webinars</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white">Community</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="text-lg font-semibold mb-4">Contact</h3>
                    <ul class="space-y-2">
                        <li class="flex items-center">
                            <i class="fas fa-map-marker-alt mr-2"></i>
                            <span class="text-gray-300">123 Security Ave, Digital City</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-phone-alt mr-2"></i>
                            <span class="text-gray-300">+1 (555) SAFE-HER</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-envelope mr-2"></i>
                            <span class="text-gray-300">support@secureher.com</span>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="border-t border-gray-700 mt-8 pt-8 text-center text-gray-400 text-sm">
                <p>© 2023 SecureHer. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Password Strength Checker
        document.getElementById('password-input').addEventListener('input', function(e) {
            const password = e.target.value;
            const strengthIndicator = document.getElementById('strength-indicator');
            const strengthScore = document.getElementById('strength-score');
            const passwordMeter = document.getElementById('password-meter');
            const feedbackList = document.getElementById('password-feedback');
            
            // Reset
            feedbackList.innerHTML = '';
            
            if (password.length === 0) {
                strengthIndicator.textContent = '';
                strengthScore.textContent = '';
                passwordMeter.style.width = '0%';
                passwordMeter.className = 'password-meter h-2 rounded-full';
                return;
            }
            
            // Criteria checks
            let score = 0;
            const feedback = [];
            
            // Length
            if (password.length < 8) {
                feedback.push('<li><i class="fas fa-times text-red-500 mr-1"></i> Should be at least 8 characters</li>');
            } else if (password.length < 12) {
                score += 1;
                feedback.push('<li><i class="fas fa-check text-green-500 mr-1"></i> Minimum length (8+)</li>');
            } else {
                score += 2;
                feedback.push('<li><i class="fas fa-check text-green-500 mr-1"></i> Strong length (12+)</li>');
            }
            
            // Contains numbers
            if (/\d/.test(password)) {
                score += 1;
                feedback.push('<li><i class="fas fa-check text-green-500 mr-1"></i> Contains numbers</li>');
            } else {
                feedback.push('<li><i class="fas fa-times text-red-500 mr-1"></i> Add numbers</li>');
            }
            
            // Contains special chars
            if (/[!@#$%^&*(),.?":{}|<>]/.test(password)) {
                score += 1;
                feedback.push('<li><i class="fas fa-check text-green-500 mr-1"></i> Contains special characters</li>');
            } else {
                feedback.push('<li><i class="fas fa-times text-red-500 mr-1"></i> Add special characters</li>');
            }
            
            // Contains uppercase
            if (/[A-Z]/.test(password)) {
                score += 1;
                feedback.push('<li><i class="fas fa-check text-green-500 mr-1"></i> Contains uppercase letters</li>');
            } else {
                feedback.push('<li><i class="fas fa-times text-red-500 mr-1"></i> Add uppercase letters</li>');
            }
            
            // Contains lowercase
            if (/[a-z]/.test(password)) {
                score += 1;
                feedback.push('<li><i class="fas fa-check text-green-500 mr-1"></i> Contains lowercase letters</li>');
            } else {
                feedback.push('<li><i class="fas fa-times text-red-500 mr-1"></i> Add lowercase letters</li>');
            }
            
            // Determine strength
            let strengthText = '';
            let meterColor = '';
            let meterWidth = '0%';
            
            if (score <= 2) {
                strengthText = 'Weak';
                meterColor = 'bg-red-500';
                meterWidth = '30%';
            } else if (score <= 4) {
                strengthText = 'Moderate';
                meterColor = 'bg-yellow-500';
                meterWidth = '60%';
            } else {
                strengthText = 'Strong';
                meterColor = 'bg-green-500';
                meterWidth = '90%';
            }
            
            strengthIndicator.textContent = 'Strength:';
            strengthScore.textContent = strengthText;
            strengthScore.className = strengthText.toLowerCase();
            passwordMeter.style.width = meterWidth;
            passwordMeter.className = `password-meter h-2 rounded-full ${meterColor}`;
            feedbackList.innerHTML = feedback.join('');
        });
        
        // Mobile menu toggle would go here
    </script>
</body>
</html>

