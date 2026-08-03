# OVERTURE-FPGA
An implementation of the OVERTURE ISA from the video game Turing Complete, made in the digital logic simulator Digital. I test it on my Tang Nano 20K.
There is a bug in the Verilog where the first press of NEXT does nothing, but not in the simulation. There is a constant that is labeled next to the NEXT input to enable/disable this.
OVERTURE_TOP adapts the rest of the project for my specific setup. It is inadvisable that you use it. The HDL exports have the constant mentioned above set to 1, changing it should be easy or just re-export it from Digital.
A basic assembler is available at https://hlorenzi.github.io/customasm/web/?code=%23ruledef%0A%7B%0A%09or%20%3D>%200b01000000%0A%09nand%20%3D>%200b01000001%0A%09nor%20%3D>%200b01000010%0A%09and%20%3D>%200b01000011%0A%09add%20%3D>%200b01000100%0A%09sub%20%3D>%200b01000101%0A%09nop%20%3D>%200b11000000%0A%09jeq%20%3D>%200b11000001%0A%09jle%20%3D>%200b11000010%0A%09jleeq%20%3D>%200b11000011%0A%09jmp%20%3D>%200b11000100%0A%09jneq%20%3D>%200b11000101%0A%09jgeq%20%3D>%200b11000110%0A%09load%2C%20%7Bvalue%7D%20%3D>%200b00%20%40%20value%606%0A%09copy%2C%20r%7Ba%7D%2C%20r%7Bb%7D%20%3D>%200b10%20%40%20a%603%20%40%20b%603%0A%7D%0A%0A%0A%0A

Digital: https://github.com/hneemann/Digital
Planned Features:
256 bytes of RAM
