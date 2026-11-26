---
layout: page
title: Projetos
permalink: /projects/
description: Estudos de caso de hardware aberto, com imagens, artefatos disponíveis e próximos passos.
nav: true
nav_order: 1
---

# Acervo de hardware aberto

Esta página organiza quatro estudos de caso com base nos arquivos públicos do [meu fork](https://github.com/JVSDutra/Bootcamp_Open_Hardware), derivado de [Open_Hardware do FabLab Casa Firjan](https://github.com/fablabcasafirjan/Open_Hardware).

**Versão de apresentação: V1** para cada projeto. “V1” identifica aqui a primeira edição organizada deste portfólio; não é uma release de firmware, certificação ou comprovação de desempenho. Nomes de arquivos e revisões herdadas (como V02, V03 e V06) continuam identificando os artefatos de origem. As fotografias são registros do acervo.

## Microscópio automatizado — V1

![Registro de imagem microscópica disponível no acervo](https://raw.githubusercontent.com/JVSDutra/Bootcamp_Open_Hardware/main/Automated_Microscope/Mosquito_Zoomed_Image.jpeg)

**Objetivo** — Explorar aquisição de imagens com uma ESP32-CAM, dois microservos e uma estrutura de corte a laser.

**Artefatos** — [Sketch para Arduino IDE](https://github.com/JVSDutra/Bootcamp_Open_Hardware/blob/main/Automated_Microscope/Microscopio_Bootcamp_V1/Microscopio_Bootcamp_V1.ino), [geometria de corte SVG](https://github.com/JVSDutra/Bootcamp_Open_Hardware/blob/main/Automated_Microscope/Microscope_LaserCuts_V01.svg), [README e imagens](https://github.com/JVSDutra/Bootcamp_Open_Hardware/tree/main/Automated_Microscope).

**Estado e limites** — Há firmware para câmera, interface HTTP e movimento. A documentação não contém esquema completo, procedimento de foco/calibração nem medidas de resolução, repetibilidade ou desempenho óptico.

**Próximas melhorias possíveis**

- Documentar ligações, alimentação, modelo exato da placa e configuração das bibliotecas na Arduino IDE.
- Remover credenciais de rede do sketch público e descrever a configuração local.
- Documentar limites mecânicos e o comportamento dos servos em falha ou perda de conexão.
- Definir um protocolo de avaliação óptica antes de publicar alegações de desempenho.

## Detector de CO₂ — V1

![Vista frontal da caixa do detector de CO₂ no acervo](https://raw.githubusercontent.com/JVSDutra/Bootcamp_Open_Hardware/main/CO2_Detector/CO2_Sensor_STL_FrontSide.jpeg)

**Objetivo** — Reunir sensor SenseAir S8, ESP32 e display OLED em um protótipo didático de monitoramento de CO₂.

**Artefatos** — [Sketch para Arduino IDE](https://github.com/JVSDutra/Bootcamp_Open_Hardware/blob/main/CO2_Detector/Sensor_CO2_comDisplay_comTelegram/Sensor_CO2_comDisplay_comTelegram.ino), [READMEs, imagens e arquivos STL](https://github.com/JVSDutra/Bootcamp_Open_Hardware/tree/main/CO2_Detector). Os nomes dos gabinetes registram revisões próprias; a documentação não identifica uma montagem final validada.

**Estado e limites** — O código integra leitura do sensor, display e envio de mensagens pela rede. A montagem, as dependências, o intervalo de envio e a validação das leituras precisam de documentação e revisão. Não há aqui comparação com um instrumento de referência nem avaliação de incerteza.

**Próximas melhorias possíveis**

- Manter Wi-Fi e tokens em configuração local não versionada; documentar como preparar essa configuração na Arduino IDE.
- Corrigir e documentar a frequência de leitura e de notificação, com limites que evitem envios excessivos.
- Explicar ligações UART, versão das bibliotecas e configuração da placa.
- Adicionar estados claros para sensor indisponível, Wi-Fi desconectado e falha de envio.
- Planejar a comparação com um instrumento de referência antes de afirmar desempenho metrológico.

## Incubadora didática — V1

![Incubadora fechada no registro fotográfico do acervo](https://raw.githubusercontent.com/JVSDutra/Bootcamp_Open_Hardware/main/Incubator/Incubator_Closed.jpeg)

**Objetivo** — Explorar controle de temperatura com Arduino UNO, sensor DS18B20, display, aquecimento e ventilação.

**Artefatos** — [Sketch para Arduino IDE](https://github.com/JVSDutra/Bootcamp_Open_Hardware/blob/main/Incubator/Incubator_Bootcamp_V1/Incubator_Bootcamp_V1.ino), [desenho SVG](https://github.com/JVSDutra/Bootcamp_Open_Hardware/blob/main/Incubator/Incubadora_V06_Organizado.svg), [README e fotografias](https://github.com/JVSDutra/Bootcamp_Open_Hardware/tree/main/Incubator).

**Estado e limites** — O sketch contém leitura do DS18B20, controle liga/desliga com histerese, botões e LCD. A documentação não especifica completamente o circuito, a polaridade do relé ou as condições seguras de falha. Não há relatório de estabilidade, uniformidade ou faixa térmica.

**Próximas melhorias possíveis**

- Publicar esquema elétrico completo e especificações dos componentes, inclusive acionamento e isolamento do aquecedor.
- Definir o estado seguro quando o sensor estiver desconectado ou retornar leitura inválida.
- Rever a inicialização do relé, leitura repetida do sensor, debounce dos botões e limites do setpoint.
- Documentar ensaios térmicos com procedimento e instrumentos identificados antes de divulgar resultados.

Como o protótipo inclui aquecimento de potência, qualquer revisão do controle deve ser conferida com o circuito real antes de uso.

## Turbidímetro didático — V1

![Vista da câmera no protótipo de turbidímetro do acervo](https://raw.githubusercontent.com/JVSDutra/Bootcamp_Open_Hardware/main/Turbidimeter/Turbidimeter_cam_view.jpeg)

**Objetivo** — Explorar visualmente a interação entre iluminação e amostras usando uma estrutura, fonte de luz e câmera.

**Artefatos** — [README, fotos e registros](https://github.com/JVSDutra/Bootcamp_Open_Hardware/tree/main/Turbidimeter), incluindo [imagem geral do protótipo](https://github.com/JVSDutra/Bootcamp_Open_Hardware/blob/main/Turbidimeter/Turbd_V1.png).

**Estado e limites** — Esta pasta não contém sketch Arduino, procedimento reproduzível de aquisição ou valores calibrados em NTU. As fotografias não comprovam uma medição quantitativa.

**Próximas melhorias possíveis**

- Definir geometria entre fonte de luz, amostra e detector, além de controlar a iluminação ambiente.
- Especificar como capturar e processar imagens de forma reproduzível.
- Registrar amostras e padrões de referência e avaliar uma curva de calibração antes de apresentar leituras em NTU.
- Criar firmware somente depois de definidos sensor, eletrônica, pinagem e protocolo de medição.

## Créditos e uso

Os arquivos de origem e seus autores permanecem creditados no [repositório do FabLab Casa Firjan](https://github.com/fablabcasafirjan/Open_Hardware) e no histórico do fork. Uma contribuição documentada de João Victor Dutra ao projeto upstream foi uma alteração pontual no README do detector de CO₂, registrada no [PR #4](https://github.com/fablabcasafirjan/Open_Hardware/pull/4); isso não representa autoria exclusiva dos quatro protótipos.

O README upstream exibe referências de licenças sem delimitar claramente o escopo de cada tipo de arquivo. Consulte a licença, os avisos e a origem de cada arquivo antes de reutilizar desenhos, imagens ou hardware. Esta página organiza os materiais e não amplia direitos de terceiros.

## English summary

This portfolio documents four V1 case studies from a public FabLab Casa Firjan open hardware repository: an automated microscope, a CO₂ detector, an educational incubator and a turbidimeter. V1 refers to this portfolio edition, not to a tested firmware release. Each section links the available Arduino IDE sketches, designs and photographs, states documentation limits, and lists possible next improvements.
