## Objetivo

O objetivo foi criar uma rede com 4 roteadores, 4 computadores e múltiplas sub-redes. Utilizei o protocolo de roteamento dinâmico RIP (versão 2) para possibilitar a comunicação entre todas as redes.

## 🔧 O que eu fiz

- Criei 4 redes locais: `192.168.0.0/24`, `192.168.1.0/24`, `192.168.2.0/24`, `192.168.3.0/24`
- Interliguei os roteadores com redes intermediárias `200.200.X.0/24`
- Configurei os roteadores exclusivamente via CLI
- Utilizei apenas interfaces FastEthernet (sem links seriais)
- Ativei o RIP v2 com `version 2` e `no auto-summary` em todos os roteadores


## Comandos úteis para testar

```bash
show running-config
show ip route
ping [destino]
tracert [destino]
```

## Arquivos

- `RIP_atividade.pkt`: arquivo do Packet Tracer com a topologia e configurações
- `relatorio_RIP_atividade.md`: este documento

---
