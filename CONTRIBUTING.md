# Contribuindo para o LogisticsHub

Obrigado por seu interesse em contribuir com o LogisticsHub! Este documento fornece diretrizes para contribuir com o projeto.

## 📋 Processo de Contribuição

### 1. Reportando Bugs

Antes de reportar um bug, por favor:

- Verifique se o bug já não foi reportado
- Verifique se o bug ainda existe na versão mais recente
- Forneça informações detalhadas para reproduzir o problema

**Template para reportar bugs:**

```markdown
**Descrição do bug**
Descrição clara do que é o bug.

**Para reproduzir**
Passos para reproduzir:
1. Vá para '...'
2. Clique em '...'
3. Veja o erro

**Comportamento esperado**
Descrição do que deveria acontecer.

**Screenshots**
Se aplicável, adicione screenshots.

**Ambiente:**
 - OS: [ex: Windows 10]
 - Navegador: [ex: Chrome 91]
 - Versão: [ex: 1.0.0]
```

### 2. Sugerindo Features

Para sugerir novas features:

- Use um título claro e descritivo
- Forneça uma descrição detalhada da feature
- Explique por que seria útil
- Inclua exemplos de uso, se possível

### 3. Pull Requests

1. **Fork** o repositório
2. **Clone** seu fork: `git clone https://github.com/seu-usuario/logistics-hub.git`
3. **Crie uma branch**: `git checkout -b feature/nome-da-feature`
4. **Faça suas mudanças**
5. **Commit** suas mudanças: `git commit -m 'Adiciona nova feature'`
6. **Push** para a branch: `git push origin feature/nome-da-feature`
7. Abra um **Pull Request**

## 📝 Padrões de Código

### JavaScript

- Use **ES6+** (arrow functions, destructuring, template literals)
- Use **ES Modules** (`import`/`export`)
- Use **const** e **let** (evite `var`)
- Use **async/await** para código assíncrono
- Siga o padrão de **2 espaços** para indentação

**Exemplo:**

```javascript
// ✅ Bom
const calculateTotal = (items) => {
  return items.reduce((sum, item) => sum + item.price, 0);
};

// ❌ Evitar
function calculateTotal(items) {
  var total = 0;
  for (var i = 0; i < items.length; i++) {
    total += items[i].price;
  }
  return total;
}
```

### CSS

- Use **variáveis CSS** para cores e espaçamentos
- Siga a metodologia **BEM** para nomenclatura
- Use **classes** ao invés de IDs para estilização
- Mantenha especificidade baixa

**Exemplo:**

```css
/* ✅ Bom */
.card {}
.card__header {}
.card--highlighted {}

/* ❌ Evitar */
#card {}
.card div {}
```

### HTML

- Use tags **semânticas**
- Inclua atributos **alt** em imagens
- Use **kebab-case** para atributos data
- Mantenha indentação consistente

**Exemplo:**

```html
<!-- ✅ Bom -->
<article class="card" data-dock-id="1">
  <header class="card__header">
    <h2>Título</h2>
  </header>
</article>

<!-- ❌ Evitar -->
<div class="card">
  <div class="header">
    <div>Título</div>
  </div>
</div>
```

## 🧪 Testes

- Escreva testes para novas funcionalidades
- Mantenha cobertura de testes acima de 80%
- Teste em diferentes navegadores

## 🔒 Segurança

- Nunca commit dados sensíveis
- Sempre sanitize inputs do usuário
- Use escape para prevenir XSS
- Valide todos os dados antes de processar

## 📚 Documentação

- Documente funções e classes com JSDoc
- Mantenha o README.md atualizado
- Atualize a documentação de API se necessário

**Exemplo de JSDoc:**

```javascript
/**
 * Calcula a taxa de ocupação do terminal
 * @param {number} occupied - Número de docas ocupadas
 * @param {number} total - Total de docas
 * @returns {number} Taxa de ocupação em porcentagem
 */
const calculateOccupancy = (occupied, total) => {
  return Math.round((occupied / total) * 100);
};
```

## 🏷️ Commits

Siga o padrão de commits semânticos:

- `feat:` Nova feature
- `fix:` Correção de bug
- `docs:` Mudanças na documentação
- `style:` Formatação, ponto e vírgula, etc
- `refactor:` Refatoração de código
- `test:` Adicionando ou corrigindo testes
- `chore:` Atualização de build, dependências, etc

**Exemplo:**

```bash
git commit -m "feat: adiciona filtro por data nos agendamentos"
git commit -m "fix: corrige cálculo de taxa de ocupação"
git commit -m "docs: atualiza README com instruções de instalação"
```

## 🎯 Revisão de Código

Antes de submeter um PR:

- [ ] Código segue os padrões do projeto
- [ ] Todos os testes passam
- [ ] Documentação está atualizada
- [ ] Commits são claros e descritivos
- [ ] Não há código comentado ou debug

## 💬 Comunicação

- Seja respeitoso e construtivo
- Use issues para discussões técnicas
- Responda a reviews em tempo hábil
- Pergunte se tiver dúvidas

## 📞 Contato

- Email: contato@logisticshub.com
- Issues: [GitHub Issues](https://github.com/seu-usuario/logistics-hub/issues)

---

Obrigado por contribuir! 🎉
