# CTranslate2 no Termux (Android) 

Este repositório contém um script de automação para compilar e instalar o **CTranslate2** nativamente no Android usando o Termux. O processo inclui correções automáticas (patching) para compatibilidade com o kernel Android e otimização via OpenBLAS (`libopenblas`)

## Características do Script
- **Patch de Código**: Comenta automaticamente blocos de afinidade de CPU (`pthread_setaffinity_np`) que causam erro no Android
- **Linker Corrigido**: Resolve o erro de símbolo `__cxa_init_primary_exception` forçando o link com `libc++_shared`
- **Otimização**: Configurado para usar **OpenBLAS** e compilação em 1 núcleo para evitar travamentos de RAM
**Créditos**
  https://t.me/cybe4
  
## Como Instalar

1. Abra o Termux e clone este repositório:
   ```bash
   git clone https://github.com/qrt2/termux_CTranslate2
   cd termux_CTranslate2 && chmod +x install_CTrasnlate2 
    ./install_CTrasnlate2
## Como usar o Tradutor
​Após a conclusão, você pode verificar a instalação com o comando:
`ct2-translator --help`

  ## Requisitos
​Espaço em disco: ~2GB (durante a compilação)
​Tempo: 15 a 30 minutos (dependendo do processador)
​Bateria: Recomendado manter o carregador conectado
