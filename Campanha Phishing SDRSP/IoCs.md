# Relatório de Indicadores de Comprometimento (IoCs)

Este documento fornece um resumo dos Indicadores de Comprometimento (IoCs) associados a uma recente campanha de phishing detectada na Secretaria de Desenvolvimento Regional de SP (SDRSP). Estes IoCs são cruciais para a identificação, prevenção e mitigação de futuras tentativas de ataque semelhantes.

## Resumo do Ataque

A campanha de phishing visava coletar informações financeiras através de e-mails fraudulentos que direcionavam as vítimas para sites maliciosos. Os e-mails continham um PDF anexado, personalizado com o nome completo e CPF do destinatário, e um link para um site de pagamento falso.

## IoCs Detalhados

### URLs Maliciosas

- `https://14022024433343.gatewaypagamentos.site/?cpf=[CPF da Vítima]`
- `https://app.gatewaypagamentos.site/govbr?cpf=[CPF da Vítima]` 
- `https://criador.gatewaypagamentos.site/typebots`
- `https://notificacaocreditosvrbb9.z24.web.core.windows.net/`
- `https://apps-resgates-info.online/`

### Análise Whois<br>
Domain: gatewaypagamentos.site<br>
Registrar: HOSTINGER operations, UAB<br>
Registered On: 2024-02-01<br>
Expires On: 2025-02-01<br>
Updated On: 2024-02-06<br>
Status: serverTransferProhibited / clientTransferProhibited<br>
Name Servers: stephane.ns.cloudflare.com / aaron.ns.cloudflare.com<br>

- Após redirecionamento: `https://portais.sdr.sp.gov.br/xmllrpc.php?cpf=[CPF da Vítima]`

### IPs Relacionados

- Inicial: `104.21.55.25:443`
- Pós-redirecionamento: `200.144.31.50:443`
- Principal: `172.67.144.35` (associado a Cloudflare, indicando o uso de serviços de privacidade para ocultar a origem real)

### Domínios Envolvidos

- Domínio principal: `gatewaypagamentos.site`

### Hashes de Arquivos

- **MD5 do PDF Anexado:** `80e970b133852f6c434bcc402cfe0c6c`
- **SHA-1 do PDF Anexado:** `d093d08fe3200c010f2002f361a260f09fca59a6`
- **SHA-256 do PDF Anexado:** `c99469ecc89d270d2f3c0cc7d174d115d68c52cec747e53e2713a2c5797d3271`

### Recomendações para Mitigação

- Bloqueio das URLs e IPs relacionados nas soluções de segurança perimetral.
- Atualização das regras de detecção de phishing em filtros de e-mail.
- Campanhas de conscientização para informar sobre as características deste tipo de ataque de phishing.

Este relatório é destinado à comunidade de segurança para facilitar a rápida identificação e resposta a ameaças similares.
