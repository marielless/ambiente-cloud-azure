# Trabalhando com Ambiente Cloud  na Azure (Microsoft AZ-900)

Repositório com anotações pessoais das aulas **AZ-900: Microsoft Azure Fundamentals**. Aqui estão reunidos os principais conceitos abordados, organizados por tema, para facilitar a revisão e o aprendizado contínuo.

---

##  Introdução à Computação em Nuvem

#### 🔹 O que é Computação em Nuvem?
> É o fornecimento de serviços de computação pela internet, permitindo inovações mais rápidas, recursos flexíveis e economias de escala.

---

###  Modelos de Nuvem

####  Nuvem Privada
- Criada e mantida internamente pela própria organização.
- Operada dentro do datacenter da empresa.
- Acesso restrito apenas aos usuários internos.
- Controle total sobre recursos, segurança e conformidade.
- A organização é responsável pela manutenção e atualizações de hardware.

#### Nuvem Pública
- Propriedade de um provedor de serviços de nuvem (ex: Microsoft, AWS, Google).
- Compartilhada entre várias organizações e usuários.
- Acessada por conexão de rede segura (geralmente pela internet).
- Sem despesas de capital para escalar.
- Provisionamento e deprovisionamento rápido de aplicativos.
- Modelo de pagamento conforme o uso.

#### Nuvem Híbrida
- Combina nuvem pública e privada.
- Aplicativos executados no ambiente mais adequado.
- Permite controle sobre segurança, conformidade e requisitos legais.
- Oferece maior flexibilidade para as organizações.

---
 
##  Tipos de Despesas

###  CapEx (Despesas de Capital)
- Gasto inicial com infraestrutura física (servidores, equipamentos etc).
- Valor depreciado ao longo do tempo.

###  OpEx (Despesas Operacionais)
- Pagamento conforme o uso.
- Gasto com produtos e serviços sob demanda.
- Cobrança imediata, sem investimento inicial.

---

##  Modelo Baseado em Consumo

> Os provedores de nuvem operam sob um modelo baseado em consumo:  
> os usuários pagam **apenas pelos recursos utilizados**.

###  Benefícios
- Melhor previsibilidade de custos.
- Preço detalhado por recurso/serviço.
- Cobrança transparente baseada no uso real.

---

##  Casos de Uso por Modelo

- **Nuvem Privada**: Ideal para organizações com altos requisitos de segurança, controle e conformidade.
- **Nuvem Pública**: Boa escolha para startups, projetos escaláveis rapidamente e aplicações com demanda variável.
- **Nuvem Híbrida**: Indicada para empresas que precisam equilibrar dados sensíveis com serviços escaláveis na nuvem.

---
## Benefícios da Nuvem

### SLA
![Image](https://github.com/user-attachments/assets/e83fee5e-0b89-418c-b569-e42adf35f530)

### Domínio do Objetivo

> Descrever os benefícios da segurança, governança e capacidade de gerenciamento na nuvem

---

### Alta Disponibilidade
- Garante **acesso contínuo** aos serviços mesmo em falhas.
- Foco na **máxima disponibilidade**.

###  Escalabilidade
- Ajuste de recursos para atender à demanda.
- Escala vertical: adicionar CPU/RAM.
- Otimiza custos: paga-se **somente pelo que usa**.

### Elasticidade
- **Expansão e redução automática** dos recursos.
- Adição de VMs ou contêineres conforme necessidade.
- Redução automática durante baixa demanda.

### Confiabilidade
- Design descentralizado e resiliente.
- Recursos disponíveis em múltiplas regiões.
- Suporte a escala global.

### Previsibilidade
- Consistência em **desempenho** e **custos**.
- Guiada pelo **Microsoft Azure Well-Architected Framework**.

### Segurança
- Ferramentas avançadas de segurança.
- Patches automáticos (PaaS) e monitoramento.
- Implementações também são responsabilidade do cliente.

### Governança
- Auditoria contínua para identificar não conformidades.
- Aplicação automática de atualizações e patches.
- Governança proativa = ambiente atualizado e seguro.

---

###  Gerenciabilidade

**Gerenciamento de Recursos**
   - um dos principais beneficios da computação em nuvem são as opções de capacidade de gerenciamento. Há dois tipos de capacidade de gerenciamento para computação em nuvem

   > O gerenciamento da nuvem diz respeito a gerenciar seus recursos de nuvem. 
**Exemplo:**
   - Escalar automaticamente a implatação de recursos com base na necessidade.
   - Implantar recursos com base em um modelo pré-configurado, removendo a necessidade de configuração manual
---
## CONCEITOS DE NUVEM

### Tipos de serviço em nuvem:

**IaaS (Infraestrutura como Serviço):**
- Infraestrutura de TI com pagamento conforme o uso, alugando servidores, máquinas virtuais, armazenamento, redes e sistemas operacionais de um provedor de nuvem.
- Serviço de nuvem mais flexível.
- Você configura e gerencia o hardware para o seu aplicativo.

**PaaS (Plataforma como Serviço):**
- Fornece um ambiente para a criação, o teste e a implantação de aplicativos de software, sem focar no gerenciamento da infraestrutura subjacente.
- Focado no desenvolvimento de aplicativos.
- O gerenciamento da plataforma é realizado pelo provedor de nuvem.

**SaaS (Software como Serviço):**
- Os usuários se conectam e usam aplicativos baseados em nuvem pela internet.  
  **Exemplo:** Microsoft Office 365, e-mail e calendários.
- Modelo de preço com pagamento conforme o uso.
- Os usuários pagam pelo software que utilizam em um modelo de assinatura.

  # Componentes de Arquitetura do Azure

## Principais Componentes Arquitetônicos do Azure

### Regiões
![Image](https://github.com/user-attachments/assets/2770602f-9e16-414e-be38-dfb505bb4464)

- O Azure oferece mais regiões globais do que outro provedor de nuvem, com mais de 60 regiões representando mais de 140 países.
- As regiões são compostas de um ou mais datacenters muito próximos.
- Fornecem flexibilidade e escala para reduzir a latência do cliente.
- Preservam a residência dos dados com uma oferta abrangente de conformidade.

### Zonas de Disponibilidade
![Image](https://github.com/user-attachments/assets/214bf540-6be8-41cc-845d-751dc5d9daae)

- Fornecem proteção contra tempo de inatividade devido a falha do datacenter.
- Separação física entre datacenters dentro da mesma região.
- Cada datacenter é equipado com alimentação, resfriamento e rede independentes.
- Conectados por meio de redes privadas de fibra óptica.

### Pares de Regiões
![Image](https://github.com/user-attachments/assets/7dc0d8e3-46dc-477b-8588-c96c4199e1be)

- Mínimo de 300 milhas de separação entre pares de regiões.
- Replicação automática para alguns serviços.
- Recuperação de região priorizada em caso de interrupção.
- Atualizações são distribuídas sequencialmente para minimizar o tempo de inatividade.

🔗 [Saiba mais sobre Pares de Regiões do Azure](https://aka.ms/PairedRegions-ptb)

### Regiões Soberanas do Azure

#### Serviços Governamentais dos EUA
- Atende às necessidades de segurança e conformidade das agências federais, governos estaduais e locais dos EUA e seus provedores de soluções.

#### Azure Governamental
- Instância separada do Azure.
- Fisicamente isolada de implantações que não sejam do governo dos EUA.
- Acessível somente a pessoal verificado e autorizado.

#### Azure China
- A Microsoft é o primeiro provedor estrangeiro de serviços de nuvem pública da China, em conformidade com as regulamentações governamentais.
- Instância fisicamente separada dos serviços de nuvem do Azure operados pela 21Vianet.
- Inacessível para outras regiões.
- Todos os dados permanecem dentro da China para garantir conformidade.

## Recursos do Azure
![Image](https://github.com/user-attachments/assets/b5272346-528f-4a02-a5d0-437f148ab2ef)

- Componentes como armazenamento, máquinas virtuais e redes que estão disponíveis para criar soluções de nuvem.

## Grupo de Recursos
![Image](https://github.com/user-attachments/assets/06aba528-2332-4abb-b0fe-e44607c28324)

- Contêiner para gerenciar e agregar recursos em uma única unidade.
- Recursos podem existir em apenas um grupo de recursos.
- Recursos podem estar em diferentes regiões.
- É possível mover recursos entre grupos.
- Aplicativos podem utilizar múltiplos grupos de recursos.

## Assinaturas do Azure
![Image](https://github.com/user-attachments/assets/fe46be07-5ce2-4ee2-963e-20ddd13c9182)

- Fornece acesso autenticado e autorizado às contas do Azure.

**Limite de cobrança:** gera relatórios e faturas separadas para cada assinatura.  
**Limite de controle de acesso:** gerencia e controla os recursos que usuários podem provisionar.

---

## Grupos de Gerenciamento
![Image](https://github.com/user-attachments/assets/1e2c2207-9b1e-41b8-a916-93a9be5c00ae)

- Podem incluir várias assinaturas do Azure.
- As assinaturas herdam as condições aplicadas ao grupo de gerenciamento.



