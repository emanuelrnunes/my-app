# my-app — Navegação em React Native

**Aluno:** Emanuel Ribeiro Ferreira Nunes e Souza

Aplicativo desenvolvido em React Native com Expo para demonstrar três padrões de navegação usando React Navigation:

- **Stack:** navegação em pilha entre Início e Produtos.
- **Bottom Tabs:** abas inferiores para Início, Produtos, Perfil e Configurações, com badge de notificação na aba Produtos.
- **Drawer:** menu lateral com as mesmas quatro seções, acessível pelo botão do cabeçalho ou por gesto a partir da borda.

## Requisitos

- Node.js compatível com o Expo SDK 54
- npm

## Como executar

1. Extraia ou clone este repositório.
2. No terminal, entre na pasta do projeto.
3. Instale as dependências:

   ```bash
   npm install
   ```

4. Inicie o Expo:

   ```bash
   npx expo start
   ```

Para limpar o cache se houver problemas:

```bash
npx expo start --clear
```

## Como alternar os modos

Abra `src/routes/index.jsx` e altere somente a constante `TIPO_DE_NAVEGACAO`:

```js
const TIPO_DE_NAVEGACAO = "stack";  // pilha
const TIPO_DE_NAVEGACAO = "bottom"; // abas inferiores
const TIPO_DE_NAVEGACAO = "drawer"; // menu lateral
```

Deixe **apenas uma** dessas declarações ativa por vez: substitua o valor da linha existente, sem criar três constantes.

## Capturas de tela

Adicione suas próprias capturas após executar e testar cada modo. Salve os arquivos na pasta `screenshots/` com estes nomes e descomente os trechos correspondentes:

- `screenshots/stack.png` — Home e Product/retorno.
- `screenshots/bottom.png` — as quatro abas e o badge vermelho com o número 3.
- `screenshots/drawer.png` — menu lateral aberto mostrando os quatro itens.

<!--
Quando as capturas estiverem na pasta screenshots/, substitua esta seção por:

### Stack
![Modo Stack](screenshots/stack.png)

### Bottom Tabs
![Modo Bottom Tabs](screenshots/bottom.png)

### Drawer
![Modo Drawer](screenshots/drawer.png)
-->

## Estrutura principal

```text
src/
├── App.jsx
├── components/
├── routes/
│   ├── index.jsx
│   ├── StackRoutes.jsx
│   ├── BottomRoutes.jsx
│   └── DrawerRoutes.jsx
└── screens/
    ├── Home.jsx
    ├── Product.jsx
    ├── Profile.jsx
    └── Settings.jsx
```
