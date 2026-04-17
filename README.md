# Explorando Práticas de Teste

Neste exercício, vamos explorar práticas de teste em sistemas reais utilizando a ferramenta [TestMiner](https://andrehora.github.io/testminer).

O TestMiner permite visualizar e analisar testes de software em repositórios do GitHub, fornecendo dados sobre como os projetos organizam seus testes, como eles evoluem entre versões e quais bibliotecas de teste são utilizadas.
Explore a ferramenta antes de começar para se familiarizar com seu funcionamento.

---

## Passo 1: Selecionar um repositório

Escolha um repositório real que possua testes escritos na linguagem de sua preferência.
Abaixo estão alguns links para ajudá-lo a encontrar projetos interessantes:

- **Python:** https://github.com/topics/python?l=python
- **JavaScript:** https://github.com/topics/javascript?l=javascript
- **TypeScript:** https://github.com/topics/typescript?l=typescript
- **Java:** https://github.com/topics/java?l=java

## Passo 2: Explorar o repositório selecionado

Busque o repositório escolhido no [TestMiner](https://andrehora.github.io/testminer) e analise os dados de teste gerados pela ferramenta.

## Passo 3: Explicar uma prática de teste

Com base nos dados obtidos, selecione uma prática ou dado de teste relevante e explique-o com suas próprias palavras.

---

## Instruções de entrega

1. Faça um `fork` deste repositório (saiba mais sobre forks [aqui](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)).
2. Responda às questões abaixo diretamente neste arquivo `README.md` do seu fork. Pode adicionar imagens para enriquecer sua explicação.
3. No Moodle, submeta apenas a URL do seu fork.

---

## Respostas

**1. Repositório selecionado:** `https://github.com/huggingface/smolagents`

**2. Explicação:** `Eu escolhi o repositório huggingface/smolagents porque ele é um projeto de agentes de IA que ja trabalhei e eu queria entender como esse tipo de sistema é validado na prática.

Ao analisar os testes, uma prática que achei muito interessante foi testar não só o “caminho certo”, mas também falhas e limites de execução. Um exemplo é o teste test_fails_max_steps, que valida se o agente para corretamente quando atinge o número máximo de passos (max_steps) e registra o erro esperado (AgentMaxStepsError). Esse teste é importante porque agentes podem entrar em loops ou não chegar a uma resposta final, então ter esse controle aumenta a segurança e evita execuções infinitas.

Outro teste que me chamou atenção foi o test_function_persistence_across_steps, que verifica se uma função definida em uma etapa continua disponível nas etapas seguintes. Isso é interessante porque mostra que os testes estão cobrindo o comportamento “multi-step” real do agente, e não apenas chamadas isoladas.

No geral, eu percebi que o projeto usa testes para garantir robustez em cenários reais, ou seja, resposta correta, tratamento de erro, persistência de contexto e controle de execução. Isso passa mais confiança para manter e evoluir a biblioteca sem quebrar comportamentos importantes.`
