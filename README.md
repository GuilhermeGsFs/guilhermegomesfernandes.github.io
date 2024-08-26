<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Site Pessoal</title>
    <link rel="stylesheet" href="styles.css"> <!-- Link para o arquivo CSS -->
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="#sobre" onclick="showContent('sobre')">Sobre mim</a></li>
                <li><a href="#formacao" onclick="showContent('formacao')">Formação Educacional</a></li>
                <li><a href="#portfolio" onclick="showContent('portfolio')">Portfólio</a></li>
                <li><a href="#contato" onclick="showContent('contato')">Contato</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section id="sobre" class="content">
            <h2>Sobre mim</h2>
            <p>Aqui você pode escrever sobre você, seus hobbies e interesses.</p>
        </section>
        <section id="formacao" class="content" style="display:none;">
            <h2>Formação Educacional</h2>
            <p>Detalhes sobre sua formação educacional e idiomas.</p>
        </section>
        <section id="portfolio" class="content" style="display:none;">
            <h2>Portfólio</h2>
            <p>Links para outros sites que você tenha feito ou trabalhos desenvolvidos durante o curso.</p>
        </section>
        <section id="contato" class="content" style="display:none;">
            <h2>Contato</h2>
            <form>
                <label for="nome">Nome:</label>
                <input type="text" id="nome" name="nome">
                
                <label for="email">Email:</label>
                <input type="email" id="email" name="email">
                
                <label for="mensagem">Mensagem:</label>
                <textarea id="mensagem" name="mensagem"></textarea>
                
                <button type="submit">Enviar</button>
            </form>
        </section>
    </main>

    <script>
        function showContent(id) {
            var contents = document.getElementsByClassName('content');
            for (var i = 0; i < contents.length; i++) {
                contents[i].style.display = 'none';
            }
            document.getElementById(id).style.display = 'block';
        }
    </script>
</body>
</html>
