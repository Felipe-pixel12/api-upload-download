# API de Upload e Download de Arquivos

## Sobre o projeto

Esta API foi desenvolvida em Python utilizando Flask. Seu objetivo é permitir o envio e o download de arquivos por meio de requisições HTTP.

A aplicação está hospedada na plataforma Render e pode ser acessada pela internet.

## Tecnologias utilizadas

- Python
- Flask
- Gunicorn
- SQLite

## URL pública

https://api-upload-download-op8i.onrender.com

## Funcionalidades

### 1. Upload de arquivos

- **Método:** POST
- **Endpoint:** `/uploads/upload`
- **Campo do arquivo:** `file`

Exemplo utilizando cURL:

```bash
curl -X POST -F "file=@teste.txt" https://api-upload-download-op8i.onrender.com/uploads/upload
```

Resposta esperada:

```json
{
  "arquivo": "teste.txt",
  "mensagem": "Arquivo salvo com sucesso!"
}
```

### 2. Download de arquivos

- **Método:** GET
- **Endpoint:** `/downloads/download/<filename>`

Exemplo:

```text
https://api-upload-download-op8i.onrender.com/downloads/download/teste.txt
```

Substitua `teste.txt` pelo nome do arquivo enviado.

## Tipos de arquivos permitidos

- PNG
- JPG
- JPEG
- GIF
- PDF
- TXT

## Como executar localmente

1. Clone o repositório:

```bash
git clone https://github.com/Felipe-pixel12/api-upload-download.git
```

2. Entre na pasta:

```bash
cd api-upload-download
```

3. Crie um ambiente virtual:

```bash
python -m venv .venv
```

4. Ative o ambiente virtual no Windows:

```powershell
.venv\Scripts\Activate.ps1
```

5. Instale as dependências:

```bash
pip install -r requirements.txt
```

6. Execute a aplicação:

```bash
python app.py
```

A API ficará disponível localmente em:

```text
http://127.0.0.1:5000
```

## Implantação

O projeto foi publicado utilizando o Render, com Gunicorn como servidor de aplicação.

Comando de inicialização:

```bash
gunicorn app:app
```

## Testes realizados

- Upload de arquivo realizado com sucesso pela URL pública.
- Download de arquivo realizado com sucesso pela URL pública.
- Aplicação publicada e disponível no Render.

## Autor

Felipe Trevisan 2°A TEC
