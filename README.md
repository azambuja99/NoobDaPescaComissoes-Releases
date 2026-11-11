# Noob da Pesca Comissões — Instalação e atualizações

Distribuição pública dos instaladores para Windows x64. Este repositório contém apenas documentação e arquivos de distribuição; o desenvolvimento e o código-fonte ficam em repositório privado.

## Baixar e instalar

1. Abra [Releases](https://github.com/azambuja99/NoobDaPescaComissoes-Releases/releases).
2. Escolha a versão e baixe `NoobDaPesca-Setup-VERSAO-win-x64.exe`.
3. Execute o instalador. O aplicativo e o .NET ficam instalados somente para seu usuário, sem exigir instalação separada do runtime.
4. Informe o endereço HTTPS da API fornecido pelo administrador. Se ainda não recebeu esse endereço, pode configurar depois executando novamente o instalador.

Requer Windows x64, Windows 10 versão 1809 ou superior. O instalador atual não possui assinatura digital de editor.

## Atualizar uma instalação

Feche o programa e execute o instalador da nova versão. Ele atualiza a mesma instalação, mantendo o endereço da API salvo para o usuário. Não é necessário desinstalar a versão anterior.

As atualizações são baixadas e instaladas manualmente pela página de Releases. Os dados de negócio permanecem no servidor; o instalador não distribui nem altera o banco de dados.

## Verificar o download

Cada release inclui `SHA256SUMS.txt`. No PowerShell:

```powershell
Get-FileHash .\NoobDaPesca-Setup-VERSAO-win-x64.exe -Algorithm SHA256
```

Compare o resultado com o hash do mesmo arquivo listado em `SHA256SUMS.txt`.

## Estado do sistema

A versão 0.1.1 é uma pré-release de homologação. Inclui acesso por usuário e senha, produtos, compras, estoque, vendas e geração de comissões sobre o lucro. Pagamento de comissões e dashboard ainda estão pendentes. A API precisa ser disponibilizada e configurada pelo administrador para usar o cliente instalado.

Nenhuma senha, credencial, certificado privado ou configuração do banco é publicada neste repositório.
