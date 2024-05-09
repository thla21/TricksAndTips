# Reset Administrator Password

Para inicio do procedimento baixe o [MediaCreationTool22H2.exe](https://www.microsoft.com/pt-br/software-download/windows10) para criar uma mídia de instalação do Windows 10.

Durante o processo de criação da mídia de instalação selecione a seguinte opção `Crie uma mídia de instalação (USB, DVD ou ISO) para outro PC`:

![Windows6](https://github.com/thla21/TricksAndTips/assets/62508225/837aa095-56ff-47bc-be31-9d6e8666fb76)

Em seguida a seguinte opção :

[![Windows7.png](https://i.postimg.cc/pdTsvLS6/Windows7.png)](https://postimg.cc/Yv56fMM6)

Selecione a linguagem, edição e arquitetura do Windows. Por fim grave a ISO em uma mídia do tipo Pendrive ou LiveCD.

Reinicie o Windows entre na BIOS do PC e inicie a mídia de crição como primeira prioridade de boot. Durante o Processo de inicialização do mídia abra o prompt de comando da seguinte maneira:

[![Windows8.png](https://i.postimg.cc/5tvvzH6G/Windows8.png)](https://postimg.cc/Ffr75Hbg)

[![Windows9.png](https://i.postimg.cc/sgb71PD7/Windows9.png)](https://postimg.cc/yDXkbZR8)

[![Windows10.png](https://i.postimg.cc/PxjDQtDq/Windows10.png)](https://postimg.cc/Mc9XWJdk)

[![Windows11.png](https://i.postimg.cc/QC6WD1yB/Windows11.png)](https://postimg.cc/D4XzdJFF)

Entre na unidade da mídia de instalação, como neste exemplo a mídia de instalação está na unidade D:

```prompt
D:
```

```prompt
cd Windows
```

```prompt
cd System32
```

```prompt
ren cmd.exe utilman2.exe
```

```prompt
ren utilman.exe cmd.exe
```

```prompt
ren utilman2.exe utilman.exe
```

Feixe o prompt de comando e clique em **Continue**, reinicie a máquina:

[![Windows13.png](https://i.postimg.cc/RFsrMm3R/Windows13.png)](https://postimg.cc/S2M1rwf2)

Na tela de login clique no ícone do meio no canto inferior direito, você terá acesso a tela de prompt com o utilitário `utilman`:

[![Windows14.png](https://i.postimg.cc/ZY3bV0Cm/Windows14.png)](https://postimg.cc/s1jC2jYH)

Execute o seguinte comando para ver seu nível de autoridade:

```prompt
whoami
```

[![Windows15.png](https://i.postimg.cc/0yq1jCfK/Windows15.png)](https://postimg.cc/QHSyn1vj)

Agora adicione um usuário e senha:

```prompt
net user <NOME_DO_USUÁRIO> <SENHA_DO_USUÁRIO> /add
```

Usuário será adicionado com sucesso

[![Windows16.png](https://i.postimg.cc/yYkBGP1w/Windows16.png)](https://postimg.cc/gnFfX36D)

Agora vamos ver o nível de privilegio deste novo usuário:

```prompt
netplwiz
```

Siga a sequencia das imagens abaixo:

[![Windows17.png](https://i.postimg.cc/13L9wYF9/Windows17.png)](https://postimg.cc/jD40rcv9)

[![Windows18.png](https://i.postimg.cc/157R5z5V/Windows18.png)](https://postimg.cc/LnfFx2Pm)

[![Windows19.png](https://i.postimg.cc/P5LXLkP3/Windows19.png)](https://postimg.cc/WdvLKCmg)

Por fim clique em aplicar e der OK. Logue com o novo usuário e sucesso!:)
