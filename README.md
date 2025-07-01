# BootCamp_AZ-104_DIO.ME

Para garantir visibilidade, controle e resposta proativa em eventos críticos no Azure, você pode montar uma estratégia baseada em boas práticas de governança e automação. Aqui vai uma lista bem estruturada com demonstrações práticas:

🌩️ Visibilidade: veja tudo o que importa
Azure Monitor Configure a coleta de métricas e logs de recursos como VMs, bancos de dados e aplicações. 👉 Exemplo: Habilite o Log Analytics para coletar logs de desempenho e diagnosticar anomalias.

Azure Activity Log Use para rastrear ações administrativas em todo o ambiente. 👉 Exemplo: Notifique alterações em grupos de segurança via Event Grid.

Azure Service Health Receba alertas sobre problemas que afetam seus serviços em regiões específicas. 👉 Exemplo: Configure notificações por e-mail ou Teams para interrupções regionais.

🛡️ Controle: defina as regras do jogo
Azure Policy Estabeleça padrões e verifique a conformidade automaticamente. 👉 Exemplo: Bloqueie a criação de recursos fora da região “Brazil South”.

Role-Based Access Control (RBAC) Limite acessos com base em funções específicas. 👉 Exemplo: Conceda apenas “Leitor” a usuários que não devem fazer alterações.

Azure Blueprints Padronize a implantação de recursos com configurações seguras e auditáveis. 👉 Exemplo: Crie um blueprint com políticas, grupos de recursos e permissões pré-definidas.

⚙️ Resposta proativa: agir antes do problema virar crise
Azure Alerts Configure alertas com base em métricas ou logs para ações automáticas. 👉 Exemplo: Se a CPU da VM ultrapassar 90%, envie alerta e execute script de scale-out.

Azure Automation + Runbooks Automatize respostas a eventos comuns. 👉 Exemplo: Detecção de VM inativa dispara runbook que desliga a máquina para economizar custo.

Azure Sentinel (SIEM) Detecte ameaças, investigue e responda a incidentes com inteligência. 👉 Exemplo: Use regras analíticas para identificar tentativas de login suspeitas e acionar bloqueios automáticos.
