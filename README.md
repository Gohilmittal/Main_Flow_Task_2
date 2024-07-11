# Main_Flow_Task_2
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Website with Dropdowns</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }

        .navbar {
            background-color: #333;
            overflow: hidden;
        }

        .navbar ul {
            list-style-type: none;
            margin: 0;
            padding: 0;
        }

        .navbar li {
            float: left;
        }

        .navbar li a, .dropbtn {
            display: inline-block;
            color: white;
            text-align: center;
            padding: 14px 16px;
            text-decoration: none;
        }

        .navbar li a:hover, .dropdown:hover .dropbtn {
            background-color: #111;
        }

        .dropdown {
            display: inline-block;
        }

        .dropdown-content {
            display: none;
            position: absolute;
            background-color: #f9f9f9;
            min-width: 160px;
            box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
            z-index: 1;
        }

        .dropdown-content a {
            color: black;
            padding: 12px 16px;
            text-decoration: none;
            display: block;
            text-align: left;
        }

        .dropdown-content a:hover {
            background-color: #f1f1f1;
        }

        .dropdown:hover .dropdown-content {
            display: block;
        }

        .content {
            padding: 16px;
        }

        .content > div {
            display: none;
        }
    </style>
    <script>
        function showSection(sectionId) {
            const sections = document.querySelectorAll('.content > div');
            sections.forEach(section => section.style.display = 'none');
            document.getElementById(sectionId).style.display = 'block';
        }
    </script>
</head>
<body onload="showSection('home')">
    <nav class="navbar">
        <ul>
            <li><a href="javascript:void(0)" onclick="showSection('home')">Home</a></li>
            <li class="dropdown">
                <a href="javascript:void(0)" class="dropbtn">Services</a>
                <div class="dropdown-content">
                    <a href="javascript:void(0)" onclick="showSection('webdesign')">Web Design</a>
                    <a href="javascript:void(0)" onclick="showSection('seo')">SEO</a>
                </div>
            </li>
            <li class="dropdown">
                <a href="javascript:void(0)" class="dropbtn">Products</a>
                <div class="dropdown-content">
                    <a href="javascript:void(0)" onclick="showSection('product1')">Product 1</a>
                    <a href="javascript:void(0)" onclick="showSection('product2')">Product 2</a>
                </div>
            </li>
            <li><a href="javascript:void(0)" onclick="showSection('about')">About</a></li>
            <li><a href="javascript:void(0)" onclick="showSection('contact')">Contact</a></li>
        </ul>
    </nav>

    <div class="content">
        <div id="home">
            <h1>Welcome to our Website</h1>
            <p>This is the home page.</p>
        </div>
        <div id="webdesign">
            <h1>Web Design Services</h1>
            <p>We provide high-quality web design services tailored to your needs. Our team of experienced designers ensures your website is visually appealing, user-friendly, and optimized for performance.</p>
        </div>
        <div id="seo">
            <h1>SEO Services</h1>
            <p>Our SEO services help improve your website's visibility on search engines. We use the latest techniques and best practices to increase organic traffic, improve rankings, and drive more conversions.</p>
        </div>
        <div id="product1">
            <h1>Product 1</h1>
            <p>Product 1 is an innovative solution designed to streamline your business processes. With advanced features and user-friendly interfaces, it enhances productivity and efficiency.</p>
        </div>
        <div id="product2">
            <h1>Product 2</h1>
            <p>Product 2 offers cutting-edge technology to meet your business needs. Its robust functionality and scalability make it a perfect choice for businesses of all sizes.</p>
        </div>
        <div id="about">
            <h1>About Us</h1>
            <p>We are a leading company in our industry, committed to providing high-quality products and services. Our team of experts works tirelessly to ensure customer satisfaction and continuous improvement.</p>
        </div>
        <div id="contact">
            <h1>Contact Us</h1>
            <p>For any inquiries, please contact us at:</p>
            <ul>
                <li>Email: gohilmittal@website.com</li>
                <li>Phone: +91 8401768753</li>
                <li>Address: 35 vadodara,Gujarat,India</li>
            </ul>
        </div>
    </div>
</body>
</html>
