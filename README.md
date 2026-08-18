# Emotion Launcher

O **Emotion Launcher** é um launcher nativo para Windows, extremamente leve, rápido e moderno, desenvolvido para **GTA San Andreas (SA-MP / open.mp)**. Ele combina uma interface visual elegante inspirada no estilo **FiveM** com a alta performance e estabilidade de um aplicativo nativo compilado.

---

## Principais Funcionalidades

* **Interface Estilo FiveM:** Design escuro, responsivo e moderno desenvolvido em HTML5/CSS3/JS, renderizado nativamente via **WebView2**.
* **Alto Desempenho e Leveza:** Aplicação nativa em **C# (.NET 10)** e **WinForms**, garantindo consumo mínimo de memória RAM e inicialização instantânea.
* **Injetor Próprio em C++:** Injeção direta no jogo através da DLL nativa `samp-injector.dll` (compatível com SA-MP e open.mp).
* **Navegador de Servidores Completo:**
  * Categorias para servidores **Internet (open.mp)**, **Hosted/Destaques**, **Favoritos** e **Recentes**.
  * Pesquisa instantânea em tempo real por Nome, IP ou Gamemode.
  * Loop dinâmico de ping e contagem de jogadores em segundo plano.
* **Conexão Rápida Estilo FiveM:** Exibição de um pop-up / modal de carregamento animado ao clicar duas vezes num servidor.
* **Validação Obrigatória do GTA SA:** Verificação automática da pasta do jogo. Se o `gta_sa.exe` não estiver configurado, exibe um modal bloqueante para seleção do diretório.
* **Modo História & Galeria:** Botões integrados para iniciar o GTA SA Singleplayer e abrir rapidamente a pasta de capturas/replays (GTA San Andreas User Files).

---

## Tecnologias Utilizadas

| Camada | Tecnologia |
| :--- | :--- |
| **Frontend (UI)** | HTML5, CSS3, JavaScript (ES6+), FontAwesome 6 |
| **Backend (Desktop)** | C# (.NET 10), WinForms, Microsoft WebView2 |
| **Injetor Nativo** | C++ (`samp-injector.dll`) |
| **Comunicação / APIs** | SAMPQuery, Open.mp API, Newtonsoft.Json |

---

## Estrutura do Código

O projeto foi construído de forma simples e direta num único ficheiro principal (`MainForm.cs`) com cerca de **1.100 linhas de código**. 

Essa estrutura unificada foi pensada para:
1. Facilitar a compilação imediata sem dependências complexas.
2. Permitir o estudo direto da integração entre **C# WinForms**, **WebView2** e **DLLs em C++**.
3. Servir de base para que a comunidade possa modularizar e refatorar conforme preferir.

---

## Pré-requisitos

* **Sistema Operativo:** Windows 10 / Windows 11 (64-bit)
* **SDK:** [.NET 10 SDK](https://dotnet.microsoft.com/)
* **Componente:** Microsoft Edge WebView2 Runtime (pré-instalado no Windows 10/11)
* **Jogo:** Cópia válida do GTA San Andreas com o executável `gta_sa.exe`

---

## Como Compilar e Executar

1. Clone o repositório:
   ```bash
   git clone [https://github.com/seu-usuario/emotion-launcher.git](https://github.com/seu-usuario/emotion-launcher.git)
Certifique-se de que a DLL samp-injector.dll está presente no diretório de saída do projeto (bin/Debug ou bin/Release).

Abra a solução no Visual Studio ou compile via terminal:

Bash
dotnet build
dotnet run
Contribuição
Sinta-se à vontade para fazer um fork do projeto, modularizar o código, adicionar novos temas ou enviar Pull Requests com melhorias!
