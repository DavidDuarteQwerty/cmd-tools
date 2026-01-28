<h1 align="left">🔐 Gerador de Senhas Seguras</h1>

<p align="left">
  Utilitário em Python para gerar senhas aleatórias e seguras diretamente no terminal.<br>
  Permite definir o tamanho da senha e os tipos de caracteres a utilizar.
</p>

<hr>

<h2>🔍 O que é</h2>

<p>
<code>password-generator-python</code> é um pequeno programa de linha de comandos que cria senhas fortes de forma automática.<br>
Em vez de inventar senhas manualmente, o utilizador:
</p>

<ol>
  <li>Executa o programa no terminal</li>
  <li>Define o tamanho da senha</li>
  <li>Escolhe os tipos de caracteres (letras, números e símbolos)</li>
  <li>Recebe uma senha aleatória gerada de forma segura</li>
</ol>

<hr>

<h2>🎯 Objetivo</h2>

<p>
Este projeto foi desenvolvido como exercício prático em Python, com foco em:
</p>

<ul>
  <li>Validação de dados introduzidos pelo utilizador</li>
  <li>Manipulação de strings</li>
  <li>Geração de valores aleatórios seguros</li>
  <li>Organização de código em funções</li>
</ul>

<hr>

<h2>📂 Estrutura</h2>

<pre><code>password-generator-python/
├── gerador_senhas.py   &lt;-- script principal
└── README.md
</code></pre>

<hr>

<h2>⚙️ Script principal (gerador_senhas.py)</h2>

<p>
O script:
</p>
<ul>
  <li>Pede um tamanho de senha entre 8 e 64 caracteres</li>
  <li>Pergunta quais os conjuntos de caracteres a utilizar</li>
  <li>Gera a senha usando o módulo <code>secrets</code></li>
  <li>Garante pelo menos um caractere de cada tipo selecionado</li>
  <li>Apresenta a senha no ecrã</li>
</ul>

<hr>

<h2>🔒 Segurança</h2>

<p>
A geração das senhas utiliza o módulo <code>secrets</code>, recomendado para criação de credenciais e tokens,
em vez do módulo <code>random</code>, que não é indicado para fins criptográficos.
</p>

<hr>

<h2>📌 Requisitos</h2>

<ul>
  <li>Python 3.8 ou superior</li>
</ul>

<hr>

<h2>🛠️ Instalação</h2>

<ol>
  <li>Instalar o Python 3</li>
  <li>Clonar este repositório ou fazer download dos ficheiros</li>
  <li>Abrir um terminal na pasta do projeto</li>
</ol>

<hr>

<h2>🚀 Como usar</h2>

<ol>
  <li>Abrir o terminal</li>
  <li>Navegar até à pasta do projeto</li>
  <li>Executar o comando:
    <pre><code>python gerador_senhas.py</code></pre>
  </li>
  <li>Responder às perguntas apresentadas no ecrã</li>
</ol>

Exemplo de execução:

<pre><code>==================================
   GERADOR DE SENHAS SEGURAS
==================================
Tamanho da senha (8 a 64): 12
Incluir letras MAIÚSCULAS? (s/n): s
Incluir letras minúsculas? (s/n): s
Incluir números? (s/n): s
Incluir símbolos? (s/n): s

Senha gerada:
A7@kP2!qZ9#L
</code></pre>

<hr>

<h2>💡 Possíveis melhorias</h2>

<ul>
  <li>Gerar várias senhas numa única execução</li>
  <li>Copiar automaticamente a senha para a área de transferência</li>
  <li>Guardar senhas num ficheiro encriptado</li>
  <li>Criar uma interface gráfica</li>
</ul>

<hr>

<h2>📄 Licença</h2>

<p>
Projeto de uso livre para fins académicos e pessoais.
</p>
