# 🛡️ Segurança, qualidade e operação

## 🔐 Controles de alto nível

O OdontoSync aplica autenticação, segundo fator, sessões com expiração e permissões de acordo com o papel da pessoa na equipe. Os serviços verificam o contexto do consultório e o vínculo clínico quando necessário.

As operações recebem validação no servidor, e ações relevantes são registradas para auditoria. A recuperação de conta utiliza um fluxo próprio de confirmação.

Esta apresentação descreve os controles de forma conceitual. Configurações, identificadores, segredos e procedimentos operacionais específicos permanecem privados.

## 📄 Integridade dos documentos

Receitas e pedidos de radiografia preservam as informações utilizadas na emissão. Rascunhos podem ser preparados e revisados pelo profissional responsável; a assinatura finaliza o documento e bloqueia sua edição.

A assinatura coletada na tela é uma imagem manuscrita. Este case não apresenta essa funcionalidade como certificação digital.

## 💾 Recuperação e continuidade

A aplicação oferece exportação cifrada por consultório e uma ferramenta de verificação da leitura e integridade dessa exportação. A existência do arquivo precisa ser acompanhada de procedimentos de armazenamento, controle de acesso e ensaios de recuperação.

Processos ampliados de recuperação e revisão independente continuam sendo frentes de evolução. Nenhuma cópia de dados ou exportação é incluída neste repositório.

## 🧪 Verificações realizadas

- Checagem de tipos e compilação da aplicação.
- Integração de autenticação, permissões e fluxos clínicos.
- Cenários de separação entre consultórios de teste e vínculo com pacientes.
- Preservação de documentos após mudanças cadastrais.
- Geração de PDFs simples e com várias páginas.
- Inspeção visual dos documentos e da interface em dimensões de tablet.

O sistema já é utilizado por um consultório com dois dentistas. Esse contexto de uso não substitui verificações adicionais nem permite afirmar resultados de produtividade ou desempenho sem medição.

## 🔒 Critérios da publicação pública

O case study inclui somente textos de apresentação e uma captura de ambiente de teste. Não inclui:

- Código-fonte da aplicação ou histórico do repositório privado.
- Credenciais, variáveis de ambiente ou configurações de produção.
- Identificadores de contas, bancos ou outros recursos de infraestrutura.
- Identidade do consultório real, dados de profissionais ou registros de pacientes.
- Bancos de dados, anexos clínicos, exportações ou backups.

[← Voltar ao case study](../README.md)
