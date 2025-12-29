# Ex.07 Design of Interactive Image Gallery
## Date:29-12-2025

## AIM:
To design a web application for an inteactive image gallery for a minimum five images with next and previous buttons.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM:
```
abcd.html

<html>
<head>
    <title>Interactive Image Gallery</title>
    <link href="style.css" rel="stylesheet">
</head>
<body>
    <header class="header">
        <h1>Image Gallery</h1>
    </header>

    <div class="gallery-container">
        <div class="gallery-card">
            <img id="galleryImage" src="pic1.jpg" alt="Gallery Image">
            <p class="caption" id="caption">white screen</p>

            <div class="buttons">
                <button onclick="prevImage()">Previous</button>
                <button onclick="nextImage()">Next</button>
            </div>
        </div>
    </div>

    <footer class="footer">
        GAUTAM.P (25009613)
    </footer>

    <script>
        let gallery = [
            { src: "tumbler.jpg", text: "TUMBLER" },
            { src: "vali.jpg", text: "VALI" },
            { src: "cooker.jpg", text: "COOKER" },
            { src: "jug.jpg", text: "JUG" },
            { src: "tomato.jpg", text: "POT" },
            
        ];
        let index = 0;
        function nextImage() {
            index++;
            if (index >= gallery.length) {
                index = 0;
            }
            updateImage();
        }
        function prevImage() {
            index--;
            if (index < 0) {
                index = gallery.length - 1;
            }
            updateImage();
        }
        function updateImage() {
            document.getElementById("galleryImage").src = gallery[index].src;
            document.getElementById("caption").innerText = gallery[index].text;
        }
    </script>
</body>
</html>

style.css

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    background-color: white;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}

.header {
    background-color: black;
    color: white;
    text-align: center;
    padding: 15px;
}

.gallery-container {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
}

.gallery-card {
    background-color: white;
    padding: 20px;
    border-radius: 12px;
    box-shadow: 0 10px 25px rgba(0,0,0,0.15);
    text-align: center;
    width: 380px;
}

.gallery-card img {
    width: 250px;     
    height: 200px;
    border-radius: 10px;
    margin-bottom: 10px;
}

.caption {
    margin: 15px 0;
    font-size: 16px;
    font-weight: bold;
}

.buttons {
    display: flex;
    justify-content: center;
    gap: 15px;
}

.buttons button {
    background-color: blueviolet;
    color: white;
    border: none;
    padding: 10px 18px;
    border-radius: 8px;
    cursor: pointer;
}

.buttons button:hover {
    background-color: violet;
}

.footer {
    background-color: grey;
    color: white;
    text-align: center;
    padding: 12px;
}
```
## OUTPUT:
![alt text](<Screenshot 2025-12-29 112131.png>)
![alt text](<Screenshot 2025-12-29 112142.png>)
![alt text](<Screenshot 2025-12-29 112156.png>)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
