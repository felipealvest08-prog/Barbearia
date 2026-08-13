## Felipe Teixeira
[index.html](https://github.com/user-attachments/files/31044999/index.html)
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Login - Barbearia</title>
    <link rel="stylesheet" href="style.css"> <!-- seu CSS original -->
</head>
<body>

<div class="login-container">

    <div class="logo">
        <img src="img/ChatGPT Image 29 de mar. de 2026, 00_10_25.png" alt="Logo da Barbearia">
    </div>

    <h2>Faça seu login</h2>

    <form id="login-form">

        <!-- NOME -->
        <input type="text" id="nome" placeholder="Seu nome" required>

        <!-- TELEFONE -->
        <div class="phone-field">
            <span class="prefix">+55</span>
            <input 
                type="tel"
                id="whatsapp"
                placeholder="DDD + número"
                inputmode="numeric"
                maxlength="13"
                required>
        </div>

        <!-- DATA -->
        <div class="date-field">
            <span class="date-label">Data de nascimento</span>
            <input 
                type="date"
                id="birthdate"
                required>
        </div>

        <!-- botão alterado para type button para evitar submit -->
        <button type="button" id="btn-login">Entrar</button>

    </form>
</div>

 <script src="script.js"></script>
<script>
    // ===== LOGIN PARA WELCOME.HTML =====
    const loginBtn = document.getElementById("btn-login");
    const nomeInput = document.getElementById("nome");
    const form = document.getElementById("login-form");

    loginBtn.addEventListener("click", () => {
        // Pega o nome do usuário
        const nome = nomeInput.value.trim() || "Usuário";
        
        // Redireciona para welcome.html passando o nome como parâmetro
        window.location.href = `welcome.html?nome=${encodeURIComponent(nome)}`;
    });

    // Evita que o Enter envie o form de forma tradicional
    form.addEventListener("submit", e => e.preventDefault());
</script>
</body>
</html>
