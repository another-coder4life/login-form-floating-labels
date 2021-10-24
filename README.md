# Login Form with Floating Labels

## Step-by-Step Video:

[YouTube-Link => Login form with floating labels](https://youtu.be/bWXruudrOsM)

## Source Code:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Login</title>
        <style>
            body {
                margin: 0;
                padding: 0;
                background: #3e3e3e;
                display: flex;
                justify-content: center;
                align-items: center;
                height: 100vh;
                color: #ffffff;
                font-family: Arial, Helvetica, sans-serif;
            }

            .login-container {
                background: #191919;
                padding: 1rem;
                width: 50%;
                text-align: center;
            }

            .login-container h1 {
                margin: 0 0 1rem 0;
                font-size: 2.5rem;
            }

            .login-container form {
                display: flex;
                flex-direction: column;
                margin: 0 auto;
                width: 50%;
            }

            .login-container form input {
                background: transparent;
                border: 0;
                border-bottom: 2px solid #ffffff;
                font-size: 1.5rem;
                width: 100%;
                color: #ffffff;
                outline: none;
            }

            .login-container form button {
                margin: 2rem auto 1rem auto;
                background: transparent;
                border: 2px solid #ffffff;
                border-radius: 4px;
                color: #ffffff;
                font-size: 1.5rem;
                padding: 0.5rem 3rem;
                cursor: pointer;
            }

            .label-group {
                position: relative;
                overflow: hidden;
                margin-top: 0.5rem;
            }

            .label-group input::placeholder {
                color: #191919;
            }

            .label-group > input,
            .label-group > label {
                padding: 1rem 0.75rem 0.5rem 0.75rem;
            }

            .label-group > label {
                position: absolute;
                top: 0;
                left: 0;
                display: block;
                margin-bottom: 0;
                transition: all 0.1s ease-in-out;
                text-align: left;
                cursor: text;
                font-size: 1rem;
            }

            .label-group input:not(:placeholder-shown),
            .label-group input:focus {
                padding-top: calc(1rem + 0.5rem * (2 / 3));
                padding-bottom: calc(0.5rem / 3);
            }

            .label-group input:not(:placeholder-shown) ~ label,
            .label-group input:focus ~ label {
                padding-top: calc(1rem / 3);
                padding-bottom: calc(0.5rem / 3);
                color: #aaaaaa;
            }
        </style>
    </head>
    <body>
        <div class="login-container">
            <h1>Login</h1>
            <form>
                <div class="label-group">
                    <input type="text" placeholder="Username" />
                    <label>Username</label>
                </div>
                <div class="label-group">
                    <input type="password" placeholder="Password" />
                    <label>Password</label>
                </div>
                <button>Submit</button>
            </form>
        </div>
    </body>
</html>
```
