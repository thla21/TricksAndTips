## Fazendo um bypass em restrição de administrador do Windows para instalar programas não permitidos em qualquer PC.

Digite `Windows + r` e inicie o notepad, no bloco de notas em branco digite o seguinte comando:

```bat
Set __COMPAT_LAYER=RunAsInvoker
Start <Nome do Programa.exe>
```

Salve o arquivo como a extenção .bat com nome da sua preferência, eu coloquei `baypass.bat`.
Execute com 2(dois) cliques o arquivo.bat e verifique que o programa solicitado irá iniciar seu wizard normalmente sem senha de restrição do Administrador.

Obs.: No campo <Nome do Programa.exe> digite o nome do programa desejável para iniciar a instalação.
Obs2.: O arquivo.bat deve está no mesmo diretório do programa de inicialiação para instalação no Windows.
