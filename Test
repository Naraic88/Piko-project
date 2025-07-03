import 
time

import 
machine



pulse_count 
= 0

pulse_in 
= machine.Pin(14,
machine.Pin.IN,
machine.Pin.PULL_DOWN)



def 
pulse_handler(pin):

    global 
pulse_count

    pulse_count 
+= 1

    print("Pulse detected! Current count:",
pulse_count)

# insert logikk her for å skrive puls til fil. Mulig du burde ha skrive til fil logikk i while-loopen på bunnen av koden her.

# Hvis denne får 2 pulser etter hverandre så er jeg usikker på hvordan den håndterer skriving til fil, om den klarer å håndtere det.

# Kan f.eks. legge til en counter i while loop og når denne når 1000 (øker med 1 per sekund) så skriver du til fil.

# Ulempen er hvis scriptet crasher i mellom disse 1000 sekundene, da mister man jo data, man får vurdere.




pulse_in.irq(trigger=machine.Pin.IRQ_RISING,
handler=pulse_handler)

print("Initial pulse count:",
pulse_count)
while 
True:

    time.sleep(1)
