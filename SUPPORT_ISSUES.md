# 📋 Documentação de Support Issues (Problemas de Suporte)

Este documento fornece diretrizes completas para a criação, gerenciamento e resolução de issues de suporte.

---

## 📑 Índice

1. [Visão Geral](#visão-geral)
2. [Tipos de Support Issues](#tipos-de-support-issues)
3. [Como Criar uma Support Issue](#como-criar-uma-support-issue)
4. [Níveis de Prioridade](#níveis-de-prioridade)
5. [Ciclo de Vida de uma Issue](#ciclo-de-vida-de-uma-issue)
6. [Templates](#templates)
7. [Exemplos Práticos](#exemplos-práticos)
8. [Boas Práticas](#boas-práticas)
9. [FAQ](#faq)

---

## Visão Geral

**Support Issues** são registros formais de problemas, dúvidas ou solicitações reportadas por usuários ou identificadas pela equipe de suporte. Elas servem como base para rastreamento, priorização e resolução de problemas.

### Objetivos

- ✅ Centralizar o registro de problemas
- ✅ Facilitar a comunicação entre equipes
- ✅ Manter histórico de soluções
- ✅ Melhorar a qualidade do produto/serviço
- ✅ Reduzir tempo de resolução

---

## Tipos de Support Issues

| Tipo | Descrição | Exemplo |
|------|-----------|---------|
| 🐛 **Bug** | Erro ou comportamento inesperado do sistema | Sistema não salva alterações |
| ❓ **Dúvida** | Pergunta sobre funcionalidade ou uso | Como exportar relatórios? |
| 🔧 **Solicitação de Recurso** | Pedido de nova funcionalidade | Adicionar filtro por data |
| ⚠️ **Incidente** | Problema crítico afetando produção | Sistema fora do ar |
| 📚 **Documentação** | Falta ou erro em documentação | Manual desatualizado |
| 🔒 **Segurança** | Vulnerabilidade ou problema de segurança | Falha de autenticação |

---

## Como Criar uma Support Issue

### Passo a Passo

1. **Identificar o Tipo** - Determine a categoria do problema
2. **Coletar Informações** - Reúna todos os dados relevantes
3. **Usar o Template** - Preencha o template apropriado
4. **Definir Prioridade** - Avalie a urgência e impacto
5. **Atribuir** - Encaminhe para a equipe responsável
6. **Acompanhar** - Monitore o progresso até a resolução

### Informações Essenciais

```
- Título claro e descritivo
- Descrição detalhada do problema
- Passos para reproduzir (se aplicável)
- Ambiente (sistema operacional, navegador, versão)
- Screenshots ou logs
- Impacto no usuário/negócio
- Dados de contato do reportador
```

---

## Níveis de Prioridade

### 🔴 Crítica (P1)
- **Tempo de Resposta:** < 1 hora
- **Tempo de Resolução:** < 4 horas
- **Critérios:**
  - Sistema completamente indisponível
  - Perda de dados
  - Vulnerabilidade de segurança ativa
  - Impacto financeiro significativo

### 🟠 Alta (P2)
- **Tempo de Resposta:** < 4 horas
- **Tempo de Resolução:** < 24 horas
- **Critérios:**
  - Funcionalidade principal comprometida
  - Afeta grande número de usuários
  - Workaround difícil ou inexistente

### 🟡 Média (P3)
- **Tempo de Resposta:** < 8 horas
- **Tempo de Resolução:** < 72 horas
- **Critérios:**
  - Funcionalidade secundária afetada
  - Workaround disponível
  - Impacto moderado

### 🟢 Baixa (P4)
- **Tempo de Resposta:** < 24 horas
- **Tempo de Resolução:** < 1 semana
- **Critérios:**
  - Problema cosmético
  - Melhoria de usabilidade
  - Impacto mínimo

---

## Ciclo de Vida de uma Issue

```
┌─────────┐    ┌──────────┐    ┌─────────────┐    ┌───────────┐    ┌──────────┐
│  Novo   │───▶│ Triagem  │───▶│ Em Análise  │───▶│ Resolução │───▶│ Fechado  │
└─────────┘    └──────────┘    └─────────────┘    └───────────┘    └──────────┘
                    │                                    │
                    │          ┌───────────┐            │
                    └─────────▶│ Pendente  │◀───────────┘
                               └───────────┘
```

### Estados

| Estado | Descrição |
|--------|-----------|
| **Novo** | Issue recém-criada, aguardando triagem |
| **Triagem** | Em análise inicial para classificação |
| **Em Análise** | Equipe técnica investigando |
| **Pendente** | Aguardando informação ou ação externa |
| **Resolução** | Solução sendo implementada |
| **Fechado** | Issue resolvida e validada |

---

## Templates

### Template: Bug Report

```markdown
## 🐛 Bug Report

**Título:** [Descrição breve do bug]

### Descrição
[Descrição detalhada do problema]

### Passos para Reproduzir
1. [Primeiro passo]
2. [Segundo passo]
3. [Terceiro passo]

### Comportamento Esperado
[O que deveria acontecer]

### Comportamento Atual
[O que está acontecendo]

### Ambiente
- **Sistema Operacional:** [ex: Windows 11, macOS 14, Ubuntu 22.04]
- **Navegador:** [ex: Chrome 120, Firefox 121]
- **Versão do Sistema:** [ex: v2.5.1]

### Screenshots/Logs
[Anexar evidências]

### Informações Adicionais
[Qualquer contexto adicional]

### Prioridade Sugerida
- [ ] Crítica (P1)
- [ ] Alta (P2)
- [ ] Média (P3)
- [ ] Baixa (P4)
```

### Template: Solicitação de Suporte

```markdown
## ❓ Solicitação de Suporte

**Título:** [Resumo da solicitação]

### Descrição do Problema/Dúvida
[Explique detalhadamente sua necessidade]

### O que já foi tentado
[Liste as soluções já testadas]

### Urgência
- [ ] Urgente - Bloqueando trabalho
- [ ] Normal - Pode aguardar
- [ ] Baixa - Quando possível

### Informações do Usuário
- **Nome:** [Nome completo]
- **Email:** [email@exemplo.com]
- **Departamento/Empresa:** [Identificação]
- **Conta/ID:** [Se aplicável]

### Anexos
[Adicione arquivos relevantes]
```

### Template: Incidente

```markdown
## ⚠️ Relatório de Incidente

**ID do Incidente:** [INC-XXXXX]
**Data/Hora de Início:** [DD/MM/AAAA HH:MM]

### Resumo
[Breve descrição do incidente]

### Impacto
- **Usuários Afetados:** [Número estimado]
- **Serviços Afetados:** [Lista de serviços]
- **Severidade:** [Crítica/Alta/Média/Baixa]

### Timeline
| Hora | Evento |
|------|--------|
| HH:MM | [Descrição do evento] |

### Causa Raiz
[Identificação da causa - se conhecida]

### Ações Tomadas
1. [Ação 1]
2. [Ação 2]

### Status Atual
- [ ] Em investigação
- [ ] Mitigado
- [ ] Resolvido

### Próximos Passos
[Ações planejadas]
```

---

## Exemplos Práticos

### Exemplo 1: Bug de Login

```markdown
## 🐛 Bug Report

**Título:** Erro 500 ao fazer login com autenticação Google

### Descrição
Usuários não conseguem fazer login usando a opção "Entrar com Google". 
O sistema retorna erro 500 após a autenticação no Google.

### Passos para Reproduzir
1. Acessar a página de login (https://app.exemplo.com/login)
2. Clicar em "Entrar com Google"
3. Selecionar conta Google válida
4. Autorizar o aplicativo
5. Observar erro 500

### Comportamento Esperado
Usuário deve ser redirecionado para o dashboard após autenticação.

### Comportamento Atual
Página de erro 500 é exibida. Usuário não consegue acessar o sistema.

### Ambiente
- **Sistema Operacional:** Windows 11
- **Navegador:** Chrome 120.0.6099.130
- **Versão do Sistema:** v3.2.0

### Screenshots/Logs
![Erro 500](screenshot-erro-500.png)

```
2026-01-08 10:23:45 ERROR OAuth2CallbackHandler: 
Token exchange failed - Invalid client credentials
```

### Informações Adicionais
- Problema iniciou após deploy de 07/01/2026
- Login com email/senha funciona normalmente
- ~500 usuários afetados (30% da base)

### Prioridade Sugerida
- [x] Crítica (P1)
- [ ] Alta (P2)
- [ ] Média (P3)
- [ ] Baixa (P4)
```

---

### Exemplo 2: Dúvida de Uso

```markdown
## ❓ Solicitação de Suporte

**Título:** Como exportar relatório de vendas em formato Excel?

### Descrição do Problema/Dúvida
Preciso exportar o relatório mensal de vendas em formato Excel (.xlsx) 
para apresentação à diretoria. Não encontro a opção de exportação.

### O que já foi tentado
- Procurei no menu "Relatórios" - só encontrei opção PDF
- Verifiquei documentação online - não encontrei informação
- Tentei botão direito na tabela - sem opção de exportar

### Urgência
- [ ] Urgente - Bloqueando trabalho
- [x] Normal - Pode aguardar
- [ ] Baixa - Quando possível

### Informações do Usuário
- **Nome:** Maria Silva
- **Email:** maria.silva@empresa.com
- **Departamento/Empresa:** Comercial / Empresa ABC
- **Conta/ID:** USR-12345

### Anexos
[Screenshot da tela de relatórios anexado]
```

---

### Exemplo 3: Incidente de Produção

```markdown
## ⚠️ Relatório de Incidente

**ID do Incidente:** INC-2026-0108
**Data/Hora de Início:** 08/01/2026 14:32

### Resumo
API de pagamentos retornando timeout, impossibilitando 
processamento de transações.

### Impacto
- **Usuários Afetados:** ~2.000 (todas as transações)
- **Serviços Afetados:** Checkout, API de Pagamentos, Webhooks
- **Severidade:** Crítica

### Timeline
| Hora | Evento |
|------|--------|
| 14:32 | Primeiros alertas de timeout recebidos |
| 14:35 | Equipe de plantão acionada |
| 14:40 | Identificado alta latência no banco de dados |
| 14:45 | Reinício do serviço de cache iniciado |
| 14:52 | Serviços normalizados |

### Causa Raiz
Cache Redis ficou sem memória devido a vazamento em job de 
sincronização implementado na última release.

### Ações Tomadas
1. Reinício do serviço Redis
2. Aumento temporário de memória
3. Rollback do job problemático

### Status Atual
- [ ] Em investigação
- [ ] Mitigado
- [x] Resolvido

### Próximos Passos
- [ ] Post-mortem completo até 10/01
- [ ] Implementar limite de memória no job
- [ ] Adicionar alertas de memória do Redis
```

---

## Boas Práticas

### ✅ Faça

1. **Seja específico** - Forneça detalhes suficientes para reproduzir o problema
2. **Use títulos descritivos** - "Erro ao salvar" ❌ vs "Erro 500 ao salvar pedido com mais de 100 itens" ✅
3. **Inclua evidências** - Screenshots, logs, vídeos ajudam muito
4. **Atualize o status** - Mantenha a issue atualizada conforme progresso
5. **Documente a solução** - Registre como o problema foi resolvido
6. **Verifique duplicatas** - Pesquise antes de criar nova issue
7. **Seja profissional** - Mantenha comunicação respeitosa

### ❌ Evite

1. **Títulos vagos** - "Não funciona", "Erro", "Ajuda"
2. **Informações incompletas** - Falta de passos para reproduzir
3. **Múltiplos problemas** - Uma issue por problema
4. **Linguagem agressiva** - Mantenha o profissionalismo
5. **Assumir prioridades** - Deixe a triagem definir
6. **Fechar sem validar** - Confirme a resolução antes de fechar

---

## FAQ

### Como sei se devo criar uma nova issue ou comentar em uma existente?

Se o problema é exatamente o mesmo descrito em uma issue aberta, adicione um comentário. Se há diferenças significativas (ambiente diferente, erro diferente), crie uma nova issue referenciando a existente.

### Quanto tempo leva para minha issue ser respondida?

O tempo de resposta depende da prioridade:
- P1 (Crítica): < 1 hora
- P2 (Alta): < 4 horas
- P3 (Média): < 8 horas
- P4 (Baixa): < 24 horas

### Posso alterar a prioridade da minha issue?

Você pode sugerir uma prioridade, mas a classificação final é feita pela equipe de triagem com base nos critérios estabelecidos.

### O que fazer se minha issue não está recebendo atenção?

1. Verifique se todas as informações foram fornecidas
2. Adicione comentário solicitando atualização
3. Se urgente, escale para seu gerente ou use canal de emergência

### Como acompanho o progresso da minha issue?

- Você receberá notificações por email a cada atualização
- Acesse o portal de suporte para ver status em tempo real
- Use o ID da issue para consultas

---

## Contatos e Escalação

| Nível | Contato | Quando Usar |
|-------|---------|-------------|
| **Suporte Geral** | suporte@exemplo.com | Dúvidas e problemas gerais |
| **Suporte Urgente** | +55 11 9999-9999 | Incidentes P1/P2 |
| **Escalação Técnica** | tech-lead@exemplo.com | Problemas técnicos complexos |
| **Escalação Gerencial** | gerencia@exemplo.com | SLA não cumprido |

---

## Changelog

| Data | Versão | Descrição |
|------|--------|-----------|
| 08/01/2026 | 1.0.0 | Versão inicial da documentação |

---

*Documentação mantida pela Equipe de Suporte*
*Última atualização: 08 de Janeiro de 2026*
