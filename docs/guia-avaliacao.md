# Guia do Modo de Avaliação — GRID

> Para quem baixou a imagem pública do GRID (`grid:eval` + `grid-web:eval`) e quer **testar o produto
> antes de contratar**. Mostra o que a avaliação limita de propósito, o primeiro dia passo a passo, o que
> não existe nela e como sair dela.
>
> Vale para as imagens publicadas a partir de 23/10/2026. Escrito a partir de uma
> varredura real de um site de avaliação. As telas e os manuais completos continuam valendo: veja o
> **Manual do Usuário**, o **Manual do Administrador** e o **Guia do Construtor** no menu **Ajuda**.

---

## O que é o modo de avaliação

Uma instalação sem licença roda em **modo de avaliação**. É o GRID de verdade, com limites:

| Limite | Na avaliação |
|---|---|
| **Casos** | no máximo **10 no total**. Excluir um caso **não devolve** a cota. Cada caso precisa de número ou assunto. |
| **Usuários** | no máximo **3** além do administrador. |
| **E-mail** | **não há**. Nenhuma tela envia e-mail: senhas e avisos aparecem **na tela**. |
| **Assistente de IA** | responde em **modo limitado** (um modelo pequeno, local, que conversa e explica mas **não consulta nem altera** dados). Para o assistente completo, cada pessoa informa a **sua** chave (seção 7). |
| **Armazenamento** | só o disco local do servidor; sem Google Cloud, Amazon S3 ou Azure. |
| **Licença** | sem licença válida a instalação continua em avaliação; com uma licença válida os limites saem. |

Os limites são aplicados pelo próprio programa e **não podem ser desligados** por configuração.

---

## 1. Primeiro acesso

1. Abra o endereço do site (por padrão `http://localhost:8080`) e clique em **Entrar no GRID**.
2. Entre com **`admin@grid.local`** e a senha inicial **`admin`**.
3. O sistema pede uma **nova senha** (mínimo de 8 caracteres, com maiúscula, minúscula, número e símbolo).
   Marque a confirmação sobre as credenciais salvas e conclua. Você será desconectado: entre de novo.
4. Guarde a senha. Não há e-mail para recuperá-la; só o administrador redefine a senha dos outros.

O administrador já tem uma **Pessoa** (criada no primeiro acesso): clicar no avatar abre **Minhas informações**
e você pode receber tarefas.

---

## 2. Trazer colegas (até 3)

Não há convite por e-mail. Cada colega faz o próprio cadastro:

1. Na página inicial, **Registre-se gratuitamente** → **Dados pessoais** (e-mail, CPF/CNPJ, nome, data de
   nascimento, celular e endereço completo; o CEP preenche o endereço quando o serviço de CEP responde) →
   **Termos** → **Confirmar e concluir cadastro**.
2. O sistema mostra uma **senha provisória na tela**. Anote-a e passe ao colega: ela **não é enviada por e-mail**.
3. No primeiro login o colega escolhe a senha definitiva. O cadastro já cria a **Pessoa** dele (celular e data de nascimento não são obrigatórios).

Se alguém esquecer a senha: o administrador abre **Usuário → o usuário → Editar → Redefinir senha do usuário** e
repassa a nova senha provisória que aparece na tela. (O link "Esqueci minha senha" não existe na avaliação.)

O quarto cadastro é recusado: *"Limite da avaliação atingido: até 3 usuários podem ser cadastrados neste ambiente de teste."*

---

## 3. Casos (limite de 10)

- **Casos → Novo**: número, assunto, fase, responsável, valor, observação. Informe ao menos o **número** ou o **assunto**.
- Excluir tira o caso da lista e dos números do Dashboard, mas a cota **não volta**.
- No décimo caso a criação seguinte é recusada: *"Limite de casos da avaliação atingido (10 no total…)"*. Para continuar é preciso licença.

---

## 4. Montar o seu sistema sem chave de IA: **Importar planilha**

Sem chave de IA o `@architectus` não funciona, mas você cria tabelas a partir de uma planilha:

1. Menu **☰** (canto direito do cabeçalho) → ícone de planilha **Importar planilha** (`/admin/import`).
2. Envie um `.xlsx`, `.csv`, `.tsv` ou `.txt` (até 100 MB).
3. **Conferir as colunas**: o GRID deduz o tipo de cada coluna. Telefones, CPF e números com zero à esquerda ficam como
   **texto**; `1.234,50` vira decimal; uma data impossível numa linha faz a coluna inteira virar texto. Corrija agora:
   depois da importação mudar o tipo mexe na estrutura.
4. **Criar a tabela**: dê o **nome**, o **grupo no menu** (padrão *Cadastros*) e uma **descrição** (vira a dica na tela).
5. **Importar**. A tabela aparece no menu e na **busca de telas (lupa)** com lista, exibição, cadastro e edição.

Ligar **Quadro**, **Calendário**, **Tarefas** e **Regras automáticas** numa tabela depende do `@architectus` (precisa de chave de IA).

---

## 5. Tarefas: crie o Evento primeiro

Toda tarefa precisa de um **Evento** (o tipo da tarefa) e uma instalação nova **não tem nenhum**.

1. **Tarefas → Nova tarefa →** botão **Novo Evento**.
2. Preencha só **Descrição** (ex.: *Compromisso geral*) e **Evento** (um código curto, ex.: `CMP`). O **Tipo** já vem como
   *Compromisso* — é ele que faz a tarefa aparecer no quadro. Ignore os demais campos (fluxo, antecedência, gatilho…).
3. Volte à tarefa: escolha o Evento, escreva o **Texto**, a **Pessoa solicitada** (você mesmo, por exemplo) e o **Vínculo**
   (*Caso* ou *Pessoa*). Sem esses itens a tarefa não é salva.
4. A tarefa aparece em **Minhas Tarefas** (e o contador do cabeçalho mostra quantas estão pendentes).

---

## 6. Painéis, documentos e agenda

- **Meus Painéis → Novo painel**: com o nome **Dashboard** ele aparece na página inicial. **Novo card**: título, **tabela** (Caso ou
  Pessoa e as ligadas a eles), **tipo de gráfico** (*Colunas, Linha, Pizza, Área* ou *Total*), agrupamento e agregação.
- **Meus Documentos**: envie arquivos (**Adicionar documento**) ou links `https` (**Adicionar link**). Ficam no disco local.
  A análise por IA (**Analisar / Resumir**) precisa de chave de IA.
- **Minha Agenda** mostra as suas tarefas por dia. Em **Tarefas → Assinar agenda** você gera um endereço privado `.ics` para
  assinar no Google Agenda, Outlook ou celular (a opção **Enviar somente os títulos** esconde o texto e o número do caso).
  Quem tem o endereço vê seus compromissos: se vazar, gere outro. **Conectar Google Agenda** não está disponível.

---

## 7. Assistente de IA

- **Sem chave**: o chat avisa *"você está usando um modelo de IA limitado"* e responde só conversando.
- **Com a sua chave**: no chat, botão do **foguete** → escolha o **provedor**, informe a **chave** e use **Verificar**, escolha o
  **modelo** e informe a **sua senha atual**. Salvar encerra a sessão. A chave fica cifrada na sua conta e o uso é cobrado pelo
  provedor. Só então valem `@architectus`, `@assistens` e `@Agent` e o assistente passa a consultar os dados.

`#help` lista os comandos do assistente (nomes e descrições em inglês; `#ajuda` também funciona).

---

## 8. O que não existe na avaliação

| Recurso | Situação |
|---|---|
| Convite por e-mail, código de 6 dígitos, "Esqueci minha senha" | Não existem; senhas aparecem na tela. |
| Notificações por e-mail e WhatsApp | Não funcionam (sem SMTP). |
| Armazenamento em nuvem e volumes frios | Só disco local. |
| Login com Google e conexão com o Google Agenda | Não disponíveis. |
| Administração de I.A. (AnythingLLM) | Não vem na avaliação; o ícone não aparece. |
| Pacote jurídico | Não faz parte da avaliação. |
| Mais de 10 casos ou 3 usuários | Exige licença. |

---

## 9. Limitações conhecidas desta versão

| Limitação | Como contornar |
|---|---|
| O **CEP** consulta serviços externos (ViaCEP e BrasilAPI). Se os dois estiverem fora do ar, o endereço não é preenchido. | Digite o endereço e escolha a UF à mão. A busca roda quando você sai do campo CEP. |
| O comando `#help` do assistente mostra tudo em inglês. | É de propósito: os comandos e as respostas do `#help` são em inglês; os manuais continuam em português. |
| Sem chave própria, o assistente só conversa (modo limitado). | Cadastre a sua chave (seção 7). |

## 10. Como sair da avaliação

A avaliação termina com uma **licença assinada** emitida pela equipe do GRID. Com ela instalada, os limites de casos e
usuários saem e a instalação passa ao regime licenciado. Pergunte à equipe do GRID como obtê-la.

Se a sua instalação **não tem servidor de e-mail** (ou ele está fora do ar), o GRID continua funcionando sem e-mail, também
licenciado: o cadastro e o login não pedem código por e-mail, a senha provisória e o código de convite aparecem na tela do
administrador (**Reiniciar senha**, **Convidar**), "Esqueci minha senha" fica oculto e, depois do login, o sistema avisa que o
serviço de e-mail está indisponível. Quando o servidor de e-mail voltar, o GRID volta ao fluxo normal sozinho.
