# Plano de Teste QA

Este documento tem como objetivo testar a API do **Restful-Booker**.
A API volta ao seu estado original a cada 10 minutos, por isso é necessário gerar um novo token a cada 10 minutos.

---

## **Casos de Teste**

### **Cenário 01 – Autenticação**
- **CT01.1** - Gerar token de autenticação
- **CT01.2** - Tentar gerar token com credenciais inválidas

### **Cenário 02 - Gestão de reservas**
- **CT02.1** - Criar uma nova reserva 
- **CT02.2** - Buscar uma reserva específica 
- **CT02.3** - Listar todas as reservas 
- **CT02.4** - Atualizar uma reserva existente 
- **CT02.5** - Deletar uma reserva

### **Cenário 03 - Filtros e buscas**
- **CT03.1** - Buscar reservas por nome 
- **CT03.2** - Buscar reservas por data de check-in 
- **CT03.3** - Buscar reservas por data de check-out 

---
# **Evidências**

## **CT01.1 - Gerar token de autenticação**
![standard_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_32.png)
### **Status**
**Passou** ✅

## **CT01.2 - Tentar gerar token com credenciais inválidas**
### **Objetivo**
Validar se a API retorna um erro ao tentar gerar um token de autenticação com credenciais inválidas.
![standard_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_33.png)
A API não gera o token, mas retorna o status 200 OK, o que não faz sentido.
### **Status**
**Não passou** ❌

## **CT02.1** - Criar uma nova reserva 
![standard_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_34.png)
### **Status**
**Passou** ✅

## **CT02.2** - Buscar uma reserva específica 
![standard_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_35.png)
### **Status**
**Passou** ✅

## **CT02.3** - Listar todas as reservas 
![standard_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_36.png)
### **Status**
**Passou** ✅

## **CT02.4** - Atualizar uma reserva existente 
Para atualizar uma reserva, é necessário informar o token.
![standard_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_37.png)
![standard_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_38.png)
### **Status**
**Passou** ✅

## **CT02.5** - Deletar uma reserva
Para deletar uma reserva, é necessário informar o token.
![standard_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_39.png)
![standard_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_40.png)
O Status consta como "201 Created", o que não faz muito sentido quando se pensa em deletar dados.
### **Status**
**Passou** ✅

## **CT03.1** - Buscar reservas por nome 
![standard_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_41.png)
![standard_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_42.png)
### **Status**
**Passou** ✅

## **CT03.2** - Buscar reservas por data de check-in 
![standard_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_43.png)
![standard_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_44.png)
Não retorna corretamente as datas buscadas por check-in.
### **Status**
**Não passou** ❌

## **CT03.3** - Buscar reservas por data de check-out 
![standard_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_45.png)
![standard_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_46.png)
Não retorna corretamente as datas buscadas por check-out.
### **Status**
**Não passou** ❌

## **Bugs encontrados**
- Ao tentar gerar um token com credenciais inválidas, o sistema retorna 200 OK, sendo que na realidade o token não é gerado.
- Ao deletar uma reserva, o status é retornado como "201 Created", o que não faz sentido ao se deletar algo. No entanto, a reserva é deletada.
- O parâmetro de busca por check-in não está funcionando, visto que as reservas retornadas por essa busca não possuem a mesma data de check-in que foi passada no parâmetro.
- O parâmetro de busca por check-out não está funcionando, visto que as reservas retornadas por essa busca não possuem a mesma data de check-out que foi passada no parâmetro. Além disso, são listadas todas as reservas, independente de utilizar o parâmetro de check-out ou não.

### **Além dos cenários evidenciados, também foram testados valores inválidos e SQL Injection.**
---
