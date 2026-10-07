# Etiquetas logísticas Dellamed

Ferramenta para gerar e imprimir as etiquetas logísticas (100 × 50 mm) dos produtos Dellamed: nome, SKU e código de barras (EAN-13 ou DUN-14).

## Arquivos

- `index.html`: a ferramenta.
- `produtos.json`: a base de produtos. **Para incluir, corrigir ou remover um produto, edite só este arquivo.**

## Como atualizar um produto

Cada produto no `produtos.json` tem este formato:

```json
{
 "grupo": "Cadeiras de Rodas",
 "sku": "05589",
 "nome": "CADEIRA DE RODAS D400 T40",
 "ean": "7898952570459",
 "dun": "",
 "medida_caixa": "82 × 29 × 77,5 cm",
 "qtd_master": "1",
 "medida_master": "82 × 29 × 77,5 cm"
}
```

- Mantenha os códigos entre aspas, para não perder zeros à esquerda.
- A ferramenta confere o dígito verificador do EAN e do DUN. Código errado aparece marcado e não vai para a etiqueta.
- Depois de salvar no GitHub, a mudança aparece no link em cerca de 1 minuto.

## Impressão

- **Imprimir na Zebra**: envia direto para a impressora. Requer o Zebra Browser Print instalado no computador.
- **Imprimir**: pelo navegador, com papel 100 × 50 mm, margens zero e escala 100%.
- **Exportar arquivo**: PDF, ZPL, Excel, CSV ou PNG.
