# LH_CD_JONATHANDANTASDEOLIVEIRA
Desafio INDICIUM de Cientista de Dados. Usando Machine Learning para a previsão de preços de casas em Nova York
# Projeto de Previsão de Preço de Aluguéis

# Sistema de Estimativa de Preços de Aluguéis

## Introdução

Este projeto aplica técnicas de **Machine Learning** para estimar o preço de aluguéis com base em diversos fatores, incluindo localização, tipo de acomodação e disponibilidade. A solução utiliza um **Random Forest Regressor** integrado a um **pipeline** do **scikit-learn**, permitindo um fluxo automatizado de processamento de dados.

## Configuração do Ambiente

Para executar o projeto corretamente, é recomendado criar um ambiente virtual e instalar as dependências necessárias.

### Criando o Ambiente Virtual

```bash
python -m venv venv
source venv/bin/activate  # Para Linux/macOS
venv\Scripts\activate    # Para Windows
```

### Instalando as Dependências

Se houver um arquivo `requirements.txt`, utilize o seguinte comando:

```bash
pip install -r requirements.txt
```

Caso precise instalar manualmente, execute:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

## Como Executar

Para iniciar a aplicação, execute o seguinte comando no terminal:

```bash
python pipeline_onehot_rf.py
```

Isso carregará o conjunto de dados, treinará o modelo e apresentará os resultados da previsão, incluindo gráficos e estatísticas.

## Como Fazer Previsões

Após a execução do código, você pode inserir os detalhes de um imóvel para obter uma estimativa do preço:

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

preco_estimado = prever_preco(novo_apartamento)
print(f'Valor estimado: {preco_estimado}')
```

## Visualização dos Resultados

O script gera:

- **Gráficos de dispersão** para identificar relações entre variáveis e preços.
- **Mapas de calor de correlação** para entender quais fatores impactam mais os valores dos aluguéis.

## Como Contribuir

Sugestões de melhorias no modelo ou na análise de dados são bem-vindas!

## Licença

Este projeto está licenciado sob os termos da MIT License.


