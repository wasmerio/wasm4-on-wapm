# WASM-4 on WAPM

This is an example repo showcasing how to publish your WASM-4 package to WAPM.

## 1. Install Wasmer

```bash
curl https://get.wasmer.io -sSfL | sh
```

> For other installation instructions you can visit this page: https://github.com/wasmerio/wasmer-install

## 2. Open a WAPM account

Open an account in [WAPM](https://wapm.io).

## 3. Login into the wapm cli

You can login via two different ways:
* Credentials: `wapm login` will ask for your credentials
* Token: `wapm login {TOKEN}` will login with a token created in https://wapm.io/settings/access-tokens

## 4. Create the `wapm.toml`

You can use the reference file and update, or Update the `wapm.toml` with your the name of the package `YOUR_USERNAME/THE_NAME_OF_THE_GAME`.

You can also type `wapm init` and follow the instructions (you will need to select the `WASM4` ABI)

## 5. Publish the package

Publish the package to wapm: `wapm publish`.
You need to execute this where the `wapm.toml` file is located.
