# 🔥 Deflationary Token (DFT) - Tokenomics Avanzadas

## 💡 VISIÓN GENERAL (El factor 'WOW')
Este proyecto resuelve el problema de la **inflación de tokens** y la estabilidad de precios al implementar una mecánica de **quema automática (Burn-on-Transfer)**. Demuestra una comprensión avanzada de las Tokenomics.

## 🛠️ STACK TECNOLÓGICO
* **Lenguaje:** Solidity ^0.8.0
* **Estándar:** OpenZeppelin (ERC-20, Ownable)
* **Entorno de Pruebas:** Remix IDE

## ⚙️ FUNCIONALIDAD ÚNICA: DEFLACIÓN POR TRANSACCIÓN
La función interna `_transfer` ha sido sobrescrita para incluir una comisión deflacionaria del **1%** por cada envío:
1.  Se calcula el 1% de la transacción total.
2.  Esa comisión es **quemada** (destruida) enviándola a `address(0)`.
3.  Solo el 99% restante se transfiere al destinatario.
* **Impacto:** Reduce el suministro total con cada uso, incentivando la escasez.

## 🔗 DESPLIEGUE (TESTNET)
[Aquí añadirás el enlace de Etherscan cuando lo pruebes en la red.]

## ⚠️ NOTA TÉCNICA Y AMBIENTE DE DESARROLLO
El código está optimizado para Hardhat/Foundry. Al usar el entorno de Remix 1.4.0, se presentó un conflicto de versiones con las librerías base de OpenZeppelin (`ERC20.sol`), lo que impedía la compilación. El desarrollo se migrará a Hardhat (Bloque 6) para asegurar la compatibilidad y el testing exhaustivo.
