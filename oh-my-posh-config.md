# Oh My Posh - Instalação e configuração no Windows

Primeiramente acesse o site [ohmyposh](https://ohmyposh.dev/docs/installation/windows) e siga o guia de instalação para o windows.

Faça o download da font que você quer usar no terminal.

```bash
oh-my-posh font install --user
```

<br />

Você também pode entrar e escolher manualmente no site: [Nerd Fonts](https://www.nerdfonts.com/font-downloads)

Para previnir que o PowerShell bloqueie a execução dos scripts locais, defina que ele exige que apenas os scripts remotos sejam assinados.

```bash
Set-ExecutionPolicy RemoteSigned
```

<br />

Certo agora é só iniciar

```bash
oh-my-posh init pwsh | Invoke-Expression
```

<br />

Se funcionou agora vamos executar o `oh-my-posh` todas as vezes que o terminal for iniciado.

Então abra o profile:

```bash
notepad $PROFILE
```

<br />

E cole isso lá dentro:

```bash
oh-my-posh init pwsh
```
<br />

## Caso queira customizar, veja os temas que te agrada

```bash
Get-PoshThemes
```

<br />

Para iniciar já com um tema definido

```bash
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\dracula.omp.json" | Invoke-Expression
```

<br />

Um tema que eu gostei

```bash
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\montys.omp.json" | Invoke-Expression
```

Outras melhorias

```bash
#Adicionar ícones em pastas do terminal
Install-Module Terminal-Icons
Import-Module -Name Terminal-Icons
```
