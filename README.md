# VestiGestão — protótipo local

Sistema demonstrativo para loja de roupas com catálogo por cor e tamanho, estoque por SKU, etiquetas Code 39, PDV local e relatórios básicos.

## Executar

Na pasta do projeto:

```bash
python3 -m http.server 4173
```

Abra `http://localhost:4173`. Não há instalação de pacotes. Também é possível abrir `index.html` diretamente no navegador.

## Uso rápido

1. Em **Produtos**, cadastre nome, preço, cores e tamanhos; cada combinação recebe um SKU e um código de barras internos.
2. Em **Estoque**, use **Registrar movimentação** para lançar entradas e saídas por SKU com motivo.
3. Em **Etiquetas**, escolha uma variação, confira a prévia e imprima uma etiqueta de teste. Configure o leitor para Code 39.
4. Em **PDV / Caixa**, clique em uma peça ou digite/bipe o código e pressione Enter. Escolha o pagamento e registre a venda.

Os dados iniciais são fictícios. Os novos registros ficam no `localStorage` daquele navegador. Limpar os dados do navegador pode apagá-los; outras máquinas e caixas não compartilham a base. Não há emissão fiscal, pagamento integrado, autenticação ou sincronização.

## OpenSpec

`openspec/config.yaml` e `openspec/changes/improve-fashion-mvp/` documentam a proposta, os requisitos, o desenho e as tarefas da evolução atual. Para prosseguir com o fluxo oficial em um ambiente com a CLI instalada, execute `openspec status --change improve-fashion-mvp` e `openspec validate improve-fashion-mvp`; após revisar a implementação, arquive a mudança conforme o fluxo OpenSpec.
