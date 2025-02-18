# FullStack VSCode Snippets

A comprehensive collection of code snippets for full-stack development, including JavaScript, Next.js, Go, PHP, and Docker.

## Features

- JavaScript/TypeScript snippets for array manipulation and object handling
- Next.js specific snippets for pages, API routes, and data fetching
- Go snippets for common structures and patterns
- PHP snippets for basic operations and OOP
- Docker snippets for Dockerfile and docker-compose configurations

## Installation

You can install this extension in several ways:

### From VS Code Marketplace

1. Open VS Code
2. Go to Extensions (Ctrl+Shift+X)
3. Search for "FullStack vscode snippets"
4. Click Install

### From VSIX File

```bash
# Package the extension
npm run package-extension

# Install the extension
npm run install-extension fullstack-snippets-0.0.6.vsix
```

## Available Snippets

### JavaScript/TypeScript

| Prefix            | Description                    |
| ----------------- | ------------------------------ |
| `fs-js-map`       | Create a new array using map   |
| `fs-js-filter`    | Filter array elements          |
| `fs-js-reduce`    | Reduce array to a single value |
| `fs-js-find`      | Find an element in array       |
| `fs-js-foreach`   | Iterate over array elements    |
| `fs-js-merge-obj` | Merge objects using spread     |
| `fs-js-dest-obj`  | Object destructuring           |

### Next.js

| Prefix             | Description                     |
| ------------------ | ------------------------------- |
| `fs-next-nextpage` | Create a Next.js page component |
| `fs-next-gsp`      | Add getStaticProps function     |
| `fs-next-gspaths`  | Add getStaticPaths function     |
| `fs-next-gssp`     | Add getServerSideProps function |
| `fs-next-api`      | Create an API route             |

### Go

| Prefix            | Description                 |
| ----------------- | --------------------------- |
| `fs-go-main`      | Create main function        |
| `fs-go-test`      | Create test function        |
| `fs-go-struct`    | Create a struct             |
| `fs-go-method`    | Add a method to struct      |
| `fs-go-interface` | Create an interface         |
| `fs-go-range`     | Create slice and range loop |

### PHP

| Prefix             | Description         |
| ------------------ | ------------------- |
| `fs-php-php-basic` | Basic PHP structure |
| `fs-php-echo`      | Echo statement      |
| `fs-php-func`      | Create function     |
| `fs-php-class`     | Create class        |
| `fs-php-array`     | Create array        |
| `fs-php-foreach`   | Foreach loop        |

### Docker

| Prefix                  | Description                  |
| ----------------------- | ---------------------------- |
| `fs-docker-basic`       | Basic Dockerfile             |
| `fs-docker-compose`     | Docker Compose configuration |
| `fs-docker-multistage`  | Multi-stage Dockerfile       |
| `fs-docker-volume`      | Docker volume configuration  |
| `fs-docker-network`     | Docker network configuration |
| `fs-docker-healthcheck` | Docker healthcheck           |

## Usage Example

1. Open a file with the appropriate extension (.js, .go, .php, Dockerfile, etc.)
2. Type the snippet prefix (e.g., `fs-js-map`)
3. Press `Tab` to trigger the snippet
4. Fill in the placeholders by typing and using `Tab` to move between them

Example with JavaScript map:

```javascript
// Type fs-js-map and press Tab
const newArray = array.map((item, index) => {
  return; // resultado para cada item
});
```

## Development

```bash
# Install dependencies
npm install

# Compile
npm run compile

# Watch mode
npm run watch

# Run tests
npm run test

# Package extension
npm run package-extension
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details

## Release Notes

### 0.0.6

- Added Docker snippets
- Updated snippets organization
- Improved documentation
