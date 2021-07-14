# AD_EAEA

# code by ucybers

import socket

import sys

from time import *

from datetime import datetime

############################# https://youtube.com/c/ucybers

def banner () :

 print ("")

print(" \033[0;31m    ___   _____        _____       ___ ") 

print(" \033[0;32m   /   | |  _  \      | ____|     /   | ")

print(" \033[0;33m  / /| | | | | |      | |__      / /| | ")

print(" \033[0;34m / / | | | | | |      |  __|    / / | | ")

print(" \033[0;31m/_/  |_| |_____/      |_____|  /_/  |_| ")

print("               \033[0;31m EA\033[0;32mH\033[0;33mO\033[0;34mIQ\033[0;39m39                         ")

print("                \033[0;31mAHMEDIQ                                    ")

#############################

ip=input ("===> ENTER YOUR IP TO START: ")

t1=datetime.now()

print("Scanning Start.. %s Please wait.. "%ip)

sleep(1)

#################################

try:

     for port in range(1,6553):

        s=socket.socket(socket.AF_INET,socket.SOCK_STREAM)

        if(s.connect_ex((ip,port))==0):

            try:            

                serv=socket.getservbyport(port)

            except socket.error:

                serv="Unknown Service"

            print ("Port %s Open Service:%s "%(port,serv))

        t2=datetime.now()

        t3=t2-t1

     print ("Scanning Completed Om %s"%t3)

except  keyboardInterrupt:

    print("See You Soon....!")

#################################

