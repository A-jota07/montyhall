# Problema de Monty Hall — Simulação em Vue.js

> Implementação interativa do clássico *Monty Hall Problem* do curso de web moderno na udemy usando **JavaScript**, **Vue.js** e **CSS**.

---

## Descrição

Este repositório contém uma simulação visual e interativa do **Problema de Monty Hall** (o famoso problema de probabilidade envolvendo três portas, um prêmio e a escolha de manter ou trocar). O objetivo é permitir que o usuário experimente o jogo, observe estatísticas em tempo real e compreenda por que a estratégia de trocar de porta costuma ser vantajosa.

## Demonstração

* Interface interativa que permite: escolher uma porta, revelar uma porta perdedora pelo apresentador (Monty), e decidir manter ou trocar.
* Modo de simulação automática (executa várias rodadas rapidamente para mostrar resultados estatísticos).

> Se você quiser um link para uma demo hospedada (Netlify, GitHub Pages etc.), adicione o deploy e eu atualizo o README com ele.

## Principais recursos

* Implementação em **Vue.js** (componentes reativos)
* Layout e estilo com **CSS** puro (responsivo)
* Estatísticas em tempo real (contagem de vitórias por estratégia: manter vs trocar)
* Modo manual e modo automático (bulk simulation)
* Código simples e documentado para facilitar aprendizado

## Estrutura do projeto

```text
/ (root)
├─ public/                # arquivos públicos estáticos (index.html)
├─ src/
│  ├─ components/
│  │  ├─ DoorDisplay.vue         # componente de porta (estado: fechada/aberta/premiada)
│  │  ├─ GiftDisplay.vue    # Estilo do presente que aparecerá ao acertar a porta premiada
│  ├─ App.vue
│  └─ main.js
├─ package.json
├─ README.md
└─ .gitignore
```

> Ajuste o layout acima conforme a sua organização real de arquivos.

## Tecnologias

* Vue.js (2)
* JavaScript (ES6+)
* CSS (Flexbox / Grid)

## Instalação

1. Clone o repositório:

```bash
git clone https://github.com/SEU_USUARIO/SEU_REPO.git
cd SEU_REPO
```

2. Instale dependências:

```bash
npm install
# ou
yarn
```

3. Rode em modo de desenvolvimento:

```bash
npm run dev
# ou (Vue CLI)
npm run serve
```

4. Abra `http://localhost:8080` (ou a porta indicada) no seu navegador.

## Como usar

### Modo manual

1. Clique em uma das três portas para escolher.
2. O apresentador (Monty) abre uma porta vazia restante.
3. Escolha `Manter` ou `Trocar`.
4. Veja o resultado (porta com prêmio aberta) e as estatísticas atualizadas.

### Modo automático

* Ative o modo de simulação e defina o número de rodadas. O sistema executará as partidas rapidamente e atualizará as porcentagens de vitória para cada estratégia.

## Explicação rápida (por que "trocar" geralmente é melhor?)

No problema clássico com 3 portas:

* Probabilidade inicial de escolher a porta com o prêmio: **1/3**.
* Probabilidade de escolher uma porta vazia: **2/3**.

Quando Monty revela uma porta vazia (sempre possível), a chance de 2/3 fica concentrada na porta não escolhida. Portanto, **trocar** dá ~66.7% de ganhar, enquanto **manter** dá 33.3%.

## Testes e Validação

* Use o modo automático com um grande número de simulações (ex.: 10.000) para verificar empiricamente as probabilidades.
* Verifique que ao aumentar o número de rodadas, as taxas de vitória convergem para ~66.7% (trocar) e ~33.3% (manter).

## Boas práticas e melhorias sugeridas

* Adicionar animações CSS nas portas para melhorar a experiência.
* Permitir configuração de número de portas (extensão do problema clássico) para explorar variantes.
* Instrumentar testes unitários (Jest) para a lógica do jogo (funções que definem porta premiada, comportamento do Monty, atualização de estatísticas).
* Adicionar acessibilidade (aria-labels, foco por teclado).
