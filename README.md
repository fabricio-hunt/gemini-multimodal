🌌 Projeto Gemini

Uma aplicação web de demonstração que captura áudio e tela do usuário,
enviando quadros de imagem para um servidor via WebSocket.
Ideal para testes de processamento em tempo real, IA e transmissões de
vídeo/áudio.

------------------------------------------------------------------------

📋 Funcionalidades

-   Captura da tela do usuário (screen share) com resolução máxima de
    640x480.
-   Envio periódico (a cada 3 s) de quadros em Base64 para o servidor.
-   Preparação para captura e transmissão de áudio em tempo real.
-   Interface simples usando Material Design Lite.

------------------------------------------------------------------------

🚀 Tecnologias Utilizadas

-   HTML5 / CSS3 / JavaScript
-   Material Design Lite (estilo e componentes)
-   WebSocket (comunicação em tempo real)

------------------------------------------------------------------------

🗂 Estrutura do Projeto

    projeto-gemini/
    │
    ├── index.html      # Página principal da aplicação
    ├── style.css       # Estilos personalizados
    └── script.js       # Lógica principal (conexão WebSocket, captura de tela e áudio)

------------------------------------------------------------------------

⚙️ Pré-requisitos

-   Node.js (opcional, se for servir via HTTP local)
-   Navegador com suporte a:
    -   navigator.mediaDevices.getDisplayMedia (captura de tela)
    -   WebSocket
-   Servidor WebSocket rodando em: ws://localhost:9090
    (pode ser alterado no código para o seu endpoint real)

------------------------------------------------------------------------

🏁 Como Executar Localmente

1.  Clone este repositório:

        git clone https://github.com/SEU_USUARIO/projeto-gemini.git
        cd projeto-gemini

2.  Abra o arquivo index.html diretamente no navegador ou sirva via um
    servidor simples:

        npx http-server .

      Se usar http-server, o endereço padrão será:
      http://127.0.0.1:8080

3.  Inicie seu servidor WebSocket na porta 9090 ou ajuste a constante
    URL no HTML/JS.

------------------------------------------------------------------------

💻 Principais Partes do Código

index.html

-   Define a interface com Material Design Lite.
-   Inclui botão de microfone para iniciar/pausar captura.
-   Possui elementos <video> e <canvas> ocultos para processamento.

script.js (ou script embutido)

-   startScreenShare(): solicita permissão e captura a tela.
-   captureImage(): captura frame a cada 3 s e converte em Base64.
-   WebSocket: conexão em tempo real para envio de imagens e áudio.

------------------------------------------------------------------------

🧩 Possíveis Melhorias

-   Mover todo o JavaScript inline para script.js (melhor manutenção).
-   Adicionar autenticação no WebSocket.
-   Otimizar taxa de captura e compressão de imagens.
-   Tratar áudio em tempo real.

------------------------------------------------------------------------

📜 Licença

Este projeto é distribuído sob a licença MIT.
Consulte o arquivo LICENSE para mais detalhes.
