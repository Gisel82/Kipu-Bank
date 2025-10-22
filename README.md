README 

DESCRIPCION DEL CONTRATO

KipuBank es un contrato inteligente permite a los usuarios depositar y retirar ETH en una bóveda personal, con restricciones de seguridad que incluyen:

Límite máximo por transacción de retiro representado por una variable inmutable
Aplica un límite global de depósitos.
Revertir con errores personalizados claros si no se cumple el Rechazo de depósitos vacíos o transferencias accidentales.
Registro de depósitos y retiros por usuario.
Uso de eventos, errores personalizados y transferencias seguras.
Características principales

✅ Depósitos de ETH en bóvedas individuales.
✅ Retiros limitados por transacción.
✅ Límite global de depósitos
✅ Seguridad reforzada: errores personalizados claros, Rechazo de transferencias directas de ETH y depositos vacios
✅ Eventos para depositos y retiros
✅ Contadores de la cantidad de depósitos y retiros por usuario.


 🚀 INSTRUCCIONES DE DESPLIEGE

Puedes desplegar KipuBank usando [Remix](https://remix.ethereum.org/) o otra herramienta como Foundry.

Despliegue en Remix

1. Abre Remix.
2. Crea un nuevo archivo `KipuBank.sol` y pega el código del contrato.
3. CompílALO con Solidity 0.8.30.
4. Ve a la pestaña "Deploy & Run transactions".
5. En el campo del constructor, ingresa:
   - "_maxRetiro": Límite de retiro por transacción (en wei).
   - "_totalDeposito": Capacidad total del banco (en wei).
6. Haz clic en "Deploy".


COMO INTERACTUO CON EL CONTRATO?

Deposita el ETH en la boveda llamando a "depositar()"  ,  wait contrato.depositar({ethers.utils.parseEther("0.10")});
Retira hasta un maximo permitido por transaccion,  await contrato.retirar({ethers.utils.parseEther("0.10")});
Consulta el saldo de cualquier usuario, const saldo = await contrato.consultarSaldo(MiDireccion);
Transferencias directas seran rechazadas
Seguridad Aplicada = errores personalizados y claros
