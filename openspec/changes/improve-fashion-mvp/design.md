# Desenho técnico

## Contexto

O projeto atual tem três arquivos, sem bundler. `app.js` renderiza as telas e persiste um objeto no `localStorage`. Manter esse formato evita introduzir dependências antes de haver backend ou equipe multiusuário.

## Decisões

1. Adicionar `movements` ao objeto persistido, com migração defensiva para quem já tem produtos e vendas no navegador.
2. Ajustar estoque por SKU identificado por produto e código; validar inteiro não nulo e saldo não negativo antes de salvar.
3. Gerar SVG Code 39 a partir de padrões locais para os caracteres usados nos códigos internos. A impressão usa somente a área da etiqueta selecionada.
4. Deixar claro que a persistência é local e que os registros iniciais são demonstração. Não sugerir caixa formalmente aberto quando não existe sessão de caixa.
5. Aplicar melhorias de foco, responsividade e hierarquia visual por CSS existente.

## Limites

`localStorage` não garante concorrência entre caixas, integridade transacional ou recuperação após limpeza do navegador. Um produto para operação real precisará de backend, banco de dados, autenticação, auditoria, emissão fiscal e integrações adequadas, tratados em outra mudança.
