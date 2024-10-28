<p align="center">
    <img width="100" src="assets/faci.png">
</p>


<p align="center">
  <a href="#"><img src="assets/Prototipo2.jpg" alt="Projeto">
  </a>
  
</p>

-------

<p align="center">
  <img 
    src="assets/Prototipofinal.png"
    width="400"  
  />
</p>

# COLORSENSE VERSÃO ONLINE - 2.0
Tecnologia Portátil para Identificação de Cores em Roupas para Pessoas com Deficiência Visual Com Suporte Online


 > ℹ️ **NOTE:** Este é o repositório **parcialmente** desenvolvido para e durante o projeto de extensão na disciplina de Programação de Microcontroladores na plataforma da [Faculdade Faci Wyden](https://www.wyden.com.br/) com o professor [Paulo Tássio da Luz Melo](https://www.linkedin.com/in/paulotassio/).

<p align="center">
  <a href="#" title="Preview do Conteúdo">
  <img src="assets/EquipeProjeto.png" width="80%">
  </a>
<p>

O projeto intitulado “COLORSENSE: Tecnologia Portátil para Identificação de Cores em Roupas para Pessoas com Deficiência Visual” tem como objetivo utilizar a tecnologia assistiva. Nossa proposta é desenvolver um dispositivo portátil que permita a uma pessoa com deficiência visual identificar a cor das roupas que está usando ou irá usar, utilizando microcontroladores e sensores. Com o apoio da Associação Paraense das Pessoas com Deficiência, esperamos proporcionar ao deficiente visual bem-estar, qualidade de vida e satisfação pessoal ao poder escolher as cores de suas roupas sem o auxílio de outras pessoas e fortalecer o vínculo entre a universidade e a comunidade local.

## 💻 Versão Alternativa

Durante a elaboraçãõ do projeto, foi levantada a possibilidade da otimização do desenvolvimento pelos alunos Rafaela Almeida e Luiz Henrique Scotta, que tiveram a iniciativa de uma versão otimizada. A transição do sensor desenvolvido com Arduino Uno e TCS3200 para a combinação de ESP32 e TCS34725 foi motivada pela busca de uma solução mais otimizada e eficiente. Essa mudança traz uma série de benefícios significativos, que vão além da mera atualização dos componentes.

Em termos de tamanho e peso, o ESP32 é consideravelmente mais compacto e leve em comparação ao Arduino Uno, que ocupa mais espaço em um projeto. Isso permite uma montagem mais discreta e leve, facilitando a integração em diversas aplicações.

A conectividade com a internet é uma das características mais marcantes dessa atualização. Enquanto o Arduino Uno geralmente requer módulos externos para comunicação via Wi-Fi ou Bluetooth, o ESP32 já possui essas funcionalidades integradas. Essa conectividade simplificada não só facilita a transmissão de dados em tempo real, mas também permite o controle remoto e o monitoramento via aplicativos móveis ou plataformas na nuvem, ampliando as possibilidades de uso do sensor, como vemos no projeto.

Em relação às features, o TCS34725 oferece vantagens adicionais em termos de precisão e faixa de operação em comparação ao TCS3200. O TCS34725 possui um melhor desempenho em condições de iluminação variadas e fornece dados de cor mais precisos, possibilitando leituras mais confiáveis. Além disso, o ESP32 oferece múltiplas interfaces de comunicação (como I2C e SPI), permitindo uma maior flexibilidade na integração com outros sensores e módulos, como sensores de temperatura ou de umidade.

No que diz respeito ao preço, embora o ESP32 e o TCS34725 possam ter um custo inicial alto, porém bem atrativos em relação a modelos semelhantes de placas pois sua capacidade de desempenho e a eliminação de módulos adicionais para conectividade frequentemente resultam em economia a longo prazo. A combinação dos dois componentes resulta em um sistema mais robusto e com menor necessidade de manutenção.

Essas melhorias no design e na funcionalidade do sensor não apenas otimizam seu desempenho, mas também ampliam suas aplicações em projetos de automação, monitoramento ambiental e sistemas IoT, tornando-o uma escolha mais viável e eficiente para desenvolvedores e entusiastas.

Equipe:
- José Roberto Vasconcellos Lopes
- Thiago Sousa Vasconcellos Lopes
- Luiz Felipe Barata Queiroz
- Luiz Henrique Gualberto Scotta
- Rafaela Mesquita Moraes de Almeida

<a href="#" title="View PDF now"> 📕Clique aqui para ler o artigo em sua versão original e publicada na disciplina</a>
<br>
<a href="#" title="View PDF now"> 📕Clique aqui para acessar o repositório da versão original e publicada na disciplina</a>

## 💻 Tecnologias utilizadas no projeto

- [Esp360] - para desenvolver o código;
- [TCS34725 ] - para desenvolver e testar o código;
- 

## 📄 Gerado na IDE do Arduino

Código：

|   Arquivo   | descrição                                                                                                                                                                                                                                                                         |
| :------: | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|  Q0704_LeitorDeCor_TCS3200.ino  | Este código em C++ usa o sensor de cor TCS230 e o módulo de som DFPlayer Mini para ler a cor detectada e tocar um arquivo de áudio correspondente. Bibliotecas e Objetos: Inclui as bibliotecas para o sensor de cor, para a contagem de frequência e para o controle de um MP3 player. Pinos e Componentes: Define os pinos para os componentes (sensor de cor, LED e botão). Configuração Inicial: No setup(), inicializa o sensor de cor, configura o botão, o LED e chama a função configuraMP3() para ajustar o módulo MP3, incluindo o volume. Loop Principal: Ao detectar o pressionamento do botão, o LED acende e o sensor de cor lê a cor. Após a leitura, exibe os valores RGB e o nome da cor correspondente. Toca o arquivo de áudio associado, onde cada cor tem um número que corresponde a um arquivo de som numerado na pasta MP3 do DFPlayer Mini. O LED é desligado após a execução do áudio. Este código permite identificar cores e tocar um som específico para cada uma, criando uma interação áudio-visual.                                                                                                                                                                                                    |
| ColorMatch.h | Este código define uma estrutura para reconhecer cores e associá-las a valores específicos, permitindo identificar a cor mais próxima de uma leitura RGB. Definições e Dados de Calibração: BLACK_CAL, WHITE_CAL, READ_VAL, e LEARN_VAL definem estados de operação; sdBlack e sdWhite são valores de calibração para preto e branco, usados para ajustar o sensor. Tabela de Cores: colorTable é uma estrutura que associa um nome a valores RGB de cada cor, e a tabela ct[] contém seis cores pré-definidas (BRANCO, VERMELHO, VERDE, AZUL, LARANJA e PRETO), cada uma com seus valores RGB e um arquivo de áudio MP3 correspondente. Função colorMatch(): Essa função recebe um valor RGB lido e calcula a distância entre ele e cada cor na tabela ct[], usando a soma dos quadrados das diferenças para medir similaridade. Retorna o índice da cor mais próxima (ou igual, se a distância for zero). Este código é projetado para identificar a cor mais próxima entre as opções da tabela e pode ser integrado a um sistema que reproduz sons específicos para cada cor reconhecida. |

## ✨ Características

- Portátil
- Cor: preto;
- Botão liga/desliga;
- Botão Push para leitura de cores;
- Medidas: 20cm x 6,5cm x 5cm (L x P x A);
- 2 Baterias de lítio recarregáveis (4.2v cada);
- Placa para balanceamento de carga;
- Fonte para carregamento 7 a 12v.

## 📚 Materiais

- Arduino UNO;
- Sensor de cor TCS3200;
- Módulo de áudio DFPlayer Mini;
- Cartão SD 8GB;
- Duas baterias de Li-Po (Lítio-Polímero) 3.7V;
- Placa BMS 3S 12V 100A;
- Botão para ligar e desligar o dispositivo;
- Botão push para acionar a leitura do sensor de cor;
- Jump’s de ligação;
- Alto-falante
- parafusos

## 🛠️ Instruções de uso

Ligue o dispositivo, pressione e solte o botão para aleitura de cor, encoste a parte frontal junto a roupa. O led acenderá e será reproduzido em áudio a cor da roupa.

## 👨‍💻 Desenvolvedores

<p>
    <img 
      align=left 
      margin=10 
      width=80 
      src="https://avatars.githbusercontent.com/u/79292597?s=96&v=4"
    />
    <p>&nbsp&nbsp&nbspRafaela Almeida<br>
    &nbsp&nbsp&nbsp
    <a href="https://github.om/jrobertovl">GitHub</a>&nbsp;|&nbsp;
    <a href="https://www.linkein.com/in/jrobertovl">LinkedIn</a>&nbsp;|&nbsp;
    <a href="https://www.instaram.com/jrobertovl/">Instagram</a>&nbsp;|&nbsp;
    <a href="https://api.whatspp.com/send?phone=5591982003052">WhatsApp</a>
    </p>
</p>
<br/><br/>
<p>
<p>
    <img 
      align=left 
      margin=10 
      width=80 
      src="https://avatars.githubuercontent.com/u/79292597?s=96&v=4"
    />
    <p>&nbsp&nbsp&nbspLuiz Henrique Scotta<br>
    &nbsp&nbsp&nbsp
    <a href="https://githu.com/jrobertovl">GitHub</a>&nbsp;|&nbsp;
    <a href="https://www.linkdin.com/in/jrobertovl">LinkedIn</a>&nbsp;|&nbsp;
    <a href="https://www.instagrm.com/jrobertovl/">Instagram</a>&nbsp;|&nbsp;
    <a href="https://api.whatspp.com/send?phone=5591982003052">WhatsApp</a>
    </p>
</p>
<br/><br/>
<p>
---
