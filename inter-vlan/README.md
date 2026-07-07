<h1 align="center">Laboratório de Redes - Roteamento Inter-VLAN (Router-on-a-Stick)</h1>

<p align="center">
Simulação de segmentação de rede utilizando VLANs e roteamento entre elas por meio da técnica <strong>Router-on-a-Stick</strong>.
</p>

---

## Objetivo
Implementar uma rede segmentada em VLANs para separar departamentos distintos e permitir a comunicação entre eles através de um roteador configurado com subinterfaces e encapsulamento IEEE 802.1Q.

---

## Cenário
Uma pequena empresa possui dois departamentos:

- **VLAN 10** – TI
- **VLAN 20** – Financeiro

Cada departamento pertence a uma rede diferente, o que impede a comunicação direta entre eles. O roteador é responsável por fazer o roteamento entre as VLANs.

---

## Tecnologias Utilizadas
- Cisco Packet Tracer
- Cisco IOS
- VLANs
- IEEE 802.1Q
- Router-on-a-Stick
- Inter-VLAN Routing

---

## Topologia

<p align="center">
<img src="Topologia.png" width="1000">
</p>

---

## Endereçamento

### VLAN 10 - TI
| Dispositivo | Endereço IP |
|-------------|-------------|
| PC 1 | 192.168.10.11 |
| PC 2 | 192.168.10.12 |
| Notebook 1 | 192.168.10.21 |
| Notebook 2 | 192.168.10.22 |
| Gateway | 192.168.10.1 |

### VLAN 20 - Financeiro
| Dispositivo | Endereço IP |
|-------------|-------------|
| PC 3 | 192.168.20.11 |
| PC 4 | 192.168.20.12 |
| Notebook 3 | 192.168.20.21 |
| Notebook 4 | 192.168.20.22 |
| Gateway | 192.168.20.1 |

---

## Configuração do Switch

### VLANs
- VLAN 10 – TI
- VLAN 20 – Financeiro
- VLAN 100 – Native VLAN

### Trunk
- Interface em modo trunk
- Encapsulamento IEEE 802.1Q
- VLAN nativa 100

<p align="center">
<img src="config-switch.png" width="850">
</p>

---

## Configuração do Roteador
Foram configuradas subinterfaces com encapsulamento IEEE 802.1Q para o roteamento entre as VLANs.

- G0/0/0.10
- G0/0/0.20
- G0/0/0.100 (Native VLAN)

<p align="center">
<img src="config-roteador.png" width="850">
</p>

---

## Topologia Detalhada
Topologia final do laboratório, já com as VLANs, a porta trunk e as subinterfaces do roteador configuradas para o roteamento Inter-VLAN.

<p align="center">
<img src="Topologia-Final.png" width="1000">
</p>

---

## Validação
Testes de conectividade feitos com o comando **ping** entre dispositivos de VLANs diferentes. O roteamento Inter-VLAN funcionou, com comunicação entre os dois departamentos passando pelo roteador.

<p align="center">
<img src="teste-ping-1.png" width="1200">
<br><br>
<img src="teste-ping-2.png" width="1200">
</p>

---

## Competências Demonstradas
- Criação de VLANs
- Configuração de portas Access
- Configuração de portas Trunk
- VLAN Nativa
- IEEE 802.1Q
- Router-on-a-Stick
- Configuração de Subinterfaces
- Endereçamento IPv4
- Testes de conectividade
- Troubleshooting básico

---

## Aprendizados
Neste laboratório apliquei conceitos de segmentação de redes com VLANs, configuração de portas Access e Trunk, encapsulamento IEEE 802.1Q e roteamento Inter-VLAN com a técnica Router-on-a-Stick. Também ficou mais claro como o planejamento do endereçamento IP afeta diretamente a validação da conectividade entre os segmentos da rede.
