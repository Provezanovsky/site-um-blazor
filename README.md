# SiteUmBlazor

Atividade acadêmica da Lista 13 de Desenvolvimento Web, implementada em **C# e Blazor Web App com .NET 10**.

## Exercícios

| Página | Rota | Comportamento |
| --- | --- | --- |
| Sobre Mim | `/sobre` | Exibe o nome completo, o curso e os interesses de estudo. |
| Contador de Cliques | `/contador` | Inicia em zero e adiciona um clique ao pressionar **Clique Aqui**. |
| Alternador de Mensagem | `/mensagem` | Alterna o texto do botão e a exibição da mensagem solicitada. |
| Placar Interativo | `/placar` | Soma, subtrai e zera os pontos, sem permitir valores negativos. |

Todas as páginas podem ser acessadas pelo menu lateral. Os três componentes interativos incluem `@rendermode InteractiveServer` na segunda linha, imediatamente abaixo de `@page`.

## Executar

Instale o [SDK do .NET 10](https://dotnet.microsoft.com/download/dotnet/10.0). Na pasta do repositório, execute:

```bash
dotnet restore SiteUmBlazor.sln
dotnet watch --project SiteUmBlazor --launch-profile http
```

Abra **http://localhost:5190**. Para acessar a apresentação diretamente, use **http://localhost:5190/sobre**.

No Visual Studio com suporte ao .NET 10, abra `SiteUmBlazor.sln`, selecione o perfil `http` e pressione **F5**.

## Compilar

```bash
dotnet build SiteUmBlazor.sln --configuration Release
```

## Estrutura

- `SiteUmBlazor/Components/Pages/`: páginas dos exercícios.
- `SiteUmBlazor/Components/Layout/NavMenu.razor`: links de navegação com `NavLink`.
- `SiteUmBlazor/Program.cs`: configuração do Blazor e da interatividade no servidor.
- `SiteUmBlazor/wwwroot/app.css`: estilos e adaptação para telas pequenas.
- `.gitignore`: regras do Visual Studio para arquivos temporários e de compilação.

## Verificação da atividade

1. Acesse **Sobre Mim** e confira o nome completo e a descrição do curso.
2. No **Contador de Cliques**, confirme o valor inicial `0` e o incremento de uma unidade a cada clique.
3. No **Alternador de Mensagem**, confirme que a mensagem começa oculta; **Exibir Mensagem** deve mostrá-la e mudar o botão para **Ocultar Mensagem**. Clique novamente para ocultá-la.
4. No **Placar Interativo**, some e subtraia pontos. Subtraia novamente ao chegar a zero e confirme que o placar permanece em `0`. **Zerar Placar** deve reiniciar a pontuação.

## Autor e licença

Rafael Provezano. Projeto distribuído sob a [licença MIT](LICENSE).
