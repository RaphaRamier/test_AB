# Introdução

O presente projeto tem por finalidade analisar o comportamento dos usuários para o aplicativo da empresa. Empresa essa que é uma startup de produtos alimentícios. 

Os designers gostariam de alterar as fontes de todo o aplicativo, mas os gerentes temem que os usuários achem o novo design intimidador. Então, decidiram tomar a decisão com base nos resultados de um teste A/A/B.

Os usuários são divididos em três grupos: dois grupos de controle recebem as fontes antigas e um grupo de teste recebe as novas. Descubra qual conjunto de fontes produz melhores resultados.


# Descrição dos Dados


Cada entrada de diário é uma ação do usuário ou um evento.

* EventName — nome do evento
* DeviceIDHash — dentificador de usuário exclusivo
* EventTimestamp — hora do evento
* ExpId — número do experimento: 246 e 247 são os grupos de controle, 248 é o grupo de teste

# Conclusão


Como se observou no decorrer da construção da análise houveram algumas inconsistências tratadas nos dados que não comprometeram o andamento do projeto. Permitindo assim fazer uma análise limpa dos dados que nos foram apresentados. 

Uma vez apresentados os dados limpos, podemos constatar que:

* Nas análises de funis percebe-se que apenas 28,9% do evento de MainScreen terminam na compra efetuada, o que pode representar em números absolutos o famoso "scrollar", apenas olhando e pesquisando para tomar uma decisão.
* A Rota mais comum é MainScreenAppear -> OffersScreenAppear -> CartScreenAppear -> PaymentScreenSuccessful, pois é a rota lógica.
* A maior perda é entre o primeiro evento e o segundo. Foi notada uma perda que quase 38%.


A respeito dos testes estatísticos:

* Fora usado o teste de Mann Whitney.
* Por convenção foi utilizado o α de 5%, ou seja, um nível de confiança de 95%
* Portanto, para o nosso caso de 12 testes estatísticos com um nível de confiança de 95% (ou α = 0,05), podemos calcular a probabilidade de nenhum erro ocorrer:

> * Probabilidade de nenhum erro = (1 - 0,05) ^ 12
> * Probabilidade de nenhum erro = 0,95 ^ 12
> * Probabilidade de nenhum erro ≈ 0,528

>> Isso significa que há uma probabilidade aproximada de 52,8% de que nenhum erro ocorra nos 12 testes estatísticos.

Posto isso os testse nos revelaram que:


* Há Diferença Estatística de OffersScreenAppear entre os Grupos: A1 e B;

* Há Diferença Estatística de CartScreenAppear entre os Grupos: A1 e A2;

* Há Diferença Estatística de PaymentScreenSuccessful entre os Grupos: A1 e A2.

* Enquanto nos outros eventos não há diferença estatística significante. 

Posto isso, o teste estatísticos nos trazem a percepção que não houve o impacto esperado a mudança da fonte do aplicativo. 


