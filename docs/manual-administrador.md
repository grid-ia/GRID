# Manual do Administrador — GRID

> Guia do **administrador de um site GRID**: a pessoa que responde pelo site da sua empresa.
> Cobre o que **só o administrador** faz — equipe, acesso, configuração, cofre,
> armazenamento, fluxos de trabalho, integrações e governança da IA — e a visão de conjunto
> da plataforma.
>
> - **Para criar as suas tabelas e telas**, o passo a passo está no
>   **[Guia do Construtor](./manual-construtor.md)**.
> - **Para o uso diário** de cada tela, veja o **[Manual do Usuário](./manual-usuario.md)**.
> - **Se o seu site usa o pacote jurídico**, veja também o
>   **[Manual do Pacote Jurídico](./manual-pacote-juridico.md)**.

---

## Sumário

**Parte I — Visão geral**
1. [O papel do administrador](#1-o-papel-do-administrador)
2. [Como o GRID é organizado: núcleo, construtor e pacotes](#2-como-o-grid-é-organizado-núcleo-construtor-e-pacotes)
3. [Onde o seu site roda](#3-onde-o-seu-site-roda)

**Parte II — Equipe e acesso**
4. [Trazer a equipe: convites e cadastro](#4-trazer-a-equipe-convites-e-cadastro)
5. [Gestão de usuários](#5-gestão-de-usuários)
6. [Modelo de acesso](#6-modelo-de-acesso)
7. [Usuários validados](#7-usuários-validados)
8. [Segurança de login](#8-segurança-de-login)

**Parte III — Configuração**
9. [Modo Esboço: layout, campos e níveis de acesso](#9-modo-esboço-layout-campos-e-níveis-de-acesso)
10. [Menu dinâmico](#10-menu-dinâmico)
11. [Cofre de credenciais](#11-cofre-de-credenciais)
12. [Armazenamento de documentos, volumes e lixeira](#12-armazenamento-de-documentos-volumes-e-lixeira)

**Parte IV — Construir e automatizar**
13. [Construir telas sem programar](#13-construir-telas-sem-programar)
14. [Fluxos de trabalho](#14-fluxos-de-trabalho)
15. [Integrações: automações externas e acesso por IA (MCP)](#15-integrações-automações-externas-e-acesso-por-ia-mcp)
16. [Comunicação (e-mail, WhatsApp)](#16-comunicação-e-mail-whatsapp)

**Parte V — Inteligência artificial**
17. [Governança do Assistente de IA](#17-governança-do-assistente-de-ia)

**Parte VI — Governança**
18. [Privacidade, Termos e LGPD](#18-privacidade-termos-e-lgpd)
19. [Checklist do administrador](#19-checklist-do-administrador)

---

# Parte I — Visão geral

## 1. O papel do administrador

O **administrador** concentra poderes que nenhum outro usuário tem:

- **Vê e edita todos os registros**, de todos os usuários.
- **Traz e gerencia a equipe** — convites, contas, ativação.
- **Constrói o sistema** — cria tabelas e telas, liga recursos e regras automáticas
  (com o `@architectus`), desenha fluxos de trabalho.
- **Ajusta telas e níveis de acesso** (Modo Esboço).
- **Guarda os segredos do site** no cofre — IA, e-mail, armazenamento, integrações.
- **Governa o Assistente de IA** — as regras inegociáveis que valem para todos.

O cabeçalho do administrador tem atalhos próprios: o botão **Convidar alguém** e, no menu **☰** (canto
direito), uma fileira de ícones — **cofre** (cadeado), **Administração de I.A.** (só onde há um AnythingLLM
instalado), **Importar planilha**, **Esboço**, **Fluxos de trabalho**, **Integrações**, **Lixeira** e o **worker de
limpeza da lixeira** (pausar/iniciar). O menu lateral ganha **Personalização**, com as
tabelas de configuração (seção 10), e o menu **Ajuda** abre os **três** manuais: Usuário, Administrador e
Construtor.

> Trate a senha do administrador como a chave mestra do site: ela protege o cofre e não há
> como recuperar o cofre sem ela (seção 11).

---

## 2. Como o GRID é organizado: núcleo, construtor e pacotes

O GRID é uma **plataforma geradora de aplicações**. Cada site é composto de três camadas:

| Camada | O que é | Quem decide |
|---|---|---|
| **Núcleo** | O que todo site tem: **Usuários**, **Pessoas**, **Casos** com **Partes** e **Papéis**, **Tarefas** (Kanban) com **fluxos de trabalho**, **Documentos**, **Meus Painéis**, **Minha Agenda** e o **Assistente de IA**. | Vem pronto. |
| **Suas tabelas** | Cadastros criados pelo administrador conversando com o `@architectus` ou importando planilhas, cada um com tela de lista, exibição, cadastro e edição, e com os recursos que você ligar: **Documentos, Tarefas, Quadro, Calendário, Painéis, Regras automáticas**. | Você (Guia do Construtor). |
| **Pacotes de área** | Módulos inteiros de um setor, com vocabulário e telas próprias. Hoje: o **pacote jurídico** (processos, andamentos dos tribunais, cobrança). | Escolhidos na criação do site. |

O que isso significa na prática:

- **Os nomes são seus.** O rótulo que você dá a uma tela ou campo vale para todos os usuários
  e **prevalece sobre a tradução padrão**. Um site pode chamar o Caso de "Atendimento".
- **Tudo é descrito por dados, não por código.** Por isso uma tela nova aparece em segundos,
  já com permissões, busca pela lupa, filtros, documentos e consulta pelo assistente.
- **Tudo passa pelas mesmas regras de acesso**: telas prontas, telas criadas e consultas da IA.

---

## 3. Onde o seu site roda

- **Site GRID na nuvem** (por exemplo, `grid.ia.br`): cada site é **isolado** dos demais —
  banco de dados próprio, usuários próprios — e é criado pela equipe do GRID com o plano
  contratado (cota de casos, convites, modelo de acesso).
- **Instalação dedicada**: o GRID roda na infraestrutura do cliente, com os mesmos recursos.

Configurações **do plano**, alteradas pelo suporte (não pelas telas): o **modelo de acesso**
(seção 6), a **cota de casos**, o número de **convites**, os **limites do construtor** e se o site
**exige uma Pessoa para cada usuário** (seção 4).

O **pacote jurídico** tem modos de implantação próprios (sobre um sistema jurídico existente);
veja o Manual do Pacote Jurídico.

---

# Parte II — Equipe e acesso

## 4. Trazer a equipe: convites e cadastro

Um site funciona de uma de duas formas:

**Somente por convite (padrão em sites novos).**
1. No cabeçalho, **"Convidar alguém"** → e-mail da pessoa → **"Enviar convite"**.
2. A pessoa recebe um **código** que só vale para aquele e-mail e expira em **2 dias**.
3. Ela escolhe "Registre-se", informa e-mail e código e define a senha.

- A janela mostra os **convites restantes**; um convite só é gasto se o e-mail sai.
- **Um e-mail pertence a um único site**: "Esse e-mail já tem uma conta" encerra ali.
- Muitos códigos errados **bloqueiam** aquele e-mail para cadastro; o desbloqueio é pelo
  suporte.
- Nada do convite fica guardado para ser roubado: o código é verificado matematicamente.

**Cadastro livre.** Em sites de demonstração ou captação, a pessoa clica em "Registre-se
gratuitamente", confirma o e-mail por código e recebe uma senha provisória.

**Pessoa obrigatória.** Num site configurado para exigir uma Pessoa por usuário, o formulário de registro
pede o **endereço residencial** (CEP, endereço, número, bairro, cidade e UF), o GRID cria a **Pessoa** junto
com a conta e **você é avisado** — por e-mail e pelo sino de **Notificações** — de cada pessoa nova. Quem já
tinha conta (e o próprio administrador) ganha uma Pessoa mínima, com nome e e-mail, no primeiro acesso.

**Site de avaliação (imagem pública).** Não há convites: o botão **Convidar alguém** não aparece, o cadastro é
livre (até **3 usuários**), a senha provisória aparece **na tela** e a Pessoa de cada usuário é criada no
cadastro (a do administrador, no primeiro acesso). Quem esquecer a senha: **Usuário → Editar → Redefinir senha do
usuário** e repasse a nova senha provisória que aparece na tela.

Boas práticas: confirme o e-mail correto (é o login e o canal dos códigos) e oriente a equipe a
usar **"Esqueci minha senha"** em vez de criar outra conta.

---

## 5. Gestão de usuários

A tela **Usuários** é exclusiva do administrador. O registro de usuário guarda dados pessoais e
**colunas de permissão** (administrador, tipo, nível, perfil):

- **Nenhum usuário edita as próprias permissões**; só o administrador.
- **O vínculo entre a conta e a Pessoa é feito só pelo sistema.** Nem o usuário nem o administrador o
  alteram: apontar uma conta para a Pessoa de outro a faria agir como ele (suas tarefas, suas equipes, seus
  registros no acesso por equipe).
- **Ativar/Inativar** — um usuário inativo não entra (nem pelo Google). Para quem sai da
  equipe, **inative**: os registros da pessoa continuam no sistema. Na tela do usuário, marque **Usuário inativo**. Nos sites que exigem uma Pessoa para cada usuário (como o de
  avaliação) a tela de usuário não tem **Novo** nem **Excluir**: as contas nascem do cadastro e saem por inativação.
- Nos sites por convite, as contas são criadas pelo próprio convite; o administrador cuida
  do resto.

> Conceder o papel de administrador dá acesso a **todos os dados e ao cofre**. Faça isso só para
> quem precisa.

---

## 6. Modelo de acesso

O GRID combina **duas camadas**.

### Camada 1 — De quem é o registro

Cada registro guarda **quem o criou**. O site usa um de três modelos (definido no plano):

**Acesso compartilhado (padrão em sites novos)**

| Quem está logado | Registro criado por… | Vê? | Edita? |
|---|---|---|---|
| Administrador | qualquer pessoa | ✅ | ✅ |
| Usuário | qualquer membro da equipe | ✅ | ✅ |
| Usuário | o **administrador** | ✅ | ❌ somente leitura |

**Acesso individual** (padrão do pacote jurídico)

| Quem está logado | Registro é… | Vê? | Edita? |
|---|---|---|---|
| Administrador | qualquer | ✅ | ✅ |
| Usuário | do administrador (compartilhado) | ✅ | ❌ |
| Usuário | **seu** | ✅ | ✅ |
| Usuário | de **outro usuário** | ❌ | ❌ |

**Acesso por equipe** — os colegas de equipe trabalham juntos (veja o fim da seção 14)

| Quem está logado | Registro criado por… | Vê? | Edita? |
|---|---|---|---|
| Administrador | qualquer pessoa | ✅ | ✅ |
| Usuário | ele mesmo | ✅ | ✅ |
| Usuário | alguém que **divide uma equipe** com ele | ✅ | ✅ |
| Usuário | o **administrador** | ✅ | ❌ somente leitura |
| Usuário | alguém de outra equipe | ❌ | ❌ |

Nos três modelos:
- **O que o administrador cria é referência da empresa**: todos leem, só ele altera. Use isso
  para listas que a equipe não deve mexer (Papéis, tabelas de preço).
- **Quando o administrador edita o registro de alguém, o registro continua sendo da pessoa.**

> O que a equipe enxerga: no acesso **por equipe**, as equipes da seção 14 também decidem a
> visibilidade dos **registros**. Nos outros dois modelos elas organizam só **tarefas e fluxos**.

### Camada 2 — Nível de acesso por tela e por campo

| Nível | Significado |
|---|---|
| **0** | Só o administrador vê e edita. A tela nem aparece no menu dos demais. |
| **1** | Todos veem; só o administrador edita. |
| **2** (padrão) | Todos veem e editam. |
| **3** / **4** | Iguais a 1 / 2, mas **só para usuários validados** (seção 7). |

O **nível da tela** decide se a pessoa lista/abre e usa Novo/Editar/Excluir; a **Camada 1**
decide **qual** registro. O bloqueio vale na tela, na URL direta e nas consultas da IA — nada o
contorna. Ajuste pelo **Modo Esboço** (seção 9).

---

## 7. Usuários validados

Uma marcação que o administrador concede a contas de confiança. Os níveis **3** e **4** só
valem para elas; uma tela marcada assim é bloqueada na entrada para os demais. Use para abrir
gradualmente telas sensíveis.

---

## 8. Segurança de login

| Situação | Comportamento |
|---|---|
| Senha incorreta | Conta o erro. |
| Após poucas tentativas | O login exige também um **código de 6 dígitos** por e-mail. |
| A cada 3 falhas | **E-mail de aviso** com as tentativas restantes. |
| Muitas tentativas | **Conta bloqueada**; recuperação por "Esqueci minha senha". |
| "Esqueci minha senha" | Senha temporária, desbloqueio e contador zerado. |

- O código tem **validade curta** e é descartado após alguns erros.
- Contas **inexistentes** nunca disparam bloqueio nem e-mail (evita descobrir quem é usuário).
- Campos de senha e código **não aceitam colar**.
- Cadastrar-se com o **CPF/CNPJ** de outra pessoa não toma o cadastro dela: reivindicar exige o
  e-mail verificado.

---

# Parte III — Configuração

## 9. Modo Esboço: layout, campos e níveis de acesso

O interruptor **"Esboço"** no cabeçalho (nas telas de exibição) personaliza **qualquer tela**,
pronta ou criada por você, sem programação:

- **Reordenar campos** e movê-los entre **visível** e **invisível**.
- **Renomear painéis** (lápis no título do grupo).
- **Nível de acesso de cada campo** (0 → 1 → 2 → 3 → 4).

Cada campo mostra marcas: **tipo** (texto, inteiro, decimal, data, sim/não, medidor, chave
estrangeira…), **cadeado** (campo do sistema, fixo), **chave**, **filtro** e **FK →** (aponta
para outra tabela). **Salvar** ou **Descartar** na barra do Esboço; vale para toda a equipe.

> O **primeiro campo** de cada cadastro é o rótulo mostrado em **todas as listas de seleção**
> que apontam para ele. O sistema avisa se você escolher um campo incomum para esse papel.

---

## 10. Menu dinâmico

O menu lateral é montado **sozinho**, para cada usuário:

- Cada tela entra no **grupo** definido para ela ("Cadastros", "Agenda e Tarefas"…); "/" cria
  subgrupos ("Cadastros/Financeiro").
- Telas de **nível 0** somem para quem não é administrador; tudo o que está em **Personalização** (e
  grupos com "Tabelas" no nome) é configuração e só o administrador vê.
- Uma tabela cujo grupo tem **o nome de outra tabela** vira **painel dentro dela** em vez de
  item de menu — é assim que as Partes aparecem dentro do Caso.
- A **Personalização** reúne as telas de configuração, visíveis só para o administrador, por assunto:
  **Equipe** (Equipe Agenda e suas listas, Célula, Função, Unidade, Matéria), **Evento** (Evento,
  Próximo evento, Encadeamento, Motivo, Situação, Prazo, Tipo de contagem, Workflow), **Caso** (Fases,
  Papel), **Financeiro** (Conta contábil), **Documento** (Tipo de documento), **Usuário** e **Preferências**.
- As tabelas que você cria entram em **Cadastros**, ou no grupo que você pedir ao
  `@architectus` (Guia do Construtor).

Para dar ou tirar uma área de um perfil, ajuste o **nível de acesso** da tela.

---

## 11. Cofre de credenciais

O **cofre** (cadeado no cabeçalho, `/admin/vault`) guarda **todos os segredos do site**,
**cifrados**. Exclusivo do administrador.

> **Zero-conhecimento:** só a senha do administrador abre o cofre — nem a equipe do GRID.

1. **Criar** — na primeira vez, com a sua senha de administrador.
2. **Desbloquear** — após reiniciar o servidor (no modo por senha), informe a senha. Com o cofre
   bloqueado, leituras e gravações ficam suspensas para todos, com aviso.
3. **Bloquear** — volta ao estado protegido.

> ⚠️ **Não há recuperação da senha do cofre.** Em instalações próprias, prefira o desbloqueio
> automático por chave gerenciada (KMS).

Os segredos são **somente-escrita** (aparece "••••••" quando definido):

| Grupo | Exemplos |
|---|---|
| **Banco de dados** | Host, nome, usuário e senha (aplicado ao reiniciar). |
| **Armazenamento** | Provedor (sistema de arquivos, Google Cloud Storage, Amazon S3, Azure), bucket, credencial, prefixos de volume. |
| **IA** | Provedor, modelo e chave do site; chave de embeddings. |
| **Comunicação** | SMTP, token do WhatsApp. |
| **Serviço** | Usuário de serviço e parâmetros de módulos. |
| **Integrações e ambiente** | Chaves de APIs externas, antivírus. |
| **Login com Google** | Client ID e chave de proteção do SSO. |

Use **Testar conexão** em cada grupo antes de confiar numa credencial. Ao **bloquear** o cofre você pode
informar uma nova senha para trocar a dele.

---

## 12. Armazenamento de documentos, volumes e lixeira

Os documentos ficam em **quatro volumes**, do mais quente ao mais frio:

| Volume | Disponibilidade |
|---|---|
| **Padrão** | Instantânea. |
| **Congelado** | Instantânea por um período. |
| **Coldline** | Exige **restauração** (tempo e custo). |
| **Arquivo** | Restauração mais demorada. |

- Defina **provedor** e **prefixos** no cofre; trocar de provedor **não migra** o que já existe. No **site de
  avaliação** o armazenamento é só o disco local (sem Google Cloud, Amazon S3 ou Azure).
- **Mover entre volumes** arquiva o que é antigo; um pedido de restauração pendente nunca se
  perde.
- **Antivírus (opcional):** cada arquivo enviado é verificado em segundo plano; infectado vira
  **erro** (vermelho) e fica bloqueado.
- **Lixeira** (ícone no cabeçalho): documentos excluídos ficam recuperáveis por um tempo; uma
  rotina noturna esvazia o que venceu. O ícone mostra se essa rotina está ativa e permite
  pausá-la.

---

# Parte IV — Construir e automatizar

## 13. Construir telas sem programar

Com o **`@architectus`** no chat, o administrador:

- **cria tabelas** descrevendo-as em linguagem natural (plano → aprovação → criação);
- **importa planilhas** (xlsx/csv) como tabelas novas, com os dados;
- **liga recursos** em cada tabela: Documentos, Tarefas, Quadro, Calendário, Painéis e
  **Regras automáticas**;
- **acrescenta campos**, **renomeia**, **muda o grupo do menu** e **exclui** tabelas.

O passo a passo completo, com exemplos, está no **[Guia do Construtor](./manual-construtor.md)**.

---

## 14. Fluxos de trabalho

O **desenhista de fluxos** (ícone **"Fluxos de trabalho"** no cabeçalho, `/admin/workflows`)
transforma um processo de várias etapas em tarefas que andam sozinhas.

**Os blocos**

| Bloco | O que faz |
|---|---|
| **Etapa de pessoa** (tarefa de usuário) | Uma tarefa para alguém: evento, responsável, prazo e as **situações** permitidas (concluir, reagendar…). |
| **Decisão** | Escolhe o caminho conforme uma condição sobre os dados do fluxo. |
| **Ação do sistema** (ação automática) | Faz algo sem ninguém: define variáveis, cria registros, aciona uma integração. |
| **Desvio** (ir para) | Salta para outro ponto do fluxo. |

**Como um fluxo começa.** Ele é ligado a um ou mais **eventos** (tipos de tarefa). Quando
alguém cria uma tarefa de um desses eventos, o fluxo inicia, e cada etapa aparece no **Quadro de
Tarefas** do responsável. Um fluxo sem evento ligado **nunca roda**.

**Validar e Salvar** fazem a mesma verificação — não existe "salvar com avisos". O desenhista
**executa** o que você montou e recusa: caminho sem saída, decisão sem o "senão", etapa
inalcançável, ciclo sem nenhuma pessoa (que rodaria para sempre) e evento inexistente.

Também é possível **ver** qualquer fluxo em andamento a partir da tarefa (todos veem; só quem
pode editar fluxos altera), e **exportar** um fluxo como diagrama BPMN.

### Quem recebe cada etapa: equipes, células e o candidato

A organização do trabalho tem três ideias, todas cadastradas como dados (sem programação):

| Conceito | O que é |
|---|---|
| **Equipe** | Uma **pessoa** (cadastrada em Pessoas, ex.: "Equipe Comercial") que tem **membros**. Cada membro tem um **papel** — o número do papel é o **nível**: quanto maior, mais acima na equipe. |
| **Célula** | Um agrupamento de trabalho (ex.: Comercial, Pós-venda, Financeiro) ao qual as equipes pertencem. É o que a etapa de um fluxo usa para escolher o destino. |
| **Papel** | A função do membro na equipe (Analista, Coordenador…). Define também quem **supervisiona** quem. |

O campo **Candidato** de cada etapa do fluxo diz **para quem a etapa vai** quando é criada:
**quem pediu**, **a pessoa do pedido**, **o responsável**, **a célula**, **a equipe**, **definido pelo próprio
fluxo** (uma ação automática escolhe), ou o primeiro responsável do caso (pacote de área). Na célula e na equipe,
o GRID busca a equipe mais específica para o caso e **cria a etapa em nome da equipe, sem responsável**.

**Como a equipe trabalha a etapa**
1. A etapa aparece, sem responsável, para **todos os membros** (visão *Monitoradas por mim*).
2. O primeiro membro que **salva ou conclui** a etapa **assume** a responsabilidade por ela.
3. Coordenadores (papel mais alto) acompanham as tarefas **atribuídas** aos membros de papel mais baixo.
4. Se a equipe tiver uma **regra de desempate**, ela escolhe um responsável automaticamente em tarefas
   simples, no passo-a-passo e no encadeamento: por evento, nenhuma, primeiro responsável, responsável do
   caso, sorteio na função ou sorteio geral, ou o usuário ativo. **Na criação de uma etapa de fluxo, nunca
   há sorteio** — a etapa fica livre e um membro a assume.

**Quando não há candidato.** Se a célula/equipe não resolve ninguém, a etapa vai para **quem pediu** o fluxo
(ou, conforme as **Preferências** do site, para o dono do caso) e o histórico registra o motivo
"Não foi possível definir o candidato da tarefa". Revise esse histórico: etapa em nome do solicitante em
vez da equipe indica célula ou equipe sem membros.

**Montar a organização (passo a passo)**
1. Cadastre cada equipe como **Pessoa** (ex.: "Equipe Pós-venda").
2. Em **Equipes**, crie a equipe ligando-a à Pessoa e à **Célula**.
3. Cadastre os **Papéis** (ex.: Analista = 6, Coordenador = 7) e inclua cada **membro** com seu papel.
4. Na etapa do fluxo, escolha **Candidato = Célula** (ou Equipe) e informe qual.
5. Confirme que cada membro tem **usuário ligado à sua Pessoa** — sem isso ele não vê nem assume a tarefa.

Os sites de demonstração já trazem um exemplo pronto: três equipes (Comercial, Pós-venda, Financeiro), uma
célula cada, um analista por equipe e o dono do site como coordenador das três. O **site de avaliação** começa
sem equipes nem células.

> **Regra ou fluxo?** Uma **regra automática** reage a um registro salvo ("se ficou pronto, crie
> uma tarefa"). Um **fluxo** organiza uma sequência de etapas, pessoas e decisões.
>
> Fluxos que vieram com o site e foram escritos em código aparecem **bloqueados** no desenhista:
> podem ser vistos, não alterados.

> **Onde montar a árvore.** Em **Personalização → Equipe → Célula** (tela *Grupo de Trabalho*), com
> **Editar**: crie células, equipes e membros na própria árvore. Cada membro mostra o **papel** e a marca
> **Pode atribuir** (a pessoa pode receber tarefas). O GRID **recusa** o mesmo membro duas vezes na mesma
> equipe, com uma mensagem clara.

> **Grupo de Trabalho mostra o que o fluxo enxerga.** Ao lado de cada equipe a árvore exibe os
> critérios que o fluxo usa para escolher a equipe (unidade, grupo, matéria e fase; **Geral** quando
> não há nenhum) e o **desempate** aplicado quando mais de um membro atende.

### Quem vê e altera os registros: o escopo de propriedade

Cada registro guarda quem o gravou. O site escolhe, na instalação, como isso limita o acesso:

| Escopo | Lê | Altera |
|---|---|---|
| **Compartilhado** | todos os registros do site | qualquer um, exceto os do Administrador |
| **Por usuário** | os próprios e os do Administrador | só os próprios |
| **Por equipe** | os seus, os de quem divide equipe com você e os do Administrador | os seus e os de quem divide equipe com você |

No escopo **por equipe** vale a árvore da tela **Grupo de Trabalho** (Célula → Equipe → Pessoa):
quem está numa mesma equipe enxerga e altera o trabalho um do outro, e a mudança de uma pessoa
de equipe vale em até 30 segundos. Quem não tem pessoa vinculada, ou não está em nenhuma equipe,
vê só o que é seu. Registros do Administrador ficam sempre somente leitura para os demais. **O
Administrador lê e altera tudo, em qualquer escopo.** A troca de escopo é feita pela equipe do
GRID na instalação (`tenantctl settings --owner-scope`).

---

## 15. Integrações: automações externas e acesso por IA (MCP)

A tela **Integrações** (ícone no cabeçalho, `/admin/integrations`) liga o GRID a outros
sistemas.

**Eventos de integração.** Uma etapa de fluxo pode **avisar** um sistema externo (por exemplo,
uma automação n8n que envia WhatsApp ou cria um lead) ou **aguardar** a resposta dele antes de
seguir. O GRID continua dono do fluxo: o sistema externo é acionado por uma etapa e devolve o
resultado, nunca decide sozinho. Cada envio é assinado, registrado e pode ser reenviado da tela.

**Consentimento (LGPD).** Mensagens a pessoas exigem **consentimento registrado**. Sem registro,
não há envio — a ausência de consentimento é tratada como recusa —, e um pedido de saída é
respeitado na hora.

**Acesso por IA (MCP).** Você emite **tokens** para que assistentes externos (Claude, ChatGPT,
n8n…) usem as ferramentas do GRID como um usuário: o token tem **exatamente** as permissões do
usuário a que pertence, nada além. Revogue um token quando não for mais usado.

**Para cada pessoa da equipe** (sem configuração do administrador): assinatura de agenda (ICS) e
sincronização com o Google Agenda — veja o Manual do Usuário, seção 12.

---

## 16. Comunicação (e-mail, WhatsApp)

- **E-mail** é usado em todo o sistema: convites, códigos de segurança, senhas provisórias,
  avisos. Depende do **SMTP** no cofre. O **site de avaliação** não tem e-mail: nenhuma tela envia mensagens, e
  senhas e avisos aparecem na tela. Garanta MX, SPF, DKIM, DMARC e PTR do domínio.
- **WhatsApp** pela API oficial da Meta, com o token no cofre: texto dentro da janela de
  conversa aberta pelo contato; mensagens proativas exigem modelo aprovado pela Meta. O envio
  automático passa pelos eventos de integração (seção 15).

---

# Parte V — Inteligência artificial

## 17. Governança do Assistente de IA

O assistente segue **documentos de regras** que o próprio site mantém, editáveis como texto.

### A estrutura de conduta

| Documento | Papel |
|---|---|
| **Identidade** (`Agent.md`) | Quem é o assistente e seu tom. |
| **Regras inegociáveis** (Guardrails) | O que ele **nunca** pode fazer. |
| **Regras de comportamento** (Rules) | Regras por área. |
| **Habilidades** (Skills) | O que ele sabe fazer. |

O site tem três conjuntos, nos documentos do administrador:

- **o assistente do site** (pastas da raiz) — vale para todos e é a base de `@assistens`;
- **o `@architectus`** (pasta `Architectus/`) — o construtor; só o administrador o usa;
- **o agente pessoal** de cada usuário (`@Agent`), nos documentos de cada um.

### Como o administrador governa

- **Edite pelo Explorador** de Meus Documentos, como texto comum.
- **As regras inegociáveis do site têm prioridade absoluta** sobre qualquer personalização. Um
  usuário pode **acrescentar** restrições ao seu agente, **nunca afrouxar** as do site.
- **Personalizar não dá poder.** Nenhum agente ganha ferramentas que o usuário não tem.
- **Atualizações do GRID.** Quando uma nova versão traz instruções melhores para o
  `@architectus`, o GRID substitui os arquivos que você **não editou**; os que você editou
  ficam como estão (e o registro do servidor avisa).

### Quando cada documento entra na conversa

| Documento | Limitado | Chave do site | Chave própria |
|---|:--:|:--:|:--:|
| **Regras inegociáveis** do site | ✅ | ✅ | ✅ |
| **Habilidades** do usuário | — | ✅ (inteiras na 1ª mensagem; depois sob demanda) | ✅ |
| **Regras de comportamento** do site | — | — | ✅ |
| **Identidade** do usuário | — | — | ✅ |
| `@assistens` / `@Agent` | — | — | ✅ |

- **No modo limitado** o assistente não tem ferramentas; recebe só as regras inegociáveis e é
  instruído a **nunca prometer** uma consulta que não pode fazer.
- **As personas exigem chave própria**, porque carregam a árvore inteira de documentos.
- O **`@architectus`** exige apenas que o site tenha IA com chave (do site ou do
  administrador); no modo limitado ele não funciona.

### `@assistens` e sugestões automáticas

- **`@assistens`** é a persona de **controladoria** do site: somente consulta, sempre sobre as
  próprias tarefas de quem pergunta. Ajuste o tom e o foco dela nos documentos do site.
- Uma rotina em segundo plano **sugere** ações sobre tarefas em atraso; nunca executa sozinha.
  Cada usuário pode desligar.

> Evite traço longo e emojis nos documentos do assistente: viram "?" no armazenamento.

### O mapa de telas

Cada tela tem uma **descrição** (uma frase sobre para que ela serve). É o que o assistente e a
lupa usam para achar a tela certa:

- **A primeira frase diz o que a tela é**; o resto pesa menos.
- **"… ficam em <tela>"** redireciona: uma tela de configuração que "rouba" a palavra do usuário
  manda a busca para a tela real.
- Nas tabelas que você cria, a descrição vem do que você contou ao `@architectus`.

### Configuração da IA

| O que | Onde | Efeito |
|---|---|---|
| **Provedor e modelo do site** | Cofre, grupo IA | Tira o site do modo **limitado**; o uso é pago pela empresa. |
| **Chave própria do usuário** | Cada um, na janela "Configuração do Assistente de Inteligência Artificial" do chat (botão de foguete); só contas validadas, e salvar encerra a sessão | Uso pago pela pessoa; libera as personas. O administrador não vê essas chaves. |
| **Cota por usuário** | Configuração do servidor | Quanto cada conta pode gastar da chave do site; `0` desliga. |
| **Ocultar nomes internos** | Configuração do servidor | Garante que nenhum nome técnico de tabela/campo apareça nas respostas. |

### Acompanhar o consumo

O topo do chat mostra a **cota restante**, **TPM** e **RPM** da conversa. Perguntas que
consultam dados custam muito mais; conversas longas encarecem cada nova pergunta. Orientar a
equipe a **limpar a conversa** ao mudar de assunto é a medida de maior efeito.

---

# Parte VI — Governança

## 18. Privacidade, Termos e LGPD

- **Termos de Uso e Política de Privacidade** ficam disponíveis no sistema e são aceitos no
  cadastro.
- **LGPD.** IA que **não treina** com os dados do site; sites isolados entre si; opção de
  instalação dedicada. Mensagens a pessoas exigem **consentimento registrado** (seção 15).
- **DPO.** Mantenha os dados do encarregado corretos junto ao responsável pelo ambiente.
- **Zero-conhecimento** das credenciais do cofre (seção 11).

---

## 19. Checklist do administrador

**Na implantação**
- [ ] Trocar a senha do administrador e guardá-la com segurança.
- [ ] **Criar o cofre** (não há recuperação) e configurar **IA, SMTP e armazenamento**; testar
      cada conexão.
- [ ] Ajustar os rótulos do núcleo (Caso, Partes, Papel) e cadastrar os **Papéis**.
- [ ] Construir as primeiras tabelas com o `@architectus` (Guia do Construtor).
- [ ] Revisar as **regras inegociáveis** do assistente do site.
- [ ] **Convidar** a equipe.

**No dia a dia**
- [ ] Acompanhar **convites restantes** e a **cota de casos**.
- [ ] **Inativar** quem sai (nunca excluir o usuário).
- [ ] Ajustar telas e níveis de acesso no **Modo Esboço**.
- [ ] Após reiniciar o servidor (modo por senha), **desbloquear o cofre**.
- [ ] Acompanhar o **consumo de IA** e os **avisos de segurança de login**.
- [ ] Conferir os envios com falha na tela **Integrações**.

**Governança**
- [ ] Manter **Termos, Política e dados do DPO** atualizados.
- [ ] Revisar **quem tem acesso a quê** (níveis, validação, tokens MCP).
- [ ] Documentar quem detém a **senha do cofre** e como recuperá-lo (custódia).
