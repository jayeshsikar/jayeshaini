# jayeshaini
this website is made for students to know their performance it shows students attendence, results,doubt and many more
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student ERP App</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #4CAF50;
            color: white;
            padding: 20px;
            text-align: center;
        }

        nav {
            background-color: #333;
            overflow: hidden;
        }

        nav a {
            color: white;
            padding: 14px 20px;
            text-align: center;
            text-decoration: none;
            float: left;
        }

        nav a:hover {
            background-color: #ddd;
            color: black;
        }

        .container {
            display: flex;
            justify-content: space-around;
            margin-top: 20px;
            padding: 20px;
        }

        .dashboard, .courses, .results, .attendance {
            width: 22%;
            background-color: #ffffff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        h2 {
            color: #4CAF50;
        }

        .course-list, .result-list, .attendance-list {
            list-style-type: none;
            padding: 0;
        }

        .course-list li, .result-list li, .attendance-list li {
            background-color: #f9f9f9;
            margin: 10px 0;
            padding: 10px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        .dashboard div {
            margin: 10px 0;
        }

        .login-form input {
            padding: 10px;
            width: 100%;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 5px;
        }

        .login-form button {
            background-color: #4CAF50;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .login-form button:hover {
            background-color: #45a049;
        }

    </style>
</head>
<body>

<header>
    <h1>Student ERP Dashboard</h1>
</header>

<nav>
    <a href="#dashboard">Dashboard</a>
    <a href="#courses">Courses</a>
    <a href="#results">Results</a>
    <a href="#attendance">Attendance</a>
    <a href="#login">Logout</a>
</nav>

<!-- Student Dashboard -->
<div class="container">
    <div class="dashboard" id="dashboard">
        <h2>Student Dashboard</h2>
        <div><strong>Name:</strong> John Doe</div>
        <div><strong>Student ID:</strong> 123456</div>
        <div><strong>Email:</strong> johndoe@example.com</div>
        <div><strong>Department:</strong> Computer Science</div>
    </div>

    <!-- Courses Section -->
    <div class="courses" id="courses">
        <h2>My Courses</h2>
        <ul class="course-list">
            <li>Introduction to Programming</li>
            <li>Web Development Basics</li>
            <li>Data Structures</li>
            <li>Machine Learning</li>
        </ul>
    </div>

    <!-- Results Section -->
    <div class="results" id="results">
        <h2>Exam Results</h2>
        <ul class="result-list">
            <li><strong>Introduction to Programming:</strong> 85%</li>
            <li><strong>Web Development Basics:</strong> 92%</li>
            <li><strong>Data Structures:</strong> 88%</li>
            <li><strong>Machine Learning:</strong> 90%</li>
        </ul>
    </div>

    <!-- Attendance Section -->
    <div class="attendance" id="attendance">
        <h2>Attendance</h2>
        <ul class="attendance-list">
            <li><strong>Introduction to Programming:</strong> 90% attendance</li>
            <li><strong>Web Development Basics:</strong> 95% attendance</li>
            <li><strong>Data Structures:</strong> 85% attendance</li>
            <li><strong>Machine Learning:</strong> 100% attendance</li>
        </ul>
    </div>
</div>

<!-- Login Form (for mock-up purposes) -->
<div class="container" id="login" style="display: none;">
    <div class="login-form">
        <h2>Student Login</h2>
        <form action="#" method="POST" id="loginForm">
            <input type="text" name="username" placeholder="Enter your username" required>
            <input type="password" name="password" placeholder="Enter your password" required>
            <button type="submit">Login</button>
        </form>
    </div>
</div>

<footer style="background-color: #333; color: white; text-align: center; padding: 10px;">
    <p>&copy; 2025 Student ERP System</p>
</footer>

<script>
    // Demo Login functionality (mock-up)
    document.getElementById("loginForm").addEventListener("submit", function(event) {
        event.preventDefault();
        
        const username = event.target.username.value;
        const password = event.target.password.value;

        // Demo credentials check
        if (username === "demoUser" && password === "demoPass123") {
            alert("Login Successful!");
            document.getElementById("login").style.display = "none";
            document.querySelector("nav").style.display = "block";
            document.querySelectorAll(".container > div").forEach(function(div) {
                div.style.display = "block";
            });
        } else {
            alert("Invalid credentials. Please try again.");
        }
    });
</script>

</body>
</html>
