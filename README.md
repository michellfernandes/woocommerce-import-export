# Importar e Exportar Produtos por CSV ([tradução da página oficial do Woocommerce](https://docs.woocommerce.com/document/product-csv-importer-exporter/))

Para importar novos produtos ou atualizar os existentes, é necessário um arquivo CSV que contenham as seguintes informações do produto:

Campo | Exemplo de Uso | Descrição
----- | -------------- | ---------
id | 1 | Ao definir o ID na planilha de importação, se houver um produto com esse mesmo ID, ele será atualizado. Para casos de produtos novos, não é necessário informar o ID
type | simple, variation, virtual | Tipo do produto. Tipos válidos: simple, variable, grouped, external, variation, virtual, downloadable.
sku | produto-001 | Utilizado como código de controle do lojista
name | Produto de Exemplo | Atributo que define o nome do produto

