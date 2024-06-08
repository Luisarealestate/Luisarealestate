<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Perfil</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #fff;
            color: #000;
            margin: 0;
            padding: 0;
        }
        .container {
            width: 80%;
            margin: 0 auto;
            text-align: center;
            padding: 20px;
        }
        .profile-header {
            margin-top: 50px;
        }
        .profile-header img {
            border-radius: 50%;
            width: 150px;
            height: 150px;
            object-fit: cover;
        }
        .profile-header h1 {
            margin: 10px 0;
            font-size: 2.5em;
        }
        .profile-header p {
            font-size: 1.2em;
            color: #666;
        }
        .profile-content {
            margin-top: 30px;
            text-align: left;
        }
        .profile-content h2 {
            border-bottom: 1px solid #000;
            padding-bottom: 10px;
            margin-bottom: 20px;
            font-size: 1.8em;
        }
        .profile-content p {
            line-height: 1.6;
        }
        .skills {
            display: flex;
            flex-wrap: wrap;
        }
        .skill {
            flex: 1;
            min-width: 200px;
            margin: 10px;
            padding: 10px;
            border: 1px solid #000;
            border-radius: 5px;
            text-align: center;
        }
        .slideshow-container {
            max-width: 100%;
            position: relative;
            margin: auto;
            margin-top: 30px;
        }
        .slides {
            display: none;
        }
        .slides img {
            width: 100%;
            height: auto;
        }
        .prev, .next {
            cursor: pointer;
            position: absolute;
            top: 50%;
            width: auto;
            margin-top: -22px;
            padding: 16px;
            color: white;
            font-weight: bold;
            font-size: 18px;
            transition: 0.6s ease;
            border-radius: 0 3px 3px 0;
            user-select: none;
        }
        .next {
            right: 0;
            border-radius: 3px 0 0 3px;
        }
        .prev:hover, .next:hover {
            background-color: rgba(0,0,0,0.8);
        }
        .footer {
            margin-top: 50px;
            padding: 20px 0;
            border-top: 1px solid #000;
            color: #666;
        }
        .video-container {
            margin-top: 30px;
            text-align: center;
        }
        .video-container video {
            width: 100%;
            height: auto;
            max-width: 600px;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="profile-header">
            <img src="profile.jpg" alt="Foto de Perfil">
            <h1>Juan Pérez</h1>
            <p>Desarrollador Web | Diseñador Gráfico</p>
        </div>
        <div class="profile-content">
            <h2>Sobre mí</h2>
            <p>
                Soy un desarrollador web apasionado con más de 5 años de experiencia en la creación de sitios web y aplicaciones interactivas. 
                Tengo un fuerte enfoque en el diseño limpio y la experiencia del usuario.
            </p>
            <h2>Habilidades</h2>
            <div class="skills">
                <div class="skill">
                    <h3>HTML & CSS</h3>
                    <p>Experto en creación de diseños responsivos y accesibles.</p>
                </div>
                <div class="skill">
                    <h3>JavaScript</h3>
                    <p>Sólidos conocimientos en ES6, React, y Node.js.</p>
                </div>
                <div class="skill">
                    <h3>Diseño Gráfico</h3>
                    <p>Proficiente en Photoshop, Illustrator y Figma.</p>
                </div>
                <div class="skill">
                    <h3>SEO</h3>
                    <p>Optimización para motores de búsqueda y análisis web.</p>
                </div>
            </div>
        </div>

        <div class="slideshow-container">
            <div class="slides">
                <img src="photo1.jpg" alt="Foto 1">
            </div>
            <div class="slides">
                <img src="photo2.jpg" alt="Foto 2">
            </div>
            <div class="slides">
                <img src="photo3.jpg" alt="Foto 3">
            </div>
            <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
            <a class="next" onclick="plusSlides(1)">&#10095;</a>
        </div>

        <div class="video-container">
            <h2>Video de Presentación</h2>
            <video controls>
                <source src="video.mp4" type="video/mp4">
                Tu navegador no soporta la reproducción de video.
            </video>
        </div>

        <div class="footer">
            <p>© 2024 Juan Pérez. Todos los derechos reservados.</p>
        </div>
    </div>

    <script>
        let slideIndex = 0;
        showSlides();

        function showSlides() {
            let i;
            let slides = document.getElementsByClassName("slides");
            for (i = 0; i < slides.length; i++) {
                slides[i].style.display = "none";  
            }
            slideIndex++;
            if (slideIndex > slides.length) {slideIndex = 1}    
            slides[slideIndex-1].style.display = "block";  
            setTimeout(showSlides, 4000); // Cambia la imagen cada 4 segundos
        }

        function plusSlides(n) {
            showSlides(slideIndex += n);
        }
    </script>
</body>
</html>
