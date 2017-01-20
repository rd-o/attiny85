name=ledblink
mmcu=attiny85

all: $(name).hex

$(name).o: $(name).c
	avr-gcc -Os -c -mmcu=$(mmcu) $^

$(name).hex: $(name).elf 
	avr-objcopy -O ihex -R .eeprom $^ $@
	avr-size $^


$(name).elf: $(name).o
	avr-gcc -mmcu=$(mmcu) $^ -o $@

up: $(name).hex
	sudo avrdude -F -c usbtiny -p t85 -U flash:w:$^

clean:
	rm $(name).hex $(name).elf $(name).o

