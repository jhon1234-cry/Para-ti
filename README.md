<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" href="img/flowers.png" type="image/x-icon">
    <title>Flores para Ti</title>
    <style>
        /* Estilos generales */
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            background-color: #ffe6f2;
            text-align: center;
            font-family: Arial, sans-serif;
            margin: 0;
            animation: fadeIn 2s ease-in-out;
        }

        /* Animación de entrada */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        /* Contenedor de la flor */
        .flower-container {
            opacity: 0;
            transform: scale(0.5);
            transition: opacity 2s ease-in-out, transform 1.5s ease-in-out;
        }

        .flower-container.show {
            opacity: 1;
            transform: scale(1);
        }

        /* Imagen de la flor */
        img {
            width: 200px;
            height: auto;
            filter: drop-shadow(5px 5px 10px rgba(0, 0, 0, 0.2));
        }

        /* Frase principal */
        .love-message {
            font-size: 24px;
            font-weight: bold;
            color: #d63384;
            margin-top: 20px;
            opacity: 0;
            transition: opacity 2s ease-in-out;
        }

        .love-message.show {
            opacity: 1;
        }

        /* Mensaje final */
        .message {
            font-size: 20px;
            color: #b91c66;
            margin-top: 20px;
            opacity: 0;
            transform: translateY(10px);
            transition: opacity 3s ease-in-out, transform 1.5s ease-in-out;
        }

        .message.show {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>

    <div class="flower-container" id="flower">
        <img src="img/flowers.png" alt="Flores">
        <div class="love-message" id="loveMessage">
            Estas flores representan lo mucho que te amo.
        </div>
        <div class="message" id="message">
            Siempre le agradezco a Dios por haberte puesto en mi camino.  
            Eres lo más bonito que me pudo haber pasado.
        </div>
    </div>

    <script>
        document.addEventListener("DOMContentLoaded", function () {
            setTimeout(() => {
                document.getElementById("flower").classList.add("show");
                document.getElementById("loveMessage").classList.add("show"); // Aparece la frase con la flor
                setTimeout(() => {
                    document.getElementById("message").classList.add("show");
                }, 2000); 
            }, 1000);
        });
    </script>

</body>
</html>
