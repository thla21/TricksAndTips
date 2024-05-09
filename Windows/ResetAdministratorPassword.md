# Reset Administrator Password

Para inicio do procedimento baixe o [MediaCreationTool22H2.exe](https://www.microsoft.com/pt-br/software-download/windows10) para criar uma mídia de instalação do Windows 10.

Durante o processo de criação da mídia de instalação selecione a seguinte opção `Crie uma mídia de instalação (USB, DVD ou ISO) para outro PC`:

![Windows7](https://github.com/thla21/TricksAndTips/assets/62508225/abba085d-a765-431e-9a1a-0b7c776bcaf1)

Em seguida a seguinte opção :

![Windows8](https://github.com/thla21/TricksAndTips/assets/62508225/fd6f37fe-9693-4694-921a-2aafc4f3f351)

Selecione a linguagem, edição e arquitetura do Windows. Por fim grave a ISO em uma mídia do tipo Pendrive ou LiveCD.

Reinicie o Windows entre na BIOS do PC e inicie a mídia de crição como primeira prioridade de boot. Durante o Processo de inicialização do mídia abra o prompt de comando da seguinte maneira:

![Windows9](https://github.com/thla21/TricksAndTips/assets/62508225/afe21db8-8f58-47ac-985a-1a596f272c1c)

![Windows10](https://github.com/thla21/TricksAndTips/assets/62508225/ad446fd4-ce50-44a0-b9b9-8e5b037c0f22)

![Windows11](https://github.com/thla21/TricksAndTips/assets/62508225/7c921631-8abb-411a-b4b9-d3ad34aa7197)

![Windows12](https://github.com/thla21/TricksAndTips/assets/62508225/6fd98d14-110f-4e02-a554-6e12cc75a293)

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

![Windows14](https://github.com/thla21/TricksAndTips/assets/62508225/9324eb9f-41c3-4d07-93bc-7f48f13e734b)

Na tela de login clique no ícone do meio no canto inferior direito, você terá acesso a tela de prompt com o utilitário `utilman`:

![Windows15](https://github.com/thla21/TricksAndTips/assets/62508225/8c8e46f9-4529-47f3-9bc3-392df163e263)

Execute o seguinte comando para ver seu nível de autoridade:

```prompt
whoami
```

![Windows16](https://github.com/thla21/TricksAndTips/assets/62508225/02e42871-90ab-40cf-9207-b635aab5bb5e)

Agora adicione um usuário e senha:

```prompt
net user <NOME_DO_USUÁRIO> <SENHA_DO_USUÁRIO> /add
```

Usuário será adicionado com sucesso

![Windows17](https://github.com/thla21/TricksAndTips/assets/62508225/53601413-2d29-4140-ba5c-83b84212e68f)

Agora vamos ver o nível de privilegio deste novo usuário:

```prompt
netplwiz
```

Siga a sequencia das imagens abaixo:

![Windows18](https://github.com/thla21/TricksAndTips/assets/62508225/7b21b9a6-6771-42ba-b69a-47eee211ad18)

![Windows19](https://github.com/thla21/TricksAndTips/assets/62508225/d439b594-4aa4-4cb6-af4c-4178f66fe739)

![Windows20](https://github.com/thla21/TricksAndTips/assets/62508225/a278f390-0f97-4992-8a34-edce7b778cae)

Por fim clique em aplicar e der OK. Logue com o novo usuário e sucesso!:)
