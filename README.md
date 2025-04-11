# FullStack VSCode Snippets

Uma coleção abrangente de snippets para desenvolvimento full-stack, incluindo JavaScript, Next.js, Python, Go, PHP, Docker e mais.

## Características

- JavaScript/TypeScript snippets para manipulação de arrays e objetos
- Next.js snippets para páginas, rotas API e data fetching
- Python snippets para estruturas básicas, manipulação de dados, testes e frameworks web
- Go snippets para estruturas comuns, GORM, repositories e services
- Testes em Go com suporte a unit tests, integration tests e mocks
- PHP snippets para operações básicas e OOP
- Docker snippets para Dockerfile e docker-compose
- SQL snippets para queries comuns

## Instalação

Você pode instalar esta extensão de várias formas:

### Via VS Code Marketplace

1. Abra o VS Code
2. Vá para Extensions (Ctrl+Shift+X)
3. Procure por "FullStack vscode snippets"
4. Clique em Install

### Via arquivo VSIX

```bash
# Empacota a extensão
npm run package-extension

# Instala a extensão
npm run install-extension fullstack-snippets-0.0.6.vsix
```

## Snippets Disponíveis

### JavaScript/TypeScript

| Prefixo           | Descrição                      |
| ----------------- | ------------------------------ |
| `ps-js-map`       | Cria um novo array usando map  |
| `ps-js-filter`    | Filtra elementos do array      |
| `ps-js-reduce`    | Redux array para um único valor |
| `ps-js-find`      | Encontra um elemento no array  |
| `ps-js-foreach`   | Itera sobre elementos do array |
| `ps-js-merge-obj` | Mescla objetos usando spread   |
| `ps-js-dest-obj`  | Desestruturação de objeto      |

### Python

| Prefixo               | Descrição                           |
| --------------------- | ----------------------------------- |
| `ps-py-main`          | Cria bloco principal (main)         |
| `ps-py-class`         | Cria esqueleto de classe            |
| `ps-py-func`          | Cria função com docstring           |
| `ps-py-lambda`        | Cria função lambda                  |
| `ps-py-listcomp`      | List comprehension                  |
| `ps-py-dictcomp`      | Dict comprehension                  |
| `ps-py-setcomp`       | Set comprehension                   |
| `ps-py-try`           | Bloco try-except(-finally)          |
| `ps-py-import`        | Import simples                      |
| `ps-py-fromimport`    | Import from específico              |
| `ps-py-pytest`        | Função de teste usando pytest       |
| `ps-py-unittest`      | Classe de teste usando unittest     |
| `ps-py-numpy`         | Import NumPy                        |
| `ps-py-pandas`        | Import Pandas                       |
| `ps-py-matplotlib`    | Import Matplotlib                   |
| `ps-py-dataframe`     | Criar DataFrame do Pandas           |
| `ps-py-flask`         | Aplicativo Flask básico             |
| `ps-py-fastapi`       | Aplicativo FastAPI básico           |
| `ps-py-requests`      | Exemplo de uso da biblioteca requests |

### Go - Básico

| Prefixo           | Descrição                  |
| ----------------- | -------------------------- |
| `ps-go-main`      | Cria função main           |
| `ps-go-test`      | Cria função de teste       |
| `ps-go-struct`    | Cria uma struct            |
| `ps-go-method`    | Adiciona um método a struct |
| `ps-go-interface` | Cria uma interface         |
| `ps-go-range`     | Cria slice e loop range    |

### Go - GORM & Database

| Prefixo                         | Descrição                     |
| ------------------------------- | ----------------------------- |
| `ps-go-gorm-model`              | Cria model do GORM            |
| `ps-go-gorm-connect`            | Configuração de conexão       |
| `ps-go-gorm-repository`         | Cria repository completo      |
| `ps-go-gorm-repository-interface` | Cria interface do repository  |
| `ps-go-gorm-service-interface`    | Cria interface do service     |
| `ps-go-gorm-service-impl`         | Cria implementação do service |
| `ps-go-gorm-find`                 | Busca registros               |
| `ps-go-gorm-complex`              | Query complexa                |
| `ps-go-gorm-join`                 | Query com JOIN                |

### Go - Testes

| Prefixo                      | Descrição                        |
| ---------------------------- | -------------------------------- |
| `ps-go-test-basic`           | Teste básico (Arrange-Act-Assert) |
| `ps-go-test-table`           | Teste table-driven               |
| `ps-go-test-repository`      | Testes para repository           |
| `ps-go-test-service`         | Testes para service com mocks    |
| `ps-go-test-mock-setup`      | Setup para testes com mock       |
| `ps-go-test-integration-setup` | Setup para testes de integração   |
| `ps-go-test-benchmark`       | Teste de benchmark               |
| `ps-go-test-http`            | Teste para HTTP handler          |

### PHP

| Prefixo            | Descrição            |
| ------------------ | -------------------- |
| `ps-php-php-basic` | Estrutura PHP básica |
| `ps-php-echo`      | Echo statement       |
| `ps-php-func`      | Cria função          |
| `ps-php-class`     | Cria classe          |
| `ps-php-array`     | Cria array           |
| `ps-php-foreach`   | Loop foreach         |

### Docker

| Prefixo                  | Descrição                   |
| ------------------------ | --------------------------- |
| `ps-docker-basic`        | Dockerfile básico           |
| `ps-docker-compose`      | Configuração docker-compose |
| `ps-docker-multistage`   | Dockerfile multi-stage      |
| `ps-docker-volume`       | Configuração de volume      |
| `ps-docker-network`      | Configuração de rede        |
| `ps-docker-healthcheck`  | Healthcheck do Docker       |

### SQL

| Prefixo         | Descrição             |
| --------------- | --------------------- |
| `ps-sql-select` | Query SELECT          |
| `ps-sql-insert` | Query INSERT          |
| `ps-sql-update` | Query UPDATE          |
| `ps-sql-delete` | Query DELETE          |
| `ps-sql-join`   | Query com JOIN        |
| `ps-sql-group`  | GROUP BY com HAVING   |

## Exemplos de Uso

### Python Flask API

```python
# Digite: ps-py-flask
from flask import Flask, request, jsonify

app = Flask(__name__)


@app.route('/api/users', methods=['GET'])
def get_users():
    # implementação da função
    return jsonify({"users": []})


if __name__ == '__main__':
    app.run(debug=True)
```

### Python List Comprehension e Lambda

```python
# Digite: ps-py-listcomp
filtered_data = [x * 2 for x in data if x > 0]

# Digite: ps-py-lambda
transform = lambda x: x.strip().lower()
```

### Go GORM Repository e Service

```go
// 1. Crie a interface do repository
// Digite: ps-go-gorm-repository-interface
type UserRepository interface {
    Create(user *User) error
    // ...
}

// 2. Crie a interface do service
// Digite: ps-go-gorm-service-interface
type UserService interface {
    Create(ctx context.Context, user *User) error
    // ...
}

// 3. Crie a implementação do repository
// Digite: ps-go-gorm-repository
type UserRepository struct {
    db *gorm.DB
}
// ...

// 4. Crie a implementação do service
// Digite: ps-go-gorm-service-impl
type UserServiceImpl struct {
    repo UserRepository
}
// ...

// 5. Crie os testes
// Digite: ps-go-test-service
func TestUserService(t *testing.T) {
    // ...
}
```

### Docker Compose com Healthcheck

```dockerfile
# Digite: ps-docker-compose
version: '3.8'
services:
  app:
    build:
      context: .
      dockerfile: Dockerfile
    healthcheck:
      test: ["CMD", "curl", "-f", "http://localhost:3000/health"]
      interval: 30s
      timeout: 10s
      retries: 3
```

## Desenvolvimento

```bash
# Instala dependências
npm install

# Compila
npm run compile

# Modo watch
npm run watch

# Executa testes
npm run test

# Empacota extensão
npm run package-extension
```

## Contribuindo

Contribuições são bem-vindas! Por favor, sinta-se à vontade para submeter um Pull Request.

1. Fork o repositório
2. Crie sua branch de feature (`git checkout -b feature/NovaFeature`)
3. Commit suas mudanças (`git commit -m 'Adiciona nova feature'`)
4. Push para a branch (`git push origin feature/NovaFeature`)
5. Abra um Pull Request

## Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo LICENSE para detalhes.

## Notas de Release

### 0.0.15
- Adicionado suporte para snippets Python
- Incluído exemplos de uso para Python
- Atualizada a documentação

### 0.0.14
- Adicionado snippets de testes para Go
- Adicionado suporte a GORM com repository/service pattern
- Adicionado snippets Docker e SQL
- Melhorada a organização por categorias
- Melhorada a documentação
