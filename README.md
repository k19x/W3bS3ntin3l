# 🛡️ WebSentinel - Advanced Web Security Testing Tool

## Visão Geral

**WebSentinel** é uma poderosa extensão Chrome (Manifest V3) para testes de segurança web avançados. Funciona como um proxy HTTP/HTTPS integrado ao navegador, oferecendo ferramentas profissionais para interceptação, modificação e análise de tráfego com suporte a inteligência artificial.

**Versão**: 13.0  
**Status**: Production Ready  
**Público-alvo**: Penetration Testers, Security Researchers, Web Application Security Specialists

---

## 🎯 Principais Pontos Fortes

### 1. **Interception & Modificação de Tráfego**
- ✅ Interceptação bidirecional de requisições HTTP/HTTPS
- ✅ Modificação de requisições em tempo real
- ✅ Captura e análise de respostas
- ✅ Suporte a múltiplas abas simultâneas
- ✅ Auto-aprovação e rejeição de requisições
- ✅ Sistema de escopo para filtrar URLs

### 2. **Análise Alimentada por IA (Gemini API)**
- 🤖 **Análise automática de vulnerabilidades** usando Google Generative AI
- 🤖 **Relatórios de segurança em português (pt-BR)** com recomendações
- 🤖 **Análise de padrões de requisição** e detecção de anomalias
- 🤖 **Análise de tráfego de intruder** com insights de segurança
- 🤖 **Export de relatórios em Markdown** para documentação

### 3. **Ataques JWT (JSON Web Tokens)**
- 🔑 Decodificação e análise de JWTs
- 🔑 Teste de segredos fracos (força bruta)
- 🔑 Manipulação de claims e algoritmos
- 🔑 Suporte a HS256, HS384, HS512
- 🔑 Simulação de assinatura com CryptoJS

### 4. **Fuzzing & Intruder**
- 🎯 **Ataque tipo Intruder** com múltiplos playloads
- 🎯 Modos: Simple List, Numbers, Clusterbomb, Pitchfork
- 🎯 Processamento paralelo e aceleração de requisições
- 🎯 Análise de resultados com sorteamento e filtros
- 🎯 Geração de relatório de análise com IA integrada

### 5. **Repeater Avançado**
- 🔄 Editor de requisições com syntax highlighting
- 🔄 Renderização automática de responses HTML
- 🔄 Sincronização de abas de requisição/resposta
- 🔄 Suporte a múltiplas abas (namespaces independentes)
- 🔄 Redirecionamento de requisições automático

### 6. **Decodificadores & Codificadores**
- 🔐 Base64 (encode/decode)
- 🔐 URL (encode/decode)
- 🔐 HTML (encode/decode)
- 🔐 Decodificação inteligente multi-camadas
- 🔐 Conversão entre formatos

### 7. **Histórico Completo de Requisições**
- 📋 Captura de todas as requisições com metadata
- 📋 Filtros avançados (método, tipo, status, escopo)
- 📋 Busca global em requisições/respostas
- 📋 Export em formato HAR para Burp Suite
- 📋 Highlight de palavras-chave em todo o histórico
- 📋 Sincronização com Sitemap

### 8. **Sitemap & Mapeamento de Application**
- 🗺️ Construção automática de árvore de domínios
- 🗺️ Visualização hierárquica de endpoints
- 🗺️ Sincronização com histórico de requisições
- 🗺️ Marcadores de escopo aplicado
- 🗺️ Suporte a edição de escopo em tempo real

### 9. **Comparador de Requisições/Respostas**
- 🔍 Comparação lado-a-lado com diff visual
- 🔍 Sincronização de scroll bidirecional
- 🔍 Estatísticas de similaridade (Levenshtein)
- 🔍 Suporte a splitter vertical e horizontal redimensionável
- 🔍 Análise detalhada de diferenças

### 10. **Visualização de Fluxo de Dados**
- 📊 Diagrama de fluxo de requisições (Request Flow)
- 📊 Visualização de padrões de autenticação
- 📊 Detecção automática de fluxos de tokens
- 📊 Zoom, pan e operações interativas
- 📊 Export em formato SVG

### 11. **Sistema de Temas**
- 🎨 Temas inteligentes (Dark/Light)
- 🎨 Cores paleta Burp Suite (Orange accent)
- 🎨 Temas personalizáveis com cores customizadas
- 🎨 Persistência de preferências de tema
- 🎨 Suporte a easter eggs (Fart Suite 🎉)

### 12. **Auto-Save & Persistência**
- 💾 **Salvamento automático em arquivo** (File System Access API)
- 💾 Persistência completa de estado da sessão
- 💾 Suporte a múltiplos diretórios de projetos
- 💾 Carregamento automático de estado anterior
- 💾 Backup de dados críticos em localStorage

### 13. **Notas & Documentação**
- 📝 Sistema multi-aba de notas
- 📝 Editores rich com undo/redo
- 📝 Sincronização com projeto
- 📝 Associação por requisição

### 14. **WebSocket Support**
- 🔌 Captura de frames WebSocket
- 🔌 Visualização de mensagens binárias e texto
- 🔌 Análise de conexões WebSocket ativas
- 🔌 Timing e metadata de frames

### 15. **Ferramentas de Segurança**
- 🔒 Manejo de certificados SSL/TLS
- 🔒 Bloqueio de conteúdo por regex (Blacklist)
- 🔒 Sistema de Escopo (Scope) para URLs
- 🔒 Context menu integrado com opções de segurança
- 🔒 Proteção de dados sensíveis

---

## 🏗️ Arquitetura Técnica

### Estrutura Modular
```
WebSentinel/
├── modules/
│   ├── core/               # Utilitários e constantes
│   │   ├── constants.obf.js
│   │   ├── themes.obf.js
│   │   └── utils.obf.js
│   ├── features/           # Funcionalidades principais
│   │   ├── encoders.obf.js
│   │   ├── request-parser.obf.js
│   │   ├── traffic-ai.obf.js
│   │   └── validators.obf.js
│   ├── services/           # Serviços
│   │   ├── storage-manager.obf.js
│   │   └── sync-manager.obf.js
│   └── ui/                 # Componentes UI
│       ├── editor-utils.obf.js
│       ├── request-builder.obf.js
│       ├── response-renderer.obf.js
│       ├── syntax-highlighter.obf.js
│       └── websocket-controller.obf.js
├── sidepanel.html          # Interface principal
├── sidepanel.obf.js        # Lógica da extensão (obfuscado)
├── background.obf.js       # Service Worker
├── devtools.html           # DevTools (futuro)
└── manifest.json           # Configuração Manifest V3
```

### Tecnologias Utilizadas
- **Manifest V3** - Segurança moderna do Chrome
- **Chrome APIs**:
  - `declarativeNetRequest` - Interceptação de rede sem performance hit
  - `debugger` - Acesso profundo ao protocolo DevTools
  - `storage` - Persistência de dados
  - `clipboardWrite` - Operações de clipboard

- **Integrações Externas**:
  - **Google Generative AI (Gemini)** - Análise assistida por IA
  - **CryptoJS** - Operações criptográficas (JWT signing)
  - **highlight.js** - Syntax highlighting com +190 linguagens

- **APIs do Navegador**:
  - **File System Access API** - Auto-save em arquivos
  - **Fetch API** - Requisições HTTP
  - **Web Workers** - Processamento paralelo
  - **requestAnimationFrame** - Animações otimizadas

---

## ⚡ Otimizações de Performance

### 1. **Processamento em Batch com requestAnimationFrame**
- Batches de 5 issues por frame (~16ms @ 60fps)
- Elimina violações de timeout do Chrome
- Renderização suave mesmo com milhares de requisições

### 2. **Debouncing de Operações Custosas**
- Filtro de histórico: debounce de 200ms
- Evita reflow/repaint excessivos
- Pesquisa otimizada com memoização

### 3. **Lazy Loading**
- Carregamento sob demanda de módulos
- Parsing progressivo de requisições
- Cache de dados computados

### 4. **Persistência Inteligente**
- Auto-save com debounce (5s)
- Sincronização incremental de estado
- Compression de dados grandes

---

## 🔐 Recursos de Segurança

✅ **Isolamento de Contexto** - Scripts executam em contextos isolados  
✅ **CSP (Content Security Policy)** - Política restritiva de segurança  
✅ **Validação de Entradas** - Sanitização de dados do usuário  
✅ **Criptografia de JWT** - Suporte a múltiplos algoritmos  
✅ **Suporte a HTTPS** - Interceptação segura de tráfego criptografado  
✅ **Prevenção de Injection** - HTML/JavaScript escaping  

---

## 🎮 Funcionalidades Interativas

### Editores Rich com Undo/Redo
- Sistema de histórico com stack de até 50 estados
- Navegação por Ctrl+Z / Ctrl+Y
- Sincronização automática com line numbers

### Splitters Redimensionáveis
- Vertical splitter para issue details (localStorage persistido)
- Horizontal splitter para comparador
- Suporte a mouse drag com snap points

### UI Responsiva
- Layout flexbox adaptável
- Tabs com context switching
- Modal dialogs para confirmação

---

## 📊 Estatísticas da Aplicação

| Métrica | Valor |
|---------|-------|
| Versão | 13.0 |
| Tamanho Base | ~150KB (obfuscated) |
| Modules | 4 categorias principais |
| Permissões | 10 permissões críticas |
| APIs Integradas | Gemini AI + 3 APIs Chrome |
| Temas Suportados | 2 temas + customização |
| Máximos de Dados | 4 repetições, ∞ histórico |

---

## 🚀 Diferenciais vs Concorrentes

1. **IA Nativa** - Gem AI integrada (relatórios em português)
2. **Auto-Save** - Persiste em arquivo local automaticamente
3. **Modular** - Arquitetura extensível e upgradable
4. **Performance** - Otimizado para 0 violações de performance
5. **Completo** - Integra features de Burp Suite Pro num add-on

---

## 🔄 Fluxo de Uso Típico

```
1. Interceptar requisição → 2. Analisar (AI) → 3. Modificar
        ↓                          ↓                  ↓
   Histórico            Relatório Security    Repeater/Intruder
        ↓                          ↓                  ↓
   Sitemap             Export em Markdown    Fuzzing & Testes
        ↓                          ↓                  ↓
   Comparador         Documentação             Análise Resultados
```

---

## 📋 Requisitos & Compatibilidade

- ✅ **Chrome/Chromium** 90+
- ✅ **API File System** (para auto-save)
- ✅ **Conexão Internet** (para análise com IA)
- ✅ **Google Generative AI API Key** (opcional)

---

## 💡 Casos de Uso

1. **Penetration Testing** → Interceptação + Fuzzing + IA Analysis
2. **API Security** → JWT analysis + Request modification
3. **Bug Bounty** → Monitoring + Flow visualization
4. **Web Development** → Request debugging + Comparação
5. **Security Research** → Traffic analysis + Pattern recognition

---

## 📝 Notas de Desenvolvimento

- Código obfuscado para proteção de IP
- Módulos web-accessible para injeção em páginas
- Service Worker para background processing
- Sincronização bidirecional de dados

---

## 🎯 Próximas Evoluções

- [ ] DevTools integration completa
- [ ] Gravação/playback de scripts
- [ ] Extensão de plugins
- [ ] Collaboration features (cloud sync)
- [ ] Machine Learning para detecção de anomalias

---

**WebSentinel** © 2025 - Advanced Web Security Testing  
*For authorized security testing only*
