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


## Tips and tricks

### Add dependencies
```
uv add lib_1 [lib_n]
```
- install dependencies to virtual environment
- to show dependency tree: `uv tree`
- `uv remove lib_1` 
