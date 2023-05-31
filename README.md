<!DOCTYPE html>
<html>
<head>
    <title>Mawasetiawan CV</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            text-align: center;
        }
        
        h1 {
            color: #333;
        }
        
        p {
            margin-bottom: 20px;
            color: #666;
        }
        
        #header {
            position: relative;
            height: 300px;
            background-color: #000;
            overflow: hidden;
        }
        
        #slideshow {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0.4;
        }
        
        #content {
            padding-top: 320px;
        }
        
        .slide {
            display: none;
            max-width: 100%;
            height: auto;
        }
    </style>
</head>
<body>
    <div id="header">
        <div id="slideshow">
            <img class="slide" src="images/image1.jpg" alt="Slideshow Image 1">
            <img class="slide" src="images/image2.jpg" alt="Slideshow Image 2">
            <img class="slide" src="images/image3.jpg" alt="Slideshow Image 3">
        </div>
    </div>
    
    <div id="content">
        <h1>Mawasetiawan CV</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla bibendum urna in tincidunt porttitor. Donec sed ex vel leo aliquam feugiat. Fusce ut vulputate nisl. Nulla pharetra ultricies tempor. Quisque laoreet facilisis nulla, at eleifend erat fringilla eu. In malesuada massa id venenatis semper.</p>
        <p>Saya adalah seorang designer dengan keahlian di bidang 3D modelling dan 2D illustration. Saya memiliki pengalaman dalam menciptakan visual yang menarik dan kreatif untuk berbagai proyek, seperti desain produk, animasi, dan ilustrasi digital.</p>
    </div>

    <script>
        var slideshow = document.getElementById('slideshow');
        var slides = document.getElementsByClassName('slide');
        var currentSlide = 0;
        var slideInterval = setInterval(nextSlide, 2000);

        function nextSlide() {
            slides[currentSlide].style.display = 'none';
            currentSlide = (currentSlide + 1) % slides.length;
            slides[currentSlide].style.display = 'block';
        }
    </script>
</body>
</html>
