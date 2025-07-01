# BootCamp_AZ-104_DIO.ME
Projeto para o BootCamp AZ-104 da DIO.me

O Azure Front Door e o Azure Application Gateway têm propósitos parecidos — ambos lidam com o tráfego HTTP(S) — mas atendem a cenários bem diferentes. A

Resumo prático:
    Use Azure Front Door se sua aplicação for voltada a usuários ao redor do mundo e você quiser entregar a melhor performance global.
    Prefira o Application Gateway se você precisa de inspeção mais profunda no tráfego dentro de uma rede virtual, como num ambiente com múltiplos serviços internos em Azure.


O Azure Application Gateway é uma solução de balanceamento de carga do tipo Layer 7 (camada de aplicação), o que significa que ele entende os protocolos HTTP e HTTPS e consegue tomar decisões com base no conteúdo das requisições.

Aqui vai um resumo dos principais recursos e diferenciais dele:
🎯 Roteamento baseado em URL e host

Você pode configurar regras para que diferentes caminhos de URL ou domínios sejam roteados para diferentes backends. Por exemplo:

    site.com/imagens → grupo de servidores para imagens
    api.site.com → outro grupo para APIs

🔐 Web Application Firewall (WAF)

O Application Gateway pode vir com o WAF ativado, que protege seu aplicativo contra vulnerabilidades comuns, como injeção de SQL, scripts maliciosos (XSS) e outras ameaças identificadas pelo OWASP.
📈 Escalabilidade e alta disponibilidade

Ele é capaz de escalar automaticamente conforme o tráfego aumenta. Também permite ter múltiplas instâncias e zonas de disponibilidade para garantir resiliência.
⚡ Terminação SSL (TLS)

Você pode configurar certificados SSL no Gateway, e ele faz a descriptografia do tráfego antes de enviá-lo aos servidores de backend — isso reduz a carga nas suas máquinas virtuais e simplifica a gestão dos certificados.
💬 Suporte a WebSocket e HTTP/2

Isso é ótimo para aplicações modernas que exigem conexões persistentes ou comunicação mais eficiente entre cliente e servidor.
🛣️ Reescrita de cabeçalhos e redirecionamentos

Você pode modificar cabeçalhos HTTP, implementar regras de redirecionamento (como forçar HTTPS), entre outras configurações avançadas.


🛰️ Azure Front Door – Quando o mundo é seu palco:

    Sites e APIs voltados para o público global: entrega rápida e otimizada onde quer que o usuário esteja.
    Plataformas de e-commerce ou SaaS que precisam de disponibilidade global e failover automático entre regiões.
    Aceleração de performance com caching em borda e compressão automática.
    Proteção DDoS e WAF no edge, com resposta rápida a ameaças antes mesmo de chegar à sua rede.
    Aplicações modernas em arquitetura distribuída, como microserviços hospedados em diferentes regiões do Azure ou até híbridos com on-premises.

🛡️ Azure Application Gateway – Quando o foco é rede e segurança interna:

    Ambientes corporativos internos, com aplicações acessadas somente dentro da organização.
    Microsserviços conectados por Azure Virtual Network (VNet), onde você precisa de inspeção profunda (camada 7) e regras de roteamento complexas.
    Ambientes com integração a Azure Kubernetes Service (AKS) via o Application Gateway Ingress Controller.
    Soluções que exigem autenticação por certificados de cliente, além de roteamento interno detalhado.
    Aplicações em regiões específicas, onde o tráfego não precisa ser roteado globalmente.
