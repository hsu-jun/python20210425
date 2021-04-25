# 筆記

![註解 2021-04-25 142820](https://user-images.githubusercontent.com/70767105/115984210-6b7ff900-a5d8-11eb-9d38-be39408b117e.png)
![image](https://user-images.githubusercontent.com/70767105/115985467-91100100-a5de-11eb-8902-98f4bdfc0c7f.png)

# COUNT
from pwn import *

ip = "140.110.112.22"
port = 2403

r = remote(ip, port)

for i in range(1, 101):
	r.recvuntil("wave")
	r.recvuntil("?")
	r.sendline(str(i))

r.interactive()

# 3rd
不想用 python 寫得話就用線上排序大小www
https://miniwebtool.com/zh-tw/sort-numbers/

# Morse code
這題就利用線上翻譯工具
https://morsecode.world/international/translator.html

本人不太會Python，所以都居多用線上工具XDD

# hello world
只要先在linux裡面創建python檔案，之後輸入下面那段程式碼，再把ip與port套進去
![image](https://user-images.githubusercontent.com/70767105/115985985-d0d7e800-a5e0-11eb-8cfc-e2ae2ef613eb.png)

from pwn import *

ip = "140.110.112.22"
port = 24035
r = remote(ip, port)

r.interactive()
