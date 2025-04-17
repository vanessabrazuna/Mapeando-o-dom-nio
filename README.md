# 📦 Sistema de Gerenciamento de Estoque

Este sistema tem como objetivo gerenciar produtos em estoque, controlar vendas, emitir alertas de baixo estoque e automatizar ordens de compra com integração a fornecedores.

---

## 🧩 Entidades de Domínio

### Produto
- `id`: Identificador único
- `nome`
- `descrição`
- `tamanho`
- `cor`
- `quantidade_em_estoque`
- `quantidade_mínima`
- `preço_de_venda`
- `custo_de_aquisição`

### Estoque
- `produto_id`
- `quantidade_atual`
- `movimentações`: lista de entradas e saídas
- `data_da_movimentação`
- `tipo`: entrada | saída

### Venda
- `id`
- `produto_id`
- `quantidade`
- `data`
- `valor_total`
- `lucro`

### Alerta
- `id`
- `produto_id`
- `tipo_de_alerta`: (ex: baixo estoque)
- `data_do_alerta`
- `status`: pendente | lido

### Ordem de Compra
- `id`
- `produto_id`
- `quantidade`
- `data_de_criação`
- `status`: pendente | enviada | recebida

### Fornecedor
- `id`
- `nome`
- `produtos_fornecidos`
- `prazos_de_entrega`
- `contato`

---

## ⚙️ Casos de Uso (Funcionalidades)

- [ ] Cadastrar, editar e remover produtos
- [ ] Rastrear produto por ID com informações como tamanho e cor
- [ ] Definir quantidade mínima de estoque por produto
- [ ] Emitir alertas automáticos quando estoque atingir o mínimo
- [ ] Enviar alertas por e-mail e notificação no sistema
- [ ] Visualizar histórico de vendas com:
  - Filtro por período
  - Lucro por produto
  - Produtos mais vendidos
- [ ] Visualizar histórico de movimentações no estoque
  - Acompanhamento de tendências ao longo do tempo
- [ ] Criar e gerenciar ordens de compra (manual e automático)
- [ ] Integrar com fornecedores e receber atualizações de prazos de entrega


