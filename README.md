### Installation
- Clone this repo:
```bash
$ git clone --depth=1 https://github.com/metis-os/metis-grub
```
- Change directory
```bash
$ cd metis-grub
```

#### Manually
- Copy files to relevant directory
    
    - Latte
```bash
$ sudo/doas cp -r metis-grub-latte/source/metis-grub-latte/* /usr/share/grub/themes/
``` 
- For mocha
    - mocha
    
    ```bash
     $ sudo/doas cp -r metis-grub-latte/source/metis-grub-mocha/* /usr/share/grub/themes/
     ```
#### Using `PKGBUILD`

- change directory to the theme you want to install

***for eg: mocha***

```bash
$ cd metis-grub/metis-grub-mocha
```
- run `makepkg`
```bash
$ makepkg -f 
```
- Use pacman to install `.zst file`

```
$ sudo/doas pacman -U <zst file>
```
### `Grub` configuration
- add the following line to your `/etc/default/grub`
```bash
GRUB_THEME="/usr/share/grub/themes/metis-grub-mocha/theme.txt"
```
### Regenrating `grub configuration`
  ```bash
  $ sudo/doas grub-mkconfig -o /boot/grub/grub.cfg
  ```
