# FullStack VSCode Snippets

Uma coleção abrangente de snippets para desenvolvimento full-stack, incluindo JavaScript, Next.js, Go, PHP, Docker e mais.

## Características

- JavaScript/TypeScript snippets para manipulação de arrays e objetos
- Next.js snippets para páginas, rotas API e data fetching
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

| Prefixo           | Descrição                       |
| ----------------- | ------------------------------- |
| `fs-js-map`       | Cria um novo array usando map   |
| `fs-js-filter`    | Filtra elementos do array       |
| `fs-js-reduce`    | Reduz array para um único valor |
| `fs-js-find`      | Encontra um elemento no array   |
| `fs-js-foreach`   | Itera sobre elementos do array  |
| `fs-js-merge-obj` | Mescla objetos usando spread    |
| `fs-js-dest-obj`  | Desestruturação de objeto       |

### Go - Básico

| Prefixo           | Descrição                   |
| ----------------- | --------------------------- |
| `fs-go-main`      | Cria função main            |
| `fs-go-test`      | Cria função de teste        |
| `fs-go-struct`    | Cria uma struct             |
| `fs-go-method`    | Adiciona um método a struct |
| `fs-go-interface` | Cria uma interface          |
| `fs-go-range`     | Cria slice e loop range     |

### Go - GORM & Database

| Prefixo                           | Descrição                     |
| --------------------------------- | ----------------------------- |
| `fs-go-gorm-model`                | Cria model do GORM            |
| `fs-go-gorm-connect`              | Configuração de conexão       |
| `fs-go-gorm-repository`           | Cria repository completo      |
| `fs-go-gorm-repository-interface` | Cria interface do repository  |
| `fs-go-gorm-service-interface`    | Cria interface do service     |
| `fs-go-gorm-service-impl`         | Cria implementação do service |
| `fs-go-gorm-find`                 | Busca registros               |
| `fs-go-gorm-complex`              | Query complexa                |
| `fs-go-gorm-join`                 | Query com JOIN                |

### Go - Testes

| Prefixo                        | Descrição                         |
| ------------------------------ | --------------------------------- |
| `fs-go-test-basic`             | Teste básico (Arrange-Act-Assert) |
| `fs-go-test-table`             | Teste table-driven                |
| `fs-go-test-repository`        | Testes para repository            |
| `fs-go-test-service`           | Testes para service com mocks     |
| `fs-go-test-mock-setup`        | Setup para testes com mock        |
| `fs-go-test-integration-setup` | Setup para testes de integração   |
| `fs-go-test-benchmark`         | Teste de benchmark                |
| `fs-go-test-http`              | Teste para HTTP handler           |

### PHP

| Prefixo            | Descrição            |
| ------------------ | -------------------- |
| `fs-php-php-basic` | Estrutura PHP básica |
| `fs-php-echo`      | Echo statement       |
| `fs-php-func`      | Cria função          |
| `fs-php-class`     | Cria classe          |
| `fs-php-array`     | Cria array           |
| `fs-php-foreach`   | Loop foreach         |

### Docker

| Prefixo                 | Descrição                   |
| ----------------------- | --------------------------- |
| `fs-docker-basic`       | Dockerfile básico           |
| `fs-docker-compose`     | Configuração docker-compose |
| `fs-docker-multistage`  | Dockerfile multi-stage      |
| `fs-docker-volume`      | Configuração de volume      |
| `fs-docker-network`     | Configuração de rede        |
| `fs-docker-healthcheck` | Healthcheck do Docker       |

### SQL

| Prefixo         | Descrição           |
| --------------- | ------------------- |
| `fs-sql-select` | Query SELECT        |
| `fs-sql-insert` | Query INSERT        |
| `fs-sql-update` | Query UPDATE        |
| `fs-sql-delete` | Query DELETE        |
| `fs-sql-join`   | Query com JOIN      |
| `fs-sql-group`  | GROUP BY com HAVING |

## Exemplos de Uso

### Go GORM Repository e Service

```go
// 1. Crie a interface do repository
// Digite: fs-go-gorm-repository-interface
type UserRepository interface {
    Create(user *User) error
    // ...
}

// 2. Crie a interface do service
// Digite: fs-go-gorm-service-interface
type UserService interface {
    Create(ctx context.Context, user *User) error
    // ...
}

// 3. Crie a implementação do repository
// Digite: fs-go-gorm-repository
type UserRepository struct {
    db *gorm.DB
}
// ...

// 4. Crie a implementação do service
// Digite: fs-go-gorm-service-impl
type UserServiceImpl struct {
    repo UserRepository
}
// ...

// 5. Crie os testes
// Digite: fs-go-test-service
func TestUserService(t *testing.T) {
    // ...
}
```

### Docker Compose com Healthcheck

```dockerfile
# Digite: fs-docker-compose
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

### 0.0.6

- Adicionado snippets de testes para Go
- Adicionado suporte a GORM com repository/service pattern
- Adicionado snippets Docker e SQL
- Melhorada a organização por categorias
- Melhorada a documentação
