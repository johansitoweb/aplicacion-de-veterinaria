# aplicacion-de-veterinaria

![image](https://github.com/user-attachments/assets/c6827095-8970-49b4-ba3e-eb2cd7ae9aa4)


Este es un proyecto es para  un cliente este proyecto sera creado con php html css bootstrap chart.js sqlite ionic 


<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contacto</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/@heroicons/react/outline"></script>
</head>
<body class="bg-gray-100 flex items-center justify-center min-h-screen">
    <div class="p-8 rounded-lg shadow-lg w-96">
        <h2 class="text-2xl font-bold mb-6 text-center">Contacto</h2>
        <form id="contactForm" class="bg-transparent">
            <div class="mb-4">
                <label class="block text-gray-700" for="name">Nombre</label>
                <input type="text" id="name" name="name" required class="mt-1 block w-full p-2 border border-gray-300 rounded"/>
            </div>
            <div class="mb-4">
                <label class="block text-gray-700" for="email">Email</label>
                <input type="email" id="email" name="email" required class="mt-1 block w-full p-2 border border-gray-300 rounded"/>
            </div>
            <div class="mb-4">
                <label class="block text-gray-700" for="message">Mensaje</label>
                <textarea id="message" name="message" rows="4" required class="mt-1 block w-full p-2 border border-gray-300 rounded"></textarea>
            </div>
            <button type="submit" class="w-full bg-blue-500 text-white p-2 rounded hover:bg-blue-600">Enviar</button>
        </form>
        <div id="alert" class="hidden fixed top-5 right-5 bg-green-500 text-white p-4 rounded flex items-center" role="alert">
            <svg class="h-6 w-6 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-3-3v6m-1-12a9 9 0 11-9 9 9 9 0 019-9z"/>
            </svg>
            <span>Este mensaje fue enviado</span>
        </div>
    </div>

    <script>
        document.getElementById('contactForm').addEventListener('submit', function(event) {
            event.preventDefault();
            // Aquí iría la lógica para enviar el formulario a tu backend
            document.getElementById('alert').classList.remove('hidden');
            setTimeout(() => {
                document.getElementById('alert').classList.add('hidden');
            }, 3000);
            this.reset(); // Resetea el formulario
        });
    </script>
</body>
</html>
