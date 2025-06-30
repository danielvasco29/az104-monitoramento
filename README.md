# Monitoramento de Máquinas Virtuais no Azure

## 📌 Visão Geral
Este projeto demonstra como configurar monitoramento, criar alertas e consultar logs no Azure para máquinas virtuais.

## 🚀 Passos Realizados
- Criação de uma máquina virtual
- Ativação do diagnóstico de monitoramento
- Configuração do Log Analytics Workspace
- Criação de regras de alerta
- Simulação de exclusão de VM
- Consulta dos eventos no Log Analytics

## 🛠️ Ferramentas Utilizadas
- Azure Portal
- Azure Monitor
- Log Analytics
- Kusto Query Language (KQL)
- GitHub

## 📝 Exemplos de Consultas KQL
```kusto
AzureActivity
| where ResourceProvider == "Microsoft.Compute"
| where OperationNameValue == "Microsoft.Compute/virtualMachines/delete"
| project TimeGenerated, Caller, ResourceGroup, Resource
