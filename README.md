# Dashboard de Vendas Porsche

Dashboard interativa para explorar 100 registros de vendas Porsche. A aplicação é uma página estática em HTML, CSS e JavaScript, com filtros, indicadores, gráficos de barras e tabela detalhada.

## Links do projeto

- **Dashboard publicada:** https://dancardoso97.github.io/dashboard-vendas-porsch/
- **Repositório público:** https://github.com/Dancardoso97/dashboard-vendas-porsch

## 1. Perguntas de negócio

A dashboard foi organizada para responder a três perguntas:

1. **Qual modelo Porsche tem mais registros de venda?** A contagem por modelo ajuda a identificar quais modelos aparecem com maior frequência na base e pode apoiar conversas sobre demanda e planejamento de estoque.
2. **Qual modelo apresenta a maior receita registrada?** A soma dos preços por modelo permite comparar o valor financeiro registrado para cada modelo. É uma métrica de receita bruta registrada, não de lucro.
3. **Qual método de pagamento aparece com maior frequência?** A contagem por forma de pagamento ajuda a entender como os compradores registrados na base pagaram e pode apoiar análises operacionais.

As perguntas foram escolhidas porque cobrem três dimensões complementares: volume, valor e comportamento de pagamento. Os resultados são recalculados conforme os filtros.

## 2. Funcionalidades e filtros

A dashboard oferece filtros por:

- Modelo Porsche.
- Estado.
- Ano-modelo.
- Método de pagamento.

Também apresenta três indicadores — quantidade de registros, receita registrada e preço médio —, gráficos de vendas por modelo, receita por modelo e métodos de pagamento, respostas em destaque e uma tabela detalhada. O botão **Limpar filtros** restaura a visão completa.

## 3. Prompt de referência e refinamentos

O histórico literal do prompt que originou a primeira versão da dashboard não está armazenado neste repositório. Para transparência e reprodutibilidade, o texto abaixo é uma **reconstrução do briefing compatível com a versão final**, e não uma transcrição comprovada do prompt original:

> Crie uma dashboard interativa de vendas Porsche em um único arquivo HTML, usando os registros da base fornecida. Antes de construir os gráficos, identifique perguntas de negócio relevantes. A dashboard deve responder: (1) qual modelo tem mais registros de venda; (2) qual modelo apresenta a maior receita registrada; e (3) qual método de pagamento é mais frequente. Inclua indicadores de quantidade de registros, soma dos preços e preço médio; filtros por modelo, estado, ano-modelo e método de pagamento; gráficos de barras; uma tabela detalhada; botão para limpar os filtros; layout responsivo e identidade visual escura inspirada no universo automotivo premium. Faça os indicadores e gráficos reagirem aos filtros no navegador, sem backend ou dependências externas. Não exiba nomes, e-mails ou telefones de compradores ou vendedores. Informe que receita registrada não equivale a lucro.

### O que foi refinado na versão final

A partir do escopo refletido no código atual, a versão final contempla:

- Três perguntas de negócio explícitas na abertura da página.
- Quatro filtros interativos (modelo, estado, ano-modelo e pagamento).
- Atualização conjunta dos KPIs, gráficos, respostas em destaque e tabela.
- Botão para limpar todos os filtros.
- Formatação dos valores em dólares americanos (USD).
- Nota metodológica esclarecendo que receita não é lucro e que os totais incluem todos os status presentes na base.
- Layout responsivo e dados incorporados ao HTML para execução estática.

**Limite do registro:** como não há histórico de conversas de geração nem versões intermediárias no repositório, não é possível afirmar quantos prompts foram usados ou listar alterações literais entre cada tentativa. Os itens acima descrevem o escopo e os refinamentos observáveis no artefato final.

## 4. Tratamento e conferência da base

O repositório contém a base já incorporada como dados estruturados em JavaScript no arquivo `index.html`. O arquivo original da planilha e um script separado de preparação não estão incluídos; portanto, não é possível reconstruir com segurança todas as etapas feitas antes de os dados chegarem ao HTML.

Na inspeção da base incorporada, foram observados:

- **100 registros** e **10 campos**: ID da venda, data da venda, modelo, ano-modelo, preço, quilometragem, método de pagamento, cidade, estado e status da entrega.
- **24 datas em branco**. Esses registros foram mantidos; não foi inventada uma data para preenchê-los.
- **Nenhum ID duplicado** na base examinada.
- Preços armazenados como valores numéricos em USD e quilometragem em milhas.
- Nenhuma coluna com nome, e-mail, telefone, CPF ou CNPJ de comprador ou vendedor.

### Cuidados de interpretação

- A contagem da dashboard considera os registros existentes, inclusive status pendentes e cancelados.
- Receita registrada é a soma dos preços informados; não representa lucro nem necessariamente receita liquidada.
- O preço médio é calculado sobre os registros do recorte que possuem preço numérico.
- Datas em branco não são usadas para inferir períodos.
- Como os dados estão dentro do HTML, qualquer informação publicada nesse arquivo fica acessível a quem visitar o repositório ou a página. Não acrescente dados pessoais ou confidenciais.

## 5. Ferramentas de IA e fluxo de trabalho

Nesta etapa de documentação e publicação, foi utilizado o **ChatGPT com a integração do GitHub** para inspecionar os arquivos do repositório e atualizar este README.

Não foi utilizado Canvas nem um agente personalizado com skill para realizar essa etapa de documentação/publicação. O repositório, por si só, não registra de forma verificável qual ferramenta ou modo foi usado na criação original do HTML; por isso, não atribuo retrospectivamente a geração da dashboard ao Canvas ou a um agente específico.

## 6. Exemplo de filtro para demonstrar a interação

Para produzir uma evidência reproduzível da dashboard:

1. Abra a dashboard publicada.
2. No filtro **Modelo**, selecione `911 Turbo S`.
3. Em **Estado**, selecione `WA`.
4. Em **Ano-modelo**, selecione `2024`.
5. Em **Pagamento**, selecione `Wire Transfer`.

Na base atual, essa combinação deve retornar um registro: uma venda de 911 Turbo S em Seattle, Washington, ano-modelo 2024, com preço registrado de **US$ 235.000**. Os indicadores devem mostrar 1 registro, receita de US$ 235.000 e preço médio de US$ 235.000.

Use esse cenário para tirar uma captura de tela com os filtros e os indicadores visíveis. A captura deve ser feita no navegador, na dashboard publicada, para servir como evidência visual real. **Nenhuma captura de tela foi incluída neste repositório até o momento.**

## 7. Tecnologias

- **HTML5:** estrutura da página.
- **CSS3:** identidade visual, organização dos componentes e responsividade.
- **JavaScript:** filtros, agregações, KPIs, gráficos e tabela.
- **GitHub Pages:** hospedagem estática.

A versão atual não depende de bibliotecas externas, backend ou processo de build.

## 8. Estrutura do repositório

```text
dashboard-vendas-porsch/
├── index.html   # Dashboard, estilos, lógica e dados incorporados
└── README.md    # Documentação, metodologia e instruções
```

Todos os arquivos listados acima existem na raiz do repositório.

## 9. Como executar localmente

### Abrir diretamente

1. Clone ou baixe o repositório.
2. Abra o arquivo `index.html` em um navegador atualizado.
3. Use os filtros para explorar os dados.

### Usar um servidor local (opcional)

1. Instale o Python 3.
2. Abra o terminal na pasta do projeto.
3. Execute:

   ```bash
   python -m http.server 8000
   ```

4. Acesse http://localhost:8000.
5. Para encerrar, pressione `Ctrl + C`.

## 10. Publicação no GitHub Pages

O projeto está associado ao repositório público e ao endereço de Pages indicado no início deste README.

Para conferir ou configurar a publicação:

1. Abra https://github.com/Dancardoso97/dashboard-vendas-porsch.
2. Acesse **Settings → Pages**.
3. Em **Build and deployment**, confira a origem de publicação.
4. Se estiver usando publicação por branch, selecione `main` e `/(root)`.
5. Salve, se tiver feito alguma alteração, e aguarde o deploy.
6. Abra https://dancardoso97.github.io/dashboard-vendas-porsch/ para conferir a página.

Para atualizar a dashboard, altere `index.html` e envie o commit para a branch `main`. O GitHub Pages publicará a nova versão conforme a configuração do repositório.

## 11. Checklist antes da entrega

- [ ] Abrir o link do GitHub Pages e testar os quatro filtros.
- [ ] Aplicar o exemplo de filtro desta documentação.
- [ ] Tirar uma captura de tela real com filtros e KPIs visíveis.
- [ ] Anexar a captura ao repositório e inserir a imagem nesta documentação.
- [ ] Conferir se não há dados pessoais ou confidenciais no HTML.
- [ ] Enviar o link do repositório como endereço do código e o link do Pages como demonstração.

## Sobre o projeto

Projeto de análise e visualização de dados de vendas Porsche. Não possui vínculo oficial com a Porsche.
