# Guia do Construtor — Monte o seu app no GRID

> Para o **administrador de um site GRID** que vai montar o sistema da sua empresa, seja qual
> for a área: atendimento, serviços, vendas, projetos, operações. Mostra o que já vem pronto,
> os primeiros passos e como **criar as suas próprias tabelas, telas e automações
> conversando com o assistente**, sem programação.
>
> A referência completa de administração (equipe, modelo de acesso, cofre, Modo Esboço,
> fluxos, integrações, governança da IA) está no **[Manual do Administrador](./manual-administrador.md)**.
> O uso diário de cada tela está no **[Manual do Usuário](./manual-usuario.md)**.
>
> **Sites com pacote de área** (como o jurídico) também podem ter o construtor, quando o plano
> o inclui: ele funciona igual e cria tabelas ao lado das do pacote, sem alterá-las.

---

## Sumário

1. [O que vem pronto no seu site](#1-o-que-vem-pronto-no-seu-site)
2. [Primeiro dia: cinco passos](#2-primeiro-dia-cinco-passos)
3. [Trazer a equipe: convites](#3-trazer-a-equipe-convites)
4. [Quem vê e quem edita](#4-quem-vê-e-quem-edita)
5. [Criar tabelas conversando: `@architectus`](#5-criar-tabelas-conversando-architectus)
6. [Transformar uma planilha em tabela](#6-transformar-uma-planilha-em-tabela)
7. [Ligar recursos numa tabela](#7-ligar-recursos-numa-tabela)
8. [Ajustar as telas sem programar](#8-ajustar-as-telas-sem-programar)
9. [Fluxos de trabalho](#9-fluxos-de-trabalho)
10. [Limites e o que ainda não existe](#10-limites-e-o-que-ainda-não-existe)
11. [Exemplo completo: de uma planilha a um app em uso](#11-exemplo-completo-de-uma-planilha-a-um-app-em-uso)
12. [Checklist do administrador do site](#12-checklist-do-administrador-do-site)

---

## 1. O que vem pronto no seu site

Todo site nasce com o núcleo comum a qualquer negócio (no pacote jurídico, os Casos são
os Processos):

| Área | Para que serve |
|---|---|
| **Casos** | O registro central do seu trabalho: um atendimento, um projeto, um pedido, um contrato. Tem número, situação e as **Partes** envolvidas. |
| **Pessoas** | Cadastro único de pessoas físicas e jurídicas (clientes, contatos, parceiros). Toda referência a uma pessoa aponta para cá. |
| **Partes** | Painel dentro do Caso: quem participa dele e com qual **Papel** (por exemplo, cliente, responsável, fornecedor). Os papéis são uma lista que você mantém. |
| **Tarefas** | Quadro (Kanban) de tarefas, cada uma ligada a uma **Pessoa** ou a um **Caso**, com prazo, responsável e situação. |
| **Documentos** | Explorador de arquivos por caso e por pessoa, com resumo e busca pelo assistente de IA. |
| **Assistente de IA** | O chat do canto da tela, que consulta os dados (respeitando as permissões de quem pergunta) e, para você, também **constrói** tabelas (seção 5). |
| **Usuários** | As contas da sua equipe (somente o administrador gerencia). |

> **Cota de casos.** Seu plano inclui um número de casos (o padrão é **10**). Cada caso
> criado consome um. Excluir um caso **não devolve** a cota: o caso excluído deixa de
> aparecer, mas continua guardado. Para ampliar a cota, fale com o suporte.

Os nomes "Caso", "Partes" e "Papel" são apenas rótulos: se na sua empresa o caso se chama
"Atendimento" ou "Projeto", renomeie (seção 8).

---

## 2. Primeiro dia: cinco passos

1. **Troque a senha** recebida no primeiro acesso. A conta de administrador vê e edita
   tudo e abre o cofre: use uma senha forte e guarde-a com cuidado.
2. **Crie o cofre de credenciais** (ícone de cadeado no cabeçalho). É ali que ficam, cifradas,
   as chaves do seu site. Não há recuperação da senha do cofre. Detalhes no Manual do
   Administrador, seção 11.
3. **Ligue a inteligência artificial.** Duas opções, que podem conviver:
   - **Chave do site:** você cadastra no cofre (grupo IA) o provedor, o modelo e a chave.
     Todos os usuários passam a usar o assistente completo, pago pela sua empresa.
   - **Chave de cada usuário:** cada pessoa cadastra a sua na janela de configuração do chat
     (botão de foguete) e paga o próprio uso.

   Sem nenhuma das duas, o assistente funciona em **modo limitado**: conversa, mas não
   consulta nem altera nada, e **não constrói tabelas**.
4. **Renomeie o que for preciso** (Caso, Partes, Papel) e cadastre os **Papéis** que sua
   equipe usa.
5. **Convide a equipe** (próxima seção).

---

## 3. Trazer a equipe: convites

Sites novos são **somente por convite**: ninguém se cadastra sozinho. (No **site de avaliação** é o contrário:
não há convites, o cadastro é livre até 3 usuários e a senha provisória aparece na tela.)

1. No cabeçalho, clique em **"Convidar alguém"** (visível apenas para o administrador).
2. Informe o **e-mail da pessoa** e clique em **"Enviar convite"**.
3. A pessoa recebe por e-mail um **código** que só funciona para aquele endereço e
   **expira em 2 dias**. Ela abre o site, escolhe "Registre-se", informa o e-mail e o código
   e define a própria senha.

O que saber:

- A janela mostra quantos **convites restantes** você tem. Um convite só é consumido quando
  o e-mail é enviado com sucesso. Para mais convites, fale com o suporte.
- **Um e-mail pertence a um único site.** Se a pessoa já tem conta com aquele e-mail, o
  convite é recusado com o aviso "Esse e-mail já tem uma conta".
- Código expirou? Basta enviar outro convite.
- Muitas tentativas com código errado **bloqueiam** aquele e-mail para cadastro, por
  segurança; o desbloqueio é feito pelo suporte.
- Para tirar alguém da equipe, **inative** a conta em Usuários: a pessoa não consegue mais
  entrar e os registros dela continuam no sistema.

---

## 4. Quem vê e quem edita

Num site novo, a equipe **trabalha junta**: o padrão é o **acesso compartilhado**.

| Quem está logado | Registro criado por… | Vê? | Edita? |
|---|---|---|---|
| **Administrador** | qualquer pessoa | ✅ | ✅ |
| Usuário | qualquer membro da equipe (inclusive ele mesmo) | ✅ | ✅ |
| Usuário | o **administrador** | ✅ | ❌ somente leitura |

- O que **você** cria funciona como **referência da empresa**: todos consultam, só você
  altera. Use isso a seu favor para listas que a equipe não deve mexer, como os Papéis ou
  uma tabela de preços.
- Quando o administrador edita o registro de alguém, o registro **continua sendo da
  pessoa** e ela continua podendo editá-lo.
- Por cima disso vale o **nível de acesso** de cada tela e de cada campo (0 só o
  administrador, 1 todos veem e só o administrador edita, 2 todos veem e editam), ajustado
  no Modo Esboço (seção 8 e Manual do Administrador, seção 6).
- Se a sua empresa precisa que **cada um veja só o que é seu** (o modelo clássico por
  usuário), peça ao suporte: é uma configuração do site, não das telas.

---

## 5. Criar tabelas conversando: `@architectus`

O **`@architectus`** é o assistente que **constrói** a estrutura do seu sistema: tabelas,
campos e recursos. Ele não preenche registros (isso é o uso normal das telas) e nunca
constrói nada sem que você aprove.

**Requisitos:** estar logado como **administrador** e ter a IA ligada com chave (seção 2,
passo 3). Os demais usuários não conseguem chamá-lo.

### Como pedir

Abra o chat e comece a mensagem com `@architectus`, descrevendo o que precisa **como você
falaria com um colega**:

> `@architectus` preciso controlar os equipamentos que emprestamos aos clientes: nome do
> equipamento, número de série, cliente, data do empréstimo, data prevista de devolução e
> situação (emprestado, devolvido, com defeito).

O assistente pode fazer uma ou duas perguntas sobre como a tabela será usada e então
apresenta um **plano**: o nome da tabela, cada campo com seu tipo, o que é obrigatório e as
opções de cada lista. **Nada é criado ainda.**

- Está bom? Responda **"pode criar"**. Ele cria a tabela e devolve o **link** para a tela.
- Quer mudar? Diga o quê ("o número de série é obrigatório", "tire a cor") e ele refaz o
  plano.
- Um plano vale por **30 minutos**. Se outra mudança na estrutura acontecer nesse meio
  tempo, ele propõe de novo.

Em segundos a tabela tem **tela de lista, de exibição, de cadastro e de edição**, aparece
no **menu lateral** e na **busca de telas (lupa)** e pode ser consultada pelo assistente de
qualquer usuário.

**Onde ela aparece no menu.** O assistente conhece os grupos que o menu do site já tem e
sugere o que combina; sem indicação, a tabela entra em **Cadastros**, e se o grupo escolhido
ainda não existe ele avisa que um grupo novo vai aparecer. Para outro lugar, diga o grupo ao
pedir ("crie no grupo Oficina") ou depois ("mova Equipamentos
para o grupo Oficina"). Use **/** para subgrupos: `Cadastros/Financeiro`. O grupo não pode
ter o mesmo nome de uma tabela: o assistente recusa, porque assim a tabela viraria um painel
dentro daquela tabela em vez de um item do menu.

### Tipos de campo

Você não precisa citar tipos: o assistente deduz pelo que você descreve. Para referência:

| Tipo | Use para |
|---|---|
| Texto / Texto longo | Nomes, códigos, observações |
| Inteiro / Decimal | Quantidades, medidas |
| Moeda | Valores em R$ (a tela já formata) |
| Data / Data e hora | Prazos, vencimentos, agendamentos |
| Sim/Não | Marcações (aparece como caixa de seleção) |
| Lista de opções | Situações fixas, cada opção com sua cor (ex.: Ouro, Prata, Bronze) |
| Referência | Aponta para outra tabela, inclusive **Pessoas** e **Casos** ("o cliente é uma pessoa do cadastro") |

**Papéis de um campo.** Diga ao assistente qual campo é o **título** do registro (o que
aparece nas listas de seleção), qual é a **data de vencimento**, qual é a **situação** e
quem é o **responsável**. São esses papéis que fazem o Calendário, o Quadro e as Tarefas
funcionarem sem nenhuma configuração extra (seção 7).

Cada tabela ganha automaticamente um identificador, o registro de **quem criou** e de
**quando foi alterado** — não peça esses campos.

### Depois de criada

| Você quer… | Diga ao `@architectus` |
|---|---|
| Ver o que já construiu | "quais tabelas eu criei?" |
| Acrescentar um campo | "acrescente o campo Voltagem, texto, em Equipamentos" |
| Renomear a tabela ou um campo | "renomeie Equipamentos para Ativos" (só muda o rótulo; os dados ficam) |
| Mudar a tabela de lugar no menu | "mova Equipamentos para o grupo Oficina" |
| Excluir uma tabela | "exclua a tabela Testes" |

- Um campo **obrigatório** numa tabela que **já tem registros** precisa de um valor
  padrão; o assistente pergunta.
- A exclusão é recusada enquanto a tabela tiver registros, a menos que você confirme
  explicitamente depois de ouvir **quantos registros serão apagados**. Também é recusada
  enquanto outra tabela apontar para ela. **Não há como desfazer.**
- O assistente só altera tabelas que **você criou**. As tabelas que vieram prontas (Casos,
  Pessoas, Tarefas…) são ajustadas pelo Modo Esboço (seção 8).

> **Dica:** comece com **uma tabela que funcione**, mesmo que larga, e divida depois, quando
> a equipe sentir falta. Quatro tabelas relacionadas no primeiro dia costumam atrapalhar
> mais do que ajudar.

---

## 6. Transformar uma planilha em tabela

Se os dados já estão numa planilha (Excel `.xlsx` ou `.csv`; Google Planilhas exportada
como CSV), o assistente cria a tabela **e** carrega as linhas.

1. **Envie o arquivo**: anexe no próprio chat ou envie para **Meus Documentos**.
2. Peça: `@architectus importe a planilha de clientes`. Se houver várias, ele lista as que
   você enviou e pergunta qual; numa planilha com várias abas, diga qual aba.
3. Ele lê o arquivo e apresenta o **plano**: os campos com o tipo detectado, o número de
   linhas, uma prévia de 3 linhas e os **avisos**. Leia os avisos.
4. Aprove. A carga roda em segundo plano; pergunte "como está a importação?" para
   acompanhar.

Como o tipo de cada coluna é decidido (sempre a favor de **não perder dado**):

- Números com **zero à esquerda**, CPF, CNPJ, CEP e telefones continuam **texto** — nunca
  viram número e perdem dígitos.
- `1.234` é lido no padrão brasileiro (mil duzentos e trinta e quatro), e o plano avisa.
- Uma única célula fora do padrão faz a coluna inteira ser texto.
- Todo campo importado aceita vazio. Acentos são preservados.

Limites: arquivo até **100 MB**, até **200 mil linhas** e até **60 colunas** por tabela.
Se a planilha tiver mais colunas, o assistente pede que você escolha quais importar; ele
nunca corta em silêncio.

**Sem chave de IA?** Use **Importar planilha** (ícone de planilha no menu **☰** do cabeçalho, `/admin/import`).
É um assistente em quatro etapas — **Arquivo, Planilha, Colunas, Importar** — com a mesma regra de tipos acima:
você confere o tipo de cada coluna, dá **nome**, **grupo no menu** e **descrição** à tabela e o GRID a cria e carrega
as linhas. Não depende de IA.

**Linhas puladas.** Uma linha que não pode ser convertida (uma data impossível, por
exemplo) é pulada e o resto continua. Ao final, o assistente informa **quantas** foram
puladas e **por quê**, com o número da linha. Corrija a planilha e importe essas linhas
de novo, ou digite-as na tela.

---

## 7. Ligar recursos numa tabela

Toda tabela que você constrói pode ganhar os mesmos recursos que as tabelas prontas têm.
Peça ao `@architectus` (precisa de chave de IA), por exemplo: "ligue o calendário em Equipamentos". Sem ele, uma
tabela importada fica só com lista, exibição, cadastro e edição.

| Recurso | O que aparece | Precisa de |
|---|---|---|
| **Documentos** | Anexar arquivos a cada registro, com a árvore de documentos e o resumo por IA | — |
| **Tarefas** | Painel **Tarefas** na tela de exibição de cada registro: criar, concluir e cancelar tarefas daquele registro | — |
| **Quadro** (Kanban) | Botão **"Quadro"** na lista: os registros como cartões em colunas, arrastáveis | Um campo de **situação** (as colunas são as opções da lista, com as cores) |
| **Calendário** | Botão **"Calendário"** na lista: os registros por data | Um campo de **data de vencimento** |
| **Painéis** | A tabela passa a aparecer em **Meus Painéis** para gráficos e indicadores (contagem, soma, média, por mês) | Para somas e médias, um campo numérico |
| **Regras automáticas** | Ações que acontecem sozinhas ao salvar um registro | O recurso **Tarefas**, se a regra criar tarefas |

Todos os recursos **respeitam as permissões**: no Quadro, arrastar um cartão é uma edição
comum, então quem não pode editar o registro não consegue movê-lo; nos Painéis, cada
pessoa só soma o que pode ver.

### Regras automáticas

Descreva a regra em uma frase: **quando** (ao criar, ao alterar ou ambos), **se** (as
condições) e **então** (as ações).

> `@architectus` em Equipamentos: quando a situação mudar para "com defeito", crie uma
> tarefa "Enviar {nome} para conserto".

> `@architectus` em Pedidos: ao criar, se o valor for maior que 10.000, marque
> "Precisa de aprovação".

O que uma regra pode fazer — de propósito, nada além disto:

- **Condições:** igual, diferente, maior, menor, está entre os valores, está vazio, foi
  alterado.
- **Ações:** preencher outro campo do mesmo registro, ou criar uma tarefa (o título pode
  usar os campos do registro: escreva o nome do campo entre chaves, como `{nome}`, e ele
  é trocado pelo valor daquele registro).

Garantias: a regra roda **depois** que o registro foi salvo e **nunca impede** o
salvamento; se uma ação falhar, as outras continuam e a falha fica registrada. Salvar de
novo sem mudar o valor **não** dispara a regra outra vez, e uma regra não entra em
ciclo infinito com outra.

---

## 8. Ajustar as telas sem programar

Pelo **Modo Esboço** (interruptor **"Esboço"** no cabeçalho, nas telas de exibição), você
ajusta qualquer tela, inclusive as que vieram prontas:

- **reordena** os campos e move campos entre **visível** e **invisível**;
- **renomeia** os painéis;
- define o **nível de acesso** de cada campo (0, 1 ou 2; veja a seção 4).

O pill **"Layout"** alterna os formulários entre **painéis** e **abas**. Detalhes no
Manual do Administrador, seção 9.

**Rótulos.** O nome que você dá a uma tabela ou a um campo vale para todos os usuários e
**prevalece sobre a tradução padrão** do GRID. Nas tabelas que você criou, peça a troca ao
`@architectus`; nas tabelas prontas (Caso, Partes, Papel…), peça ao suporte enquanto a
tela de renomear não chega para elas.

**Descrição de cada tabela.** Ao criar, conte ao assistente *para que serve* a tabela. Essa
frase vira a **dica** que aparece ao passar o mouse e é o que ajuda o assistente de toda a
equipe a achar a tabela certa quando alguém pergunta "quantos equipamentos estão com
defeito?".

---

## 9. Fluxos de trabalho

Para processos com várias etapas e responsáveis (aprovar, executar, conferir), o GRID tem
um **desenhista de fluxos** — ícone **"Fluxos de trabalho"** no cabeçalho, só para o
administrador.

- Você desenha o fluxo como um diagrama: **etapas** (uma tarefa para uma pessoa, com prazo
  e as situações possíveis), **decisões** (caminho A ou B conforme uma condição) e
  **ações automáticas**.
- Um fluxo começa quando alguém cria uma tarefa do **evento** ligado a ele. Um fluxo sem
  evento ligado nunca roda.
- **Validar** e **Salvar** fazem a mesma verificação: o desenhista recusa um fluxo com
  caminho sem saída, etapa inalcançável ou um ciclo que não passa por nenhuma pessoa. Não
  existe "salvar com avisos".
- Cada etapa vira uma tarefa no **Quadro de Tarefas** de quem é responsável; concluir a
  tarefa avança o fluxo.

> **Regra automática ou fluxo?** Use uma **regra** (seção 7) para uma reação simples a um
> registro ("se ficou com defeito, crie uma tarefa"). Use um **fluxo** quando há uma
> sequência de etapas, pessoas diferentes e decisões no meio.

---

## 10. Limites e o que ainda não existe

**Limites do construtor**

| Limite | Padrão |
|---|---|
| Campos por tabela | 60 |
| Tabelas construídas por site | 200 |
| Linhas por importação | 200 mil |
| Tamanho da planilha | 100 MB |

Um limite atingido é explicado pelo assistente com a saída possível ("esta tabela teria 74
campos; vamos dividir em duas?"). Para ampliar, fale com o suporte.

**Ainda não existe** (dito com clareza para evitar surpresa):

- **Não há tela para escrever regras automáticas**: elas são descritas ao `@architectus`.
- Não é possível **alterar o tipo** de um campo nem **remover** um campo de uma tabela já
  criada pelo assistente; crie um campo novo e deixe o antigo invisível pelo Modo Esboço.
- O `@architectus` **não altera as tabelas prontas** (Casos, Pessoas, Tarefas, Documentos).
- **Grupos de acesso próprios por tabela** (cada tabela com a sua regra de quem vê) não existem: o
  acesso aos registros é do **site inteiro** — compartilhado por todos, individual por usuário ou **por
  equipe** (colegas de equipe veem e editam o trabalho uns dos outros; Manual do Administrador, seções 6
  e 14). Quem escolhe o modelo é o suporte, na instalação. **Equipes** também distribuem **tarefas e
  etapas de fluxo** — veja "Quem recebe cada etapa" no Manual do Administrador, seção 14.

---

## 11. Exemplo completo: de uma planilha a um app em uso

Uma assistência técnica controla ordens de serviço numa planilha.

1. **Dia 1, manhã.** O administrador cria o cofre, cadastra a chave de IA do site e renomeia
   "Caso" para "Atendimento".
2. Envia a planilha `ordens.xlsx` no chat:
   `@architectus importe esta planilha como Ordens de serviço, no grupo Oficina`.
   O plano mostra 9 campos, 1.840 linhas e um aviso: "Telefone continuará texto (zeros à
   esquerda)". Ele aprova; 1.838 linhas entram e 2 são puladas por data inválida, com o
   número das linhas.
3. `@architectus em Ordens de serviço, a Situação é uma lista: Aberta (azul), Em conserto
   (laranja), Pronta (verde), Entregue (cinza); o Técnico é o responsável e a Previsão é
   a data de vencimento.`
4. `@architectus ligue o quadro, o calendário, documentos e tarefas em Ordens de serviço.`
5. `@architectus quando a Situação virar Pronta, crie a tarefa "Avisar o cliente da {número}".`
6. No Modo Esboço, ele deixa Observações invisível e coloca Situação em primeiro lugar.
7. **Dia 1, tarde.** Convida os três técnicos. Eles abrem a tela pelo menu, usam o
   **Quadro** para arrastar as ordens entre colunas, anexam fotos em Documentos, e o
   balcão vê pelo **Calendário** o que fica pronto em cada dia.
8. **Semana seguinte.** Em **Meus Painéis**, o administrador monta um gráfico de ordens
   entregues por mês e outro do valor total por técnico.

---

## 12. Checklist do administrador do site

**No primeiro dia**
- [ ] Trocar a senha do administrador e guardá-la com segurança.
- [ ] Criar o **cofre de credenciais** (não há recuperação da senha).
- [ ] Ligar a **IA**: chave do site no cofre e/ou orientar a equipe a usar a própria chave.
- [ ] Configurar o **e-mail** do site no cofre, se o suporte não o tiver feito (convites e
      códigos de segurança dependem dele).
- [ ] Ajustar os rótulos de **Caso / Partes / Papel** e cadastrar os **Papéis**.
- [ ] **Convidar** a equipe.

**Ao construir**
- [ ] Descrever cada tabela nova ao `@architectus` com **para que serve**.
- [ ] Indicar o **título**, a **situação**, o **vencimento** e o **responsável** de cada tabela.
- [ ] Ligar só os **recursos** que a equipe vai usar.
- [ ] Ler os **avisos** de cada importação e tratar as **linhas puladas**.
- [ ] Ajustar a ordem e a visibilidade dos campos no **Modo Esboço**.

**No dia a dia**
- [ ] Acompanhar a **cota de casos** e os **convites restantes**.
- [ ] **Inativar** quem sai da equipe (nunca excluir o usuário).
- [ ] Revisar quem pode ver e editar cada tela (níveis de acesso).
- [ ] Revisar as **regras inegociáveis** do assistente do site (Manual do Administrador,
      seção 17).
