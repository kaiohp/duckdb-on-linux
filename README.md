# duckdb-on-linux

Este guia fornece um passo a passo detalhado para instalar o DuckDB em seu sistema Linux, especialmente no ambiente WSL Ubuntu.

## Instalação do DuckDB no Linux

Execute os seguintes comandos no terminal para instalar o DuckDB no seu sistema Linux:

### Passo 1: Baixar o Arquivo Binário

Use o seguinte comando para baixar o arquivo binário do DuckDB:

```bash
curl -LO https://github.com/duckdb/duckdb/releases/download/v0.9.2/duckdb_cli-linux-amd64.zip
```

Consulte a documentação oficial do [DuckDB](https://duckdb.org/docs/installation), para atualizar o link da versão no futuro.

### Passo 2: Descompactar o Arquivo

Descompacte o arquivo baixado usando o seguinte comando:

```bash
unzip duckdb_cli-linux-amd64.zip
```

> Caso não tenha a ferramenta unzip, instale-a com os seguintes comandos:
>```bash
>   sudo apt update
>   sudo apt install unzip -y
>```

### Passo 3: Mover para o Diretório de Binários

Mova o executável do DuckDB para o diretório /usr/local/bin/ com o seguinte comando:

```bash
sudo mv duckdb /usr/local/bin/
```

> Não é necessário adicionar o diretório ao arquivo .bashrc ou similares, pois a pasta /usr/local/bin/ já está no PATH.

### Passo 4: Dar Permissões de Execução

Conceda permissões de execução ao executável do DuckDB com o seguinte comando:

```bash
sudo chmod +x /usr/local/bin/duckdb
```

### Passo 5: Testar se Está Funcionando

Verifique a versão do DuckDB e execute o console do DuckDB para garantir que a instalação foi bem-sucedida:

A versão deste link é a v0.9.2 3c695d7ba9

```bash
duckdb --version
duckdb
```
