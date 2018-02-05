#!urs/bin/python3
#-*- coding: utf-8 -*-
import socket
import urllib.request
import urllib.parse
import requests
import codecs;

hdr = { 
		'Host':'119.160.218.5',
		'User-Agent':'Mozilla/5.0 (Windows NT 6.1) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/63.0.3239.132 Safari/537.36',
		'Accept':'text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8',
		'Accept-Encoding':'gzip, deflate',
		'Accept-Language':'en-US,en;q=0.9,th-TH;q=0.8,th;q=0.7',
		'Cookie':'PHPSESSID=f2121b712564730b733634b6df8f6959'
		}
		
DataErevenue = {'id_project':'ALL',
                'type_service':'ALL',
                'date_start':'01-08-2017',
                'date_end':'01-08-2017',
                'Submit':'Find'}

url = 'http://119.160.218.5/hlpdsk/menu.php';
values = {'username':'','password':'','submit':'Login'};
urlPercall = 'http://119.160.218.5/hlpdsk/helpdesk/report_by_supplier2.php';
data = urllib.parse.urlencode(values);
data = data.encode('UTF-8') # data should be bytes
req = urllib.request.Request(url, data)
data_login = urllib.parse.urlencode(DataErevenue);
data_login = data_login.encode('UTF-8');
req_content = urllib.request.Request(urlPercall, data_login,headers = hdr)
resp = urllib.request.urlopen(req_content);
con = resp.read();
h = con.decode('iso 8859-1');
#status = codecs.decode(con,encoding = 'iso 8859-1');
with open('222.html','wt',encoding = 'iso 8859-1') as out: 
	out.write(str(h));
	
#print(r);
