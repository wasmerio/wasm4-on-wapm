# WASM-4 on WAPM

This is an example repo showcasing how to publish your WASM-4 game as a package to WAPM.

## 1. Install Wasmer

```bash
curl https://get.wasmer.io -sSfL | sh
```

> For other installation instructions you can visit this page: https://github.com/wasmerio/wasmer-install

## 2. Open an account in WAPM

Open an account in [WAPM](https://wapm.io).

## 3. Login into the `wapm` CLI

You can login via two different ways:
* Credentials: `wapm login` will ask for your credentials
* Token: `wapm login {TOKEN}` will login with a token created in https://wapm.io/settings/access-tokens

## 4. Create the `wapm.toml`

You can use the reference [`wapm.toml`](https://github.com/wasmerio/wasm4-on-wapm/blob/main/wapm.toml) and update the details.
Don't forget it to put the proper name for the package `YOUR_USERNAME/THE_NAME_OF_THE_GAME` and a good description for it.

> Note: You can also type `wapm init` and follow the instructions (you will need to select the `WASM4` ABI)

## 5. Publish the package

Publish the package to wapm: `wapm publish`.
You need to execute this where the `wapm.toml` file is located.
