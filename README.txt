# LABORATORIO KALI LINUX - FILE DI TEST

Materiale didattico per esercitazioni locali e autorizzate.

## 1. Preparazione
Estrai l'archivio in una cartella di lavoro.
Apri il terminale Kali Linux.
Entra nella cartella del laboratorio con cd.
Controlla la posizione con pwd.
Visualizza il contenuto con ls -lah.

## 2. File inclusi
logs/access.log: 200 righe di accessi web simulati.
logs/system.log: 200 righe di eventi di sistema simulati.
data/utenti.csv: intestazione e 200 record sintetici.
data/eventi.txt: 200 righe di eventi classificati.
data/messaggi_duplicati.txt: 200 righe con messaggi ripetuti.
data/hosts_lab.txt: 200 host dimostrativi non reali.
config/app_v1.conf: 200 parametri di configurazione.
config/app_v2.conf: 200 parametri con alcune differenze.

## 3. Esercizi con head
head logs/access.log
head -n 20 logs/access.log
head -n 5 data/utenti.csv
head -n 10 data/eventi.txt
Osserva come head mostra le prime righe.

## 4. Esercizi con tail
tail logs/system.log
tail -n 15 logs/system.log
tail -n 8 data/messaggi_duplicati.txt
tail -f logs/system.log
Interrompi tail -f con CTRL+C.

## 5. Esercizi con wc
wc logs/access.log
wc -l logs/system.log
wc -w data/eventi.txt
wc -c data/utenti.csv
wc -l config/app_v1.conf config/app_v2.conf
Ricorda: wc -l conta le righe.

## 6. Esercizi con sort
sort data/eventi.txt
sort -r data/eventi.txt
sort data/messaggi_duplicati.txt
sort -t, -k2 data/utenti.csv
sort -n -t, -k1 data/utenti.csv

## 7. Esercizi con uniq
sort data/messaggi_duplicati.txt | uniq
sort data/messaggi_duplicati.txt | uniq -c
sort data/messaggi_duplicati.txt | uniq -d
sort data/messaggi_duplicati.txt | uniq -u
Nota: uniq confronta righe adiacenti.

## 8. Esercizi con grep
grep 'ERROR' logs/system.log
grep -i 'warning' logs/system.log
grep -n '401' logs/access.log
grep -c 'ERROR' logs/system.log
grep -E '401|403|404' logs/access.log
grep -v 'INFO' logs/system.log
grep -R 'parametro_088' config/

## 9. Esercizi con find
find . -type f
find . -type f -name '*.log'
find . -type f -name '*.csv'
find . -type f -size +1k
find data/ -type f
find config/ -type f -name '*.conf'

## 10. Esercizi con diff
diff -u config/app_v1.conf config/app_v2.conf
diff -q config/app_v1.conf config/app_v2.conf
Individua le righe modificate.

## 11. Esercizi con history
history
history | tail -n 20
history | grep 'grep'
La cronologia dipende dai comandi eseguiti nella tua sessione.

## 12. Combinazioni utili
grep 'ERROR' logs/system.log | wc -l
grep '401' logs/access.log | sort
sort data/eventi.txt | uniq -c
find . -type f | sort
grep -i 'ssh' logs/system.log | tail -n 10

## 13. Salvataggio dei risultati
mkdir -p risultati
grep 'ERROR' logs/system.log > risultati/errori.txt
sort data/messaggi_duplicati.txt | uniq -c > risultati/conteggi.txt
diff -u config/app_v1.conf config/app_v2.conf > risultati/differenze.txt
wc -l risultati/*.txt

## 14. Regole del laboratorio
Usa questi file solo per esercitazioni didattiche.
I dati sono sintetici e non identificano persone reali.
Non eseguire scansioni o test su reti di terzi senza autorizzazione.
Non modificare file di sistema per svolgere questi esercizi.
Lavora nella cartella estratta del laboratorio.
Prima di sovrascrivere un file, verifica il percorso.

## 15. Verifica finale
Conta le righe di ogni file con wc -l.
Confronta app_v1.conf e app_v2.conf con diff.
Trova tutti gli errori con grep.
Ordina i messaggi e conta i duplicati.
Individua tutti i file .log con find.
Scrivi un breve report con i risultati ottenuti.

Fine della guida rapida.
Esercizio aggiuntivo 017: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 018: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 019: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 020: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 021: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 022: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 023: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 024: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 025: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 026: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 027: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 028: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 029: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 030: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 031: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 032: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 033: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 034: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 035: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 036: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 037: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 038: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 039: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 040: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 041: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 042: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 043: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 044: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 045: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 046: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 047: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 048: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 049: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 050: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 051: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 052: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 053: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 054: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 055: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 056: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 057: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 058: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 059: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 060: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 061: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 062: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 063: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 064: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 065: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 066: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 067: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 068: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 069: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 070: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 071: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 072: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 073: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 074: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 075: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 076: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 077: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 078: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 079: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 080: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 081: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 082: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 083: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 084: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 085: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 086: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 087: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 088: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 089: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 090: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 091: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 092: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 093: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 094: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 095: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 096: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 097: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 098: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 099: ripeti un comando su un file diverso e annota il risultato.
Esercizio aggiuntivo 100: ripeti un comando su un file diverso e annota il risultato.
