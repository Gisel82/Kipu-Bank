KipuBank - Contrato de Bóveda en Ethereum

KipuBank es un contrato inteligente permite a los usuarios depositar y retirar ETH en una bóveda personal, con restricciones de seguridad que incluyen:

- Límite máximo por transacción de retiro representado por una variable inmutable
- Aplica un límite global de depósitos.
- Revertir con errores personalizados claros si no se cumple el Rechazo de depósitos vacíos o transferencias accidentales.
- Registro de depósitos y retiros por usuario.
- Uso de eventos, errores personalizados y transferencias seguras.

 Características principales

- ✅ Depósitos de ETH en bóvedas individuales.
- ✅ Retiros limitados por transacción.
- ✅ Límite global de depósitos 
- ✅ Seguridad reforzada: errores personalizados claros, control de receive, .
- ✅ Eventos para depositos y retiros
- ✅ Contadores de la cantidad de depósitos y retiros por usuario.

Como interactuo con el contrato?

- Deposita el ETH en la boveda
  await contrato.depositar({ethers.utils.parseEther("0.10")});
- Retira hasta un maximo permitido por transaccion
  await contrato.retirar({ethers.utils.parseEther("0.10")});
- Consulta el saldo de cualquier usuario
  const saldo = await contrato.consultarSaldo(MiDireccion);
- Transferencias directas seran rechazadas
- Seguridad Aplicada = require - errores personalizados y claros 
