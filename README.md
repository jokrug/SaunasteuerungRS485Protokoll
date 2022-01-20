# SaunasteuerungRS485Protokoll
Reengineering des RS485-Protokolls der Klein-Elektronik (weka) Saunasteuerung

Belegung RJ10-Buchse: von vorne auf Buchse gesehen, Arretierung unten, Kontakte oben:
Von links: 1: Masse, 2: RS485, 3: RS485, 4: +12V

38400 Baud 8N1
Binäres Protokoll
Blöcke zu 117 und 40 Bytes.
Sender sendet ein oder zwei Bytes, Empfänger quittiert mit 0x06 ACK.
Ein Block beginnt mit 0x84 und endet mit 0x80. Die 0x80 werden nicht quittiert.
