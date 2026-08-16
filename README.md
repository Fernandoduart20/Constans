# 🛍️ Constans - Loja Online

Este é o repositório oficial do e-commerce **Constans**, um projeto web completo e responsivo integrado ao **Supabase** para gerenciamento de produtos, clientes e pedidos em tempo real.

---

## 🚀 Funcionalidades

### 🛒 Loja Online (Cliente)
- **Navegação por Categorias:** Filtro rápido para Moda Feminina, Masculina, Fitness e Acessórios.
- **Carrinho Dinâmico:** Adição, remoção e atualização de quantidade em tempo real.
- **Integração com WhatsApp:** Finalização de pedidos enviando os itens do carrinho diretamente pelo WhatsApp.
- **Área de Usuário:** Cadastro, login e exibição personalizada do perfil do cliente.
- **Busca de Produtos:** Pesquisa instantânea por nome de item.

### ⚙️ Painel de Administração (`admin.html` + `admin.js`)
- **Gestão de Produtos:** Cadastro, listagem e exclusão de itens com links ou caminhos de imagens locais.
- **Gestão de Clientes:** Exibição em tempo real dos clientes cadastrados na plataforma.
- **Notificação de Pedidos:** Acompanhamento de vendas em tempo real via **Supabase Realtime**.

---

## 🛠️ Tecnologias Utilizadas

- **Frontend:** HTML5, CSS3 e JavaScript (Arquitetura MVC: `model.js`, `view.js`, `controller.js` e `admin.js`)
- **Backend / Banco de Dados:** Supabase (PostgreSQL)
- **Design System:** Fontes Google (*Cormorant Garamond* e *Montserrat*)

---

## 🗄️ Estrutura do Banco de Dados (Supabase)

O projeto depende de 3 tabelas principais configuradas no Supabase:

1. **`produtos`**: Armazena `id`, `nome`, `categoria`, `preco` e `img`.
2. **`clientes`**: Armazena `id`, `nome`, `email`, `telefone` e `senha`.
3. **`pedidos`**: Armazena `id`, `cliente_id`, `cliente_nome`, `itens` (JSONB) e `total`.

> 💡 **Nota:** Para o painel administrativo e a loja funcionarem perfeitamente, certifique-se de executar as queries SQL de criação de tabelas e liberar as publicações do Realtime no painel do Supabase.

---

## 📁 Estrutura de Pastas

```text
├── img/                  # Pasta para fotos de produtos e logo
├── js/
│   ├── admin.js          # Lógica do Painel do Administrador (CRUD e Realtime)
│   ├── controller.js     # Regras de negócio e rotas da loja
│   ├── model.js          # Conexão com Supabase e estado de dados
│   └── view.js           # Renderização e manipulação da DOM da loja
├── admin.html            # Painel do Administrador
├── index.html            # Interface Principal da Loja
├── login.html            # Tela de Login/Cadastro
├── style.css             # Estilização global e responsiva
└── README.md             # Documentação do projeto
