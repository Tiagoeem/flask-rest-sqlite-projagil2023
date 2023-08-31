# Exercício de Web Services REST com Flask e SQLite

Neste exercício, você aprimorará a aplicação web da biblioteca que foi desenvolvida anteriormente, agora incorporando os princípios REST até o Nível 2 do Modelo de Maturidade de Richardson. A aplicação deve continuar gerenciando livros e usuários, mas agora com uma abordagem mais padronizada e alinhada com as práticas RESTful. Além disso, você preparará seu projeto para um possível deploy no Heroku.

## Requisitos:

1. **Estrutura de Pastas**:
    - Mantenha a estrutura anterior, garantindo a presença da pasta `/db` e do arquivo principal `app.py`.

2. **Recursos e Verbos HTTP**:
    - Seus endpoints devem ser organizados em torno de recursos (por exemplo, `/livros` e `/usuarios`).
    - Utilize os verbos HTTP para representar ações CRUD sobre esses recursos: 
        - **GET** para leitura.
        - **POST** para criação.
        - **PUT** ou **PATCH** para atualização.
        - **DELETE** para exclusão.
    - Garanta que os códigos de status HTTP sejam usados de forma adequada para representar o resultado de cada operação.

3. **Endpoints RESTful**:
    - As rotas e métodos devem seguir o padrão RESTful. Por exemplo:
        - **GET** `/livros`: Lista todos os livros.
        - **POST** `/livros`: Adiciona um novo livro.
        - **GET** `/livros/1`: Obtém detalhes do livro com ID 1.
        - **PUT** `/livros/1`: Atualiza o livro com ID 1.
        - **DELETE** `/livros/1`: Exclui o livro com ID 1.
    - Siga a mesma lógica para o recurso `/usuarios`.

4. **Testando com Postman**:
    - Crie uma collection no Postman para testar todos os endpoints.
    - Após realizar os testes, exporte a collection atualizada:
        1. No Postman, clique com o botão direito na collection que você criou.
        2. Selecione "Export".
        3. Escolha a versão do formato (recomendamos a versão 2.1).
        4. Clique em "Export" e salve o arquivo na pasta `postman` do projeto.
    - **ATENÇÃO**: A exportação da collection atualizada é essencial e vale pontos. Certifique-se de substituir o arquivo existente na pasta `postman`.

5. **Preparação para Deploy no Heroku**:
    - Prepare seu repositório para um possível deploy no Heroku. Embora o deploy em si não seja necessário neste exercício, é essencial que o repositório esteja corretamente preparado para tal.
    - Adicione um arquivo `requirements.txt` contendo todas as bibliotecas e dependências necessárias para executar sua aplicação. Este arquivo é crucial para que o Heroku saiba quais pacotes instalar.
    - Crie um arquivo chamado `Procfile` (sem extensão) na raiz do seu projeto. Este arquivo é usado pelo Heroku para determinar como iniciar sua aplicação. Não se esqueça que para executar o webservice com robustez é necessario ter gunicorn em suas configurações.

## Observações:

- Ao refatorar sua aplicação para adotar os princípios REST, você estará operando no Nível 2 do Modelo de Maturidade de Richardson.
- Lembre-se de que, no Nível 2, é importante não apenas usar verbos HTTP, mas também garantir que os códigos de status HTTP sejam usados corretamente.
- Dê atenção especial à organização dos seus endpoints, garantindo que eles estejam alinhados com os princípios RESTful.
- O uso do arquivo `db_utils.py` continua opcional nesta atividade.
