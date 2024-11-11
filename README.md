# AGO-section-control-UDP-7rel-7sw
AgOpenGps UDP section control with feedback and manual/auto mode. It has 7 outputs, 7 section switches, AUTO/MANUAL switch with LED.
AUTO mode allows to operate scections directly from AgOpenGPS. 
MANUAL mode allows to control section from switches. In this mode AgOpenGPS aplication is notyfied about sections current state.
Based on arduino nano board with ENC28J60 module (SPI + CS pin -> 10)

default pinout (can be modyfied in #define headers) 
    //switch definitions
    #define AUTO_SW A0  //switch for choosing between auto (with section control from AOG) and manual (operate by switches) modes 
    #define S1_SW A1    //section 1 manual switch
    #define S2_SW A2
    #define S3_SW A3
    #define S4_SW A4
    #define S5_SW A5
    #define S6_SW 0
    #define S7_SW 1

    //section output definitions
    #define S1_OUT 2    //section 1 output (for relay or other working element) 
    #define S2_OUT 3
    #define S3_OUT 4
    #define S4_OUT 5
    #define S5_OUT 6
    #define S6_OUT 7
    #define S7_OUT 8
    #define AGO_LED 9  //diode indicate usage of auto mode

On arduino nano pins 0 and 1 is also used for programing the board and UART debugging so every log about current state is put in to a commented. 
