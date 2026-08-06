# Brasileiro Psi

Site de **Priscila Brasileiro** — Psicóloga · CRP 05/51361
Psicoterapia online. Diagnóstico tardio e neurodivergência na vida adulta.

🔗 [brasileiropsi.com.br](https://brasileiropsi.com.br) · [@psipriscilabrasileiro](https://www.instagram.com/psipriscilabrasileiro/) · [Psico das Pretas](https://psicodaspretas.com.br)

---

## O que é

Site estático de uma página só, com navegação em cinco abas. Sem framework, sem build, sem dependência: é HTML, CSS e um pouco de JavaScript num arquivo único. Para publicar, basta subir os arquivos.

**As cinco abas**

| Aba | Endereço | Função |
|---|---|---|
| Início | `#inicio` | Reconhecimento, para quem é, e a diferença entre as duas casas |
| Diagnóstico tardio | `#neuro` | A especialidade. É a página que o Google encontra |
| Sobre mim | `#sobre` | Trajetória, território, abordagem e formação |
| Como funciona | `#processo` | O processo passo a passo e as condições práticas |
| Perguntas | `#perguntas` | As oito perguntas que mais chegam no WhatsApp |

Cada aba tem endereço próprio: `brasileiropsi.com.br/#neuro` abre direto na página de diagnóstico tardio. Serve para mandar o link certo para a pessoa certa.

## Arquivos

```
index.html                    todo o site — estrutura, estilo e comportamento
preview.jpg                   imagem que aparece ao compartilhar o link
CNAME                         domínio personalizado (só para GitHub Pages)
README.md                     este arquivo
img/
  priscila-retrato.jpg        abertura, 1200×1800
  priscila-retrato-sm.jpg     mesma foto em 700px, para celular
  priscila-mar.jpg            aba Sobre mim
  priscila-consultorio.jpg    aba Sobre mim, seção Formação
  priscila-contato.jpg        painel de contato
  priscila-respira.jpg        seção "Terapia não é luxo. É chão."
```

A abertura carrega ~570 KB (site + retrato). As outras fotos só baixam quando a pessoa chega nelas.

## Como mexer nas coisas

Tudo está em `index.html`. Abra num editor de texto e procure pelo trecho indicado.

**Trocar o número do WhatsApp** — procure `const ZAP` (perto do fim do arquivo):

```js
const ZAP = '5521980142421';
```

Logo abaixo está o objeto `MSG`, com a mensagem que já vem escrita conforme a página de onde a pessoa clicou. Serve para saber por onde ela entrou antes de responder.

**Acrescentar as formações em neurodivergência** — procure `FORMACOES_NEURO`. Substitua o comentário por itens no mesmo formato dos que já estão lá:

```html
<li><b>Nome da formação.</b> Instituição, ano.</li>
```

**Trocar uma foto** — substitua o arquivo em `img/` mantendo o mesmo nome. Proporção 2:3 para o retrato da abertura, 3:4 para as demais.

**Cores e tipografia** — no topo do `<style>`, em `:root`. Paleta: areia, papel, mar, céu, folha, tinta. Fontes: Fraunces (títulos) e Crimson Pro (texto).

## O que este site deliberadamente não tem

Não são esquecimentos. São limites do Código de Ética Profissional do Psicólogo e da LGPD:

- **Nenhum preço em nenhuma página.** O CFP permite informar valor quando perguntado, mas proíbe usá-lo como propaganda (CEPP Art. 20). O valor vai na primeira resposta do WhatsApp.
- **Nenhum depoimento de paciente**, nem anonimizado. Nota Técnica CFP 1/2022 orienta não usar nem com consentimento.
- **Nenhuma promessa de resultado.** Vedação do Art. 20, "e".
- **Nenhum formulário.** Campo aberto pedindo que a pessoa conte o caso é coleta de dado de saúde antes de qualquer vínculo. O site manda direto para o WhatsApp, onde a conversa já está sob sigilo profissional.
- **Nome, título e CRP** visíveis no topo e no rodapé de todas as abas, como o Art. 20 exige.

**Sobre política de privacidade:** hoje não é necessária, porque o site não coleta nada — sem formulário, sem cookie, sem analytics. Ela passa a ser obrigatória no momento em que entrar qualquer uma destas quatro coisas: formulário de contato, Google Analytics, chat embutido ou **pixel da Meta** (necessário para anúncios com retargeting).

## O que nunca deve entrar neste repositório

Este repositório é público. Nada de material clínico, de pesquisa ou interno vem para cá — em especial dados da escuta territorial, prontuários, documentos de estratégia e qualquer arquivo com informação de paciente. Dado de saúde é dado sensível pela LGPD (Art. 11).

## Publicação

Site estático: qualquer hospedagem serve. No GitHub Pages, ative em *Settings → Pages* apontando para a branch principal, na raiz. O arquivo `CNAME` cuida do domínio personalizado — se a hospedagem não for o GitHub Pages, ele pode ser removido.

---

<sub>Arquitetura e desenvolvimento: François R. Vargas Ozanne · Ozanne Consultoria<br>
Conteúdo: Priscila Brasileiro. Nenhuma alteração de texto clínico sem revisão dela.</sub>
