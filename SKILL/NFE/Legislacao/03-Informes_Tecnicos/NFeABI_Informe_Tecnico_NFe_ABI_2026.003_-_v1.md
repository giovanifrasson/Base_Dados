Sistema Nota Fiscal Eletrônica

Informe Técnico 2026.003

Versão 1.00 – Outubro de 2026

---

Nota Fiscal Eletrônica
NF-e ABI – Anexo I, Leiaute e Regras de Validação
## Sumário

Controle de Versões ............................................................................................................................................ 3
1. Objetivo ........................................................................................................................................................... 3
2. Descrição ........................................................................................................................................................ 3

Página 2 / 3

---

1

Nota Fiscal Eletrônica de Alienação de Bens Imóveis
NF-e ABI – Anexo I, Leiaute e Regras de Validação
## Controle de Versões

Versão Publicação Descrição

1.00 Outubro/2026 Publicação da primeira versão

## 1. Objetivo

O presente Informe Técnico tem como objetivo divulgar a publicação da nova Tabela de Códigos da
NF-e ABI v.1.01, bem como informar que a Tabela de Códigos da NF-e ABI v.1.00a - Publicada em
25/08/2026, disponível no Portal Nacional da NF-e, na aba “NF-e ABI”, opção “Diversos” está
revogado.

## 2. Descrição

A Tabela de Códigos da NF-e ABI traz os códigos a serem utilizados na emissão da Nota Fiscal
Eletrônica de Alienação de Bens Imóveis – NF-e ABI, assim como fórmulas e explicações que
norteiam as regras de negócio específicas do documento fiscal.

A Tabela de Códigos da NF-e ABI v.1.01 reflete a alteração da descrição da modalidade de operação
(tag: ide/modOper) “2. Arrematação, Adjudicação ou Remição” para “2. Arrematação Judicial,
Adjudicação ou Remição”, uma vez que as arrematações em leilão extrajudicial estão enquadradas
na modalidade “1. Alienação em geral” com IBS e CBS devidos pelo vendedor ou transmitente.

As opções de Tipo de Instrumento (tag: infOper/tpInstrumento) foram alteradas para contemplar
mais formas possíveis de ato de alienação, bem como eliminar as opções de “Carta de arrematação”
e “Carta de adjudicação”, a fim de não gerar confusão com as opções já existentes “Auto de
arrematação” e “Auto de adjudicação”.

Foram adicionados também os códigos aplicáveis ao Tipo de desfazimento (tag:
evDesfazimAlienac/tpDesfaz), mediante os quais o emitente deverá informar se a alienação de bem
imóvel está sendo desfeita por conta de distrato, decisão judicial, reversão da consolidação da
propriedade, etc.
