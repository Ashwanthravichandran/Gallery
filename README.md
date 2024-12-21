# Ex.08 Design of Interactive Image Gallery
# Date:19-12-2024
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Photo Gallery</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            background-color: #040404;
            color: #fff;
        }

        h1, h2 {
            font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
            text-align: center;
        }

        h1 {
            color: #f0f0f1;
        }

        h2 {
            color: #edf5ed;
        }

        .gallery {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            max-width: 1200px;
            padding: 10px;
            justify-content: center;
        }

        .gallery-item {
            cursor: pointer;
            text-align: center;
            width: 200px;
            margin: 10px;
            border: 2px solid #101111;
            border-radius: 10px;
            overflow: hidden;
            transition: transform 0.3s;
        }

        .gallery-item img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .gallery-item:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
        }

        
        #modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        #modal img {
            max-width: 90%;
            max-height: 90%;
            border: 2px solid #fff;
        }

        #modal .close {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 30px;
            color: #fff;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1>Interactive Photo Gallery</h1>
    <h2></h2>

    <div class="gallery">
        <div class="gallery-item"><img src="dud.jpg" alt=""></div>
        <div class="gallery-item"><img src="lad.jpg" alt=""></div>
        <div class="gallery-item"><img src="lak.jpg" alt=""></div>
        <div class="gallery-item"><img src="lal.jpg" alt=""></div>
        <div class="gallery-item"><img src="man.jpg" alt=""></div>
        <div class="gallery-item"><img src="mun.jpg" alt=""></div>
        <div class="gallery-item"><img src="red.jpg" alt=""></div>
        <div class="gallery-item"><img src="taj.jpg" alt=""></div>
        <div class="gallery-item"><img src="tem.jpg" alt=""></div>
        <div class="gallery-item"><img src="var.jpg" alt=""></div>
    </div>

    
    <div id="modal">
        <span class="close">&times;</span>
        <img id="modal-img" src="" alt="Enlarged">
    </div>

    <footer>
        &copy; 2024 designed by RAJA ASHWANTH R . @ All Rights Reserved.
    </footer>

    <script>
        
        const galleryItems = document.querySelectorAll('.gallery-item img');
        const modal = document.getElementById('modal');
        const modalImg = document.getElementById('modal-img');
        const closeModal = document.querySelector('.close');

        
        galleryItems.forEach(item => {
            item.addEventListener('click', () => {
                modal.style.display = 'flex';
                modalImg.src = item.src; 
            });
        });

        
        closeModal.addEventListener('click', () => {
            modal.style.display = 'none';
        });

        
        modal.addEventListener('click', (event) => {
            if (event.target === modal) {
                modal.style.display = 'none';
            }
        });
    </script>
</body>
</html>

```
# OUTPUT:
![alt text](<Screenshot (29).png>)
![Screenshot 2024-12-21 160725](https://github.com/user-attachments/assets/d46f383d-bd66-4f7d-9fad-787898f86a3a)
![Screenshot 2024-12-21 160744](https://github.com/user-attachments/assets/ec273159-5d9e-4464-b015-a8d36b7dceec)
![Screenshot 2024-12-21 160804](https://github.com/user-attachments/assets/57854b16-59a5-458f-95cf-dd645eb0040a)
![Screenshot 2024-12-21 160823](https://github.com/user-attachments/assets/40c2dad6-8e90-44ec-81a3-dfa59820dbf1)
![Screenshot 2024-12-21 160835](https://github.com/user-attachments/assets/12c5fcd0-6263-4f40-84fc-120cea331923)
![Screenshot 2024-12-21 160848](https://github.com/user-attachments/assets/d8c74917-99af-4f1c-9012-8a502a5d5ade)
![Screenshot 2024-12-21 160902](https://github.com/user-attachments/assets/ae77c927-df38-46e1-8364-729fbbc03749)
![Screenshot 2024-12-21 160912](https://github.com/user-attachments/assets/d093ce01-76e1-4ccc-835d-b03489210a1c)
![Screenshot 2024-12-21 160923](https://github.com/user-attachments/assets/73167b1d-c53b-4049-a53c-dd993bb7c041)
![Screenshot 2024-12-21 160936](https://github.com/user-attachments/assets/72e3e7a7-1471-4025-adbf-c249dbd810c6)









# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
