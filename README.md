# 🌳 "Exploratio" Docker Compose + Apache(httpd)

Este projeto é um site estático que apresenta um portal visual e interativo sobre a **Exploração na Amazônia**, destacando pesquisas de campo, corredores ecológicos, saberes culturais e expedições reais pela maior floresta tropical do mundo.

O conteúdo é servido por um contêiner **Apache HTTPD** usando **Docker Compose**, com a pasta `/data/exploratio` montada como diretório raiz do servidor.

O site foi desenvolvido em **HTML, CSS e JavaScript puro**, totalmente responsivo, com modo claro/escuro e mapa interativo usando **Leaflet + OpenStreetMap**.

---

## 🚀 Funcionalidades

- **Layout responsivo**
- **Modo claro/escuro**
- **Seções dinâmicas**
- **Mapa interativo**
- **Formulário de contato**
- **Hospedagem containerizada**

---

## 📂 Estrutura do projeto

```
.
├── compose.yml
└── data/
    └── exploratio/
        └── index.html
```

---

## 🐳 Executando com Docker Compose

Este projeto inclui um `compose.yml` para subir um servidor Apache HTTPD e servir o site.

### 1️⃣ Pré-requisitos

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

### 2️⃣ Clonar este repositório

```bash
git clone https://github.com/ian-cunha/exploratio_docker-apache.git
cd exploratio_docker-apache-main
```

### 3️⃣ Criar a estrutura de pastas e arquivos

```bash
mkdir -p /data/exploratio
cp index.html /data/exploratio/
```

> Se preferir usar caminho relativo, crie a pasta `data/exploratio` dentro do projeto e ajuste o `compose.yml`.

### 4️⃣ Subir o contêiner

```bash
docker compose up -d
```

O site ficará disponível em:  
➡️ **<http://localhost:8080>**

### 5️⃣ Parar o contêiner

```bash
docker compose down
```
