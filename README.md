# pgvector: Busca Vetorial no PostgreSQL 

Repositório destinado à demonstração prática do Seminário de Banco de Dados II (BAN2002) - Ciência da Computação, UDESC (CCT).

**Tema 02:** pgvector: PostgreSQL como Banco de Dados Vetorial para IA.

## Sobre o Projeto
Este artefato demonstra como o PostgreSQL, através da extensão `pgvector`, pode realizar buscas por similaridade semântica (Busca Vetorial). 
Foi utilizada a biblioteca `sentence-transformers` para gerar os embeddings (vetores de 384 dimensões) localmente e o operador `<->` (Distância Euclidiana) nativo do pgvector para encontrar os registros mais relevantes, mesmo sem correspondência exata de palavras.

## Como reproduzir o ambiente

**1. Subir o PostgreSQL com pgvector via Docker:**
```bash
docker run --name pgvector-demo -e POSTGRES_PASSWORD=senha_secreta -p 5432:5432 -d pgvector/pgvector:pg16
```
**2. Instalar as dependências Python:**
```python
pip install -r requirements.txt
```
**3. Executar o código:** Basta rodar o script demo_pgvector.ipynb em um ambiente Jupyter ou VSCode.

_Projeto desenvolvido para fins acadêmicos._
