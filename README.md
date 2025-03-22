# Carta-para-denisse-hermosa
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Carta de Amor</title>
    <style>
        body {
            font-family: 'Georgia', serif;
            color: #333;
            background-color: #f7f7f7;
            margin: 0;
            padding: 0;
        }
        .container {
            width: 80%;
            margin: 50px auto;
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        h1 {
            text-align: center;
            color: #d66b8d;
        }
        p {
            font-size: 16px;
            line-height: 1.6;
        }
        .signature {
            text-align: right;
            margin-top: 40px;
            font-style: italic;
        }
        .btn {
            display: block;
            width: 200px;
            margin: 20px auto;
            padding: 10px;
            text-align: center;
            background-color: #d66b8d;
            color: white;
            text-decoration: none;
            border-radius: 5px;
        }
        .btn:hover {
            background-color: #b95d76;
        }
    </style>
</head>
<body>

    <div class="container" id="letter">
        <h1>Carta de Amor</h1>
        <p>Mi querido/a [Nombre del destinatario],</p>
        <p>Hoy me siento inspirado/a para escribirte estas palabras, aunque sé que nunca podrían expresar por completo lo que siento por ti. Desde que entraste en mi vida, todo ha cambiado de manera maravillosa.</p>
        <p>Tu amor me da fuerzas, me llena de alegría y, sobre todo, me hace ser mejor persona. Cada momento que paso contigo es un regalo que atesoro profundamente, y no puedo esperar a seguir construyendo recuerdos juntos.</p>
        <p>No hay nada que desee más que verte feliz, que compartas conmigo todos tus sueños, tus miedos, tus alegrías. Me siento afortunado/a de tenerte en mi vida y quiero que sepas que siempre estaré aquí para ti, en los momentos buenos y malos.</p>
        <p>Te amo más de lo que las palabras pueden expresar, y espero que este amor siga creciendo con el paso del tiempo.</p>
        <div class="signature">
            Con todo mi amor,<br>
            [Tu nombre]
        </div>
        <a href="#" class="btn" id="download">Descargar como PDF</a>
    </div>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
    <script>
        const { jsPDF } = window.jspdf;
        const btnDownload = document.getElementById('download');

        btnDownload.addEventListener('click', function () {
            const doc = new jsPDF();
            const content = document.getElementById('letter').innerHTML;

            doc.html(content, {
                callback: function (doc) {
                    doc.save('carta_de_amor.pdf');
                },
                margin: [20, 20, 20, 20]
            });
        });
    </script>

</body>
</html>
