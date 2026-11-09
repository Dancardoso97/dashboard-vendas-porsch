# Dashboard de Vendas Porsche

Dashboard interativa para explorar registros de vendas Porsche. O projeto é uma página estática feita com HTML, CSS e JavaScript, sem dependências externas ou processo de build.

## Acesse a dashboard

**[Abrir Dashboard de Vendas Porsche](https://dancardoso97.github.io/dashboard-vendas-porsch/)**

## Sobre o projeto

A dashboard apresenta uma visão executiva dos registros de vendas, com indicadores, gráficos e tabela detalhada. Os dados são carregados a partir de uma estrutura JavaScript incorporada ao próprio arquivo `index.html` e processados localmente no navegador.

### Indicadores

- Quantidade de vendas no recorte selecionado.
- Receita registrada, calculada pela soma dos preços de venda.
- Preço médio dos registros com preço válido.

### Análises e filtros

Os filtros permitem analisar os registros por:

- Modelo Porsche.
- Estado.
- Ano-modelo.
- Método de pagamento.

Os gráficos apresentam vendas por modelo, receita por modelo e frequência dos métodos de pagamento. A dashboard também destaca o modelo com mais registros, o modelo com maior receita e o método de pagamento mais utilizado.

> **Nota:** receita registrada não é o mesmo que lucro. Para calcular lucro, seria necessário incluir os custos. Os totais consideram os registros presentes na base, inclusive registros com status pendente ou cancelado. A tabela exibe até 300 registros por vez.

## Tecnologias utilizadas

- **HTML5** — estrutura da página.
- **CSS3** — layout, tema visual e responsividade.
- **JavaScript** — filtros, cálculos, indicadores, gráficos e tabela.
- **GitHub Pages** — hospedagem estática do site.

Não é necessário instalar bibliotecas, frameworks ou pacotes para executar esta versão.

## Estrutura do projeto

```text
dashboard-vendas-porsch/
├── index.html   # Dashboard, estilos, lógica e dados incorporados
└── README.md    # Documentação do projeto
```

## Como executar localmente

### Opção 1 — Abrir diretamente

1. Faça o download ou clone este repositório.
2. Abra o arquivo `index.html` em um navegador atualizado.
3. Utilize os filtros para explorar os dados.

### Opção 2 — Usar um servidor local

Se preferir servir a página por HTTP:

1. Instale o [Python 3](https://www.python.org/) caso ainda não esteja instalado.
2. Abra o terminal na pasta do projeto.
3. Execute:

   ```bash
   python -m http.server 8000
   ```

4. Acesse [http://localhost:8000](http://localhost:8000) no navegador.
5. Para encerrar o servidor, pressione `Ctrl + C` no terminal.

## Como publicar ou atualizar no GitHub Pages

O repositório é público e a publicação utiliza o GitHub Pages. Para configurar a publicação a partir da branch principal:

1. Acesse [o repositório no GitHub](https://github.com/Dancardoso97/dashboard-vendas-porsch).
2. Abra **Settings**.
3. No menu lateral, selecione **Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch** como fonte, se essa opção estiver disponível.
5. Em **Branch**, selecione `main` e a pasta `/ (root)`.
6. Clique em **Save**.
7. Aguarde a conclusão da publicação. O endereço do site será:
   [https://dancardoso97.github.io/dashboard-vendas-porsch/](https://dancardoso97.github.io/dashboard-vendas-porsch/).

### Atualizar a dashboard

1. Edite o arquivo `index.html` mantendo os caminhos e a estrutura necessários.
2. Envie as alterações para a branch `main` (por exemplo, usando **Add file → Upload files** no GitHub).
3. Aguarde o GitHub Pages publicar a nova versão.
4. Recarregue o endereço público para conferir a atualização.

## Repositório

[Código-fonte no GitHub](https://github.com/Dancardoso97/dashboard-vendas-porsch)

## Observações sobre os dados

Os dados da dashboard estão incorporados ao arquivo `index.html` e são disponibilizados ao navegador de quem acessa o site. Não inclua informações pessoais, confidenciais ou dados que não possam ser publicados em um repositório público. A dashboard não envia os dados a um servidor: o processamento dos filtros e indicadores ocorre no navegador.

---

Projeto publicado com GitHub Pages.
