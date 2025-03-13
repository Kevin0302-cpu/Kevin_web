<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Random Trái Ác Quỷ</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; padding: 50px; }
        button { font-size: 20px; padding: 10px 20px; cursor: pointer; }
        p { font-size: 24px; font-weight: bold; margin-top: 20px; }
    </style>
</head>
<body>
    <h1>🎲 Random Trái Ác Quỷ 🎲</h1>
    <button onclick="showRandomFruit()">Nhận Ngay</button>
    <p id="result">🍏 Nhấn nút để random!</p>

    <script>
        const bloxFruits = [
            { name: "Leopard 🐆 (Mythical)", chance: 5 },
            { name: "Dragon 🐉 (Mythical)", chance: 1 },
            { name: "Dough 🍩 (Mythical)", chance: 15 },
            { name: "Venom 🐍 (Mythical)", chance: 10 },
            { name: "Shadow 👤 (Mythical)", chance: 10 },
            { name: "Spirit 👻 (Mythical)", chance: 10 },
            { name: "Control ☯️ (Mythical)", chance: 5 },
            { name: "Gravity 🌍 (Legendary)", chance: 7 },
            { name: "Portal 🚪 (Legendary)", chance: 8 },
            { name: "Rumble ⚡ (Legendary)", chance: 10 },
            { name: "Blizzard ❄️ (Legendary)", chance: 10 },
            { name: "Yeti ☃ (Mythical)", chance: 4 },
            { name: "Kitsune 🦊 (Mythical)", chance: 5 }
        ];

        function showRandomFruit() {
            let randomNumber = Math.random() * 100; 
            let cumulativeChance = 0;

            for (let fruit of bloxFruits) {
                cumulativeChance += fruit.chance;
                if (randomNumber < cumulativeChance) {
                    document.getElementById("result").innerText = `🔥 Bạn nhận được: ${fruit.name}!`;
                    return;
                }
            }
        }
    </script>
</body>
</html>
