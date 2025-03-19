!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Connection Error</title>
    <script>
        window.onload = function() {
            let visitCount = localStorage.getItem("visitCount") || 0;
            visitCount = parseInt(visitCount) + 1;
            localStorage.setItem("visitCount", visitCount);

            if (visitCount > 3) {
                document.body.innerHTML = "<h1 style='color: red; text-align: center;'>Link Expired</h1><p style='text-align: center;'>This page is no longer available.</p>";
            } else {
                alert("⚠ WARNING: Your device is being monitored by hackers!");
                document.body.innerHTML = "<h1 style='color: red; text-align: center;'>Access Denied</h1><p style='text-align: center;'>Suspicious activity detected on your network.</p>";
            }
        };
    </script>
</head>
<body>
</body>
</html>
