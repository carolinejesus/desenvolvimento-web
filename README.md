# Empréstimos e Reservas de Materiais da Biblioteca
<!-- EXEMPLO: "Empréstimos e Reservas de Materiais da Biblioteca" -->

## 1) Problema
<!-- Escreva o problema sem falar de telas/tecnologias.
     Responda: Quem sofre? Onde? O que atrapalha? Por que isso importa?
     Em uma realidade alternativa, alunos precisam diariamente de livros para que possam acompanhar suas
     aulas. Como em uma turma de Desenvolvimento WEB existem 42 alunos e apenas 13 exemplares emprestáveis 
     do livro "Lógica de Programação e algoritmos com JavaScript", por exemplo, os alunos precisam rotacionar de uma 
     forma dinâmica a forma como pegam esse livro emprestado, tendo a possibilidade de ficarem com ele 
     durante um dia.
     O objetivo é criar um Sistema de Biblioteca Online, onde será permitida a reserva desses livros por alunos,
     fazendo com que sempre haja disponibilidade de material no acervo para os alunos que necessitem dele. Fazendo com 
     que a rotabilidade dos empréstimos seja mais fluida e organizada e todos os alunos consigam utilizar o material.
     O sistema estará dentro da "Minha biblioteca" institucional, então o aluno precisa estar regularmente matriculado 
     para ter acesso ao sistema e as telas de empréstimos e reservas, não precisando haver qualquer tipo de verificação 
     para confirmar que o aluno possui ou não matricula.
      -->
Em uma realidade alternativa, alunos precisam diariamente de livros para que possam acompanhar suas
     aulas. Como em uma turma de Desenvolvimento WEB existem 42 alunos e apenas 13 exemplares emprestáveis 
     do livro "Lógica de Programação e algoritmos com JavaScript", por exemplo, os alunos precisam rotacionar de uma 
     forma dinâmica a forma como pegam esse livro emprestado, tendo a possibilidade de ficarem com ele 
     durante um dia.
     O objetivo é criar um Sistema de Biblioteca Online, onde será permitida a reserva desses livros por alunos,
     fazendo com que sempre haja disponibilidade de material no acervo para os alunos que necessitem dele. Fazendo com 
     que a rotabilidade dos empréstimos seja mais fluida e organizada e todos os alunos consigam utilizar o material.
     O sistema estará dentro da "Minha biblioteca" institucional, então o aluno precisa estar regularmente matriculado 
     para ter acesso ao sistema e as telas de empréstimos e reservas, não precisando haver qualquer tipo de verificação 
     para confirmar que o aluno possui ou não matricula.

## 2) Atores e Decisores (quem usa / quem decide)
<!-- Liste papéis (não nomes).
     EXEMPLO:
     Usuários principais: Alunos regulamente matriculados, bibliotecários
     Decisores/Apoiadores: Bibliotecários -->
Usuários principais: Alunos regulamente matriculados, bibliotecários
Decisores/Apoiadores: Bibliotecários

## 3) Casos de uso (de forma simples)
<!-- Formato "Ator: ações que pode fazer".
     DICA: Use "Manter (inserir, mostrar, editar, remover)" quando for CRUD.
     EXEMPLO:
     Todos: Logar/deslogar do sistema; Manter dados cadastrais
     Aluno: Pode pesquisar livros e verificar quantos exemplares estão se disponíveis se o livro existir no acervo.
     Ele pode também fazer a reserva de um único exemplar, caso não esteja disponível e vai ficar em uma fila de espera
     para quando o material estiver disponível. Ele também pode emprestar um livro, deixando ele no seu nome para que 
     faça a retirada do material na biblioteca.
     Bibliotecários: Podem atulizar a quantidade de exemplares disponíveis no acervo, verificar a fila de espera, emprestam os materiais disponíveis, atualizam a fila e o status do material. 

      -->
Aluno: Pode pesquisar livros e verificar quantos exemplares estão se disponíveis se o livro existir no acervo.
Ele pode também fazer a reserva de um único exemplar, caso não esteja disponível e vai ficar em uma fila de espera
para quando o material estiver disponível. Ele também pode emprestar um livro, deixando ele no seu nome para que 
faça a retirada do material na biblioteca.
Bibliotecários: Podem atulizar a quantidade de exemplares disponíveis no acervo, verificar a fila de espera, emprestam os materiais disponíveis, atualizam a fila e o status do material.

## 4) Limites e suposições
<!-- Simples assim:
     - Limites = regras/prazos/obrigações que você não controla.
     - Suposições = coisas que você espera ter e podem falhar.
     - Plano B = como você segue com a 1ª fatia se algo falhar.

     O aluno pode pedir emprestado apenas um exemplar de cada material, podendo ficar com ele durante 24hrs. Ele pode
     fazer a devolução a qualquer momento, porém ele não pode renovar o livro no mesmo dia, para que possa haver a rotatividade
     esperada. Ele, no entando, pode reservar o livro e entrar na fila de espera para poder pegar outro exemplar. Caso vença a 
     data de devolução do material, o aluno ficará impossibilidade de fazer uma nova reserva ou empréstimo durante 24hrs.
     -->
O aluno pode pedir emprestado apenas um exemplar de cada material, podendo ficar com ele durante 24hrs. Ele pode
fazer a devolução a qualquer momento, porém ele não pode renovar o livro no mesmo dia, para que possa haver a rotatividade
esperada. Ele, no entando, pode reservar o livro e entrar na fila de espera para poder pegar outro exemplar. Caso vença a 
data de devolução do material, o aluno ficará impossibilidade de fazer uma nova reserva ou empréstimo durante 24hrs.

## 5) Hipóteses + validação
<!-- Preencha as duas frases abaixo. Simples e direto.
     EXEMPLO Valor: Se o aluno ver sua posição na fila, sente mais controle e conclui melhor a atividade.
     Validação: teste com 5 alunos; sucesso se ≥4 abrem/fecham chamado sem ajuda.
     EXEMPLO Viabilidade: Com app no navegador (HTML/CSS/JS + armazenamento local),
     criar e listar chamados responde em até 1 segundo na maioria das vezes (ex.: 9 de cada 10).
     Validação: medir no protótipo com 30 ações; meta: pelo menos 27 de 30 ações (9/10) em 1s ou menos. -->
H-Valor: Se [X], então [Y] melhora em [critério].  
Validação (valor): [teste rápido/observação]; alvo: [meta simples].

H-Viabilidade: Com [tecnologia], [ação/tela] leva até [n] s.  
Validação (viabilidade): [medição no protótipo]; meta: [n] s ou menos na maioria das vezes (ex.: 9/10).

## 6) Fluxo principal e primeira fatia
<!-- Pense “Entrada → Processo → Saída”.
     Fluxo principal:
     1) Aluno faz uma pesquisa de um material;
     2) Checa quantos materias estão disponíveis;
     3) Se tiver disponibilidade -> faz reserva pra retirar na biblioteca;
     4) Se não tiver mais exemplares -> faz reserva e entra na fila para retirada;
     5) Bibliotecário recebe notificação para fazer a liberação do material;
     6) Faz a entrega para o aluno do material;
     7) Depois de fazer o uso necessário, o aluno devolve o material;
     8) Bibliotecário atualiza o status do material devolvido ou o atribui para o próximo da fila.

     EXEMPLO de Fluxo:
     1) Aluno faz login
     2) Clica em "Pedir ajuda" e descreve a dúvida
     3) Sistema salva e coloca na fila
     4) Lista mostra ordem e tempo desde criação
     5) Professor encerra o chamado
     EXEMPLO de 1ª fatia:
     Inclui login simples, criar chamado, listar em ordem.
     Critérios de aceite (objetivos): criar → aparece na lista com horário; encerrar → some ou marca "fechado". -->
**Fluxo principal (curto):**  
1) [entrada do usuário] → 2) [processo] → 3) [salvar algo] → 4) [mostrar resultado]

**Primeira fatia vertical (escopo mínimo):**  
Inclui: [uma tela], [uma ação principal], [salvar], [mostrar algo]  
Critérios de aceite:
- [Condição 1 bem objetiva]
- [Condição 2 bem objetiva]

## 7) Esboços de algumas telas (wireframes)
<!-- Vale desenho no papel (foto), Figma, Excalidraw, etc. Não precisa ser bonito, precisa ser claro.
     EXEMPLO de telas:
     • Login
     • Lista de chamados (ordem + tempo desde criação)
     • Novo chamado (formulário simples)
     • Painel do professor (atender/encerrar)
     EXEMPLO de imagem:
     ![Wireframe - Lista de chamados](img/wf-lista-chamados.png) -->
[Links ou imagens dos seus rascunhos de telas aqui]

## 8) Tecnologias
<!-- Liste apenas o que você REALMENTE pretende usar agora. -->

### 8.1 Navegador
**Navegador:** [HTML/CSS/JS | React/Vue/Bootstrap/etc., se houver]  
**Armazenamento local (se usar):** [LocalStorage/IndexedDB/—]  
**Hospedagem:** [GitHub Pages/—]

### 8.2 Front-end (servidor de aplicação, se existir)
**Front-end (servidor):** [ex.: Next.js/React/—]  
**Hospedagem:** [ex.: Vercel/—]

### 8.3 Back-end (API/servidor, se existir)
**Back-end (API):** [ex.: FastAPI/Express/PHP/Laravel/Spring/—]  
**Banco de dados:** [ex.: SQLite/Postgres/MySQL/MongoDB/—]  
**Deploy do back-end:** [ex.: Render/Railway/—]

## 9) Plano de Dados (Dia 0) — somente itens 1–3
<!-- Defina só o essencial para criar o banco depois. -->

### 9.1 Entidades
<!-- EXEMPLO:
     - Usuario — pessoa que usa o sistema (aluno/professor)
     - Chamado — pedido de ajuda criado por um usuário -->
- [Entidade 1] — [o que representa em 1 linha]
- [Entidade 2] — [...]
- [Entidade 3] — [...]

### 9.2 Campos por entidade
<!-- Use tipos simples: uuid, texto, número, data/hora, booleano, char. -->

### Usuario
| Campo           | Tipo                          | Obrigatório | Exemplo            |
|-----------------|-------------------------------|-------------|--------------------|
| id              | número                        | sim         | 1                  |
| nome            | texto                         | sim         | "Ana Souza"        |
| email           | texto                         | sim (único) | "ana@exemplo.com"  |
| senha_hash      | texto                         | sim         | "$2a$10$..."       |
| papel           | número (0=aluno, 1=professor) | sim         | 0                  |
| dataCriacao     | data/hora                     | sim         | 2025-08-20 14:30   |
| dataAtualizacao | data/hora                     | sim         | 2025-08-20 15:10   |

### Chamado
| Campo           | Tipo               | Obrigatório | Exemplo                 |
|-----------------|--------------------|-------------|-------------------------|
| id              | número             | sim         | 2                       |
| Usuario_id      | número (fk)        | sim         | 8f3a-...                |
| texto           | texto              | sim         | "Erro ao compilar"      |
| estado          | char               | sim         | 'a' \| 'f'              |
| dataCriacao     | data/hora          | sim         | 2025-08-20 14:35        |
| dataAtualizacao | data/hora          | sim         | 2025-08-20 14:50        |

### 9.3 Relações entre entidades
<!-- Frases simples bastam. EXEMPLO:
     Um Usuario tem muitos Chamados (1→N).
     Um Chamado pertence a um Usuario (N→1). -->
- Um [A] tem muitos [B]. (1→N)
- Um [B] pertence a um [A]. (N→1)


<!-- 
Procurar todos os comandos npm's precisos para que possa rodar o node.js.
Também iniciar o trabalho, tentando utilizar o que já produzi em DOO com a biblioteca digital que ue criei.
Tentar fazer o mais simples possível para que não fique complicado de modificar e entender o fluxo.
Já possuo o problema e já sei mais ou menos como chegar na solução. O que o professor explicou na sala é facilmente
entendido com o chat, mas sempre daquele jeito: pede pra ele explicar e aprende a fazer sozinha.
Preciso fazer com que o que está rodando no VS suba automaticamente para o GitHub. Para isso, tenho que alterar a minha chave SSH
talvez até mesmo reconfigurar o Git.

Isso é para ser entregue até semana que vem. 
Tudo o que ele produz em sala de aula ele também adiciona ao repositório dele no Git e no SIGAA.
Precisa criar uma pasta src e um arquivo .gitignore, para dentro desta pasta ir adicionando arquivos que não precisam ir para o git.
 --># desenvolvimento-web
