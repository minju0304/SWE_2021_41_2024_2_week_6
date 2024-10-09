# SWE_2021_41_2024_2_week_6
## Week 4 Assignment
[week_4](https://github.com/minju0304/SWE_2021_41_2024_2_week4.git)
<pre></pre>
<code>
def isHappy(n):
  num = n
  seen = set()

  while n != 1 and n not in seen:
    seen.add(n)
    n = getsum(n)

  if(n==1):
    print("True")
  else :
    print("False")

  return

def getsum(n):
  sum = 0
  while n!=0:
    i=n%10
    sum += i*i
    n=n//10

  return sum

n = int(input())
isHappy(n)
</code>
</pre>
__orderd list__ ('-')
- download the colab notebook
- find happy num
---
## Week5 Assignment
<pre>
><code>
docker exec <ossp_container> cat /etc/os-release
</code>
  </pre>
*PRETTY_NAME="Ubuntu 24.04.1 LTS"/
NAME="Ubuntu"/
VERSION_ID="24.04" ... etc
><code>
docker exec <ossp_container> git --version
</code>
*git version 2.43.0
><code>
docker exec <ossp_container> python3 --version
</code>
*python3 version 3.12.3
><code>
docker inspect --format="(( .HostConfig.Binds }}" ossp-container 
</code>
*[/mnt/ossp_host_dir:/mnt/ossp_container_dir]
