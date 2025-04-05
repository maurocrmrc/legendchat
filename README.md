# LegendChat

Aplicação para visualizar jogadores no mesmo lobby do League of Legends.

## Funcionalidades

- Visualização de jogadores no lobby
- Detecção de partidas em andamento
- Status dos jogadores durante a partida

## Modos de Uso

### Modo Local

1. Clone o repositório
2. Instale as dependências: `npm install`
3. Inicie o aplicativo: `npm start`
4. Acesse no navegador: `http://localhost:3000`

### Modo Remoto

Para acessar o LegendChat a partir de outro computador:

1. Execute o servidor em um computador com League of Legends instalado: `npm start`
2. Obtenha o endereço IP deste computador
3. Em outro computador, acesse: `http://IP-DO-SERVIDOR:3000`
4. Selecione o servidor remoto na interface

### Versão Executável

Para distribuir o LegendChat como executável:

1. Gere o executável: `npm run prepare-release`
2. O arquivo .exe estará disponível em `public/download/`
3. Hospede o executável em uma das plataformas recomendadas
4. Atualize os links na página de apresentação (landing.html)

## Publicando no GitHub Releases

### Preparação

1. Certifique-se de ter o Node.js e pkg instalados
2. Execute `npm run prepare-release` para gerar o executável e os arquivos de suporte
3. O script irá gerar `LegendChat-vX.Y.Z.exe` na pasta `public/download/`

### Publicação no GitHub

1. Crie um repositório no GitHub (ou use um existente)
2. Faça push do código para o repositório
3. Acesse a seção "Releases" no GitHub (https://github.com/seu-usuario/legendchat/releases)
4. Clique em "Draft a new release"
5. Preencha os campos:
   - Tag version: `vX.Y.Z` (ex: v1.0.0)
   - Release title: `LegendChat vX.Y.Z`
   - Descrição: Cole o conteúdo do arquivo CHANGELOG.md gerado
6. Arraste o arquivo .exe da pasta `public/download/` para o campo de upload
7. Clique em "Publish release"

### Atualizando Links de Download

Após a publicação, o executável estará disponível nas seguintes URLs:
- Versão específica: `https://github.com/seu-usuario/legendchat/releases/download/vX.Y.Z/LegendChat-vX.Y.Z.exe`
- Última versão: `https://github.com/seu-usuario/legendchat/releases/latest/download/LegendChat-vX.Y.Z.exe`

A página de landing do LegendChat já está configurada para buscar automaticamente a última versão.

## Hospedagem do Executável

O executável .exe do LegendChat pode ser hospedado gratuitamente em várias plataformas:

### GitHub Releases (Recomendado)

1. Crie uma conta no [GitHub](https://github.com)
2. Crie um repositório para o LegendChat
3. Vá até a seção "Releases" do repositório
4. Crie uma nova versão (release) e faça upload do .exe
5. A URL será algo como: `https://github.com/seuusuario/legendchat/releases/download/v1.0.0/LegendChat-v1.0.0.exe`

Vantagens do GitHub Releases:
- Até 2GB por arquivo
- Download direto sem anúncios
- Controle de versões
- Alta confiabilidade e velocidade

### Outras Opções

- **Google Drive**: 15GB gratuitos, fácil compartilhamento
- **MediaFire**: 10GB gratuitos, links diretos para download
- **OneDrive**: 5GB gratuitos, integração com contas Microsoft

## Requisitos

- Node.js 14+
- League of Legends instalado (para modo local)

## Configuração Avançada

Para conexão remota, você precisa:

1. Garantir que a porta 3000 está liberada no firewall
2. Usar o endereço IP privado da rede ou configurar port forwarding para acesso externo

## Solução de Problemas

Se tiver dificuldades para conectar remotamente:

1. Verifique se o servidor está rodando: `npm run diagnose`
2. Teste se a porta está acessível: `telnet IP-DO-SERVIDOR 3000`
3. Verifique as configurações de firewall do sistema
