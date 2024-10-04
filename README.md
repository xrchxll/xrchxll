<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Daily Reminders</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f4f4f4;
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 0;
        }
        .reminder {
            font-size: 48px;
            color: #35424a;
            background: #ffffff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
    </style>
</head>
<body>

<div class="reminder" id="reminder"></div>

<script>
    // Array of reminders with dates
    const reminders = [
        { date: '2024-10-01', text: 'Meeting with the team at 10 AM' },
        { date: '2024-10-02', text: 'Submit the project report' },
        { date: '2024-10-03', text: 'Doctor’s appointment at 3 PM' },
        { date: '2024-10-04', text: 'Tell Venice nga wala koy sweldo huhu pahingin ng pera Alice Guo huhu' },
        // Add more reminders as needed
    ];

    function displayReminder() {
        const today = new Date().toISOString().split('T')[0]; // Get today's date in YYYY-MM-DD format
        const reminder = reminders.find(rem => rem.date === today);

        const reminderDiv = document.getElementById('reminder');
        if (reminder) {
            reminderDiv.textContent = reminder.text;
        } else {
            reminderDiv.textContent = 'No reminders for today!';
        }
    }

    displayReminder();
</script>

</body>
</html>
