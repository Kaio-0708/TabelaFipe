# Tabela Fipe

## Descrição

O projeto **Tabela Fipe** é uma aplicação Java desenvolvida utilizando o Spring Boot que permite consultar e visualizar informações de veículos com base na Tabela Fipe. A aplicação consome dados de uma API pública e oferece uma interface de linha de comando para interagir com o usuário.

### Funcionalidades

- **Consulta de Marcas:** Exibe uma lista de marcas de carros, motos e caminhões.
- **Consulta de Modelos:** Permite consultar os modelos disponíveis para uma marca selecionada.
- **Filtragem de Modelos:** Filtra os modelos com base em um trecho do nome do veículo fornecido pelo usuário.
- **Consulta de Avaliações:** Exibe avaliações dos veículos por ano, permitindo verificar as informações detalhadas.

### Estrutura do Projeto

O projeto é estruturado em várias camadas para manter a organização e a separação das responsabilidades:

- **`br.com.alura.TabelaFipe`**
  - `TabelaFipeApplication`: Classe principal que inicia a aplicação Spring Boot e executa o menu de opções.

- **`br.com.alura.TabelaFipe.service`**
  - `IConverteDados`: Interface para conversão de dados JSON para objetos Java e listas.
  - `ConverteDados`: Implementação da interface `IConverteDados`, utilizando a biblioteca Jackson para conversão de dados.
  - `ConsumoApi`: Classe responsável por consumir a API externa e retornar os dados em formato JSON.

- **`br.com.alura.TabelaFipe.principal`**
  - `Principal`: Classe principal para interação com o usuário, exibindo o menu e realizando as consultas.

- **`br.com.alura.TabelaFipe.model`**
  - `Veiculo`: Classe de modelo que representa um veículo com suas propriedades.
  - `Modelos`: Classe de modelo que contém uma lista de modelos de veículos.
  - `Dados`: Classe de modelo para dados genéricos com código e nome.

### Requisitos

- JDK 21 ou superior
- Spring Boot
- Jackson para manipulação de JSON
- API da Tabela Fipe (https://parallelum.com.br/fipe/api/v1/)

## Autor

Kaio Vitor - [GitHub](https://github.com/Kaio-0708)
