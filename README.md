# OpenAI Playground - Desafio

Este repositório contém exemplos e aprendizados da exploração do OpenAI Playground. O objetivo foi entender as configurações e parâmetros dos modelos, testar a geração de conteúdo e documentar os resultados obtidos.

## O que foi explorado

- **Parâmetros ajustados no Playground**:
  - **Temperatura**: Controla a aleatoriedade das respostas geradas.
  - **Máximo de tokens**: Limita o número de tokens na resposta.
  - **Penalidades**: Configurações para controlar repetição e presença de tokens.
  
- **Exemplos de Prompt**:
  - Com base nos parâmetros acima, fizemos testes de geração de texto, alterando a temperatura e o número máximo de tokens.

## Exemplos de Testes

1. **Testando com temperatura baixa (0.1)**:
    - **Prompt**: "Como a inteligência artificial pode ser aplicada em educação?"
    - **Resultado**: Resposta mais objetiva e direta.

2. **Testando com temperatura alta (0.9)**:
    - **Prompt**: "Como a inteligência artificial pode ser aplicada em educação?"
    - **Resultado**: Resposta mais criativa e diversificada.

## Geração de Imagens e Som

Utilizei o Playground para testar a geração de imagens e som com base em prompts criados de forma interativa.

### Scripts e Códigos

No código abaixo, apresento uma implementação para ilustrar como a interação pode ser realizada.

```python
# Exemplo de código de geração de respostas usando OpenAI Playground

import openai

# Função para gerar respostas com parâmetros configuráveis
def generate_response(prompt, temperature=0.7, max_tokens=100):
    response = openai.Completion.create(
        engine="text-davinci-003",  # Substitua com o modelo utilizado
        prompt=prompt,
        max_tokens=max_tokens,
        temperature=temperature
    )
    return response.choices[0].text.strip()

# Exemplo de uso da função
prompt = "Quais são as aplicações da inteligência artificial em negócios?"
response = generate_response(prompt, temperature=0.9, max_tokens=150)
print(response)

### **Passo 3: Código e Scripts**

Adicione os arquivos de código conforme o exemplo:

1. **Crie um arquivo Python com o código**:

Crie um arquivo chamado `openai_integration.py` com o seguinte código de exemplo:

```python
# Exemplo de código de geração de respostas usando OpenAI Playground

import openai

# Função para gerar respostas com parâmetros configuráveis
def generate_response(prompt, temperature=0.7, max_tokens=100):
    response = openai.Completion.create(
        engine="text-davinci-003",  # Substitua com o modelo utilizado
        prompt=prompt,
        max_tokens=max_tokens,
        temperature=temperature
    )
    return response.choices[0].text.strip()

# Exemplo de uso da função
prompt = "Quais são as aplicações da inteligência artificial em negócios?"
response = generate_response(prompt, temperature=0.9, max_tokens=150)
print(response)
