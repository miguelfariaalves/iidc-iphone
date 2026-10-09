# IIDC PWA v0.2 — protótipo experimental

## Incluído
- Importação local de texto TXT, seleção de imagem/PDF, pré-visualização de fotografia.
- Classificação heurística de 8 tipos de exame e outros relatórios.
- Extração heurística de campos de análises, ECG, Holter, MAPA, prova de esforço, ecocardiografia, TC/RM cardíaca e cateterismo.
- Revisão campo a campo, edição, adição manual, registo de linhas não classificadas.
- Transcrição parcial por grupo apenas de campos confirmados; TXT de auditoria.
- Sem chamadas remotas no código, sem envio de documentos para servidores pela aplicação.

## Não incluído / limitações
- **PDF não é extraído automaticamente**; deve colar o texto. OCR de fotografias via TextDetector é experimental e habitualmente indisponível no Safari iOS.
- Não interpreta traçados ECG nem imagens; analisa texto do relatório.
- Não certifica completude; não extrai intervalos de referência ou flags de forma fiável.
- Não foi compilado/testado num Safari real; não está clinicamente validado.
- Não tem persistência clínica, integração EHR, autenticação nem segurança de produção.

## Teste local
`node tests/engine.test.js`

## Publicação gratuita (sem doentes reais)
Publicar **apenas os ficheiros da aplicação**, nunca relatórios clínicos, num alojamento estático HTTPS, por exemplo GitHub Pages. No Safari do iPhone, abrir o URL HTTPS e escolher Partilhar > Adicionar ao ecrã principal. A publicação exige uma conta e ação do utilizador; não foi realizada automaticamente.
