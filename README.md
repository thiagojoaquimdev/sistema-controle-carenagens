# Fairing Control System

Web-based system developed to digitalize, organize, and track the operational process of receiving, checking, and registering motorcycle fairings.

The project was developed with a focus on organization, traceability, process control, user management, and reducing manual processes.

---

## About the Project

The Fairing Control System centralizes the parts receiving workflow, allowing each stage to be tracked from delivery registration through the completion of the inventory entry.

The application allows users to register deliveries, perform physical inspections, attach fiscal documents, compare invoice information with the received items, record discrepancies, and track the complete process history.

The system also includes role-based access control, allowing different permissions to be assigned according to each user's responsibilities.

---

## Main Features

- User authentication and role-based access control
- User and permission management
- Delivery and receiving management
- Physical inspection and discrepancy tracking
- Part reference and description lookup
- Excel database integration
- Invoice (NF-e) attachment and verification
- Approval, rejection, and invoice replacement workflow
- Receiving status and process tracking
- Complete history and activity timeline
- Dashboard with operational indicators
- Search and filtering by receipt, user, status, or invoice
- Change tracking and administrator notifications

---

## Process Flow

The operational process follows these stages:

**New Delivery**

↓

**Receiving**

↓

**Physical Inspection**

↓

**Invoice Attachment**

↓

**Invoice Verification**

↓

**Approval or Rejection**

### If Approved

**Entry Completed**

↓

**Process Finalized**

### If Rejected

**Correction / Invoice Replacement**

↓

**New Verification**

---

## Access Control

The system has different user roles:

| Role | Access |
|---|---|
| Administrator | Full system access |
| Operator | Receiving and operational management |
| Inspector | Invoice and document verification |
| Supplier | New delivery registration |

Permissions can be individually configured according to each user's role.

---

## Traceability

Each receiving record has its own history, allowing the complete process to be tracked, including:

- Delivery creation
- Receiving responsible user
- Receiving start
- Physical inspection performed by the operator
- Reference and description changes
- Invoice attachment
- Invoice verification
- Approval or rejection
- Rejection reason
- Verification responsible user
- Entry completion
- Date and time of each stage

This allows the entire process to be monitored from its creation through completion.

---

## Excel Integration

The system uses an Excel database as the parts catalog.

Based on the entered part reference, the system searches the database and automatically fills in the corresponding description.

This reduces manual data entry and helps maintain consistent information throughout the system.

---

## Dashboard

The system includes a dashboard for monitoring operations within a selected period.

The dashboard displays indicators such as:

- Number of painted fairings
- Number of generated receipts
- Part references processed
- Quantities inspected
- Selected analysis period

The data can also be viewed grouped by part reference.

---

## System Interface

### Home

![Home](./screenshots/01-inicio.png)

---

### Receiving Details

![Receiving Details](./screenshots/02-detalhes-recebimento.png)

---

### Dashboard

![Dashboard](./screenshots/03-dashboard.png)

---

### New Delivery

![New Delivery](./screenshots/04-nova-entrega.png)

---

### Receive Delivery

![Receive Delivery](./screenshots/05-receber-entrega.png)

---

### Receiving Entry

![Receiving Entry](./screenshots/06-entrada-recebimento.png)

---

### Verification

![Verification](./screenshots/07-conferencia.png)

---

### Approved Entry

![Approved Entry](./screenshots/08-entrada-aprovada.png)

---

### Invoices

![Invoices](./screenshots/09-notas-fiscais.png)

---

### History

![History](./screenshots/10-historico.png)

---

### User Management

![User Management](./screenshots/11-gerenciamento.png)

---

## Technologies Used

### Languages

- Python
- HTML5
- CSS3
- JavaScript

### Technologies & Tools

- Flask
- SQLite
- OpenPyXL
- JSON

---

## Project Structure

```text
sistema-controle-carenagens/
│
├── app.py
├── carenagens.db
├── historico_fluxo.json
├── Base de Dados - Carenagens.xlsx
│
├── templates/
│   ├── login.html
│   ├── index.html
│   ├── gerenciamento.html
│   └── trocar_senha.html
│
├── nfes/
