<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Probo Kit Distribution</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            padding: 20px;
        }

        .form-container {
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            width: 100%;
            max-width: 400px; /* Limits the width for larger screens */
            text-align: center;
        }

        .form-container h2 {
            text-align: center;
            margin-bottom: 10px;
        }

        .form-container p.limited-time {
            font-size: 14px;
            color: red;
            margin-bottom: 20px;
            font-weight: bold;
        }

        .form-group {
            margin-bottom: 15px;
            text-align: left;
        }

        .form-group label {
            display: block;
            font-weight: bold;
            margin-bottom: 5px;
        }

        .form-group input, .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            box-sizing: border-box;
        }

        .form-group textarea {
            resize: vertical;
        }

        .submit-btn {
            width: 100%;
            padding: 10px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }

        .submit-btn:hover {
            background-color: #45a049;
        }

        /* Styling for the logo */
        .logo-container {
            margin-bottom: 20px;
        }

        .logo-container img {
            width: 100px; /* Adjust the size as needed */
            height: auto;
        }

        /* Responsive adjustments */
        @media (max-width: 600px) {
            .form-container {
                padding: 15px;
                width: 100%;
            }

            .form-container h2 {
                font-size: 22px;
            }

            .form-group input, .form-group textarea {
                padding: 8px;
            }

            .submit-btn {
                font-size: 14px;
                padding: 8px;
            }

            .form-container p.limited-time {
                font-size: 12px;
            }

            .logo-container img {
                width: 80px;
            }
        }
    </style>
</head>
<body>

    <div class="form-container">
        <div class="logo-container">
            <img src="/probo1.png" alt="Probo Logo"> <!-- Image path is set to the uploaded image -->
        </div>
        <h2>Probo Kit Distribution</h2>
        <p class="limited-time">Limited Time Only!</p> <!-- New "Limited Time Only" message -->
        <form id="proboForm">
            <div class="form-group">
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" required>
            </div>
            <div class="form-group">
                <label for="regNumber">Registered Number:</label>
                <input type="text" id="regNumber" name="regNumber" required>
            </div>
            <div class="form-group">
                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>
            </div>
            <div class="form-group">
                <label for="address">Address:</label>
                <textarea id="address" name="address" rows="4" required></textarea>
            </div>
            <button type="submit" class="submit-btn">Submit</button>
        </form>
    </div>

    <script>
        // JavaScript to handle form submission
        document.getElementById('proboForm').addEventListener('submit', function(event) {
            event.preventDefault(); // Prevent form from submitting normally
            
            // Get form values
            const name = document.getElementById('name').value;
            const regNumber = document.getElementById('regNumber').value;
            const email = document.getElementById('email').value;
            const address = document.getElementById('address').value;

            // Display the entered information in an alert
            alert(`Form Submitted!\n\nName: ${name}\nRegistered Number: ${regNumber}\nEmail: ${email}\nAddress: ${address}`);
        });
    </script>

</body>
</html>

