
## **Sistemas finais e Sistemas Intermediários**

**Sistemas Finais** são dispositivos que estão na extremidade da rede e que são a origem ou o destino final dos dados. Exemplos: PCs, celulares, servidores, impressoras, consoles. Responsáveis por iniciar e finalizar as comunicações de rede.
**Sistemas Intermediários** são dispositivos que não são a origem nem o destino final dos dados, mas que ajudam a encaminhar os dados de uma origem a um destino. Exemplos: Roteadores, switches, hubs, bridges.

## Camada de Transporte

Responsável pela comunicação de ponta a ponta entre dispositivos. Parte totalmente de software.

Garante a entrega confiável dos dados, controla de fluxo e correção de erros entre sistemas finais.

Transforma dados de aplicações em segmentos ou datagramas para transmissão e assegura que cheguem corretamente ao destino.

Adiciona cabeçalhos que contêm:

- Portas de origem e destino
- Número de sequência e reconhecimento
- Controle de fluxo e janelas de congestionamento
- Verificação de integridade (checksum)

Principais funcionalidades:

- **Estabelecimento e terminação de conexões**: Criação e encerramento de sessões de comunicação entre dispositivos.
- **Controle de fluxo**: Garante que o remetente não sobrecarregue o receptor com muitos dados de uma vez.
- **Correção de erros**: Detecta e retransmite pacotes perdidos ou corrompidos.
- **Multiplexação**: Permite que vários processos de aplicação utilizem a rede simultaneamente, diferenciando-os através de números de porta.

Os dispositivos que operam nessa camada são os **Sistemas finais** **(hosts)**: Incluem computadores, servidores e dispositivos móveis que se comunicam através da rede.

- **TCP (Transmission Control Protocol)**: Protocolo orientado a conexão que garante entrega confiável, controle de fluxo e retransmissão de pacotes perdidos. É adequado para aplicações que necessitam de alta confiabilidade, como transferência de arquivos e navegação na web.
- **UDP (User Datagram Protocol)**: Protocolo sem conexão que oferece entrega rápida, sem garantias de entrega ou ordem. É adequado para aplicações que podem tolerar perda de dados, como streaming de vídeo e jogos online.

## Camada de Rede

Responsável pelo encaminhamento de pacotes de dados entre redes diferentes.

Gerencia endereços IP, define roteamento e determina o melhor caminho para os pacotes percorrerem através dos grafos de sistemas intermediários até o sistema final

Transforma segmentos ou datagramas (da camada de transporte) em pacotes, adicionando cabeçalhos específicos e fragmentando-os quando necessário. Reassembla pacotes no destino.

Adiciona cabeçalhos que contêm:

- Endereços IP de origem e destino
- Informação de controle e fragmentação
- Tempo de Vida (TTL) para limitar o número de saltos que o pacote pode realizar

Alguns dispositivos que operam nessa camada:

- **Roteadores**: Encaminham pacotes de dados entre diferentes redes usando endereços IP e tabelas de roteamento para determinar o melhor caminho. Eles decidem o próximo salto para o pacote com base na tabela de roteamento.
- **Firewalls (nível de rede)**: Filtram pacotes com base em endereços IP e protocolos, controlando o tráfego de entrada e saída para proteger a rede.
- **Gateways**: Incluem roteadores e firewalls, funcionando como pontos de interface entre diferentes redes e protocolos, traduzindo dados entre redes distintas e garantindo a interoperabilidade.

Principais Protocolos:

- **IP (Internet Protocol)**: Principal protocolo que define a estrutura dos pacotes e endereçamento para a entrega de dados.
- **ICMP (Internet Control Message Protocol)**: Usado para mensagens de controle e erros, como o comando "ping" para verificar a conectividade.
- **IGMP (Internet Group Management Protocol)**: Gerencia membros de grupos multicast, permitindo que os roteadores saibam quais dispositivos desejam receber transmissões multicast.

## Camada de Enlace

Responsável pela transmissão confiável de quadros (frames) entre dois dispositivos diretamente conectados na mesma rede local.

Gerencia a entrega correta dos dados, controle de acesso ao meio físico e detecção e correção de erros.

Adiciona cabeçalhos e rodapés aos pacotes recebidos da camada de rede, formando quadros para transmissão.

### Técnicas de detecção e correção de erros.

(Organizado em ordem de complexidade)

- **CRC (Cyclic Redundancy Check)**: método de verificação de erros que usa uma função de hash específica para detectar mudanças acidentais em dados de comunicação digital. Ele é amplamente utilizado em redes e armazenamento de dados.
- **Checksum**: algoritmo que soma todos os valores dos dados em unidades específicas. O valor do checksum é anexado aos dados antes da transmissão.
- **Checagem de paridade:** método simples de detecção de erros que adiciona um bit de paridade aos dados para garantir que o número total de bits 1 na cadeia de dados seja par ou ímpar.

### Cabeçalhos e Rodapés

**Cabeçalhos (Headers)**:

- **Endereço MAC de Destino**: Identifica o destinatário do quadro.
- **Endereço MAC de Origem**: Identifica o remetente do quadro.
- **Tipo/EtherType**: Especifica o tipo de protocolo da camada superior.
- **Controle de Qualidade de Serviço (QoS)**: (Se aplicável) Prioriza o tráfego.

**Rodapés (Trailers)**:

- **CRC (Cyclic Redundancy Check)**: Sequência de verificação para detectar erros na transmissão.

Aparelhos que operam na camada de enlace:

- **Switches (comutadores)**: Encaminham quadros com base em endereços MAC e reduzem colisões criando domínios de colisão separados.
- **Bridges**: Conectam e filtram tráfego entre diferentes segmentos de redes.

## Camada Física

Transmissão de bits brutos através de um meio físico. Parte do Hardware.

É a interface do modelo TCP/IP com os diversos tipos de redes (Ethernet, por exemplo).

E por fim, transmite os frames pelo meio físico (Podendo ser desde cabos até utilizando sistemas sem fio).

Alguns dispositivos que operam nessa camada: 

- Hubs: Simplesmente retransmitem sinais elétricos para todos os dispositivos conectados. Não processam dados ou endereços. Qualquer mensagem enviada por um dos computadores também chegará aos demais. Entretanto, apenas o computador de destino irá responder à mensagem. Esse processo leva a problemas de congestionamento.
- Repetidores: Repetem e amplificam sinais para cobrir distâncias maiores, sem qualquer processamento adicional.

## Encapsulamento - PDU (**Protocol Data Unit)**

- **Aplicação**: Dado
- **Transporte**: Segmento (TCP) ou Datagrama (UDP)
- **Rede**: Pacote
- **Enlace**: Quadro (ou frame)
- **Física**: Bits

## Hub, Bridge, Switch e Roteador

Dispositivos essenciais na construção e operação de redes locais (LANs)

### Hub

Opera na Camada Física.

Simplesmente retransmitem sinais elétricos para todos os dispositivos conectados. Não processam dados ou endereços. Qualquer mensagem enviada por um dos computadores também chegará aos demais. Entretanto, apenas o computador de destino irá responder à mensagem. Esse processo leva a problemas de congestionamento.

### Bridge

Opera na Camada de Enlace.

Conecta duas redes locais entre si (desde que elas rodem os mesmos protocolos) e encaminha quadros com base nos endereços MAC. Processa endereços MAC para tomar decisões de encaminhamento, isolando o tráfego entre segmentos, o que reduz colisões e melhora o desempenho. Mantém uma tabela de endereços MAC para saber quais dispositivos estão em quais segmentos, encaminhando quadros somente para o segmento correto, reduzindo congestionamento e melhorando a segurança ao limitar a propagação de frames entre segmentos.

### Switch (Comutador)

Projetado para Topologia Estrela

Conecta vários computadores em uma rede. Encaminha frames de dados de forma inteligente utilizando uma tabela de endereços MAC.

- **Switches de Camada 2 com VLANs**: Operam na Camada 2 para segmentar e isolar tráfego dentro de VLANs. Encaminham quadros com base em endereços MAC.
- **Switches de Camada 3 com VLANs**: Adicionam capacidades de roteamento na Camada 3 para permitir a comunicação entre diferentes VLANs. Encaminham pacotes com base em endereços IP, além de gerenciar tabelas de roteamento.

### VLAN

A VLAN é um protocolo usado para organizar vários dispositivos dentro de uma rede física única sem precisar fazer mudanças físicas na infraestrutura. Um exemplo é para separar departamentos de uma empresa. 

### Roteador

Opera na camada de rede, encaminhando pacotes entre diferentes redes com base em endereços IP. Determina a melhor rota para transmitir os pacotes e mantém tabelas de roteamento para gerenciar o tráfego de dados. Roteador é um Gateway da rede.

## Broadcast

**Broadcast** é uma forma de comunicação em rede onde uma mensagem é enviada para todos os dispositivos em um segmento de rede usando o endereço MAC de broadcast (FF:FF:FF:FF:FF). Todos os dispositivos recebem a mensagem, mas apenas o destinatário específico responde. Pode causar congestionamento se usado em excesso ou se a rede for muito grande.

**Uso Comum**: Usado para descobrir dispositivos na rede, como DHCP e ARP.

- **ARP (Camada de Enlace)**: Um dispositivo envia uma solicitação ARP em broadcast para descobrir o endereço MAC correspondente a um endereço IP.
- **DHCP (Camada de Rede)**: Um dispositivo envia uma solicitação DHCP em broadcast para descobrir um servidor DHCP e obter um endereço IP.

## Endereço MAC

**Endereço MAC (Media Access Control)** é um identificador único atribuído a cada dispositivo de rede que possui uma interface de rede, como placas de rede Ethernet ou adaptadores Wi-Fi. É usado para comunicação dentro de uma rede local (LAN). Opera na camada de enlace.
Geralmente, é representado por 12 dígitos hexadecimais, separados por dois pontos ou hifens (por exemplo, 00:1A:2B:3C:4D:5E)

## Roteador de Borda

Dispositivo de rede que conecta a rede interna de uma organização à Internet ou a outras redes externas. Ele atua como um ponto de entrada e saída de tráfego para a rede interna, gerenciando a comunicação entre redes diferentes e garantindo a segurança e eficiência no tráfego de dados.

## Protocolo ARP (Address Resolution Protocol)

Protocolo usado para descobrir o endereço físico (MAC) de um dispositivo a partir de seu endereço IP em uma rede local. Atua na camada de enlace.

Passo a passo:
→ Quando um dispositivo precisa enviar um pacote para outro dispositivo na mesma rede local, ele conhece o endereço IP do destino, mas não o endereço MAC. O dispositivo envia uma **solicitação ARP** em broadcast para toda a rede, perguntando: "Qual é o endereço MAC associado ao IP X.X.X.X?" 

→ O dispositivo que possui o endereço IP solicitado responde com um **pacote ARP de resposta**, informando seu endereço MAC.
→ O dispositivo que fez a solicitação ARP atualiza sua tabela ARP com a correspondência entre o endereço IP e o endereço MAC recebido. Isso permite que ele envie pacotes diretamente para o dispositivo de destino usando o endereço MAC.