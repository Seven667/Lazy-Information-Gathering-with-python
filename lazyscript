import socket 
import sys
import os 
import re
import time
import urllib
import builtwith
import pythonwhois

#defining functions for operations 
def whois():
    result = socket.gethostbyname(url)

    print("Whois ========>> " , pythonwhois.get_whois(result));


def ping():
    result = os.system("ping -c 3 "+ url)
    if result == 0:
        print("***** server is up *****")
    else:
        print("****server is down**** ")


def port():
    for i in range(1,100):
        setting = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
        result =setting.connect_ex((url , i) )
        if result == 0 :
            print("Port %d : open " %  (i,))
        setting.close()
        


def email():
    result = urllib.urlopen(url).read()
    print re.findall("[\w]+@[\w]+",result)


def tech():
    print("Technology Used ====> ")
    print(builtwith.parse(url))

def dnsToIp():
    print socket.gethostbyname(url)



       


print("******************Coded By $even667 *******************\n\n")
#getting inputs from user
 
print("1 - Whois  2 - Connector checker \n3 - Port checker 4 - Email finder\n5 - Technology resolver  6 - dns to ip \n 7 - do the all thing at the time")

option = input("Number : ")
url = raw_input("Your Target url or DNS : ")

#something fun 
animation = "|/-\\"

for i in range(30):
    time.sleep(0.1)
    sys.stdout.write("\r" + animation[i % len(animation)])
    sys.stdout.flush()

#using switch for calling functions 

if option ==1:
    whois()

if option ==2:
    ping()

if option ==3:
    port()

if option ==4:
    email()

if option ==5:
    tech()

if option ==6:
    dnsToIp()



