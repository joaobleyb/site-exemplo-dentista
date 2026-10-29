# Lúmen Sorriso · Odontologia estética

Site de exemplo para um consultório de odontologia estética, com um vídeo que acompanha a rolagem da página.

![Lúmen Sorriso](assets/hero-ending.jpg)

> **Marca fictícia**, criada para demonstração. Imagens e vídeo gerados por IA. Depoimentos ilustrativos.

## A ideia

Esmalte de verdade é **opalescente**: levemente azulado na borda, mais quente no centro, e deixa a luz passar. Sorriso com cara de falso é o que perdeu essa luz (branco demais, opaco, grande, todos iguais). O site inteiro ensina uma coisa só: o sorriso mais bonito não é o mais branco, é o que tem luz por dentro.

## O que tem no site

- **Hero com vídeo controlado pela rolagem:** uma gota de opala cai na água e se abre em nuvem. Rolar para baixo avança o vídeo, rolar para cima volta. Quatro frases entram em sincronia com a cena.
- **"Ficou bonito. Mas parece falso.":** os três medos mais citados por pacientes.
- **Momento interativo:** segure o botão e o dente passa de branco chapado para opalescente.
- **Tratamentos, Como funciona (3 passos), Depoimentos e Dúvidas.**
- **Formulário de agendamento** com uma única chamada para ação: agendar a avaliação com prova do sorriso.

## Estrutura

```
index.html   estrutura da página
style.css    todo o visual: cores, fontes, layout e animações
script.js    vídeo na rolagem, entradas dos textos, botão de segurar e formulário
assets/      vídeo do hero, imagem inicial e final, fotos dos passos
```

HTML, CSS e JavaScript puros. Sem framework, sem build, sem dependências.

## Como ver localmente

Clone o repositório e sirva a pasta com qualquer servidor simples:

```bash
npx http-server -p 8080
```

Depois abra `http://localhost:8080` no navegador.

Abrir o `index.html` com dois cliques também funciona, mas mostra uma imagem parada no lugar do vídeo, porque o navegador bloqueia o carregamento do vídeo em arquivos locais. É o mesmo visual que celulares recebem.

## Detalhes técnicos

- O vídeo é baixado inteiro (Blob) atrás de um anel de carregamento, para a rolagem funcionar em qualquer hospedagem.
- A posição do vídeo é suavizada a cada quadro e as buscas no vídeo nunca se sobrepõem, o que deixa a rolagem lisa no Chrome.
- O vídeo foi codificado com um quadro-chave a cada 8 quadros, para responder bem a qualquer ponto da rolagem.
- Celulares, tablets em pé e quem prefere menos movimento recebem uma versão com imagem estática, sem baixar o vídeo.
- Todos os textos sobre o vídeo passaram por medição de contraste no pior quadro (mínimo 3,5:1).
- O formulário é só demonstração: mostra a mensagem de confirmação, mas não envia os dados para lugar nenhum.

## Créditos

Feito com Claude Code e a skill 10K Websites. Imagens e vídeo gerados no Higgsfield.
