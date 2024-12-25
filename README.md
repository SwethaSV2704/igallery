# Ex.08 Design of Interactive Image Gallery

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

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

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FESTIVALS</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
             
        }
        .gallery {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            justify-content: center;
            padding: 20px;
        }
        .gallery img {
            width: 200px;
            height: 150px;
            object-fit: cover;
            border-radius: 8px;
            cursor: pointer;
            transition: transform 0.3s;
        }
        .gallery img:hover {
            transform: scale(1.1);
        }
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(69, 9, 9, 0.8);
            justify-content: center;
            align-items: center;
        }
        .modal img {
            max-width: 90%;
            max-height: 80%;
            border-radius: 10px;
        }
        .modal-close {
            position: absolute;
            top: 20px;
            right: 30px;
            font-size: 30px;
            color: white;
            cursor: pointer;
        }
    </style>
</head>
<body background="bg.jpg" >

<h1 style="text-align: center; margin-top: 20px;">FESTIVALS AROUND THE WORLD</h1>
<div class="gallery">
    
    
    <div class="align-items">
        <div class="row">
            <div class="col-md-3">
    <img src=Diwali-Festival.jpg   alt="Image 1">
    <img src=ramadan.jpg alt="Image 2">
    <img src=christmas.jpg alt="Image 3">
            </div>
            <div class="col-md-3">
    <img src=holi.jpg alt="Image 4">
    <img src=chinise-new-year.jpg alt="Image 5">
    <img src=dayofthedead-mexico.jpg alt="Image 5">
            </div>
    <img src=easter.jpg alt="Image 5">
    <img src=Timkat.jpg alt="Image 5">
    <img src=sinulog.jpg alt="Image 5">
            </div>
        </div>
    
</div>
</div>

<div class="modal" id="imageModal">
    <span class="modal-close" id="closeModal">&times;</span>
    <img src="" alt="Expanded View" id="modalImage">
</div>


<script>
    const galleryImages = document.querySelectorAll('.gallery img');
    const modal = document.getElementById('imageModal');
    const modalImage = document.getElementById('modalImage');
    const closeModal = document.getElementById('closeModal');

    galleryImages.forEach(img => {
        img.addEventListener('click', () => {
            modal.style.display = 'flex';
            modalImage.src = img.src;
        });
    });

    closeModal.addEventListener('click', () => {
        modal.style.display = 'none';
    });

    modal.addEventListener('click', (e) => {
        if (e.target === modal) {
            modal.style.display = 'none';
        }
    });
</script>

</body>
</html>
```
## OUTPUT:
![Screenshot (47)](https://github.com/user-attachments/assets/02699244-645b-4f35-915c-b376cf4c3cda)
![Screenshot (48)](https://github.com/user-attachments/assets/33472054-5837-4824-849e-0cef48c3bb3f)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
