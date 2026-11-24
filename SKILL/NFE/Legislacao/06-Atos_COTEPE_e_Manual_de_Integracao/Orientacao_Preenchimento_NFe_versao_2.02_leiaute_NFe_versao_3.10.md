**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

# Projeto Nota Fiscal Eletrônica

### Orientação de Preenchimento da NF-e - versão 2.02 –  04/02/2015 –
**adaptado para a versão 3.10 do leiaute da NF-e.**

### Divulga orientação sobre como gerar a NF-e em situações
### específicas que têm suscitado dúvidas pelos Contribuintes do
### ICMS.

## Fevereiro-2015

_________________________________________________________________________________________

**Pág. 1 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

**Sumário**

Orientação para informar o grupo ICMS na operação com Diferimento Parcial do ICMS...................................... 3

Dispensa da emissão da DI, DSI ou outro documento controlado pela RFB ........................................................... 4

Transferência de crédito do ICMS/ressarcimento/restituição do ICMS-ST ............................................................ 6

NF-e Complementar .............................................................................................................................................. 10

Venda de Mercadoria a Pessoa Física Estrangeira ................................................................................................ 14

Mercadoria com unidade comercial diferente da unidade tributada. .................................................................. 15

NF-e  destinada a Zona Franca de Manaus (ZFM) ................................................................................................. 17

Simples Nacional ................................................................................................................................................... 19

_________________________________________________________________________________________

**Pág. 2 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

### Orientação para informar o grupo ICMS na operação com Diferimento Parcial do
### ICMS

O Diferimento Parcial do ICMS é uma técnica de tributação que adia o pagamento de uma parcela do
imposto devido na operação para uma etapa posterior, prevista na legislação ou no Regime Especial
concedido pela unidade da Federação.
Exemplo de demonstração do cálculo do ICMS de uma operação com diferimento parcial:
Valor da Mercadoria R$ 1.000,00 (a)
Alíquota do ICMS 18% (b)
Valor do ICMS da operação (18% de R$ 1.000,00) R$ 180,00 (c) = (a) x (b)
Percentual do ICMS diferido 33,33% (Previsto na legislação do Estado ou no Regime Especial
concedido) (d)
Valor do ICMS diferido (33,33% de R$ 180,00) R$ 60,00 (e) = (c) x (d)
Valor do ICMS devido (R$ 180,00 – R$ 60,00) R$ 120,00 (f) = (c) – (d)
O valor do ICMS da operação é R$ 180,00, mas a legislação permite o diferimento parcial de 33,33%
deste valor, sendo devido o ICMS no valor de R$ 120,00, que corresponde à diferença do ICMS da
operação (R$ 180,00) e a parcela do ICMS diferido (R$ 60,00).

A estrutura do grupo ICMS 51 foi adequada, na versão 3.10 do leiaute da NF-e, para tratar o
Diferimento parcial com a criação dos campos destacados em amarelo abaixo:

Os valores do exemplo citado acima devem ser informados na NF-e conforme abaixo:
<ICMS>
<ICMS51>
<orig>0</orig>
<CST>51</CST>
<modBC>3</modBC>
<vBC>1000.00</vBC>
<pICMS>18.00</pICMS>
<vICMSOp>180.00</vICMSOp> Valor do ICMS da Operação ( Valor como se não tivesse o
diferimento)
<pDif>33.33</pDif > Percentual de diferimento
<vICMSDif>60.00</vICMSDif> Valor do ICMS diferido
<vICMS>120.00</vICMS> Valor do ICMS realmente devido
<ICMS51>
<ICMS>

A informação de que o imposto foi parcialmente diferido e o seu valor seguido do correspondente
dispositivo legal deve ser informado na tag infCpl. Segue exemplo:

_________________________________________________________________________________________

**Pág. 3 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

<infAdic>
<infCpl>Operação com diferimento parcial do imposto no valor de R$ 60,00 ( 33,33% de R$
180,00) nos termos do inciso I do art.96 do Decreto n° 1.980/07 (RICMS/PR). </infCpl>
</infAdic>

Os campos modBC (Modalidade de determinação da base de cálculo do ICMS), pRedBC (Percentual
da Redução de BC), vBC (Valor da BC do ICMS), pICMS (Alíquota do imposto), vICMSOp (Valor
do ICMS da Operação), pDif (Percentual do diferimento), vICMSDif (Valor do ICMS diferido) e
**vICMS (Valor do ICMS) só devem ser preenchidos no caso do diferimento ser parcial, exceto se**
**alguma SEFAZ exigir o preenchimento dos mesmos no caso do diferimento total. No caso de**
diferimento parcial, alertamos que os campos modBC (Modalidade de determinação da BC do ICMS),
pRedBC (Percentual da Redução de BC), vBC (Valor da BC do ICMS), pICMS (Alíquota do
imposto), vICMSOp (Valor do ICMS da Operação) devem ser preenchidos com o valor como se não
tivesse o diferimento.

### Dispensa da emissão da DI, DSI ou outro documento controlado pela RFB

Nos casos específicos de emissão de NF-e com CFOP iniciado com 3 que não constem da exceção
à regra de validação disposta abaixo, deverão ser informados os números de referência ao processo
de importação (DI, DSI, NTS, etc.) ou a expressão “NIHIL” caso não haja documento de referência.

Exemplo prático: A operação foi concluída sem geração de nenhum documento de
importação. Nesse caso deve ser informada a expressão “NIHIL” no campo “Número DI/DSI/
DIRE,...)” – tag “nDI.”.
Sugerimos repetir a data da emissão da NF-e “dd/mm/aaaa” no campo “ Data de Registro do
documento” (tag “dDI");
No campo “Local de desembaraço” (tag “xLocDesemb”), informar a unidade de onde foi retirada a
mercadora;
O campo “Número da Adição” (tag “nAdicao”) deve ser preenchido com “999”.

_________________________________________________________________________________________

**Pág. 4 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

Observação: os dados destacados em amarelo foram inseridos na versão 3.10 do leiaute da NF-e.

Exemplo de XML, considerando a data de emissão da NF-e/desembaraço em 08/11/2011, UF
= “MG” e via de transporte = “Aérea” (“4”):
- <DI>
<nDI>NIHIL</nDI>
<dDI>2011-11-08</dDI>
<xLocDesemb>local de retirada</xLocDesemb>
<UFDesemb>MG</UFDesemb>
<dDesemb>2011-11-08</dDesemb>
<tpViaTransp>4</tpViaTransp>
<tpIntermedio>1</tpIntermedio>
<cExportador>Código do Fornecedor</cExportador>
- <adi>
<nAdicao>999</nAdicao>
<nSeqAdic>1</nSeqAdic>
<cFabricante> Código do Fabricante</cFabricante>

_________________________________________________________________________________________

**Pág. 5 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

</adi>
</DI>

Ou seja, se tiver NTS (Nota de Tributação Simplificada) ou qualquer outro documento com
registro no SISCOMEX, deverá ser digitado esse número no campo“Número DI/DSI/
DIRE,...)” – tag “nDI.”.
Fora dessas situações, aí sim o campo “Número DI/DSI/ DIRE,...)” – tag “nDI.” será
preenchido com a expressão "NIHIL".

No caso do preenchimento com a expressão “NIHIL”, sugerimos que seja informado na
NF-e o código de “Rastreamento de objetos” no grupo de Informações Adicionais – tag
“infAdFisco” ou “infCpl”.

### Transferência de crédito do ICMS/ressarcimento/restituição do ICMS-ST

A nota fiscal eletrônica (NF-e) também será emitida nas hipóteses de transferências de crédito
acumulado de ICMS assim como nos casos de restituição do ICMS.
De acordo com a legislação, há regras a serem observadas para a emissão da NF-e nessas
hipóteses.

Destacam-se o preenchimento de alguns campos conforme abaixo:

. No local destinado ao valor da operação do quadro “Cálculo do Imposto”, o valor do crédito
acumulado transferido ou do valor do ICMS a ser ressarcido/restituído (no aplicativo gratuito de NF-e,
esse valor será informado no Valor Total bruto). Nos demais campos, preencher com “0” (zero) para
todos locais numéricos e obrigatórios nos quais não consta orientação específica;
. Como natureza da operação: “Transferência de Crédito Acumulado de ICMS” ou “Ressarcimento de
ICMS” ou “Restituição de ICMS/ST”, conforme disposto na legislação estadual;

. No campo “Finalidade de emissão” informar “NF-e de Ajuste”;
. Utilizar o CST “090”;
. O código do produto deverá ser preenchido com “CFOP5601” ou “CFOP5602” ou “CFOP5603”,
conforme o caso;
. A “Descrição do Produto” será informada com a mesma expressão do campo da natureza da
operação;
. O código NCM deverá ser informado como “00”;
. Situação tributária do PIS e da COFINS: “Operação sem incidência da Contribuição”;
. “Modalidade do frete”: indicar “Sem frete”.

**Instruções Específicas para o preenchimento dos seguintes campos da NF-e**
_________________________________________________________________________________________

**Pág. 6 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

**A) Identificação da Nota Fiscal eletrônica:**
Informar a Natureza da operação = “Transferência de crédito acumulado de ICMS” ou
“Ressarcimento de ICMS” ou “Restituição de ICMS/ST”, conforme disposto na legislação estadual.

Informar a Finalidade da emissão = “3 - NF-e de ajuste”.

**B) Produtos e Serviços da NF-e**

1. Código do Produto – utilizar a expressão “CFOP” + o código do CFOP.

Ex.: CFOP=5601, Código do produto = “CFOP5601”.

2. Descrição do produto – preencher com o mesmo conteúdo do campo Natureza da Operação.
Caso o regulamento obrigue mais informações, complementar no próprio campo ou em Informações
Adicionais.

Poderá ser usado o campo de “Informações Adicionais do Produto”:

Ou os campos de “Informações Adicionais” da NF-e (tag “infAdic”)..

Caso haja referência a algum Processo Tributário Administrativo, deve ser utilizado esse grupo
de informações (tag “infAdic”), inserindo o número do processo no campo “Identificador do
processo ou ato concessório” – tag “nProc”:

_________________________________________________________________________________________

**Pág. 7 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

3. Código NCM – informar “00”.

4. Campo Código Fiscal de Operações e Prestações – informar o CFOP (“5601” ou  “5602” ou
“5.603”), conforme o caso.

5. A Unidade Comercial, a Quantidade Comercial e o Valor Unitário de Comercialização serão
informados com o dígito “0” (zero).
Caso o sistema da empresa exija valores diferentes de zero para esses campos, a unidade comercial
poderá ser preenchida com o conteúdo “Un”, quantidade comercial = “1” e valor unitário igual ao
valor da transferência/ressarcimento/restituição.

6. Valor Total Bruto dos Produtos ou Serviços – informar o valor total da
transferência/ressarcimento/restituição.

7. A Unidade Tributável, a Quantidade Tributável e o Valor Unitário de tributação serão informados
com o dígito “0” (zero).
Caso o sistema da empresa exija valores diferentes de zero para esses campos, a unidade tributável
poderá ser preenchida com o conteúdo “Un”, quantidade tributável = “1” e valor unitário igual ao valor
da transferência/ressarcimento/restituição.
_________________________________________________________________________________________

**Pág. 8 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

8. Origem da mercadoria – informar “0” e Código de Situação Tributária – CST – informar “90”.

9. Código de Situação Tributária de PIS e de COFINS – informar a não incidência destes tributos na
operação.

_________________________________________________________________________________________

**Pág. 9 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

**C) Informações do Transportes da NF-e**

Informar a modalidade sem frete.

### NF-e Complementar

A Nota Fiscal Complementar é emitida para acrescentar dados e valores antes não informados no
documento fiscal original, observando as definições da legislação, tais como:

 Na exportação, se o valor resultante do contrato de câmbio acarretar acréscimo ao valor da
operação constante na Nota Fiscal;
 Na regularização em virtude de diferença no preço, em operação ou prestação, ou na
quantidade de mercadoria;
 Para lançamento do imposto, não efetuado em época própria, em virtude de erro de cálculo
ou de classificação fiscal.

Desse modo, o contribuinte deverá emitir nota fiscal eletrônica complementar quando o documento
fiscal original consignar quantidade de mercadoria e/ou valor inferior ao da efetiva operação. Assim,
essa NF-e corresponderá a diferença de quantidade ou de valor, fazendo constar na mesma o motivo
de sua emissão e a referência da nota fiscal original, devendo o emitente escriturá-la no livro
Registro de Saída no período em que for emitida. Neste documento constará a mesma informação
sobre o tipo de tributação ocorrida na operação original, ou seja, tributação normal, diferimento e
outros.

***Instruções Específicas para o preenchimento dos seguintes campos da NF-e:***

O contribuinte preencherá o dado não informado na nota fiscal original e, para os demais, o
complemento ou o dígito “0” (zero) nos campos numéricos e obrigatórios para os quais não constar
orientação específica.

**A) Identificação da Nota Fiscal eletrônica:**

1. Informar a finalidade da emissão = “NF-e Complementar”.
_________________________________________________________________________________________

**Pág. 10 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

2. Os dados de identificação do documento fiscal original, que está sendo complementado,
deverão ser informados na NF-e Complementar na aba “Informação de Documentos Fiscais
referenciados”. A chave de acesso deverá ser informada quando a nota fiscal original for NF-
e.

**B) Produtos e Serviços da NF-e**

1. Caso algum produto venha a ter complemento de quantidade, deverá ser informado o
respectivo código e o correspondente valor do complemento.
Se o complemento não se referir a algum produto, deverá ser criado código “escritural” para
identificação do complemento. Exemplo: CFOP=5.949, Código do produto = “CFOP5.949”.

_________________________________________________________________________________________

**Pág. 11 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

2. Caso o complemento não se refira a algum produto, deverá ser informada uma descrição
“escritural” (tag “xProd”) para identificação do complemento. Exemplo: “Nota Fiscal
Complementar referente à falta de destaque do valor do ICMS na nota fiscal original”.

3. Entretanto, há situações relacionadas à alteração de preço da mercadoria, sem alteração de
quantidade, que poderão afetar escrituração fiscal em um sistema integrado. Neste caso,
sugere-se que o contribuinte utilize o código e a respectiva descrição da mercadoria e informe
o dígito “0” (zero) nos campos de quantidade.

Para facilitar o entendimento, abaixo um exemplo do XML:

- <prod>
<cProd>0</cProd>
<cEAN /> [preencher o código EAN, se houver]
<xProd>Descrição da Mercadoria</xProd>
<NCM>Classificação Fiscal da Mercadoria</NCM>
<CFOP>5949</CFOP>
<uCom>0</uCom>
<qCom>00000</qCom>
<vUnCom>10.0000000000</vUnCom>
<vProd>10.00</vProd>
<cEANTrib />
<uTrib>0</uTrib>
<qTrib>0.0000</qTrib>
<vUnTrib>10.0000000000</vUnTrib>
<indTot>1</indTot>
</prod>
- <imposto>
- <ICMS>
- <ICMS00>
<orig>0</orig>
_________________________________________________________________________________________

**Pág. 12 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

<CST>00</CST>
<modBC>3</modBC>
<vBC>10.00</vBC>
<pICMS>18.00</pICMS>
<vICMS>1.80</vICMS>
</ICMS00>
**</ICMS>**

4. Código NCM – informar “00” quando não for indicar produto ou mercadoria. Do contrário,
informar a classificação fiscal do produto ou mercadoria descrita.

**Observação: Para todos os outros campos numéricos e obrigatórios, para os quais não constar**
orientação específica, preencher com o dígito “0” (zero).

**C) Informações Adicionais da NF-e:**

O contribuinte indicará o dispositivo legal neste campo e as demais informações do documento
fiscal original de interesse do contribuinte.

**D) Informações do Transporte da NF-e**

Informar a modalidade sem frete, código “9”.

_________________________________________________________________________________________

**Pág. 13 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

### Venda de Mercadoria a Pessoa Física Estrangeira

***A NF-e emitida para turista estrangeiro não inscrito no Cadastro de Pessoa Física (CPF) deve seguir***
a mesma forma adotada para a natureza da operação como se fosse destinada ao cidadão brasileiro
consumidor final.

**O contribuinte emitirá uma nota fiscal eletrônica de venda utilizando um CFOP de operação interna**
**e informará os dados e o endereço original do consumidor estrangeiro.**
Nesse caso deverá ser informada a identificação do estrangeiro na tag “idEstrangeiro”, assim como:
- na tag "PAÍS" o país de origem;
- na tag "UF" a sigla "EX";
- na tag "Município" deve constar a expressão “EXTERIOR”.
- o campo de indicador de operação com consumidor final (“IndFinal”) deverá ser preenchido com “1”
(Consumidor final);
- campo “indIEDest” (Tipo de Contribuinte) – preencher com “9” (Não Contribuinte).

***Instruções Específicas para o preenchimento dos seguintes campos da NF-e:***
**A) Identificação do Emitente da Nota Fiscal eletrônica:**

Informar a finalidade da emissão = “NF-e normal”.

Preencher o indicador de operação com “1” (Consumidor final).

**B) Identificação do Destinatário da Nota Fiscal Eletrônica**

Informar o nome do País de origem do turista estrangeiro, a expressão “EXTERIOR” no campo
“Nome do Município” e a sigla “EX” na “UF” (Unidade da Federação). O campo indicador de IE
(indIEDest) deve ser preenchido com “9”.

_________________________________________________________________________________________

**Pág. 14 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

**C) Produtos e Serviços da NF-e**

1. Código Fiscal de Operações e Prestações– utilizar o código do CFOP de operação interna
(5.xxx) de acordo com a legislação.

**D) Informações Adicionais da NF-e:**

O contribuinte indicará o dispositivo legal neste campo e as demais informações de interesse do
contribuinte.

### Mercadoria com unidade comercial diferente da unidade tributada.

As empresas nas suas relações comerciais efetivam a negociação através de unidades de medidas
já costumeiras no mercado. Tal linguagem mercantil facilita o entendimento entre as partes e agiliza
o consenso na interação para a venda-compra da mercadoria.

Tendo em vista a necessidade do fisco de padronização das unidades de medidas informadas nos
documentos fiscais foi criado o campo de unidade tributável.  É o caso, por exemplo, da unidade
comercial ser acordada como “tonelada” e nos registros fiscais a unidade tributável ser adotada como
“quilograma”. Isso também ocorre nas grandezas barril, fardo, arroba e outras.

Com isso, conceituam-se a “Unidade Tributável” como sendo  o padrão de medida adotado pelo fisco
para determinado produto; e a “Unidade Comercial” aquela medida quantitativa que usualmente já
vem sendo utilizada no ambiente da negociação (costume).

Tais unidades devem ser vinculadas com o objetivo de alcançar a mesma quantidade envolvida na
operação (exemplo: 01 (uma) tonelada representa 1.000 (mil) quilogramas). Desse modo, é
_________________________________________________________________________________________

**Pág. 15 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

importante observar que o valor unitário dessas grandezas não serão idênticos, pois o valor total
bruto dos mercadorias consignado na NF-e é o mesmo para cada medida quantitativa:

- 01 (uma) tonelada com preço de venda unitário de R$ 10.000,00 é o mesmo que 1.000 (mil)
quilogramas com preço de venda unitário de R$ 10,00.

Informamos, a título de exemplo, as Portarias 363/2011 e 7/2012 publicadas pela SEFAZ/MT.

Segue, abaixo, procedimentos específicos para emissão da nota fiscal eletrônica que deverão ser
observados.

***Instruções Específicas para o preenchimento dos seguintes campos da NF-e:***

**A) Produtos e Serviços da NF-e**
1. Na descrição do produto, o contribuinte indicará a mercadoria envolvida na operação.

2. Informar a unidade de medida costumeiramente utilizada no mercado (exemplo: tonelada,
barril, fardo, arroba, quilograma, litro e outras), a quantidade vendida e o seu valor unitário
que estão diretamente vinculados a esta medida de grandeza.

_________________________________________________________________________________________

**Pág. 16 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

3. .Informar a unidade de medida padrão adotada pelo fisco para esse produto , a quantidade
vendida e seu valor unitário que estão diretamente vinculados a esta medida de grandeza.

### NF-e  destinada a Zona Franca de Manaus (ZFM)

No leiaute versão 3.10 da NF-e foi criado o campo “vICMSDeson” para tratar a desoneração do
ICMS como desconto tributário de forma que a NF-e passou a ter dois campos de desconto: - um
para informação do desconto comercial (tag “vDesc”), já existente na versão 2.0 e o campo de
desconto tributário (tag “vICMSDeson”) criado para informar o valor do ICMS desonerado, caso em
que esse valor deve ser abatido do preço da mercadoria nas situações definidas pela legislação das
SEFAZ.
A informação da desoneração do ICMS está prevista para os seguintes grupos de CST:
- ICMS20 – CST 20: Redução de base de cálculo
- ICMS30 – CST 30: Isenta ou não tributada e com cobrança do ICMS por ST
- ICMS40 – CST 40,41, 50: Isenta, Não tributada ou Suspensão
- ICMS70 – CST 70: Redução de base de cálculo e cobrança do ICMS por ST
- ICMS90 – CST 90: Outros

**ORIENTAÇÕES PARA PREENCHIMENTO**

A emissão de NF-e para acobertar operações incentivadas destinadas à Zona Franca de Manaus
(ZFM) e Áreas de Livre Comércio (ALC) deverá observar, para o preenchimento dos campos do
documento fiscal, as recomendações que seguem:
Os exemplos de preenchimento tomam com base a seguinte operação hipotética:
 Grupo de CST = “40”
 UF do remetente: MG (alíquota interestadual de 7%)
 Valor bruto do produto sem descontos: R$ 1.000,00

_________________________________________________________________________________________

**Pág. 17 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

 Desconto comercial: R$ 200,00
 Base de Cálculo do ICMS para fins de cálculo do abatimento: R$ 800,00 (R$ 1.000,00 – R$
200,00)
 Valor do ICMS abatido: R$ 56,00 (7% sobre R$ 800,00)
 Valor da Nota: R$ 744,00 (R$ 1.000,00 – R$ 200,00 – R$ 56,00)

1. Grupo de Identificação do Destinatário
Informar obrigatoriamente a Inscrição na SUFRAMA.

2. Grupo do Detalhamento de Produtos e Serviços
**2.1  Informar no campo “Valor Total Bruto dos Produtos ou Serviços” o valor do produto sem a**
**desoneração do ICMS.**
Exemplo de XML:
<vProd>1000.00</vProd>

2.2. Informar no campo “Valor do Desconto” o valor do desconto comercial.
Exemplo de XML:
<vDesc>200.00</vDesc>

3. Grupo de Tributação do ICMS
3.1 Preencher o grupo de tributação do ICMS 40
 Origem da Mercadoria: “0” (“nacional”)
 CST: “40” (“isenta”)
 Valor do ICMS (tag “vICMSDeson”): informar o valor do ICMS que foi abatido na operação.
 Motivo da desoneração do ICMS: “7” (“SUFRAMA”)

Exemplo de XML:
<ICMS40>
<orig>0</orig>
<CST>40</CST>
<vICMSDeson>56.00</vICMSDeson>
<motDesICMS>7</motDesICMS>
</ICMS40>

4. Grupo de Tributação do PIS
Preencher o grupo de tributação do PIS não tributado
CST: 06 – Operação Tributável (alíquota zero)
Exemplo de XML:
<PISNT>
<CST>06</CST>
<PISNT>

5. Grupo de Tributação da COFINS
_________________________________________________________________________________________

**Pág. 18 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

Preencher o grupo de tributação da COFINS não tributada
CST: 06 – Operação Tributável (alíquota zero)
Exemplo de XML:
<COFINSNT>
<CST>06</CST>
</COFINSNT>

6. Grupo de Valores Totais da NF-e
Valor Total do ICMS:
<ICMSTot>
<vBC>0.00</vBC>
<vICMS>0.00</vICMS>
<vICMSDeson>56.00</vICMSDeson>
<vBCST>0.00</vBCST>
<vST>0.00</vST>
<vProd>1000.00</vProd>
<vFrete>0.00</vFrete>
<vSeg>0.00</vSeg>
<vDesc>200.00</vDesc>
<vII>0.00</vII>
<vIPI>0.00</vIPI>
<vPIS>0.00</vPIS>
<vCOFINS>0.00</vCOFINS>
<vOutro>0.00</vOutro>
<vNF>744.00</vNF>
</ICMSTot>

7. Grupo de Informações Adicionais
Informações Adicionais de Interesse do Fisco conforme legislação das SEFAZ, como por exemplo:
“Remessa para Zona Franca de Manaus ou Área de Livre Comércio. Isenção de ICMS (Convênio
ICMS 65/88). Isenção de IPI (Art. 81 do RIPI - Decreto 7.212 de 15 de junho de 2010). Redução a
zero das alíquotas do PIS e COFINS (art. 2º da Lei 10.996, de 15/12/2004).”

### Simples Nacional

**Orientações de preenchimento da NF-e para contribuintes do Simples Nacional**

A NF-e emitida por Microempresa (ME) ou Empresa de Pequeno Porte (EPP) optante pelo
Simples Nacional deve observar as disposições da Seção VIII, Subseção I da Resolução
CGSN nº 94 de 29 de novembro de 2011 e do Ajuste SINIEF nº 3, de 09/07/2010.
Sem prejuízo dos demais campos obrigatórios, a emissão da NF-e por estabelecimento de
ME/EPP optante pelo Simples Nacional deverá observar as recomendações desta Nota
Técnica.

_________________________________________________________________________________________

**Pág. 19 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

**Recomendações para o preenchimento da NF-e por ME/EPP optante pelo Simples**
**Nacional:**

1. Grupo de tributos de PIS

Informar o código “99” (“outras operações”) no campo CST.
Exemplo de XML:
**<PISOutr>  * Situação Tributária: PIS 99 – Outras**
**<CST>99</CST> Operações**
- Tipo de Cálculo: Percentual
**<qBCProd>0.0000</qBCProd>**
- Valor da Base de Cálculo: 0,00
**<vAliqProd>0.0000</vAliqProd>**
- Alíquota: 0,00
**<vPIS>0.00</vPIS>**
- Valor do PIS: 0,00
</PISOutr>

2. Grupo de tributos de COFINS

Informar o código “99” (“outras operações”) no campo CST.

Exemplo de XML:

**<COFINSOutr>  * Situação Tributária: COFINS 99 –**
**Outras Operações**
**<CST>99</CST>**
- Tipo de Cálculo: Percentual
**<qBCProd>0.0000</qBCProd>**
- Valor da Base de Cálculo: 0,00
**<vAliqProd>0.0000</vAliqProd>**
- Alíquota: 0,00
**<vCOFINS>0.00</vCOFINS>**
- Valor do PIS: 0,00
</COFINSOutr>

3. Grupo de tributos de ICMS (Normal ou ST)

**TABELA “A” - Código de Regime Tributário – CRT**
**1 - Simples Nacional**
**2 - Simples Nacional - excesso de sublimite da receita bruta**
**3 - Regime Normal**

_________________________________________________________________________________________

**Pág. 20 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

**O código “1” será preenchido pelo contribuinte quando for optante pelo Simples**
**Nacional.**
**O código “2” será preenchido pelo contribuinte optante pelo Simples Nacional,**
**mas que tiver ultrapassado o sublimite de receita bruta fixado pelo estado/DF e**
**estiver impedido de recolher o ICMS/ISS por esse regime, conforme arts. 19 e 20 da**
**LC 123/06.**
**O código “3” será preenchido pelo contribuinte que não estiver na situação 1 ou 2.**

**Informar o CRT = “1” (Simples Nacional) e no campo “Situação Tributária” = o**
**CSOSN correspondente a operação, na sub-aba “ICMS” da aba “Tributos” do**
**Aplicativo Emissor da NF-e.**
**CRT = “2 e 3” (Operações fora Simples Nacional) informar CST.**

**TABELA B - Código de Situação da Operação no Simples Nacional – CSOSN**
101 – Tributada pelo Simples Nacional com permissão de crédito;

102 – Tributada pelo Simples Nacional sem permissão de crédito;

103 – Isenção do ICMS no Simples Nacional para faixa de receita bruta;

201 – Tributada pelo Simples Nacional com permissão de crédito e com cobrança do ICMS por
substituição tributária;

202 – Tributada pelo Simples Nacional sem permissão de crédito e com cobrança do ICMS por
substituição tributária;

203 – Isenção do ICMS no Simples Nacional para faixa de receita bruta e com cobrança do ICMS
por substituição tributária;

300 – Imune;

400 – Não tributada pelo Simples Nacional;

500 – ICMS cobrado anteriormente por substituição tributária (substituído) ou por antecipação;

900 – Outros.

**OBS: Na emissão de Nota Fiscal Eletrônica (NF-e), modelo 55, a base de cálculo e o ICMS**
**porventura devido serão indicados nos campos próprios, conforme estabelecido no Manual**

_________________________________________________________________________________________

**Pág. 21 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

**de Orientação do Contribuinte da NF-e, nos termos do Ajuste SINIEF que instituiu o referido**
**documento eletrônico (art. 57 § 7º da Resolução CGSN nº 94/11).**

### 3.1) Operações normais

**3.1.1) Emissão de NF-e em operação tributada pelo Simples Nacional e com permissão de**
**crédito de ICMS (art. 58 da Resolução CGSN nº 94/2011):**

**O código “101” será utilizado nos casos em que a operação incida tributação do ICMS no regime**
Simples Nacional, quando for permitido ao remetente emitir Nota Fiscal com direito ao crédito do
ICMS, conforme estabelecido no art. 58  da Resolução do CGSN nº 94/11.

**3.1.1.1) Informar o código “101” (“Tributada pelo Simples Nacional com permissão de crédito”) no**
campo CSOSN.

Exemplo de XML:

**<ICMSSN101>  Informar:**

**<orig>?</orig>  Origem (orig) da mercadoria: 0**
(Nacional) ou 1 (Estrangeira –
**<CSOSN>101</CSOSN>**
Importação Direta) ou 2 (Estrangeira
**– Adquirida no Mercado Interno);**
**<pCredSN>?</pCredSN>**
**CSOSN (CSOSN): 101 (Tributada**
**<vCredICMSSN>?</vCredICMSSN>**
pelo Simples Nacional com permissão
de crédito);
**<ICMSSN101>**
***Alíquota (pCredSN) percentual**
**aplicável no cálculo do crédito;**

- Crédito (vCredICMSSN) valor do
ICMS que pode ser aproveitado:

_________________________________________________________________________________________

**Pág. 22 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

**3.1.1.2) A ME ou EPP optante pelo Simples Nacional emitirá nota fiscal com direito ao crédito**
estabelecido no § 1º do art. 23 da Lei Complementar nº 123, de 2006, desde que as mercadorias
sejam destinadas à comercialização ou industrialização, consignará no campo informações
complementares a expressão (art. 58 da Resolução CGSN nº 94/11):

"DOCUMENTO EMITIDO POR ME OU EPP OPTANTE PELO SIMPLES NACIONAL";

“NÃO GERA DIREITO A CRÉDITO FISCAL DE IPI.”

"PERMITE O APROVEITAMENTO DO *CRÉDITO DE ICMS NO VALOR DE R$......;
CORRESPONDENTE À *ALÍQUOTA DE...%, NOS TERMOS DO ART. 23 DA LEI COMPLEMENTAR
Nº 123, DE 2006".

**OBS: Percentual* - percentual da alíquota utilizado para cálculo do ICMS no DAS do mês**
**anterior.**

**3.1.2) Emissão de NF-e em operação tributada pelo Simples Nacional e sem permissão de**
**crédito de ICMS (art. 59, da Resolução CGSN nº 94/2011):**

**3.1.2.1) Informar o código “102” (“Tributada pelo Simples Nacional sem permissão de crédito”) no**
campo CSOSN.

**O código “102” refere-se às operações tributadas pelo ICMS no Simples Nacional, quando não for**
permitido ao remetente emitir Nota Fiscal com direito ao crédito do ICMS (art. 59, incisos I,II e V da
Resolução do CGSN nº 94/11).

Exemplos de não concessão de crédito pelo remetente nesse código:

- estiver sujeita à tributação do ICMS no Simples Nacional por valores fixos mensais;

- tratar-se de operação de venda ou revenda de mercadorias em que o ICMS não é devido na forma
do Simples Nacional;
_________________________________________________________________________________________

**Pág. 23 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

- considerar, por opção, que a base de cálculo do Simples Nacional será representada pela receita
recebida no mês (Regime de Caixa);

Exemplo de XML:

**<ICMSSN102>  Informar:**

**<orig>?</orig>  * Origem (orig) da mercadoria: 0**
(Nacional) ou 1 (Estrangeira –Importação
**<CSOSN>102</CSOSN>**
Direta) ou 2 (Estrangeira – Adquirida no
**Mercado Interno);**
**<ICMSSN102>**
- CSOSN (CSOSN): 102 – Tributada pelo
Simples Nacional sem permissão de
**crédito.**

A ME ou EPP optante pelo Simples Nacional não poderá consignar no documento fiscal a expressão
*mencionada no caput do art. 58 da Resolução, CGSN nº 94/11 (art. 59 da Resolução CGSN nº*
94/11).

**3.1.2.2) Indicar, no campo de Informações Complementares da Nota Fiscal, as expressões:**

“DOCUMENTO EMITIDO POR ME OU EPP OPTANTE PELO SIMPLES NACIONAL";

“NÃO GERA DIREITO A CRÉDITO FISCAL DE IPI.”;

**3.1.3) Emissão de NF-e em operação com isenção concedida pelo Estado ou Distrito Federal (**
**art. 31, inciso I da Resolução do CGSN nº 94/11):**

**3.1.3.1) Informar o código “103” (“Isenção do ICMS no Simples Nacional para faixa de receita bruta”)**
no campo CSOSN.

**O código “103” refere-se às operações isentas do ICMS no Simples Nacional,  sobre a parcela das**
receitas brutas sujeitas a isenção onde serão desconsiderados os percentuais do ICMS,

_________________________________________________________________________________________

**Pág. 24 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

consequentemente o remetente não poderá conceder o crédito do ICMS (art. 35, inciso I  c/c art. 59,
inciso III da Resolução do CGSN nº 94/11).

Exemplo de XML:

**<ICMSSN103>  Informar:**

**<orig>?</orig>  Origem (orig) da mercadoria: 0**
(Nacional) ou 1 (Estrangeira –Importação
**<CSOSN>103</CSOSN>**
Direta) ou 2 (Estrangeira – Adquirida no
**Mercado Interno);**
**<ICMSSN103>**
**CSOSN (CSOSN): 103 – Isenção do**
ICMS no Simples Nacional para faixa de
**receita bruta.**

**3.1.3.2) Indicar, no campo de Informações Complementares da Nota Fiscal as expressões:**

**“DOCUMENTO EMITIDO POR ME OU EPP OPTANTE PELO SIMPLES NACIONAL";**

**“NÃO GERA DIREITO A CRÉDITO FISCAL DE IPI.”;**

### 3.2) Operações com substituição tributária

- Na hipótese de a ME ou EPP optante pelo Simples Nacional se encontrar na condição de substituta
tributária (art. 28 da Resolução do CGSN nº 94/11):

*Art. 28 da Resolução CGSN nº 94/11.*

*(...)*

***“§ 1º Na hipótese do caput, a ME ou EPP optante pelo Simples Nacional deverá recolher a parcela***
*dos tributos devidos por responsabilidade tributária diretamente ao ente detentor da respectiva*
*competência tributária.*

_________________________________________________________________________________________

**Pág. 25 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

*§ 2º Em relação ao ICMS, no que tange ao disposto no § 1º, o valor do imposto devido por*
*substituição tributária corresponderá à diferença entre:*

*I - o valor resultante da aplicação da alíquota interna do ente a que se refere o § 1º sobre o preço*
*máximo de venda a varejo fixado pela autoridade competente ou sugerido pelo fabricante, ou sobre o*
*preço a consumidor usualmente praticado; e*

*II - o valor resultante da aplicação da alíquota interna ou interestadual sobre o valor da operação ou*
*prestação própria do substituto tributário.”*

- A diferença entre a alíquota interna e a interestadual do ICMS será calculada tomando-se por base
**as alíquotas aplicáveis às pessoas jurídicas não optantes pelo Simples Nacional. (Lei Complementar**
nº 123, de 2006, art. 13, § 5º)

- Quando a ME ou EPP revestir-se da condição de responsável, inclusive de substituto tributário,
fará a indicação alusiva à base de cálculo e ao imposto retido no campo próprio (Art. 57 § 4º da
Resolução 94/11).

- Cálculo da ST - Aplicar a MVA Original no cálculo da Substituição Tributária para os
optantes pelo Simples Nacional.

A partir de 01/06/11, nas operações interestaduais com mercadorias sujeitas à substituição
tributária, quando remetidas por contribuinte optante pelo Simples Nacional, para obtenção
da base de cálculo da substituição tributária será aplicada, em vez da “MVA ajustada”, a
“MVA ST original”, estabelecida em Convênio e Protocolo, ou a MVA para as operações
internas, prevista na legislação deste Estado (Convênio ICMS 35/11).

Tabela para aplicação da “MVA original” sendo o remetente optante pelo Simples Nacional

ACORDO OPERAÇÃO MVA
REMETENTE DESTINATÁRIO
INTERESTADUAL INTERESTADUAL UTILIZADA

SIMPLES
SIM – CONV. OU PROT. NORMAL SIM ORIGINAL
NACIONAL

SIMPLES SIMPLES
SIM – CONV. OU PROT. SIM ORIGINAL
NACIONAL NACIONAL

_________________________________________________________________________________________

**Pág. 26 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

SIM – CONV. OU PROT. NORMAL     NORMAL SIM AJUSTADA

SIMPLES
SIM – CONV. OU PROT. NORMAL SIM AJUSTADA
NACIONAL

SIM
SIMPLES
SEM ACORDO NORMAL ORIGINAL
NACIONAL

SIMPLES SIMPLES
SEM ACORDO SIM ORIGINAL
NACIONAL NACIONAL

SEM ACORDO NORMAL NORMAL SIM AJUSTADA

SIMPLES
SEM ACORDO NORMAL SIM AJUSTADA
NACIONAL

**3.2.1) Emissão de NF-e em operação com substituição tributária, pelo contribuinte substituto,**
**tributada pelo Simples Nacional e com permissão de crédito de ICMS(art. 57, § 4º, da**
**Resolução CGSN nº 94/2011).**

**O código “201” poderá ser utilizado na operação com mercadoria sujeita à Substituição Tributária,**
tributada pelo Simples Nacional, e a legislação do Estado ou DF exigir a cobrança do ICMS do
substituto tributário.

**3.2.1.1) Informar o código “201” (“Tributada pelo Simples Nacional com permissão de crédito e com**
cobrança do ICMS por substituição tributária”) no campo CSOSN.

Exemplo de XML:

**<ICMSSN201>  Informar:**

**<orig>?</orig> Origem (orig) da mercadoria: 0**
(Nacional) ou 1 (Estrangeira –
**<CSOSN>201</CSOSN>**
Importação Direta) ou 2 (Estrangeira
**– Adquirida no Mercado Interno);**
**<pCredSN>?</pCredSN>**
**CSOSN (CSOSN): 201 – Tributada**

_________________________________________________________________________________________

**Pág. 27 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

**<vCredICMSSN>?</vCredICMSSN> pelo Simples Nacional com permissão**
de crédito e com cobrança do ICMS
**<modBCST>?</modBCST>**
por substituição tributária
**<vBCST>?</vBCST>**
**Alíquota (pCredSN) *percentual**
**<pICMSST>?</pICMSST>**
**aplicável no cálculo do crédito do SN;**
**<vICMSST>?</vICMSST>**
- Crédito (vCredICMSSN) do ICMS
**<ICMSSN201> do SN que pode ser aproveitado.**

Modalidade de BC ICMS ST
(modBCST): informar uma das
seguintes modalidades de Base de
**cálculo do ICMS ST = 0 (Preço**
**tabelado ou máximo sugerido) ou 1**
**(Lista Negativa) ou 2 (Lista**
**Positiva) ou 3 (Lista Neutra) ou 4**
**(Margem Valor Agregado) ou 5**
**(Pauta);**

- Base de Cálculo do ICMS ST
(vBCST): informar a BC do ICMS ST;

- Alíquota do ICMS ST (pICMSST):
informar a alíquota do ICMS interna
do ente destinatário.

- ICMS ST (vICMSST):
**corresponderá à diferença entre: o
valor resultante da aplicação da
alíquota interna do ente sobre a BC
da ST e o valor resultante da
aplicação da alíquota interna ou
interestadual sobre o valor da
operação ou prestação própria do
substituto tributário;

Obs.: Em algumas operações serão
exigidas também:

Percentual da margem de

valor Adicionado do ICMS ST

_________________________________________________________________________________________

**Pág. 28 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

Percentual da Redução de BC

**do ICMS ST.**

**3.2.1.2) Indicar, no campo de Informações Complementares, da Nota Fiscal as expressões:**

**"DOCUMENTO EMITIDO POR ME OU EPP OPTANTE PELO SIMPLES NACIONAL";**

**“NÃO GERA DIREITO A CRÉDITO FISCAL DE IPI.”**

**"PERMITE O APROVEITAMENTO DO *CRÉDITO DE ICMS NO VALOR DE R$......;**
**CORRESPONDENTE À *ALÍQUOTA DE...%, NOS TERMOS DO ART. 23 DA LEI**
**COMPLEMENTAR Nº 123, DE 2006".**

**3.2.1.3) - Devem ser indicados, nos respectivos campos, o valor do ICMS utilizado no cálculo e o**
*percentual da alíquota utilizado para cálculo do ICMS no DAS do mês anterior.

- *Para o cálculo da substituição tributária poderá ser utilizado a diferença entre a alíquota interna e a
interestadual do ICMS, tomando-se por base as alíquotas aplicáveis às pessoas jurídicas não
**optantes pelo Simples Nacional. (Lei Complementar nº 123, de 2006, art. 13, § 5º).**

**3.2.2) Emissão de NF-e em operação sujeita a substituição tributária,  por contribuinte**
**substituto, tributada pelo Simples Nacional e sem permissão de crédito de ICMS (art. 57, § 4º,**
**da Resolução CGSN nº 94/2011):**

**O código “202” será utilizado na operação com mercadoria sujeita à Substituição Tributária, pelo**
contribuinte substituto, tributada pelo Simples Nacional, nas hipóteses em que o remetente não
possa conceder o crédito do ICMS.

**3.2.2.1) Informar o código “202” (“Tributada pelo Simples Nacional sem permissão de crédito e com**
cobrança do ICMS por substituição tributária”) no campo CSOSN.

_________________________________________________________________________________________

**Pág. 29 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

Exemplo de XML:

**<ICMSSN202>  Informar:**

**<orig>?</orig> Origem (orig) da mercadoria: 0**
(Nacional) ou 1 (Estrangeira –Importação
**<CSOSN>202</CSOSN>**
Direta) ou 2 (Estrangeira – Adquirida no
**Mercado Interno);**
**<modBCST>?</modBCST>**
**<vBCST>?</vBCST>  CSOSN (CSOSN): 202 – Tributada pelo**
Simples Nacional sem permissão de
**<pICMSST>?</pICMSST>**
crédito e com cobrança do ICMS por
**<vICMSST>?</vICMSST>**
substituição tributária

<ICMSSN202>
Modalidade de BC ICMS ST
(modBCST): informar uma das seguintes
modalidades de Base de cálculo do ICMS
**ST = 0 (Preço tabelado ou máximo**
**sugerido) ou 1 (Lista Negativa) ou 2**
**(Lista Positiva) ou 3 (Lista Neutra) ou 4**
**(Margem Valor Agregado) ou 5 (Pauta);**

Base de Cálculo do ICMS ST (vBCST):
informar a BC do ICMS ST;

Alíquota do ICMS ST (pICMSST):
informar a alíquota do ICMS interna do
ente destinatário.

**ICMS ST (vICMSST): corresponderá à
diferença entre: o valor resultante da
aplicação da alíquota interna do ente
sobre a BC da ST e o valor resultante da
aplicação da alíquota interna ou
interestadual sobre o valor da operação
ou prestação própria do substituto
tributário;

Obs.: Em algumas operações serão
exigidas também:

Percentual da margem de

_________________________________________________________________________________________

**Pág. 30 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

valor Adicionado do ICMS ST

Percentual da Redução de BC

do ICMS ST.

**3.2.2.2) Indicar, no campo de Informações Complementares, as expressões:**

**"DOCUMENTO EMITIDO POR ME OU EPP OPTANTE PELO SIMPLES NACIONAL";**

**“NÃO GERA DIREITO A CRÉDITO FISCAL DE IPI.”**

- *Para o cálculo da substituição tributária poderá ser utilizado à diferença entre a alíquota interna e a
interestadual do ICMS, tomando-se por base as alíquotas aplicáveis às pessoas jurídicas não
**optantes pelo Simples Nacional. (Lei Complementar nº 123, de 2006, art. 13, § 5º).**

**3.2.3) Emissão de NF-e em operação sujeita a substituição tributária,  por contribuinte**
**substituto tributário, com isenção do ICMS estabelecida pelo Estado ou Distrito Federal a que**
**a ME ou EPP esteja sujeita no mês da operação (art. 57, § 4º, c/c art. 35, I da Resolução CGSN**
**nº 94/2011 c/c ):**

**O código “203” será utilizado na operação com mercadoria sujeita à Substituição Tributária, pelo**
contribuinte substituto tributário, com isenção do ICMS estabelecida pelo Estado ou DF,
consequentemente o remetente não poderá conceder o crédito do ICMS.

**3.2.3.1) Informar o código “203” (“Isenção do ICMS no Simples Nacional para faixa de receita bruta e**
com cobrança do ICMS por substituição tributária”) no campo CSOSN.

Exemplo de XML:

**<ICMSSN203>  Informar:**

**<orig>?</orig> Origem (orig) da mercadoria: 0**
(Nacional) ou 1 (Estrangeira –Importação
**<CSOSN>203</CSOSN>**
Direta) ou 2 (Estrangeira – Adquirida no
**Mercado Interno);**
**<modBCST>?</modBCST>**

_________________________________________________________________________________________

**Pág. 31 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

**<vBCST>?</vBCST>  CSOSN (CSOSN): 203 – Isenção do**
ICMS no Simples Nacional para faixa de
**<pICMSST>?</pICMSST>**
receita bruta e com cobrança do ICMS
**<vICMSST>?</vICMSST>**
por substituição tributária

<ICMSSN203>
Modalidade de BC ICMS ST
(modBCST): informar uma das seguintes
modalidades de Base de cálculo do ICMS
**ST = 0 (Preço tabelado ou máximo**

**sugerido) ou 1 (Lista Negativa) ou 2**
**(Lista Positiva) ou 3 (Lista Neutra) ou 4**
**(Margem Valor Agregado) ou 5 (Pauta);**

Base de Cálculo do ICMS ST (vBCST):
informar a BC do ICMS ST;

Alíquota do ICMS ST (pICMSST):
informar a alíquota do ICMS interna do
ente destinatário.

**ICMS ST (vICMSST): corresponderá à
diferença entre: o valor resultante da
aplicação da alíquota interna do ente
sobre a BC da ST e o valor resultante da
aplicação da alíquota interna ou
interestadual sobre o valor da operação
ou prestação própria do substituto
tributário;

Obs.: Em algumas operações serão
exigidas também:

- Percentual da margem de

valor Adicionado do ICMS ST

- Percentual da Redução de BC

do ICMS ST.

**3.2.3.2) Indicar, no campo de Informações Complementares, as expressões:**

_________________________________________________________________________________________

**Pág. 32 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

**"DOCUMENTO EMITIDO POR ME OU EPP OPTANTE PELO SIMPLES NACIONAL";**

**“NÃO GERA DIREITO A CRÉDITO FISCAL DE IPI.”**

- *Para o cálculo da substituição tributária poderá ser utilizado à diferença entre a alíquota interna e a
interestadual do ICMS, tomando-se por base as alíquotas aplicáveis às pessoas jurídicas não
**optantes pelo Simples Nacional. (Lei Complementar nº 123, de 2006, art. 13, § 5º).**

**3.2.4) Emissão de NF-e em operação sujeita a substituição tributária,  por contribuinte**
**substituído ou nas operações em que o imposto já tenha sido retido anteriormente.**

**O código “500” será utilizado na operação em que o contribuinte remetente, esteja na condição de**
substituído tributário, tendo sido o ICMS recolhido anteriormente, por substituição tributária ou por
antecipação com encerramento de fase, sendo segregada da receita bruta de revenda de mercadoria
do Simples Nacional, desconsiderando-se os percentuais do ICMS.

**3.2.4.1) Informar o código “500” (“ICMS cobrado anteriormente por substituição tributária (substituído**
ou por antecipação”) no campo CSOSN.

Exemplo de XML:

**<ICMSSN500>  Informar:**

**<orig>?</orig> * Origem (orig) da mercadoria: 0**
(Nacional) ou 1 (Estrangeira –Importação
**<CSOSN>500</CSOSN>**
Direta) ou 2 (Estrangeira – Adquirida no
**Mercado Interno);**
**<vBCSTRet>?</vBCSTRet>**
**<vICMSSTRet>?</vICMSSTRet>**
- CSOSN (CSOSN): 500 – ICMS cobrado
anteriormente por substituição tributária
<ICMSSN500>
(substituído) ou por antecipação, alguns
Estados exigem essas informações:

- Base de Cálculo do ICMS ST
(vBCSTRet): informar a BC do ICMS ST
retido;

_________________________________________________________________________________________

**Pág. 33 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

- ICMS ST (vICMSST): informar o valor
**do ICMS ST retido.**

**3.2.4.2) Indicar, no campo de Informações Complementares da Nota Fiscal, as expressões:**

**"DOCUMENTO EMITIDO POR ME OU EPP OPTANTE PELO SIMPLES NACIONAL";**

**“NÃO GERA DIREITO A CRÉDITO FISCAL DE IPI.”**

OBS: Na hipótese de a ME ou EPP optante pelo Simples Nacional se encontrar na condição de
substituída tributária (art. 29 da Resolução do CGSN nº 94/11):

Art. 29, Resolução CGSN nº 94/11.

(...)

*“Na hipótese de a ME ou EPP optante pelo Simples Nacional se encontrar na condição de*
*substituída tributária, as receitas decorrentes: (Lei Complementar nº 123, de 2006, art. 2º, inciso I e §*
*6º; art. 18, §§ 4º, inciso IV, 12, 13 e 14)*

*I - da revenda de mercadorias sujeitas à substituição tributária deverão ser segregadas na forma da*
*alínea "b" do inciso I do art. 25.”*

**3.3) Operações não tributadas**

**3.3.1) Emissão de NF-e em operação imune:**

**O código “300” refere-se a operações imunes de tributação pelo ICMS, no Simples Nacional, tais**
como operações com livros, jornais, periódicos e o papel destinado à sua impressão e operações
*destinadas ao exterior (exportações), inclusive por meio de trade company (art. 30 da Resolução*
CGSN nº 94/11).

_________________________________________________________________________________________

**Pág. 34 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

**3.3.1.1) Informar o código “300” (“Imune”) no campo CSOSN.**

Exemplo de XML:

**<ICMSSN300>  Informar:**

**<orig>?</orig>  Origem (orig) da mercadoria: 0**
(Nacional) ou 1 (Estrangeira –Importação
**<CSOSN>300</CSOSN>**
Direta) ou 2 (Estrangeira – Adquirida no
**Mercado Interno);**
**<ICMSSN300>**
**CSOSN (CSOSN): 300 – Imune.**

**3.3.1.2) Indicar, no campo de Informações Complementares da Nota Fiscal, as expressões:**

**“DOCUMENTO EMITIDO POR ME OU EPP OPTANTE PELO SIMPLES NACIONAL";**

**“NÃO GERA DIREITO A CRÉDITO FISCAL DE IPI.”;**

*Art. 59 da Resolução CGSN nº 94/11.*

*(...)*

*A ME ou EPP optante pelo Simples Nacional não poderá consignar no documento fiscal a expressão*
*mencionada no caput do art. 58, ou caso já consignada, deverá inutilizá-la, quando: (Lei*
*Complementar nº 123, de 2006, art. 23, §§ 1º, 2º e 4º; art. 26, inciso I e § 4º)*

*(...)*

*IV - a operação for imune ao ICMS;*

_________________________________________________________________________________________

**Pág. 35 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

**3.3.2) Emissão de NF-e em operação não tributada pelo Simples Nacional:**

**O código “400” refere-se a quaisquer operações realizadas que não gerem receita bruta nos termos**
da LC 123/06, consequentemente, não serão tributadas no Simples Nacional.

Alguns exemplos:

- operações de remessa de um modo geral (remessa para industrialização por encomenda, remessa
para utilização em prestação de serviço, remessa para locação, remessa para beneficiamento,
remessa em comodato, remessa em demonstração, remessa para conserto);

- operações realizadas a título gratuito (amostras, bonificações, doações, brindes);

- operações de transferência de mercadorias entre matriz e filial mesmo que entre Unidades da
Federação distintas;

- operações de transferência de propriedade (onde exista o sucessor e o sucedido).

**3.3.2.1) Informar o código “400” (“Não tributada pelo Simples Nacional”) no campo CSOSN.**

Exemplo de XML:

**<ICMSSN400>  Informar:**

**<orig>?</orig>  Origem (orig) da mercadoria: 0**
(Nacional) ou 1 (Estrangeira –Importação
**<CSOSN>400</CSOSN>**
Direta) ou 2 (Estrangeira – Adquirida no
**Mercado Interno);**
**<ICMSSN400>**
**CSOSN (CSOSN): 400 – Não tributada**
**pelo Simples Nacional.**

_________________________________________________________________________________________

**Pág. 36 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

**3.3.2.2) Indicar, no campo de Informações Complementares da Nota Fiscal, as expressões:**

**“DOCUMENTO EMITIDO POR ME OU EPP OPTANTE PELO SIMPLES NACIONAL";**

**“NÃO GERA DIREITO A CRÉDITO FISCAL DE IPI.”;**

**3.3.3) Emissão de NF-e na situação de outras operações ou prestações:**

**O código “900” será utilizado nos casos que não se enquadrem nos códigos anteriores.**

Alguns exemplos:

- Importações de mercadorias, NF-e (Entrada) em que o ICMS é pago por fora do regime Simples
Nacional;

- Demais hipóteses de emissão de NF-e (Entrada) pelo contribuinte optante pelo Simples Nacional,
na condição de destinatário da operação, não se enquadrando esta operação nos demais códigos;

- Devolução de mercadorias para contribuinte não optante pelo Simples Nacional;

**3.3.3.1) Informar o código “900” (“outros”) no campo CSOSN.**

Exemplo de XML:

_________________________________________________________________________________________

**Pág. 37 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

**<CSOSN>900</CSOSN>  Informar:**
**<modBC>?</modBC>  Origem (orig) da mercadoria: 0 (Nacional) ou 1**
(Estrangeira –Importação Direta) ou 2
<vBC>?</vBC>
**(Estrangeira – Adquirida no Mercado Interno);**
<pRedBC>?</pRedBC>
**CSOSN (CSOSN): 900 – Outros;**
<pICMS>?</pICMS>
**Obs.1: Nesse código a emissão da NF-e**
<vICMS>?</vICMS>
obedecerá a legislação de cada ente.
<modBCST>?</modBCST>
**Obs.2: Em algumas operações serão exigidas**
<pMVAST>?</pMVAST>
também:
<pRedBCST>?</pRedBCST>
***2.1)No cálculo do ICMS no Simples**
<vBCST>?</vBCST>
**Nacional, o preenchimento dos campos:**
<pICMSST>?</pICMSST>
**Alíquota: pCredSN> Alíquota aplicável de**
<vICMSST>?</vICMSST>
cálculo do crédito (SIMPLES NACIONAL);
<pCredSN>?</pCredSN>
**Crédito: vCredICMSSN>Valor crédito do**
<vCredICMSSN>?</vCredICMSSN>
ICMS que pode ser aproveitado nos termos do
</ICMSSN900> art. 23 da LC 123 (SIMPLES NACIONAL).
****2.2) No cálculo do ICMS Normal, a**
**exemplo de Devoluções e importações,**
**preenchimento dos campos próprios da NF-**
**e:**
modBC> Modalidade de determinação   da BC
do ICMS;
vBC> BC do ICMS;
pRedBC> Percentual da Redução  de BC, se
for o caso;
pICMS> Alíquota do imposto;
vICMS> Valor do ICMS.
****  2.3) No cálculo do ICMS ST,  nas**
**hipóteses de importação de mercadorias do**
**exterior sujeitas a ST,  preenchimento dos**
**campos próprios da NF-e:**
<modBCST> Modalidade de determinação da
BC do ICMS ST;
<pMVAST> Percentual da margem de valor
Adicionado do ICMS ST;
<pRedBCST> Percentual da Redução de BC
do ICMS ST, se for o caso;
<vBCST> Valor da BC do ICMS ST;
<pICMSST> Alíquota do imposto do ICMS
ST;
**<vICMSST> Valor do ICMS ST.**

***3.3.3.2) Indicar, no campo de Informações Complementares, as expressões:**

**"DOCUMENTO EMITIDO POR ME OU EPP OPTANTE PELO SIMPLES NACIONAL";**

_________________________________________________________________________________________

**Pág. 38 / 39**

---

**Nota Fiscal Eletrônica**

**Orientação de Preenchimento da NF-e - versão 2.02 (leiaute NF-e 3.10) –  04/02/2015**

**“NÃO GERA DIREITO A CRÉDITO FISCAL DE IPI.”**

**"PERMITE O APROVEITAMENTO DO *CRÉDITO DE ICMS NO VALOR DE R$......;**
**CORRESPONDENTE À *ALÍQUOTA DE...%, NOS TERMOS DO ART. 23 DA LEI**
**COMPLEMENTAR Nº 123, DE 2006".**

**** Na hipótese de emissão de Nota Fiscal de devolução de compra e ou de NF de entrada de**
**mercadoria, através de Nota Fiscal Eletrônica (NF-e), modelo 55, não se aplicará o disposto**
**nos §§ 5º e 6º do art. 57 da Resolução CGSN nº 94/11, devendo a base de cálculo e o ICMS,**
**porventura devidos serem indicados nos campos próprios, conforme estabelecido em manual**
**de especificações e critérios técnicos da NF-e, baixado nos termos do Ajuste SINIEF que**
**instituiu o referido documento eletrônico (art.57 § 7º da Resolução CGSN nº 94/11).**

**3.4) Operações tributadas fora do Simples Nacional**

**Informar o CRT = “2” - O código 2 será preenchido pelo contribuinte optante pelo**
**Simples Nacional que tiver ultrapassado o sublimite de receita bruta fixado pelo**
**Estado ou DF e estiver impedido de recolher o ICMS/ISS por esse regime, conforme**
**arts. 19 e 20 da LC 123/06.**

**3.4.1)  Emissão de NF-e por estabelecimento impedido de recolher o ICMS por ultrapassagem do**
**sub-limite estadual de receita bruta (art. 57, § 3º, da Resolução CGSN nº 94/2011):**

**3.4.1.1) Os campos da NF-e deverão ser preenchidos como se o emitente não fosse optante pelo**
Simples Nacional, isto é, com os CST aplicáveis à operação (00, 10, 20, 30, 40, 41, 50, 51, 60, 70 ou
90, conforme o caso) e o preenchimento dos demais campos pertinentes;

**3.4.1.2) Indicar, no campo de Informações Complementares, as expressões:**

**“DOCUMENTO EMITIDO POR ME OU EPP OPTANTE PELO SIMPLES NACIONAL";**

**"ESTABELECIMENTO IMPEDIDO DE RECOLHER O ICMS/ISS PELO SIMPLES NACIONAL, NOS**
**TERMOS DO § 1º DO ART. 20 DA LC 123/2006";**

**"NÃO GERA DIREITO A CRÉDITO FISCAL DE IPI".**

_________________________________________________________________________________________

**Pág. 39 / 39**
