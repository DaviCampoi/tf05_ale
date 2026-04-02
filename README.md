# TF05 - Sistema de Monitoramento e Automação

## Aluno

* **Nome:** Davi Lucas Conteli Campoi
* **RA:** 6324300
* **Curso:** Análise e Desenvolvimento de Sistemas - 5° semestre

---

## 📌 Descrição do Projeto

Este projeto implementa um sistema completo de monitoramento de aplicações com healthchecks inteligentes, coleta de métricas, automação de deploy e scripts de manutenção.

O sistema é composto por:

* Backend em Flask (API de monitoramento)
* Banco de dados MySQL (armazenamento de métricas)
* Redis (simulado para cache)
* Dashboard web para visualização
* Scripts de automação e manutenção
* Ambiente containerizado com Docker

---

## 🚀 Funcionalidades

### ✔ Healthchecks Inteligentes

* Verificação HTTP, TCP e Database
* Endpoint `/health`
* Endpoint `/health/status`
* Endpoint `/health/all`
* Endpoint `/health/report`

### ✔ Métricas de Performance

* Tempo de resposta (response time)
* Uptime simulado
* Armazenamento no banco de dados

### ✔ Sistema de Alertas

* Alertas automáticos via console (simulado)
* Detecção de falhas em serviços (TCP e Database)

### ✔ Dashboard

* Exibição de métricas em tempo real
* Atualização automática via JavaScript
* Status dos serviços

### ✔ Automação

* Build automatizado
* Deploy com Docker
* Scripts de manutenção
* Backup e limpeza

---

## 🐳 Tecnologias Utilizadas

* Python (Flask)
* MySQL
* Redis
* Docker / Docker Compose
* JavaScript (Frontend)
* Bash (scripts)

---

## 📂 Estrutura do Projeto

```
TF05/
├── api/
│   ├── app.py
│   ├── models/
│   │   └── metrics.py
│   └── healthchecks/
│       ├── tcp_check.py
│       └── db_check.py
├── dashboard/
│   ├── index.html
│   ├── js/
│   │   └── dashboard.js
├── database/
│   └── init.sql
├── scripts/
│   ├── build.sh
│   ├── deploy.sh
│   ├── rollback.sh
│   ├── backup.sh
│   ├── cleanup.sh
│   └── health-monitor.sh
├── docker-compose.yml
└── README.md
```

---

## ⚙️ Como Executar

### 🔧 Pré-requisitos

* Docker
* Docker Compose

---

### ▶️ Subir o projeto

```bash
docker-compose up -d
```

---

### 🌐 Acessos

* **Dashboard:** http://localhost:3000
* **API:** http://localhost:5000

---

### 🔍 Testes de Healthcheck

```bash
curl http://localhost:5000/health
curl http://localhost:5000/health/status
curl http://localhost:5000/health/all
curl http://localhost:5000/metrics
```

---

## 🧪 Scripts Disponíveis

### 🔨 Build

```bash
./scripts/build.sh
```

---

### 🚀 Deploy

```bash
./scripts/deploy.sh
```

---

### 🔄 Rollback

```bash
./scripts/rollback.sh
```

---

### 💾 Backup

```bash
./scripts/backup.sh
```

---

### 🧹 Limpeza

```bash
./scripts/cleanup.sh
```

---

### ❤️ Monitoramento manual

```bash
./scripts/health-monitor.sh
```

---

## 📊 Banco de Dados

Tabela utilizada:

```sql
CREATE TABLE metrics (
    id INT AUTO_INCREMENT PRIMARY KEY,
    service VARCHAR(50),
    status VARCHAR(20),
    response_time FLOAT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

---

## 📈 Monitoramento

### Verificar status em tempo real

```bash
./scripts/health-monitor.sh
```

### Testar endpoints

```bash
curl http://localhost:5000/health/status
```

---

## ⚠️ Observações

* Redis está configurado como simulação
* Alertas estão implementados via console (modo simplificado)
* Métricas são armazenadas no banco MySQL
* O sistema pode ser expandido para alertas reais (email/webhook)

---

