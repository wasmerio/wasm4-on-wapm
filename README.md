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
* Credentials:

  ```
  wapm login
  ```

  Note: this method will not work if you have registered with a social account and haven't set
  a password.

* Token:

  ```
  wapm login {TOKEN}
  ```
  
  You can login with any token created in https://wapm.io/settings/access-tokens

## 4. Create the `wapm.toml`

You can use the reference [`wapm.toml`](https://github.com/wasmerio/wasm4-on-wapm/blob/main/wapm.toml) and update the details.

Don't forget it to put the proper name for the package `YOUR_USERNAME/THE_NAME_OF_THE_GAME` and a good description for it.

> Note: You can also type `wapm init` and follow the instructions (you will need to select the `WASM4` ABI)

## 5. Create a README.md file

Next to your `wapm.toml`, create a file named `README.md`.

This will help other people to see instructions or any other useful insights about your game.

## 6. Publish the package

Publish the package to wapm:

```
wapm publish
```

You need to execute this where the `wapm.toml` file is located.
