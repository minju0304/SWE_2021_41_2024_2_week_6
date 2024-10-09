# SWE_2021_41_2024_2_week_6
## Week 4 Assignment
[week_4](https://github.com/minju0304/SWE_2021_41_2024_2_week4.git)
<pre>
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
- The code defines a function isHappy(n) that checks if a number is a "happy number," meaning it eventually reaches 1 when repeatedly replacing it with the sum of the squares of its digits. It uses a helper function getsum(n) to calculate the sum of the squares of the digits.
---
## Week5 Assignment

>  <code>
>docker exec <ossp_container> cat /etc/os-release
></code>
>  
>- PRETTY_NAME="Ubuntu 24.04.1 LTS"
>- NAME="Ubuntu"
>- VERSION_ID="24.04"
>- ... etc

<br>

><pre>
>  <code>
>docker exec <ossp_container> git --version
></code>
> </pre>
>- git version 2.43.0

<br>

><pre>
>  <code>
>docker exec <ossp_container> python3 --version
></code>
>  </pre>
>- python3 version 3.12.3

<br>

><pre>
>  <code>
>docker inspect --format="{{ .HostConfig.Binds }}" ossp-container 
></code>
></pre>
>- [/mnt/ossp_host_dir:/mnt/ossp_container_dir]

