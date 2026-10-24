# Exercício de criptografia de arquivos

Este repositório registra um exercício de um desafio de cibersegurança da DIO. Os scripts demonstram, em escala pequena, a criptografia e a descriptografia de um arquivo de teste usando AES no modo CTR.

O exemplo foi feito para estudo. A chave está escrita no código e o modo usado não autentica os dados, então isto não é uma implementação segura para proteger arquivos.

## Antes de executar

Use somente uma máquina ou pasta de laboratório isolada e um arquivo descartável chamado `teste.txt`. O script de criptografia apaga esse arquivo depois de ler seu conteúdo e grava uma versão com a extensão `.ransomwaretroll`. O script de descriptografia lê esse arquivo e também o apaga ao recriar `teste.txt`.

Não use documentos pessoais, arquivos de trabalho ou dados de terceiros. Faça uma cópia de segurança do material de teste.

## Arquivos

- `encrypter.py`: lê `teste.txt` e grava o conteúdo criptografado.
- `decrypter.py`: lê `teste.txt.ransomwaretroll` e recria `teste.txt`.
- `teste.txt`: texto descartável usado no exemplo.

## Como executar

Requer Python e a biblioteca `pyaes`.

```bash
python -m pip install pyaes
python encrypter.py
python decrypter.py
```

Execute os scripts a partir da pasta que contém o arquivo de teste. A descriptografia depende da mesma chave fixa que está nos dois arquivos Python.

Este projeto é um exercício didático local. Não é um ransomware funcional para uso contra outras pessoas ou sistemas.