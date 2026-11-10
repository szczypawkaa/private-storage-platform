# Backend

## Development Guide
### 1. Running the Application
```bash
uv run fastapi dev
```
- `dev` - development mode

### 2. Testing
```bash
uv run pytest
```
- `-v` - verbose output
- `--collect-only` - dry-run

### 3. Test Coverage
#### Generate Coverage Report
```bash
uv run coverage run -m pytest
uv run coverage report
```
#### Show Missing Lines
```bash
uv run coverage report -m
```

### 4. Linting and formatting
```
uv run ruff check --fix
```
```
uv run ruff format
```

## Tips and tricks

### Add dependencies
```
uv add lib_1 [lib_n]
```
- install dependencies to virtual environment
- add to dependecy group: `uv add --dev lib_1`
- to show dependency tree: `uv tree`
- `uv remove lib_1` 

### Run in container
```
docker build -t backend .
docker run -d --name mycontainer -p 8080:8080 backend
```