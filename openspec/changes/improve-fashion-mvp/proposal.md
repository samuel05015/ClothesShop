# Melhorar o MVP de gestão de moda

## Por quê

O protótipo já organiza produtos por cor e tamanho, mas ainda comunica algumas capacidades que não executa: a barra de etiqueta é ilustrativa, o ajuste de estoque é um aviso, e o painel mostra uma comparação fictícia com ontem. Isso pode induzir o operador a confiar em números ou etiquetas incorretos.

## O que muda

- Organizar a navegação e os estados das telas com textos e ações mais claros para o trabalho diário.
- Produzir uma etiqueta com barras efetivamente codificadas a partir do código interno, adequada para impressão e leitura compatível.
- Registrar ajustes de estoque por variação, com motivo e histórico local.
- Impedir que o carrinho ultrapasse a quantidade disponível e preservar o pagamento selecionado ao adicionar itens.
- Remover indicadores fictícios do painel e distinguir dados de demonstração de dados reais.

## Impacto

Arquivos da interface estática (`index.html`, `styles.css`, `app.js`). Persistência local no navegador. Nenhuma alteração fiscal, integração de pagamento ou operação multiusuário.
