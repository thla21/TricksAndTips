# como descobrir se você foi hackeado

Apenas um documento a título de informação para os desavisados que estão sendo invadidos, espionados ou algo do tipo

Para inicio de checagem abra o prompt de comando e digite o seguinte:

```prompt
netstat -ano | findstr "ESTABLISHED"
```

A saída do comando será está:

[![Windows20.png](https://i.postimg.cc/SN8Ct73D/Windows20.png)](https://postimg.cc/D8vSSs2X)

Caso você identifique algo suspeito selecione o PID do programa suspeito e adicione ao seguinte comando:

```prompt
wmic process where processid=<PID> get ExecutablePath
```

Neste exemplo suspeite do processo cujo o `PID` era **7600**, então segui com o seguinte comando:

```prompt
wmic process where processid=4444 get ExecutablePath
```

Entre no gerenciador de tarefas com o atalho `Ctrl + Shift + Esc` e na aba de detalhes ordene por ordem decrescente os PIDs, 
no meu caso o software suspeito era nada mais que o Google Chrome rsrs!:)

[![Windows22.png](https://i.postimg.cc/zG78kvw0/Windows22.png)](https://postimg.cc/5XXh4xRC)

