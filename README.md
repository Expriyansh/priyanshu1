<!DOCTYPE html>
<html>
<head>
    <title>Random Background Color</title>
</head>
<body>
    <script>
        const button = document.createElement('button');
        button.textContent = 'Change Background Color';
        document.body.appendChild(button);

        function getRandomColor() {
            const letters = '0123456789ABCDEF';
            let color = '#';
            for (let i = 0; i < 6; i++) {
                color += letters[Math.floor(Math.random() * 16)];
            }
            return color;
        }

        button.addEventListener('click', () => {
            document.body.style.backgroundColor = getRandomColor();
        });
    </script>
</body>
</html>
