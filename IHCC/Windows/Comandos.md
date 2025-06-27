- **CRIAR USUÁRIO**
```
net user /add [username] [password]
```

- **FORCAR O USUÁRIO A TROCAR A SENHA NO PRÓXIMO LOGIN**
```
net user username /logonpasswordchg
```
"No website de referência da Microsoft sobre a ferramenta "net user" não está listada a opção /logonpasswordchg, porém ao usar o comando de ajuda no terminal vemos que a opção é válida"
REFERENCIA: https://learn.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/cc771865(v=ws.11)

- **INSERIR USUÁRIO EM UM GRUPO**
```
net localgroup [group] [username] /add
```

- **CRIAR GRUPO**
```
net localgroup [group] /add
```

- **CRIAR ARQUIVO**
```
echo "" > [nomeArquivo].[extensao]
```

- **EDITAR ARQUIVO**
"Infelizmente o Windows não possuí uma ferramenta interna para editar arquivos texto diretamente pelo terminal, sendo necessário abrir uma ferramenta GUI ou instalar algum editor TUI, portanto, para cumprir os requisitos da avaliação, foi aberto o notepad e realizada a inserção de texto por meio deste."
"o comando echo com redirecionamento de saída poderia ser utilizado para o exercício, porém este apenas iria sobrescrever o arquivo."

- **PERMISSÕES SOBRE UM ARQUIVO**
```
icacls [arquivo] /grant:r [usuario]:([permissoes]
```
ou
```
icacls [arquivo] /grant:r [grupo]:([permissoes])
```
REFERENCIA: https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/icacls
