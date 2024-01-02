# Code Snippets

![GitHub last commit (by committer)](https://img.shields.io/github/last-commit/kevinliao852/fastapi-snippet)
![Visual Studio Marketplace Release Date](https://img.shields.io/visual-studio-marketplace/release-date/kevinliao852.fastapi-snippet)
![Visual Studio Marketplace Installs](https://img.shields.io/visual-studio-marketplace/i/kevinliao852.fastapi-snippet)
![GitHub pull requests](https://img.shields.io/github/issues-pr/kevinliao852/fastapi-snippet)
![GitHub License](https://img.shields.io/github/license/kevinliao852/fastapi-snippet)

## FastAPI Router (frt)

```python
from fastapi import APIRouter
router = APIRouter()
```

## FastAPI Get Route (frg)

```python
from fastapi import APIRouter

router = APIRouter()

@router.get("/", tags=["${1:tag}"])
async def ${2:route_name}():
    return {"message": "${3:Hello World}"}
```

## FastAPI Post Route (frp)

```python
from fastapi import APIRouter

router = APIRouter()

@router.post("/", tags=["${1:tag}"])
async def ${2:route_name}():
    return {"message": "${3:Hello World}"}
```

## FastAPI Put Route (frpu)

```python
from fastapi import APIRouter

router = APIRouter()

@router.put("/", tags=["${1:tag}"])
async def ${2:route_name}():
    return {"message": "${3:Hello World}"}
```

## FastAPI Delete Route (frd)

```python
from fastapi import APIRouter

router = APIRouter()

@router.delete("/", tags=["${1:tag}"])
async def ${2:route_name}():
    return {"message": "${3:Hello World}"}
```

## SQLAlchemy Model (sqlm)

```python
from sqlalchemy import Column, Integer, String
from sqlalchemy.ext.declarative import declarative_base

Base = declarative_base()

class ${1:ModelName}(Base):
    __tablename__ = "${2:table_name}"

    id = Column(Integer, primary_key=True, index=True)
    ${3:column_name} = Column(String)
```

## SQL Get From Model (sqlg)

```python
from sqlalchemy.orm import Session
from . import models

def ${1:func_name}(db: Session, ${2:args}):
    return db.query(models.${3:ModelName}).filter(models.${3:ModelName}.${4:column_name} == ${5:arg})
```

## SQL Create From Model (sqlc)

```python
from sqlalchemy.orm import Session
from . import models

def ${1:func_name}(db: Session, ${2:args}):
    ${3:model_name} = models.${4:ModelName}(${5:args})
    db.add(${3:model_name})
    db.commit()
    db.refresh(${3:model_name})
    return ${3:model_name}
```

## SQL Update From Model (sqlu)

```python
from sqlalchemy.orm import Session
from . import models

def ${1:func_name}(db: Session, ${2:args}):
    ${3:model_name} = db.query(models.${4:ModelName}).filter(models.${4:ModelName}.${5:column_name} == ${6:arg}).first()
    ${3:model_name}.${7:column_name} = ${8:arg}
    db.commit()
    db.refresh(${3:model_name})
    return ${3:model_name}
```

## Pydantic Model (pym)

```python
from pydantic import BaseModel

class ${1:ModelName}(BaseModel):
    ${2:column_name}: ${3:str}
```

Certainly! Here's an updated README based on the provided code snippets:

# FastAPI Snippets

This repository provides a collection of Visual Studio Code snippets for FastAPI development. These snippets can help you write FastAPI applications more efficiently.

## Snippet List

### FastAPI Router (frt)

```python
from fastapi import APIRouter
router = APIRouter()
```

### FastAPI Get Route (frg)

```python
from fastapi import APIRouter

router = APIRouter()

@router.get("/", tags=["${1:tag}"])
async def ${2:route_name}():
    return {"message": "${3:Hello World}"}
```

### FastAPI Post Route (frp)

```python
from fastapi import APIRouter

router = APIRouter()

@router.post("/", tags=["${1:tag}"])
async def ${2:route_name}():
    return {"message": "${3:Hello World}"}
```

### FastAPI Put Route (frpu)

```python
from fastapi import APIRouter

router = APIRouter()

@router.put("/", tags=["${1:tag}"])
async def ${2:route_name}():
    return {"message": "${3:Hello World}"}
```

### FastAPI Delete Route (frd)

```python
from fastapi import APIRouter

router = APIRouter()

@router.delete("/", tags=["${1:tag}"])
async def ${2:route_name}():
    return {"message": "${3:Hello World}"}
```

### SQLAlchemy Model (sqlm)

```python
from sqlalchemy import Column, Integer, String
from sqlalchemy.ext.declarative import declarative_base

Base = declarative_base()

class ${1:ModelName}(Base):
    __tablename__ = "${2:table_name}"

    id = Column(Integer, primary_key=True, index=True)
    ${3:column_name} = Column(String)
```

### SQL Get From Model (sqlg)

```python
from sqlalchemy.orm import Session
from . import models

def ${1:func_name}(db: Session, ${2:args}):
    return db.query(models.${3:ModelName}).filter(models.${3:ModelName}.${4:column_name} == ${5:arg})
```

### SQL Create From Model (sqlc)

```python
from sqlalchemy.orm import Session
from . import models

def ${1:func_name}(db: Session, ${2:args}):
    ${3:model_name} = models.${4:ModelName}(${5:args})
    db.add(${3:model_name})
    db.commit()
    db.refresh(${3:model_name})
    return ${3:model_name}
```

### SQL Update From Model (sqlu)

```python
from sqlalchemy.orm import Session
from . import models

def ${1:func_name}(db: Session, ${2:args}):
    ${3:model_name} = db.query(models.${4:ModelName}).filter(models.${4:ModelName}.${5:column_name} == ${6:arg}).first()
    ${3:model_name}.${7:column_name} = ${8:arg}
    db.commit()
    db.refresh(${3:model_name})
    return ${3:model_name}
```

### Pydantic Model (pym)

```python
from pydantic import BaseModel

class ${1:ModelName}(BaseModel):
    ${2:column_name}: ${3:str}
```

### Raise FastAPI 400 Exception (fa400)

```python
raise HTTPException(status_code=400, detail="${1:detail}")
```

### Raise FastAPI 404 Exception (fa404)

```python
raise HTTPException(status_code=404, detail="${1:detail}")
```

### Raise FastAPI 500 Exception (fa500)

```python
raise HTTPException(status_code=500, detail="${1:detail}")
```

### Raise FastAPI 401 Exception (fa401)

```python
raise HTTPException(status_code=401, detail="${1:detail}")
```

### Raise FastAPI 403 Exception (fa403)

```python
raise HTTPException(status_code=403, detail="${1:detail}")
```

### Raise FastAPI 422 Exception (fa422)

```python
raise HTTPException(status_code=422, detail="${1:detail}")
```

### Raise FastAPI 409 Exception (fa409)

```python
raise HTTPException(status_code=409, detail="${1:detail}")
```

### Raise FastAPI 405 Exception (fa405)

```python
raise HTTPException(status_code=405, detail="${1:detail}")
```

### Raise FastAPI 406 Exception (fa406)

```python
raise HTTPException(status_code=406, detail="${1:detail}")
```

### Raise FastAPI 500 Exception (fa500)

```python
raise HTTPException(status_code=500, detail="${1:detail}")
```

### Raise FastAPI 503 Exception (fa503)

```python
raise HTTPException(status_code=503, detail="${1:detail}")
```

### Raise FastAPI 501 Exception (fa501)

```python
raise HTTPException(status_code=501, detail="${1:detail}")
```

### Raise FastAPI 502 Exception (fa502)

```python
raise HTTPException(status_code=502, detail="${1:detail}")
```

### Raise FastAPI 504 Exception (fa504)

```python
raise HTTPException(status_code=504, detail="${1:detail}")
```

Feel free to use these snippets to streamline your FastAPI development process. If you have any suggestions or improvements, feel free to contribute!

---

## Compact Table of Prefixes

| Prefix | Description                 |
| ------ | --------------------------- |
| frt    | FastAPI Router              |
| frg    | FastAPI Get Route           |
| frp    | FastAPI Post Route          |
| frpu   | FastAPI Put Route           |
| frd    | FastAPI Delete Route        |
| sqlm   | SQLAlchemy Model            |
| sqlg   | SQL Get From Model          |
| sqlc   | SQL Create From Model       |
| sqlu   | SQL Update From Model       |
| pym    | Pydantic Model              |
| fa400  | Raise FastAPI 400 Exception |
| fa401  | Raise FastAPI 401 Exception |
| fa403  | Raise FastAPI 403 Exception |
| fa404  | Raise FastAPI 404 Exception |
| fa422  | Raise FastAPI 422 Exception |
| fa409  | Raise FastAPI 409 Exception |
| fa405  | Raise FastAPI 405 Exception |
| fa406  | Raise FastAPI 406 Exception |
| fa500  | Raise FastAPI 500 Exception |
| fa503  | Raise FastAPI 503 Exception |
| fa501  | Raise FastAPI 501 Exception |
| fa502  | Raise FastAPI 502 Exception |
| fa504  | Raise FastAPI 504 Exception |
