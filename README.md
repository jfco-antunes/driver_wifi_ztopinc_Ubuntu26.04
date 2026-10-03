# ZTOP Wi-Fi Linux Driver (ZT9101 / ZT714)

Driver para interfaces Wi-Fi baseadas no chipset ZTOP (ZT9101/ZT714).

## Origem e Licença
- **Repositório Base:** [Codeberg - sallecta/driver_wifi_ztopinc](https://codeberg.org/sallecta/driver_wifi_ztopinc)
- **Copyright Original:** (c) 2021 Shandong ZTop Microelectronics Co., Ltd
- **Licença:** GNU General Public License v2 (GPL-2.0)

## Modificações e Compatibilidade
- Atualizado e adaptado para suporte a kernels Linux modernos (Kernel 6.8+ e 7.0+):
  - Correção das diretivas de pré-processador e flags de Kbuild (`ccflags-y`).
  - Substituição da API legada `del_timer` por `timer_delete`.
  - Adaptação das funções de `cfg80211_ops` para suporte a multi-link (`link_id`).
  - Compatibilidade com o callback de `shutdown` em `struct usb_driver`.

Build
make
Install
sudo insmod ./zt9101_ztopmac_usb.ko cfg=./wifi.cfg
Uninstall
sudo rmmod zt9101_ztopmac_usb.ko
