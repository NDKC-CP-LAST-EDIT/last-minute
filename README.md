
<!DOCTYPE html>
<html>
<head>
    <title>RUOK?</title>
    <script src="data.json"></script>
    <style>
        #password-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.3);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 9999;
        }

        #password-box {
            width: max-content;
            background: #fff;
            padding: 30px;
            border-radius: 4px;
            text-align: center;
        }
    </style>
</head>
<body>
    <div id="password-overlay">
        <div id="password-box">
            <h3>Please enter the password:</h3>
            <input type="password" id="password-input">
            <button onclick="submitPassword()">Submit</button>
        </div>
    </div>

    <div id="content" style="display: none;">
        <html>
        <title>Wellness Scale</title>
        <style type="text/css">
            body {
                font-family: Arial, sans-serif;
                background-color: lightblue;
                margin: 0;
                padding: 0;
                display: flex;
                flex-direction: column;
                align-items: center;
            }

            main {
                flex: 1;
                display: flex;
                justify-content: center;
            }

            form {
                height: fit-content;
                width: 600px;
                max-width: 1920px; /* Set a maximum width for the form */
                background-color: white;
                padding: 50px;
                border-radius: 10px;
                box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
                box-sizing: border-box; /* Add this property to include padding and border in the width */
            }

            label, input, textarea {
                display: flex;
                margin-bottom: 10px;
            }

                input[type="text"], input[type="number"], textarea {
                    width: 100%;
                    border-radius: 5px;
                    border: none;
                    box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
                }

            button {
                display: block;
                margin-top: 5px;
                margin-bottom: 5px;
                padding: 5px 10px;
                background-color: #fff;
                color: black;
                border: 2px solid black;
                border-radius: 15px;
                cursor: pointer;
                transition: background-color 0.2s ease-in-out;
                font-size: 12px;
            }

                button:hover {
                    background-color: #fff;
                    border-color: black;
                }

            #scale-container {
                position: relative;
                display: flex;
                align-items: center;
                height: 20px;
                background-color: lightgray;
                border-radius: 5px;
                overflow: hidden;
            }

            .light {
                height: 100%;
                width: 0;
                border-radius: 5px;
                transition: width 1s ease-in-out;
            }

            .light-1 {
                background-color: #770000;
            }

            .light-2 {
                background-color: #7c0901;
            }

            .light-3 {
                background-color: #821201;
            }

            .light-4 {
                background-color: #871901;
            }

            .light-5 {
                background-color: #8c2001;
            }

            .light-6 {
                background-color: #912601;
            }

            .light-7 {
                background-color: #962c00;
            }

            .light-8 {
                background-color: #9b3200;
            }

            .light-9 {
                background-color: #a03800;
            }

            .light-10 {
                background-color: #a53e00;
            }

            .light-11 {
                background-color: #aa4300;
            }

            .light-12 {
                background-color: #ae4900;
            }

            .light-13 {
                background-color: #b34f00;
            }

            .light-14 {
                background-color: #b75500;
            }

            .light-15 {
                background-color: #bc5b00;
            }

            .light-16 {
                background-color: #c06100;
            }

            .light-17 {
                background-color: #c46700;
            }

            .light-18 {
                background-color: #c86d00;
            }

            .light-19 {
                background-color: #cc7300;
            }

            .light-20 {
                background-color: #d07900;
            }

            .light-21 {
                background-color: #d47f00;
            }

            .light-22 {
                background-color: #d78500;
            }

            .light-23 {
                background-color: #db8b00;
            }

            .light-24 {
                background-color: #de9200;
            }

            .light-25 {
                background-color: #e19800;
            }

            .light-26 {
                background-color: #e49e00;
            }

            .light-27 {
                background-color: #e7a500;
            }

            .light-28 {
                background-color: #eaab00;
            }

            .light-29 {
                background-color: #edb200;
            }

            .light-30 {
                background-color: #efb800;
            }

            .light-31 {
                background-color: #f1bf00;
            }

            .light-32 {
                background-color: #f4c500;
            }

            .light-33 {
                background-color: #f6cc00;
            }

            .light-34 {
                background-color: #d7d300;
            }

            .light-35 {
                background-color: #f9da00;
            }

            .light-36 {
                background-color: #fbe000;
            }

            .light-37 {
                background-color: #fce700;
            }

            .light-38 {
                background-color: #fdee00;
            }

            .light-39 {
                background-color: #fef500;
            }

            .light-40 {
                background-color: #fffc03;
            }

            .light-41 {
                background-color: #faf803;
            }

            .light-42 {
                background-color: #f6f503;
            }

            .light-43 {
                background-color: #f2f103;
            }

            .light-44 {
                background-color: #edee03;
            }

            .light-45 {
                background-color: #e9ea03;
            }

            .light-46 {
                background-color: #e4e703;
            }

            .light-47 {
                background-color: #e0e303;
            }

            .light-48 {
                background-color: #dce003;
            }

            .light-49 {
                background-color: #d7dc03;
            }

            .light-50 {
                background-color: #d3d902;
            }

            .light-51 {
                background-color: #d3d302;
            }

            .light-52 {
                background-color: #d0d300;
            }

            .light-53 {
                background-color: #cdd300;
            }

            .light-54 {
                background-color: #cad400;
            }

            .light-55 {
                background-color: #c7d400;
            }

            .light-56 {
                background-color: #c4d400;
            }

            .light-57 {
                background-color: #c1d400;
            }

            .light-58 {
                background-color: #bed400;
            }

            .light-59 {
                background-color: #bbd400;
            }

            .light-60 {
                background-color: #b8d400;
            }

            .light-61 {
                background-color: #b5d500;
            }

            .light-62 {
                background-color: #b1d500;
            }

            .light-63 {
                background-color: #aed500;
            }

            .light-64 {
                background-color: #abd500;
            }

            .light-65 {
                background-color: #a7d500;
            }

            .light-66 {
                background-color: #a4d500;
            }

            .light-67 {
                background-color: #a0d500;
            }

            .light-68 {
                background-color: #9cd500;
            }

            .light-69 {
                background-color: #99d600;
            }

            .light-70 {
                background-color: #95d600;
            }

            .light-71 {
                background-color: #91d600;
            }

            .light-72 {
                background-color: #8dd600;
            }

            .light-73 {
                background-color: #89d600;
            }

            .light-74 {
                background-color: #85d600;
            }

            .light-75 {
                background-color: #80d600;
            }

            .light-76 {
                background-color: #7cd600;
            }

            .light-77 {
                background-color: #77d600;
            }

            .light-78 {
                background-color: #73d600;
            }

            .light-79 {
                background-color: #6ed600;
            }

            .light-80 {
                background-color: #68d600;
            }

            .light-81 {
                background-color: #63d600;
            }

            .light-82 {
                background-color: #5dd600;
            }

            .light-83 {
                background-color: #57d600;
            }

            .light-84 {
                background-color: #51d600;
            }

            .light-85 {
                background-color: #4ad600;
            }

            .light-86 {
                background-color: #42d600;
            }

            .light-87 {
                background-color: #39d600;
            }

            .light-88 {
                background-color: #2ed600;
            }

            .light-89 {
                background-color: #1fd603;
            }

            .light-90 {
                background-color: #03d608;
            }

            .light-91 {
                background-color: #03da09;
            }

            .light-92 {
                background-color: #03de0a;
            }

            .light-93 {
                background-color: #03e20a;
            }

            .light-94 {
                background-color: #04e60b;
            }

            .light-95 {
                background-color: #04ea0c;
            }

            .light-96 {
                background-color: #04ee0d;
            }

            .light-97 {
                background-color: #04f30e;
            }

            .light-98 {
                background-color: #04f70e;
            }

            .light-99 {
                background-color: #04fb0f;
            }

            .light-100 {
                background-color: #04ff10;
            }


            #scale-percentage {
                position: absolute;
                top: 50%;
                left: 0;
                transform: translateX(-100%) translateY(-50%);
                font-weight: bold;
                transition: left 1s ease-in-out;
            }

            .input-container {
                position: relative;
                display: flex;
                align-items: center;
                border-radius: 15px;
                flex-wrap: wrap;
            }

            .info-icon {
                position: relative;
                top: -5.99px;
                right: 0;
                margin-left: 5px;
                cursor: pointer;
                padding: 5px;
            }

                .info-icon::after {
                    content: '🛈';
                    font-size: 20px;
                }

            .dialogue-box {
                position: relative;
                top: -280px;
                right: -150px; /* Adjust this value to align the dialogue box properly */
                width: 500px;
                padding: 10px;
                background-color: #fff;
                border: 1px solid #ccc;
                border-radius: 5px;
                box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
                display: none;
                z-index: 2;
                font-size: 12px;
            }

            .info-icon.active + .dialogue-box {
                display: block;
            }

            .submit-container {
                display: flex;
                justify-content: center;
                padding: 0 50px; /* Add 50px space on both sides */
            }

                .submit-container input[type="submit"] {
                    display: block;
                    margin-top: 100px;
                    margin-bottom: 50px;
                    padding: 5px 10px;
                    background-color: lightblue;
                    color: white;
                    border: none;
                    border-radius: 5px;
                    cursor: pointer;
                    transition: background-color 0.2s ease-in-out;
                }

            /* Responsive Styles */

            @media only screen and (max-width: 600px) {
                form {
                    width: 70%; /* Adjust the width for smaller screens */
                }
            }

            .gif-container {
                position: fixed;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                width: 500px;
                height: 500px;
                background-color: #fff;
                border: 2px solid black;
                border-radius: 25px;
                display: none;
                z-index: 9999;
            }

            .gif {
                display: block;
                width: 100%;
                height: 100%;
                object-fit: contain;
            }

            .collapsible {
                cursor: pointer;
                padding: 10px;
                background-color: white;
                color: black;
                border: 2px solid black;
                border-radius: 5px;
                margin-bottom: 10px;
            }

            .content {
                display: none;
                padding: 10px;
                font-size: 12px;
                border: 2px solid black;
            }

                .content.active {
                    display: block;
                    border: 2px solid black;
                }
        </style>
        </head>
        <body>
            <header>
                <h1>Wellness Scale</h1>
            </header>

            <main>
                <form>
                    <h3>Wellness Information:</h3>
                    <div class="collapsible" onclick="toggleBMI()">BMI:<p id="bmi"></p></div>
                    <div class="content">
                        <label for="age">Age:</label>
                        <input type="number" id="age" name="age" oninput="validateNumericInput(this)">
                        <label for="gender">Gender:</label>
                        <select id="gender" name="gender">
                            <option value="male">Male</option>
                            <option value="female">Female</option>
                        </select>
                        <label for="height">Height (in m):</label>
                        <input type="text" step="0.01" id="height" name="height" oninput="validateNumericInput(this)">
                        <label for="weight">Weight (in kg):</label>
                        <input type="text" step="0.01" id="weight" name="weight" oninput="validateNumericInput(this)">
                        <button type="button" id="calculate-bmi-button" value="Calculate BMI" onclick="calculateBMI()">Calculate BMI</button>

                    </div>
                    <div class="input-container">
                        <label for="activities">Recent activities:</label>
                        <div class="info-icon" onclick="showActivitiesInfo(this)"></div>
                    </div>
                    <div class="input-container">
                        <select id="activities-select" name="activities">
                            <option value="20">Sedentary/Low Intensity</option>
                            <option value="40">Light Intensity</option>
                            <option value="60">Moderate Intensity</option>
                            <option value="80">Vigorous Intensity</option>
                            <option value="100">High Intensity</option>
                        </select>
                    </div>
                    <div class="input-container">
                        <label for="food-intake">Recent food intake:</label>
                        <div class="info-icon" onclick="showInfo(this)"></div>
                    </div>
                    <select id="food-intake" name="food-intake">
                        <option value="20">Unhealthy</option>
                        <option value="40">Slightly unhealthy</option>
                        <option value="60">Neutral</option>
                        <option value="80">Slightly healthy</option>
                        <option value="100">Healthy</option>
                    </select>
                    <div class="input-container">
                        <label for="water">Water Intake:</label>
                        <div class="info-icon" onclick="showWaterInfo(this)"></div>
                    </div>
                    <div class="input-container">
                        <!-- Move the input container below the label container -->
                        <select id="water-select" name="water">
                            <option value="20">Insufficient</option>
                            <option value="40">Inadequate</option>
                            <option value="60">Minimal</option>
                            <option value="80">Optimal</option>
                            <option value="100">Recommended</option>
                        </select>
                    </div>
                    <div class="input-container">
                        <label for="sleep">Amount of sleep:</label>
                        <div class="info-icon" onclick="showSleepInfo(this)"></div>
                    </div>
                    <select id="sleep" name="sleep">
                        <option value="20">Insufficient</option>
                        <option value="40">Inadequate</option>
                        <option value="60">Minimal</option>
                        <option value="80">Optimal</option>
                        <option value="100">Recommended</option>
                    </select>
                    <div class="input-container">
                        <label for="social-interactions">Amount of social interactions:</label>
                        <div class="info-icon" onclick="showInteractionInfo(this)"></div>
                    </div>
                    <select id="social-interactions" name="social-interactions">
                        <option value="20">Isolated</option>
                        <option value="40">Limited</option>
                        <option value="60">Moderate</option>
                        <option value="80">Active</option>
                        <option value="100">Extensive</option>
                    </select>
                    <br><br><br><input type="submit" value="Submit">
                    <h3>Wellness Scale:</h3>
                    <div id="scale-container">
                        <div class="light"></div>
                        <div id="scale-percentage"></div>
                    </div>
                    <div id="water-info" class="dialogue-box" style="top: -320px; right: -135px;">
                        <p>
                            Insufficient: Below recommended daily water intake.
                            <br>

                            Inadequate: Not enough water for proper hydration.
                            <br>

                            Minimal: Bare minimum water intake.
                            <br>

                            Optimal: Ideal water intake for optimal hydration.
                            <br>

                            Recommended: Suggested daily water intake for good hydration.
                            <br>
                        </p>
                    </div>
                    <div id="interactions-info" class="dialogue-box" style="top: -200px; right: -235px;">
                        <p>
                            Isolated: Minimal or no social interaction, feeling disconnected from others.
                            <br>
                            Limited: Infrequent or occasional social interactions with a small circle of acquaintances or friends.
                            <br>
                            Moderate: Regular social interactions with a moderate-sized social circle, engaging in social activities and maintaining connections.
                            <br>
                            Active: Frequent and meaningful social interactions with a diverse group of individuals, actively participating in social events, and maintaining strong relationships.
                            <br>
                            Extensive: Highly active and extensive social interactions, having a wide network of relationships, and regularly engaging in various social activities and events.
                            <br>
                        </p>
                    </div>
                    <div id="activities-info" class="dialogue-box" style="top: -455px; right: -155px;">
                        <p>
                            Sedentary: Minimal physical activity, mostly sitting or lying down.
                            <br>
                            Light: Low-intensity activities like walking or casual cycling.
                            <br>
                            Moderate: Activities that elevate heart rate and breathing, like brisk walking or swimming.
                            <br>
                            Vigorous: High-intensity exercises like running or intense aerobics.
                            <br>
                            High Intensity: Maximum effort exercises like sprinting or heavy weightlifting.
                            <br>
                        </p>
                    </div>

                    <div id="info-text" class="dialogue-box" style="top: -375px; right: -175px;">
                        <p>
                            Unhealthy: Dominated by processed and unhealthy foods, lacking in nutritious choices.
                            <br>
                            Slightly Unhealthy: Occasional indulgence in unhealthy options, but with some healthier choices included.
                            <br>
                            Balanced: A mix of nutritious and less nutritious foods in moderation.
                            <br>
                            Slightly Healthy: Prioritizing nutritious choices, with occasional treats or less healthy options.
                            <br>
                            Healthy: Consistently focusing on whole, unprocessed foods and prioritizing nutrition.
                            <br>
                        </p>
                    </div>
                    <div id="sleep-info" class="dialogue-box" style="top: -300px; right: -150px;">
                        <p>
                            Insufficient: Less than 6 hours of sleep per day.
                            <br>
                            Inadequate: Not enough sleep, typically below 7 hours per day.
                            <br>
                            Minimal: The bare minimum amount of sleep needed, around 8 hours per day.
                            <br>
                            Optimal: The ideal amount of sleep, typically between 7-9 hours per day.
                            <br>
                            Recommended: The suggested amount of sleep, usually 8-10 hours per day, to promote overall well-being.
                            <br>
                        </p>
                    </div>

                    <div class="gif-container" id="gif-container">
                        <img class="gif" src="https://hackernoon.imgix.net/images/0*4Gzjgh9Y7Gu8KEtZ.gif" alt="Loading GIF">
                    </div>
                    <script type="text/javascript">
                        const calculateBMIButton = document.getElementById('calculate-bmi-button');
                        calculateBMIButton.addEventListener('click', calculateBMI);
                        const waterSelect = document.getElementById('water-select');
                        const activitiesSelect = document.getElementById('activities-select');
                        const socialInteractionsSelect = document.getElementById('social-interactions');
                        const foodIntakeSelect = document.getElementById('food-intake');
                        const sleepSelect = document.getElementById('sleep');
                        const scalePercentage = document.getElementById('scale-percentage');
                        const light = document.querySelector('.light');
                        const infoText = document.getElementById('info-text');
                        const sleepInfo = document.getElementById('sleep-info');
                        const waterInfo = document.getElementById('water-info');
                        const activitiesInfo = document.getElementById('activities-info');
                        const interactionsInfo = document.getElementById('interactions-info');
                        function toggleBMI() {
                            const content = document.querySelector('.content');
                            content.classList.toggle('active');
                        }
                        function updateScale() {
                            const water = parseInt(waterSelect.value);
                            const activities = parseInt(activitiesSelect.value);
                            const socialInteractionsValue = parseInt(socialInteractionsSelect.value);
                            const foodIntakeValue = parseInt(foodIntakeSelect.value);
                            const sleepValue = parseInt(sleepSelect.value);

                            const averageValue = Math.round((water + activities + socialInteractionsValue + sleepValue + foodIntakeValue) / 5);
                            const percentageValue = averageValue;

                            light.style.width = percentageValue + '%';
                            light.className = 'light';
                            light.classList.add('light-' + averageValue);

                            scalePercentage.style.left = percentageValue + '%';
                            scalePercentage.textContent = percentageValue + '%';
                        }
                        function showInteractionInfo(element) {
                            element.classList.toggle('active');
                            interactionsInfo.style.display = (interactionsInfo.style.display === 'block') ? 'none' : 'block';
                        }
                        function showActivitiesInfo(element) {
                            element.classList.toggle('active');
                            activitiesInfo.style.display = (activitiesInfo.style.display === 'block') ? 'none' : 'block';
                        }
                        function showInfo(element) {
                            element.classList.toggle('active');
                            infoText.style.display = (infoText.style.display === 'block') ? 'none' : 'block';
                        }
                        function showWaterInfo(element) {
                            element.classList.toggle('active');
                            waterInfo.style.display = (waterInfo.style.display === 'block') ? 'none' : 'block';
                        }
                        function showSleepInfo(element) {
                            element.classList.toggle('active');
                            sleepInfo.style.display = (sleepInfo.style.display === 'block') ? 'none' : 'block';
                        }


                        function validateNumericInput(input) {
                            const inputValue = input.value.trim();
                            const numericRegex = /^\d*\.?\d+$/;

                            if (inputValue === '') {
                                input.setCustomValidity('');
                            } else if (!numericRegex.test(inputValue)) {
                                input.setCustomValidity('Only input numeric values');
                            } else {
                                input.setCustomValidity('');
                            }
                        }
                        function calculateBMI() {
                            const weight = parseFloat(document.getElementById("weight").value);
                            const height = parseFloat(document.getElementById("height").value);

                            if (isNaN(weight) || isNaN(height) || height === 0) {
                                alert("Please enter valid weight and height values.");
                                return;
                            }

                            const bmi = weight / (height * height);
                            let bmiResult = " " + bmi.toFixed(2);

                            if (bmi < 18.5) {
                                bmiResult += " (Underweight)";
                            } else if (bmi >= 18.5 && bmi < 25) {
                                bmiResult += " (Healthy Weight)";
                            } else if (bmi >= 25 && bmi < 30) {
                                bmiResult += " (Overweight)";
                            } else {
                                bmiResult += " (Obese)";
                            }

                            document.getElementById("bmi").textContent = bmiResult;
                        }

                        function validateNumericInput(input) {
                            input.value = input.value.replace(/[^0-9.]/g, '');

                            const decimalCount = (input.value.match(/\./g) || []).length;
                            if (decimalCount > 1) {
                                const parts = input.value.split('.');
                                input.value = parts[0] + '.' + parts.slice(1).join('');
                            }
                        }


                        const form = document.querySelector('form');
                        const gifContainer = document.getElementById('gif-container');
                        const inputs = form.querySelectorAll('input, select, textarea');
                        const submitButton = form.querySelector('input[type="submit"]');

                        form.addEventListener('submit', function (event) {
                            event.preventDefault();

                            inputs.forEach((input) => input.disabled = true);
                            submitButton.disabled = true;

                            gifContainer.style.display = 'block';

                            setTimeout(function () {
                                gifContainer.style.display = 'none';

                                inputs.forEach((input) => input.disabled = false);
                                submitButton.disabled = false;

                                updateScale(); // Call updateScale to update the scale
                            }, 3000);
                        });
                    </script>
</div>

<script>
    function saveData() {
        var height = document.getElementById("height").value;
        var weight = document.getElementById("weight").value;
        var age = document.getElementById("age").value;

        var data = {
            height: height,
            weight: weight,
            age: age
        };

        localStorage.setItem("userData", JSON.stringify(data));
    }

    // Function to load the data from localStorage
    function loadData() {
        var data = localStorage.getItem("userData");
        if (data) {
            data = JSON.parse(data);
            document.getElementById("height").value = data.height;
            document.getElementById("weight").value = data.weight;
            document.getElementById("age").value = data.age;
        }
    }
    // Check if data is already stored in localStorage
    if (localStorage.getItem('bmiData')) {
        const storedData = JSON.parse(localStorage.getItem('bmiData'));
        document.getElementById('age').value = storedData.age;
        document.getElementById('height').value = storedData.height;
        document.getElementById('weight').value = storedData.weight;
        calculateBMI();
    }

    // Calculate BMI and display result
    function calculateBMI() {
        const age = parseFloat(document.getElementById('age').value);
        const height = parseFloat(document.getElementById('height').value);
        const weight = parseFloat(document.getElementById('weight').value);

        const bmi = weight / ((height / 100) ** 2);

        let result = '';
        if (!isNaN(bmi)) {
            result = `Your BMI is: ${bmi.toFixed(2)}`;
        } else {
            result = 'Please enter valid values.';
        }

        document.getElementById('result').textContent = result;

        // Store data in localStorage
        const bmiData = { age, height, weight };
        localStorage.setItem('bmiData', JSON.stringify(bmiData));
    }

    // Attach event listener to the form submission
    document.getElementById('bmiForm').addEventListener('submit', function (e) {
        e.preventDefault(); // Prevent form submission
        calculateBMI();
    });
    function submitPassword() {
        var password = document.getElementById('password-input').value;
        if (password === '1') {
            document.getElementById('password-overlay').style.display = 'none';
            document.getElementById('content').style.display = 'block';
        } else {
            alert('Incorrect password. Please try again.');
        }
    }
</script>
</body>
</html>
