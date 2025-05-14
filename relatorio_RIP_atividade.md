
# Análise do Projeto - RIP_atividade.pkt

Este é um pequeno relatório técnico que escrevi para documentar minha atividade de redes utilizando o Cisco Packet Tracer.

## 🧠 Objetivo

O objetivo foi criar uma rede com 4 roteadores, 4 computadores e múltiplas sub-redes. Utilizei o protocolo de roteamento dinâmico RIP (versão 2) para possibilitar a comunicação entre todas as redes.

## 🔧 O que eu fiz

- Criei 4 redes locais: `192.168.0.0/24`, `192.168.1.0/24`, `192.168.2.0/24`, `192.168.3.0/24`
- Interliguei os roteadores com redes intermediárias `200.200.X.0/24`
- Configurei os roteadores exclusivamente via CLI
- Utilizei apenas interfaces FastEthernet (sem links seriais)
- Ativei o RIP v2 com `version 2` e `no auto-summary` em todos os roteadores

## ✅ Acertos

- A maioria das interfaces foi corretamente configurada com IPs válidos e ativadas com `no shutdown`
- RIP foi corretamente ativado na maioria dos roteadores
- As redes locais dos PCs estavam configuradas corretamente em geral

## ⚠️ O que deu errado

- Percebi que algumas `network` statements estavam faltando no `router rip`, então algumas rotas não estavam sendo propagadas
- Algumas interfaces estavam com IPs incorretos ou fisicamente desconectadas no Packet Tracer
- Alguns PCs estavam com gateway padrão incorreto ou IP fora da faixa

## 🛠️ O que posso melhorar

- Conferir todas as interfaces com `show ip interface brief` para garantir que estão up/up
- Verificar a tabela de rotas com `show ip route` e garantir que todas as rotas remotas estão visíveis
- Sempre configurar corretamente o IP e o gateway nos PCs
- Salvar as configurações com `write memory` após terminar

## 🧪 Comandos úteis para testar

```bash
show running-config
show ip route
ping [destino]
tracert [destino]
```

## 📁 Arquivos

- `RIP_atividade.pkt`: arquivo do Packet Tracer com a topologia e configurações
- `Relatorio_RIP_Atividade.pdf`: versão em PDF deste relatório
- `README.md`: este documento

---

*Este repositório é parte do meu aprendizado em redes de computadores usando o Cisco Packet Tracer e roteamento dinâmico com RIP.*
