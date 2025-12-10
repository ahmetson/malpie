# Malpie
Proof of Concept of the trustful yet anonymous cashback system using zero-knowledge proof.

It's a mobile app for the users to collect the casbacks and coupons. For the shops Malpie provides the zero-knowledge proof of the user data.

For more information, check this out:

https://www.youtube.com/embed/8gTu-eRWgV8?si=f8DaIqN79GjbH-Ed

1st prize winner: The best use of Polygon ID at [Chainlink Constellation](https://devpost.com/software/malpie)

## Installation

1. Create `.env` from `.env.example`.

2. Deploy the smartcontracts on the network.

```shell
cd smartcontracts/
npx hardhat run --network sepolia scripts/deploy.ts
```

3. Upon success, the script will show todo. Follow them up.

The second todo item requires setting of the smartcontract address.
Set it in the scripts/set_js_in_loyalty.ts.

4. Whitelist the shop.
The shop is registered in the loyalty system.

The whitelisted shop is able to announce loyalty points for the user.

Edit the `scripts/add_shop.ts`, then call: 

```shell
npx hardhat run --network sepolia scripts/add_shop.ts
```

5. Add the credential types.

Edit the `scripts/add_credential.ts`, then call:

```shell
npx hardhat run --network sepolia scripts/add_credential.ts
```

6. Announce User's loyalty points.

Edit the `scripts/announce_loyalty_points.ts`, then call:

```shell
npx hardhat run --network sepolia scripts/announce_loyalty_points.ts
```

7. Submit user data

Copy the receipt_id from the first announce_loyalty_points.
