<h2 align="center"> Manual da Ju sobre <img align="center" alt="git" width="75" img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-plain-wordmark.svg"> </h2>
<div align="justify">

<div align="justify">
:construction: Neste repositório estão comandos básicos para enviar um projeto para essa plataforma e também conta com alguns erros e as soluções que aprendi durante o uso do Git. </br>
</br>
⚙ <i>Esse repositório está em constante atualização.</i>

<h2 align="center"> Comandos Básicos 🧩 </h2>

- Esses dois comandos abaixo são para sua identificação no Git, esse comando só será realizado uma vez após a instalação do programa: </br>
<code>git config --global user.name "seu nome"</code></br>
<code> git config --global user.email "seu email de cadastro nessa plataforma"</code></br>

- O bloco de comandos abaixo são para realizar um primeiro commit para o seu repositório remoto no GitHub: </br>
<code>git init</code>    <i>(esse comando é para iniciar/criar um novo repositório Git)</i></br>
<code>git add .</code>   <i>(esse comando é para adicionar TODOS os arquivos ao repositório)</i></br>
<code>git commit -m "mensagem para seu commit"</code>   <i>(esse comando é para adicionar uma mensagem em seu commit)</i></br>
<code>git branch -M main</code><i>(esse comando é para renomear a branch, mesmo que já existe. ex.: se o nome da branch antes é <b>master</b>, após esse comando será chamada de <b>main</b> **nome da branch)</i></br>
<code>git remote add origin git@github.com:seu-usuario/seu-repositorio.git</code> <i>(esse comando estabelece conexão entre o repositótio local e um remoto)</i></br>
<code>git push -u origin main</code><i>(esse comando é para subir modificação para repositório remoto conectado com o comando anterior **nome da branch)</i></br>

- Os comandos para utilizar, conforme a necessidade: </br>
<code>git add *</code> <i>(esse comando é para adicionar os arquivos novos/modificados ao repositório)</i></br>
<code>git add nome-arquivo</code> <i>(esse comando é para adicionar um arquivo específico ao repositório)</i></br>
<code>git clone git@github.com:seu-usuario/seu-repositorio.git</code><i>(esse comando cria uma cópia de um repositório já existente)</i></br>
<code>git checkout main</code><i>(esse comando é trocar de ramificação para outra **nome da branch)</i></br>

<h2 align="center"> Erros e Soluções ⚠️ </h2>

- <b> Erro encontrado: </b>  
<code>! [rejected]        master -> master (fetc h first) </code> <br>
<code> error: failed to push some refs to 'git@github.com:abc/abc.git'"</code> [...]

- <b> Solução #1 - Melhor encontrada: </b> <i>Digitar os seguintes comandos abaixo:</i><br> 
<code> git fetch origin master:tmp </code> ➡️<code> git rebase tmp </code> ➡️<code> git push origin HEAD:master </code> ➡️<code> git branch -D tmp </code>

- <b> Solução #2 - Cuidado! * </b> <i>Digitar o seguinte comando abaixo:</i><br>
<code>git push origin master --force</code>

<i> * Se alguém tiver construpido em cima de sua história original, euquanto você está <b>rebasing</b> (processo de mover ou combinar uma sequência de commits para um novo commit base), a branch no controle remoto pode avançar com seu compromisso, e cegamente empurrar com </i><b>-- force</b><i> perderá seu trabalho.</i>
 
##
