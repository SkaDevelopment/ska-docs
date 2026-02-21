# 🛠️​ Installation

## Installation

1. Add this resource into your `resources/` folder.

    Place the resource folder inside your server’s:
    ```
    resources/
    ```
    Example:
    ```
    resources/[ska]/ska-traffic
    ```

2. Ensure it in your `server.cfg`.

    Add the following line to your server.cfg:
    ```
    ensure ska-traffic
    ```
    or:
    ```
    ensure [ska]
    ```
    
3. Adjust any required configuration inside `shared/config.lua`.

4. Restart Your Server

No additional dependencies required.

!!! info
    - Changes apply dynamically while players are connected
    - Works with all frameworks