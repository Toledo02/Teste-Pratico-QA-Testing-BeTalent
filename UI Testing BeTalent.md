# Plano de Teste QA

Este documento tem como objetivo testar a plataforma de e-commerce **Sauce Demo**.

---

## **Casos de Teste**

### **Cenário 01 – Login com diferentes tipos de usuários disponíveis**
- **CT01.1** – Login com usuário `standard_user`
- **CT01.2** – Login com usuário `locked_out_user`
- **CT01.3** – Login com usuário `problem_user`
- **CT01.4** – Login com usuário `performance_glitch_user`
- **CT01.5** – Login com usuário `error_user`
- **CT01.6** – Login com usuário `visual_user`
- **CT01.7** – Login com usuário válido e senha inválida
- **CT01.8** – Login com usuário inválido e senha válida
- **CT01.9** – Login com usuário e senha inválidos
- **CT01.10** – Login com usuário e senha em branco

### **Cenário 02 – Ordenação e filtragem de produtos**
- **CT02.1** – Validar a ordenação e filtragem para o usuário `standard_user`
- **CT02.2** – Validar a ordenação e filtragem para o usuário `problem_user`
- **CT02.3** – Validar a ordenação e filtragem para o usuário `performance_glitch_user`
- **CT02.4** – Validar a ordenação e filtragem para o usuário `error_user`
- **CT02.5** – Validar a ordenação e filtragem para o usuário `visual_user`

### **Cenário 03 – Fluxo completo de compra**
- **CT03.1** – Realizar uma compra com o usuário `standard_user`
- **CT03.1** – Realizar uma compra com o usuário `problem_user`
- **CT03.1** – Realizar uma compra com o usuário `performance_glitch_user`
- **CT03.1** – Realizar uma compra com o usuário `error_user`
- **CT03.1** – Realizar uma compra com o usuário `visual_user`

### **Cenário 04 – Remoção de itens do carrinho**
- **CT04.1** – Remover itens do carrinho com o usuário `standard_user`
- **CT04.2** – Remover itens do carrinho com o usuário `problem_user`
- **CT04.3** – Remover itens do carrinho com o usuário `performance_glitch_user`
- **CT04.4** – Remover itens do carrinho com o usuário `error_user`
- **CT04.5** – Remover itens do carrinho com o usuário `visual_user`

### **Cenário 05 – Logout**
- **CT05.1** – Validar o logout para o usuário `standard_user`
- **CT05.2** – Validar o logout para o usuário `problem_user`
- **CT05.3** – Validar o logout para o usuário `performance_glitch_user`
- **CT05.4** – Validar o logout para o usuário `error_user`
- **CT05.5** – Validar o logout para o usuário `visual_user`

---

## **Evidências**

## **CT01.1** – Login com usuário `standard_user`
### **Objetivo**
Garantir que o sistema permita login com credenciais válidas.
### **Procedimento**
    Dado que acesso a página "https://www.saucedemo.com/"
    Quando insiro o username "standard_user"
    E insiro a senha "secret_sauce"
    E aperto o botão "Login"
    Então posso ver a página inicial com os dados corretos
### **Dados de Teste**
Nome de usuário: `standard_user`
Senha: `secret_sauce`
![standard_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_1.png)
**Resultado esperado:** acessar a página "inventory.html" e visualizar os itens corretamente
**Resultado obtido:**
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Homepage.png)
### **Status**
**Passou** ✅ 

## **CT01.2** – Login com usuário `locked_out_user` 
### **Objetivo**
Garantir que o sistema não permita login para usuários bloqueados. 
### **Procedimento**
    Dado que acesso a página "https://www.saucedemo.com/"
    Quando insiro o username "locked_out_user" 
    E insiro a senha "secret_sauce"
    E aperto o botão "Login"
    Então vejo uma mensagem indicando que meu usuário está bloqueado 
### **Dados de Teste**
Nome de usuário: `locked_out_user` 
Senha: `secret_sauce`
![locked_out_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_2.png)
**Resultado esperado:** mensagem informando que o usuário está impedido de acessar o site
**Resultado obtido:**
![locked_out_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_3.png)
### **Status**
**Passou** ✅

## **CT01.3** – Login com usuário `problem_user`  
### **Objetivo**
Validar se o usuário consegue acessar e visualizar o site corretamente.  
### **Procedimento**
    Dado que acesso a página "https://www.saucedemo.com/"
    Quando insiro o username "problem_user"  
    E insiro a senha "secret_sauce"
    E aperto o botão "Login"
    Então posso ver a página inicial com os dados corretos
### **Dados de Teste**
Nome de usuário: `problem_user`  
Senha: `secret_sauce`
![problem_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_4.png)
**Resultado esperado:** acessar a página "inventory.html" e visualizar os itens corretamente
**Resultado obtido:**
![problem_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_5.png)
As imagens estão incorretas.
### **Status**
**Não passou** ❌

## **CT01.4** – Login com usuário `performance_glitch_user`
### **Objetivo**
Validar se o usuário consegue acessar e visualizar o site corretamente.  
### **Procedimento**
    Dado que acesso a página "https://www.saucedemo.com/"
    Quando insiro o username "performance_glitch_user"  
    E insiro a senha "secret_sauce"
    E aperto o botão "Login"
    Então posso ver a página inicial com os dados corretos
### **Dados de Teste**
Nome de usuário: `problem_user`  
Senha: `secret_sauce`
![performance_glitch_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_6.png)
**Resultado esperado:** acessar a página "inventory.html" e visualizar os itens corretamente
**Resultado obtido:**
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Homepage.png)
No entanto, algumas funcionalidades não respondem e há muita lentidão ao serem executadas.
### **Status**
**Passou** ✅

## **CT01.5** – Login com usuário `error_user`
### **Objetivo**
Validar se o usuário consegue acessar e visualizar o site corretamente.
### **Procedimento**
    Dado que acesso a página "https://www.saucedemo.com/"
    Quando insiro o username "error_user"  
    E insiro a senha "secret_sauce"
    E aperto o botão "Login"
    Então posso ver a página inicial com os dados corretos
### **Dados de Teste**
Nome de usuário: `error_user`  
Senha: `secret_sauce`
![performance_glitch_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_7.png)
**Resultado esperado:** acessar a página "inventory.html" e visualizar os itens corretamente
**Resultado obtido:**
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Homepage.png)
No entanto, o filtro não está funcionando para esse usuário.
### **Status**
**Passou** ✅

## **CT01.6** – Login com usuário `visual_user`
### **Objetivo**
Validar se o usuário consegue acessar e visualizar o site corretamente.
### **Procedimento**
    Dado que acesso a página "https://www.saucedemo.com/"
    Quando insiro o username "visual_user"  
    E insiro a senha "secret_sauce"
    E aperto o botão "Login"
    Então posso ver a página inicial com os dados corretos
### **Dados de Teste**
Nome de usuário: `visual_user`  
Senha: `secret_sauce`
![performance_glitch_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_8.png)
**Resultado esperado:** acessar a página "inventory.html" e visualizar os itens corretamente
**Resultado obtido:**
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_9.png)
Imagens, formatação e valores incorretos. Necessário correção.
### **Status**
**Não passou** ❌

## **CT01.7** – Login com usuário válido e senha inválida
### **Objetivo**
Validar se o sistema trava o login e exibe mensagem informando que a senha é inválida.
### **Procedimento**
    Dado que acesso a página "https://www.saucedemo.com/"
    Quando insiro o username "standard_user"  
    E insiro a senha "1234"
    E aperto o botão "Login"
    Então o sistema barra o login 
    E informa que a senha é inválida
### **Dados de Teste**
Nome de usuário: `standard_user`  
Senha: `1234`
![performance_glitch_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_10.png)
**Resultado esperado:** o sistema trava o login e exibe mensagem informando que a senha é inválida.
**Resultado obtido:**
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_11.png)
O login não é efetuado e é exibida uma mensagem informando que o login e senha não correspondem a nenhum usuário cadastrado.
### **Status**
**Passou** ✅

## **CT01.8** – Login com usuário inválido e senha válida
### **Objetivo**
Validar se o sistema trava o login e exibe mensagem informando que a senha é inválida.
### **Procedimento**
    Dado que acesso a página "https://www.saucedemo.com/"
    Quando insiro o username "user"  
    E insiro a senha "secret_sauce"
    E aperto o botão "Login"
    Então o sistema barra o login 
    E informa que o login é inválido
### **Dados de Teste**
Nome de usuário: `user`  
Senha: `secret_sauce`
![performance_glitch_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_10.png)
**Resultado esperado:** o sistema trava o login e exibe mensagem informando que a senha é inválida.
**Resultado obtido:**
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_11.png)
O login não é efetuado e é exibida uma mensagem informando que o login e senha não correspondem a nenhum usuário cadastrado.
### **Status**
**Passou** ✅

## **CT01.9** – Login com usuário e senha inválidos
### **Objetivo**
Validar se o sistema trava o login e exibe mensagem informando que o login e a senha são inválidos.
### **Procedimento**
    Dado que acesso a página "https://www.saucedemo.com/"
    Quando insiro o username "user"  
    E insiro a senha "1234"
    E aperto o botão "Login"
    Então o sistema barra o login 
    E informa que o login e a senha são inválidos
### **Dados de Teste**
Nome de usuário: `user`  
Senha: `1234`
![performance_glitch_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_13.png)
**Resultado esperado:** o sistema trava o login e exibe mensagem informando que o login e a senha são inválidos.
**Resultado obtido:**
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_14.png)
O login não é efetuado e é exibida uma mensagem informando que o login e senha não correspondem a nenhum usuário cadastrado.
### **Status**
**Passou** ✅

## **CT01.10** – Login com usuário e senha em branco
### **Objetivo**
Validar se o sistema trava o login e exibe mensagem informando que o login e a senha são inválidos.
### **Procedimento**
    Dado que acesso a página "https://www.saucedemo.com/"
    Quando insiro o username ""  
    E insiro a senha ""
    E aperto o botão "Login"
    Então o sistema barra o login 
    E informa que o login é inválido
### **Dados de Teste**
Nome de usuário: null
Senha: null
![performance_glitch_user](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_15.png)
**Resultado esperado:** o sistema trava o login e exibe mensagem informando que o login e a senha são inválidos.
**Resultados obtidos:**
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_16.png)
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_17.png)
O login não é efetuado e é exibida uma mensagem informando que o login e a senha são necessários.
### **Status**
**Passou** ✅

## **CT02.1** – Validar a ordenação e filtragem para o usuário `standard_user`
### **Objetivo**
Validar se o filtro por nome e por preço está funcionando corretamente.
### **Procedimento**
    Dado que estou logado na página "https://www.saucedemo.com/" como "standard_user"
    Quando seleciono o tipo de filtro
    Então os itens são listados de acordo com o filtro selecionado
### **Dados de Teste**
Filtros: Name (A to Z), Name (Z to A), Price (low to high) e Price (high to low)

**Resultado esperado:** os itens são listados de acordo com o filtro selecionado
**Resultados obtidos:**
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_18.png)
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_19.png)
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_20.png)
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_21.png)
Os itens são ordenados de acordo com os filtros selecionados.
### **Status**
**Passou** ✅

## **CT02.2** – Validar a ordenação e filtragem para o usuário `problem_user`
### **Objetivo**
Validar se o filtro por nome e por preço está funcionando corretamente.
### **Procedimento**
    Dado que estou logado na página "https://www.saucedemo.com/" como "problem_user"
    Quando seleciono o tipo de filtro
    Então os itens são listados de acordo com o filtro selecionado
### **Dados de Teste**
Filtros: Name (A to Z), Name (Z to A), Price (low to high) e Price (high to low)

**Resultado esperado:** os itens são listados de acordo com o filtro selecionado
**Resultados obtidos:**
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_22.png)
Os itens não são alterados de acordo com o filtro selecionado.
### **Status**
**Não passou** ❌

## **CT02.3** – Validar a ordenação e filtragem para o usuário `performance_glitch_user`
### **Objetivo**
Validar se o filtro por nome e por preço está funcionando corretamente.
### **Procedimento**
    Dado que estou logado na página "https://www.saucedemo.com/" como "performance_glitch_user"
    Quando seleciono o tipo de filtro
    Então os itens são listados de acordo com o filtro selecionado
### **Dados de Teste**
Filtros: Name (A to Z), Name (Z to A), Price (low to high) e Price (high to low)

**Resultado esperado:** os itens são listados de acordo com o filtro selecionado
**Resultados obtidos:**
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_18.png)
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_19.png)
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_20.png)
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_21.png)
Os itens são ordenados de acordo com os filtros selecionados, mas há lentidão ao selecionar os filtros.
### **Status**
**Passou** ✅

## **CT02.4** – Validar a ordenação e filtragem para o usuário `error_user`
### **Objetivo**
Validar se o filtro por nome e por preço está funcionando corretamente.
### **Procedimento**
    Dado que estou logado na página "https://www.saucedemo.com/" como "error_user"
    Quando seleciono o tipo de filtro
    Então os itens são listados de acordo com o filtro selecionado
### **Dados de Teste**
Filtros: Name (A to Z), Name (Z to A), Price (low to high) e Price (high to low)

**Resultado esperado:** os itens são listados de acordo com o filtro selecionado
**Resultados obtidos:**
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_23.png)
É retornada uma mensagem informando que o filtro não está funcionando.
### **Status**
**Não passou** ❌

## **CT02.5** – Validar a ordenação e filtragem para o usuário `visual_user`
### **Objetivo**
Validar se o filtro por nome e por preço está funcionando corretamente.
### **Procedimento**
    Dado que estou logado na página "https://www.saucedemo.com/" como "visual_user"
    Quando seleciono o tipo de filtro
    Então os itens são listados de acordo com o filtro selecionado
### **Dados de Teste**
Filtros: Name (A to Z), Name (Z to A), Price (low to high) e Price (high to low)

**Resultado esperado:** os itens são listados de acordo com o filtro selecionado
**Resultados obtidos:**
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_24.png)
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_25.png)
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_26.png)
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_27.png)
O filtro por ordem alfabética está funcional, porém o filtro de preço não está funcionando, visto que os itens são ordenados de forma aleatória. Além disso, os valores estão incorretos e a imagem do item "Sauce Labs Fleece Jacket" está incorreta.
### **Status**
**Não passou** ❌

## **CT03.1** – Realizar uma compra com o usuário `standard_user`
### **Objetivo**
Realizar a compra de um item no site.
### **Procedimento**
    Dado que estou logado na página "https://www.saucedemo.com/" como "standard_user"
    Quando adiciono o item "Sauce Labs Bolt T-Shirt" ao carrinho
    E seleciono o carrinho
    E aperto o botão "Checkout"
    E informo os dados de nome de endereço
    E aperto o botão "Continue"
    E aperto o botão "Finish"
    Então vejo uma mensagem de confirmação do pedido
### **Dados de Teste**
First name: Gustavo
Last name: Toledo
Zip/Postal Code: 12345678

**Resultado esperado:** é exibida uma mensagem informando que o pedido foi confirmado.
**Resultados obtidos:**
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_28.png)
É retornada uma mensagem informando que o pedido foi confirmado.
### **Status**
**Passou** ✅

## **CT03.2** – Realizar uma compra com o usuário `problem_user`
### **Objetivo**
Realizar a compra de um item no site.
### **Procedimento**
    Dado que estou logado na página "https://www.saucedemo.com/" como "problem_user"
    Quando adiciono o item "Sauce Labs Bolt T-Shirt" ao carrinho
    E seleciono o carrinho
    E aperto o botão "Checkout"
    E informo os dados de nome de endereço
    E aperto o botão "Continue"
    E aperto o botão "Finish"
    Então vejo uma mensagem de confirmação do pedido
### **Dados de Teste**
First name: Gustavo
Last name: Toledo
Zip/Postal Code: 12345678

**Resultado esperado:** é exibida uma mensagem informando que o pedido foi confirmado.
**Resultados obtidos:**
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_29.png)
Não é possível completar a compra, visto que não tem como preencher o campo "Last Name". Ao tentar preencher o campo "Last Name", é alterado o campo "First Name". Além disso, não é possível adicionar todos os itens ao carrinho, apenas alguns.
### **Status**
**Não passou** ❌

## **CT03.3** – Realizar uma compra com o usuário `performance_glitch_user`
### **Objetivo**
Realizar a compra de um item no site.
### **Procedimento**
    Dado que estou logado na página "https://www.saucedemo.com/" como "performance_glitch_user"
    Quando adiciono o item "Sauce Labs Bolt T-Shirt" ao carrinho
    E seleciono o carrinho
    E aperto o botão "Checkout"
    E informo os dados de nome de endereço
    E aperto o botão "Continue"
    E aperto o botão "Finish"
    Então vejo uma mensagem de confirmação do pedido
### **Dados de Teste**
First name: Gustavo
Last name: Toledo
Zip/Postal Code: 12345678

**Resultado esperado:** é exibida uma mensagem informando que o pedido foi confirmado.
**Resultados obtidos:**
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_28.png)
É retornada uma mensagem informando que o pedido foi confirmado.
### **Status**
**Passou** ✅

## **CT03.4** – Realizar uma compra com o usuário `error_user`
### **Objetivo**
Realizar a compra de um item no site.
### **Procedimento**
    Dado que estou logado na página "https://www.saucedemo.com/" como "error_user"
    Quando adiciono o item "Sauce Labs Backpack" ao carrinho
    E seleciono o carrinho
    E aperto o botão "Checkout"
    E informo os dados de nome de endereço
    E aperto o botão "Continue"
    E aperto o botão "Finish"
    Então vejo uma mensagem de confirmação do pedido
### **Dados de Teste**
First name: Gustavo
Last name: Toledo
Zip/Postal Code: 12345678

**Resultado esperado:** é exibida uma mensagem informando que o pedido foi confirmado.
**Resultados obtidos:**
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_30.png)
Não é possível finalizar a compra, visto que não acontece nada ao clicar em "Finish". Além disso, o campo "Last Name" não é obrigatório nesse caso, e não são todos os itens que podem ser adicionados ao carrinho.
### **Status**
**Não passou** ❌

## **CT03.5** – Realizar uma compra com o usuário `visual_user`
### **Objetivo**
Realizar a compra de um item no site.
### **Procedimento**
    Dado que estou logado na página "https://www.saucedemo.com/" como "visual_user"
    Quando adiciono o item "Sauce Labs Bolt T-Shirt" ao carrinho
    E seleciono o carrinho
    E aperto o botão "Checkout"
    E informo os dados de nome de endereço
    E aperto o botão "Continue"
    E aperto o botão "Finish"
    Então vejo uma mensagem de confirmação do pedido
### **Dados de Teste**
First name: Gustavo
Last name: Toledo
Zip/Postal Code: 12345678

**Resultado esperado:** é exibida uma mensagem informando que o pedido foi confirmado.
**Resultados obtidos:**
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_28.png)
É retornada uma mensagem informando que o pedido foi confirmado. No entanto, alguns itens estão alocados de forma errada na tela.
![Homepage](https://raw.githubusercontent.com/Toledo02/Teste-Pratico-QA-Testing-BeTalent/main/Screenshot_31.png)
### **Status**
**Não passou** ❌

## **CT04.1** – Remover itens do carrinho com o usuário `standard_user`
### **Objetivo**
Remover itens do carrinho.
### **Procedimento**
    Dado que estou logado na página "https://www.saucedemo.com/" como "standard_user"
    E possuo o item "Sauce Labs Onesie" no carrinho
    E seleciono o carrinho
    Quando aperto o botão "Remove"
    Então o item é removido do carrinho
### **Dados de Teste**
Item: Sauce Labs Onesie

**Resultado esperado:** o item é removido do carrinho.
**Resultados obtidos:**
O item foi removido do carrinho.
### **Status**
**Passou** ✅

## **CT04.2** – Remover itens do carrinho com o usuário `problem_user`
### **Objetivo**
Remover itens do carrinho.
### **Procedimento**
    Dado que estou logado na página "https://www.saucedemo.com/" como "problem_user"
    E possuo o item "Sauce Labs Onesie" no carrinho
    E seleciono o carrinho
    Quando aperto o botão "Remove"
    Então o item é removido do carrinho
### **Dados de Teste**
Item: Sauce Labs Onesie

**Resultado esperado:** o item é removido do carrinho.
**Resultados obtidos:**
O item foi removido do carrinho. No entanto, não é possível adicionar todos os itens ao carrinho, apenas alguns.
### **Status**
**Passou** ✅

## **CT04.3** – Remover itens do carrinho com o usuário `performance_glitch_user`
### **Objetivo**
Remover itens do carrinho.
### **Procedimento**
    Dado que estou logado na página "https://www.saucedemo.com/" como "performance_glitch_user"
    E possuo o item "Sauce Labs Onesie" no carrinho
    E seleciono o carrinho
    Quando aperto o botão "Checkout"
    Então o item é removido do carrinho
### **Dados de Teste**
Item: Sauce Labs Onesie

**Resultado esperado:** o item é removido do carrinho.
**Resultados obtidos:**
O item foi removido do carrinho. No entanto, há lentidão ao utilizar as funcionalidades.
### **Status**
**Passou** ✅

## **CT04.4** – Remover itens do carrinho com o usuário `error_user`
### **Objetivo**
Remover itens do carrinho.
### **Procedimento**
    Dado que estou logado na página "https://www.saucedemo.com/" como "error_user"
    E possuo o item "Sauce Labs Onesie" no carrinho
    E seleciono o carrinho
    Quando aperto o botão "Remove"
    Então o item é removido do carrinho
### **Dados de Teste**
Item: Sauce Labs Onesie

**Resultado esperado:** o item é removido do carrinho.
**Resultados obtidos:**
O item foi removido do carrinho. No entanto, não é possível adicionar todos os itens ao carrinho, apenas alguns.
### **Status**
**Passou** ✅

## **CT04.5** – Remover itens do carrinho com o usuário `visual_user`
### **Objetivo**
Remover itens do carrinho.
### **Procedimento**
    Dado que estou logado na página "https://www.saucedemo.com/" como "visual_user"
    E possuo o item "Sauce Labs Onesie" no carrinho
    E seleciono o carrinho
    Quando aperto o botão "Remove"
    Então o item é removido do carrinho
### **Dados de Teste**
Item: Sauce Labs Onesie

**Resultado esperado:** o item é removido do carrinho.
**Resultados obtidos:**
O item foi removido do carrinho. No entanto, alguns itens estão incorretos.
### **Status**
**Passou** ✅

## **CT05.1** – Validar o logout para o usuário `standard_user`
### **Objetivo**
Fazer logout do site.
### **Procedimento**
    Dado que estou logado na página "https://www.saucedemo.com/" como "standard_user"
    Quando aperto o botão do menu
    E seleciono a opção "Logout"
    Então sou redirecionado para a página de login
### **Dados de Teste**
Não há

**Resultado esperado:** sou redirecionado para a tela de login.
**Resultados obtidos:**
Sou redirecionado para a tela de login.
### **Status**
**Passou** ✅

## **CT05.2** – Validar o logout para o usuário `problem_user`
### **Objetivo**
Fazer logout do site.
### **Procedimento**
    Dado que estou logado na página "https://www.saucedemo.com/" como "problem_user"
    Quando aperto o botão do menu
    E seleciono a opção "Logout"
    Então sou redirecionado para a página de login
### **Dados de Teste**
Não há

**Resultado esperado:** sou redirecionado para a tela de login.
**Resultados obtidos:**
Sou redirecionado para a tela de login.
### **Status**
**Passou** ✅

## **CT05.3** – Validar o logout para o usuário `performance_glitch_user`
### **Objetivo**
Fazer logout do site.
### **Procedimento**
    Dado que estou logado na página "https://www.saucedemo.com/" como "performance_glitch_user"
    Quando aperto o botão do menu
    E seleciono a opção "Logout"
    Então sou redirecionado para a página de login
### **Dados de Teste**
Não há

**Resultado esperado:** sou redirecionado para a tela de login.
**Resultados obtidos:**
Sou redirecionado para a tela de login.
### **Status**
**Passou** ✅

## **CT05.4** – Validar o logout para o usuário `error_user`
### **Objetivo**
Fazer logout do site.
### **Procedimento**
    Dado que estou logado na página "https://www.saucedemo.com/" como "error_user"
    Quando aperto o botão do menu
    E seleciono a opção "Logout"
    Então sou redirecionado para a página de login
### **Dados de Teste**
Não há

**Resultado esperado:** sou redirecionado para a tela de login.
**Resultados obtidos:**
Sou redirecionado para a tela de login.
### **Status**
**Passou** ✅

## **CT05.5** – Validar o logout para o usuário `visual_user`
### **Objetivo**
Fazer logout do site.
### **Procedimento**
    Dado que estou logado na página "https://www.saucedemo.com/" como "visual_user"
    Quando aperto o botão do menu
    E seleciono a opção "Logout"
    Então sou redirecionado para a página de login
### **Dados de Teste**
Não há

**Resultado esperado:** sou redirecionado para a tela de login.
**Resultados obtidos:**
Sou redirecionado para a tela de login.
### **Status**
**Passou** ✅

## **Sugestão de melhorias**
- É possível realizar uma compra sem ter nenhum item no carrinho, o que não faz sentido.
- Há muita lentidão no sistema ao utilizar o usuário "performance_glitch_user".
- Utilizar padronização de imagens para todos os usuários.

## **Bugs encontrados**
- Em alguns casos, não é possível finalizar a compra porque o campo "Last Name" na página "checkout-step-one.html" é preenchido de forma errada.
- No caso do usuário "error_user" é possível passar para a página "checkout_step_two" sem informar o campo "Last Name".
- Para alguns usuários, não é possível adicionar todos os itens ao carrinho, apenas alguns.
- As imagens estão incorretas para os usuários "visual_user" e "problem_user".
- O filtro não está funcionando para o usuário "problem_user".
- O filtro não está funcionando para o usuário "error_user".
- O filtro está funcionando parcialmente para o usuário "visual_user", sendo a parte funcional a ordenação por ordem alfabética e a não funcional por preço.
- O botão "Finish" não está funcionando para o usuário "error_user".
- Os preços dos itens estão incorretos para o usuário "visual_user".

## **Análise de riscos da aplicação**
- Há muita lentidão para alguns usuários, o que pode impactar negativamente na experiência do cliente.
- Para alguns usuários não é possível finalizar a compra, o que gera irritabilidade nos usuários e perda de vendas para o site.
- Alguns usuários terão dificuldade de localizar as funcionalidades, visto que alguns botões estão em lugares pouco intuitivos, o que gera desconforto para o usuário.
- 
## **Sugestões de automação**
- Todos os fluxos podem ser facilmente automatizados utilizando Cypress, visto que todas as funcionalidades são web.
- Poderiam ser feitos cenários de Login para todos os usuários, fluxo completo de compra, remoção de itens do carrinho, navegação entre páginas e logout.
- Além do Cypress, também é possível utilizar o Selenium, visto que todos os testes possuem Gherkin já escrito.
---

