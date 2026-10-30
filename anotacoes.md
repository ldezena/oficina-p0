# Anotações do curso

## Terminal
- pwd: mostra onde estou
- cd: entrar em uma pasta
- mkdir: criar pasta
- ni: criar arquivo
- rm: apagar arquivos e pastas completamente
- code .: abre o VS Code na pasta atual
- ls: mostra o que tem dentro da pasta atual (arquivos e pastas)
- cd ..: volta para a pasta de cima

## Git
- git status: mosta a situaçao do meu git
- git add nome-do-arquivo: adiciona só aquele arquivo
- git add .: adiciona tudo que mudou (olhar o status antes!)
- git init: liga com a maquina do tempo
- git commit: faz a foto do projeto que fica guardada no histórico
- git log: mostra o histórico das fotos (os commits)
- git config: muda configuraçoes do git
- git branch: mexe na linha do tempo (para renomear alguma coisa por exemplo) 
- git commit --amend: corrigi o ultimo commit antes de mandar pro github
- git remote add origin URL: conecta o PC ao GitHub (antes disso, o Git do PC não sabia que o repositório existia lá)
- git remote -v: lista os endereços remotos conectados
- git push -u origin main: envia os commits pro GitHub. O -u faz o Git lembrar pra onde mandar (só precisa na primeira vez)
- git push: envia os commits, depois que o -u já foi usado

## Erros que já vi

- `1s` / `pwm` → "El término '...' no se reconoce como nombre de un cmdlet"
  - O que significava: o comando não existe. Foi erro de digitação (1s em vez de ls, pwm em vez de pwd).
  - Lição: quando aparecer "no se reconoce", primeiro confira se escrevi o comando certo.

- `C:\Users\user\Documents` (caminho sozinho) → "no se reconoce como nombre de un cmdlet"
  - O que significava: o terminal lê a primeira palavra como uma ordem. Faltou o `cd` na frente.
  - Lição: pra ir a um lugar, sempre `cd` + caminho.

- `cd notas.txt` → "No se encuentra la ruta de acceso... porque no existe"
  - O que significava: o cd só entra em pastas, e notas.txt é um arquivo. O terminal procurou uma PASTA com esse nome.
  - Lição: às vezes o erro diz "não existe" quando a coisa existe, mas é do tipo errado.

- `git . add` → "'.' is not a git command"
  - O que significava: a ordem estava errada. No Git, o verbo vem logo depois de `git`.
  - Lição: formato certo é `git VERBO em-quê` (ex: `git add .`).

- `git commit --amend "mensagem"` → "error: pathspec '...' did not match any file(s) known to git"
  - O que significava: esqueci o -m. Sem ele, o Git achou que a minha frase era o nome de um arquivo, procurou e não achou nenhum arquivo com esse nome.
  - Lição: a mensagem do commit sempre vai depois do -m.

## VS Code

- `code .`: abre o VS Code na pasta atual (sem o ponto, pode abrir em outra pasta)
- Ctrl + S: salva o arquivo. Sem salvar, o Git não vê a mudança
- Bolinha branca na aba: arquivo não salvo
- `U` ao lado do arquivo: Untracked (arquivo novo que o Git ainda não acompanha)
- Tab: empurra a linha pra direita (recuo)
- Shift + Tab: puxa a linha pra esquerda
- Alt + seta pra cima/baixo: move a linha inteira
- Restricted Mode: só confiar em pastas que eu criei ou de alguém que conheço