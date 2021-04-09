## WslRegisterDistribution failed with error: 0xc03a001a

When running `wsl --set-default-version 2`, you might get a:
```
Error: 0xc03a001a The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.
```
![image](https://user-images.githubusercontent.com/45776359/114172634-474fc700-990c-11eb-9687-39ff94dd2536.png)

To fix this issue, open the `File Explorer` and go to:
`C:\Users\<YOUR_USERNAME>\AppData\Local\Packages\CanonicalGroupLimited<SOMETHING>`

It should look something like this:
![image](https://user-images.githubusercontent.com/45776359/114173107-01473300-990d-11eb-81c6-9950d6315569.png)

Right click on `LocalState`, then `Properties`, then `Advanced`.

Ensure `Compress contents to save disk space` and `Encrypt contents to secure data` are both deselected.

Click `OK`, then `Apply`, then `Apply changes to this folder only`.

[Credits](https://simplernerd.com/wsl2-uncompressed/).