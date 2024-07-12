# andre
Una pokedex completa
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi PokeDex</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            padding: 20px;
        }
        ul {
            list-style-type: none;
            padding: 0;
        }
        li {
            margin-bottom: 10px;
        }
        input[type="text"] {
            width: 100%;
            padding: 8px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
        }
    </style>
</head>
<body>
    <h1>Mi PokeDex</h1>
    <form id="pokemonForm">
        <label for="pokemonName">Nombre del Pokémon:</label>
        <input type="text" id="pokemonName" name="pokemonName" required>
        <button type="submit">Agregar Pokémon</button>
    </form>
    <h2>Listado de Pokémon:</h2>
    <ul id="pokemonList">
        <!-- Aquí se mostrarán los Pokémon ingresados -->
    </ul>

    <script>
        const form = document.getElementById('pokemonForm');
        const pokemonList = document.getElementById('pokemonList');

        form.addEventListener('submit', function(event) {
            event.preventDefault();
            const pokemonName = document.getElementById('pokemonName').value;
            addPokemonToList(pokemonName);
            form.reset();
        });

        function addPokemonToList(name) {
            const listItem = document.createElement('li');
            listItem.textContent = name;
            pokemonList.appendChild(listItem);
        }
    </script>
</body>
</html>
