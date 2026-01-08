# ⚡ Guia de Referência Rápida - Support Issues

> Guia rápido para consulta durante a criação e gerenciamento de support issues.

---

## 🎯 Qual Template Usar?

| Situação | Template | Link |
|----------|----------|------|
| Algo não funciona como esperado | Bug Report | [templates/BUG_REPORT.md](templates/BUG_REPORT.md) |
| Preciso de ajuda/tenho dúvida | Support Request | [templates/SUPPORT_REQUEST.md](templates/SUPPORT_REQUEST.md) |
| Sistema fora do ar/problema crítico | Incident Report | [templates/INCIDENT_REPORT.md](templates/INCIDENT_REPORT.md) |
| Quero sugerir uma melhoria | Feature Request | [templates/FEATURE_REQUEST.md](templates/FEATURE_REQUEST.md) |

---

## 🚨 Níveis de Prioridade

| Nível | Resposta | Resolução | Quando Usar |
|-------|----------|-----------|-------------|
| 🔴 **P1 Crítica** | < 1h | < 4h | Sistema indisponível, perda de dados |
| 🟠 **P2 Alta** | < 4h | < 24h | Funcionalidade principal quebrada |
| 🟡 **P3 Média** | < 8h | < 72h | Funcionalidade secundária afetada |
| 🟢 **P4 Baixa** | < 24h | < 1 semana | Problemas menores, cosméticos |

---

## 📋 Checklist Rápido

### Antes de Criar Issue
- [ ] Pesquisei issues existentes
- [ ] Tentei reproduzir o problema
- [ ] Coletei informações do ambiente
- [ ] Preparei screenshots/logs

### Informações Essenciais
- [ ] Título claro e descritivo
- [ ] Passos para reproduzir
- [ ] Comportamento esperado vs atual
- [ ] Ambiente (SO, navegador, versão)
- [ ] Evidências anexadas

---

## 📞 Contatos Rápidos

| Tipo | Contato |
|------|---------|
| Suporte Geral | suporte@exemplo.com |
| Emergências | +55 11 9999-9999 |
| Escalação | gerencia@exemplo.com |

---

## 🔄 Estados da Issue

```
Novo → Triagem → Em Análise → Resolução → Fechado
                     ↓
                 Pendente
```

---

## ✍️ Bons Títulos

| ❌ Ruim | ✅ Bom |
|---------|--------|
| "Erro" | "Erro 500 ao salvar pedido com cupom de desconto" |
| "Não funciona" | "Botão de login não responde no Safari 17" |
| "Ajuda" | "Como exportar relatório de vendas em Excel?" |
| "Bug" | "Cálculo de frete incorreto para região Norte" |

---

## 📝 Modelo Mínimo de Bug

```markdown
**Título:** [Ação + Resultado + Contexto]

**Passos:**
1. [Passo]
2. [Passo]

**Esperado:** [O que deveria acontecer]
**Atual:** [O que acontece]

**Ambiente:** [SO/Browser/Versão]
```

---

## 🏷️ Labels Comuns

| Label | Uso |
|-------|-----|
| `bug` | Erro no sistema |
| `enhancement` | Melhoria |
| `question` | Dúvida |
| `urgent` | Necessita atenção imediata |
| `blocked` | Aguardando dependência |
| `wontfix` | Não será corrigido |
| `duplicate` | Issue duplicada |

---

*Documentação completa: [SUPPORT_ISSUES.md](SUPPORT_ISSUES.md)*
