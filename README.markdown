# Configuração de Automação de Testes para Urban Routes - Sprint 7 TripleTen

## Visão Geral

Este projeto foi desenvolvido como parte do **Sprint 7 do Bootcamp de Análise de QA da TripleTen**. O objetivo foi estabelecer a base para a automação de testes do aplicativo **Urban Routes** usando **Python** e **Pytest**, preparando a estrutura para a implementação de testes com **Selenium** no próximo sprint. O projeto envolveu a criação de arquivos de suporte, configuração de constantes, definição de funções de teste e verificação da conectividade com o servidor do aplicativo.

## Objetivos do Projeto

- **Configurar o ambiente de automação**: Criar um ambiente virtual e organizar a estrutura do repositório com arquivos essenciais (`helpers.py`, `data.py`, `main.py`).
- **Adicionar código auxiliar**: Incluir um arquivo `helpers.py` com funções predefinidas para suporte aos testes, sem modificações.
- **Definir constantes**: Armazenar dados de teste em `data.py` para facilitar a manutenção futura.
- **Preparar funções de teste**: Criar funções vazias no `main.py` compatíveis com Pytest, prontas para receber código Selenium no Sprint 8.
- **Verificar conectividade com o servidor**: Implementar uma verificação de disponibilidade do servidor Urban Routes.
- **Preparar lógica inicial para automação**: Estruturar um ciclo para o teste de pedido de sorvetes, a ser completado no próximo sprint.

## Metodologia

1. **Tarefa 1: Criação e Commit do Arquivo `helpers.py`**:
   - Criei o arquivo `helpers.py` e colei o código auxiliar fornecido, sem modificações.
   - Realizei o commit e enviei as alterações ao repositório no GitHub.

2. **Tarefa 2: Adição de Constantes em `data.py`**:
   - Criei o arquivo `data.py` e adicionei a constante `URBAN_ROUTES_URL` com uma string vazia (`''`) para armazenar a URL do servidor.
   - Incluí as seguintes constantes com dados de teste:
     - `ADDRESS_FROM`: 'East 2nd Street, 601'
     - `ADDRESS_TO`: '1300 1st St'
     - `PHONE_NUMBER`: '+1 123 123 12 12'
     - `CARD_NUMBER`: '1234 5678 9100'
     - `CARD_CODE`: '1111'
     - `MESSAGE_FOR_DRIVER`: 'Pare no bar de sucos'

3. **Tarefa 3: Preparação do Arquivo `main.py`**:
   - Importei o módulo `data` no arquivo `main.py`.
   - Dentro da classe `TestUrbanRoutes`, defini 8 funções de teste com o prefixo `test_` para compatibilidade com Pytest:
     - `test_set_route`
     - `test_select_plan`
     - `test_fill_phone_number`
     - `test_fill_card`
     - `test_comment_for_driver`
     - `test_order_blanket_and_handkerchiefs`
     - `test_order_2_ice_creams`
     - `test_car_search_model_appears`
   - Cada função incluiu o parâmetro `self`, um comentário `#Adicionar em S8`, uma instrução `pass` e, opcionalmente, uma instrução `print` para verificação (ex.: `print("função criada para definir a rota")`).

4. **Tarefa 4: Verificação do Servidor**:
   - Importei o módulo `helpers` no `main.py`.
   - Adicionei o método especial `@classmethod def setup_class(cls)` na classe `TestUrbanRoutes`.
   - Implementei uma instrução `if` chamando a função `is_url_reachable` do `helpers.py`, passando `data.URBAN_ROUTES_URL` como parâmetro.
   - Configurei mensagens de saída:
     - Sucesso: "Conectado ao servidor Urban Routes"
     - Falha: "Não foi possível conectar ao Urban Routes. Verifique se o servidor está ligado e ainda em execução."

5. **Tarefa 5: Preparação do Teste de Pedido de Sorvetes**:
   - Na função `test_order_2_ice_creams`, adicionei um ciclo `for` usando `range(2)` para iterar duas vezes.
   - Incluí um comentário `#Adicionar em S8` e uma instrução `pass` dentro do ciclo.

6. **Documentação e Envio**:
   - Adicionei comentários apropriados nos arquivos para clareza e manutenção.
   - Verifiquei que o código executava sem erros antes do envio.
   - Enviei os arquivos ao repositório no GitHub.

## Ferramentas Utilizadas

- **Python**: Para estruturação do código de automação.
- **Pytest**: Framework de testes para compatibilidade das funções.
- **GitHub**: Para versionamento e armazenamento do repositório.
- **Urban Routes**: Aplicativo referência, com verificação de conectividade ao servidor.

## Estrutura do Repositório

- `helpers.py`: Arquivo com código auxiliar fornecido, sem modificações.
- `data.py`: Arquivo com constantes de dados de teste.
- `main.py`: Arquivo principal com a classe de testes e funções preparadas para automação.
- `README.md`: Este arquivo, descrevendo o projeto.

## Resultados

- Configurei com sucesso a estrutura inicial para automação de testes do Urban Routes, criando arquivos essenciais e organizando o repositório.
- Defini constantes em `data.py` para facilitar a manutenção de dados de teste.
- Preparei funções de teste em `main.py`, prontas para receber código Selenium no Sprint 8.
- Implementei uma verificação de conectividade com o servidor, garantindo que os testes futuros sejam executados em um ambiente funcional.
- Estruturei a lógica inicial para o teste de pedido de sorvetes, preparando o terreno para automação.

## Sobre Mim

Sou um profissional em transição de carreira para a área de Qualidade de Software, com formação no **Bootcamp de Análise de QA da TripleTen**. Minha experiência prévia em ambientes dinâmicos me proporcionou habilidades como atenção aos detalhes, organização e colaboração. Estou entusiasmado para aplicar meus conhecimentos em automação de testes e continuar evoluindo na área de tecnologia.

## Contato

- 📍 São Paulo, Brasil
- 📧 luis_commans@hotmail.com
- 🔗 https://www.linkedin.com/in/danilocommansqa
- 💻 https://github.com/MrCommans

Obrigado por visitar meu repositório! 🚖
