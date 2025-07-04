# ⌨️ KeeBoard: A Custom Mechanical, CNC, RGB Backlight and Sleek finished Gasket mounted Keyboard 🔥
TOTAL TIME SPENT:
65 hours over 15 days
<hr>

## Day 1: Reasearch and planning.
OKay i decided to make a keyboard for fathers day as a gift. I aim for it to be wireless, have a compact and cool look, be fully cnc machined, and have creamy switches with a gasket mounted backlighted rgb keyboard. Spoiler: later I remove the wireless thing :(

I would be making a wireless one with the Adafruit Feather nRF52840 Express with kmk firmware. I first researched on how to make a keyboard, because i dint know anything about keyboards... I decided i would go with the geatron milky yellow pro switches and a gasket mount system. I thought i will also be adding an oled display but later on i reomve it because of gpio issues. todays day was fully of research and planning. i saw many tutorial videos to see where to get started. for now i just create a lyout in KLE and i have some 65% kyboard thingy with weirdly 1.25u arrow keys bruh.
![image](https://github.com/user-attachments/assets/3c12860e-5cb8-4664-9707-234c51e3310b)

Thanks to [@Daamin](https://hackclub.slack.com/team/U07GLQY6UN4) for helping me choosemy keycaps and stabs:
(Durock Smokey Stabs)[https://stackskb.com/store/durock-smokey-screw-in-stabilizers-v2/]
And these very cool blaze gradient keycaps:
(Veekos gradient keycaps)[https://stackskb.com/store/veekos-gradient-keycaps-cherry-profile-135-keys/]
![image](https://github.com/user-attachments/assets/4640afb0-7f92-4437-9c7d-4a0f1808b596)
🔥 ikr
Thats all for today...

## Day 2: Yeah..
Today is the day i released the adafruit mcu doesnt have enough gpios for my keyboard.
I decided to use qmk firmware which also supports standalone chips like the ATmega32u4 chip. i would basiclly making my mcu on my keyboard pcb which would make routing more harder and if anything goes wrong i have to order a new pcb bruh.
And yeah. this means no wireless connectivity.
Now i created my keyboard matrix for the routing whihc i can refer to.
![image](https://github.com/user-attachments/assets/3f8e8825-5fb8-4ef8-aae2-488b1059e150)
These shows the rowas and columns which i can use to see how many gpios i have to use.
Also because of less space i will be using ws2812b-2020 which is basically the small ws2812 neopixels.
Okay and i have started a bit fo my schematic 😭 yeah tmrw im cooked 💀

## Day 3: Schematic day 💩
Bruh the chip has like a 400 page datasheet whcih shows how i cna wire the schmatic. hopefully i ttook some help from the unterent and some ctrl+f's on the datasheet and i am almost doing the schematic properly. bruh
I added a crystal and most of the power of usb wiring to my keyboard.

## Day 4-6: Schematic Redo and some pcb design started
Okay bruh dont ask.
I struggled to make the standalone chip to work with everything and i am finally done. i have also wired like some 90 neopixels for my keyboard.
Another problem was that neopixels are very power hungry especially with many of them. so i had to add big tatalum capcitors like after 15 every 15 neopixels because the usb c only provides about 900mA iirc.
Here is a quick Look:

![image](https://github.com/user-attachments/assets/e8fec772-86a5-438f-95e4-b467b34085aa)
![image](https://github.com/user-attachments/assets/a3203061-4a57-425a-9aa8-095cf2447e47)

OKay it might bebad but yeah.
I started assign the symbols to footprints of parts ill get from lcsc

![image](https://github.com/user-attachments/assets/b64f6914-9c1a-44a5-b7f8-1c109626971e)

I realized component selection will take a long long time..

## Day 7: PCB Day
Started making my pcb as soon as i come back from school(5pm).
First i got the drawing of the plate file from ai03 plate generator of my kle layout.
Then i put it into kicad's pcb editor and started placing all the keys.
And also i put the USB.

## Day 8-10: PCB Grinding day.
I made almost the whole pcb. i connected the keys in a matrix with diodes. i also put all the leds. the routing was pretty hectic. i had to use so mayn vias nad like i have routing going from one side to another side of keyboard.  

![image](https://github.com/user-attachments/assets/9d10bc8b-0a4e-4fa8-a7d4-01cfc95cb7d4)

In the end i put all of the nopeixels. bruh this was the worstt i has to connect the dout pin of neopixels from the right side neopixels to the din pin of the left side neopixels and there were aleady so many routes in between.
check this img if you wanna know what i mean.

![image](https://github.com/user-attachments/assets/aee0fdb7-e083-4a00-aa34-61085a0c143a)

Once i was done with this you will notice the biggest mistake an engineer will do:
I FORGOT TO PUT THE STABILIZERS. and like no components can be under the screw in stabilizers and i had like components on the stabilizers drill holes. i had to reroute almsot everything around that and redo stuff.
bruh yeah its 12:10pm
🌙 imma go sleep.

## Day 11: Final pcb edge cut edits and 3d modeling started for keyboard.
I have started modeling the keyboard after fixing some issues with my pcb design and i have no errors in DRC or ERC.
Now, first i went through some tutorials on them designing keyboards and i was very donfused on how i could mount the keyboard.
If i just put 4 holes in the corners and screw the ocb in then the pcb would be felxy in the middle not giving enough balance. so i decided to gasket mount the entire keyboard.(i hope it works)
I first started designing the top plate.
ANd then i was exhausted so i started doing it tmrw.

## Day 12-15
I finished my top plate which look svery cool and complact. also i have done the gasket mounting things.
I have started making my bottom plate and the encoder.
Also a nice touch i added is that i have a custom ccnced like small plate on my black cnc keyboard which will glow light in the holes making it more cool:

![image](https://github.com/user-attachments/assets/19e85a07-16af-440e-a78e-9c86ee7195b5)

Yeah and i finished some silly mistakes and also added a 5 degree tilt to my keyboard so my wrist will be much better.
I mean it looks sick but i hope everything fits together properly.

Here is the final thing:

![image](https://github.com/user-attachments/assets/395beb5a-8896-4f48-bc64-f2323be01f60)
![image](https://github.com/user-attachments/assets/6c43854a-185b-41a5-a901-12056fd9e421)
![image](https://github.com/user-attachments/assets/074ee52b-9d52-4a0c-b587-1ad383ade981)

Now with the designign finished i had to make my bom and do my github things.
I SWEAR THIS IS THE MOST BORING PART TO DO.

Okay im done. now submitting it in the highway pitstop channel!

Thanks!
IK either te keboard looks bad or i made 1000 mistakes.
btw thanks to alex ren!

