# 🏗️ Arquitetura do OdontoSync

## 🎯 Visão geral

O OdontoSync é uma aplicação web com interface Angular, serviços em Cloudflare Workers e persistência em Cloudflare D1. Está em uso por um consultório com dois dentistas.

A arquitetura separa apresentação, regras de aplicação e dados. Esta documentação descreve essas responsabilidades em nível conceitual, sem publicar código, configurações ou estrutura física do banco.

## 🖥️ Interface

A interface reúne agenda, pacientes, prontuário, catálogos e documentos. Componentes e formulários conduzem o preenchimento e apresentam os resultados das operações.

O layout considera computadores e dispositivos de toque. Telas, indicadores e atalhos são reorganizados conforme o espaço disponível. A verificação responsiva utiliza o navegador; testes em dispositivos físicos continuam fazendo parte da evolução do produto.

## ⚙️ Serviços de aplicação

Os serviços processam autenticação, autorização, validação e regras de negócio. Entre suas responsabilidades estão verificar o acesso ao prontuário, respeitar a disponibilidade do profissional e registrar mudanças relevantes.

A interface apresenta as ações disponíveis para cada perfil. A autorização da operação é verificada no servidor antes do acesso ou da alteração dos registros.

## 🗃️ Organização dos dados

Os dados relacionam consultórios, usuários, pacientes, atendimentos e documentos. A separação por consultório é aplicada às operações e aos registros, e as alterações de estrutura são conduzidas por migrações versionadas.

O desenho considera atendimento por vários profissionais. O contexto atual de uso é um consultório com dois dentistas; a capacidade em outros cenários depende de testes e acompanhamento de consumo.

## 📄 Documentos

Documentos emitidos preservam os dados utilizados no preenchimento. Isso evita que uma alteração no cadastro modifique o conteúdo de uma receita ou pedido de exame anterior.

O PDF é montado no navegador a partir do registro correspondente. A implementação trata identificação, opções selecionadas, textos, assinaturas e paginação.

## 📧 Integração externa

O envio de mensagens de conta utiliza uma integração de e-mail. Essa responsabilidade é limitada a confirmação de cadastro e recuperação de senha, sem envio de prontuários.

## 🔎 Pontos de avaliação técnica

- Separação de responsabilidades entre interface, aplicação e persistência.
- Regras de acesso verificadas no servidor.
- Vínculo dos registros ao contexto do consultório.
- Evolução controlada da estrutura de dados.
- Preservação de documentos e histórico durante mudanças cadastrais.
- Tratamento dos documentos como parte do fluxo do atendimento.

[← Voltar ao case study](../README.md)
