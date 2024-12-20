# Jogo de Adivinhação com Flask

Este é um simples jogo de adivinhação desenvolvido utilizando o framework Flask. O jogador deve adivinhar uma senha criada aleatoriamente, e o sistema fornecerá feedback sobre o número de letras corretas e suas respectivas posições.

## Funcionalidades

- Criação de um novo jogo com uma senha fornecida pelo usuário.
- Adivinhe a senha e receba feedback se as letras estão corretas e/ou em posições corretas.
- As senhas são armazenadas utilizando base64.
- As adivinhações incorretas retornam uma mensagem com dicas.

## Requisitos

- git
- docker-compose

## Instalação

1. Clone o repositório:

   ```bash
   git clone --recurse-submodules https://github.com/larissacollossi/trabalho-1-docker
   cd trabalho-1-docker
   ```

2. Inicie o container:

   ```bash
   docker-compose up
   ```

## Como Jogar

### 1. Criar um novo jogo

Acesse a url do frontend http://localhost

Digite uma frase secreta

Envie

Salve o game-id

### 2. Adivinhar a senha

Acesse a url do frontend http://localhost

Vá para o endponint breaker

entre com o game_id que foi gerado pelo Creator

Tente adivinhar

## Estrutura do Código

### Rotas:

- **`/create`**: Cria um novo jogo. Armazena a senha codificada em base64 e retorna um `game_id`.
- **`/guess/<game_id>`**: Permite ao usuário adivinhar a senha. Compara a adivinhação com a senha armazenada e retorna o resultado.

### Classes Importantes:

- **`Guess`**: Classe responsável por gerenciar a lógica de comparação entre a senha e a tentativa do jogador.
- **`WrongAttempt`**: Exceção personalizada que é levantada quando a tentativa está incorreta.

## Melhorias Futuras

- Implementar autenticação de usuário para salvar e carregar jogos.
- Adicionar limite de tentativas.
- Melhorar a interface de feedback para as tentativas de adivinhação.

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
