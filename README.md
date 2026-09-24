# Painel de Redes Sociais

Simulação de um smartphone em CSS puro, com telas de redes sociais navegáveis dentro de um `iframe` e um menu lateral de atalhos.

[![Demo](https://img.shields.io/badge/demo-online-22d3ee?style=flat-square)](https://nicolasmoreiraferreira.github.io/projeto-social/)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)

**[Acessar a demonstração](https://nicolasmoreiraferreira.github.io/projeto-social/)**

---

## Sobre o projeto

A ideia era apresentar várias telas de aplicativo em um único site, mantendo a sensação de que o
visitante está realmente usando um celular. Em vez de gerar imagens estáticas de cada tela, o
projeto monta um aparelho de verdade em CSS e carrega as telas ao vivo.

O aparelho tem moldura, alto-falante, botão físico e tela com rolagem própria. O menu lateral
direito troca qual rede social aparece no display, sem recarregar a página.

## Decisões técnicas

- **O mockup do celular é feito inteiramente em CSS.** Sem imagens do aparelho, o que mantém o
  projeto leve e permite ajustar dimensões e cores por variáveis.
- **Telas carregadas em `iframe`.** Cada rede social é um arquivo HTML independente. O menu usa
  links com `target` apontando para o frame nomeado, então a troca acontece sem recarregar a página.
- **Escalabilidade por design.** Adicionar uma rede nova significa criar um arquivo HTML e um item
  no menu — nada no layout precisa ser alterado.
- **Fundo com imagem fixa** para dar profundidade ao aparelho, ajustado para não interferir na
  leitura das telas.
- **Botão de início** que retorna à tela principal do aparelho.

## Estrutura

```
projeto-social/
├── index.html              # Mockup do celular e menu lateral
├── estilo/
│   └── style.css           # Aparelho, telas e layout geral
├── imagens/                # Ícones das redes e fundo
└── paginas-extras/         # Telas individuais carregadas no iframe
```

## Como executar

```bash
git clone https://github.com/nicolasmoreiraferreira/projeto-social.git
cd projeto-social
# Abra o arquivo index.html no navegador
```

Ou acesse a [demonstração publicada](https://nicolasmoreiraferreira.github.io/projeto-social/).

> Observação técnica: o carregamento por `iframe` funciona apenas com os arquivos servidos
> (por um servidor local ou pelo GitHub Pages). Abrir o arquivo direto pelo sistema de arquivos
> pode bloquear o carregamento dos frames por política de segurança do navegador.

## O que pratiquei

- Composição visual complexa apenas com CSS
- Organização de múltiplas páginas em um só projeto
- Uso de `iframe` com alvo nomeado (`target`) para navegação interna
- Publicação no GitHub Pages

## Licença

Distribuído sob a licença MIT. Consulte [LICENSE](LICENSE).
