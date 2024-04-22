## some orders
circom MiMC5Sponge.circom --wasm

then: input.json add some inputs

node ./MiMC5Sponge_js/generate_witness.js ./MiMC5Sponge_js/MiMC5Sponge.wasm input.json output.wtns
snarkjs wtns export json output.wtns output.json

## solidity

In output.json:

 "20477946113538319030857511878118876049165535131249240964536911889205139499294", output hash
 "238793157801341097593479208",key
 "290753982375871409709127895137914", input
 "81947871209538581094380931", input

so input:
[290753982375871409709127895137914, 81947871209538581094380931],238793157801341097593479208
output:
20477946113538319030857511878118876049165535131249240964536911889205139499294