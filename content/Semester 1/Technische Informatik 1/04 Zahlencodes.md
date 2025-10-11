## Tetraden-Codes
- Binärcode der eine Zahl **ziffernweise** codiert
- **Hilft** dabei die **Skalierbarkeit zu erhalten** und **Rechnungen zu vereinfachen** (siehe 7-Segment-Anzeige) 
- **Jede Ziffer** ist **4 Bits breit (Tetrade)**. Es werden **6 Pseudo-Tetraden nicht verwendet** da wir nur 0-9 benötigen 
- **Eine Tetrade ist** so zusagen **eine Dezimalziffer**

![[Pasted image 20251006175720.png | 300]]

## Am häufigsten verwendeten Codes:
![[Pasted image 20251006175904.png]]

## BCD-Code (Binary Coded Decimal)
- Der am häufigsten verwendete Code
- Weißt Bits innerhalb der Tetrade die Wertigkeiten 8, 4, 2 und 1 zu
- Wird deswegen auch 8421-Code genannt
- Wir können Dezimalzahlen darstellen, indem wir sie zuerst in Binär umwandeln und anschließend in mehrere 4 Bit Tetraden umwandeln und mit Nullen ergänzen, wenn nötig
- Es können bei der Addition Fehler entstehen falls das Ergebnis > 9 ist also eine Pseudo-Tetrade ensteht
	- Kann durch eine Korrektur behoben werden indem man 0110 dazu addiert (Korrektur-Tetrade)

## Stibitz-Code 
- Bitmuster um 3 verschoben
	- somit symmetrisch
- Subtraktionen sind einfacher zwischen Stibitz-Codes
- Pseudo Tetrade lautet 0000
- Bitstellen haben jedoch keine Wertigkeit mehr
	- Konvertierung ins Binärzahlensystem viel schwieriger
	- Ergebnis aus Addition kann 2 Tetraden beeinhalten
		- Wert muss um 3 vergrößert werden
	- Ansonsten muss um 3 verringert werden bei nur einem Überlauf für Korrektur