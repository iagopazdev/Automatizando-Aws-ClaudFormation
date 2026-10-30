# Automatizando-Aws-ClaudFormation

# Implementando Infraestrutura Automatizada com AWS CloudFormation

## Sobre o Projeto

Este projeto foi desenvolvido durante o desafio da DIO com foco na implementação de Infraestrutura como Código (IaC) utilizando AWS CloudFormation.

O objetivo principal foi compreender como automatizar o provisionamento de infraestrutura na AWS através de templates declarativos, reduzindo erros manuais e garantindo a padronização dos ambientes.

---

## Conceitos Aplicados

- Infrastructure as Code (IaC)
- AWS CloudFormation
- Stack Management
- Provisionamento Automatizado
- Templates YAML
- Versionamento com Git e GitHub

---

## Arquitetura Implementada

A solução utiliza um template CloudFormation para automatizar a criação da infraestrutura.

Fluxo:

```text
CloudFormation Template
          │
          ▼
     AWS Stack
          │
          ▼
 Recursos Provisionados
```

---

## Estrutura do Projeto

```text
aws-cloudformation-dio
│
├── README.md
├── template.yaml
├── docs
└── images
```

---

## Template CloudFormation

O template desenvolvido possui uma estrutura simples para fins educacionais.

```yaml
AWSTemplateFormatVersion: '2010-09-09'
Description: Stack de exemplo para laboratório DIO

Resources:

  LabBucket:

    Type: AWS::S3::Bucket

    Properties:
      BucketName: !Sub dio-lab-${AWS::AccountId}
```

---

## Implantação da Stack

### Passo 1

Acessar o serviço CloudFormation.

### Passo 2

Selecionar:

```text
Create Stack
With new resources
```

### Passo 3

Realizar upload do template YAML.

### Passo 4

Definir nome da Stack.

Exemplo:

```text
dio-cloudformation-lab
```

### Passo 5

Executar a criação dos recursos.

---

## Resultados Obtidos

Após a implantação automática foi possível observar:

- Criação da Stack com sucesso;
- Validação do template;
- Gerenciamento centralizado dos recursos;
- Facilidade para replicação do ambiente.

---

## Benefícios do CloudFormation

### Padronização

Mantém a infraestrutura consistente entre ambientes.

### Automação

Reduz atividades manuais.

### Escalabilidade

Facilita criação de novos ambientes.

### Controle de Versão

Permite armazenar a infraestrutura diretamente em repositórios Git.

---

## Desafios Encontrados

Durante a execução do laboratório foram observados alguns pontos importantes:

- Necessidade de atenção à identação do YAML;
- Entendimento da estrutura Resources;
- Gerenciamento de permissões AWS;
- Validação do template antes da implantação.

---

## Aprendizados

Este desafio permitiu consolidar conhecimentos sobre:

- Infraestrutura como Código;
- Automação em ambientes Cloud;
- Boas práticas de documentação técnica;
- Utilização do GitHub como portfólio técnico.

---

## Evidências

Adicionar prints nesta seção.

### Criação da Stack

![Stack](images/stack-create.png)

### Recursos Provisionados

![Recursos](images/resources-created.png)

### Console CloudFormation

![Console](images/cloudformation-console.png)

---

## Referências

- AWS CloudFormation Documentation
- AWS Well-Architected Framework
- Documentação oficial da DIO

---

## Autor

Projeto desenvolvido para fins educacionais durante a Formação AWS da DIO.