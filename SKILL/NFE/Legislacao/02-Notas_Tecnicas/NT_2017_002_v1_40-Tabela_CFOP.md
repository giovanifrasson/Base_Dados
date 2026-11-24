# Projeto Nota Fiscal
# Eletrônica

## Nota Técnica 2017.002

## Implementa nova Tabela CFOP

### Versão 1.40 – Janeiro/2020

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

## Sumário

Controle de Versões ......................................................................................................................... 3
Histórico de Alterações / Cronograma .............................................................................................. 4
1 Resumo ..................................................................................................................................... 5
2 Regras de Validação (RV) da Nota Fiscal Eletrônica ................................................................. 5
2.1 Regras de Validação Alteradas ............................................................................................. 5
3 Novos registros na Tabela CFOP ............................................................................................ 11
4 ANEXO I - Ajuste SINIEF 11/18 - Alterações e Inclusões de CFOP......................................... 13
4.1 CFOP alterados ................................................................................................................... 13
4.2 CFOP incluídos ................................................................................................................... 14
5 ANEXO II - Ajuste SINIEF 07/19 - Inclusões de CFOP com as respectivas Notas Explicativas 15
6 ANEXO II - Ajuste SINIEF 20/19 – Alterações e Inclusões de CFOP com as respectivas Notas
Explicativas ..................................................................................................................................... 16
6.1 CFOP alterados ................................................................................................................... 16
6.2 CFOP incluídos ................................................................................................................... 18
7 ANEXO II - Ajuste SINIEF 27/19 – Alteração e Inclusões de CFOP com as respectivas Notas
Explicativas ..................................................................................................................................... 23
7.1 CFOP alterado .................................................................................................................... 23
7.2 CFOP incluídos ................................................................................................................... 23

**Página 2 / 24**

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

# Controle de Versões

**Versão Publicação Descrição**

**1.40 Janeiro/2020 Alteração do CFOP 5.929 e inclusão de novos registros, conforme disposto no**
**Ajuste SINIEF 27/19.**

**1.30 Novembro/2019 Insere novos registros na Tabela CFOP com as respectivas Notas Explicativas, conforme**
Ajuste SINIEF 20/19. Esse Ajuste também altera CFOP já existentes.

**1.20 Abril/2019 Insere novos registros na Tabela CFOP com as respectivas Notas Explicativas**

**1.10 Agosto/2018 Insere novos registros na Tabela CFOP e Altera Notas Explicativas de CFOP já existentes**

**1.00 Dezembro/ 2017 Publicação da NT, implementação da nova Tabela CFOP e Alterações nas validações**

**Página 3 / 24**

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

# Histórico de Alterações / Cronograma

**Versão Histórico de atualizações Implantação Implantação**
**Homologação Produção**

 Alteração do CFOP 5.929 e inclusão de novos registros, conforme
### 1.40 15/01/2020 03/02/2020
disposto no Ajuste SINIEF 27/19.
 Insere novos registros na Tabela CFOP e respectivas Notas
**1.30 27/11/2019 01/12/2019**
Explicativas, conforme Ajuste SINIEF 20/19.
 Este mesmo Ajuste altera CFOP existentes.
 Insere novos registros na Tabela CFOP e respectivas Notas
**1.20 09/04/2019 01/05/2019**
Explicativas
 Esta versão informa a inclusão dos CFOP e alteração das Notas
**1.10 Entre 01/09/2018**
Explicativas de alguns já existentes, por meio do Ajuste SINIEF
**28/08/2018 e**
11/18.
**01/09/2018**
 Insere novos registros na Tabela CFOP publicada no Portal da NF-
e, decorrente desse Ajuste.
 A alteração das Notas Explicativas de CFOP já existentes,
decorrente desse Ajuste, não tem impacto na tabela publicada no
Portal da NF-e.
 Modificação do leiaute da NT para o novo padrão de identidade
visual.
 Alteração nas validações e unificação das tabelas
**1.00 05/03/2018 02/04/2018**
** Inclusão dos novos CFOPs**

**Página 4 / 24**

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

## 1 Resumo

Esta edição insere novos registros e indicadores na Tabela CFOP publicada no Portal da NF-e.

## 2 Regras de Validação (RV) da Nota Fiscal Eletrônica

## 2.1 Regras de Validação Alteradas

Seguem as alterações relativas às Regras de Validação.

### Grupo L. Item / Combustível

**Campo- Modelo Regra de Validação Aplic. Msg Efeito Descrição Erro**
**Seq**
LA01-20 55/65 Obrigatória a informação do grupo de combustível para os CFOP Facul. 660 Rej. Rejeição: CFOP de Combustível e
constantes na Tabela CFOP, indComb=1 ou 2. (NT 2012/003) não informado grupo de combustível
**Observação: Para a NFC-e, a regra de validação é opcional, a critério [nItem:nnn]**
da UF.
**Exceção: Para a NFC-e, a regra de validação não se aplica, em**
produção, para Nota Fiscal com Data de Emissão anterior a
01/01/2016.

### Grupo N. Item / Tributo: ICMS

**Campo- ModelRegra de Validação AplicMsg EfeitDescrição Erro**
**Seq o . o**
**N12-70 55 Operação com Não Contribuinte (indIEDest=9) e CST difere da Obrig. 508 Rej. Rejeição: CST incompatível na**
relação abaixo: operação com Não Contribuinte
- 00-Tributada integralmente; [nItem:999]

**Página 5 / 24**

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

- 20-Com redução da Base de Cálculo;
- 40-Isenta;
- 41-Não tributada;
- 60-ICMS cobrado anteriormente por substituição tributária;
**Exceção 1: A regra de validação acima não se aplica para NF-e de**
entrada (tpNF=0-Entrada).
**Exceção 2: A regra de validação acima não se aplica para o CST=50**
(Suspensão), nas operações com CFOP de Retorno de Mercadorias
(Tabela CFOP, indRetor=1), nem nas operações com CFOP de
Remessa de Mercadorias (Tabela CFOP, indRemes=1), e nem nas
operações com CFOP 5.949 ou 6.949.
**Exceção 3: A regra de validação acima não se aplica quando houver**
ao menos um item de venda de veículos novos (grupo “veicProd”).
**Exceção 4: A regra de validação não se aplica, em produção, para**
Nota Fiscal com data de emissão anterior a 01/07/2016.
**Exceção 5: A regra de validação não se aplica para o CST=30 (Isenta**
ou não tributada e com cobrança do ICMS por substituição
tributária), em operação interestadual (idDest=2) com combustíveis
(tag: comb) derivados de petróleo (código ANP diferente de:
820101001, 820101010, 810102001, 810102004, 810102002,
810102003, 810101002, 810101001, 810101003, 220101003,
220101004, 220101002, 220101001, 220101005, 220101006,
560101001).
**Exceção 6: A regra de validação acima não se aplica para os**
CST=50 (Suspensão) e 51 (Diferimento), nas operações de
devolução (finNFe=4).
**Exceção 7: A regra de validação acima não se aplica para o CST=51**
(Diferimento), nas operações com CFOP 5.123, 5.922, 6.123 e
6.922, nem nas operações internas (idDest=1) de retorno de
mercadoria depositada em depósito fechado ou armazém geral
(CFOP 5.906 ou 5.907).
**Exceção 8: A critério da UF, a regra de validação não se aplica para o**
CST=10 (Tributada e com cobrança do ICMS por substituição tributária)
em operação interna (idDest=1).

**Página 6 / 24**

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

**N16-04 55 Validação alíquota do ICMS na operação interestadual de produtos Facul. 663 Rej Rejeição: Alíquota do ICMS com**
importados (NT 2012/005 e NT2013/006):  valor superior a 4 por cento na
- Operação Interestadual de Saída (idDest=2 e tpNF=1);  operação de saída interestadual
- Origem da mercadoria = 1, 2, 3 ou 8;  com produtos importados
- CST de ICMS = 00, 10, 20, 70 ou 90;  [nItem:999]
- Data de Emissão igual ou superior a 01/01/2013;
- Valor alíquota do ICMS  maior do que “4.00” (4 por cento).
**Exceção  0: Para as NF-e com Data de Emissão anterior a 01/07/2016,**
a regra de validação acima não se aplica para destinatário Não
Contribuinte (tag:dest/indIEDest=9).
**Exceção 1: A regra acima não se aplica para as operações de**
Devolução (finNFe=4).
**Exceção 2: A regra de validação acima não se aplica para as**
operações com CFOP de Retorno de Mercadorias (Tabela CFOP,
indRetor=1).
**Exceção 3: A regra de validação acima não se aplica na venda de**
veículos novos (grupo “veicProd”) se existir ao menos um item de
Venda direta para grandes consumidores (tpOp=3), ou de Faturamento
direto para consumidor final (tpOp=2).
**Exceção 4: Para as NF-e com Data de Emissão anterior a 01/07/2016,**
mesmo que informada a IE do destinatário, a regra de validação acima
não se aplica para as operações com os CFOP 6107, 6108 (Não
Contribuinte).
**Exceção 5: A regra de validação acima não se aplica para a NF**
Complementar (finNFe=2) quando:
- Se referenciada uma NF-e, a NF-e referenciada tem a Data de
Emissão anterior a 01/01/13;
- Se referenciada uma NF modelo 1, a Data de Emissão é anterior a
1301 (tag refNF/AAMM).
**Exceção 6: Para as NF-e com Data de Emissão anterior a 01/07/2016,**
mesmo que informada a IE do destinatário, a regra de validação acima
não se aplica para as operações com o CFOP 6.929 - Lançamento
relativo a operação registrada em Cupom Fiscal (NT 2013/004).

**Página 7 / 24**

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

N16-20 55 Validação alíquota do ICMS na operação interestadual de Saída Obrig. 693 Rej. Rejeição: Alíquota de ICMS superior
Normal: a definida para a operação
- Operação Interestadual de Saída Normal (idDest=2, tpNF=1 e interestadual [nItem:999]
finNFe=1);
- Origem da mercadoria difere de 1, 2, 3 ou 8;
- Valor alíquota do ICMS (tag:pICMS) maior do que “7.00” (7
por cento) para os Estados de origem (enderEmit/UF) do Sul e
Sudeste, exceto ES, destinado (enderDest/UF) para os Estados
do Norte, Nordeste, Centro-Oeste e Espírito Santo.
- Valor alíquota do ICMS (tag:pICMS) maior do que “12.00” (12
por cento) para os demais casos.
**Exceção 1: Para as NF-e com Data de Emissão anterior a 01/07/2016,**
a regra de validação acima não se aplica para destinatário Não
Contribuinte (tag:dest/indIEDest=9).
**Exceção 2: A regra de validação acima não se aplica na venda de**
veículos novos (grupo “veicProd”) se existir ao menos um item de
Venda direta para grandes consumidores (tpOp=3), ou de Faturamento
direto para consumidor final (tpOp=2).
**Exceção 3: A regra de validação acima não se aplica para as**
operações com CFOP de Retorno de Mercadorias ou Anulação de Valor
(Tabela CFOP, indRetor=1 ou indAnula=1).
**Exceção 4: A regra de validação acima não se aplica para as**
operações de venda à ordem (CFOP 6.118, 6.119, 6.122 e 6.123)
**Exceção 5: A regra de validação não se aplica se informada UF do local**
de entrega (tag: entrega/UF) diferente da UF do emitente (tag:
enderEmit/UF);
**Exceção 6: A regra de validação não se aplica se informada UF do local**
de retirada (tag: retirada/UF) diferente da UF do destinatário (tag:
enderDest/UF);

**Página 8 / 24**

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

### Grupo NA. Item / Tributo: ICMS para a UF de Destino

**Campo- ModelRegra de Validação Aplic. Msg EfeitDescrição Erro**
**Seq o o**
**NA01-20 55 Não informado grupo de ICMS para a UF de Destino Obrig. 694 Rej. Rejeição: Não informado o grupo de**
(tag:ICMSUFDest):  ICMS para a UF de destino
- Operação Interestadual (idDest=2) e  [nItem:999]
- Operação com Consumidor Final (indFinal=1) e
- Operação com Não Contribuinte (indIEDest=9) e
- Não é operação de prestação de serviços (não existe tag
**“ISSQN”). Exceção 1: Esse grupo não deve ser exigido se o**
Grupo de Partilha do ICMS (campo ICMSPart) estiver
preenchido.
**Exceção 2: A regra de validação não se aplica, em produção, para Nota**
Fiscal com data de emissão anterior a 01/07/2016.
**Exceção 3: A regra de validação não se aplica para Devolução de**
Mercadoria (finNFe=4) que referencie Nota Fiscal com chave de acesso
anterior a 2016.
**Exceção 4: A regra de validação acima não se aplica para as**
operações com CFOP de Retorno de Mercadorias (Tabela CFOP,
indRetor=1).
**Exceção 5: A regra de validação acima não se aplica nas NF-e de**
entrada (tpNF=0).
**Exceção 6: A regra de validação acima não se aplica nas operações**
com combustíveis (tag:comb) derivados de petróleo: código ANP
diferente de: 820101001, 820101010, 810102001, 810102004,
810102002, 810102003, 810101002, 810101001, 810101003,
220101003, 220101004, 220101002, 220101001, 220101005,
220101006, 560101001.
**Exceção 7: A regra de validação acima não se aplica se informada UF**
do local de entrega (tag: entrega/UF) igual à UF do emitente (tag:
emit/enderEmit/UF).
**Exceção 8: A regra de validação acima não se aplica para as**
operações com CFOP de Remessa de Mercadoria (Tabela CFOP,
indRemes=1).

**Página 9 / 24**

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

**Exceção 9: A regra de validação acima não se aplica para os CFOP: -**
6.552 - Transferência de bem do ativo imobilizado; - 6.922 -
Lançamento efetuado a título de simples faturamento decorrente de
venda p/ entrega futura; - 6.929 - Lançamento relativo a Cupom Fiscal.
**Exceção 10: Esta regra de validação não se aplica nas operações**
isentas (CST=40-Isenta ou CSOSN=103-Isento), imunes ou não
tributadas (CST=41-Não tributada, ou CSOSN=300-Imune, ou
CSOSN=400-Não tributada pelo Simples Nacional).
**Exceção 11: A regra de validação acima não se aplica nas NF-e**
complementares (finNFe=2) nem nas de ajuste (finNFe=3).
**Exceção 12: A regra de validação acima não se aplica para emitentes**
optantes pelo Simples Nacional (CRT=1).
NA09-30 55 Se informada alíquota interestadual (tag:pICMSInter) de 7% ou 12% em Obrig. 698 Rej. Rejeição: Alíquota interestadual do
NF de Saída Normal (tpNF=1 e finNFe=1) e alíquota interestadual ICMS incompatível com as UF
incompatível com as UF envolvidas: - 7% para os Estados de origem envolvidas na operação [nItem:999]
do Sul e Sudeste, exceto ES, destinado para os Estados do Norte,
Nordeste, Centro-Oeste e Espírito Santo; - 12% para os demais casos.
**Exceção 1: A regra de validação acima não se aplica para as**
operações com CFOP de Retorno de Mercadorias (Tabela CFOP,
indRetor=1).
**Exceção 2: A regra de validação não se aplica, em produção, para Nota**
Fiscal com data de emissão anterior a 01/07/2016.
**Exceção 3: A regra de validação não se aplica se informada UF do**
local de entrega (tag: entrega/UF) diferente da UF do emitente (tag:
enderEmit/UF);
**Exceção 4: A regra de validação não se aplica se informada UF do**
local de retirada (tag: retirada/UF) diferente da UF do destinatário (tag:
enderDest/UF);
**NA11-10 55 Percentual do ICMS Interestadual para a UF de destino Obrig. 699 Rej. Rejeição: Percentual do ICMS**
(tag:pICMSInterPart) difere do previsto para o ano da Data de Emissão.  Interestadual para a UF de destino
**Observação: Nas operações que não sejam de finalidade de emissão difere do previsto para o ano da Data**
normal (finNFe<>1) ou nas operações com CFOP de Retorno de de Emissão [nItem:999]
Mercadorias (Tabela CFOP, indRetor=1) considerar o ano da NF
referenciada em substituição ao ano da Data de Emissão.
**Exceção: A regra de validação não se aplica, em produção, para Nota**
Fiscal com data de emissão anterior a 01/01/2016.

**Página 10 / 24**

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

**Grupo X. Transporte da NF-e**

**Campo- ModelRegra de Validação AplicMsg EfeitDescrição Erro**
**Seq o . o**
X04-10 55 Obrigatória a informação de identificação do Transportador para os Facul. 362 Rej. Rejeição: Venda de combustível
CFOP de venda de combustível (tag: CNPJ/CPF, id:X04/X05) com esta
sem informação do
obrigatoriedade na Tabela CFOP, indComb=2.
Transportador
**Exceção 1: A regra de validação acima se aplica somente para a Nota**
Fiscal com Finalidade de Emissão normal (tag:finNFe=1);
**Exceção 2: A regra de validação acima se aplica somente para os**
Códigos de Produto ANP relacionados no Anexo XI.02 do MOC;
**Exceção 3: A regra de validação acima não se aplica se for informada**
a UF do Transportador no exterior (tag:transporta/UF=”EX”, id:X10)
**Observação: Nos casos em que não houver circulação física de**
mercadoria, os dados do transportador poderão ser preenchidos com o
CNPJ do próprio emitente do documento fiscal.

## 3 Novos registros na Tabela CFOP

A Tabela CFOP, disponibilizada no Portal Nacional da NF-e, fica atualizada com novos registros para o atendimento das cláusulas
previstas no Ajuste SINIEF 27/19, sendo que o mesmo Ajuste também altera CFOP existentes.

A Tabela CFOP, disponibilizada no Portal Nacional da NF-e, fica atualizada com novos registros para o atendimento das cláusulas
previstas no Ajuste SINIEF 20/19, sendo que o mesmo Ajuste também altera alguns CFOP existentes.

A Tabela CFOP, disponibilizada no Portal Nacional da NF-e, fica atualizada com novos registros para o atendimento das cláusulas
previstas no Ajuste SINIEF 07/19.

A Tabela CFOP, disponibilizada no Portal Nacional da NF-e, fica atualizada com novos registros para o atendimento das cláusulas
previstas no Ajuste SINIEF 11/18.

A Tabela CFOP, disponibilizada no Portal Nacional da NF-e, fica atualizada com novos registros para o atendimento das cláusulas
previstas no Ajuste SINIEF 18/17.

**Página 11 / 24**

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

A Tabela de CFOP publicada no Portal da NF-e mantém controles por CFOP para os indicadores abaixo, conforme consta na NT
2015.002:

● Indicador de CFOP que pode ser utilizado na NF-e (indNFe=1);
● Indicador de CFOP de comunicação (indComunica=1);
● Indicador de CFOP de transporte (indTransp=1);
● Indicador de CFOP de devolução (indDevol=1);

Nesta NT está sendo eliminado o “Anexo III – CFOP Específicos”, constante no MOC, e a ampliação deste “Anexo III – CFOP Específicos”,
constante na NT 2015.003.

Para suprir a necessidade de controle sobre os CFOP, foram incluídos novos indicadores na Tabela de CFOP, alterando as RV que citavam os
anexos eliminados.

Os novos indicadores vinculados ao CFOP são:

● Indicador de CFOP de retorno de mercadorias (indRetor=1);
● Indicador de CFOP de anulação de valor (indAnula=1);
● Indicador de CFOP de remessa de mercadorias (indRemes=1).
● Indicador de CFOP de combustível sem informação de transporte obrigatória (indComb=1).
● Indicador de CFOP de combustível com informação de transporte obrigatória (indComb=2).

**Página 12 / 24**

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

## 4 ANEXO I - Ajuste SINIEF 11/18 - Alterações e Inclusões de CFOP

### 4.1 CFOP alterados

“1.505 - Entrada decorrente de devolução de mercadorias remetidas para formação de lote de exportação, de produtos industrializados
ou produzidos pelo próprio estabelecimento
Classificam-se neste código as devoluções simbólicas ou físicas de mercadorias, bem como o retorno de mercadorias não entregues,
remetidas para formação de lote de exportação cujas saídas tenham sido classificadas no código “5.504 - Remessa de mercadorias para
formação de lote de exportação, de produtos industrializados ou produzidos pelo próprio estabelecimento”.
1.506 - Entrada decorrente de devolução de mercadorias, adquiridas ou recebidas de terceiros, remetidas para formação de lote de
exportação
Classificam-se neste código as devoluções simbólicas ou físicas de mercadorias, bem como o retorno de mercadorias não entregues,
remetidas para formação de lote de exportação em armazéns alfandegados, entrepostos aduaneiros ou outros estabelecimentos que
venham a ser regulamentados pela legislação tributária de cada Unidade Federada, efetuadas pelo estabelecimento depositário, cujas
saídas tenham sido classificadas no código “5.505 - Remessa de mercadorias, adquiridas ou recebidas de terceiros, para formação de
lote de exportação”.”;
“2.505 - Entrada decorrente de devolução de mercadorias remetidas para formação de lote de exportação, de produtos industrializados
ou produzidos pelo próprio estabelecimento
Classificam-se neste código as devoluções simbólicas ou físicas de mercadorias, bem como o retorno de mercadorias não entregues,
remetidas para formação de lote de exportação, cujas saídas tenham sido classificadas no código “6.504 - Remessa de mercadorias
para formação de lote de exportação, de produtos industrializados ou produzidos pelo próprio estabelecimento”.
2.506 - Entrada decorrente de devolução de mercadorias, adquiridas ou recebidas de terceiros, remetidas para formação de lote de
exportação
Classificam-se neste código as devoluções de mercadorias, bem como o retorno de mercadorias não entregues, remetidas para formação
de lote de exportação em armazéns alfandegados, entrepostos aduaneiros ou outros estabelecimentos que venham a ser
regulamentados pela legislação tributária de cada Unidade Federada, efetuadas pelo estabelecimento depositário, cujas saídas tenham

**Página 13 / 24**

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

sido classificadas no código “6.505 - Remessa de mercadorias, adquiridas ou recebidas de terceiros, para formação de lote de
exportação”.”.

### 4.2 CFOP incluídos

**“1.159 – Entrada decorrente do fornecimento de produto ou mercadoria de ato cooperativo**
Classificam-se neste código as entradas decorrentes de fornecimento de produtos ou mercadorias por estabelecimento de cooperativa
destinados a seus cooperados ou a estabelecimento de outra cooperativa, cujo fornecimento tenha sido classificado no código "5.159 –
Fornecimento de produção do estabelecimento de ato cooperativo” ou “5.160 – Fornecimento de mercadoria adquirida ou recebida de
terceiros de ato cooperativo”.”;
**“2.159 – Entrada decorrente do fornecimento de produto ou mercadoria de ato cooperativo**
Classificam-se neste código as entradas decorrentes de fornecimento de produtos ou mercadorias por estabelecimento de cooperativa
destinados a seus cooperados ou a estabelecimento de outra cooperativa, cujo fornecimento tenha sido classificado no código "6.159 –
Fornecimento de produção do estabelecimento de ato cooperativo” ou “6.160 – Fornecimento de mercadoria adquirida ou recebida de
terceiros de ato cooperativo”.”;
**“5.159 – Fornecimento de produção do estabelecimento de ato cooperativo**
Classificam-se neste código os fornecimentos de produtos industrializados ou produzidos pelo próprio estabelecimento de cooperativa
destinados a seus cooperados ou a estabelecimento de outra cooperativa.
**5.160 – Fornecimento de mercadoria adquirida ou recebida de terceiros de ato cooperativo**
Classificam-se neste código os fornecimentos de mercadorias adquiridas ou recebidas de terceiros, que não tenham sido objeto de
qualquer processo industrial no estabelecimento de cooperativa, destinados a seus cooperados ou a estabelecimento de outra
cooperativa.”;
**“6.159 – Fornecimento de produção do estabelecimento de ato cooperativo**
Classificam-se neste código os fornecimentos de produtos industrializados ou produzidos pelo próprio estabelecimento de cooperativa
destinados a seus cooperados ou a estabelecimento de outra cooperativa.
**6.160 – Fornecimento de mercadoria adquirida ou recebida de terceiros de ato cooperativo**

**Página 14 / 24**

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

Classificam-se neste código os fornecimentos de mercadorias adquiridas ou recebidas de terceiros, que não tenham sido objeto de
qualquer processo industrial no estabelecimento de cooperativa, destinados a seus cooperados ou a estabelecimento de outra
cooperativa.”;
**“7.504 - Exportação de mercadoria que foi objeto de formação de lote de exportação**
Classificam-se neste código as exportações das mercadorias cuja operação anterior tenha sido objeto de formação de lote de exportação,
e a remessa foi classificada nos códigos 5.504, 5.505, 6.505 ou 6.504 e a posterior devolução simbólica foi classificada nos códigos
1.505, 1.506, 2.505 ou 2.506.”.

## 5 ANEXO II - Ajuste SINIEF 07/19 - Inclusões de CFOP com as respectivas Notas Explicativas

**“1.215 – Devolução de fornecimento de produção do estabelecimento de ato cooperativo**

Classificam-se neste código as devoluções de fornecimentos de produtos industrializados ou produzidos pelo próprio estabelecimento
de cooperativa destinados a seus cooperados ou a estabelecimento de outra cooperativa, cujas saídas tenham sido classificadas no
código 5.159 – Fornecimento de produção do estabelecimento de ato cooperativo.

**1.216 – Devolução de fornecimento de mercadoria adquirida ou recebida de terceiros de ato cooperativo**

Classificam-se neste código as devoluções de fornecimentos de mercadorias adquiridas ou recebidas de terceiros, que não tenham sido
objeto de qualquer processo industrial no estabelecimento de cooperativa, destinados a seus cooperados ou a estabelecimento de outra
cooperativa, cujas saídas tenham sido classificadas no código 5.160  –  Fornecimento de mercadoria adquirida ou recebida de terceiros
de ato cooperativo.”;

**“2.215 – Devolução de fornecimento de produção do estabelecimento de ato cooperativo**

Classificam-se neste código as devoluções de fornecimentos de produtos industrializados ou produzidos pelo próprio estabelecimento
de cooperativa destinados a seus cooperados ou a estabelecimento de outra cooperativa, cujas saídas tenham sido classificadas no
código 6.159 – Fornecimento de produção do estabelecimento de ato cooperativo.

**2.216 – Devolução de fornecimento de mercadoria adquirida ou recebida de terceiros de ato cooperativo**

**Página 15 / 24**

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

Classificam-se neste código as devoluções de fornecimentos de mercadorias adquiridas ou recebidas de terceiros, que não tenham sido
objeto de qualquer processo industrial no estabelecimento de cooperativa, destinados a seus cooperados ou a estabelecimento de outra
cooperativa, cujas saídas tenham sido classificadas no código 6.160 – Fornecimento de mercadoria adquirida ou recebida de terceiros
de ato cooperativo.”;

**“5.216 – Devolução de entrada decorrente do fornecimento de produto ou mercadoria de ato cooperativo**

Classificam-se neste código as devoluções de entradas decorrentes de fornecimento de produtos ou mercadorias por estabelecimento
de cooperativa destinados a seus cooperados ou a estabelecimento de outra cooperativa, cujo fornecimento tenha sido classificado no
código 1.159 – Entrada decorrente do fornecimento de produto ou mercadoria de ato cooperativo.”;

**“6.216 – Devolução de entrada decorrente do fornecimento de produto ou mercadoria de ato cooperativo**

Classificam-se neste código as devoluções de entradas decorrentes de fornecimento de produtos ou mercadorias por estabelecimento
de cooperativa destinados a seus cooperados ou a estabelecimento de outra cooperativa, cujo fornecimento tenha sido classificado no
código 2.159 – Entrada decorrente do fornecimento de produto ou mercadoria de ato cooperativo.”.

## 6 ANEXO II - Ajuste SINIEF 20/19 – Alterações e Inclusões de CFOP com as respectivas
## Notas Explicativas

### 6.1 CFOP alterados

**“1.450 – SISTEMAS DE INTEGRAÇÃO E PARCERIA RURAL**

Classificam-se, neste grupo, as operações e prestações de integração e parceria rural. Constitui parceria rural o contrato agrário com
cessão, por tempo determinado ou não, do uso de imóvel rural, para exercer atividade agrícola, pecuária, agroindustrial, extrativa vegetal
ou mista; e ou entrega de animais para cria, recria, invernagem, engorda ou extração de matérias primas de origem animal, mediante

**Página 16 / 24**

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

partilha de riscos e frutos, produtos ou lucros havidos. Constitui integração vertical ou integração a relação contratual entre produtores
integrados e integradores que visa a planejar e a realizar a produção e a industrialização ou comercialização de matéria-prima, bens
intermediários ou bens de consumo final.

**1.451 - Entrada de animal - Sistema de Integração e Parceria Rural**

Classificam-se neste código as entradas de animais pelo sistema integrado e de produção animal, para criação, recriação ou engorda,
inclusive em sistema de confinamento. Também serão classificadas neste código as entradas do sistema de integração e produção
animal decorrentes de “ato cooperativo”, inclusive as operações entre cooperativa singular e cooperativa central.

**1.452 - Entrada de insumo - Sistema de Integração e Parceria Rural**

Classificam-se neste código as entradas de insumos pelo sistema integrado e de produção animal, para criação, recriação ou engorda,
inclusive em sistema de confinamento. Também serão classificadas neste código as entradas do sistema de integração e produção
animal decorrentes de “ato cooperativo”, inclusive as operações entre cooperativa singular e cooperativa central.”;

**1.908 - Entrada de bem por conta de contrato de comodato ou locação**

Classificam-se neste código as entradas de bens recebidos em cumprimento de contrato de comodato ou locação.

**1.909 - Retorno de bem remetido por conta de contrato de comodato ou locação**

Classificam-se neste código as entradas de bens recebidos em devolução após cumprido o contrato de comodato ou locação.

**2.908 - Entrada de bem por conta de contrato de comodato ou locação**

Classificam-se neste código as entradas de bens recebidos em cumprimento de contrato de comodato ou locação.

**2.909 - Retorno de bem remetido por conta de contrato de comodato ou locação**

Classificam-se neste código as entradas de bens recebidos em devolução após cumprido o contrato de comodato ou locação.”;

**5.450 - SISTEMAS DE INTEGRAÇÃO E PARCERIA RURAL**

**Página 17 / 24**

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

Classificam-se, neste grupo, as operações e prestações de integração e parceria rural. Constitui parceria rural o contrato agrário com
cessão, por tempo determinado ou não, do uso de imóvel rural, para exercer atividade agrícola, pecuária, agroindustrial, extrativa vegetal
ou mista; e ou entrega de animais para cria, recria, invernagem, engorda ou extração de matérias primas de origem animal, mediante
partilha de riscos e frutos, produtos ou lucros havidos. Constitui integração vertical ou integração a relação contratual entre produtores
integrados e integradores que visa a planejar e a realizar a produção e a industrialização ou comercialização de matéria-prima, bens
intermediários ou bens de consumo final.

**5.451 - Remessa de animal - Sistema de Integração e Parceria Rural**

Classificam-se neste código as saídas referentes à remessa de animais para criação, recriação, produção ou engorda em
estabelecimento de produtor no sistema integrado e de produção animal, inclusive em sistema de confinamento. Também serão
classificadas neste código as remessas decorrentes de “ato cooperativo”, inclusive as operações entre cooperativa singular e cooperativa
central.”.

**5.908 - Remessa de bem por conta de contrato de comodato ou locação**

Classificam-se neste código as remessas de bens para o cumprimento de contrato de comodato ou locação.

**5.909 - Retorno de bem recebido por conta de contrato de comodato ou locação**

Classificam-se neste código as remessas de bens em devolução após cumprido o contrato de comodato ou locação.

**6.908 - Remessa de bem por conta de contrato de comodato ou locação**

Classificam-se neste código as remessas de bens para o cumprimento de contrato de comodato ou locação.

**6.909 - Retorno de bem recebido por conta de contrato de comodato ou locação**

Classificam-se neste código as remessas de bens em devolução após cumprido o contrato de comodato ou locação.”.

### 6.2 CFOP incluídos

**Página 18 / 24**

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

**"1.453 - Retorno do animal ou da produção - Sistema de Integração e Parceria Rural**

Classificam-se neste código as entradas referentes ao retorno da produção, bem como de animais criados, recriados ou engordados
pelo produtor no sistema integrado e de produção animal, cujas saídas tenham sido classificadas no código “5.453 - Retorno de animal
ou da produção - Sistema de Integração e Parceria Rural”. Também serão classificados neste código os retornos do sistema de integração
e produção animal decorrentes de “ato cooperativo”, inclusive as operações entre cooperativa singular e cooperativa central.

**1.454 - Retorno simbólico do animal ou da produção - Sistema de Integração e Parceria Rural**

Classificam-se neste código as entradas referentes ao retorno simbólico da produção, bem como de animais criados, recriados ou
engordados pelo produtor no sistema integrado e de produção animal, cujas saídas tenham sido classificadas no código “5.454 - Retorno
simbólico de animal ou da produção - Sistema de Integração e Parceria Rural”.

**1.455 - Retorno de insumo não utilizado na produção - Sistema de Integração e Parceria Rural**

Classificam-se neste código os retornos de insumos não utilizados pelo produtor na criação, recriação ou engorda de animais pelo
sistema integrado e de produção animal, cujas saídas tenham sido classificadas no código “5.455 - Retorno de insumos não utilizados
na produção – Sistema de Integração e Parceria Rural”, inclusive as operações entre cooperativa singular e cooperativa central.

**1.456 - Entrada referente a remuneração do produtor no Sistema de Integração e Parceria Rural**

Classificam-se neste código as entradas da parcela da produção do produtor realizadas em sistema de integração e produção animal,
quando da entrega ao integrador ou parceiro. Também serão classificadas neste código as entradas decorrentes de “ato cooperativo”,
inclusive as operações entre cooperativa singular e cooperativa central.

**2.450 - SISTEMAS DE INTEGRAÇÃO E PARCERIA RURAL**

Classificam-se, neste grupo, as operações e prestações de integração e parceria rural. Constitui parceria rural o contrato agrário com
cessão, por tempo determinado ou não, do uso de imóvel rural, para exercer atividade agrícola, pecuária, agroindustrial, extrativa vegetal
ou mista; e ou entrega de animais para cria, recria, invernagem, engorda ou extração de matérias primas de origem animal, mediante
partilha de riscos e frutos, produtos ou lucros havidos. Constitui integração vertical ou integração a relação contratual entre produtores
integrados e integradores que visa a planejar e a realizar a produção e a industrialização ou comercialização de matéria-prima, bens
intermediários ou bens de consumo final.

**Página 19 / 24**

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

**2.451 - Entrada de animal - Sistema de Integração e Parceria Rural**

Classificam-se neste código as entradas de animais pelo sistema integrado e de produção animal, para criação, recriação ou engorda,
inclusive em sistema de confinamento. Também serão classificadas neste código as entradas do sistema de integração e produção
animal decorrentes de “ato cooperativo”, inclusive as operações entre cooperativa singular e cooperativa central.

**2.452 - Entrada de insumo - Sistema de Integração e Parceria Rural**

Classificam-se neste código as entradas de insumos pelo sistema integrado e de produção animal, para criação, recriação ou engorda,
inclusive em sistema de confinamento. Também serão classificadas neste código as entradas do sistema de integração e produção
animal decorrentes de “ato cooperativo”, inclusive as operações entre cooperativa singular e cooperativa central.

**2.453 - Retorno do animal ou da produção - Sistema de Integração e Parceria Rural**

Classificam-se neste código as entradas referentes ao retorno da produção, bem como dos de animais criados, recriados ou engordados
pelo produtor no sistema integrado e de produção animal, cujas saídas tenham sido classificadas no código “5.453 - Retorno de animal
ou da produção - Sistema de Integração e Parceria Rural”. Também serão classificados neste código os retornos do sistema de integração
e produção animal decorrentes de “ato cooperativo”, inclusive as operações entre cooperativa singular e cooperativa central.

**2.454 - Retorno simbólico do animal ou da produção - Sistema de Integração e Parceria Rural**

Classificam-se neste código as entradas referentes ao retorno simbólico da produção, bem como dos de animais criados, recriados ou
engordados pelo produtor no sistema integrado e de produção animal, cujas saídas tenham sido classificadas no código “5.454 - Retorno
simbólico de animal ou da produção - Sistema de Integração e Parceria Rural”.

**2.455 - Retorno de insumo não utilizado na produção - Sistema de Integração e Parceria Rural**

Classificam-se neste código os retornos de insumos não utilizados pelo produtor na criação, recriação ou engorda de animais pelo
sistema integrado e de produção animal, cujas saídas tenham sido classificadas no código “5.455 - Retorno de insumos não utilizados
na produção – Sistema de Integração e Parceria Rural”, inclusive as operações entre cooperativa singular e cooperativa central.

**2.456 - Entrada referente a remuneração do produtor no Sistema de Integração e Parceria Rural**

**Página 20 / 24**

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

Classificam-se neste código as entradas da parcela da produção do produtor realizadas em sistema de integração e produção animal,
quando da entrega ao integrador ou parceiro. Também serão classificadas neste código as entradas decorrentes de “ato cooperativo”,
inclusive as operações entre cooperativa singular e cooperativa central.”;

**5.452 - Remessa de insumo - Sistema de Integração e Parceria Rural**

Classificam-se neste código as saídas referentes à remessa de insumos para utilização em estabelecimento de produtor no sistema
integrado e de produção animal, para criação, recriação ou engorda, inclusive em sistema de confinamento. Também serão classificadas
neste código as remessas decorrentes de “ato cooperativo”, inclusive as operações entre cooperativa singular e cooperativa central.

**5.453 - Retorno de animal ou da produção - Sistema de Integração e Parceria Rural**

Classificam-se neste código as saídas referentes ao retorno da produção, bem como dos animais criados ou engordados pelo produtor
no sistema integrado e de produção animal, inclusive em sistema de confinamento. Também serão classificados neste código os retornos
decorrentes de “ato cooperativo”, inclusive as operações entre cooperativa singular e cooperativa central.

**5.454 - Retorno simbólico de animal ou da produção - Sistema de Integração e Parceria Rural**

Classificam-se neste código as saídas referentes ao retorno simbólico da produção, bem como de animais criados ou engordados pelo
produtor no sistema integrado e de produção animal, inclusive em sistema de confinamento.

**5.455 - Retorno de insumos não utilizados na produção - Sistema de Integração e Parceria Rural**

Classificam-se neste código as saídas referentes ao retorno de insumos não utilizados em estabelecimento de produtor no sistema
integrado e de produção animal, para criação, recriação ou engorda, inclusive em sistema de confinamento e nas operações entre
cooperativa singular e cooperativa central

**5.456 - Saída referente a remuneração do produtor - Sistema de Integração e Parceria Rural**

Classificam-se neste código as saídas da parcela da produção do produtor realizadas em sistema de integração e produção animal,
quando da entrega ao integrador ou parceiro. Também serão classificadas neste código as saídas decorrentes de “ato cooperativo”,
inclusive as operações entre cooperativa singular e cooperativa central.

**6.450 - SISTEMAS DE INTEGRAÇÃO E PARCERIA RURAL**

**Página 21 / 24**

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

Classificam-se, neste grupo, as operações e prestações de integração e parceria rural. Constitui parceria rural o contrato agrário com
cessão, por tempo determinado ou não, do uso de imóvel rural, para exercer atividade agrícola, pecuária, agroindustrial, extrativa vegetal
ou mista; e ou entrega de animais para cria, recria, invernagem, engorda ou extração de matérias primas de origem animal, mediante
partilha de riscos e frutos, produtos ou lucros havidos. Constitui integração vertical ou integração a relação contratual entre produtores
integrados e integradores que visa a planejar e a realizar a produção e a industrialização ou comercialização de matéria-prima, bens
intermediários ou bens de consumo final.

**6.451 - Remessa de animal - Sistema de Integração e Parceria Rural**

Classificam-se neste código as saídas referentes à remessa de animais para criação, recriação, produção ou engorda em
estabelecimento de produtor no sistema integrado e de produção animal, inclusive em sistema de confinamento. Também serão
classificadas neste código as remessas decorrentes de “ato cooperativo”, inclusive as operações entre cooperativa singular e cooperativa
central.

**6.452 - Remessa de insumo - Sistema de Integração e Parceria Rural**

Classificam-se neste código as saídas referentes à remessa de insumos para utilização em estabelecimento de produtor no sistema
integrado e de produção animal, para criação, recriação ou engorda, inclusive em sistema de confinamento. Também serão classificadas
neste código as remessas decorrentes de “ato cooperativo”, inclusive as operações entre cooperativa singular e cooperativa central.

**6.453 - Retorno de animal ou da produção - Sistema de Integração e Parceria Rural**

Classificam-se neste código as saídas referentes ao retorno da produção, bem como de animais criados, recriados ou engordados pelo
produtor no sistema integrado e de produção animal, inclusive em sistema de confinamento. Também serão classificados neste código
os retornos decorrentes de “ato cooperativo”, inclusive as operações entre cooperativa singular e cooperativa central.

**6.454 - Retorno simbólico de animal ou da produção - Sistema de Integração e Parceria Rural**

Classificam-se neste código as saídas referentes ao retorno simbólico da produção, bem como de animais criados ou engordados pelo
produtor no sistema integrado e de produção animal, inclusive em sistema de confinamento.

**6.455 - Retorno de insumos não utilizados na produção - Sistema de Integração e Parceria Rural**

**Página 22 / 24**

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

Classificam-se neste código as saídas referentes ao retorno de insumos não utilizados em estabelecimento de produtor no sistema
integrado e de produção animal, para criação, recriação ou engorda, inclusive em sistema de confinamento, e nas operações entre
cooperativa singular e cooperativa central

**6.456 - Saída referente a remuneração do produtor - Sistema de Integração e Parceria Rural**

Classificam-se neste código as saídas da parcela da produção do produtor realizadas em sistema de integração e produção animal,
quando da entrega ao integrador ou parceiro. Também serão classificadas neste código as saídas decorrentes de “ato cooperativo”,
inclusive as operações entre cooperativa singular e cooperativa central.”.

## 7 ANEXO II - Ajuste SINIEF 27/19 – Alteração e Inclusões de CFOP com as respectivas Notas
## Explicativas

### 7.1 CFOP alterado

“5.929 – Lançamento efetuado em decorrência de emissão de documento fiscal relativo a operação ou prestação também acobertada
por documento fiscal do varejo.

Classificam-se neste código os registros relativos aos documentos fiscais emitidos em operações ou prestações que também tenham
sido acobertadas por documento fiscal do varejo.”.

### 7.2 CFOP incluídos

“1.657 - Retorno de remessa de combustível ou lubrificante para venda fora do estabelecimento. Classificam-se neste código as entradas
em retorno de combustível ou lubrificante remetidos para venda fora do estabelecimento, inclusive por meio de veículos, e não
comercializados.

**Página 23 / 24**

---

**Projeto**
**Nota Fiscal Eletrônica**
**NT 2017.002**

**“2.657 - Retorno de remessa de combustível ou lubrificante para venda fora do estabelecimento.**
Classificam-se neste código as entradas em retorno de combustível ou lubrificante remetidos para venda fora do estabelecimento,
inclusive por meio de veículos, e não comercializados.”.

**Página 24 / 24**
