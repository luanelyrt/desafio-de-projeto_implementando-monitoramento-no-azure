# Entrega do Desafio:

<br>

### Monitoramento no Azure

### Visão Geral

Azure Monitor unifica métricas, logs e diagnósticos de recursos em nuvem e ambientes híbridos.  
Permite detectar anomalias em tempo real, diagnosticar falhas e disparar automações.

### Componentes Principais

- **Metrics**  
  Coleta métricas de performance (CPU, memória, throughput) com resolução de até 1 minuto.  
- **Log Analytics Workspace**  
  Armazena e consulta logs e eventos via Kusto Query Language (KQL).  
- **Application Insights**  
  Telemetria de aplicações web e APIs: latência, disponibilidade e erros.  
- **Azure Alerts**  
  Cria regras para enviar notificações (e-mail, SMS, webhook) ou disparar runbooks.  
- **Azure Diagnostics**  
  Captura logs de sistema e aplicação em VMs, App Services e outros serviços PaaS.

### Configuração Rápida

1. No Portal ou CLI, **crie um Log Analytics Workspace**.  
2. **Associe recursos** (VM, AKS, App Service) para envio de métricas e logs.  
3. **Habilite Application/Container Insights** nos workloads desejados.  
4. Defina **Alert Rules** com thresholds e ações (e-mail, webhook, Logic Apps).  
5. Construa **dashboards** e **Workbooks** para visualização customizada.

### Boas Práticas

- Use convenções de nomenclatura padronizadas para workspaces e alertas.  
- Aplique **tags** em recursos para controle de custos e responsabilidades.  
- Reveja periodicamente thresholds para minimizar falsos positivos.  
- Ajuste políticas de retenção conforme compliance e necessidade de auditoria.  
- Crie **Workbooks** colaborativos para relatórios interativos.

### Otimização de Custo e Performance

- Monitore apenas métricas e logs essenciais ao negócio.  
- Ajuste a frequência de coleta com base na criticidade dos dados.  
- Exporte logs antigos para **Storage** de baixo custo ou Data Lake.  
- Empregue consultas KQL filtradas e parametrizadas para reduzir volume.  
- Prefira dash­boards dinâmicos em vez de múltiplos gráficos estáticos.

### Infraestrutura como Código & Automação

- Provisionamento via **Azure CLI**, **PowerShell**, **ARM Templates** ou **Bicep**.  
- Versione toda a configuração em repositório Git (Terraform, GitHub Actions).  
- Automatize respostas e playbooks usando **Logic Apps**, **Functions** ou **Runbooks**.  
- Integre pipelines CI/CD (Azure DevOps, GitHub Actions) para deploy consistente.
