# t12seminar

Kasutusvaldkonnad:
1. veebi serverite rakendused
2. Android
3. Majanduses, serveri rakendus, kasutatakse pankades elektroonilistes kaubanduste süsteemides, asustus ja kinnitus süsteemides.
4. Tarkvara tööriistad (nt. Eclipse, Inetelli J Idea, Netbans IDE)
5. Andmemahulised tehnoloogiad (Apache's HBase ja Accumulo)
6. Teaduslikes rakendustes
7. J2ME Apps (Nokia ja Samsung, telefonimängud, Blu-Ray)

Käivitamise moodused:

Vaja on enamasti .jar
Paljud jar failid on jooksutatavad mitmetel operatsiooni süsteemidel, topelt-klikkides nende peal. 
Failis on kirjas detailid - milliseid Java classi faile jooksutada.

1. Topelt-klikk
2. Command line/terminal
3. Shell Scripts
(A shell script is a computer program designed to be run by the Unix shell, a command-line interpreter.)


#!/bin/sh
GPSDIR=/home/sven/Desktop/gps
PROXY=www-proxy
export JAVA_HOME=/usr/local/java/jdk1.6.0_04/
DCOPREF=`kdialog --title "Hole JOSM"  --progressbar "Hole JosmLatest" 100`
cd $GPSDIR
wget -N http://josm.openstreetmap.de/download/josm-latest.jar
dcop "$DCOPREF"  close
$JAVA_HOME/bin/java -Xmx1024M -DproxyHost=$PROXY -DproxyPort=8080 -jar josm-latest.jar
