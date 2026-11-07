# Organizador de Imposto de Renda (Excel)

Ferramenta em Excel que reúne, em um só lugar, as informações necessárias para preparar a declaração de imposto de renda: rendimentos, despesas dedutíveis, bens, dívidas e um resumo final com checklist de documentos. Feita como desafio da DIO.

Arquivo: `Organizador_IR.xlsx`

> Todos os dados que aparecem na planilha (nomes, CPF/CNPJ, valores) são **fictícios, apenas para exemplo**. Apague as linhas de exemplo antes de usar com seus dados reais.

## Objetivo

Ajudar o usuário a organizar suas entradas de forma validada e prática, para que, na hora de declarar, os totais e os documentos já estejam reunidos.

## Estrutura da planilha

| Aba | Para que serve |
|---|---|
| **Menu** | Tela inicial com botões de navegação para cada aba e links rápidos para sites oficiais |
| **Rendimentos** | Registro de cada rendimento: data, fonte pagadora, CPF/CNPJ, tipo, valor bruto e imposto retido |
| **Deducoes** | Despesas dedutíveis por categoria, com indicação de comprovante em mãos |
| **Bens** | Bens e direitos, com valor em 31/12 do ano anterior e do ano atual e a variação |
| **Dividas** | Dívidas e ônus, com saldo anterior, saldo atual e variação |
| **Resumo** | Totais de rendimentos, deduções por categoria, patrimônio líquido e checklist de documentos |
| **Apoio** | Listas usadas nos menus suspensos |

## Recursos utilizados

**Navegação:** o Menu usa hiperlinks internos para levar a cada aba, e cada aba tem o link "Voltar ao Menu".

**Links rápidos:** atalhos para a página "Meu Imposto de Renda" da Receita Federal, o portal e-CAC e a consulta de situação cadastral do CPF.

**Validação de dados:**
- Listas suspensas (tipo de rendimento, categoria de dedução, tipo de bem, instituição, Sim/Não, tipo de dívida), alimentadas pela aba Apoio por meio de intervalos nomeados.
- Datas: só aceita datas válidas.
- Valores: só aceita números maiores ou iguais a zero.
- CPF/CNPJ: só aceita números, com 11 dígitos (CPF) ou 14 (CNPJ).
- Ano-calendário: só aceita ano entre 2000 e 2100.
- Cada validação mostra uma mensagem de erro explicando o que digitar.

**Fórmulas e intervalos nomeados:**
- `SOMA` para os totais de cada aba, com nomes como `total_rendimentos`, `total_ir_retido`, `total_deducoes`, `total_bens_atual` e `total_dividas_atual`.
- `SOMASE` no Resumo, para somar as deduções de cada categoria.
- `SE`, `ÉNÚM` e `E` para calcular a variação de bens e dívidas só quando os dois valores estão preenchidos.
- `CONT.SE` para contar quantos documentos do checklist já foram reunidos.

**Formatação:** linhas de grade ocultas, painéis congelados no cabeçalho, células editáveis em amarelo com fonte azul, células calculadas em cinza, e formatação condicional (comprovante "Não" fica vermelho; "Sim" fica verde no checklist).

## Como usar

1. Abra `Organizador_IR.xlsx` no Excel e comece pelo **Menu**.
2. Preencha as abas Rendimentos, Deducoes, Bens e Dividas, apenas nas células amarelas.
3. Informe o ano-calendário na aba Resumo e marque o checklist de documentos.
4. Consulte o Resumo para ver os totais.

## Prints

Capturas de tela na pasta `images/`: Menu, uma aba preenchida, e um erro de validação.

## O que aprendi

> Neste projeto aprendi a montar no Excel uma ferramenta de organização com cara de aplicativo. Usei **hiperlinks internos** para criar um menu de navegação e links rápidos para sites oficiais, e **validação de dados** (listas suspensas, datas, valores numéricos e CPF/CNPJ) para evitar erros de digitação. Também pratiquei **intervalos nomeados**, para deixar as fórmulas mais legíveis, e funções como `SOMA`, `SOMASE`, `SE` e `CONT.SE`, para calcular totais, deduções por categoria, variação de patrimônio e o andamento do checklist. Por fim, usei **formatação condicional** para destacar pendências, como comprovantes que ainda faltam.

A principal lição foi que uma planilha bem estruturada, com campos validados e telas separadas por assunto, fica mais fácil de usar e confiar do que uma tabela solta. Também aprendi a documentar o projeto em um README e a compartilhá-lo no GitHub.
