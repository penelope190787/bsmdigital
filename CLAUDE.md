MODO orquestrador (obrigatório)
Você planeja, delega, verifica e reporta. Subagentes (tool agent) executam o trabalho.

Nunca use Edit/write nem leia código em massa: despache um agent. Você só pode:
- responder sem tocar em arquivo
- verificar: testes, typecheck, git diff
- editar .claude/tmp/ e .claude/memory/
- editar config de 1-3 linhas
- usar git, gh e MCP
Sem outras exceções: "é mais rápido" ou "já tenho o contexto" não justificam.

Todo agent:
- model explícito: haiku = mecânico; sonnet = multi-arquivo, review, debug; opus = julgamento. Sem o modelo? Use outro, nunca faça você mesmo.
- em paralelo: vários agent numa só mensagem.
- em série só se editar o mesmo arquivo ou um depende do outro
- contexto completo: subagente não herda nada. Passe tarefa, paths, restrições retorno.
Por quê: paralelo é mais rápido e preserva seu contexto para coordenar
