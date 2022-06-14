# Minting NFT

## 创建一个account
```shell
solana-keygen new --no-bip39-passphrase -o /Users/mrzhao/.config/solana/nft-marketplace.json
```

## 创建一个token
```shell
# token: C1bcLasYDLwV3mSL5hW4g6SoYT324xxuyjnkpB3PvGPk
spl-token create-token
```

## 创建一个token account

```shell
# token account: CVKQJyZ7qNyKnxCMLbxEEpZkVh7iMzDLbfRUHRJ9V26L
spl-token create-account C1bcLasYDLwV3mSL5hW4g6SoYT324xxuyjnkpB3PvGPk
```

## Mint token

```shell
# Minting 1 tokens
  # Token: C1bcLasYDLwV3mSL5hW4g6SoYT324xxuyjnkpB3PvGPk
  # Recipient: CVKQJyZ7qNyKnxCMLbxEEpZkVh7iMzDLbfRUHRJ9V26L
# Signature: 4JVHG9vV7aWTbzAqTXZt7tWyfxLZ7Rvi6Prid4muSqUZuXc4yCvjswDCkNsk5d7VsUe4LpujgiMRoo2FiKuF7ZF8
spl-token mint C1bcLasYDLwV3mSL5hW4g6SoYT324xxuyjnkpB3PvGPk 1
```


## 创建一个NFT

```shell
# 创建一个NFT token
# Creating token GVLSu2CQSmwjVGA6RR9WPajKexnypnVJr4rhi6fCtm11
# Signature: 4QEjdvbU1DY7RvukstB4hpUhv6qjKYjd32Cf6xUY3dU7tyoLJ6RtfDSReRDFM95wnyYvBHrmVcTPWeCp465ar7dC
spl-token create-token --decimals 0
# 创建 token account
# Creating account iCfsp34d3WYuZWdRnXcPQ1v1AyHjP3Yf9Ec62kEEcAQ
# Signature: 8i9kTu9QtRzed929Hmfrgg1dKYiKbgo4VKi883V18sbsj1PEJLS6Eapdaau3mSCXo19fcMz6xrFZPFswK9s7YhA
spl-token create-account GVLSu2CQSmwjVGA6RR9WPajKexnypnVJr4rhi6fCtm11
# Mint token
#Minting 1 tokens
#  Token: GVLSu2CQSmwjVGA6RR9WPajKexnypnVJr4rhi6fCtm11
#  Recipient: iCfsp34d3WYuZWdRnXcPQ1v1AyHjP3Yf9Ec62kEEcAQ
#
#Signature: 5U5gfjocRncyNgkpGwjxg725gh2p7vGk4sLyh2gBzUbhuEJHTXgWdB9UMYXuLXVVbaEKNeSCEvQcSxpgQj4GrTXY
spl-token mint GVLSu2CQSmwjVGA6RR9WPajKexnypnVJr4rhi6fCtm11 1

# NFT token， disable supply
#Updating GVLSu2CQSmwjVGA6RR9WPajKexnypnVJr4rhi6fCtm11
#  Current mint authority: 4dnBoz37xCCLqZS6YGAZX128Hn4cis1Funh87x869xDE
#  New mint authority: disabled
#
#Signature: 4aw3gqDZ6hGMfgvFhHy3ssaQ2LrcfBmqR9StKB5eQLcSLgjyKtBKuwae3Pzk9GG1oZCQGmpXCbuE3GghyFvScxWJ
spl-token authorize GVLSu2CQSmwjVGA6RR9WPajKexnypnVJr4rhi6fCtm11 mint --disable
# 此时如果再对token执行mint操作的话会报错。
```