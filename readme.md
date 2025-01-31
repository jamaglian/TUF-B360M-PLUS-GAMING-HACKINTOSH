# Hackintosh EFI - macOS Sequoia 15.3

Este repositório contém a EFI configurada para Hackintosh utilizando o macOS Sequoia em um sistema com a seguinte configuração de hardware.

![macOS](https://img.shields.io/badge/macOS-Sequoia-brightgreen?style=flat-square&logo=apple)
![EFI](https://img.shields.io/badge/EFI-Hackintosh-blueviolet?style=flat-square&logo=apple)

## 📦 Hardware Compatível
| Componente         | Modelo                        |
| ------------------ | ----------------------------- |
| **Placa-mãe**      | ASUS TUF B360M-PLUS GAMING     |
| **Placa de Vídeo** | XFX RX 580 8GB                |
| **Memória RAM**    | 24 GB DDR4                    |
| **Processador**    | Intel Core i5-9400F     |

## 🚀 Pré-requisitos

- **macOS Sequoia** instalado ou pronto para instalação.
- Configuração adequada do OpenCore, contida neste repositório.
- Conhecimento básico em Hackintosh e instalação de sistemas operacionais.

## 🔧 Configurações de BIOS

Antes de iniciar o processo de instalação, certifique-se de aplicar as seguintes configurações na BIOS da sua placa-mãe:

- AHCI **Sata Mode**
- Desativar **CFG Lock**
- Ativar **Above 4G Decoding**
- Definir **XHCI Hand-off** como **Enabled**
- Definir **Secure Boot** como **OTHER OS**

## 🖥️ Funcionalidades

### Funcionando:

- [x] Aceleração de GPU (RX 580 8GB)
- [x] Áudio, Ethernet e USB
- [x] Sleep/Wake


### A serem ajustadas:

- [ ] Bluetooth (testar adaptador compatível)
- [ ] NVMe (Ainda devo fazer o teste)

## 📂 Como Usar

1. Clone ou baixe este repositório.
```bash
git clone https://github.com/jamaglian/TUF-B360M-PLUS-GAMING-HACKINTOSH.git
```
2. Copie a pasta `EFI` para o diretório raiz do seu pendrive de instalação macOS.
3. Ajuste as configurações específicas do seu sistema no arquivo `config.plist` usando a ferramenta [OCAuxiliaryTools](https://github.com/ic005k/OCAuxiliaryTools/releases) ou a que preferir.
4. Lembre-se de ajustar as configurações de SystemProductName, MLB, SystemSerialNumber e SystemUUID, o OCAuxiliaryTools pode gerar para você mas garanta que o serial é inválido no site da Apple.

## ⚠️ Aviso
Este projeto é voltado para uso pessoal e educativo. Não me responsabilizo por danos ao hardware ou software.

## 📚 Referências
Aqui estão alguns repositórios de referência que foram utilizados para configurar este Hackintosh:

- Baseado no repositório
  - [Repo guilhermeHenry](https://github.com/guilhermeHenry/EFI-Hackintosh-ASUS-TUF-B360M-PLUS-GAMINGBR)
- OpenCore
  - [Guide](https://dortania.github.io/OpenCore-Install-Guide/)
  - [Source](https://github.com/acidanthera/OpenCorePkg)
- Ferramenta de Configuração
  - [OCAuxiliaryTools](https://github.com/ic005k/OCAuxiliaryTools/releases)
- Kexts
  - [Lilu.kext](https://github.com/acidanthera/Lilu/releases)
  - [IntelMausi.kext](https://github.com/acidanthera/IntelMausi/releases)
  - [VirtualSMC.kext](https://github.com/acidanthera/VirtualSMC/releases)
  - [WhateverGreen.kext](https://github.com/acidanthera/whatevergreen/releases)
  - [SMCProcessor.kext](https://github.com/acidanthera/VirtualSMC/releases)
  - [SMCSuperIO.kext](https://github.com/acidanthera/VirtualSMC/releases)
  - [AppleALC.kext](https://github.com/acidanthera/AppleALC/releases)