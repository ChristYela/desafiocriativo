🎯 README — Desafio Criativo: Prompt de Agente de Atendimento ao Cliente
Plataforma: DIO
Desafio: Projetando o Prompt de um Agente de Atendimento ao Cliente
Cenário escolhido: Streaming de música por assinatura
Canal: Chat do aplicativo (mobile e desktop)

📖 Sobre o Desafio
Este repositório contém a entrega do Desafio Criativo da DIO, cujo objetivo é construir, passo a passo, o prompt de um Agente de Atendimento ao Cliente capaz de orientar uma IA a se comportar de forma clara, segura e útil em conversas reais com clientes.

O exercício foi dividido em três etapas:

Passo	O que foi feito
1	Definição do papel do Agente, do público e dos pedidos que ele resolve
2	Definição de tom, formato, regras de conduta e critérios de encaminhamento humano
3	União das peças em um prompt final, testes em casos difíceis e refinamento
🎧 Cenário Escolhido
Optei por criar o Tune, um Agente de atendimento de uma plataforma de streaming de música por assinatura, atuando no chat do aplicativo.

A escolha se deu por três motivos:

Conhecimento real do serviço — uso diariamente e conheço os problemas típicos (playlists que somem, cobranças duplicadas, plano familiar, qualidade de áudio).

Público bem definido — jovens adultos e famílias, acostumados com o app, que chegam ao chat com pressa.

Casos difíceis naturais — cobrança não reconhecida, exclusão de conta (LGPD), suspeita de invasão — situações que exigem encaminhamento humano e testam os limites do Agente.

🧱 Estrutura do Prompt
O prompt final está organizado em blocos que se complementam:

text
1. Papel e Escopo
   ├── Quem é o Agente (Tune)
   ├── Canal de atendimento
   ├── Quem fala com ele
   └── Pedidos que resolve

2. Tom e Formato
   ├── Tom de voz
   ├── Limite de linhas
   ├── Uso de listas numeradas
   └── Uso moderado de emojis

3. Regras que sempre segue
   ├── Dados que nunca pede
   ├── O que faz quando não sabe
   └── O que nunca inventa

4. Encaminhamento humano
   ├── Situações que exigem pessoa
   └── Como encaminhar

5. Regra de ouro
   └── Perguntar antes de responder
🧪 Testes Realizados
O prompt foi testado em uma IA conversacional com três situações propositalmente difíceis, conforme o Passo 3 do desafio.

✅ Teste 1 — Pedido comum
Cliente: "Minha playlist de corrida sumiu do nada, tinha umas 200 músicas!"

Resposta do Tune: lista numerada com passos de recuperação, tom próximo, um emoji, encerramento com pergunta.

Resultado: dentro do formato e do limite de linhas. ✅

✅ Teste 2 — Informação que o Agente não tem
Cliente: "Quanto vou pagar de multa se eu cancelar o plano anual agora?"

Resposta do Tune: admitiu não ter o valor, indicou a tela onde o cliente encontra, ofereceu ajuda para chegar lá. Não inventou número.

Resultado: comportamento esperado — não alucinou. ✅

✅ Teste 3 — Caso que exige encaminhamento
Cliente: "Apareceu uma cobrança de R$ 89,90 no meu cartão que eu não reconheço."

Resposta do Tune: encaminhou para o time de segurança, explicou o motivo, registrou o relato, informou canal e prazo, sugeriu troca de senha.

Resultado: encaminhou corretamente sem tentar resolver sozinho. ✅

🔧 Ajuste Feito Após os Testes
Na primeira versão, o Tune respondia com 6 a 7 linhas nos casos técnicos — acima do limite pedido.

Correção aplicada: reforcei no prompt a regra "no máximo 4 linhas por resposta" e acrescentei a orientação "se precisar de mais espaço, pergunte antes de despejar tudo".

Após o ajuste, o Agente passou a respeitar o formato em todos os testes.

💡 Aprendizado Principal
A parte mais difícil do exercício não foi listar o que o Agente faz — foi escrever o que ele não faz e, principalmente, autorizá-lo a admitir que não sabe.

A linha final do prompt — "Se faltar alguma informação para responder com segurança, pergunte antes de responder" — foi o que mais mudou o comportamento nos testes.

Sem ela, o modelo inventava prazos e valores com muita confiança. Com ela, virou um atendente que parece humano de verdade. É essa diferença que separa um bot confiável de um bot que apenas soa confiante.

📁 Conteúdo do Repositório
text
📦 desafio-prompt-atendimento-dio
 ┣ 📄 README.md          → este arquivo
 ┗ 📄 prompt-tune.md     → prompt final do Agente Tune
🚀 Como Usar o Prompt
Abra o arquivo prompt-tune.md.

Copie o conteúdo integral.

Cole em uma IA conversacional de sua preferência (ChatGPT, Gemini, Copilot, etc.).

Converse com o Agente como se fosse um cliente — teste pedidos comuns, pedidos fora do escopo e casos que exigem encaminhamento.

🔗 Entrega
Prompt final: prompt-tune.md

Plataforma: DIO



✍️ Autor 
Cristian Yela
Desenvolvido como parte do Desafio Criativo da DIO — "Projetando o Prompt de um Agente de Atendimento ao Cliente".

"Um bom prompt nasce de intenção clara, contexto e instruções específicas."
— DIO
