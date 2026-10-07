# cyberDeck
Cataloging plans, schematics, code, and progress on prototype cyberdeck.
# 10/7/2026
-Exercise 5 means you're still early in C, so I'd start with a hardware-flavored learning path rather than the cyberdeck itself. I'm not familiar with that specific repo's exercises, so I'll go by the topics embedded work needs.

**Phase 1: Finish the C fundamentals (now)**
Keep going through the exercises, but make sure you get truly comfortable with these, because embedded C leans on them constantly:
- Pointers and pointer arithmetic (the biggest hurdle, so don't rush it)
- Arrays, strings, and structs
- Bitwise operators (`&`, `|`, `^`, `~`, `<<`, `>>`). Embedded work is full of setting and clearing register bits.
- Fixed-width types (`uint8_t`, `uint32_t`) and `volatile`
- Header files, multiple source files, and a basic Makefile

If the exercises don't cover bitwise operations or pointers well, supplement them yourself with small programs: for example, write functions that set, clear, and toggle bit N of a byte.

**Phase 2: Get a cheap board in your hands (around exercise 10 or whenever you feel ready)**
Buy a **Raspberry Pi Pico** (RP2040, about $5) or a Pico 2. Its documentation is excellent and it's forgiving for beginners. Then work through these in order:
1. Blink an LED using the Pico C SDK
2. Read a button, then debounce it in code
3. Print over UART/USB serial
4. Talk to an I2C sensor (a temperature or IMU breakout)
5. Drive a small SPI display
6. Use a timer interrupt instead of delay loops

Also buy a breadboard, jumper wires, a few LEDs, resistors, and tactile buttons. Total cost is roughly $25 to $30.

**Phase 3: Go deeper**
- Read a datasheet and write a driver for a sensor yourself, without a library
- Learn FreeRTOS basics (tasks and queues)
- Learn KiCad by designing a tiny breakout board and having it fabricated

**Phase 4: Your handheld**
By then you'll have the skills to prototype the real thing, and the project will go much more smoothly.

Resources that pair well with this: *Making Embedded Systems* by Elecia White, and the official "Getting started with Raspberry Pi Pico" guide.

What topics have the first few exercises covered so far? If you tell me, I can point out what to focus on next and suggest small hardware-style practice problems.
