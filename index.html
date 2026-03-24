<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TR's Mewtwo ex - Premium Tracker</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Nunito:wght@400;700;900&display=swap');
        body { 
            background-color: #0f172a;
            background-image: radial-gradient(#4c1d95 1px, transparent 1px);
            background-size: 20px 20px;
            font-family: 'Nunito', sans-serif; 
            color: #f8fafc;
        }
        .deck-card { transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1); }
        .deck-card:hover { transform: translateY(-5px); box-shadow: 0 10px 25px -5px rgba(147, 51, 234, 0.4); }
        .glass-panel { background: rgba(30, 41, 59, 0.85); backdrop-filter: blur(10px); }
        .no-scrollbar::-webkit-scrollbar { display: none; }
        .no-scrollbar { -ms-overflow-style: none; scrollbar-width: none; }

        /* --- Animación de la Moneda 3D --- */
        .perspective-1000 { perspective: 1000px; }
        .coin { width: 120px; height: 120px; transform-style: preserve-3d; transition: transform 2s cubic-bezier(0.4, 2, 0.2, 0.8); }
        .coin-face { position: absolute; width: 100%; height: 100%; backface-visibility: hidden; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 4rem; font-weight: 900; box-shadow: inset 0 0 15px rgba(0,0,0,0.8); }
        .coin-front { background: radial-gradient(#dc2626, #7f1d1d); color: white; border: 6px solid #f87171; text-shadow: 2px 2px 4px rgba(0,0,0,0.5); }
        .coin-back { background: radial-gradient(#1f2937, #030712); color: #9ca3af; transform: rotateY(180deg); border: 6px solid #4b5563; }

        /* --- Animación del Dado 3D --- */
        .dice-container { perspective: 1000px; margin: 20px; }
        .dice { width: 80px; height: 80px; transform-style: preserve-3d; transition: transform 1.5s cubic-bezier(0.2, 0.8, 0.2, 1); }
        .dice-face { position: absolute; width: 100%; height: 100%; background: #1e293b; border: 3px solid #ef4444; border-radius: 12px; display: flex; align-items: center; justify-content: center; font-size: 2.5rem; color: white; font-weight: bold; box-shadow: inset 0 0 10px rgba(0,0,0,0.5); }
        .front  { transform: rotateY(  0deg) translateZ(40px); }
        .back   { transform: rotateY(180deg) translateZ(40px); }
        .right  { transform: rotateY( 90deg) translateZ(40px); }
        .left   { transform: rotateY(-90deg) translateZ(40px); }
        .top    { transform: rotateX( 90deg) translateZ(40px); }
        .bottom { transform: rotateX(-90deg) translateZ(40px); }
    </style>
</head>
<body class="pb-12">

    <header class="bg-gradient-to-r from-gray-900 via-purple-950 to-gray-900 text-white p-4 shadow-[0_4px_20px_rgba(220,38,38,0.2)] sticky top-0 z-40 border-b-4 border-red-600">
        <div class="max-w-6xl mx-auto flex flex-col md:flex-row justify-between items-center gap-4">
            <div class="flex items-center gap-4">
                <img src="https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/other/official-artwork/150.png" alt="Mewtwo" class="w-12 h-12 drop-shadow-[0_0_8px_rgba(168,85,247,0.8)]">
                <h1 class="text-2xl font-black tracking-wide text-purple-100">Team Rocket's <span class="text-red-500 font-black">Mewtwo ex</span></h1>
            </div>
            
            <div class="flex flex-wrap justify-center items-center gap-2 md:gap-4">
                <div class="flex gap-2 bg-black/40 p-1 rounded-lg backdrop-blur-sm border border-purple-900/50">
                    <button onclick="animateCoin()" class="hover:bg-purple-900/50 px-3 py-1 rounded text-sm font-bold transition-colors text-purple-200">🪙 Tirar Moneda</button>
                    <button onclick="animateDice()" class="hover:bg-purple-900/50 px-3 py-1 rounded text-sm font-bold transition-colors border-l border-purple-900/50 text-purple-200">🎲 Lanzar Dado</button>
                </div>

                <div class="flex items-center gap-2 bg-black/60 p-2 rounded-xl border border-red-900/50 backdrop-blur-sm shadow-inner">
                    <span class="text-xl font-mono font-bold w-16 text-center text-red-400" id="timer-display">50:00</span>
                    <button onclick="startTimer()" class="bg-green-600 hover:bg-green-500 text-white px-2 py-1 rounded text-sm font-bold shadow">▶</button>
                    <button onclick="pauseTimer()" class="bg-yellow-600 hover:bg-yellow-500 text-white px-2 py-1 rounded text-sm font-bold shadow">⏸</button>
                    <button onclick="resetTimer()" class="bg-red-600 hover:bg-red-500 text-white px-2 py-1 rounded text-sm font-bold shadow">⏹</button>
                </div>
            </div>
        </div>
    </header>

    <main class="max-w-6xl mx-auto p-4 mt-6 grid grid-cols-1 lg:grid-cols-3 gap-8">
        
        <div class="lg:col-span-1 flex flex-col gap-6">
            
            <div class="glass-panel p-6 rounded-2xl shadow-xl border border-purple-900/50">
                <div class="bg-red-900/80 border border-red-500 text-red-100 text-xs font-black px-3 py-1 rounded-full w-fit mb-4 tracking-widest">MI MAZO: TR's MEWTWO</div>
                <h2 class="text-2xl font-black mb-4 text-purple-300">Nueva Partida</h2>
                
                <div class="mb-4">
                    <label class="block text-sm font-bold mb-1 text-purple-200">¿Contra qué jugaste?</label>
                    <select id="opp-deck" class="w-full border-2 border-purple-800 rounded-xl p-2 bg-gray-900 font-bold text-white focus:outline-none focus:border-red-500 transition-colors"></select>
                </div>

                <div class="mb-4">
                    <label class="block text-sm font-bold mb-1 text-purple-200">¿Quién empezó?</label>
                    <div class="grid grid-cols-2 gap-2">
                        <button id="btn-turn-1" onclick="setTurn(1)" class="py-2 rounded-xl border-2 border-red-600 bg-red-600 text-white font-black transition-colors shadow-[0_0_10px_rgba(220,38,38,0.3)]">Fui 1º</button>
                        <button id="btn-turn-2" onclick="setTurn(2)" class="py-2 rounded-xl border-2 border-purple-800 bg-gray-900 text-purple-400 font-bold transition-colors">Fui 2º</button>
                    </div>
                </div>

                <div class="mb-4">
                    <label class="block text-sm font-bold mb-1 text-purple-200">Notas (Opcional)</label>
                    <input type="text" id="match-notes" placeholder="Ej: No robé energías oscuras..." class="w-full border-2 border-purple-800 rounded-xl p-2 bg-gray-900 text-white text-sm focus:outline-none focus:border-red-500 transition-colors placeholder-gray-500">
                </div>

                <label class="block text-sm font-bold mb-1 text-purple-200">Resultado Final</label>
                <div class="grid grid-cols-3 gap-2">
                    <button onclick="addMatch('W')" class="bg-green-900/40 hover:bg-green-600 hover:text-white border border-green-700 text-green-400 font-black text-lg py-3 rounded-xl transition-all shadow-sm">WIN</button>
                    <button onclick="addMatch('L')" class="bg-red-900/40 hover:bg-red-600 hover:text-white border border-red-700 text-red-400 font-black text-lg py-3 rounded-xl transition-all shadow-sm">LOSS</button>
                    <button onclick="addMatch('T')" class="bg-gray-800 hover:bg-gray-600 hover:text-white border border-gray-600 text-gray-400 font-black text-lg py-3 rounded-xl transition-all shadow-sm">TIE</button>
                </div>
            </div>

... (410 líneas restantes)
