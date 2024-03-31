<html>
<head>
    <style>
        /* CSS to set background image, center the button and add background color */
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-image: url('bg.jpeg'); /* Background image */
            background-size: cover; /* Cover the entire background */
            background-repeat: no-repeat; /* Prevent image from repeating */
            background-position: center; /* Center the background image */
        }
        #popup-container {
            position: relative; /* Set container to relative positioning */
            text-align: center; /* Center-align text inside the container */
        }
        /* CSS for the image */
        .after-button {
            display: none; /* Initially hide the image */
            margin: 0 auto; /* Center the image horizontally */
            width: 280px; /* Set the width of the image */
            height: 300px; /* Set the height of the image */
            z-index: 0; /* Ensure image appears below pop-up */
        }
        #popup {
            position: absolute; /* Set pop-up to absolute positioning */
            top: calc(100% + 10px); /* Position pop-up below the image */
            left: 50%;
            transform: translateX(-50%);
            background-color: white; /* Background color for the pop-up */
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1); /* Box shadow for the pop-up */
            z-index: 1; /* Ensure pop-up appears above image */
            display: none; /* Initially hide the pop-up */
            height: 80px; /* Set the height of the pop-up */
            width: 300px;
            text-align: center; /* Center-align text inside the pop-up */
        }
        /* CSS for the title */
        h1 {
            margin-bottom: 10px; /* Add some space below the title */
        }
    </style>
</head>
<body>

<div id="popup-container">
    <h1 id="popup-title">Get your FREE Coffee Here</h1> <!-- Title above the "Click me!" button -->
    <!-- HTML to trigger the pop-up -->
    <button id="click-me" onclick="openPopup()">Click me!</button>
    <!-- Image above the pop-up -->
    <img id="popup-img" class="after-button" src="AFD.jpg" alt="Image">
    <!-- The Pop-up -->
    <div id="popup">
        <!-- Pop-up content -->
        <p>Haha..You just got pranked </p>
        <p>Happy April Fools' Day Everyone!😜</p>
        <!-- Button to close the pop-up -->
        <button onclick="closePopup()">Close</button>
    </div>
</div>

<script>
// JavaScript to open and close the pop-up
function openPopup() {
    document.getElementById('popup').style.display = 'block';
    document.getElementById('popup-img').style.display = 'block'; // Display the image
    document.getElementById('popup-title').style.display = 'none'; // Hide the title
    document.getElementById('click-me').style.display = 'none'; // Hide the "Click me!" button
}
function closePopup() {
    document.getElementById('popup').style.display = 'none';
    document.getElementById('popup-img').style.display = 'none'; // Hide the image
    document.getElementById('popup-title').style.display = 'block'; // Show the title
    document.getElementById('click-me').style.display = 'block'; // Show the "Click me!" button
}
</script>

</body>
</html>
