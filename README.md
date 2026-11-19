# API Escola

API ASP.NET Core para gerenciamento de cursos (Curso, Aluno, Professor, Matrícula), usando SQL Server LocalDB.

## Como rodar a API

1. Abra a solução `API_ESCOLA_NOVO.slnx` no Visual Studio (ou use o terminal).
2. Rode com o perfil **https**:
   ```bash
   dotnet run --launch-profile https
   ```
3. A API vai responder em `https://localhost:7019` (e `http://localhost:5046`).

## Testando com o Postman

A collection do Postman fica em [`postman/Escola.postman_collection.json`](postman/Escola.postman_collection.json).

### Passo a passo para importar

1. Baixe o arquivo `postman/Escola.postman_collection.json` deste repositório
   (ou clone o repositório: `git clone https://github.com/LUCASDESENVOLVEDOR/api_pizza.git`).
2. Abra o **Postman**.
3. Clique no botão **Import**, no canto superior esquerdo (ou use `Ctrl + O`).
4. Arraste o arquivo `Escola.postman_collection.json` para a janela, ou clique em **files** e selecione o arquivo.
5. Confirme clicando em **Import**.
6. A collection **Escola** vai aparecer na aba **Collections**, na barra lateral esquerda.
7. Com a API rodando (veja acima), abra uma das requisições e clique em **Send**.

> **Erro de certificado SSL?** Se o Postman reclamar do certificado de `https://localhost:7019`, desative a verificação em
> **Settings → General → SSL certificate verification → OFF**, ou confie no certificado de desenvolvimento com
> `dotnet dev-certs https --trust`.

### Requisições disponíveis

| Nome         | Método | URL                                  | Body (JSON)                                  |
|--------------|--------|--------------------------------------|----------------------------------------------|
| Buscar Todos | GET    | `https://localhost:7019/api/curso`   | —                                            |
| ATUALIZAR    | PUT    | `https://localhost:7019/api/curso/1` | `{ "Nome": "C# 2", "CargaHoraria": 200 }`    |
