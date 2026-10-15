# Modelos 3D — fontes e limites

Os caminhos das bibliotecas usam `${KICAD_3RD_PARTY}/3dmodels`. Arquivos STEP pareados aos WRL permitem exportação mecânica com a opção de substituir modelos.

Os modelos simplificados abaixo são envelopes de visualização baseados nas dimensões publicadas. Não são CAD homologado pelo fabricante e não representam tolerâncias de encaixe ou peças móveis.

| Footprint | Modelo | Origem | Tipo |
|---|---|---|---|
| PinHeader_1x05_P2.54mm_Horizontal | [PinHeader_1x05_P2.54mm_Horizontal.step](Connector_PinHeader_2.54mm.3dshapes/PinHeader_1x05_P2.54mm_Horizontal.step) | KiCad10 official packages3D | ready |
| SOT-23-5 | [SOT-23-5.step](Package_TO_SOT_SMD.3dshapes/SOT-23-5.step) | KiCad10 official packages3D | ready |
| SOIC-8-1EP_3.9x4.9mm_P1.27mm_EP2.62x3.51mm | [SOIC-8-1EP_3.9x4.9mm_P1.27mm_EP2.29x3mm.step](Package_SO.3dshapes/SOIC-8-1EP_3.9x4.9mm_P1.27mm_EP2.29x3mm.step) | KiCad10 official packages3D | ready_generic_package |
| Wisevision_N096-1608TBBIG09-C08_FPC_Mechanical | [Wisevision_N096-1608TBBIG09-C08.step](Display.3dshapes/Wisevision_N096-1608TBBIG09-C08.step) | https://modules.easyeda.com/qAxj6KHrDKw4blvCG8QJPs7Y/0be0f225b51b436f9c8002ad7a8b9803 | ready |
| USB_C_Receptacle_HRO_TYPE-C-31-M-12 | [HRO_TYPE-C-31-M-12.step](Connector_USB.3dshapes/HRO_TYPE-C-31-M-12.step) | https://github.com/ai03-2725/Type-C.pretty/blob/master/HRO%20%20TYPE-C-31-M-12.step | ready |
| Fuse_Littelfuse-NANO2-451_453 | [Littelfuse_451_453_NANO2.step](Fuse.3dshapes/Littelfuse_451_453_NANO2.step) | https://www.pcb-3d.com/wordpress/models/fuse_littelfuse_451-453_xxx_series_nano_sm/ | ready |
| Bourns_SRP1038CC | [Bourns_SRP1038CC_simplified.wrl](Inductor_SMD.3dshapes/Bourns_SRP1038CC_simplified.wrl) | https://www.bourns.com/docs/Product-Datasheets/SRP1038CC.pdf | simplified_datasheet_envelope |
| L_TDK_SPM6530T | [TDK_SPM6530T_simplified.wrl](Inductor_SMD.3dshapes/TDK_SPM6530T_simplified.wrl) | https://product.tdk.com/en/search/inductor/inductor/smd/info?part_no=SPM6530T-6R8M | simplified_datasheet_envelope |
| Crystal_SMD_SeikoEpson_MC306-4Pin_8.0x3.2mm | [HCI_FR08S4_simplified.wrl](Crystal.3dshapes/HCI_FR08S4_simplified.wrl) | https://www.rxelectronics.kr/datasheet/a6/fr08s4-32.768-n06lldtk.pdf | simplified_datasheet_envelope |
| SW_SPST_Omron_B3SN-3012P | [Omron_B3SN-3012P_simplified.wrl](Button_Switch_SMD.3dshapes/Omron_B3SN-3012P_simplified.wrl) | https://omronfs.omron.com/en_US/ecb/products/pdf/en-b3sn.pdf | simplified_datasheet_envelope |
| CP_Elec_8x11.5_Aishi_VZ | [Aishi_VZ_8x11.5_simplified.wrl](Capacitor_SMD.3dshapes/Aishi_VZ_8x11.5_simplified.wrl) | Aishi VZ series dimensional drawing (local manufacturer catalog) | simplified_datasheet_envelope |
| Hirose_FH34SRJ-8S-0.5SH | [Hirose_FH34SRJ-8S-0.5SH_simplified.wrl](Connector_FFC-FPC.3dshapes/Hirose_FH34SRJ-8S-0.5SH_simplified.wrl) | https://www.hirose.com/en/product/p/CL0580-1231-8-50 | simplified_datasheet_envelope |
| microSD_XYECONN_TF-01A-ZYD9AH1.85 | [XYECONN_TF-01A-ZYD9AH1.85_simplified.wrl](Connector_Card.3dshapes/XYECONN_TF-01A-ZYD9AH1.85_simplified.wrl) | https://www.xyeconn.com/product/ljqxl/tfkazuo/223.html | simplified_datasheet_envelope |

## Observações mecânicas

- Wisevision N096: modelo pronto da biblioteca EasyEDA/JLCEDA, com FPC aberto no plano, alinhado ao datum da ponta. Não simula curvatura do flex, espessura da fita adesiva ou espaçadores.
- SOIC-8EP: modelo genérico do KiCad de corpo3,9×4,9mm e terminal térmico2,29×3mm, dentro da faixa mecânica do encapsulamento SO-8EP. O land pattern de cobre é independente da dimensão do metal exposto no CAD.
- Hirose: o STEP da EasyEDA foi rejeitado por divergir da geometria de corpo/ancoragens. O envelope simplificado representa o atuador fechado; o desenho oficial continua sendo a referência de montagem.
- Terminais USB-C: orientação adaptada do modelo HRO publicado por ai03; pads e furação não foram alterados.

## Envelopes simplificados

### Bourns_SRP1038CC_simplified

Nominal10x10x3.8mm, terminal span11mm. Simplified lead shape; not manufacturer CAD.

Fonte: https://www.bourns.com/docs/Product-Datasheets/SRP1038CC.pdf

### TDK_SPM6530T_simplified

7.1x6.5x3.0mm nominal envelope. Ready TDK STEP download not accessible; simplified terminals.

Fonte: https://product.tdk.com/en/search/inductor/inductor/smd/info?part_no=SPM6530T-6R8M

### HCI_FR08S4_simplified

HCI FR08S4 body8x3.2mm, four J-leads span3.8mm, nominal height2.5mm. Not Epson-branded CAD.

Fonte: https://www.rxelectronics.kr/datasheet/a6/fr08s4-32.768-n06lldtk.pdf

### Omron_B3SN-3012P_simplified

6.5x6mm body,3.1mm nominal height, four SMT terminals; does not depict internal mechanism. Manufacturer TraceParts download requires interactive access/login.

Fonte: https://omronfs.omron.com/en_US/ecb/products/pdf/en-b3sn.pdf

### Aishi_VZ_8x11.5_simplified

8mm diameter,11.5mm total nominal height; base8.3mm. Polarity side retained. Generic approximation of sleeve and leads.

Fonte: Aishi VZ series dimensional drawing (local manufacturer catalog)

### Hirose_FH34SRJ-8S-0.5SH_simplified

Closed actuator nominal6x3.8x1mm. EasyEDA model rejected: body/contact-anchor geometry differs; official downloadable ZIP deniedHTTP403. Contact details simplified, use official drawing for mating tolerances.

Fonte: https://www.hirose.com/en/product/p/CL0580-1231-8-50

### XYECONN_TF-01A-ZYD9AH1.85_simplified

Manufacturer body14.75x14.5mm;1.85mm maximum height (model1.75nominal); pegs0.8mm diameter,0.95mm below board. No inserted card. Shell openings/contact spring geometry illustrative.

Fonte: https://www.xyeconn.com/product/ljqxl/tfkazuo/223.html

