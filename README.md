# cicd-fw-sdk

Assuming you have the Zephyr SDK & `west`:

```
west init -m https://github.com/goliothlabs/cicd-fw-sdk cicdsample
cd cicdsample/
west update -n -o=--depth=1
west zephyr-export
west blobs fetch hal_espressif
west build -b esp32_devkitc_wrover app/
west flash
west espressif monitor
```