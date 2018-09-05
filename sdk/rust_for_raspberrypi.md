
1. goto your home

```
cd ~/
```

2. make a dir for project

```
mkdir rust_rpi
```

3. download raspbian

```
wget http://downloads.raspberrypi.org/raspbian/images/raspbian-2017-04-10/2017-04-10-raspbian-jessie.zip
```

4. download kernel-qemu

```
wget https://github.com/dhruvvyas90/qemu-rpi-kernel/raw/master/kernel-qemu-4.4.34-jessie
```

5. install qemu

```
apt install qemu
```

6. start raspbian on your linux

```
qemu-system-arm -M versatilepb -cpu arm1176 -hda 2017-04-10-raspbian-jessie.img -kernel kernel-qemu-4.4.34-jessie -m 256 -append "root=/dev/sda2"
```

7. download RustSDK

```
git clone https://github.com/trustnotedevelopers/sdk_rust
```

8. install RustLanguage

```
curl https://sh.rustup.rs -sSf | sh
```

9. build sdk

```
cd sdk_rust
cargo build
```

10. get sdk (name:ttt)

ttt in sdk_rust/target/debug
