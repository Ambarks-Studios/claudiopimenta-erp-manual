<div align="center">
  <img src="[https://i.ibb.co/1GnQZWKH/Sem-T-tulo-1-copiar.png](https://i.ibb.co/HDDLPz3y/Screenshot-1780483012.png)" alt="deez-logo"/>
</div>

# Manual de Instruções do Sistema Imobiliário

Este manual descreve como utilizar o sistema administrativo imobiliário, cobrindo acesso, navegação, módulos operacionais, permissões, documentos, relatórios e rotinas técnicas básicas.

## Sumário

- [1. Visão geral](#1-visão-geral)
- [2. Acesso ao sistema](#2-acesso-ao-sistema)
- [3. Navegação principal](#3-navegação-principal)
- [4. Permissões e cargos](#4-permissões-e-cargos)
- [5. Dashboard](#5-dashboard)
- [6. Clientes](#6-clientes)
- [7. Imóveis](#7-imóveis)
- [8. Processos](#8-processos)
- [9. Documentos](#9-documentos)
- [10. Aprovações](#10-aprovações)
- [11. Usuários](#11-usuários)
- [12. Cargos e permissões](#12-cargos-e-permissões)
- [13. Status de processo](#13-status-de-processo)
- [14. Relatórios](#14-relatórios)
- [15. Auditoria](#15-auditoria)
- [16. Boas práticas de uso](#16-boas-práticas-de-uso)
- [17. Rotina técnica básica](#17-rotina-técnica-básica)
- [18. Problemas comuns](#18-problemas-comuns)

## 1. Visão geral

O sistema centraliza a operação imobiliária em uma única área administrativa. Ele permite:

- Cadastrar e acompanhar clientes.
- Cadastrar imóveis e seus documentos.
- Criar processos vinculando cliente, imóvel e corretor.
- Acompanhar etapas do processo imobiliário.
- Anexar e baixar documentos.
- Solicitar e registrar aprovações.
- Gerenciar usuários, cargos, permissões e status de processo.
- Exportar relatórios em PDF, XLSX e CSV.
- Consultar auditoria de ações realizadas no sistema.

O acesso às telas depende das permissões do cargo do usuário. Se um módulo não aparecer no menu lateral, o usuário provavelmente não possui a permissão necessária.

## 2. Acesso ao sistema

1. Abra a URL do sistema no navegador.
2. Na tela de login, informe `E-mail` e `Senha`.
3. Clique em `Entrar`.
4. Após a autenticação, o sistema carrega os módulos permitidos para o seu cargo.

Regras importantes:

- Apenas usuários com status `Ativo` conseguem entrar.
- Usuários `Inativos` ou `Bloqueados` recebem erro de acesso.
- Ao terminar o uso, clique em `Sair` no menu lateral.
- Caso a sessão expire, entre novamente com e-mail e senha.

## 3. Navegação principal

O sistema usa um menu lateral com os módulos disponíveis para o usuário logado.

Módulos principais:

- `Dashboard`: indicadores gerais da operação.
- `Clientes`: cadastro, consulta e documentos de clientes.
- `Imóveis`: cadastro, consulta e documentos de imóveis.
- `Processos`: fluxo comercial e operacional.
- `Aprovações`: solicitações de decisão vinculadas a processos.
- `Usuários`: cadastro e controle de acesso da equipe.
- `Cargos`: gerenciamento de cargos e permissões.
- `Status`: configuração das etapas do processo.
- `Relatórios`: exportações em PDF, Excel e CSV.
- `Auditoria`: histórico de ações do sistema.

Na parte superior há uma busca global. Ela pesquisa clientes, imóveis e processos a partir de termos com pelo menos 2 caracteres.

## 4. Permissões e cargos

As permissões controlam o que cada usuário pode visualizar ou executar.

Permissões principais:

- `dashboard.view`: visualizar Dashboard.
- `search.read`: usar busca global.
- `clients.create`, `clients.read`, `clients.edit`, `clients.delete`: criar, visualizar, editar e excluir clientes.
- `properties.create`, `properties.read`, `properties.edit`, `properties.delete`: criar, visualizar, editar e excluir imóveis.
- `processes.create`, `processes.read`, `processes.edit`, `processes.delete`: criar, visualizar, editar e excluir processos.
- `documents.upload`, `documents.download`, `documents.delete`: enviar, baixar e excluir documentos.
- `approvals.create`, `approvals.read`, `approvals.edit`, `approvals.delete`: criar, visualizar, decidir e excluir aprovações.
- `users.create`, `users.read`, `users.edit`, `users.delete`: gerenciar usuários.
- `roles.manage`: gerenciar cargos.
- `permissions.manage`: gerenciar permissões via API.
- `process_statuses.manage`: gerenciar status e etapas de processo.
- `reports.export`: exportar relatórios.
- `audit.read`: visualizar auditoria.

Cargos iniciais configurados pelo sistema:

- `Administrador`: possui todas as permissões.
- `Corretor`: opera clientes, processos e documentos básicos.
- `Supervisor`: opera clientes, imóveis, processos, documentos e aprovações de leitura.
- `Analista`: consulta e edita clientes/processos, envia documentos e cria aprovações.
- `Financeiro`: consulta dados, decide aprovações e exporta relatórios.
- `Engenharia`: consulta imóveis/processos e atua em etapas técnicas.
- `Diretoria`: consulta dados estratégicos, aprova decisões, exporta relatórios e acessa auditoria.

Observação: a exibição de cada item do menu depende da permissão específica usada pela tela. Por exemplo, o menu `Relatórios` aparece para usuários com `reports.export`.

## 5. Dashboard

O Dashboard apresenta um resumo da operação.

Indicadores exibidos:

- Total de clientes.
- Total de processos.
- Novos clientes no mês.
- Novos processos no mês.
- Aprovações pendentes.
- Documentos anexados no mês.
- Processos sem documentos.

Áreas do Dashboard:

- `Cadastros por mês`: gráfico com clientes, processos e imóveis criados nos últimos meses.
- `Anotações`: bloco pessoal para registrar lembretes. As anotações ficam salvas no navegador do usuário.
- `Processos recentes`: últimos processos criados.
- `Aprovações em espera`: aprovações pendentes.
- `Documentos recentes`: últimos documentos anexados.
- `Fila por etapa`: quantidade de processos por status.
- `Atenção operacional`: pontos que exigem acompanhamento.

## 6. Clientes

Use `Clientes` para cadastrar compradores, vendedores ou outros envolvidos no processo.

### 6.1 Cadastrar cliente

1. Acesse `Clientes`.
2. Clique em `Novo`.
3. Preencha os campos obrigatórios e os dados complementares disponíveis.
4. Clique em `Salvar`.

Campos principais:

- `Nome completo` obrigatório.
- `CPF`, `RG`, `Passaporte`.
- `Data de nascimento`, `Nacionalidade`, `Estado civil`, `Profissão`.
- `E-mail`, `Telefone`, `Celular`, `WhatsApp`.
- Endereço: `CEP`, `Rua`, `Número`, `Complemento`, `Bairro`, `Cidade`, `Estado`, `País`.
- Renda e crédito: `Renda mensal`, `Empresa atual`, `Tempo de emprego`, `Status de Crédito`.
- Situação: `Status`.

Status do cliente:

- `Ativo`.
- `Em análise`.
- `Aprovado`.
- `Reprovado`.

Status de crédito:

- `Aprovado`.
- `Pendente`.
- `Negado`.
- `Aguardando`.

Regras:

- O CPF é normalizado e não pode estar duplicado em clientes ativos.
- O campo `Nome completo` é obrigatório.

### 6.2 Editar cliente

1. Acesse `Clientes`.
2. Localize o cliente na lista ou use a busca.
3. Clique em `Editar`.
4. Atualize os dados.
5. Clique em `Salvar`.

### 6.3 Excluir cliente

1. Acesse `Clientes`.
2. Clique em `Excluir`.
3. Confirme a exclusão.

Ao excluir um cliente, os documentos associados também são removidos.

### 6.4 Documentos do cliente

Dentro do cadastro do cliente é possível anexar documentos se o usuário tiver permissão de upload.

Tipos comuns:

- `RG frente`.
- `RG verso`.
- `CPF`.
- `Passaporte`.
- `CNH`.
- `Comprovante de residência`.
- `Comprovante de renda`.
- `Contratos`.
- `Fotos`.
- `Plantas`.
- `Laudos`.
- `Escrituras`.
- `Arquivo personalizado`.

Para anexar:

1. Abra o cadastro do cliente.
2. Selecione o tipo do documento.
3. Preencha `Tipo personalizado` se necessário.
4. Selecione um ou mais arquivos.
5. Clique em `Enviar documento`.

## 7. Imóveis

Use `Imóveis` para cadastrar a carteira imobiliária.

### 7.1 Cadastrar imóvel

1. Acesse `Imóveis`.
2. Clique em `Novo`.
3. Preencha os dados do imóvel.
4. Clique em `Salvar`.

Campos principais:

- `Código interno` obrigatório. Pode ser gerado pelo botão `Gerar`.
- `Título` obrigatório.
- `Tipo` obrigatório.
- `Categoria`.
- `Finalidade` obrigatória.
- `Status` obrigatório.
- `Valor` obrigatório.
- `Área total`.
- `Área construída`.
- Endereço: `CEP`, `Rua`, `Número`, `Bairro`, `Cidade`, `Estado`.

Status do imóvel:

- `Disponível`.
- `Reservado`.
- `Em negociação`.
- `Vendido`.
- `Alugado`.
- `Cancelado`.

Regras:

- O código interno não pode estar duplicado em imóveis ativos.
- Se nenhum código for informado no backend, o sistema pode gerar um código automaticamente.

### 7.2 Editar imóvel

1. Acesse `Imóveis`.
2. Localize o imóvel.
3. Clique em `Editar`.
4. Atualize os dados.
5. Clique em `Salvar`.

### 7.3 Excluir imóvel

1. Acesse `Imóveis`.
2. Clique em `Excluir`.
3. Confirme a exclusão.

Ao excluir um imóvel, os documentos associados também são removidos.

### 7.4 Documentos do imóvel

Os documentos de imóvel são anexados após salvar o cadastro.

Tipos sugeridos para imóvel:

- `Inteiro Teor`.
- `Laudo de Engenharia`.
- `Arquivo personalizado`.

## 8. Processos

O módulo `Processos` controla o fluxo operacional de uma negociação ou atendimento imobiliário.

### 8.1 Criar processo

1. Acesse `Processos`.
2. Clique em `Novo`.
3. Selecione o `Cliente`.
4. Selecione o `Imóvel`.
5. Selecione o `Corretor responsável`.
6. Preencha a `Descrição`, se necessário.
7. Clique em `Salvar`.

Regras:

- Cliente, imóvel e corretor são obrigatórios.
- O protocolo é gerado automaticamente com base no imóvel.
- O processo inicia no status padrão configurado no módulo `Status`.

### 8.2 Consultar processo

Na lista de processos são exibidos:

- `Protocolo`.
- `Cliente`.
- `Imóvel`.
- `Corretor`.
- `Status`.

Clique em `Perfil` para abrir o painel completo do processo.

### 8.3 Perfil do processo

O perfil reúne todas as informações relevantes:

- Dados do processo.
- Dados do cliente.
- Dados do imóvel.
- Etapas do processo.
- Documentos anexados.
- Aprovações vinculadas.
- Timeline de movimentações.
- Comentários.

### 8.4 Etapas do processo

O fluxo padrão é:

1. Documentos clientes.
2. Documentos vendedor.
3. Conta Vendedor.
4. Conta comprador.
5. Entrevista Banco.
6. Documentos imóvel.
7. Laudo engenharia.
8. Conformidade.
9. Assinatura Contrato.
10. ITBI.
11. Cartório.
12. Devolução Contrato Banco.
13. Conclusão.

As etapas são baseadas nos status cadastrados no módulo `Status`. Para marcar uma etapa como concluída, o usuário precisa ter permissão `processes.edit`.

Na etapa final, o sistema permite selecionar um status final, como:

- `Cancelado`.
- `Finalizado`.
- `Completo`.

Quando um status final é selecionado, outros status finais marcados anteriormente são removidos do processo.

### 8.5 Documentos do processo

No perfil do processo:

1. Vá até `Documentos anexados`.
2. Selecione o tipo do documento.
3. Informe um tipo personalizado se necessário.
4. Selecione os arquivos.
5. Clique em `Anexar`.

Também é possível baixar ou excluir documentos conforme a permissão do usuário.

### 8.6 Comentários do processo

No perfil do processo:

1. Digite o comentário.
2. Marque ou desmarque a opção `Interno`.
3. Clique em `Comentar`.

Comentários ficam registrados no histórico do processo.

## 9. Documentos

Os documentos são anexados a clientes, imóveis ou processos.

Tipos de arquivo aceitos:

- `pdf`.
- `jpg`, `jpeg`, `png`, `webp`.
- `doc`, `docx`.
- `xls`, `xlsx`.
- `csv`.
- `txt`.

Limites e regras:

- Cada arquivo pode ter até 50 MB pela validação da aplicação.
- Os arquivos são armazenados criptografados.
- Cada novo envio para o mesmo tipo de documento gera uma nova versão.
- Downloads registram histórico e auditoria.
- A exclusão de um documento remove o arquivo do storage e registra histórico.

## 10. Aprovações

O módulo `Aprovações` registra decisões vinculadas a processos.

### 10.1 Criar aprovação

1. Acesse `Aprovações`.
2. Clique em `Novo`.
3. Selecione o processo.
4. Preencha a observação, se necessário.
5. Clique em `Salvar`.

A aprovação nasce com status `Pendente`.

### 10.2 Decidir aprovação

1. Acesse `Aprovações`.
2. Clique em `Editar` na aprovação desejada.
3. Escolha o status:
   - `Pendente`.
   - `Aprovado`.
   - `Reprovado`.
   - `Cancelado`.
4. Preencha a observação da decisão, se necessário.
5. Clique em `Salvar`.

Quando o status passa para `Aprovado`, `Reprovado` ou `Cancelado`, o sistema registra o usuário decisor e a data da decisão.

### 10.3 Excluir aprovação

Somente aprovações pendentes podem ser excluídas.

## 11. Usuários

Use `Usuários` para controlar quem acessa o sistema.

### 11.1 Criar usuário

1. Acesse `Usuários`.
2. Clique em `Novo`.
3. Preencha:
   - `Nome`.
   - `E-mail`.
   - `Status`.
   - `CPF`, `Telefone`, `Cargo interno`, se necessário.
   - `Cargo RBAC`.
   - `Senha`.
4. Clique em `Salvar`.

Regras:

- Nome, e-mail, status e senha são obrigatórios na criação.
- A senha deve ter pelo menos 8 caracteres.
- E-mail e CPF não podem estar duplicados.
- Usuários só conseguem entrar quando o status é `Ativo`.

### 11.2 Editar usuário

1. Acesse `Usuários`.
2. Clique em `Editar`.
3. Atualize os dados.
4. Para manter a senha atual, deixe o campo `Senha` vazio.
5. Clique em `Salvar`.

### 11.3 Excluir usuário

1. Acesse `Usuários`.
2. Clique em `Excluir`.
3. Confirme a exclusão.

O sistema não permite que o usuário logado exclua o próprio cadastro.

## 12. Cargos e permissões

Use `Cargos` para definir perfis de acesso.

### 12.1 Criar cargo

1. Acesse `Cargos`.
2. Clique em `Novo`.
3. Informe o nome e a descrição.
4. Marque as permissões desejadas em cada módulo.
5. Clique em `Salvar`.

### 12.2 Editar cargo

1. Acesse `Cargos`.
2. Clique em `Editar`.
3. Ajuste nome, descrição ou permissões.
4. Clique em `Salvar`.

### 12.3 Excluir cargo

Cargos do sistema ou cargos vinculados a usuários não podem ser excluídos.

## 13. Status de processo

Use `Status` para configurar as etapas disponíveis no fluxo de processos.

Campos:

- `Nome`.
- `Cor`.
- `Ordem`.
- `Padrão`.
- `Final`.
- `Ativo`.

Regras:

- Apenas um status pode ser marcado como padrão.
- Status final representa encerramento ou conclusão de processo.
- Status inativo não pode ser alterado no perfil do processo.
- Status em uso por processos não pode ser excluído.

Cuidados:

- O nome do status deve corresponder às etapas do fluxo para aparecer corretamente na timeline.
- A ordem define a sequência de exibição e organização do pipeline.

## 14. Relatórios

O módulo `Relatórios` permite exportar dados nos formatos:

- `PDF`.
- `XLSX`.
- `CSV`.

Relatórios disponíveis:

- Clientes.
- Imóveis.
- Processos.
- Aprovações.
- Usuários.

Para exportar:

1. Acesse `Relatórios`.
2. Localize o relatório desejado.
3. Clique no formato desejado.
4. O arquivo será baixado pelo navegador.

## 15. Auditoria

O módulo `Auditoria` exibe registros das ações importantes realizadas no sistema.

Informações exibidas:

- Data.
- Usuário.
- Ação.
- IP.

Exemplos de ações auditadas:

- Login e logout.
- Criação, edição e exclusão de clientes.
- Criação, edição e exclusão de imóveis.
- Criação, edição e exclusão de processos.
- Alteração de etapas de processo.
- Upload, download e exclusão de documentos.
- Criação e decisão de aprovações.
- Alterações de cargos e permissões.
- Alterações de status de processo.

## 16. Boas práticas de uso

- Mantenha clientes e imóveis atualizados antes de criar processos.
- Anexe documentos diretamente ao registro correto: cliente, imóvel ou processo.
- Use o campo `Tipo personalizado` quando o tipo padrão não representar o arquivo.
- Registre comentários no perfil do processo para preservar o contexto operacional.
- Evite excluir cadastros com histórico relevante; prefira bloquear ou inativar usuários quando aplicável.
- Revise permissões sempre que um usuário trocar de função.
- Use status finais apenas quando o processo realmente estiver encerrado.

## 17. Problemas comuns

### Login não funciona

Verifique:

- E-mail e senha.
- Status do usuário.
- Se o administrador inicial foi criado.

### Módulo não aparece no menu

Verifique:

- Cargo do usuário.
- Permissões vinculadas ao cargo.
- Se o usuário está usando o cargo correto.

### Documento não envia

Verifique:

- Permissão `documents.upload`.
- Tamanho do arquivo.
- Extensão permitida.
- Configuração de `DOCUMENTS_DISK`.
- Credenciais S3, se aplicável.

### Relatório não baixa

Verifique:

- Permissão `reports.export`.
- Se há dados cadastrados.
- Logs da aplicação.

### Status não aparece corretamente na timeline

Verifique:

- Se o status está ativo.
- Se o nome corresponde à etapa esperada.
- Se a ordem está configurada corretamente.
- Se existe status padrão para novos processos.

