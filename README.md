# kicad_libraries

Bibliotecas reutilizáveis organizadas por família, independentes de projetos.

Cada `.kicad_sym` reúne os símbolos da categoria; cada pasta `.pretty` reúne os
footprints da família em arquivos `.kicad_mod` individuais. Modelos3D em `3dmodels`.

No KiCad, os nomes usam o prefixo `Custom_` para não conflitar com as bibliotecas
padrão. Os caminhos usam `${KICAD_3RD_PARTY}`. Bibliotecas registradas globalmente.

## Símbolos

| Biblioteca | Símbolos |
| --- | ---: |
| Comparator.kicad_sym | 2 |
| Connector_Card.kicad_sym | 2 |
| Connector_Generic.kicad_sym | 6 |
| Connector_Molex_KK254.kicad_sym | 3 |
| Crystal.kicad_sym | 1 |
| Device.kicad_sym | 12 |
| Diode.kicad_sym | 1 |
| Interface_Protection.kicad_sym | 1 |
| MCU_ST_STM32H7.kicad_sym | 1 |
| Power.kicad_sym | 1 |
| RF_Module.kicad_sym | 1 |
| Regulator_Linear.kicad_sym | 2 |
| Regulator_Switching.kicad_sym | 2 |
| Sensor_Motion.kicad_sym | 2 |
| Supervisor.kicad_sym | 1 |
| Switch.kicad_sym | 1 |
| Transistor_BJT.kicad_sym | 2 |
| Transistor_FET.kicad_sym | 3 |

## Footprints

| Pasta | Footprints |
| --- | ---: |
| Button_Switch_SMD.pretty | 1 |
| Capacitor_SMD.pretty | 5 |
| Connector_Card.pretty | 2 |
| Connector_FFC_FPC.pretty | 1 |
| Connector_Molex_KK254.pretty | 3 |
| Connector_PinHeader_2.54mm.pretty | 2 |
| Connector_Samtec_TSM.pretty | 7 |
| Crystal.pretty | 3 |
| Diode_SMD.pretty | 3 |
| Fuse.pretty | 1 |
| Inductor_SMD.pretty | 3 |
| LED_SMD.pretty | 1 |
| Package_LGA.pretty | 2 |
| Package_QFP.pretty | 1 |
| Package_SO.pretty | 3 |
| Package_TO_SOT_SMD.pretty | 5 |
| Potentiometer_SMD.pretty | 1 |
| RF_Module.pretty | 1 |
| Resistor_SMD.pretty | 1 |
| Sensor_Motion.pretty | 2 |
| TerminalBlock_Phoenix.pretty | 1 |
| TerminalBlock_Wago.pretty | 1 |

Os modelos Molex KK254 de2,3e4 vias estão reunidos em Connector_Molex_KK254.
Os modelos Samtec TSM estão reunidos em Connector_Samtec_TSM.
C_0603 e R_0603 são genéricos, sem fabricante/MPN obrigatório; respeitar as
especificações do componente no circuito. Sensores têm marcações dos eixos
físicos X/Y; a orientação na aplicação é definida pelo projeto que os utilizar.
