# Implementando (processo de) qualidade

Primeiramente, é preciso conhecer o time, suas atividades cotidianas, o que fazem e como fazem. E time não fica só num grupo seleto de pessoas, mas se estende a toda empresa.

Após esse primeiro contato, mapear como é o processo de qualidade no momento, o que o time faz para garantir que o seu código e software desenvolvido funcione conforme o esperado e com o mínimo de bugs possível. Em caso de bugs, como é feita a priorização e resolução se encontrados durante o desenvolvimento e produção? Existe documentação desses processos?

Caso não exista uma documentação, criar algo simples como um fluxograma ou mesmo um passo a passo em texto. Aqui o importante é ter uma visualização e um consenso de como é feito o processo.

De posse da documentação, já existente ou a criada no parágrafo anterior, estudá-la e propor melhorias em pontos-chaves. Esses pontos devem ser definidos com o time, levando em consideração criticidade para o negócio, áreas descobertas ou até mesmo facilidade de implementação. O importante é que seja consenso do time onde atacar primeiro.

Definido o onde, estudar o que pode ser feito de melhoria. Se falta testes, definir qual tipo será implementado primeiro, como testes de unidade, integração, funcional, não funcional, ou todos juntos. Se já existe testes, é possível melhorá-los? Existe monitoramento da saúde do que está em produção? Existe alguma métrica, não só de testes, mas algo que nos ajude a tomar alguma decisão sem ser no achismo? Talvez testes nem seja o necessário no momento para a qualidade do produto.

Como anda a automação dos processos em geral? Processos manuais são altamente suscetíveis a erros.

Decisão tomada, criar uma plano de ação, um _roadmap_ das atividades que precisam serem feitas. Estabelecer _checkpoints_ para verificação, quem estará envolvido e como as tarefas serão distribuídas.

Caso haja dúvidas sobre ferramentas ou metodologias a serem utilizadas, fazer uma ou mais provas de conceito (POC) para decidir qual se adequa melhor a situação. Fazer adaptações empiricamente.

Definir métricas, OKRs por exemplo, para saber se o objetivo, como redução de bugs, diminuição do tempo de build ou resposta de um serviço etc. estão sendo alcançadas.

## QA não é só tester ou automatizador

O QA (Quality Assurance), como o nome diz, é quem garante a qualidade. E muitas vezes a qualidade não está só nos testes ou automação. Muitas vezes, para se garantir a qualidade, é necessário que o QA "use o chapéu" de outras funções, como PO, UX/Designer, Writer, Researcher.

O produto final é uma junção das expertises de várias áreas e o QA deve saber ao menos "conversar" com todas elas.
