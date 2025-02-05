# LH_CD_JONATHANDANTASDEOLIVEIRA
Desafio INDICIUM de Cientista de Dados. Usando Machine Learning para a previsão de preços de casas em Nova York
# Projeto de Previsão de Preço de Aluguéis

## Visão Geral
Este projeto utiliza **Machine Learning** para prever o preço de aluguéis baseando-se em diversas variáveis, como localização, tipo de acomodação e disponibilidade.
A implementação usa um **Random Forest Regressor** dentro de um **pipeline** do **scikit-learn**, garantindo um processamento automatizado de dados.

## Instalação
Antes de rodar o projeto, instale os pacotes necessários.
Recomenda-se o uso de um ambiente virtual:

```bash
python -m venv venv
source venv/bin/activate  # Para Linux/macOS
venv\Scripts\activate    # Para Windows
```

Em seguida, instale as dependências:

```bash
pip install -r requirements.txt
```

Caso não tenha um arquivo `requirements.txt`, instale os pacotes manualmente:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

## Execução
Para rodar o projeto, basta executar o script Python principal:

```bash
python pipeline_onehot_rf.py
```

Isso irá carregar o dataset, treinar o modelo e exibir os resultados da previsão, incluindo análises visuais como scatter plots e heatmaps.

## Como Prever o Preço de um Novo Apartamento
Após rodar o script, você pode inserir as características de um novo apartamento para prever seu preço:

```python
novo_apartamento = {
    'id': 2595,
    'nome': 'Skylit Midtown Castle',
    'host_id': 2845,
    'host_name': 'Jennifer',
    'bairro_group': 'Manhattan',
    'bairro': 'Midtown',
    'latitude': 40.75362,
    'longitude': -73.98377,
    'room_type': 'Entire home/apt',
    'minimo_noites': 1,
    'numero_de_reviews': 45,
    'ultima_review': '2019-05-21',
    'reviews_por_mes': 0.38,
    'calculado_host_listings_count': 2,
    'disponibilidade_365': 355
}

preco_sugerido = prever_preco(novo_apartamento)
print(f'Preço sugerido: {preco_sugerido}')
```

## Visualização dos Resultados
O script gera:
- **Scatter plots** para entender a relação entre as variáveis e o preço.
- **Heatmaps de correlação** para identificar quais variáveis têm maior impacto no preço.

## Contribuição
Sinta-se à vontade para contribuir com melhorias no modelo ou análise dos dados!

## Licença
Este projeto está sob a licença MIT.

