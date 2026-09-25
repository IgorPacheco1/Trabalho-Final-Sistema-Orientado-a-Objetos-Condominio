# Sistema de Condomínio

Trabalho final da disciplina **Programação Orientada por Objetos**
PUC Minas – Campus Betim · ADS · 2º/2026
Professor: Jardell Fillipe da Silva

Sistema de console em **C# (.NET 10)** para administrar um condomínio: unidades, moradores, taxas do mês, reservas de áreas comuns e ocorrências.

---

## Integrantes

- Igor Nunes Pacheco
- Eduardo Henrick Souza Lopes
- Davi Satler Rodrigues
- Matheus Lage da Silva
- Raphael Angelo Alves

---

## O que o sistema faz

1. **Unidades e moradores**: cadastrar apartamentos, coberturas e salas comerciais e os moradores de cada uma.
2. **Taxas**: gerar a taxa do mês para todas as unidades, pagar taxas e ver quem está inadimplente.
3. **Reservas**: reservar o salão de festas, a churrasqueira ou a quadra.
4. **Ocorrências**: registrar reclamações/avisos e mudar a situação delas.

### Regras do condomínio

- A taxa é calculada de um jeito diferente para cada tipo de unidade.
- Uma área comum não pode ter duas reservas no mesmo horário.
- Unidade inadimplente (com taxa vencida) não pode reservar área comum.
- Cada área comum tem uma regra própria:
  - Salão de festas: reservar com 7 dias de antecedência
  - Churrasqueira: uso até as 22h
  - Quadra: no máximo 2 horas por reserva
- Toda ocorrência tem autor, data e situação. Ocorrência resolvida não pode mais ser alterada.


---

## Como o código está organizado

```
SistemaCondominio/
├── Program.cs          
├── Menu.cs             
├── Leitura.cs          
└── Modelos/            
    ├── Condominio.cs       
    ├── Unidade.cs          
    ├── Apartamento.cs      
    ├── Cobertura.cs        
    ├── SalaComercial.cs    
    ├── AreaComum.cs        
    ├── SalaoDeFestas.cs    
    ├── Churrasqueira.cs    
    ├── Quadra.cs           
    ├── Morador.cs
    ├── Taxa.cs
    ├── Reserva.cs
    └── Ocorrencia.cs
```