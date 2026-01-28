<h1 align="left">⚙️ Cmd-Tools</h1>

<p align="center">
<p align="left">
  Ferramentas CMD para Windows.<br>
  Digite <code>ferramentas</code> no CMD e escolha, por número, qual script Python executar.
</p>



<h2>🔍 O que é</h2>

<p>
<code>cmd-tools</code> é um atalho para os seus scripts Python no Windows.<br>
Em vez de navegar por pastas e escrever comandos longos, você:
</p>

<ol>
  <li>Abre o CMD</li>
  <li>Escreve <code>ferramentas</code></li>
  <li>Escolhe um número na lista</li>
  <li>O script <code>.py</code> é executado automaticamente</li>
</ol>

<hr>

<h2>📂 Estrutura básica</h2>

<pre><code>ferramentas/              &lt;-- pasta adicionada ao PATH
├── ferramentas.bat       &lt;-- menu principal
├── conversor_imagem.py   &lt;-- exemplo de script
├── outro_script.py
└── ...
</code></pre>

<hr>

<h2>⚙️ Script principal (ferramentas.bat)</h2>

<p>
Exemplo simples de ficheiro <code>ferramentas.bat</code> que:
</p>
<ul>
  <li>entra na pasta onde ele está</li>
  <li>lista todos os <code>.py</code></li>
  <li>mostra um menu numerado</li>
  <li>executa o script escolhido com <code>python</code></li>
</ul>

<pre><code>@echo off
cd %~dp0

setlocal enabledelayedexpansion
cls
echo Lista de ferramentas (.py)
echo.

set i=0
for %%f in (*.py) do (
    set /a i+=1
    set file!i!=%%f
    echo !i!. %%f
)

echo.
set /p escolha=Escolha o numero: 

if not defined file%escolha% (
    echo.
    echo Opcao invalida.
    pause
    exit /b
)

set ficheiro=!file%escolha%!

echo.
echo A executar: %ficheiro%
echo.

python "%ficheiro%"

endlocal
exit /b
</code></pre>

<hr>

<h2>🛠️ Instalação</h2>

<ol>
  <li>Crie uma pasta, por exemplo: <code>C:\Users\SEU_NOME\ferramentas</code></li>
  <li>Coloque dentro dessa pasta:
    <ul>
      <li>o ficheiro <code>ferramentas.bat</code></li>
      <li>os seus scripts <code>.py</code></li>
    </ul>
  </li>
  <li>Adicione essa pasta ao <strong>PATH</strong> do Windows:
    <ul>
      <li>Abrir “Variáveis de Ambiente”</li>
      <li>Editar a variável <code>Path</code> do utilizador</li>
      <li>Adicionar o caminho da pasta <code>ferramentas</code></li>
    </ul>
  </li>
  <li>Fechar todas as janelas do CMD e abrir uma nova</li>
</ol>

<hr>

<h2>🚀 Como usar</h2>

<ol>
  <li>Abrir o CMD</li>
  <li>Escrever: <code>ferramentas</code></li>
  <li>Ver a lista numerada de scripts <code>.py</code></li>
  <li>Digitar o número da ferramenta que quer executar</li>
</ol>

Exemplo de saída:

<pre><code>Lista de ferramentas (.py)

1. conversor_imagem.py
2. limpar_temp.py
3. gerar_relatorio.py

Escolha o numero: 1
A executar: conversor_imagem.py
</code></pre>

<hr>

<h2>💡 Ideias de scripts</h2>

<ul>
  <li><code>conversor_imagem.py</code> – converter PNG para JPG</li>
  <li><code>limpar_temp.py</code> – apagar ficheiros temporários</li>
  <li><code>organizar_downloads.py</code> – organizar a pasta Downloads por tipo</li>
  <li><code>backup_projeto.py</code> – fazer backup rápido de uma pasta</li>
</ul>
