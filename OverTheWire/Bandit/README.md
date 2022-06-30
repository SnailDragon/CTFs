# Bandit

This is a collection of solutions to the [OverTheWire Bandit Challenges](https://overthewire.org/wargames/bandit/bandit0.html). Some have quick write-ups, some are just passwords. It's mostly for my recond keeping so the write-ups will probably be sparse.

# Password List:
1. boJ9jbbUNNfktd78OOpsqOltutMc3MY1
2. CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
3. UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
4. pIwrPrtPN36QITSp3EQaw936yaFoFgAB
5. koReBOKuIDDepwhWk7jZC0RTdopnAYKh
6. DXjZPULLxYr17uwoI01bNLQbtFemEgo7
7. HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
8. cvX2JJa4CFALtqS87jk27qwqGhBM9plV
9. UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
10. truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
11. IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
12. 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
13. 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL
14. 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
15. BfMYroe26WYalil77FoDi9qh59eK5xNr
16. cluFn7wTiGryunymYOu4RcffSxQluehd
17. [ssh-key17.txt](/OverTheWire/Bandit/ssh-key17.txt) ([Write-up](#bandit-16-to-17))

# Write-Ups

## Bandit 16 to 17:
Password: cluFn7wTiGryunymYOu4RcffSxQluehd

### Method:
First use nmap to scan the port range on localhost for service type:
nmap -p 31000-32000 -sV localhost
This should find a serive of "ssl/unknown" on port 31790. Then use openssl and s_client to connect to the port and get the RSA key for the next level: 
openssl s_client --connect localhost:31790

Found password: [ssh-key17.txt](/OverTheWire/Bandit/ssh-key17.txt)

## Bandit 17 to 18