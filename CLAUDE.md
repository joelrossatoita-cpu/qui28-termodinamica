# Projeto: revisão QUI-28 Termodinâmica (prova 16/11/2026, 19h–22h)

O aluno estuda pelas aulas 1–7 do prof. Amauri. A prova usa a lista Q1–Q40 (aulas 2–7).

## Arquivos
- `Apostila_QUI-28_Termodinamica_Quimica.pdf` / `apostila.txt`: fonte principal
- `revisao-qui28.html`: teoria por aula (dos slides), a lista com resolução e o gabarito
- `duvidas-qui28.md`: caderno de dúvidas (D1, D2…), mantido pelo revisor
- `progresso-aluno.md`: onde o aluno está (aula, assunto, apostila lida, questões feitas), mantido pelo professor

## Abertura de toda sessão
Na primeira mensagem do aluno em cada sessão, antes de qualquer outra coisa, chame o agente **professor-qui28** com o prompt `ABERTURA` (mais a mensagem do aluno, se ela já trouxer algo). Mostre a saudação como veio ("E aí, <nome de bixo>!…"). Se a primeira mensagem também tiver uma dúvida, depois da saudação siga o fluxo de dúvida abaixo.

## Fluxo para toda dúvida do aluno
1. Mande a pergunta, literal, ao agente **professor-qui28** (Agent tool). No prompt inclua o endereço do revisor ("revisor: <nome ou id>") e o contexto recente da conversa que a dúvida pressupõe (por exemplo, a que slide ou questão ela se refere).
2. Se ainda não houver um revisor ativo nesta sessão, crie um a partir de **revisor-qui28**, com o nome `revisor`, antes do passo 1. Nas sessões seguintes, reuse esse nome.
3. Mostre ao aluno a explicação do professor como ela veio. Se ela terminar com um bloco "PARA O REVISOR", repasse esse bloco ao revisor com SendMessage e tire o bloco do texto mostrado ao aluno.

## Progresso do aluno
Quando o aluno contar o que leu da apostila ou o que fez da lista ("li até o 2.5", "fiz Q7–Q10", "errei a Q9"), mande a mensagem, literal, ao **professor-qui28** com o prompt `PROGRESSO: <mensagem>`. Ele atualiza `progresso-aluno.md` e devolve o próximo passo; mostre como veio.

## Outros pedidos
Pedidos que não são dúvida nem progresso (mudar a página, criar arquivos) não passam pelo professor.
