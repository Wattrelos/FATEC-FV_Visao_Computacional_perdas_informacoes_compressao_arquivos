# Amostra Comparativa: RAW vs. JPEG (Canon Cinema EOS R5 C)

## 👨‍🏫 Informações Acadêmicas
- **Instituição:** Faculdade de Tecnologia de Ferraz de Vasconcelos (FATEC-FV)
- **Curso:** Análise e Desenvolvimento de Sistemas (ADS)
- **Disciplina:** Visão Computacional / Trabalho de Graduação (TG)
- **Pesquisador / Discente:** Josias Sobrinho
- **Orientadora:** Profa. Márcia Bissaco

---

## 1. Contextualização da Amostra

Para comprovar experimentalmente o impacto da compressão e o dilema entre armazenamento e fidelidade de dados, foram analisadas capturas simultâneas em modo duplo (**Dual Shooting: RAW + JPG**) obtidas por uma câmera profissional de cinema **Canon EOS R5 C** (sensor Full-Frame de 45 Megapixels com processador DIGIC X).

### 📁 Estrutura de Diretórios dos Arquivos

```bash
.  
└── image/                                          # 🚀 Diretório de Imagens  
    └── raw-vs-jpg/                                 # 🌐 Amostras RAW vs. JPG  
        ├── IMG_2750.CR3                            # 📷 Canon RAW 3: 107,8 MiB (113.051.616 bytes) 
        ├── IMG_2750.JPG                            # 📸 JPEG Câmera: 5,0 MiB (5.230.041 bytes) 
        ├── IMG_7108.CR3                            # 📷 Canon RAW 3: 81,5 MiB (85.475.912 bytes) 
        ├── IMG_7108.JPG                            # 📸 JPEG Câmera: 2,4 MiB (2.536.560 bytes)  
        ├── IMG_7711.CR3                            # 📷 Canon RAW 3: 95,4 MiB (100.078.056 bytes)  
        ├── IMG_7711.JPG                            # 📸 JPEG Câmera: 2,4 MiB (2.516.451 bytes)  
        ├── IMG_7835.CR3                            # 📷 Canon RAW 3: 82,4 MiB (86.365.600 bytes)  
        └── IMG_7835.JPG                            # 📸 JPEG Câmera: 2,3 MiB (2.430.799 bytes)
```

---

## 2. Comparação Quantitativa de Tamanho e Armazenamento

| Amostra | Arquivo Bruto (.CR3) | Arquivo Comprimido (.JPG) | Economia de Espaço | Taxa de Compressão |
| :--- | :--- | :--- | :--- | :--- |
| **Foto 1 (IMG_7711)** | [IMG_7711.CR3](image/raw-vs-jpg/IMG_7711.CR3) (~95,4 MiB) | [IMG_7711.JPG](image/raw-vs-jpg/IMG_7711.JPG) (~2,4 MiB) | **97,5% menor** | ~39,8 : 1 |
| **Foto 2 (IMG_2750)** | [IMG_2750.CR3](image/raw-vs-jpg/IMG_2750.CR3) (~107,8 MiB) | [IMG_2750.JPG](image/raw-vs-jpg/IMG_2750.JPG) (~5,0 MiB) | **95,4% menor** | ~21,6 : 1 |
| **Foto 3 (IMG_7108)** | [IMG_7108.CR3](image/raw-vs-jpg/IMG_7108.CR3) (~81,5 MiB) | [IMG_7108.JPG](image/raw-vs-jpg/IMG_7108.JPG) (~2,4 MiB) | **97,0% menor** | ~33,7 : 1 |
| **Foto 4 (IMG_7835)** | [IMG_7835.CR3](image/raw-vs-jpg/IMG_7835.CR3) (~82,4 MiB) | [IMG_7835.JPG](image/raw-vs-jpg/IMG_7835.JPG) (~2,3 MiB) | **97,2% menor** | ~35,5 : 1 |
| **Total / Média** | **~367,1 MiB** (384.971.184 bytes) | **~12,1 MiB** (12.713.851 bytes) | **96,7% menor** (média) | **~30,3 : 1** (global) |

> [!NOTE]
> **Por que os navegadores não abrem o arquivo `.CR3` diretamente?**  
> O arquivo `.CR3` (Canon RAW 3) não é um formato de imagem rasterizada convencional para web. Ele armazena diretamente a leitura analógico-digital dos fotodiodos sob o mosaico de filtros de cor Bayer com **14 bits de profundidade linear**, antes de qualquer interpolação cromática (*demosaicing*). Navegadores reconhecem apenas formatos finais rasterizados (como JPG, PNG e WebP). Para processar o arquivo `.CR3`, utilizam-se ferramentas de revelação digital ou bibliotecas em Python como `rawpy`/`LibRaw`.

---

## 3. Pré-visualização das Capturas em JPG

| Amostra 1: IMG_7711.JPG (©Josias) | Amostra 2: IMG_2750.JPG (©Josias) |
| :---: | :---: |
| ![IMG_7711.JPG](image/raw-vs-jpg/IMG_7711.JPG) | ![IMG_2750.JPG](image/raw-vs-jpg/IMG_2750.JPG) |
| *Arquivo RAW (.CR3):* [IMG_7711.CR3](image/raw-vs-jpg/IMG_7711.CR3) | *Arquivo RAW (.CR3):* [IMG_2750.CR3](image/raw-vs-jpg/IMG_2750.CR3) |
| **Quadro Histórico (Nationalmuseum, Estocolmo):** Obra *Rainha Maria Antonieta de França e dois de seus filhos passeando no Parque de Trianon* (1785), por Adolf Ulrik Wertmüller. Ampla riqueza de tons médios e sutilezas de óleo sobre tela. | **Grand Foyer / Salão de Ouro (Palais Garnier, Paris):** Teto ricamente decorado com folheados a ouro e afrescos mitológicos de Paul Baudry (década de 1870). Extremo alcance dinâmico entre lustres incandescentes e ornatos dourados. |
| Amostra 3: IMG_7108.JPG (©Josias) | Amostra 4: IMG_7835.JPG (©Josias) |
| :---: | :---: |
| ![IMG_7108.JPG](image/raw-vs-jpg/IMG_7108.JPG) | ![IMG_7835.JPG](image/raw-vs-jpg/IMG_7835.JPG) |
| *Arquivo RAW (.CR3):* [IMG_7108.CR3](image/raw-vs-jpg/IMG_7108.CR3) | *Arquivo RAW (.CR3):* [IMG_7835.CR3](image/raw-vs-jpg/IMG_7835.CR3) |
| **Orla e Porto de Estocolmo (Teleobjetiva 105mm):** Vista da enseada de Saltsjön a partir da Skeppsholmsbron, com a balsa *Djurgården 11* e o navio veleiro histórico de aço *af Chapman* ancorado em Skeppsholmen. | **Ponte Skeppsholmsbron (Grande-Angular 24mm):** Perspectiva frontal da passarela da ponte em direção a Skeppsholmen com o veleiro *af Chapman* ao fundo e docks flutuantes sob forte iluminação solar natural direta. |

---

## 4. O "Custo Real" Pago pela Compressão JPEG

Embora a compressão reduza em média mais de **96,7% do tamanho em disco** (alcançando entre **95,4% e 97,5%** de economia nas amostras), na Visão Computacional e no processamento científico essa redução impõe um custo significativo:

1. **Perda de 98,4% da Resolução Radiométrica:**  
   O RAW registra $2^{14} = 16.384$ níveis de intensidade por canal de cor, enquanto o JPG é forçado a apenas $2^8 = 256$ níveis. Transições sutis de brilho sofrem posterização (*color banding*).
2. **Corte Irreversível (*Clipping*) em Altas Luzes e Sombras:**  
   O JPG já tem uma curva de contraste e gama aplicada pela câmera, estourando brancos e empastando pretos. No RAW, a resposta linear preserva a informação física, permitindo recuperar de 3 a 4 stops de exposição.
3. **Subamostragem de Cor (Chroma Subsampling YCbCr 4:2:0):**  
   O JPEG descarta até 75% da informação de cor porque o olho humano percebe pouco essa perda. Contudo, algoritmos de segmentação cromática e rastreamento perdem precisão nas bordas dos objetos.
4. **Balanço de Branco "Assado" (*Baked-in*):**  
   No RAW, o balanço de branco é apenas um metadado ajustável matematicamente a qualquer momento. No JPG, o tom de cor está gravado definitivamente nos pixels.
5. **Artefatos de Bloco (DCT):**  
   A Transformada Discreta de Cosseno em blocos de $8 \times 8$ gera ruídos de alta frequência (*ringing*) e bordas artificiais que enganam detectores como Canny e Sobel.

---

## 5. Documentos Relacionados
* Artigo Principal: [dilema-edicao-imagens.md](dilema-edicao-imagens.md)
* Experimento com OCR em Placas: [experimento-pratico.md](experimento-pratico.md)

---

## 6. Referências das Amostras Fotográficas
* **Amostra 1 (IMG_7711):** WERTMÜLLER, Adolf Ulrik. *Queen Marie Antoinette of France and two of her Children Walking in The Park of Trianon*. 1785. Óleo sobre tela, 276 x 194 cm. Nationalmuseum, Estocolmo. Fotografia por Josias Sobrinho / Josias Wattrelos (Canon EOS R5 C, out. 2024).
* **Amostra 2 (IMG_2750):** GARNIER, Charles; BAUDRY, Paul. *Plafond du Grand Foyer*. Década de 1870. Decorações e afrescos clássicos. Palais Garnier, Paris. Fotografia por Josias Sobrinho / Josias Wattrelos (Canon EOS R5 C, set. 2024).
* **Amostra 3 (IMG_7108):** SOBRINHO, Josias. *Vista panorâmica de Saltsjön com a balsa Djurgården 11 e o navio histórico af Chapman a partir da Skeppsholmsbron*. Estocolmo, Suécia. Fotografia autoral (Canon EOS R5 C, out. 2024).
* **Amostra 4 (IMG_7835):** SOBRINHO, Josias. *Passarela da ponte Skeppsholmsbron com vista para Skeppsholmen e o veleiro af Chapman*. Estocolmo, Suécia. Fotografia autoral (Canon EOS R5 C, out. 2024).
