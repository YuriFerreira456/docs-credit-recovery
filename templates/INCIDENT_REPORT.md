# ⚠️ Incident Report Template (Relatório de Incidente)

> Use este template para documentar incidentes de produção ou problemas críticos.

---

## Identificação do Incidente

| Campo | Valor |
|-------|-------|
| **ID do Incidente** | INC-[AAAA]-[NÚMERO] |
| **Título** | [Descrição breve do incidente] |
| **Data de Abertura** | [DD/MM/AAAA HH:MM] |
| **Reportado por** | [Nome] |
| **Equipe Responsável** | [Nome da equipe] |

---

## Status Atual

### Estado
- [ ] 🔴 **Ativo** - Incidente em andamento
- [ ] 🟡 **Mitigado** - Impacto reduzido, investigação continua
- [ ] 🟢 **Resolvido** - Problema corrigido
- [ ] ⚪ **Fechado** - Documentação completa, post-mortem realizado

### Severidade
- [ ] **SEV-1 (Crítica)** - Indisponibilidade total / Perda de dados / Segurança
- [ ] **SEV-2 (Alta)** - Degradação severa / Funcionalidade principal afetada
- [ ] **SEV-3 (Média)** - Degradação parcial / Funcionalidade secundária
- [ ] **SEV-4 (Baixa)** - Impacto mínimo / Problema isolado

---

## Impacto

### Serviços Afetados
| Serviço | Status | Início | Fim |
|---------|--------|--------|-----|
| [Nome do serviço] | [Indisponível/Degradado] | [HH:MM] | [HH:MM] |
| [Nome do serviço] | [Indisponível/Degradado] | [HH:MM] | [HH:MM] |

### Usuários Afetados
- **Quantidade estimada:** [Número ou porcentagem]
- **Tipo de usuários:** [Todos / Região específica / Tipo específico]
- **Reclamações recebidas:** [Número]

### Impacto no Negócio
- [ ] Perda de receita: [Estimativa se conhecida]
- [ ] Violação de SLA: [Sim/Não - detalhes]
- [ ] Danos à reputação: [Avaliação]
- [ ] Outros: [Especificar]

---

## Timeline do Incidente

| Timestamp | Evento | Responsável |
|-----------|--------|-------------|
| [DD/MM HH:MM] | **Detecção:** [Como foi detectado] | [Nome/Sistema] |
| [DD/MM HH:MM] | **Alerta:** [Quem foi notificado] | [Automático/Manual] |
| [DD/MM HH:MM] | **Ação:** [O que foi feito] | [Nome] |
| [DD/MM HH:MM] | **Ação:** [O que foi feito] | [Nome] |
| [DD/MM HH:MM] | **Mitigação:** [Ação de mitigação] | [Nome] |
| [DD/MM HH:MM] | **Resolução:** [Como foi resolvido] | [Nome] |

---

## Descrição Técnica

### Resumo do Problema
[Descrição técnica clara do que aconteceu]

### Sintomas Observados
- [Sintoma 1: ex. Latência elevada nas requisições]
- [Sintoma 2: ex. Erros 500 no endpoint /api/users]
- [Sintoma 3: ex. CPU em 100% nos servidores web]

### Causa Raiz
> **Status da Causa Raiz:** [Identificada / Em investigação / Desconhecida]

[Descrição detalhada da causa raiz, se identificada]

### Métricas e Logs

#### Métricas Chave
```
[Cole métricas relevantes: CPU, memória, latência, error rate, etc.]
```

#### Logs Relevantes
```
[Cole trechos de log que mostram o problema]
[Remova informações sensíveis]
```

#### Gráficos/Dashboards
[Links para dashboards ou anexe screenshots]

---

## Ações de Resposta

### Ações Imediatas (Durante o incidente)
| # | Ação | Responsável | Status | Resultado |
|---|------|-------------|--------|-----------|
| 1 | [Ação tomada] | [Nome] | ✅ Completa | [Resultado] |
| 2 | [Ação tomada] | [Nome] | ✅ Completa | [Resultado] |
| 3 | [Ação tomada] | [Nome] | 🔄 Em andamento | [Status atual] |

### Solução Aplicada
[Descreva a solução que resolveu o incidente]

### Rollback (Se aplicável)
- [ ] Rollback foi necessário
- **Versão anterior:** [Versão]
- **Versão problemática:** [Versão]
- **Tempo de rollback:** [Minutos]

---

## Comunicação

### Comunicação Interna
| Quando | Canal | Mensagem |
|--------|-------|----------|
| [HH:MM] | [Slack/Email] | [Resumo da mensagem] |

### Comunicação Externa (Clientes)
| Quando | Canal | Mensagem |
|--------|-------|----------|
| [HH:MM] | [Status Page/Email] | [Resumo da mensagem] |

---

## Post-Mortem

### O que funcionou bem?
- [Item 1]
- [Item 2]
- [Item 3]

### O que poderia ter sido melhor?
- [Item 1]
- [Item 2]
- [Item 3]

### Lições Aprendidas
1. [Lição 1]
2. [Lição 2]
3. [Lição 3]

---

## Ações Preventivas (Follow-ups)

| # | Ação | Responsável | Prazo | Prioridade | Status |
|---|------|-------------|-------|------------|--------|
| 1 | [Ação preventiva] | [Nome] | [DD/MM] | Alta | 🔴 Pendente |
| 2 | [Ação preventiva] | [Nome] | [DD/MM] | Média | 🟡 Em andamento |
| 3 | [Melhorar monitoramento] | [Nome] | [DD/MM] | Alta | 🔴 Pendente |
| 4 | [Atualizar runbook] | [Nome] | [DD/MM] | Baixa | 🟢 Completa |

---

## Referências

### Links Úteis
- [Link para PR/commit do fix]
- [Link para dashboard de métricas]
- [Link para runbook relacionado]
- [Link para documentação técnica]

### Incidentes Relacionados
- [INC-XXXX - Descrição]
- [INC-YYYY - Descrição]

---

## Aprovações

| Papel | Nome | Data | Assinatura |
|-------|------|------|------------|
| Incident Commander | [Nome] | [DD/MM] | ☑️ |
| Tech Lead | [Nome] | [DD/MM] | ☑️ |
| Gerente | [Nome] | [DD/MM] | ☐ |

---

## Histórico de Atualizações

| Data | Autor | Mudança |
|------|-------|---------|
| [DD/MM/AAAA] | [Nome] | Criação do documento |
| [DD/MM/AAAA] | [Nome] | [Descrição da mudança] |

---

*Template versão 1.0 - Atualizado em 08/01/2026*
