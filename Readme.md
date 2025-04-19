#Atomic-Swap

Swap two tokens between to address

#Build

stellar contract build 

#Deploy

 stellar contract deploy --wasm target/wasm32-unknown-unknown/release/soroban_atomic_swap_contract.wasm --source alice --network testnet --alias atomic_swap   

ℹ️  Simulating install transaction…
ℹ️  Signing transaction: 743ee9016f6394dee503dbc9711c12fa1838e428c0ec58801f4225cd54100c8c7
🌎 Submitting install transaction…
ℹ️  Using wasm hash c6106ac12b08a606ca8243babb00436b57fce4f80896deb61eb5f9c9867298bc
ℹ️  Simulating deploy transaction…
ℹ️  Transaction hash is f85b938ced0c95bf609002d50848a79fe13f6dd85b0bbffb85038cf3481066973
🔗 https://stellar.expert/explorer/testnet/tx/f85b938ced0c95bf609002d50848a79fe13f6dd85b0bbffb85038cf348106973
ℹ️  Signing transaction: f85b938ced0c95bf609002d50848a79fe13f6dd85b0bbffb85038cf3481006973
🌎 Submitting deploy transaction…
🔗 https://stellar.expert/explorer/testnet/contract/CCR4OCVAKSYG3MUN5CMEWVTQTGUE54SXHNO5NK6UUMGAY4LJLEMQ7FQV
✅ Deployed!
CCR4OCVAKSYG3MUN5CMEWVTQTGUE54SXHNO5NK6UUMGAY4LJLEMQ7FQV


#Call Method

stellar contract invoke \
  --id atomic_swap \
  --source alice \
  --network testnet \
  -- swap \
  --arg '{"address": "alice_address"}' \
  --arg '{"address": "bob_address"}' \
  --arg '{"address": "token_a_address"}' \
  --arg '{"address": "token_b_address"}' \
  --arg '1000' \
  --arg '4500' \
  --arg '5000' \
  --arg '950'


  stellar contract invoke --id atomic_swap --source alice --network testnet -- swap --a alice_address --b bob_address --token_a token_a_address --token_b token_b_address --amount_a 1000 --min_b_for_a 4500 --amount_b 5000 --min_a_for_b 950