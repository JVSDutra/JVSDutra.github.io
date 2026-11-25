---
layout: page
title: Projetos
permalink: /projects/
description: Estudos de caso de hardware aberto documentados publicamente.
nav: true
nav_order: 1
---

## Acervo aberto do FabLab Casa Firjan

Os estudos abaixo usam somente materiais já públicos no repositório [Bootcamp_Open_Hardware](https://github.com/JVSDutra/Bootcamp_Open_Hardware), um fork do projeto [Open_Hardware, do FabLab Casa Firjan](https://github.com/fablabcasafirjan/Open_Hardware). O crédito ao FabLab e à comunidade de hardware aberto se aplica ao acervo de origem; não reivindico autoria exclusiva dos projetos. Os registros disponíveis são breves, então cada caso separa os artefatos observáveis do que ainda não está documentado.

## Microscópio DIY automatizado

**Objetivo** — Explorar uma montagem para observação microscópica com estrutura cortada a laser e captura por câmera.

**Abordagem** — O diretório documenta uma estrutura em MDF, uma ESP32-CAM e dois microservos. O firmware disponível organiza o controle dos servos; os arquivos de fabricação e as imagens registram partes da montagem.

**Artefatos públicos** — [README e imagens](https://github.com/JVSDutra/Bootcamp_Open_Hardware/tree/main/Automated_Microscope), [arquivo SVG da estrutura](https://github.com/JVSDutra/Bootcamp_Open_Hardware/blob/main/Automated_Microscope/Microscope_LaserCuts_V01.svg) e [firmware](https://github.com/JVSDutra/Bootcamp_Open_Hardware/blob/main/Automated_Microscope/Microscopio_Bootcamp_V1/Microscopio_Bootcamp_V1.ino).

**Limites** — O README lista componentes e imagens, mas não descreve protocolo de calibração, desempenho óptico ou validação quantitativa. Não apresento esses pontos como resultados medidos.

## Detector de CO₂ com telemetria

**Objetivo** — Reunir componentes de um detector didático de CO₂ com visualização local e envio de dados.

**Abordagem** — A lista de materiais identifica o sensor SenseAir S8, uma placa ESP32 e um display OLED. O repositório inclui modelos STL do gabinete e firmware nomeado para display e Telegram.

**Artefatos públicos** — [README, imagens e modelos](https://github.com/JVSDutra/Bootcamp_Open_Hardware/tree/main/CO2_Detector), [firmware](https://github.com/JVSDutra/Bootcamp_Open_Hardware/blob/main/CO2_Detector/Sensor_CO2_comDisplay_comTelegram/Sensor_CO2_comDisplay_comTelegram.ino) e [modelo do gabinete](https://github.com/JVSDutra/Bootcamp_Open_Hardware/tree/main/CO2_Detector).

**Limites** — A documentação não informa calibração, incerteza, comparação com instrumento de referência ou séries de medição. O projeto é apresentado como protótipo de hardware aberto, sem alegação de desempenho metrológico.

## Turbidímetro V1

**Objetivo** — Investigar uma montagem simples para observar turbidez com uma fonte de luz, material difusor e câmera.

**Abordagem** — O registro lista um LED, uma bateria, papel difusor e uma câmera. As imagens públicas mostram a montagem e exemplos visuais com amostras.

**Artefatos públicos** — [README e imagens do projeto](https://github.com/JVSDutra/Bootcamp_Open_Hardware/tree/main/Turbidimeter), incluindo [registro da montagem](https://github.com/JVSDutra/Bootcamp_Open_Hardware/blob/main/Turbidimeter/Turbd_V1.png).

**Limites** — O material não descreve curva de calibração, método analítico ou resultados numéricos. As imagens são registros visuais e não comprovam exatidão ou faixa de medição.

---

**Crédito e contexto:** conteúdo baseado no [fork público de Open_Hardware do FabLab Casa Firjan](https://github.com/fablabcasafirjan/Open_Hardware), consultado em 25/11/2026. Os arquivos-fonte e seus créditos permanecem nos repositórios de origem.
