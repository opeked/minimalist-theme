# 🎨 VENCORD MINIMALISTA & ANIMADO - Guia Completo

## 📋 Sobre o Tema

Um tema **minimalista**, **bonito** e **altamente animado** para Vencord (Discord modificado) com:

✨ **Principais Features:**
- 🎭 Paleta de cores elegante (roxo/violeta com tons escuros)
- 🎬 Animações suaves em transições e hover
- 💫 Efeitos de glow, bounce e shimmer
- 📱 Totalmente responsivo
- ⚡ Performance otimizada (apenas CSS)
- 🔄 Transições fluidas em todos os elementos

---

## 📥 Instalação

### Passo 1: Abrir QuickCSS no Vencord

1. Abra Discord/Vencord
2. Pressione `Ctrl + Shift + C` (ou `Cmd + Shift + C` no Mac)
3. Procure por "QuickCSS" na busca de plugins
4. Ative o plugin **QuickCSS**

### Passo 2: Adicionar o CSS

1. Volte para a busca de plugins
2. Procure por "QuickCSS" novamente e clique em ⚙️ (Settings)
3. Clique em "Open QuickCSS File" ou "Edit QuickCSS"
4. Copie TODO o conteúdo do arquivo `vencord-minimalista.css`
5. Cole no editor QuickCSS
6. **Salve as alterações** (Ctrl + S)
7. Discord vai atualizar automaticamente!

### Passo 3: Verificar Instalação

- Você deve ver cores diferentes (tons de roxo/violeta)
- As transições devem ser suaves
- Elementos devem ter animações ao passar o mouse

---

## 🎨 Personalizações Rápidas

### Mudar Cor Principal

No início do CSS, encontre:

```css
:root {
  --accent: #7c3aed;        /* Roxo principal */
  --accent-hover: #9f7aea;  /* Roxo ao passar mouse */
}
```

**Trocar por:**
- 🔵 Azul: `#3b82f6` (hover: `#60a5fa`)
- 🟢 Verde: `#10b981` (hover: `#34d399`)
- 🔴 Vermelho: `#ef4444` (hover: `#f87171`)
- 🟠 Laranja: `#f97316` (hover: `#fb923c`)
- 🟡 Amarelo: `#eab308` (hover: `#facc15`)

### Exemplo: Mudar para Azul
```css
:root {
  --accent: #3b82f6;
  --accent-hover: #60a5fa;
}
```

### Mudar Fundos

```css
--bg-dark: #0f1117;      /* Fundo escuro principal */
--primary: #2a2f3a;      /* Painel lateral */
--secondary: #1a1e28;    /* Barra de servidores */
```

### Mudar Velocidade de Animações

Procure por `transition:` e altere o tempo:
- Mais rápido: `0.1s` ou `0.15s`
- Mais lento: `0.4s` ou `0.5s`

Exemplo:
```css
/* Original */
transition: all 0.3s ease !important;

/* Mais rápido */
transition: all 0.15s ease !important;

/* Mais lento */
transition: all 0.5s ease !important;
```

---

## 🎬 Animações Disponíveis

O tema inclui várias animações:

| Animação | Efeito |
|----------|--------|
| **fadeIn** | Desvanece suavemente |
| **slideInLeft** | Desliza da esquerda |
| **glowPulse** | Brilho pulsante |
| **floatUp** | Flutua para cima |
| **smoothBounce** | Pequeno pulo suave |
| **shimmer** | Brilho passando |

---

## 🎯 Dicas Avançadas

### 1. Desabilitar Animações Específicas

Se uma animação incomodar, procure por ela e troque:

```css
/* Desabilitar */
animation: glowPulse 2s ease-in-out infinite !important;

/* Para */
/* animation: none !important; */
```

### 2. Aumentar Brilho (Glow)

Encontre `box-shadow:` e aumente os valores:

```css
/* Padrão */
box-shadow: 0 0 8px rgba(124, 58, 237, 0.3);

/* Mais brilho */
box-shadow: 0 0 16px rgba(124, 58, 237, 0.6);
```

### 3. Mudar Radius (Cantos Arredondados)

Procure por `border-radius:` e altere:
- Mais arredondado: `16px` ou `20px`
- Menos arredondado: `4px` ou `6px`

### 4. Modo Light (Tema Claro)

No final do arquivo, altere:

```css
@media (prefers-color-scheme: dark) {
```

Para usar cores claras:

```css
@media (prefers-color-scheme: light) {
  :root {
    --bg-darker: #f5f5f5 !important;
    --primary: #ffffff !important;
    --text-primary: #000000 !important;
    --text-secondary: #666666 !important;
  }
}
```

---

## 🔧 Solução de Problemas

### CSS Não Está Sendo Aplicado?

1. ✅ Verifique se QuickCSS está **ativado**
2. ✅ Pressione `F5` ou `Ctrl + R` para recarregar Discord
3. ✅ Feche e reabra Discord completamente
4. ✅ Verifique se não há **erros de sintaxe** (abra DevTools: F12)

### Elementos Específicos Não Mudam?

O CSS pode estar sendo sobrescrito. Adicione `!important` no final:

```css
background: var(--bg-dark) !important;  /* ← !important */
```

### Tema Afeta Outras Abas do Navegador?

Isso é normal com QuickCSS. Se quiser limitar:

1. Desative QuickCSS temporariamente
2. Use um plugin alternativo como **CustomCSS**

---

## 🎨 Combinações de Cores Recomendadas

### 1. Roxo Escuro (Padrão)
```css
--accent: #7c3aed;
--accent-hover: #9f7aea;
--bg-dark: #0f1117;
--primary: #2a2f3a;
```

### 2. Azul Neon
```css
--accent: #0ea5e9;
--accent-hover: #38bdf8;
--bg-dark: #0a0e1a;
--primary: #0f172a;
```

### 3. Verde Neon
```css
--accent: #10b981;
--accent-hover: #34d399;
--bg-dark: #0a1a1a;
--primary: #1a2f2a;
```

### 4. Rosa Pastel
```css
--accent: #ec4899;
--accent-hover: #f472b6;
--bg-dark: #1a0a15;
--primary: #2a1a25;
```

### 5. Cyan Cyberpunk
```css
--accent: #06b6d4;
--accent-hover: #22d3ee;
--bg-dark: #0a1620;
--primary: #1a2a35;
```

---

## 📊 Comparação: Antes vs Depois

| Aspecto | Antes | Depois |
|---------|-------|--------|
| Cores | Discord Padrão | Roxo/Violeta Elegante |
| Transições | Padrão | Suave 0.3s |
| Hover Effects | Básico | Animado + Glow |
| Cantos | Menos arredondados | Mais arredondados |
| Sombras | Simples | Camadas de sombra |
| Performance | Normal | Otimizada (CSS Only) |

---

## 🌟 Recursos Extras

### Adicionar Fonte Customizada

No início, adicione:

```css
@import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;600&display=swap');

body {
  font-family: 'JetBrains Mono', monospace !important;
}
```

### Mais Animações

Crie sua própria animação:

```css
@keyframes meuEfeito {
  0% {
    opacity: 0;
    transform: scale(0.8);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}

/* Usar em algum elemento */
.meuElemento {
  animation: meuEfeito 0.4s ease !important;
}
```

---

## 📖 Referências Úteis

- **Discord API Docs**: https://discord.com/developers/docs
- **Vencord GitHub**: https://github.com/Vendicated/Vencord
- **CSS MDN**: https://developer.mozilla.org/pt-BR/docs/Web/CSS

---

## 💡 Dicas Finais

1. 🔄 **Sempre faça backup** do seu CSS antes de grandes mudanças
2. 📱 **Teste em mobile** se usar Discord lá
3. ⚡ **Performance**: Evite usar `box-shadow` em muitos elementos
4. 🎨 **Combine cores**: Escolha 2-3 cores principais
5. ✨ **Não abuse de animações**: Qualidade > Quantidade

---

## 🐛 Encontrou Um Bug?

Se encontrar problemas:

1. Abra DevTools (`F12`)
2. Procure por mensagens de erro (aba Console)
3. Teste desabilitando partes do CSS
4. Compartilhe a screenshot do erro

---

## 🎉 Aproveite seu novo tema!

Se gostou, considere:
- ⭐ Fazer backup do arquivo
- 🔄 Compartilhar com amigos
- 📸 Tirar screenshots do resultado

**Divirta-se customizando! 🚀**

---

*Tema criado com ❤️ para a comunidade Vencord*
*Última atualização: 2026*
