# Porsche Sales Dashboard

Dashboard interativa para o desafio da DIO, feita em um único arquivo HTML com CSS e JavaScript. Os gráficos usam a biblioteca Chart.js via CDN.

## Dashboard publicada

Depois de ativar o GitHub Pages, coloque aqui o endereço publicado: `https://SEU-USUARIO.github.io/porsche-sales-dashboard/`

## Perguntas de negócio

1. **Quais modelos geram mais receita?** Ajuda a identificar os modelos que mais contribuem para o faturamento.
2. **Quais cidades lideram em vendas?** Mostra onde há maior concentração de registros de vendas e pode orientar ações comerciais.
3. **Como os clientes pagam?** Compara os métodos de pagamento mais utilizados, apoiando a compreensão das preferências dos compradores.

Os indicadores de topo mostram receita total, quantidade de vendas e preço médio considerando os filtros aplicados.

## Filtros

- Modelo Porsche
- Cidade
- Ano do veículo
- Método de pagamento

O botão **Limpar filtros** restaura a visualização completa.

## Tratamento da base

- Foram utilizadas somente as colunas sanitizadas: `SaleDateSanitized`, `PorscheModelSanitized`, `ModelYearSanitized`, `SalesPriceSanitized`, `VehicleMileageSanitized`, `PayMethodSanitized`, `CitySanitized`, `StateSanitized` e `DeliveryStatusSanitized`.
- Preço e ano foram convertidos para valores numéricos.
- A data foi considerada válida somente quando pôde ser interpretada como data. Valores `INVALID` foram preservados como ausência de data válida; como esta versão não contém gráfico temporal, eles não afetam os gráficos.
- Campos pessoais e colunas cruas, como nome do cliente, identificador da venda e vendedor, foram excluídos do HTML incorporado.
- A base fornecida contém 100 registros. A dashboard mostra os valores encontrados nessa base e não representa dados atuais da Porsche.

## Prompt utilizado e refinamento

Prompt inicial utilizado para orientar a criação:

> Crie uma dashboard de vendas Porsche em um único arquivo HTML, com estilo premium escuro inspirado em preto, cinza e vermelho. Use somente os campos sanitizados da planilha. Inclua filtros funcionais por modelo, cidade, ano do veículo e método de pagamento. No topo, exiba receita total, quantidade de vendas e preço médio. Crie três visualizações para responder: quais modelos geram mais receita, quais cidades têm mais vendas e quais métodos de pagamento são mais usados. Use gráficos claros, responsivos, títulos em português e permita limpar todos os filtros. Não invente dados e não inclua nomes de clientes.

Refinamentos realizados na versão final:
- Mantive os gráficos limitados aos 8 principais modelos/cidades para melhorar a leitura.
- Fiz os indicadores e os três gráficos reagirem aos filtros.
- Adicionei um botão para limpar filtros e um aviso para combinações sem resultados.
- Excluí colunas pessoais e dados não sanitizados do arquivo HTML.

## Ferramentas

- HTML, CSS e JavaScript
- Chart.js via CDN
- ChatGPT para estruturar e gerar a primeira versão do código

## Como publicar no GitHub Pages

1. Crie um repositório público chamado `porsche-sales-dashboard` no GitHub.
2. Envie o arquivo `index.html` e este `README.md` para a raiz do repositório.
3. No repositório, abra **Settings → Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch**.
5. Selecione a branch `main` e a pasta `/(root)`, depois clique em **Save**.
6. Aguarde a publicação e abra o endereço exibido na própria página de configuração do Pages.
7. Substitua o endereço de exemplo no início deste README pelo link real.
8. Para submeter à DIO, envie o **link do repositório**, não somente o link da dashboard.

## Observações

A biblioteca Chart.js é carregada por CDN, portanto o navegador precisa de conexão com a internet para renderizar os gráficos. O restante da dashboard e os dados estão no próprio `index.html`.
