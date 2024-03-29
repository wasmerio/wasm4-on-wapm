# WASM-4 on WAPM

This is an example repo showcasing how to publish your WASM-4 game as a package to WAPM.

> All packages properly tagged and showing up on https://wapm.io/interface/wasm4 will opt-in for the prize of the [WASM-4 Jam #2](https://itch.io/jam/wasm4-v2)

## 1. Install Wasmer

```bash
curl https://get.wasmer.io -sSfL | sh
```

> For other installation instructions you can visit this page: https://github.com/wasmerio/wasmer-install


*Note: If you have Wasmer already installed, make sure that your wapm version is 0.5.5 or greater. Any new installation of Wasmer will install the latest version of WAPM*

```
wapm --version 
```

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

Example `wapm.toml` file:

```toml
[package]
name = "{YOUR_USERNAME}/my-game"
version = "0.1.4"
description = "This is my awesome game"
readme = "README.md"
repository = "https://github.com/..."

[[module]]
name = "game"
source = "game.wasm"
abi = "wasm4"
interfaces = { wasm4 = "0.0.1" }

[[command]]
runner = "wasm4@0.0.1"
name = "play"
module = "game"
```

## 5. Create a README.md file

Next to your `wapm.toml`, create a file named `README.md`.

This will help other people to see instructions or any other useful insights about your game.

## 6. Publish the package

Publish the package to wapm:

```
wapm publish
```

You need to execute this where the `wapm.toml` file is located.
