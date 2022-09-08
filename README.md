# designated-verifier-zkp

The designated verifier circuit is a pluggable component that can be included to **add a designated verifier** inside any zk-SNARK. This means that the prover can choose the designated verifier. The prover will be able to convince only the designated verifier of the veracity of that proof. Everyone else accessing the *same proof* wouldn't be able to tell whether the proof was actually generated by the prover or forged by the designated verifer. 

Inspired by : 

- [Jordi Baylina - ZKP and SSI - Iden3](https://www.youtube.com/watch?v=Rd6SMShk7-c&t=998s)
- [Markus Jakobsson - Designated Verifier Proofs and Their Applications paper](http://markus-jakobsson.com/papers/jakobsson-eurocrypt96.pdf)

## Setup 

- Clone submodule
- Go into submodule
- Install the dependencies

## Key concept of Designated Verifier ZKproof

- [ ] Add explanation of the logic of the circuit "I prove that I know your private key or that I know X"

## Designated Verifier Signature ZKProof

- [ ] Add Miro illustration of circuit design

## Plug into your SNARK

- [ ] Add instructions about how to modify your current circuit to accomodate the SVZkp


## To do 

- [ ] Move function to support testing inside an utils folder 
- [ ] How can I access someone's publickey?
- [ ] Modify usage of message hash
- [ ] What is the sense of ff javascript?

Initial Tree => Leaves #1, #2, #3, #4 

Goal: Prover wants to prove that he/she knows a leaf included in the tree without revealing which one that is.

#1 Direction Prover to Designated Verifier => Leaf #1 belongs to the tree - Condition 1 verified. 
Prover knows Verifier's Private key - Condition 2 not verified 
Proof is valid => Verifier knows that the prover doesn't know his private key so he/she supposes that it must be verified for condition 1

#2 Direction Prover to Designated Verifier => Leaf #5 belongs to the tree - Condition 2 not verified

Combo 3 => verifier send an invalid proof to a third party => verified? I don’t know why?
Combo 4 => Verifier send a valid proof to a third party => Verified? I don't know why?





