<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Home Page</title>
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        body, html {
            margin: 0;
            padding: 0;
            height: 100%;
            overflow: hidden;
            display: flex;
            flex-direction: column;
        }
        #full-screen-image {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            object-fit: cover;
        }
        .content {
            flex: 1;
            overflow-y: auto;
        }
        section {
            display: none;
            position: relative;
            background: rgba(0, 0, 0, 0.5);
            color: #fff;
            padding: 20px;
        }
        section.active {
            display: block;
        }
        .navbar {
            z-index: 1;
        }
        footer {
            z-index: 1;
        }
    </style>
</head>
<body>
    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
        <div class="container-fluid">
            <a class="navbar-brand" href="#">Smart Waste Management</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <a class="nav-link" href="#" onclick="showSection('about')">About</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#" onclick="showSection('services')">Services</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#" onclick="showSection('contact')">Contact</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="index.html">Login</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="register.html">Register</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <img id="full-screen-image" src="https://i.pinimg.com/736x/bb/62/94/bb6294c40997975fdc9d02992f5eaa02.jpg" alt="Smart Waste Management">
    <br><br><br>
    <div class="content">
        <!-- About Section -->
        <section id="about" class="active">
            <div class="container">
                <h2 class="text-center">About Us</h2>
                <p>At Smart Waste Management, we are dedicated to transforming waste management into an efficient, sustainable, and technologically-driven process. Our mission is to provide innovative solutions that address the growing challenges of waste disposal and environmental sustainability.</p>
                <p>We combine cutting-edge technologies like Internet of Things (IoT), Artificial Intelligence (AI), and Data Analytics to optimize waste collection, reduce landfill dependency, and promote recycling and reuse. Our services cater to various sectors, including residential, commercial, and industrial waste management.</p>
                <p>Our team of experts works tirelessly to create eco-friendly and sustainable solutions, aiming for cleaner cities, reduced environmental impact, and more efficient waste management practices. We strive to make waste management smarter, reducing operational costs and contributing to a more sustainable future.</p>
                <p>Join us on our journey toward a greener and smarter future. Together, we can make a significant impact in shaping a cleaner, waste-free world.</p>
            </div>
        </section>

        <!-- Services Section -->
        <section id="services" class="active">
            <div class="container">
                <h2 class="text-center">Our Services</h2>
                <p>We offer a wide range of services designed to make waste management smarter, more efficient, and eco-friendly. Whether you need regular waste collection for your home, specialized waste management for your business, or solutions for large-scale industrial waste, we have a service to fit your needs.</p>
                <ul>
                    <li>Residential Waste Collection</li>
                    <li>Commercial Waste Management</li>
                    <li>Industrial Waste Solutions</li>
                    <li>Recycling Services</li>
                    <li>E-Waste Management</li>
                    <li>Waste-to-Energy Solutions</li>
                    <li>Composting Services</li>
                    <li>Smart Technology Services</li>
                    <li>Waste Audit and Analysis</li>
                    <li>Customized Waste Reduction Strategies</li>
                    <li>Sustainability Consulting</li>
                </ul>
            </div>
        </section>
    </div>

    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <h2 class="text-center">Contact Us</h2>
            <form class="mx-auto mt-4" style="max-width: 500px;">
                <div class="mb-3">
                    <label for="name" class="form-label">Name</label>
                    <input type="text" class="form-control" id="name" placeholder="Your Name" required>
                </div>
                <div class="mb-3">
                    <label for="email" class="form-label">Email</label>
                    <input type="email" class="form-control" id="email" placeholder="Your Email" required>
                </div>
                <div class="mb-3">
                    <label for="message" class="form-label">Message</label>
                    <textarea class="form-control" id="message" rows="4" placeholder="Your Message" required></textarea>
                </div>
                <button type="submit" class="btn btn-primary w-100">Submit</button>
            </form>
            <div class="text-center mt-4">
                <p><strong>Address:</strong> NHCE, Bengaluru, India</p>
                <p><strong>Email:</strong> zeeshanali9757@gmail.com</p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-dark text-white text-center py-3">
        <p>&copy; 2024 Smart Waste Management. All rights reserved.</p>
    </footer>

    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>

    <script>
        function showSection(sectionId) {
            // Hide all sections
            const sections = document.querySelectorAll('section');
            sections.forEach(section => section.classList.remove('active'));

            // Show the selected section
            const selectedSection = document.getElementById(sectionId);
            if (selectedSection) {
                selectedSection.classList.add('active');
            }
        }

        // Show the "About" and "Services" sections by default
        document.addEventListener('DOMContentLoaded', () => {
            document.getElementById('about').classList.add('active');
            document.getElementById('services').classList.add('active');
        });
    </script>
</body>
</html>
