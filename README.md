# Cutecom

cutecom is a simple serial console.

# Rational

I was using screen on my mac which works perfectly fine. However recently I
have to use the USB to serial converter with baud rate 1500000 with FT232RL.
`screen` does not work at all, I also tried `minicom` with the same result.

Then I came across comtool, which works OK, however it is with the GUI, which
I am not fan of.

I need a screen like tool, which could be used with other tools like `script`,
or tmux. I failed to find this one in short time.

`comtool` is built on python, so it inspires me that the PySerial package under
python might be robust enough to support high baud rate. Hence I create this
tool in a few hours.

I also took sometime to create setup.py for easy installation and also this
README to record the story behind.

Hope it helps others.

# How to Install

After clone this repo, in the `cutecom` directory:

```
python3 setup.py install
```

This will install the tool `cutecom` as well as its dependencies and add the
`cutecom` to your "PATH".

# How to use

In any path, type `cutecom` will print how to use.

```
A simple serial console

Use: cutecom tty_device baudrate [output_file_name]
  tty_device: /dev/your_tty_device
  baudrate: 115200, 1500000, or others

Options:
output_file_name: save the printing to a file
```

# Disclaimer

I only tested on my macbook air and on python3 only. It only depends on popular
packages. So I believe it might also work on other platforms. But the Software
and code samples available are provided "as is" without warranty of any kind,
either express or implied. Use at your own risk.
