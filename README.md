# Automatizando a Infraestrutura com AWS CloudFormation

> Projeto educacional desenvolvido durante um desafio da DIO para praticar **Infraestrutura como Código (IaC)** na AWS.

O objetivo é demonstrar como templates declarativos do AWS CloudFormation podem automatizar o provisionamento de recursos, reduzir tarefas manuais e padronizar ambientes.

## Navegação

- [Visão geral](#visao-geral)
- [Arquitetura](#arquitetura)
- [Estrutura do repositório](#estrutura-do-repositorio)
- [Exemplo de template](#exemplo-de-template)
- [Como implantar](#como-implantar)
- [Resultados e aprendizados](#resultados-e-aprendizados)
- [Evidências](#evidencias)
- [Referências](#referencias)

## Visão geral

| Item | Descrição |
|---|---|
| **Plataforma** | Amazon Web Services (AWS) |
| **Serviço** | AWS CloudFormation |
| **Abordagem** | Infraestrutura como Código (IaC) |
| **Formato do template** | YAML |
| **Contexto** | Desafio educacional da DIO |

### Conceitos praticados

- Infrastructure as Code (IaC);
- AWS CloudFormation e gerenciamento de stacks;
- Provisionamento automatizado de recursos;
- Templates declarativos em YAML;
- Versionamento com Git e GitHub.

## Arquitetura

O template descreve os recursos desejados. O CloudFormation interpreta essa definição e os provisiona como parte de uma stack.

```text
Template CloudFormation (YAML)
              │
              ▼
       Stack na AWS
              │
              ▼
     Recursos provisionados
```

## Estrutura do repositório

```text
Automatizando-Aws-ClaudFormation/
├── README.md
├── image.png
├── image-1.png
└── image-2.png
```

## Exemplo de template

O trecho abaixo ilustra uma stack simples que declara um bucket Amazon S3. Para implantá-lo, salve o conteúdo em um arquivo YAML, por exemplo `template.yaml`.

```yaml
AWSTemplateFormatVersion: '2010-09-09'
Description: Stack de exemplo para laboratório DIO

Resources:
  LabBucket:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: !Sub dio-lab-${AWS::AccountId}
```

## Como implantar

1. Acesse o serviço **AWS CloudFormation** no console da AWS.
2. Selecione **Create stack** e, em seguida, **With new resources (standard)**.
3. Faça upload do arquivo YAML com o template.
4. Informe um nome para a stack, por exemplo `dio-cloudformation-lab`.
5. Revise as configurações e avance até a criação da stack.
6. Acompanhe o status até a conclusão da implantação.

> **Atenção:** a criação de recursos pode gerar custos na AWS. Revise os recursos provisionados e remova a stack quando não precisar mais dela.

## Resultados e aprendizados

Durante o laboratório, foram praticados:

- Validação e organização de templates YAML;
- Uso da seção `Resources` para declarar recursos;
- Criação e gerenciamento de stacks;
- Atenção às permissões necessárias na AWS;
- Uso do GitHub para documentar e versionar um projeto de infraestrutura.

O CloudFormation também ajuda a manter ambientes consistentes, automatizar tarefas repetitivas e facilitar a replicação da infraestrutura.

## Evidências

As imagens disponíveis no repositório podem ser consultadas abaixo:

- [Imagem 1](image.png)
- [Imagem 2](image-1.png)
- [Imagem 3](image-2.png)

## Referências

- [AWS CloudFormation — documentação oficial](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/Welcome.html)
- [AWS Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html)
- Materiais da formação AWS da DIO.

## Autor

Projeto desenvolvido para fins educacionais durante a Formação AWS da DIO.
