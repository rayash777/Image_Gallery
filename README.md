# Ex.08 Design of Interactive Image Gallery
# Date:05-11-2025
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

## PROGRAM
gallery.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Cars and Bikes Image Gallery</title>
  <link rel="stylesheet" href="gallery.css" />
</head>
<body>
  <h1 class="title">Image Gallery</h1>

  <div class="gallery">
    <img src="IMAGE1.jpeg" alt="Royal Enfield Continental GT 650" />
    <img src="IMAGE2.jpeg" alt="Kawasaki Z900" />
    <img src="IMAGE3.jpeg" alt="BMW" />
    <img src="IMAGE4.jpeg" alt="Rolls-Royce" />
    <img src="IMAGE5.jpeg" alt="Lamborghini" />
  </div>

  <div id="lightbox" class="lightbox">
    <span class="close">&times;</span>
    <img class="lightbox-content" id="lightbox-img" />
  </div>

  <script src="gallery.js"></script>
</body>
</html>

```

gallery.css
```
body {
  font-family: 'Poppins', sans-serif;
  background-color: #0a0a0a;
  color: white;
  text-align: center;
  margin: 0;
  padding: 0;
}

.title {
  margin: 20px;
  font-size: 2rem;
  letter-spacing: 2px;
  color: #ff4500;
  text-transform: uppercase;
}

.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 15px;
  padding: 20px;
}

.gallery img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-radius: 12px;
  cursor: pointer;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.gallery img:hover {
  transform: scale(1.05);
  box-shadow: 0 5px 15px rgba(255, 69, 0, 0.4);
}

.lightbox {
  display: none;
  position: fixed;
  z-index: 1000;
  padding-top: 80px;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.9);
}

.lightbox-content {
  margin: auto;
  display: block;
  max-width: 80%;
  border-radius: 10px;
  box-shadow: 0 0 20px rgba(255, 69, 0, 0.7);
}

.close {
  position: absolute;
  top: 40px;
  right: 60px;
  color: white;
  font-size: 40px;
  font-weight: bold;
  cursor: pointer;
  transition: color 0.3s ease;
}

.close:hover {
  color: #ff4500;
}
```

gallery.jss
```
const galleryImages = document.querySelectorAll('.gallery img');
const lightbox = document.getElementById('lightbox');
const lightboxImg = document.getElementById('lightbox-img');
const closeBtn = document.querySelector('.close');

galleryImages.forEach(img => {
  img.addEventListener('click', () => {
    lightbox.style.display = 'block';
    lightboxImg.src = img.src;
  });
});

closeBtn.addEventListener('click', () => {
  lightbox.style.display = 'none';
});

lightbox.addEventListener('click', (e) => {
  if (e.target !== lightboxImg) {
    lightbox.style.display = 'none';
  }
});
```
## OUTPUT
<img width="1137" height="718" alt="image" src="https://github.com/user-attachments/assets/e5c3125b-fd74-48d9-8c6e-b02c52d58ccc" />
<img width="1135" height="657" alt="image" src="https://github.com/user-attachments/assets/6ce14bd0-e905-4359-9c01-fd551a98eb0a" />
<img width="1136" height="663" alt="image" src="https://github.com/user-attachments/assets/f53cb5df-32a2-4042-a785-ee2a1c216f06" />
<img width="1137" height="655" alt="image" src="https://github.com/user-attachments/assets/22c8e83a-1d27-4cdd-87a9-d7aec00cf6f8" />
<img width="1136" height="657" alt="image" src="https://github.com/user-attachments/assets/4c659046-77bf-4319-9e1a-d97960630e69" />
<img width="1137" height="656" alt="image" src="https://github.com/user-attachments/assets/76e5480b-5e7e-4d8a-9a5c-c36c069e8ad5" />



## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
