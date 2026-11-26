# Campanha de Doação Agasalho e Ração - 2027

Aplicação web para organizar uma campanha de doação de agasalhos (pessoas carentes e em situação de rua) e de ração (abrigos de animais).
Projeto Integrado – Desenvolvimento para Web – UNIFEOB (4º trimestre 2026).

## Funcionalidades
- RF01 Cadastrar e excluir ONGs e abrigos de destino
- RF02 Registrar doações (tipo, quantidade, doador, data, destino e observações)
- RF03 Exibir painel com totais arrecadados, doadores e distribuição por ONG ou abrigo
- RF04 Consultar histórico de doações e filtrar por tipo
- RF05 Excluir doação
- RF06 Exportar histórico em planilha (CSV)
- RF07 Validar formulários
- RF08 Exibir a unidade conforme o destino: abrigos de pessoas em peças e abrigos de animais em quilogramas
- RNF01 Funciona sem instalação (dados salvos no navegador) | RNF02 Interface simples e responsiva

## Tecnologias
HTML, CSS e JavaScript, sem frameworks. Os dados são salvos com localStorage.

## Ambiente de desenvolvimento
- Windows 11, com terminal PowerShell
- Visual Studio Code para editar o código
- Python 3.11, apenas para o servidor local (opcional)
- Git e GitHub para controle de versão

Para obter o projeto:
git clone https://github.com/JohnnyGarcia182/Projeto-Integrado-Unifeob-Campanha-de-doacao-agasalho-e-racao.git

## Como rodar
Abra o arquivo index.html no navegador. Para usar um servidor local, execute no terminal, dentro da pasta do projeto:

python -m http.server 8000

Depois acesse http://localhost:8000 (Ctrl+C para encerrar).

Versão publicada (GitHub Pages, hospedagem gratuita):
https://johnnygarcia182.github.io/Projeto-Integrado-Unifeob-Campanha-de-doacao-agasalho-e-racao/

Observação: os dados ficam salvos no próprio navegador; trocar de computador ou limpar os dados do navegador apaga as informações. O endereço local, o servidor local e a versão publicada guardam dados separados.

## Estrutura de diretórios
.
|-- index.html       painel
|-- registrar.html   nova doação
|-- historico.html   lista, filtro e CSV
|-- abrigos.html     cadastro de ONGs e abrigos
|-- css/
|   `-- style.css    visual
|-- js/
|   `-- app.js       funcionamento e armazenamento
`-- README.txt       instruções de uso

## Permissões de arquivos
A aplicação é estática: o navegador e o servidor só precisam de permissão de leitura nos arquivos. Nenhum arquivo precisa de permissão de execução, e a aplicação não grava nada na pasta do projeto.

- Linux ou macOS: 644 nos arquivos (dono lê e escreve; os demais só leem) e 755 nas pastas (permite entrar e listar).
  Conferir: ls -lR
  Ajustar:  find . -type f -not -path "./.git/*" -exec chmod 644 {} +
            find . -type d -not -path "./.git/*" -exec chmod 755 {} +
- Windows: o usuário precisa de permissão de leitura na pasta (e de escrita para editar o código).
  Conferir: icacls .
