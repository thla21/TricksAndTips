# como descobrir se você foi hackeado

Apenas um documento a título de informação para os desavisados que estão sendo invadidos, espionados ou algo do tipo

Para inicio de checagem abra o prompt de comando e digite o seguinte:

```prompt
netstat -ano | findstr "ESTABLISHED"
```

A saída do comando será está:

![Windows21](https://github.com/thla21/TricksAndTips/assets/62508225/b1e6f876-7c16-4fa6-bb1b-b0131faf20ea)


Caso você identifique algo suspeito selecione o PID do programa suspeito e adicione ao seguinte comando:

```prompt
wmic process where processid=<PID> get ExecutablePath
```

Neste exemplo suspeite do processo cujo o `PID` era **7600**, então segui com o seguinte comando:

```prompt
wmic process where processid=4444 get ExecutablePath
```

A saída será o diretório do executável cujo o PID está relacionado

![Windows22](https://github.com/thla21/TricksAndTips/assets/62508225/42596dc2-12b2-40b9-a4d5-e48312e7810f)

Entre no gerenciador de tarefas com o atalho `Ctrl + Shift + Esc` e na aba de detalhes ordene por ordem decrescente os PIDs, 
no meu caso o software suspeito era nada mais que o Google Chrome rsrs!:)

![Windows23](https://github.com/thla21/TricksAndTips/assets/62508225/a455bc42-56f1-4fd8-9bd3-985a362ce4ff)

