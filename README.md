# SERIAL-TRANSFER-OF-SINGLE-BYTE-CHARACTER-USING-8051-KEIL.-EMBEDDED-C-PROGRAM-

**AIM:** 

To write and execute Embedded C Program for Serial Transfer of Single Byte / Character using 8051 KEIL

**APPARATUS REQUIRED:**

Personal computer with Keil software

**PROGRAM:**

**(i)	Serial port transfer a character A**


ORG 00H
MOV TMOD, #20H
MOV TH1, #0FCH
MOV SCON, #40H
SETB TR1
MOV SBUF, #'B'
WAIT: JNB TI, WAIT
CLR TI
END

**(ii)	Serial port to Transfer a Message**

TMOD = 0x20;   // TIMER 1, MODE 2
TH1  = 0xFC;
SCON = 0x40;
TR1  = 1;
for (i = 0; i < 17; i++)
    {
  SBUF = msg[i];
 while (TI == 0);
  TI = 0;
   }
 while(1);
            }


**OUTPUT:**
![WhatsApp Image 2025-11-09 at 13 29 55_391c3bbd](https://github.com/user-attachments/assets/f2f5c1c8-a03d-4e8e-a305-f3e708d469b8)

![WhatsApp Image 2025-11-09 at 13 30 29_5f2c113b](https://github.com/user-attachments/assets/e9a0087f-d311-402a-9377-58b5773124b3)






**Result:**

Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
