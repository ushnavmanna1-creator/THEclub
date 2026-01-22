<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Club Registration</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #667eea, #764ba2);
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .container {
            background: white;
            padding: 25px;
            width: 400px;
            border-radius: 10px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.2);
        }

        h2 {
            text-align: center;
            margin-bottom: 20px;
            color: #333;
        }

        label {
            font-weight: bold;
            display: block;
            margin-top: 10px;
        }

        input, select {
            width: 100%;
            padding: 8px;
            margin-top: 5px;
            border-radius: 5px;
            border: 1px solid #ccc;
        }

        .gender {
            margin-top: 5px;
        }

        .gender input {
            width: auto;
        }

        button {
            width: 100%;
            padding: 10px;
            margin-top: 20px;
            background: #667eea;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
        }

        button:hover {
            background: #5a67d8;
        }

        .success {
            color: green;
            text-align: center;
            margin-top: 15px;
            font-weight: bold;
        }
    </style>
</head>
<body>

<div class="container">
    <h2>Club Registration</h2>

    <form id="clubForm">
        <label>Full Name</label>
        <input type="text" id="name" required>

        <label>Email</label>
        <input type="email" id="email" required>

        <label>Phone Number</label>
        <input type="tel" id="phone" required>

        <label>Department</label>
        <input type="text" id="department" required>

        <label>Year</label>
        <select id="year" required>
            <option value="">Select Year</option>
            <option>1st Year</option>
            <option>2nd Year</option>
            <option>3rd Year</option>
            <option>4th Year</option>
        </select>

        <label>Club</label>
        <select id="club" required>
            <option value="">Select Club</option>
            <option>Technical Club</option>
            <option>Cultural Club</option>
            <option>Sports Club</option>
            <option>Music Club</option>
        </select>

        <label>Gender</label>
        <div class="gender">
            <input type="radio" name="gender" required> Male
            <input type="radio" name="gender"> Female
        </div>

        <button type="submit">Register</button>
    </form>

    <div class="success" id="successMsg"></div>
</div>

<script>
    document.getElementById("clubForm").addEventListener("submit", function(e) {
        e.preventDefault();
        document.getElementById("successMsg").innerText =
            "🎉 Registration Successful! Welcome to the club.";
        this.reset();
    });
</script>

</body>
</html>
