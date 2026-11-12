# Lab 01 · Handshake TCP e traceroute no Wireshark

- Aluno: Sérgio Ricardo dos Reis
- Sistema: Windows · interface wi-fi
- Data: 10/11/2026

## Minha rede (Passo 2)
- IP/máscara: (não preenchido)
- MAC: cc:d4.a1.d3.8d.7c
- Gateway: 192.168.1.1 · MAC do gateway (ARP reply): f4.7b.09.f9.bf.8c
- Servidor DNS: 172.67.167.77

## DNS (Passo 5)
- Registros A de www.cybersec.com.br: 104.21.16.109  172.67.167.77
- Transporte: UDP, porta 53

## Handshake (Passo 6)
- Conexão: (não preenchido):59249 → 172.67.167.77:443
- Frames SYN / SYN-ACK / ACK: 63/91/98 (flags 0x002, 0x012, 0x010)
- RTT do handshake: 331.526988200 ms

## Encapsulamento (Passo 7)
- Headers Ethernet / IP / TCP: 14/20/44 bytes
- MAC de destino do SYN é o MAC do gateway? Sim

## Caminho L3 (Passo 8)
- TTL do SYN-ACK: 56 · saltos estimados: 7
- Saltos no traceroute: 9
- Último salto = ip.dst do SYN? Sim
- Diferença: Bem, ambos medem a quantidade de roteadores intermediarios ( tipo saltos ) na camada 3 e... na prática . O traceroute mee a rota de ida, enquanto o TTL do Syn-Ack reflete a rota da volta. Variando de 1 a 3 saltos, creio que isto seja o que chama de roteamento assimétrico na internet.

## Problema enfrentado
Foi dificil, tive que entender conceitos minimos um por um, usei google p explicar alguns conceitos, e fui decifrando, e pouco a pouco foi abrindo o laboratorio de forma que eu consegui entender um básico que é o objetivo final.

## Debrief
mac é rg da placa de rede.. ip é o endereço lógico aonde vai atuar e Porta é o a parte efemera aleatoria aonde se atua exatamente.

Referências: RFC 9293 (TCP), RFC 791 (IPv4), RFC 792 (ICMP), RFC 826 (ARP), RFC 1035 (DNS).