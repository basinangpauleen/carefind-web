<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CareFind</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" rel="stylesheet"> <!-- Font Awesome Icons -->
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #ffffff;
            color: #333;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            background-image: url('https://www.example.com/background-image.jpg'); /* Replace with your background image */
            background-size: cover;
            background-position: center;
            transition: background 0.5s ease-in-out;
        }

        .container {
            width: 90%; /* Increased width of the container */
            max-width: 1000px; /* Larger max width for the form section */
            background: rgba(255, 255, 255, 0.9); /* Semi-transparent white background */
            padding: 60px; /* Increased padding for the form */
            border-radius: 20px; /* More rounded corners */
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease-in-out;
            overflow: hidden;
        }

        h1 {
            text-align: center;
            color: #c30010;
            margin-bottom: 30px;
            font-size: 3rem;
            text-transform: uppercase;
            font-weight: bold;
        }

        .hero-text {
            text-align: center;
            font-size: 1.5rem;
            font-weight: bold;
            color: #c30010;
            margin-bottom: 15px;
        }

        .donation-info {
            text-align: center;
            color: #666;
            margin-bottom: 25px;
            font-size: 1.2rem;
        }

        .input-field {
            margin-bottom: 20px;
            position: relative;
        }

        .input-field label {
            font-size: 1.2rem;
            color: #555;
            display: block;
            margin-bottom: 5px;
        }

        .input-field input, .input-field select {
            width: 100%;
            padding: 15px;
            font-size: 1.1rem;
            border-radius: 10px;
            border: 2px solid #ddd;
            transition: all 0.3s ease;
        }

        .input-field input:focus, .input-field select:focus {
            border-color: #c30010;
            outline: none;
            box-shadow: 0 0 10px rgba(195, 0, 16, 0.5);
        }

        .button {
            width: 100%;
            padding: 15px;
            font-size: 1.2rem;
            background-color: #c30010;
            color: white;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        .button:hover {
            background-color: #8e24aa;
        }

        /* Admin Section */
        .admin-section {
            display: admin;
            margin-top: 40px;
            padding: 30px;
            background: #f1f1f1;
            border-radius: 15px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
        }

        .admin-section input {
            padding: 15px;
            width: 100%;
            border: 2px solid #ddd;
            border-radius: 10px;
            margin-bottom: 15px;
            font-size: 1.1rem;
            transition: all 0.3s ease;
        }

        .admin-section input:focus {
            border-color: #c30010;
            outline: none;
            box-shadow: 0 0 10px rgba(195, 0, 16, 0.5);
        }

        .admin-section button {
            padding: 15px;
            width: 100%;
            background-color: #c30010;
            color: white;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            font-size: 1.2rem;
            transition: background-color 0.3s ease;
        }

        .admin-section button:hover {
            background-color: #8e24aa;
        }

        .admin-list {
            margin-top: 20px;
            background: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
            max-height: 300px;
            overflow-y: scroll;
        }

        .admin-list table {
            width: 100%;
            border-collapse: collapse;
        }

        .admin-list table, .admin-list th, .admin-list td {
            border: 1px solid #ddd;
        }

        .admin-list th, .admin-list td {
            padding: 10px;
            text-align: center;
        }

    </style>
</head>
<body>

<div class="container">
    <h1>Blood Donation Form</h1>

    <!-- Hero Message -->
    <div class="hero-text">Be a Hero, Save Lives!</div>
    <div class="donation-info">
        Blood donation is a simple, safe, and effective way to help those in need. Every donation can save up to 3 lives. Donate today and make a difference!
    </div>

    <!-- Blood Donor Form -->
    <form id="donorForm">
        <div class="input-field">
            <label for="name"><i class="fas fa-user icon"></i>Name</label>
            <input type="text" id="name" required>
        </div>

        <div class="input-field">
            <label for="age"><i class="fas fa-calendar-alt icon"></i>Age</label>
            <input type="number" id="age" required>
        </div>

        <div class="input-field">
            <label for="sex"><i class="fas fa-transgender-alt icon"></i>Sex</label>
            <select id="sex" required>
                <option value="Male">Male</option>
                <option value="Female">Female</option>
            </select>
        </div>

        <div class="input-field">
            <label for="address"><i class="fas fa-map-marker-alt icon"></i>Address</label>
            <input type="text" id="address" required>
        </div>

        <div class="input-field">
            <label for="contact"><i class="fas fa-phone icon"></i>Contact Number</label>
            <input type="text" id="contact" required>
        </div>

        <div class="input-field">
            <label for="bloodType"><i class="fas fa-tint icon"></i>Blood Type</label>
            <select id="bloodType" required>
                <option value="A+">A+</option>
                <option value="A-">A-</option>
                <option value="B+">B+</option>
                <option value="B-">B-</option>
                <option value="O+">O+</option>
                <option value="O-">O-</option>
                <option value="AB+">AB+</option>
                <option value="AB-">AB-</option>
            </select>
        </div>

        <button type="button" class="button" id="submitDonor"><i class="fas fa-heart icon"></i>Donate</button>
        <button type="button" class="button" id="submitSell"><i class="fas fa-coins icon"></i>Sell</button>
    </form>

    <!-- Admin Section -->
    <div class="admin-section" id="adminSection">
        <h2>Admin Panel</h2>
        <input type="password" id="adminPassword" placeholder="Enter Admin Password">
        <button type="button" class="button" id="adminLoginButton"><i class="fas fa-sign-in-alt icon"></i>Login</button>

        <!-- List of Donors -->
        <div class="admin-list" id="adminList"></div>
    </div>

</div>

<script>
    // Array to store donor information
    const donors = [];

    // Function to toggle the visibility of hidden details
    function toggleDetails(id) {
        const details = document.getElementById(id);
        // Toggle display between 'none' and 'block'
        if (details.style.display === 'none' || details.style.display === '') {
            details.style.display = 'block';  // Show the details
        } else {
            details.style.display = 'none';  // Hide the details
        }
    }

    // Function to handle the donor form submission
    document.getElementById('submitDonor').addEventListener('click', function() {
        const name = document.getElementById('name').value;
        const age = document.getElementById('age').value;
        const sex = document.getElementById('sex').value;
        const address = document.getElementById('address').value;
        const contact = document.getElementById('contact').value;
        const bloodType = document.getElementById('bloodType').value;

        // Store the donor details in the donors array
        donors.push({ name, age, sex, address, contact, bloodType });

        // Clear the form fields
        document.getElementById('donorForm').reset();
        alert('Thank you for donating!');

        // Optionally, hide the learn-more section or show a confirmation
    });

    // Admin Login functionality
    document.getElementById('adminLoginButton').addEventListener('click', function() {
        const password = document.getElementById('adminPassword').value;
        if (password === 'adminPassword') {
            document.getElementById('adminSection').style.display = 'block';
            showDonorList(); // Display the list of donors
        } else {
            alert('Invalid password. Please try again.');
        }
    });

    // Function to display all donors in the admin panel
    function showDonorList() {
        const adminList = document.getElementById('adminList');
        adminList.innerHTML = `
            <table>
                <thead>
                    <tr>
                        <th>Name</th>
                        <th>Age</th>
                        <th>Sex</th>
                        <th>Address</th>
                        <th>Contact</th>
                        <th>Blood Type</th>
                    </tr>
                </thead>
                <tbody>
                    ${donors.map(donor => `
                        <tr>
                            <td>${donor.name}</td>
                            <td>${donor.age}</td>
                            <td>${donor.sex}</td>
                            <td>${donor.address}</td>
                            <td>${donor.contact}</td>
                            <td>${donor.bloodType}</td>
                        </tr>
                    `).join('')}
                </tbody>
            </table>
        `;
    }
</script>

</body>
</html>
