# ⚖️ Decisões técnicas e compromissos

## ☁️ Implantação serverless

**Objetivo:** concentrar a entrega da interface e dos serviços em uma operação de publicação simples.

**Implementação:** serviços em Cloudflare Workers, dados em D1 e assets estáticos entregues junto à aplicação.

**Implicação:** a evolução precisa considerar os limites da plataforma, o consumo e a compatibilidade entre aplicação e dados. A adoção atual por um consultório com dois dentistas não é apresentada como comprovação de capacidade em larga escala.

## 🧩 Interface por componentes

**Objetivo:** organizar formulários e comportamentos reutilizados em diferentes telas.

**Implementação:** componentes Angular e TypeScript para os fluxos de atendimento, com recursos compartilhados, como a coleta de assinatura e os campos de medicamentos.

**Implicação:** reutilização exige atenção ao estado de cada formulário, à troca de paciente e às ações que dependem de operações assíncronas.

## 🔐 Autorização nos serviços

**Objetivo:** controlar o acesso aos dados e às ações de acordo com as responsabilidades da equipe.

**Implementação:** verificações no servidor para perfil, consultório e vínculo clínico quando aplicável.

**Implicação:** testes precisam cobrir também tentativas de acesso indevido e operações em registros de outro contexto, além do fluxo permitido.

## 📄 Dados preservados por emissão

**Objetivo:** conservar o conteúdo de um documento após alterações nos cadastros.

**Implementação:** cada emissão registra os dados usados no documento. Receitas e radiografias possuem rascunhos editáveis pelo responsável e bloqueio de edição após assinatura.

**Implicação:** o histórico mantém informações próprias do momento da emissão. Correções em documentos finalizados exigem uma nova emissão.

## 💊 Modelo e prescrição individual

**Objetivo:** reutilizar orientações cadastradas sem restringir o preenchimento individual.

**Implementação:** o medicamento selecionado preenche os campos da receita; o profissional pode ajustar as instruções para aquele paciente.

**Implicação:** o catálogo e o documento possuem ciclos diferentes. Uma alteração na receita preserva o modelo; mudanças no modelo preservam receitas anteriores.

## 🖨️ PDF gerado no dispositivo

**Objetivo:** permitir a geração do arquivo a partir do documento salvo.

**Implementação:** montagem no navegador com identificação, conteúdo, assinatura e paginação.

**Implicação:** a qualidade depende de testes com textos longos, diferentes combinações de campos e inspeção visual. A assinatura manuscrita na tela não utiliza certificado digital.

## 🗃️ Evolução versionada dos dados

**Objetivo:** acrescentar funcionalidades preservando registros de um sistema já utilizado.

**Implementação:** migrações de banco versionadas e revisão da exportação quando novos domínios são incluídos.

**Implicação:** aplicação, dados e procedimentos de recuperação precisam evoluir de forma coordenada.

## 🧪 Validação em camadas

**Objetivo:** verificar a implementação sob diferentes perspectivas.

**Implementação:** tipos, compilação, cenários de integração, geração de documentos e conferência visual.

**Implicação:** cada verificação tem um escopo. Compilar com sucesso não substitui testes de fluxo, recuperação ou utilização em um dispositivo físico.

[← Voltar ao case study](../README.md)
