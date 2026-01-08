# 🛠️ Support Issues - Base de Conhecimento

Registro de problemas conhecidos e suas soluções.

---

## Índice

- [Autenticação](#autenticação)
- [Banco de Dados](#banco-de-dados)
- [Performance](#performance)
- [Integração](#integração)
- [Interface](#interface)

---

## Autenticação

### Login retorna erro 401 mesmo com credenciais corretas

**Problema:** Usuário não consegue fazer login, recebe erro 401 Unauthorized.

**Causa:** Token JWT expirado armazenado no localStorage.

**Solução:**
```javascript
// Limpar storage do navegador
localStorage.clear();
sessionStorage.clear();
// Tentar login novamente
```

---

### OAuth Google falha com "redirect_uri_mismatch"

**Problema:** Autenticação com Google retorna erro de redirect_uri.

**Causa:** URI de callback não cadastrada no Google Console.

**Solução:**
1. Acessar [Google Cloud Console](https://console.cloud.google.com)
2. Ir em APIs & Services > Credentials
3. Adicionar a URI correta em "Authorized redirect URIs"
4. Aguardar 5 minutos para propagação

---

## Banco de Dados

### Conexão recusada ao banco PostgreSQL

**Problema:** Erro `ECONNREFUSED` ao conectar no banco.

**Causa:** Serviço PostgreSQL não está rodando.

**Solução:**
```bash
# Linux
sudo systemctl start postgresql
sudo systemctl status postgresql

# Docker
docker start postgres-container
```

---

### Query lenta em tabela grande

**Problema:** SELECT demora mais de 10 segundos.

**Causa:** Falta de índice na coluna de busca.

**Solução:**
```sql
-- Criar índice na coluna usada no WHERE
CREATE INDEX idx_users_email ON users(email);

-- Verificar se índice está sendo usado
EXPLAIN ANALYZE SELECT * FROM users WHERE email = 'test@test.com';
```

---

## Performance

### Alto consumo de memória em Node.js

**Problema:** Aplicação consome mais de 1GB de RAM.

**Causa:** Memory leak em event listeners.

**Solução:**
```javascript
// Remover listeners quando não mais necessários
eventEmitter.removeListener('event', handler);

// Ou usar once() para listeners únicos
eventEmitter.once('event', handler);
```

---

### Aplicação React lenta ao renderizar listas

**Problema:** Scroll travando em listas com muitos itens.

**Causa:** Renderização de todos os itens ao mesmo tempo.

**Solução:**
```bash
npm install react-window
```

```jsx
import { FixedSizeList } from 'react-window';

<FixedSizeList
  height={400}
  itemCount={items.length}
  itemSize={50}
>
  {({ index, style }) => (
    <div style={style}>{items[index]}</div>
  )}
</FixedSizeList>
```

---

## Integração

### Webhook não recebe requisições

**Problema:** Endpoint de webhook nunca é chamado.

**Causa:** Firewall bloqueando requisições externas.

**Solução:**
```bash
# Verificar se porta está aberta
sudo ufw allow 443/tcp

# Testar endpoint externamente
curl -X POST https://seu-dominio.com/webhook -d '{"test": true}'
```

---

### CORS bloqueando requisições do frontend

**Problema:** Erro `Access-Control-Allow-Origin` no console.

**Causa:** Backend não está configurado para aceitar origem do frontend.

**Solução (Express.js):**
```javascript
const cors = require('cors');

app.use(cors({
  origin: 'https://seu-frontend.com',
  methods: ['GET', 'POST', 'PUT', 'DELETE'],
  credentials: true
}));
```

---

## Interface

### Imagens não carregam em produção

**Problema:** Imagens aparecem quebradas após deploy.

**Causa:** Caminho relativo incorreto ou falta de configuração de assets.

**Solução:**
```javascript
// Usar caminho absoluto ou variável de ambiente
const imageUrl = `${process.env.PUBLIC_URL}/images/logo.png`;

// Ou importar diretamente
import logo from './assets/logo.png';
```

---

### CSS não aplica estilos após build

**Problema:** Estilos funcionam em dev mas não em produção.

**Causa:** Classes CSS sendo removidas pelo purge/tree-shaking.

**Solução (Tailwind):**
```javascript
// tailwind.config.js
module.exports = {
  content: [
    './src/**/*.{js,jsx,ts,tsx}',
    './public/index.html'
  ],
}
```

---

## Como Adicionar Nova Issue

Copie o formato abaixo:

```markdown
### Título descritivo do problema

**Problema:** O que acontece.

**Causa:** Por que acontece.

**Solução:**
[Código ou passos para resolver]
```

---

*Última atualização: 08/01/2026*
