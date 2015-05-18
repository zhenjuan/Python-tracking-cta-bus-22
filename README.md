# Python-tracking-cta-bus-22
#using urlopen to get information of bus 22 in City of Chicago

#code starts after this line

import urllib.request
import webbrowser

u=urllib.request.urlopen('http://ctabustracker.com/bustime/map/getBusesForRoute.jsp?route=22')
data = u.read()
f=open('rt22.xml', 'wb')
f.write(data)
f.close()
