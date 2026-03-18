# LogisticsHub 🚛

Sistema de Controle de Docas para gerenciamento de operações logísticas em tempo real.

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![ES Modules](https://img.shields.io/badge/ES-Modules-orange.svg)

## 📋 Índice

- [Sobre](#sobre)
- [Funcionalidades](#funcionalidades)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Instalação](#instalação)
- [Uso](#uso)
- [Segurança](#segurança)
- [Tecnologias](#tecnologias)
- [Contribuição](#contribuição)
- [Licença](#licença)

## 🎯 Sobre

O **LogisticsHub** é uma aplicação web moderna para controle e gerenciamento de docas em terminais logísticos. Desenvolvido com foco em segurança, performance e experiência do usuário.

### Principais Características

- ✅ Interface responsiva e moderna
- ✅ Tema claro/escuro
- ✅ Operações em tempo real
- ✅ Gerenciamento de agendamentos
- ✅ Relatórios e estatísticas
- ✅ Segurança reforçada contra XSS e injeções

## ✨ Funcionalidades

### 📊 Visão Geral
- Dashboard com métricas principais
- Taxa de ocupação do terminal
- Atividade recente
- Próximos agendamentos

### 🏭 Controle de Docas
- Visualização em tempo real do status das docas
- Filtros por status (Todas, Ativas, Disponíveis, Manutenção)
- Busca por nome, fornecedor ou ID do pedido
- Detalhes operacionais com timeline

### 📅 Agendamentos
- Criação de novos agendamentos
- Visualização da agenda do dia
- Status de agendamentos (Concluído, Ativo, Pendente, Confirmado)

### 📈 Relatórios
- Taxa de ocupação média
- Tempo médio de doca
- Entregas no prazo
- Desempenho por doca

### ⚙️ Configurações
- Informações do terminal
- Preferências de notificações
- Aparência (tema claro/escuro)

## 📁 Estrutura do Projeto

```
logistics-hub/
├── assets/
│   ├── css/
│   │   ├── variables.css      # Design tokens e variáveis
│   │   ├── base.css           # Reset e estilos base
│   │   ├── components.css     # Componentes reutilizáveis
│   │   ├── layout.css         # Layout e estrutura
│   │   └── main.css           # Arquivo principal (importa todos)
│   ├── js/
│   │   ├── utils/
│   │   │   ├── security.js    # Funções de segurança
│   │   │   └── helpers.js     # Funções utilitárias
│   │   ├── data/
│   │   │   └── dockData.js    # Gerenciamento de dados
│   │   ├── ui/
│   │   │   ├── renderer.js    # Funções de renderização
│   │   │   └── components.js  # Componentes interativos
│   │   └── app.js             # Aplicação principal
│   └── images/                # Imagens e assets
├── components/                # Componentes HTML reutilizáveis
├── pages/                     # Páginas adicionais
├── docs/                      # Documentação
├── index.html                 # Página principal
├── README.md                  # Este arquivo
├── LICENSE                    # Licença MIT
└── .gitignore                 # Arquivos ignorados pelo Git
```

## 🚀 Instalação

### Pré-requisitos

- Navegador moderno (Chrome, Firefox, Safari, Edge)
- Servidor web local (recomendado para desenvolvimento)

### Passos

1. **Clone o repositório**
   ```bash
   git clone https://github.com/seu-usuario/logistics-hub.git
   cd logistics-hub
   ```

2. **Inicie um servidor local**
   
   Usando Python:
   ```bash
   python -m http.server 8000
   ```
   
   Usando Node.js (http-server):
   ```bash
   npx http-server -p 8000
   ```
   
   Usando PHP:
   ```bash
   php -S localhost:8000
   ```

3. **Acesse a aplicação**
   
   Abra o navegador e acesse: `http://localhost:8000`

## 💻 Uso

### Navegação

- Use o menu lateral ou superior para navegar entre as abas
- Atalho `Ctrl + K` para focar na busca
- Atalho `ESC` para fechar modais

### Gerenciando Docas

1. **Visualizar docas**: Acesse "Controle de Docas" para ver todas as docas
2. **Filtrar**: Use as abas de filtro para ver docas por status
3. **Buscar**: Digite na barra de busca para encontrar docas específicas
4. **Ações**: Clique nos botões de ação em cada card para:
   - Atribuir caminhão
   - Colocar em manutenção
   - Marcar como disponível

### Criando Agendamentos

1. Clique no botão "Novo Agendamento"
2. Preencha os campos obrigatórios
3. Clique em "Criar Agendamento"

## 🔒 Segurança

O LogisticsHub implementa várias camadas de segurança:

### Prevenção de XSS
- Sanitização de todos os inputs do usuário
- Escape de caracteres especiais em HTML
- Uso de `textContent` ao invés de `innerHTML` quando possível

### Proteção de Dados
- Dados sensíveis não são expostos no console
- Validação de inputs antes de processamento
- Prevenção contra prototype pollution

### Headers de Segurança
- Content Security Policy (CSP)
- X-Frame-Options: DENY
- X-Content-Type-Options: nosniff
- Referrer-Policy

### Boas Práticas
- ES Modules para encapsulamento
- Validação de tipos e formatos
- Rate limiting em funções críticas

## 🛠 Tecnologias

- **HTML5** - Estrutura semântica
- **CSS3** - Estilos modernos com variáveis
- **JavaScript ES6+** - Módulos, classes, arrow functions
- **Tailwind CSS** - Framework CSS utilitário
- **Material Symbols** - Ícones
- **Inter Font** - Tipografia

## 🤝 Contribuição

Contribuições são bem-vindas! Siga os passos:

1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/nova-feature`)
3. Commit suas mudanças (`git commit -m 'Adiciona nova feature'`)
4. Push para a branch (`git push origin feature/nova-feature`)
5. Abra um Pull Request

### Diretrizes de Código

- Siga o padrão ESLint recomendado
- Escreva testes para novas funcionalidades
- Documente funções e classes
- Mantenha a compatibilidade com ES Modules

## 📝 Licença

Este projeto está licenciado sob a licença MIT - veja o arquivo [LICENSE](LICENSE) para detalhes.

## 👥 Autores

- **LogisticsHub Team** - *Desenvolvimento inicial*

## 🙏 Agradecimentos

- [Tailwind CSS](https://tailwindcss.com/) - Framework CSS
- [Google Fonts](https://fonts.google.com/) - Tipografia e ícones
- [Material Design](https://material.io/) - Sistema de design

---

<p align="center">
  Feito com ❤️ pela equipe LogisticsHub
</p>
