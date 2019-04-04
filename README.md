# Importar e Exportar Produtos por CSV
[tradução da página oficial do Woocommerce](https://docs.woocommerce.com/document/product-csv-importer-exporter/)

Para importar novos produtos ou atualizar os existentes, é necessário um arquivo CSV que contenham as seguintes informações do produto:

Campo | Exemplo de Uso | Descrição
----- | -------------- | ---------
id | 1 | Ao definir o ID na planilha de importação, se houver um produto com esse mesmo ID, ele será atualizado. Para casos de produtos novos, não é necessário informar o ID
type | simple, variation, virtual | Tipo do produto. Tipos válidos: `simple`, `variable`, `grouped`, `external`, `variation`, `virtual`, `downloadable`.
sku | produto-001 | Utilizado como código de controle do lojista
name | Produto de Exemplo | Atributo que define o nome do produto
status | 1 | `1` para publicado, `0` para privado, `-1` para rascunho
featured | 1 | `1`, ou `0`
catalog_visibility | visible | Visibilidade no catálogo; Valores possíveis: `visible`, `catalog`, `search`, `hidden`
short_description | Descrição do produto | Atributo utilizado para definir a descrição curta do produto
description | Descrição do produto longa | Atributo utilizado para definir a descrição longa do produto
date_on_sale_from | 2013-06-07 10:53:15 | À venda à partir da data; pode ser definido, ou deixado em branco
date_on_sale_to | 2013-06-07 10:53:15 | À venda até; pode ser definido, ou deixado em branco
tax_status | taxable | Atributo para definir se o produto é taxável; Valores possíveis: `taxable`, `shipping`, `none`
tax_class | standard | Pode utilizar qualquer classe de taxa (classe deve ser definida no painel antes)
stock_status | 1 | Disponível em estoque? Valores possíveis:`1`, ou `0`
backorders | 1 | Pedido em espera; Valores possíveis: `0` para não; `1` para sim; ou `notify` para notificar
sold_individually | 1 | Vender individualmente?; `1` para sim; `0` para não
weight | 100 | Unidade de peso
length | 20 | Unidade de comprimento
width | 20 | Unidade de largura
height | 20 | Unidade de altura
reviews_allowed | 1 | Permitir avaliação dos clientes?; `1` para sim; `0` para não
purchase_note | Obrigado por comprar | Mensagem de agradecimento pela compra
price | 20.99 | Preço do produto com desconto
regular_price | 24.99 | Preço do produto sem desconto
manage_stock/stock_quantitiy | 20 | Quantidade de produtos em estoque
category_ids | Categoria 1 > Categoria 1.1, Categoria 2 | Categorias do produto (Sub categorias são indicados pelo símbolo `>`); Categorias devem ser previamente cadastradas
tag_ids | TagA, TagB | Tag dos produtos
shipping_class_id | Correios | Nome da classe de entrega
attributes | Color | Usado para variações de produtos
attributes | Blue, Red, Green | Lista de valores para o atributo anterior
default_attributes | Red | Valor padrão para o atributo
attributes | 1 | Visibilidade do atributo. `1` para sim; `0` para não
attributes | 1 | Mapeia o atributo como Global, ou não. `1` para sim; `0` para não
image_id / gallery_image_ids | http://somewhere.com/image.jpg, http://somewhere.com/image2.jpg | Lista de imagens do produto; A primeira será a padrão
downloads | Arquivo 1 | Nome do arquivo
downloads | url.zip | URL para download do arquivo
download_limit | 1 | `n/a`, ou o limite de downloads permitidos
download_expiry | 1 | `n/a`, ou a quantidade de dias para expiração do download
parent_id | produto-001 | SKU do produto pai; Utilizado para produtos variáveis
upsell_ids | produto-001, produto-002 | Produtos recomendados (upsell)
cross_sell_ids | produto-003, produto-004 | Produtos recomendados (cross sell)
menu_order | 1 | Ordem no menu

### Pré-requisitos para criação do arquivo
* CSV deve ser no formato UTF-8;
* Todas as datas devem ser definidas no fuso-horário local;
* Múltiplos valores devem ser separados por vírgula;
* Imagens devem ser previamente carregadas, pois sua definição se dá pela indicação da URL.

> [Clique aqui para baixar um exemplo da planilha de importação](./docs/importacao_produtos.csv)

## Processo de Importação

1. Vá para **Woocommerce > Produtos**
2. Selecione **Importar** no topo da página; Será aberta a tela de upload
3. Clique em **Selecionar o arquivo** e escolha o CSV de importação
4. Selecione a opção **Atualizar produtos existentes**
5. Clique em **Continue**
6. Será aberta a tela de mapeamento dos atributos; Faça o mapeamento
7. Clique em **Executar Importação**



##### Referências
* [Exportação e Importação de Produtos](https://docs.woocommerce.com/document/product-csv-importer-exporter/)
* [Esquema de Dados](https://github.com/woocommerce/woocommerce/wiki/Product-CSV-Import-Schema#csv-columns-and-formatting)