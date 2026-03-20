
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NexsiteDigital Patos - Em Manutenção</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        @keyframes spin-slow {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        .animate-spin-slow {
            animation: spin-slow 8s linear infinite;
        }
        body {
            background-color: #020617; /* slate-950 */
        }
    </style>
</head>
<body class="text-slate-100 font-sans min-h-screen flex items-center justify-center p-6 overflow-hidden relative">

    <div class="absolute top-0 left-0 w-64 h-64 bg-indigo-600/10 rounded-full blur-[80px] -z-10"></div>
    <div class="absolute bottom-0 right-0 w-96 h-96 bg-blue-600/10 rounded-full blur-[100px] -z-10"></div>

    <main class="flex flex-col items-center max-w-4xl w-full text-center">
        
        <div class="mb-8">
            <i data-lucide="settings" class="w-20 h-20 text-indigo-500 animate-spin-slow"></i>
        </div>

        <h1 class="text-4xl md:text-6xl font-bold mb-4 tracking-tight">
            Estamos em <span class="text-indigo-500 text-transparent bg-clip-text bg-gradient-to-r from-indigo-400 to-blue-500">Manutenção</span>
        </h1>
        
        <p class="text-slate-400 text-lg md:text-xl max-w-2xl mb-12">
            O <strong>Nexsite</strong> está passando por atualizações para melhorar sua experiência. 
            Voltaremos em instantes com novidades incríveis!
        </p>

        <div class="grid grid-cols-2 md:grid-cols-4 gap-4 mb-12" id="countdown">
            <div class="flex flex-col items-center bg-slate-900/50 border border-slate-800 p-4 rounded-2xl w-28">
                <span class="text-3xl font-mono font-bold text-indigo-400" id="days">00</span>
                <span class="text-xs uppercase tracking-widest text-slate-500">Dias</span>
            </div>
            <div class="flex flex-col items-center bg-slate-900/50 border border-slate-800 p-4 rounded-2xl w-28">
                <span class="text-3xl font-mono font-bold text-indigo-400" id="hours">00</span>
                <span class="text-xs uppercase tracking-widest text-slate-500">Horas</span>
            </div>
            <div class="flex flex-col items-center bg-slate-900/50 border border-slate-800 p-4 rounded-2xl w-28">
                <span class="text-3xl font-mono font-bold text-indigo-400" id="minutes">00</span>
                <span class="text-xs uppercase tracking-widest text-slate-500">Minutos</span>
            </div>
            <div class="flex flex-col items-center bg-slate-900/50 border border-slate-800 p-4 rounded-2xl w-28">
                <span class="text-3xl font-mono font-bold text-indigo-400" id="seconds">00</span>
                <span class="text-xs uppercase tracking-widest text-slate-500">Segundos</span>
            </div>
        </div>

        <div class="w-full max-w-md bg-slate-900 p-1 rounded-full border border-slate-800 flex items-center mb-12 focus-within:ring-2 focus-within:ring-indigo-500 transition-all">
            <input 
                type="email" 
                placeholder="Seu melhor e-mail" 
                class="bg-transparent flex-1 px-6 py-3 outline-none text-sm text-slate-100"
            />
            <button class="bg-indigo-600 hover:bg-indigo-700 text-white px-6 py-3 rounded-full text-sm font-semibold transition-colors">
                Avisar-me
            </button>
        </div>

        <div class="flex gap-6 text-slate-500">
            <a href="#" class="hover:text-indigo-400 transition-colors"><i data-lucide="instagram"></i></a>
            <a href="#" class="hover:text-indigo-400 transition-colors"><i data-lucide="linkedin"></i></a>
            <a href="#" class="hover:text-indigo-400 transition-colors"><i data-lucide="mail"></i></a>
        </div>

        <footer class="mt-16 text-slate-600 text-sm">
            &copy; <span id="year"></span> Nexsite. Todos os direitos reservados.
        </footer>
    </main>

    <script>
        // Inicializar Ícones
        lucide.createIcons();

        // Atualizar Ano no Rodapé
        document.getElementById('year').textContent = new Date().getFullYear();

        // Lógica do Contador (24 horas a partir do acesso)
        let totalSeconds = 3600 * 24;
        
        function updateTimer() {
            const d = Math.floor(totalSeconds / (3600 * 24));
            const h = Math.floor((totalSeconds % (3600 * 24)) / 3600);
            const m = Math.floor((totalSeconds % 3600) / 60);
            const s = totalSeconds % 60;

            document.getElementById('days').innerText = String(d).padStart(2, '0');
            document.getElementById('hours').innerText = String(h).padStart(2, '0');
            document.getElementById('minutes').innerText = String(m).padStart(2, '0');
            document.getElementById('seconds').innerText = String(s).padStart(2, '0');

            if (totalSeconds > 0) totalSeconds--;
        }

        setInterval(updateTimer, 1000);
        updateTimer();
    </script>
</body>
</html>
