# Pinterest Clone

Um clone do Pinterest desenvolvido com Nuxt 3, integrando a API do Pexels para fornecer imagens de alta qualidade.

## 🚀 Tecnologias

- **[Nuxt 3](https://nuxt.com/)** - Framework Vue.js para aplicações web
- **[Vue 3](https://vuejs.org/)** - Framework JavaScript progressivo
- **[ShadcnUI](https://www.shadcn-vue.com/)** - Componentes reutilizáveis para Vue
- **[Tailwind CSS v4](https://tailwindcss.com/)** - Framework CSS utility-first
- **[Pexels API](https://www.pexels.com/api/)** - API gratuita de imagens de alta qualidade

## ✨ Funcionalidades

- 📸 Galeria de imagens em estilo masonry (grid do Pinterest)
- 🔍 Busca de imagens por palavras-chave
- 🎨 Interface responsiva e moderna
- ♾️ Scroll infinito para carregamento de mais imagens
- 🖼️ Visualização detalhada de imagens
- 💾 Navegação fluida entre páginas

## 📋 Pré-requisitos

- Node.js (versão 18 ou superior)
- npm ou yarn
- Chave de API do Pexels (gratuita)

## 🔧 Instalação

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/pinterest-clone.git
cd pinterest-clone
```

2. Instale as dependências:
```bash
npm install
```

3. Configure as variáveis de ambiente:
```bash
cp .env.example .env
```

4. Adicione sua chave da API do Pexels no arquivo `.env`:
```env
NUXT_PUBLIC_PEXELS_API_KEY=sua_chave_aqui
```

## 🎯 Como obter a API Key do Pexels

1. Acesse [Pexels API](https://www.pexels.com/api/)
2. Crie uma conta gratuita
3. Gere sua chave de API
4. Cole a chave no arquivo `.env`

## 🚀 Uso

### Desenvolvimento
```bash
npm run dev
```

O projeto estará disponível em `http://localhost:3000`

### Build para produção
```bash
npm run build
```

### Preview da build de produção
```bash
npm run preview
```

## 📁 Estrutura do Projeto

```
pinterest-clone/
├── components/         # Componentes Vue reutilizáveis
│   └── ui/             # Componentes ShadcnUI
├── pages/              # Páginas da aplicação
├── composables/        # Composables do Vue
├── assets/             # Arquivos estáticos (CSS, imagens)
├── public/             # Arquivos públicos
├── app.vue             # Componente raiz
└── nuxt.config.ts      # Configuração do Nuxt
```

## 🎨 Componentes Principais

- **Sidebar**: Sidebar
- **ImageGrid**: Grid masonry para exibição das imagens
- **SearchBar**: Barra de busca de imagens
- **ImageCard**: Card individual de cada imagem
- **ImageModal**: Modal para visualização detalhada

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 🤝 Contribuindo

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e pull requests.

## 👨‍💻 Autor

Jorge Vinicius - [@J-Vinicius](https://github.com/J-Vinicius)

## 🙏 Agradecimentos

- [Pexels](https://www.pexels.com/) por fornecer a API gratuita de imagens.
- [Nuxt](https://nuxt.com/) pela excelente documentação.
- [ShadcnUI](https://www.shadcn-vue.com/) pelos componentes elegantes.