# Ex.08 Design of Interactive Image Gallery

## AIM
  To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS

## Step 1:

Clone the github repository and create Django admin interface

## Step 2:

Change settings.py file to allow request from all hosts.

## Step 3:

Use CSS for positioning and styling.

## Step 4:

Write JavaScript program for implementing interactivit

## Step 5:

Validate the HTML and CSS code

## Step 6:

Publish the website in the given URL.

## PROGRAM:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Photo Gallery</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f9;
        }

        .gallery-container {
            max-width: 1200px;
            margin: 20px auto;
            padding: 10px;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 15px;
        }

        .gallery-item {
            position: relative;
            cursor: pointer;
            overflow: hidden;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .gallery-item img {
            width: 100%;
            height: auto;
            transition: transform 0.3s ease;
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        .image-title {
            position: absolute;
            bottom: 10px;
            left: 10px;
            background-color: rgba(0, 0, 0, 0.6);
            color: white;
            padding: 5px 10px;
            border-radius: 5px;
            font-size: 14px;
        }

        .lightbox {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            display: none;
            align-items: center;
            justify-content: center;
            z-index: 1000;
        }

        .lightbox img {
            max-width: 90%;
            max-height: 80%;
            border-radius: 10px;
        }

        .lightbox-close {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 30px;
            color: white;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1 style="text-align: center; margin-top: 20px;"> IMAGE GALLERY</h1>
    <div class="gallery-container">
        <div class="gallery-item">
            <img src="AAA.jpg" alt="Image 1">
            <div class="image-title">Image 1</div>
        </div>
        <div class="gallery-item">
            <img src="AAA1.jpg" alt="Image 2">
            <div class="image-title">Image 2</div>
        </div>
        <div class="gallery-item">
            <img src="AAA2.jpg" alt="Image 3">
            <div class="image-title">Image 3</div>
        </div>
        <div class="gallery-item">
            <img src="AAA3.jpg" alt="Image 4">
            <div class="image-title">Image 4</div>
        </div>
        
    </div>

    <div class="lightbox" id="lightbox">
        <span class="lightbox-close" id="lightboxClose">&times;</span>
        <img src="" alt="Full Size Image" id="lightboxImage">
    </div>

    <script>
        const galleryItems = document.querySelectorAll('.gallery-item img');
        const lightbox = document.getElementById('lightbox');
        const lightboxImage = document.getElementById('lightboxImage');
        const lightboxClose = document.getElementById('lightboxClose');

        galleryItems.forEach(item => {
            item.addEventListener('click', () => {
                lightboxImage.src = item.src;
                lightbox.style.display = 'flex';
            });
        });

        lightboxClose.addEventListener('click', () => {
            lightbox.style.display = 'none';
        });

        lightbox.addEventListener('click', (e) => {
            if (e.target === lightbox) {
                lightbox.style.display = 'none';
            }
        });
    </script>
    <center><footer>
        DESIGN AND DEVELOPMENT BY PRIYESH 
        
    </footer></center>
</body>
</html>
```

## OUTPUT:
![alt text](<Screenshot 2025-05-21 213625.png>)
![alt text](AAA.jpg)
![alt text](AAA1.jpg)
![alt text](AAA2.jpg)
![alt text](AAA3.jpg)
## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
